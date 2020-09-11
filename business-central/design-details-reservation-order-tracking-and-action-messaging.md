---
    title: Design Details - Reservation, Order Tracking, and Action Messaging | Microsoft Docs
    description: The reservations system is comprehensive and includes the interrelated and parallel features of Order Tracking and Action Messaging.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: design, replenishment, reordering
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Detaily návrhu: Rezervace, sledování zásilky a zasílání zpráv
Rezervační systém je komplexní a zahrnuje vzájemně propojené a paralelní funkce sledování zakázky a zasílání zpráv o akci.

Jádrem rezervačního systému je propojení položky poptávky a odpovídající položky dodávky, a to buď prostřednictvím rezervace nebo pomocí sledování zakázky. Rezervace je odkaz vygenerovaný uživatelem a záznam sledování objednávky je odkaz vygenerovaný systémem. Množství položky, které je zadáno v rezervačním systému, je buď rezervováno, nebo sledováno, ale ne obojí současně. Způsob, jakým systémy zpracovávají položku závisí na tom, jak je položka nastavena.

Rezervační systém spolupracuje se systémem plánování vytvořením zpráv o akcích na plánovacích řádcích během spuštění plánování. Zprávu akce lze považovat za přílohu záznamu sledování objednávky. Zprávy o akci, ať už jsou vytvořeny dynamicky při plánování objednávek nebo během plánování, poskytují pohodlný nástroj pro efektivní plánování zásobování.

> [!NOTE]
> Rezervovaná množství jsou plánovacím systémem ignorována, to znamená, že pevné propojení mezi nabídkou a poptávkou nelze plánováním změnit.

Rezervační systém také tvoří strukturální základ pro systém sledování zboží. Pro více informací navštivte [Detaily návrhu: Sledování zboží](design-details-item-tracking.md).

Pro bližší informace o tom, jak funguje rezervační systém, navštivte dokument "Tabulka položky rezervace" na [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348).

## Rezervace
Rezervace je pevné spojení, které mezi sebou propojuje konkrétní požadavek a konkrétní nabídku. Toto propojení přímo ovlivňuje následnou skladovou transakci a zajišťuje správné vyrovnání položek zboží za účelem výpočtu nákladů. Rezervace přepíše výchozí způsob kalkulace položky. Další informace naleznete v části “Detaily návrhu: Metody ocenění”.

Stránka **Rezervace** je přístupná ze všech řádků objednávky typu poptávky i typu dodávky. Na této stránce může uživatel určit, kterou položku poptávky nebo dodávky chcete propojit pomocí rezervace. Rezervace se skládá z dvojice záznamů, které sdílejí stejné číslo položky. Jeden záznam má záporné znaménko a ukazuje na poptávku. Druhý záznam má pozitivní znaménko a ukazuje na nabídku. Tyto záznamy jsou uloženy v tabulce **Položka rezervace** s hodnotou stavu **Rezervace**. Uživatel může zobrazit všechny rezervace na stránce **Položky rezervace**.

### Zásobník v rezervacích
Rezervace jsou prováděny proti dostupným množstvím položek. Dostupnost zboží se počítá v základních termínech takto:

dostupné množství = zásoba + naplánované příjmy - hrubé požadavky

V následující tabulce jsou uvedeny podrobnosti o entitách sítě objednávek, které jsou součástí výpočtu dostupnosti.

