---
    title: Walkthrough - Selling, Assembling, and Shipping Kits | Microsoft Docs
    description: To support just-in-time inventory and the ability to customize products to customer requests, assembly orders can be automatically created and linked as soon as the sales order line is created. The link between the sales demand and the assembly supply enables sales order processors to customize the assembly item and promise delivery dates according to component availability. In addition, assembly consumption and output are posted automatically with the shipment of the linked sales order.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Návod: Prodejní, montážní a přepravní sestavy

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

Aby byla možná podpora zásob za běhu a aby bylo možné přizpůsobit produkty požadavkům zákazníků, lze montážní zakázky automaticky vytvořit a propojit, jakmile je vytvořen řádek prodejní objednávky. Spojení mezi prodejní poptávkou a dodávkou montáže umožňuje procesorům prodejní objednávky přizpůsobit zboží montáže a slíbit dodací termíny podle dostupnosti komponent. Kromě toho se spotřeba a výstup sestavy automaticky zaúčtují s dodávkou propojenou s prodejní objednávky.

Existuje speciální funkce, která reguluje přepravu množství montáže na zakázku, a to jak v základní, tak v pokročilé konfiguraci skladu. Když pracovníci odpovědní za montáž dokončí montáž dílů nebo veškerého množství montáže na zakázku, zaznamenají to do pole **K  dodání** v řádku dodávky ze skladu v pokročilých konfiguracích pak třeba zvolit možnost **Účtovat dodávku**. Výsledkem je zaúčtování odpovídajícího výstupu montáže, včetně spotřeby související komponenty, a zaúčtování prodejní dodávky pro množství pro propojenou prodejní objednávku. Tento návod ilustruje pokročilý skladový proces.