||Pole v T27|Zdrojová tabulka|Filtr tabulky|Zdrojové pole|
|-|------------------|------------------|------------------|------------------|
|**Zásoby**|Zásoby|Položka zboží|N/A|Množství|
|**Naplánované příjmy**|Příjem pevně plán.zak.(množ.)|Řádek výrobní zakázky|=Pevně plánováno|Zůstatkové množ. (základ)|
|**Naplánované příjmy**|Příjem  vydané zakázky (množ.)|Řádek výrobní zakázky|=Uvolněno|Zůstatkové množ. (základ)|
|**Naplánované příjmy**|Množství v montážní zakázce|Hlavička montáže|=Objednávka|Zůstatkové množ. (základ)|
|**Naplánované příjmy**|Množ. na nák. objednávce|Řádek nákupu|=Objednávka|Zbýv.množství (základ)|
|**Naplánované příjmy**|Příjemka  obj. transf.(množ.)|Řádek transferu|N/A|Zbývající množství|
|**Celkové požadavky**|Množ. na prod.objednávce|Prodejní řádek|=Objednávka|Zbýv.množství (základ)|
|**Hrubé požadavky**|Plánovaná potřeba (množ.)|Komponenta výrobní zakázky|<>Stimulováno|Zůstatkové množ. (základ)|
|**Hrubé požadavky**|Množství  v montážní zakázce|Řádek montáže|=Objednávka|Zůstatkové množ. (základ)|
|**Hrubé požadavky**|Dodávka obj. transf.(množ.)|Řádek transferu|N/A|Zbývající množství|

Pro více informací navštivte [Detaily návrhu: Dostupnost ve skladu](design-details-availability-in-the-warehouse.md).

### Ruční rezervace
Když uživatel záměrně vytvoří rezervaci, získá plné vlastnictví a odpovědnost za tyto položky. To znamená, že uživatel musí také ručně změnit nebo zrušit rezervaci. Tyto ruční změny mohou způsobit automatickou úpravu souvisejících rezervací.

Následující tabulka ukazuje, kdy a jaké změny mohou nastat:

| Uživatelská akce | Reakce systému |
|-----------------|---------------------|  
| Snížení rezervovaného množství | Související pole množství jsou aktualizována. |
| Změna datových polí | Související datová jsou aktualizována.<br /><br /> **Note:** Pokud se datum splatnosti na požádání změní tak, aby předcházelo datu dodávky nebo datu splatnosti dodávky, rezervace je zrušena. |
| Odstranění objednávky | Rezervace je zrušena. |
| Změna umístění, přihrádky, varianty, sériového čísla nebo čísla šarže | Rezervace je zrušena. |

> [!NOTE]
> Funkce Pozdní vazba může také změnit rezervace, aniž by o tom informovala uživatele, přeskupením nespecifických rezervací sériových čísel nebo čísel šarží. Pro více informací navštivte “Detaily návrhu: Sledování a rezervace zboží”.

### Automatické rezervace
Kartu zboží lze nastavit tak, aby byla vždy automaticky rezervována z poptávky, například z prodejních objednávek. V takovém případě se provádí rezervace na zásoby, nákupní objednávky, objednávky sestavení a výrobní zakázky. Upozornění je vydáno, pokud je dodávka nedostatečná.

Kromě toho jsou položky automaticky rezervovány různými funkcemi plánování, aby byla poptávka spojena s konkrétní dodávkou. Položky sledování objednávky pro tyto odkazy plánování obsahují  **Rezervaci** v poli **Stav rezervace** v tabulce **Položka rezervace**. Automatické rezervace jsou vytvářeny v následujících situacích:

- Víceúrovňová výrobní zakázka, kde je pole **Způsob výroby** zapojených nadřazených a podřízených položek nastaveno na **Zhotovit na objednávku**. Systém plánování vytváří rezervace mezi nadřazenou výrobní zakázkou a podkladovými výrobní zakázky, aby bylo zajištěno, že jsou zpracovány společně. Taková vazba rezervace přepíše výchozí způsob výpočtu nákladů a způsob aplikace.

- Výrobní, montážní nebo nákupní objednávka, kde je pole **Způsob přiobjednání** příslušné položky nastaveno na **Objednávka**. Plánovací systém vytváří rezervace mezi poptávkou a plánovanou dodávkou, aby bylo zajištěno vytvoření konkrétní dodávky. Pro více informací navštivte [Objednávka](design-details-handling-reordering-policies.md#order).

- Výrobní zakázka vytvořená z prodejní objednávky s funkcí **Plánování prod.objednávky** je propojena s prodejní objednávkou s automatickou rezervací.

- Objednávka sestavy vytvořená automaticky pro řádek prodejní objednávky, aby se splnilo množství v poli **($ T_37_900 Qty. to Assemble to Order $)**. Tato automatická rezervace propojí prodejní poptávku a dodávku sestavy tak, aby procesory prodejních objednávek mohly přizpůsobit a slíbit položku sestavy přímo zákazníkovi. Kromě toho rezervace propojí výstup sestavy s řádkem prodejní objednávky s přepravní aktivitou, která splňuje objednávku zákazníka.

V případě nepřidělené nabídky nebo poptávky přidělí plánovací systém automaticky stav rezervace typu  **Přebytek**. To může způsobit poptávka, která je vytvořena díky předpokládanému množství nebo parametrem plánování zadaných uživatelem. Jedná se o legitimní přebytek, který systém uznává, a nevede k přijetí zpráv o akci. Přebytek by také mohl být skutečný, převis nabídky nebo poptávky, který zůstává nesledován. To je známka nerovnováhy v objednávkové síti, která způsobí, že systém vydává akční zprávy. Všimněte si, že zpráva akce, která naznačuje změnu množství, vždy odkazuje na typ **Přebytek**. Pro více informací navštivte v tomto tématu sekci “Příklad: Sledování zásilky v prodeji, výrobě a transferu".

Automatické rezervace, které jsou vytvořeny během plánování, jsou zpracovány následujícími způsoby:

- Jsou použity pro množství položek, které jsou součástí výpočtu dostupnosti, stejně jako ruční rezervace. Pro více informací navštivte v tomto tématu sekci "Zásobník v rezervacích”.

- Na rozdíl od ručně rezervovaného zboží jsou zahrnuty a případně změněny v následných plánovacích cyklech.

## Sledování zakázky
Sledování zakázky pomáhá plánovači udržovat platný plán dodávek tím, že poskytuje přehled o vyrovnání mezi poptávkou a dodávkou v síti objednávek. Záznamy sledování zakázek slouží jako základ pro vytváření dynamických akčních zpráv a řádků plánování během běh plánování.

> [!NOTE]
> Systém sledování zakázek odsadí dostupné zásob, jakmile jsou objednávky zadány do sítě objednávek. To znamená, že systém neupřednostňuje objednávky, které mohou být naléhavější z hlediska jejich data splatnosti. Je tedy na logice plánovacího systému nebo moudrosti plánovače, aby tyto priority smysluplně uspořádali.

> [!NOTE]
> Zásady sledování objednávek a funkce Získat hlášení akcí nejsou integrovány do úloh. To znamená, že poptávka související s úlohou není automaticky sledována. Vzhledem k tomu, že není sledována, může způsobit, že použití existujícího doplňování s informacemi o úloze bude sledováno k jiné poptávce, například k prodejní objednávce. V důsledku toho se můžete setkat se situací, ve které jsou vaše informace o dostupných zásobách nesynchronizované.

### Síť objednávek
Systém sledování objednávek je založen na principu, že síť objednávek musí být vždy ve stavu rovnováhy, ve kterém je každá poptávka, která vstupuje do systému, kompenzována odpovídající nabídkou a naopak. Tohle systém poskytuje pomocí identifikace logických vazeb mezi všemi položkami poptávky a nabídky v objednávkové síti.

Z této zásady vyplývá, že změna poptávky vede k odpovídající nerovnováze na straně nabídky v síti objednávek. Naopak změna nabídky vede k odpovídající nerovnováze na straně poptávky v síti objednávek. Ve skutečnosti je síť objednávek ve stavu konstantního toku, protože uživatelé zadávají, mění a odstraňují objednávky. Sledování zakázky zpracovává zakázky dynamicky a reaguje na každou změnu v okamžiku, kdy vstupuje do systému a stává se součástí sítě objednávek. Jakmile jsou vytvořeny nové záznamy sledování objednávek, je síť objednávek v rovnováze, ale pouze do doby, než dojde k další změně.

Aby se zvýšila transparentnost výpočtů v plánovacím systému, stránka **Nesledované prvky plánování** zobrazuje nesledované množství, které představuje rozdíl v množství mezi známou poptávkou a doporučenou nabídkou. Každý řádek na stránce odkazuje na příčinu nadměrného množství, například  **Hromadná objednávka**, **Úroveň pojistných zásob**, **Pevné přiobj.množ.**, **Minimální obj.množství**, **Zaokrouhlení**, nebo **Prodleva**.

### Posunování při sledování zakázky
Na rozdíl od rezervací, které lze provést pouze proti dostupným množstvím položek, je sledování objednávek možné u všech entit sítě objednávek, které jsou součástí výpočtu čistých požadavků plánovacího systému. Čisté požadavky se vypočítají takto:

čisté požadavky = hrubé požadavky + bod přiobjednání - naplánované příjmy - plánované příjmy - předpokládané dost.množ.

> [!NOTE]
> Poptávka související s prognózami nebo parametry plánování není sledována podle pořadí.

### Příklad: Sledování zásilky v prodeji, výrobě a transferu
Následující scénář ukazuje, které položky sledování objednávek jsou v tabulce  **Položka rezervace** vytvořeny jako výsledky různých změn sítě objednávek.

Předpokládejme následující data pro dvě zboží, které jsou nastaveny pro sledování objednávky.

|Zboží 1|Název|“Komponenta”|
|-|-|-|
||Dostupnost|100 jednotek v lokaci ČERVENÝ<br /><br />- 30 jednotek LOTA<br />- 70 jednotek LOTB|
|Zboží 2|Název|“Vyrobené zboží”|
||Výrobní kusovník|1 množ. za “komponentu”|
||Poptávka|Prodej za 100 jednotek na lokaci MODRÁ|
||Dodávka|Vydaná výrobní zakázka (generovaná s funkcí **Plánování prod.objednávky**  pro prodej 100 jednotek)|

Na stránce **Nastavení výroby**, pole **Komponenty na lokaci** je nastaveno na **ČERVENÁ**.

Následující položky sledování objednávky existují v tabulce **Položka rezervace** na základě dat v tabulce.

![Položky sledování objednávek v tabulce Položka rezervace](media/supply_planning_RTAM_1.png "supply_planning_RTAM_1")

### Vstupní čísla 8 a 9
Pro potřebu komponent pro LOTA a LOTB jsou vytvořeny odkazy sledování objednávek z poptávky v tabulce 5407, **Komponenta výrobní zakázky**, k dodání v tabulce 32, **Položka zboží**. Pole **Stav rezervace** obsahuje **Sledování**, které označuje, že tyto položky jsou dynamickými odkazy na sledování objednávek mezi nabídkou a poptávkou.

> [!NOTE]
> Pole **Číslo šarže** je na řádcích poptávky prázdné, protože čísla šarží nejsou specifikována na řádcích komponent vydané výrobní zakázky.

### Vstupní čísla 10
Z prodejní poptávky v tabulce 37, **Prodejní řádek**, je vytvořen odkaz sledování objednávek v tabulce 5406, **Řádek výrobní zakázky**. Pole **Stav rezervace** obsahuje **Rezervace**, a pole **Vazba** obsahuje **Zakázka-na-zakázku**. Je tomu tak proto, že uvolněná výrobní objednávka byla vytvořena speciálně pro prodejní objednávku a musí zůstat propojená na rozdíl od odkazů na sledování zakázek se stavem rezervace **Sledování**, které jsou vytvářeny a měněny dynamicky. Další informace naleznete v tomto tématu v části “Automatické rezervace”.

V tomto bodě scénáře je 100 jednotek LOTA a LOTB převedeno na lokaci MODRÝ převodním příkazem.

> [!NOTE]
> V tomto okamžiku se zaúčtuje pouze zásilka objednávky převodu, nikoli potvrzení.

Nyní existují následující položky sledování objednávky v tabulce **Položka rezervace**.

![Položka sledování objednávky v tabulce Položky rezervace](media/supply_planning_RTAM_2.png "supply_planning_RTAM_2")

### Vstupní čísla 8 a 9
Položky sledování objednávek pro dvě šarže komponentů odrážející poptávku v tabulce 5407  se změní ze stavu rezervace **Sledování** na **Přebytek**. Důvodem je, že dodávky, se kterými byly dříve spojeny, byly v tabulce 32 použity zásilkou převodního příkazu.

Skutečný přebytek, jako v tomto případě, odráží nadbytečnou nabídku nebo poptávku, která zůstává nevyřešena. Jedná se o známku nerovnováhy v síti objednávek, která vygeneruje zprávu o akci systémem plánování, pokud nebude dynamicky vyřešena.

### Vstupní čísla 12 až 16
Vzhledem k tomu, že dvě části komponenty jsou zaúčtovány na převodní příkaz jako dodané, ale ne přijaté, jsou všechny související položky sledování kladné objednávky typu rezervace **Nadbytek**, což znamená, že nejsou přiřazeny k žádným požadavkům. Pro každé číslo šarže se jeden záznam týká tabulky 5741, **Řádek transferu**, a jeden záznam se týká položky zboží v lokaci na cestě, kde nyní zboží existuje.

V tomto okamžiku ve scénáři je zaúčtováno pořadí převodu komponent z umístění MODRÝ do ČERVENÝ jako přijaté.

Nyní existují následující položky sledování objednávky v tabulce **Položka rezervace**.

![Položky sledování objednávek v tabulce Položka rezervace](media/supply_planning_RTAM_3.png "supply_planning_RTAM_3")

Položky pro sledování objednávek jsou nyní podobné prvnímu bodu ve scénáři, než byla objednávka přenosu zaúčtována pouze jako dodaná, kromě položek pro komponentu je nyní stav rezervace **Přebytek**. Je to proto, že potřeba komponenty je stále na lokaci ČERVENÝ, což odráží, že pole **Kód lokace** na řádku komponenty výrobní zakázky obsahuje **ČERVENÝ** jak je nastaveno na poli **Komponenty na lokaci**. Nabídka, která byla k této poptávce přidělena dříve, byla přenesena do lokace MODRÝ a nyní ji nelze plně sledovat, dokud nejsou změněny potřebné komponenty na řádku výrobní zakázky změnit na lokaci MODRÝ.

V tomto bodě scénáře je **Kód lokace** na řádku výrobní zakázky nastaven na **MODRÝ**. Kromě toho je na stránce **Řádky sledování zboží**, přiřazeno 30 jednotek LOTA a 70 jednotek LOTB k řádku výrobní zakázky.

Nyní existují následující položky sledování objednávky v tabulce **Položka rezervace**.

![Položky sledování objednávek v tabulce Položka rezervace](media/supply_planning_RTAM_4.png "supply_planning_RTAM_4")

### Vstupní čísla 21 a 22
Vzhledem k tomu, že potřebné komponenty byly změněny na lokaci MODRÝ a dodávka je k dispozici jako položka sledování zboží v lokaci BLUE, jsou všechny položky sledování objednávek pro dvě čísla šarží nyní plně sledovány, což je označeno stavem rezervace **Sledování**.

Pole **Číslo šarže** je nyní vyplněno v položce sledování objednávky pro tabulku 5407, protože čísla šarží byla přiřazena řádkům komponent výrobní zakázky.

Pro více příkladů o Položkách sledování objednávky v tabulce **Položka rezervace**, navštivte dokument “Tabulka položky rezervace” na [PartnerSource](https://go.microsoft.com/fwlink/?LinkId=258348) (vyžaduje přihlášení).

## Zprávy o akcích
Když systém sledování objednávek zjistí nerovnováhu v síti objednávek, automaticky vytvoří zprávu akce, která uživatele upozorní. Zprávy o akcích jsou systémem generované výzvy pro akce uživatele, které určují podrobnosti nerovnováhy a návrhy, jak obnovit rovnováhu v síti objednávek. Jsou zobrazeny jako plánovací řádky na stránce **Sešity plánování** když zvolíte **Získat hlášení akcí**. Kromě toho jsou zprávy o akcích zobrazeny na řádcích plánování, které jsou generovány spuštěním plánování, aby odrážely návrhy systému plánování, jak obnovit rovnováhu v síti objednávek. V obou případech se návrhy spustí v síti objednávek, když vyberete **Provést hlášené akce**.

Zpráva o akci adresuje vždy jednu úroveň kusovníku. Pokud uživatel přijme zprávu akce, může to vést k dalším zprávám akce na další úrovni kusovníku.

V následující tabulce jsou uvedeny existující zprávy akcí.

| Akční zpráva | Popis |
|--------------------|---------------------------------------|  
| **Změnit množství** | Změní množství na existující objednávce dodávky tak, aby pokrylo změněnou nebo novou poptávku. |
| **Přeplánování** | Přeplánuje datum splatnosti u stávající objednávky. |
| **Přeplán. změna množ.** | Přeplánuje termín splatnosti a změní množství u stávající objednávky. |
| **Nový** | Vytvoří novou objednávku, pokud poptávku nelze splnit některou z předchozích zpráv akce. |
| **Zrušit** | Zruší existující objednávku. |

Systém sledování objednávek se vždy pokouší vyřešit nerovnováhu ve stávající síti objednávek. Pokud to není možné, vydá akční zprávu k vytvoření nové objednávky. Následuje seznam priorit, který systém sledování objednávek používá, když určuje, jak obnovit rovnováhu. Pokud do sítě objednávek vstoupila další poptávka, systém se snaží sledovat objednávku pomocí následujících kontrol:

1. Zkontrolujte nadbytečnou nabídku ve stávajícím záznamu sledování objednávky pro tuto poptávku.
2. Zkontrolujte plánované a naplánované příjmy v pořadí podle data přijetí. Je vybráno poslední možné datum.
3. Kontrola dostupných zásoby.
4. Zkontrolujte, zda v aktuálním záznamu sledování objednávky existuje záznam sledování. Pokud ano, systém vydá zprávu akce typu **Změna** aby se zvýšila objednávka.
5. Zkontrolujte, zda v aktuálním záznamu sledování objednávky neexistuje žádná objednávka dodávky. Pokud ano, systém vydá zprávu akce typu **Nový** a vytvoří novou objednávku.

Otevřený požadavek prochází seznamem a odsune dostupnou dodávku v každém bodě. Všechny zbývající požadavky jsou vždy pokryty kontrolou 4 nebo kontrolou 5.

Pokud dojde ke snížení množství poptávky, systém sledování objednávek se pokusí vyřešit nerovnováhu provedením předchozích kontrol v opačném pořadí. To znamená, že existující zprávy akcí mohou být v případě potřeby změněny nebo dokonce odstraněny. Systém sledování objednávek uživateli vždy předkládá čistý výsledek jeho výpočtů.

## Sledování a plánování objednávek
Po spuštění systému plánování, odstraní všechny existující záznamy sledování objednávek a položky zpráv akcí a znovu je vytvoří jako návrhy řádků plánování podle párů nabídky a poptávky a priorit. Po dokončení plánovacího běhu je síť objednávek v rovnováze.

### Systém plánování versus Plánování objednávek a Zasílání zpráv o akci
Následující porovnání ukazuje rozdíly mezi metodami, které systém plánování používá k vytváření návrhů řádků plánování, a metodami, které systém sledování objednávek používá k vytváření záznamů sledování objednávek a zpráv akcí.

- Systém plánování se zabývá celým vzorem nabídky a poptávky konkrétní položky, zatímco sledování objednávek se zabývá objednávkou, která ji aktivovala.

- Systém plánování se zabývá všemi úrovněmi hierarchie kusovníku, zatímco sledování objednávek se zabývá vždy jednou úrovní kusovníku.

- Systém plánování vytváří vazby mezi poptávkou a nabídkou podle prioritního termínu splatnosti. Sledování objednávky vytváří vazby mezi poptávkou a nabídkou podle posloupnosti zadávání objednávek.

- Systém plánování bere v úvahu parametry plánování, zatímco sledování objednávek nikoli.

- Plánovací systém vytváří propojení v dávkovém režimu aktivovaném uživatelem, když vyrovnává poptávku a nabídku, zatímco sledování objednávek vytváří odkazy automaticky a dynamicky, když uživatel zadává objednávky.

## Viz také
[Detaily návrhu: Centrální koncepce plánovacího systému](design-details-central-concepts-of-the-planning-system.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)