Když je v základních konfiguracích skladu připraveno množství k montáži na zakázku k odeslání, odpovědný pracovník skladu zaúčtuje vyskladnění skladu pro řádky prodejní objednávky. Tím se vytvoří pohyb zásob pro komponenty, zaúčtuje se výstup montáže a dodávka prodejní objednávky. Pro více informací navštivte [Zpracování zboží montáže na zakázku vo vyskladnění zásob](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## Návod
Tento návod ukazuje následující úkoly:

### Nastavení montáže zboží
Zboží montáže se vyznačuje systémem doplňování a kusovníkem montáže. Zásady montáže zboží mohou být buď montáž na objednávku (MNO), nebo montáž na sklad (MNS). Tato část zahrnuje následující úkoly:

- Nastavení příslušného doplňovacího systému a zásad montáže na nové kartě zboží montáže.
- Vytvoření kusovníku montáže se seznamem komponent montáže a zdrojů, které budou součástí zboží montáže.

### Prodej přizpůsobeného zboží montáže
[!INCLUDE[prod_short](includes/prod_short.md)] poskytuje flexibilitu pro zadávání množství skladu i množství montáže na zakázku na jednom řádku prodejní objednávky. Tato část zahrnuje následující úkoly:

- Vytvoření čisté řady prodejních objednávek MNO, kde není k dispozici celé množství a musí být před odesláním smontováno.
- Přizpůsobení zboží MNO.
- Přepočítání jednotkové ceny přizpůsobeného zboží montáže.
- Vytvoření řádku smíšené prodejní objednávky, kde je část prodejního množství poskytována ze skladu a zbývající část musí být před dodávkou sestavena.
- Principy upozornění na dostupnost MNO.

### Plánování zboží montáže
Poptávka montáže a nabídka jsou řešeny plánovacím systémem, stejně jako při nákupu, transferu a výrobě. Tato část zahrnuje následující úkoly:

- Spuštění regeneračního plánu pro zboží s prodejní poptávkou pro smontovanou nabídku.
- Generování montážní objednávky pro splnění množství prodejního řádku do požadovaného data dodání.

### Sestavování zboží
Montážní zakázky fungují podobným způsobem jako výrobní zakázky, očekávejte, že spotřeba a výstup budou zaznamenány a zaúčtovány přímo z objednávky. Když je zboží sestaveno do skladu, montážní pracovník má plný přístup ke všem polím záhlaví a samotného řádku. Když je zboží sestaveno do zakázky, kde je zákazníkovi přislíbeno množství a datum, pak některá pole v objednávce nelze upravovat. V takovém případě se zaúčtování montáže provádí ze skladové dodávky pro propojenou prodejní objednávku. Tato část popisuje následující úkoly.

- Zaznamenávání a účtování spotřeby a výstupu montáže na sklad.
- Přístup k řádku dodávky skladu z montážní objednávky MNO pro záznam montážních prací.
- Přístup k objednávce montáže MNO z řádku dodávky ze skladu a kontrola automaticky zadaných dat.

### Dodání zboží montáže ze skladu a zboží sestaveného na objednávku
K dispozici jsou speciální funkce, kterými se řídí dodání množství sestaveného na objednávku. Tato část zahrnuje následující úkoly:

- Vytvoření vyskladnění pro skladové zboží montáže a pro komponenty montáže, které mají být sestaveny před dodávkou.
- Registrace vyskladnění pro komponenty montáže a poté pro zboží montáže.
- Přístup k montážní zakázce ze skladové dodávky ke kontrole vybraných nebo spotřebovaných komponent.
- Dodání množství sestaveného na zakázku.
- Dodání skladového zboží montáže.

## Role
Tento návod ukazuje úkoly, které jsou prováděny následujícími uživatelskými rolemi:

- Zpracovatel prodejní objednávky
- Plánovač
- Montážní pracovník
- Skladník
- Odpovědná osoba za dopravu

## Předpoklady
Před provedením úkolů v návodu je nutné provést následující kroky:

- Nainstalujte [!INCLUDE[prod_short](includes/prod_short.md)].
- Vytvořte si zaměstnance skladu v lokaci BÍLÝ takto:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaměstnanci skladu** a poté vyberte související odkaz.
2. Vyberte pole **ID uživatele** a na stránce **Uživatelé** vyberte svůj vlastní uživatelský účet.
3. Do pole **Kód lokace** zadejte BÍLÝ.
4. Vyberte pole **Výchozí**.

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Připravte lokaci BÍLÝ pro zpracování montáže pomocí následujících kroků:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete kartu lokace pro lokaci BÍLÝ.
3. Na záložce **Přihrádky** zadejte do pole **Kód přihrádky na montáž** hodnotu **W-10-0001**.

   Zadáním tohoto nevybraného kódu přihrádky jsou všechny řádky montážní objednávky připraveny přijímat své komponenty do přihrádky.

4. Do pole **Kód přihrádky z montáže** zadejte **W-01-0001**.

   Zadáním tohoto kódu přihrádky vyskladnění se do přihrádky vyvede hotové zboží montáže.

Odeberte výchozí dodací lhůtu pro interní procesy pomocí těchto kroků:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení výroby** a poté vyberte související odkaz.
2. Na stránce **Nastavení výroby** na záložce **Plánování** odeberte hodnotu v poli **Výchozí bezp.průběžná doba**.

Vytvořte zásoby pro komponenty montáže pomocí [Přípravy ukázkových dat](walkthrough-selling-assembling-and-shipping-kits.md#prepare-sample-data).

## Příběh
Susan, zpracovatelka objednávky, převezme 23. ledna od společnosti Kutilka, s.r.o objednávku na tři jednotky Sady B, což je zboží MNO. Všechny tři jednotky jsou přizpůsobeny a musí obsahovat silnou grafickou kartu a další extra RAM. Diskové jednotky jsou upgradovány na DWD, protože jednotky CD nejsou k dispozici. Susan ví, že jednotky lze sestavit okamžitě, takže opouští navrhované datum dodání 23. ledna.

Současně si zákazník objedná patnáct jednotek sady A se speciálním požadavkem, aby pět jednotek bylo přizpůsobeno tak, aby obsahovaly silnou grafickou kartu. Ačkoli sada A je obvykle položkou montáže na sklad, procesor objednávky kombinuje množství prodejního řádku a prodává deset jednotek ze skladu a sestavuje pět přizpůsobených jednotek do objednávky. Deset jednotek sady A není k dispozici a musí být nejprve dodáno do skladu montážní zakázkou v souladu se zásadou montáže zboží. Susan se od montážního oddělení dozvídá, že jednotky sady A nemohou být dokončeny v aktuálním týdnu. Nastaví datum odeslání druhého řádku prodejní objednávky pro smíšené MNO a množství zásob na 27. ledna a informuje zákazníka, že 15 jednotek sady A bude odesláno o čtyři dny později než tři jednotky sady B. Do přepravního oddělení odešle upozornění, že tato prodejní objednávka vyžaduje zpracování montáže a vytvoří z prodejní objednávky doklad skladové zakázky.

Eduardo, plánovač, vede sešit plánování a generuje montážní zakázku pro deset standardních jednotek sady A s interním datem splatnosti 27. ledna.

Sammy, který je zodpovědný za přepravu, získá tři řádky dodávky ze skladu pro prodejní objednávku: jeden řádek pro tři čisté jednotky AMNO, jeden řádek pro pět jednotek MNO na řádku smíšené prodejní objednávky a jeden řádek pro deset jednotek MNS na řádku smíšené prodejní objednávky. Vytvoří doklad vyskladnění skladu pro všechny komponenty montáže, které jsou potřebné k sestavení celkem osmi jednotek MNO na dokladu dodávky ze skladu.

John, skladník, načte komponenty pro všechna množství MNO na dokladu dodávky ze skladu a přinese je do oblasti montáže. Zadá množství, které se má zpracovat, a zaregistruje vyskladnění skladu.

Linda sestavuje tři jednotky MNO sady B. Komponenty jsou již vyskladněny a nezaznamená množství výstupu a spotřeby ani nezaúčtuje objednávku, protože obě tyto akce jsou prováděny automaticky prostřednictvím souvisejících řádků dodávky ze skladu.

Sammy zaznamená sestavené množství na řádku dodávky ze skladu a zaúčtuje dodávku tří jednotek sady B. První řádek prodejní objednávky je aktualizován jako dodaný. Propojená montážní objednávka zůstane otevřená, dokud nebude prodejní objednávka plně fakturována. Dva řádky dodávky ze skladu, jedna MNO a jedna MNS, pro sadu A s daty splatnosti 27. ledna zůstávají otevřené.

Linda zpracovává 27. ledna dvě montážní objednávky na sadu A. První objednávkou je objednávka MNO na pět jednotek, kterou zpracovává jinak než objednávku MNO pro sadu B, kterou zpracovala 23. ledna. Na této objednávce je oprávněna k přístupu na řádek dodávky ze skladu, aby zaznamenála dokončené montážní práce. Potřebné komponenty jsou připraveny v montážním oddělení, protože byly vybrány společně s komponentami pro sadu B.

Druhá montážní objednávka je objednávka MNS pro deset jednotek, které byly vytvořeny plánovacím systémem. Na této objednávce MNS provede Linda všechny zúčastněné akce z montážní objednávky. Vytvoří doklad vyskladnění skladu pro komponenty montáže, které jsou potřebné k sestavení deseti jednotek. Když jsou počítače sestaveny, Linda zaúčtuje montážní objednávku a tím signalizuje, že zboží je k dispozici ve skladu a může být vyskladněno pro dodávku.

Sammy vytvoří doklad vyskladnění pro veškeré množství, které zůstane před zaúčtováním dodávky ze skladu. Doklad vyskladnění je vytvořen pro deset jednotek sady A, které se právě dokončili. Komponenty potřebné k sestavení pěti jednotek sady A na objednávku byly vyskladněny 23. ledna.

John přinese deset jednotek sady A ze skladu do určené oblasti expedice, zaznamená množství, které má být zpracováno, a pak zaregistruje vyskladnění.

Sammy zabalí deset jednotek MNS do pěti jednotek MNO, které Linda sestavila dříve během dne. Vyplní množství, které má být dodáno na obou řádncích, a poté zaúčtuje poslední dodávku pro Kutilka, s.r.o. Související montážní zakázka pro pět jednotek sady A je automaticky zaúčtována. Druhý řádek na prodejní objednávce je aktualizován tak, jak byl dodán. Dvě propojené montážní objednávky zůstávají otevřené, dokud není prodejní objednávka fakturována a uzavřena.

Když je prodejní objednávka později zaúčtována jako plně fakturovaná, prodejní objednávka a propojené montážní objednávky budou odstráněny.

## Příprava ukázkových dat

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky  zboží skladu** a poté vyberte související odkaz.
2. Vyberte pole **Název dávky** a poté vyberte výchozí deník.
3. Vytvořte kladné úpravy zásob v lokaci BÍLÝ k datu práce 23. ledna zadáním následujících informací.

   | **Číslo zboží** | **Kód zóny** | **Kód přihrádky** | **Množství** |
   |-----------------------------------|---------------------------------------|--------------------------------------|------------------------------------|  
   | 80001 | VYSKL | W-01-0001 | 20 |
   | 80005 | VYSKL | W-01-0001 | 20 |
   | 80011 | VYSKL | W-01-0001 | 20 |
   | 80014 | VYSKL | W-01-0001 | 20 |
   | 80203 | VYSKL | W-01-0001 | 20 |
   | 80209 | VYSKL | W-01-0001 | 20 |

4. Vyberte akci **Registrace** a pak zvolte tlačítko **Ano**.

   Dále synchronizujte nové položky skladu se zásobou.

5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky zboží** a poté vyberte související odkaz. Otevře se stránka **Deník zboží**.
6. Vyberte akci **Výpočet adjustace  skladu**.
7. Na stránce **Výpočet adjustace  skladu** klikněte na tlačítko **OK**.
8. Na stránce **Deník zboží** vyberte akci **Účtovat** a poté klikněte na tlačítko **Ano**.

### Vytváření zboží montáže

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vytvořte první zboží montáže na základě následujících informací.

   | Pole | Hodnota |
   |---------------------------------|-----------|  
   | **Popis** | Sada A – Základní PC |
   | **Základní měrná jednotka** | KS |
   | **Kód kategorie zboží** | Různé |
   | **Systém doplnění** | Montáž |
   | **Způsob montáže** | Montáž-na-sklad |
   | **Způsob přiobjednání** | Dávka-pro-dávku |

   > [!NOTE]  
   > Sada A je obvykle dodána pomocí montáže na sklad, a proto má způsob přiobjednání na to, aby se stala součástí obecného plánování zásobování.

4. Vyberte akci **Montáž** a poté vyberte **Kusovník montáže**.
5. Definujte kusovník montáže pro sadu A s následujícími informacemi.

   | **Typ** | **Číslo** | **Množství za** |
   |-------------------------------|------------------------------|---------------------------------------|  
   | Zboží | 80001 | 1 |
   | Zboží | 80011 | 1 |
   | Zboží | 80209 | 1 |
   | Zdroj | Linda | 1 |

6. Vytvořte druhou položku montáže na základě následujících informací.

   | Pole | Hodnota |
   |---------------------------------|-----------|  
   | **Popis** | Sada B – Profesionální PC |
   | **Základní měrná jednotka** | KS |
   | **Kód kategorie zboží** | Různé |
   | **Systém doplnění** | Montáž |
   | **Způsob montáže** | Montáž-na-zakázku |

   > [!NOTE]  
   > Sada B je obvykle dodávána pomocí montáže na zakázku, a proto nemá spůsob přiobjednání, protože by neměla být součástí obecného plánování zásobování.

7. Vyberte akci **Montáž** a poté vyberte **Kusovník montáže**.
8. Definujte kusovník montáže pro sadu B s následujícími informacemi.

   | **Typ** | **Číslo** | **Množství za** |
   |-------------------------------|------------------------------|---------------------------------------|  
   | Zboží | 80005 | 1 |
   | Zboží | 80014 | 1 |
   | Zboží | 80210 | 1 |
   | Zdroj | Linda | 1 |

### Prodej zboží montáže

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
2. Vyberte akci **Nový**.
3. Vytvořte dva řádky prodejní objednávky pro zákazníka 62000, Kutilka, s.r.o, k pracovnímu datu s následujícími informacemi.

   | **Typ** | **Popis** | **Množství** | Množství  k montáži na zakázku | Datum odeslání |
   |--------------|---------------------|------------------|-------------------------------|-------------------|  
   | Zboží | Sada B – Profesionální PC | 3 | 3 | 23. ledna |
   | Zboží | Sada A – Základní PC | 15 | 5 | 27. ledna |

   > [!NOTE]  
   > Pro řádek prodejní objednávky pro sadu B existuje následující problém s dostupností:
   >
   > - Součást montáže 80210 není k dispozici. To znamená, že tři zadané jednotky sady B nelze sestavit, jsou označeny hodnotou **0** v poli **Schopen montáže** na stránce **Dostupnost montáže**.
   >
   > Pro řádek prodejní objednávky pro sadu A existuje následující problém s dostupností:
   >
   > - Deset jednotek sady A není k dispozici. To znamená pro plánovací systém, že množství musí být smontováno do skladu.

   Dále přizpůsobte prodejní objednávku.

4. Vyberte řádek prodejní objednávky pro tři jednotky sady B.
5. Na záložce **Řádky** vyberte **Řádek** zvolte **Montáž na objednávku** a poté vyberte **Řádky montáže na zakázku**.
6. Na stránce **Řádky montáže na zakázku** na řádku montážní objednávky pro zboží 80014 zadejte **2** do pole **Množství za**.
7. Na řádku montážní objednávky pro zboží 80210 zvolte pole **Číslo** a místo toho vyberte položku 80209.
8. Vytvořte nový řádek montážní objednávky s následujícími informacemi.

   | Typ | Číslo | Množství za |
   |----------|---------|------------------|  
   | Zboží | 80203 | 1 |

9. Zavřete stránku **Řádky montáže na zakázku**.

   Dále aktualizujte jednotkovou cenu sady B podle přizpůsobení, které jste právě provedli. Všimněte si aktuální hodnoty pole **Jednotková cena bez  DPH**.

10. Na záložce **Řádky** zvolte  **Řádek** zvolte **Montáž na objednávku** a poté zvolte **Cena více úrovní**.
11. Vyberte tlačítko **Ano**. Všimněte si zvýšené hodnoty v poli **Jednotková cena bez  DPH**.
12. Vyberte řádek prodejní objednávky pro 15 jednotek sady A.
13. Na záložce **Řádky** vyberte **Řádek** zvolte **Montáž na objednávku** a poté vyberte **Řádky montáže na zakázku**.
14. Na stránce **Řádky montáže na zakázku** vytvořte nový řádek montážní zakázky s následujícími informacemi.

   | Typ | Číslo | Množství za |
   |----------|---------|------------------|  
   | Zboží | 80203 | 1 |

   Dále změňte datum dodávky druhého řádku prodejní objednávky podle plánu sestavení.

15. Do řádku prodejní objednávky pro 15 jednotek sady A zadejte **01-27-2014** do pole **Datum odeslání**.
16. Vyberte akci **Vydat**.
17. Vyberte akci **Vytvořit dodávku  ze skladu**.
18. Zavřete prodejní objednávku.

### Plánování nedostupného zboží MNS

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat<"), zvolte **Plánovací sešit** a poté vyberte související odkaz.
2. Vyberte akci **Vypočítat regenerační plán**.
3. Na stránce **Vypočítat plán** nastavte následující filtry.

   | Počáteční datum | Datum ukončení | Číslo |
   |-------------------|-----------------|---------|  
   | 01-23-2014 | 01-27-2014 | Sada A – Základní PC |

4. Zvolte tlačítko **OK**.

   Pro potřebnou montážní zakázku deseti jednotek, která má být splatná 27. ledna, je vytvořen nový řádek plánování. Nepotřebuje žádné změny, takže nyní můžete vytvořit objednávku.

5. Vyberte akci **Provést hlášené akce**.
6. Na stránce **Provést hlášení akce-pož.** vyberte pole **Objednávka sestavení** a poté vyberte **Vytvořit montážní zakázky**.
7. Zvolte tlačítko **OK**.

### Sestavení a dodání množství prvního MNO

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dodávka ze skladu** a poté vyberte související odkaz.

   > [!NOTE]  
   > V této části je osoba odpovědná za přepravu odpovědná za zaznamenávání dokončených montážních prací MNO na řádku dodávky ze skladu. K tomuto pracovnímu postupu může dojít v prostředích, kde montážní práce provádí osoba odpovědná za dopravu nebo montážní pracovníci v oblasti expedice.
   >
   > V této části se akce na montážní zakázce provádějí nepřímo z řádku dodávky ze skladu. Pro více informací o přímém zpracování montážní objednávky navštivte "Zboží montáže do skladu" v tomto návodu.

2. Otevřete nejnovější dodávku ze skladu, která je vytvořena na lokaci BÍLÝ.

   Všimněte si tří řádků dodávky ze skladu: Jeden řádek pro množství MNO sady B, splatné 23. ledna. Jeden řádek pro množství MNO sady A, splatné 27. ledna. Jeden řádek pro množství zásob sady A, splatné 27. ledna.

   Pole **Montáž na objednávku** určuje metodu montáže.

   Dále vytvořte doklad vyskladnění pro všechny komponenty sestavy MNO, které jsou potřebné pro dodávku ze skladu.

3. Vyberte akci **Vytvořit vyskladnění** a poté klikněte na tlačítko **OK**.

   Dále proveďte úlohu vyskladnění.

4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění** a poté vyberte související odkaz.
5. Otevřete doklad vyskladnění, který jste vytvořili v kroku 3 v této části.

   Všimněte si hodnoty v poli **Původní doklad** a toho, že všechny řádky vyskladnění jsou pro komponenty montáže.

   Dále zaregistrujte vyskladnění bez změny výchozích informací.

6. Zvolte akci **Automat.vyplnit množ. ke zprac.**.
7. Vyberte akci **Zápis vyskladnění**.

   Vraťte se k provádění úkolů dodání.

8. Znovu otevřete stránku **Dodávka ze skladu**.

   Všimněte si, že pole **Vyskladněné  množství** je na všech řádcích stále prázdné. Důvodem je to, že jste stále nevyskladnili zboží, které má být dodáno, ale pouze komponenty potřebné k sestavení množství MNO.

   Pokračujte kontrolou příslušné objednávky montáže.

9. Vyberte řádek dodávky pro tři jednotky sady B.
10. Na záložce **Řádky** zvolte **Řádek** a pak zvolte **Montáž na objednávku**. Otevře se stránka **Montážní zakázka**.

   Všimněte si, že několik polí v montážní zakázce není k dispozici, protože zakázka je propojena s prodejní objednávkou.

   Všimněte si, že na řádcích montážní zakázky, je pole **Vyskladněné  množství** vyplněno. To je způsobeno vyskladnění, který jste zaregistrovali v kroku 7 v této sekci.

11. Do pole **Množství k montáži** zkuste zadat libovolnou hodnotu nižší než **3**.

   Přečtěte si chybovou zprávu s vysvětlením, proč lze toto pole vyplnit pouze prostřednictvím pole **K  dodání** na související dodávce.

   Pole **Množství k montáži** je upravitelné pro podporu situací, kdy chcete částečně odeslat množství zásob namísto sestavení více jednotek do objednávky. Pro více informací navštivte sekci "Kombinované scénáře" v [Princip montáže na zakázku a montáže na sklad](assembly-assemble-to-order-or-assemble-to-stock.md).

12. Zavřete stránku **Montážní zakázka** a vraťte se na stránku **Dodávka ze skladu**.
13. Na řádku dodávky pro tři jednotky sady B, zadejte do pole **K  dodání** hodnotu **3**.
14. Vyberte akci **Účtovat dodávku** a poté klikněte na tlačítko **Dodat**.

   Spolu s tímto zaúčtováním dodávky ze skladu jsou zaúčtována úplná spotřeba a výstupní množství související objednávky sestavy a pole **Zbývající množství** je prázdné. Řádek prodejní objednávky pro sadu B je aktualizován tak, aby zobrazoval, že jsou dodány tři jednotky.

   Aktivity skladu pro splnění prvního řádku prodejní objednávky do 23. ledna jsou dokončeny. Dále proveďte řádky prodejní objednávky, které jsou dodávány 27. ledna

### Montáž a zaznamenání množství druhého MNO

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Montážní zakázky** a poté zvolte související odkaz.

   Všimněte si, že objednávka MNO pro dodané jednotky sady B je stále v seznamu, i když pole **Zbývající množství** je prázdné. Je to proto, že propojená prodejní objednávka stále není plně fakturována.

   > [!NOTE]  
   > V této části je montážní pracovník zodpovědný za zaznamenávání dokončených montážních prací MNO na řádku dodávky ze skladu. K tomuto pracovnímu postupu může dojít v prostředích, kde jsou montážní práce prováděny v samostatném montážním oddělení a montážní pracovníci jsou oprávněni změnit řádek dodávky ze skladu.

2. Otevřete montážní zakázku MNO pro pět jednotek sady A.

   Všimněte si, že pole **Množství k montáži** a **Množství ke spotřebě** jsou prázdná, protože zatím není zaznamenána žádná práce.

   Všimněte si, že na řádcích montážní zakázky, je pole **Vyskladněné  množství** vyplněno. To je způsobeno vyskladněním, které bylo zaregistrováno 23. ledna.

   Dále zaznamenejte, že je montážní objednávka dokončena.

3. Vyberte akci **Řádek dod. ze skladu  mont. zakázky**.
4. Na stránce **Řádek dod. ze skladu  mont. zakázky** do pole **K  dodání** zadejte **5** a poté stránku zavřete.

   Všimněte si na stránce **Montážní zakázky**, že pole  **Množství k montáži** a **Množství ke spotřebě** jsou nyní vyplněna množstvím výstupu a spotřeby, které budou zaúčtovány s dodávkou.

5. Zavřete stránku **Montážní zakázky**.

### Montáž množství MNS

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Montážní zakázky** a poté zvolte související odkaz.
2. Otevřete montážní objednávku pro deset jednotek sady A.

   Všimněte si, že pole **Množství k montáži** je vyplněno očekávaným množstvím.

   Dále vytvořte doklad vyskladnění pro načtení potřebných komponent.

3. Vyberte akci **Vydat**.
4. Vyberte akci **Vytvořit  vyskladnění** a klikněte na tlačítko **OK**.

   Dále proveďte úlohu vyskladnění.

5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění** a poté vyberte související odkaz.
6. Otevřete doklad vyskladnění, který jste vytvořili v kroku 4 v této části.

   Pokračujte v registraci vyskladnění bez změny výchozích informací.

7. Zvolte akci **Automat.vyplnit množ. ke zprac.**.
8. Vyberte akci **Zápis vyskladnění**.

   Vraťte se do montážní zakázky a proveďte poslední úkol montáže.

9. V **Montážní zakázce** vyberte akci **Účtovat** a poté klikněte na tlačítko **Ano**.

   Všimněte si, že montážní zakázka je odebrána ze seznamu otevřených zakázek.

### Dodání zbývajícího zboží, částečně ze skladu a částečně z montáže na zakázku

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dodávka ze skladu** a poté vyberte související odkaz.
2. Otevřete nejnovější dodávku ze skladu, která je vytvořena na lokaci BÍLÝ.

   Všimněte si na řádku pro deset jednotek sady A, že pole **K  dodání** a **Vyskladněné  množství** sou prázdná.

   Dále vyskladněte všechno zbývající zboží.

3. Vyberte akci **Vytvořit vyskladnění** a poté klikněte na tlačítko **OK**.

   Dále proveďte poslední úkol vyskladnění pro tuto skladovou dodávku.

4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění** a poté vyberte související odkaz.
5. Otevřete doklad vyskladnění, který jste vytvořili v kroku 3 v této části.

   Všimněte si, že tento doklad vyskladnění je pro zboží montáže, nikoli pro komponenty montáže.

   Dále zaregistrujte vyskladnění beze změny výchozích informací.

6. Zvolte akci **Automat.vyplnit množ. ke zprac.**.
7. Vyberte akci **Zápis vyskladnění** a poté klikněte na tlačítko **Ano**.

   Vraťte se do dodávky ze skladu a proveďte poslední úkol.

8. Znovu otevřete stránku **Dodávka ze skladu**.

   Na stránce **Dodávka ze skladu** na řádku pro deset jednotek sady A si všimněte, že pole **K  dodání** a **Vyskladněné  množství** nyní obsahují hodnotu **10**.

9. Vyberte akci **Účtovat dodávku** a zvolte **Dodat**.

   Dokument dodávky ze skladu je odebrán, což znamená, že příslušné aktivity skladu jsou dokončeny. Dále ověřte, že byla zpracována prodejní objednávka.

10. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
11. Otevřete prodejní objednávku pro Kutilka, s.r.o.

   Všimněte si, že pole **Dodané množství** obsahuje celé množství na obou řádcích.

   Když Kutilka, s.r.o. zaplatí za dodání 18 počítačů od společnosti CRONUS, prodejní objednávka a její propojené montážní zakázky budou odstraněny.

## Viz také
[Princip montáže na zakázku a montáže na sklad](assembly-assemble-to-order-or-assemble-to-stock.md)     
[Montáž zboží](assembly-how-to-assemble-items.md)     
[Vyskladnění zboží pro dodávku ze skladu](warehouse-how-to-pick-items-for-warehouse-shipment.md)     
[Prodej zboží montáže na obejdnávku](assembly-how-to-sell-items-assembled-to-order.md)     
[Montáž zboží](assembly-how-to-assemble-items.md)     
[Podrobnosti návrhu: Účtování montážní zakázky](design-details-assembly-order-posting.md)     
[Detaily návrhu: Vnitřní procesy skladu](design-details-internal-warehouse-flows.md)     
[Detaily návrhu: Výstupní procesy skladu](design-details-outbound-warehouse-flow.md)     
[Návod: Automatické plánování dodávek](walkthrough-planning-supplies-automatically.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]