---
    title: Design Details - Balancing Demand and Supply | Microsoft Docs
    description: To understand how the planning system works, it is necessary to understand the prioritized goals of the planning system, the most important of which are to ensure that any demand will be met by sufficient supply and any supply serves a purpose.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
#  Detaily návrhu: Vyvažování poptávky a nabídky
Abychom pochopili, jak plánovací systém funguje, je nutné porozumět prioritním cílům plánovacího systému, z nichž nejdůležitější je zajistit, aby:

- Jakákoli poptávka bude uspokojena dostatečnou nabídkou.
- Jakákoli dodávka slouží svému účelu.

Obecně lze těchto cílů dosáhnout vyvážením nabídky s poptávkou.

## Nabídka a poptávka
Poptávka je běžný termín používaný pro jakýkoli druh hrubé poptávky, jako je prodejní objednávka a potřeba komponent z výrobní zakázky. Kromě toho aplikace umožňuje více technických typů poptávky, jako jsou negativní zásoby a vratky.

Nabídka je běžný termín používaný pro jakýkoli druh kladného nebo příchozího množství, jako jsou zásoby, nákupy, montáže, výroba nebo vstupy transferu. Kromě toho, může vratka představovat také nabídku.

Aby bylo možné vyřešit mnoho zdrojů poptávky a nabídky, plánovací systém je uspořádá do dvou časových linií nazvaných profily zásob. Jeden profil obsahuje události poptávky a druhý obsahuje odpovídající události nabídky. Každá událost představuje jednu entitu sítě objednávky, například řádek prodejní objednávky, položka hlavní knihy nebo řádek výrobní zakázky.

Když jsou načteny profily zásob, jsou různé sady nabídky a poptávky vyváženy tak, aby vydávaly plán dodávek, který splňuje uvedené cíle.

Parametry plánování a úrovně zásob jsou další typy poptávky a nabídky, které procházejí integrovaným vyvážením k doplnění skladových položek. Pro více informací navštivte [Detaily návrhu: Zpracování způsobu přiobjednání](design-details-handling-reordering-policies.md).

## Koncept bilancování ve zkratce
Poptávka je udána zákazníky společnosti. Nabídka je to, co společnost může vyrobit a vytvořit rovnováhu. Plánovací systém začíná nezávislou poptávkou a pak odkazuje zpátky k nabídce.

Profily zásob se používají k tomu, aby obsahovaly informace o požadavcích, zásobách, množství a načasování. Tyto profily v podstatě tvoří obě strany vyvažovací stupnice.

Cílem plánovacího mechanismu je vyvážit poptávku a nabídku položky, aby bylo zajištěno, že nabídka bude proveditelným způsobem odpovídat poptávce, jak je definováno v plánovacích parametrech a pravidlech.

![Přehled vyrovnávání nabídky a poptávky](media/nav_app_supply_planning_2_balancing.png "Přehled vyrovnávání nabídky a poptávky")

## Vyřizování objednávek před datem zahájení plánování
Aby se zabránilo tomu, že plán dodávek ukazuje nemožné, a tudíž zbytečné návrhy, považuje systém plánování období až do data zahájení plánování jako zmrazenou zónu, kde se nic neplánuje. Pro zmrazenou zónu platí následující pravidlo:

Veškerá nabídka a poptávka před začátkem plánovacího období budou považovány za součást inventáře nebo odeslány.

Systém plánování proto až na několik výjimek nebude navrhovat žádné změny objednávek dodávek v zamrazené zóně a pro toto období nebudou vytvořeny ani udržovány žádné odkazy na sledování objednávek.

Výjimky z tohoto pravidla jsou následující:

* Pokud jsou předpokládané dostupné zásoby, včetně součtu nabídky a poptávky ve zmrazené zóně, pod nulou.
* Pokud jsou sériová čísla nebo čísla šarže požadována v zastaralých pokynech.
* Pokud je sada nabídky a poptávky propojena se zakázkou-na-zakázku.

Pokud jsou počáteční dostupné zásoby pod nulou, navrhne plánovací systém nouzovou objednávku dodávky den před plánovacím obdobím k pokrytí chybějícího množství. V důsledku toho budou plánované a dostupné zásoby vždy na počátku dalšího období plánování minimálně nulové. Řádek plánování pro tuto objednávku dodávky zobrazí ikonu nouzového varování a další informace se zobrazí při vyhledávání.

### Sériová čísla, čísla šarží a odkazy na objednávku jsou osvobozeny od zamrzlé zóny
Pokud je požadováno sériové číslo, číslo šarže, nebo existuje odkaz na objednávku, systém plánování ignoruje zmrazenou zónu a začlení taková množství, která jsou zpětně datována od počátečního data, a pokud nebudou synchronizovány poptávka a nabídka, případně navrhnou nápravná opatření. Hlavním obchodním důvodem pro použití tohoto principu je, že konkrétní sady poptávky a nabídky se musí shodovat, aby bylo zajištěno splnění této konkrétní poptávky.

## Načítání profilů zásob
Chcete-li vyřešit mnoho zdrojů poptávky a nabídky, systém plánování je uspořádá na dvou časových osách nazývaných profily zásob.

Do každého profilu zásob se načtou běžné typy poptávky a nabídky s daty splatnosti v den zahájení plánování nebo po něm. Po načtení se různé typy poptávky a nabídky seřadí podle obecných priorit, jako je datum splatnosti, nízkoúrovňové kódy, umístění a varianta. Kromě toho jsou priority objednávek aplikovány na různé typy, aby bylo zajištěno, že nejdůležitější poptávka bude splněna jako první. Pro více informací navštivte [Stanovení priorit objednávek](design-details-balancing-demand-and-supply.md#prioritizing-orders).

Jak již bylo zmíněno dříve, poptávka může být také negativní. To znamená, že by se s ní mělo zacházet jako s dodávkou, avšak na rozdíl od běžných typů dodávky, se záporná poptávka považuje za pevnou dodávku. Systém plánování to může vzít v úvahu, ale nenavrhne žádné změny.

Obecně platí, že plánovací systém považuje všechny objednávky dodávek po datu zahájení plánování za předmět změny, aby vyhověl poptávce. Jakmile je však množství zaúčtováno z objednávky dodávky, systém plánování jej již nemůže změnit. Následující různé objednávky tedy nelze znovu naplánovat:

- Vydané výrobní zakázky, kde byla zaúčtována spotřeba nebo výstup.
- Montážní objednávky, kde byla zaúčtována spotřeba nebo výstup.
- Dodávky transferu, kde byla zaúčtována dodávka transferu.
- Nákupní objednávky, kde byla zaúčtována příjemka.

Kromě načítání typů poptávky a nabídky jsou určité typy načítány s důrazem na speciální pravidla a závislosti, které jsou popsány v následujícím textu.

### Dimenze položky jsou odděleny
Plán dodávek musí být vypočítán pro kombinaci dimenzí položky, jako je varianta a umístění. Neexistuje však žádný důvod k výpočtu jakékoli teoretické kombinace. Je třeba vypočítat pouze ty kombinace, které nesou poptávku nebo nabídku.

Plánovací systém to řídí spuštěním profilu zásob Když je nalezena nová kombinace, aplikace vytvoří záznam interního řízení přístupu, který obsahuje skutečné informace o kombinaci. Aplikace vloží SKJ jako řídící záznam nebo vnější smyčku. Ve výsledku jsou nastaveny správné plánovací parametry podle kombinace varianty a umístění a aplikace může pokračovat do vnitřní smyčky.

> [!NOTE]  
> Aplikace nevyžaduje, aby uživatel zadával záznam SKJ při zadávání poptávky, nebo nabídky pro konkrétní kombinaci varianty a lokací. Proto pokud skladová položka neexistuje pro danou kombinaci, aplikace vytvoří vlastní dočasný záznam SKJ na základě dat karty zboží. Pokud je na stránce Nastavení zásob nastaveno Lokace nutná na Ano, pak musí být vytvořena SKJ nebo pole Komponenty na lokaci nastaveno na Ano. Pro více informací navštivte [Detaily návrhu: Poptávka v prázdném skladu](design-details-demand-at-blank-location.md).

### Načítání sériových čísel a čísel šarží podle úrovně zadání
Atributy ve formě sériových čísel a čísel šarží jsou načteny do profilů zásob spolu s poptávkou a nabídkou, ke které jsou přiřazeny.

Atributy poptávky a nabídky jsou seřazeny podle priority objednávky a úrovně jejich specifikace. Vzhledem k tomu, že shody sériových čísel a čísel šarže odrážejí úroveň specifikace, bude konkrétnější poptávka, například číslo šarže vybraná speciálně pro řádek prodeje, hledat shodu před méně specifickou poptávkou, například prodej z libovolného vybraného čísla šarže.

> [!NOTE]  
> Pro sériové čísla a čísla šarží poptávky a nabídky neexistují žádná speciální pravidla upřednostňování, kromě úrovně specifikace definované jejich kombinací sériových čísel a čísel šarží a nastavení sledování položek u příslušných položek.

Během vyrovnávání považuje plánovací systém dodávku, která nese sériová čísla nebo čísla šarží, za nepružnou a nebude se pokoušet tyto objednávky na objednávku zvýšit nebo přeplánovat (pokud nejsou použity ve vztahu mezi zakázka na zakázku). Viz Propojení zakázky na zakázku není nikdy zrušeno). To chrání dodávky z přijímání několika, možná konfliktních, zpráv akcí při dodání, když nese různé atributy – například kolekce různých sériových čísel.

Dalším důvodem, proč jsou sériová a čísla šarže dodávky nepružná, je to, že sériová čísla a čísla šarží jsou obecně přiřazována tak pozdě v procesu, že by bylo matoucí, kdyby byly navrženy změny.

Vyvážení sériových čísel/čísel šarží nerespektuje *zmrazenou zónu*. Pokud poptávka a nabídka nejsou synchronizovány, plánovací systém navrhne změny nebo nové objednávky bez ohledu na počáteční datum plánování.

### Propojení zakázky na zakázku není nikdy zrušeno
Při plánování položky na zakázku nesmí být propojená nabídka použita pro jinou poptávku, než pro kterou byla původně určena. Propojená poptávka by neměla být pokryta žádnou jinou náhodnou nabídkou, i když je za své současné situace dostupná v čase a množství. Například montážní objednávku, která je propojena s prodejní objednávkou ve scénáři Montáž na zakázku, nelze použít k pokrytí jiné poptávky.

Poptávka a nabídka zakázky na zakázku se musí přesně vyvážit. Systém plánování zajistí dodávku za všech okolností bez ohledu na parametry velikosti objednávky, modifikátory a množství v inventáři (jiné než množství vztahující se k propojeným objednávkám). Ze stejného důvodu systém navrhne snížení nadbytečných dodávek, pokud se sníží související poptávka.

Toto vyvažování také ovlivňuje časování. Omezený horizont, který je dán intervalem dostupnosti, se nebere v potaz; pokud se změní načasování poptávky, bude nabídka přeplánována. Doba prodlevy však bude respektována a zabrání naplánování dodávek zakázek na zakázku, s výjimkou interních dodávek víceúrovňové výrobní zakázky (projektová objednávka).

> [!NOTE]  
> Sériová čísla a čísla šarží lze také určit na základě poptávky zakázky na zakázku. V takovém případě není dodávka standardně považována za nepružnou, jako je tomu obvykle u sériových čísel a čísel šarží. V tomto případě se systém bude zvyšovat a snižovat podle změn v poptávce. Kromě toho, pokud jedna poptávka nese různá sériová čísla, nebo čísla šarží, například více než jedno číslo šarže, bude pak navržena jedna objednávka dodávky na šarži.

> [!NOTE]  
> Prognózy by neměly vést k vytváření objednávek na dodávky, které jsou vázány odkazem zakázky na zakázku. Pokud se použije prognóza, měla by se použít pouze jako generátor závislé poptávky ve výrobním prostředí.

### Potřeba komponenty je načtena podle změn výrobní zakázky
Při zpracování výrobních zakázek musí plánovací systém, před jejich načtením do profilu poptávky, sledovat potřebné součásti. Řádky komponent, které jsou výsledkem pozměněné výrobní zakázky, nahradí řádky původní objednávky. Tím je zajištěno, že systém plánování stanoví, že řádky plánování pro potřebu komponenty nejsou nikdy duplikovány.

### <a name="BKMK_SafetyStockMayBeConsumed"></a> Pojistné zásoby mohou být spotřebovány
Množství pojistných zásob je primárně typem poptávky, a proto je načteno do profilu zásob k datu zahájení plánování.

Pojistná zásoba je množství zásob vyčleněné k vyrovnání nejistot v poptávce během dodací lhůty. Může však být spotřebována, pokud je nutné ji využít k umoření poptávky. V takovém případě plánovací systém zajistí, že pojistná zásoba bude rychle vyměněna, a to tak, že navrhne objednávku na doplnění množství pojistné zásoby k datu její spotřeby. Tento řádek plánování zobrazí ikonu upozornění výjimky, která plánovači vysvětlí, že bezpečnostní sklad byl částečně nebo plně spotřebován pomocí objednávky výjimky pro chybějící množství.

### Prognóza poptávky je snížena o prodejní objednávky
Prognóza poptávky vyjadřuje očekávanou budoucí poptávku. Zatímco je zadána skutečná poptávka, obvykle jako prodejní objednávky pro vyrobené zboží, tak spotřebovává prognózu.

Samotná prognóza není ve skutečnosti snížena prodejními objednávkami; zůstává stejná. Předpokládané množství použité v plánovacím výpočtu se však sníží (o množství prodejní objednávky), než zbývající množství, pokud existuje, vstoupí do profilu zásob poptávky. Když systém plánování zkontroluje skutečný prodej během daného období, jsou zahrnuty jak otevřené prodejní objednávky, tak položky zboží z dodaného prodeje, pokud nejsou odvozeny z hromadné objednávky.

Uživatel je povinen definovat platné období prognózy. Datum předpokládaného množství definuje začátek období a datum v další prognóze definuje konec období.

Prognóza pro období před plánovacím obdobím se nepoužívá, bez ohledu na to, zda byla spotřebována nebo ne. První údaj o prognóze je buď datum nebo nejbližší datum před datem zahájení plánování.

Prognóza může být pro nezávislou poptávku, jako jsou například prodejní objednávky, nebo závislé poptávky, jako jsou komponenty výrobní zakázky (prognóza modulu). Položka může mít oba typy prognózy. Během plánování dochází ke spotřebě samostatně, nejprve pro nezávislou poptávku a poté pro závislou poptávku.

### Celková poptávka po objednávkách je snížena o prodejní objednávky
Prognózy jsou doplněny paušální prodejní objednávkou jako prostředek k určení budoucí poptávky konkrétního zákazníka. Stejně jako u (nespecifikované) prognózy by měl skutečný prodej spotřebovat očekávanou poptávku a zbývající množství by mělo zadat profil zásob poptávky. Opět platí, že spotřeba ve skutečnosti nesnižuje plošnou objednávku.

Výpočet plánování bere v úvahu otevřené prodejní objednávky spojené s konkrétním řádkem hromadné objednávky, ale nebere v úvahu žádné platné časové období. Nezohledňuje ani zaúčtované objednávky, protože postup zaúčtování již snížil zbývající hromadné množství objednávky.

## Stanovení priorit objednávek
V rámci dané SKJ představuje požadované nebo dostupné datum nejvyšší prioritu; poptávka dneška by měla být řešena před poptávkou příštího týdne. Kromě této celkové priority však systém plánování také navrhne, jaký typ poptávky by měl být splněn před splněním další poptávky. Stejně tak navrhne, jaký zdroj dodávek by měl být použit před použitím jiných zdrojů dodávek. To se provádí pomocí priorit objednávky.

Načtená poptávka a nabídka přispívají k předpokládanému profilu zásob podle následujících priorit:

### Priority na straně poptávky
1. Již dodáno: Položka zboží
2. Objednávka nákupní vratky
3. Prodejní objednávka
4. Servisní zakázka
5. Potřeba výrobní komponenty
6. Řádek montážní zakázky
7. Objednávka odchozího transferu
8. Hromadná objednávka (která ještě nebyla spotřebována souvisejícími prodejními objednávkami)
9. Prognóza (která ještě nebyla spotřebována jinými prodejními objednávkami)

> [!NOTE]  
> Výnosy z nákupu obvykle nejsou zahrnuty do plánování dodávek; vždy by si měli být vyhrazeni ze šarže, která se má vrátit. Pokud nejsou rezervovány, tak nákupní vratky hrají roli v dostupnosti a jsou vysoce upřednostňovány, aby se zabránilo tomu, že plánovací systém navrhne objednávku dodávky, aby sloužila jako nákupní vratka.

### Priority na straně nabídky
1. Již v zásobách: Položky zboží (Pružnost plánování = Žádná)
2. Objednávka prodejní vratky (Pružnost plánování = Žádná)
3. Objednávka příchozího transferu
4. Výrobní zakázka
5. Montážní zakázka
6. Nákupní objednávka

### Priorita týkající se stavu poptávky a nabídky
Kromě priorit stanovených typem poptávky a nabídky definuje současný stav příkazů v procesu provádění také prioritu. Například mají dopad, aktivity skladu a zohledňuje se také stav prodejních, nákupních, transferů, montážních a výrobních objednávek:

1. Částečně zpracovány (Pružnost plánování = Žádná)
2. Již probíhá ve skladu (Pružnost plánování = Žádná)
3. Vydáno - všechny typy objednávek (Pružnost plánování = Neomezená)
4. Pevně plánované výrobní zakázky (Pružnost plánování = Neomezená)
5. Plánované/otevřené – všechny typy objednávek (Pružnost plánování = Neomezená)

## Vyrovnávání nabídky s poptávkou
Jádro plánovacího systému zahrnuje vyvážení poptávky a nabídky prostřednictvím návrhu uživatelských opatření na revizi objednávek dodávek v případě nerovnováhy. To se děje na kombinaci variant a umístění.

Představte si, že každý profil zásob obsahuje řetězec událostí poptávky (seřazený podle data a priority) a odpovídající řetězec událostí dodávek. Každá událost odkazuje zpět na svůj zdrojový typ a identifikaci. Pravidla pro vyvažování položky jsou jednoduchá. V kterémkoli okamžiku procesu mohou nastat čtyři případy shody poptávky a nabídky:

1. Pro zboží neexistuje poptávka ani nabídka => plánování bylo dokončeno (nebo by nemělo začít).
2. Poptávka existuje, ale neexistuje žádná nabídka => měla by být navržena nabídka.
3. Nabídka existuje, ale není po ní poptávka => nabídka by měla být zrušena.
4. Poptávka i nabídka existují = > prvně bychom se měli zeptat a odpovědět si na otázky, než systém může zajistit, že poptávka bude uspokojena a nabídka je dostatečná.

   Pokud načasování dodávky není vhodné, je možné dodávku přeplánovat následujícím způsobem:

   1. Pokud je nabídka umístěna dříve než poptávka, je možné nabídku přeplánovat tak, aby zásoby byly co nejnižší.
   2. Pokud je nabídka umístěna později než poptávka, možná je možné nabídku přeplánovat. V opačném případě systém navrhne nové dodávky.
   3. Pokud má dodávka stejné datum jako nabídka, může plánovací systém pokračovat ve zkoumání, zda množství dodávky může pokrýt poptávku.

   Jakmile je načasování na místě, dostatečné množství, které má být dodáno, lze vypočítat takto:

   1. Pokud je množství dodávky menší než poptávka, je možné, že množství dodávky by mohlo být zvýšeno (nebo ne, pokud je omezeno zásadou maximálního množství).
   2. Pokud je množství nabídky větší než poptávka, je možné, že množství dodávky lze snížit (nebo ne, pokud je omezeno zásadou minimálního množství).

   V tomto okamžiku existuje některá z těchto dvou situací:

   1. Aktuální poptávka může být pokryta, v takovém případě může být uzavřena a plánování pro další poptávku může začít.
   2. Nabídka dosáhla svého maxima, přičemž část poptávaného množství zůstala nezakrytá. V takovém případě může plánovací systém uzavřít aktuální napájení a přejít k dalšímu.

Postup začíná znovu s dalším požadavkem a aktuální dodávkou nebo naopak. Současná nabídka by mohla být schopna pokrýt i tuto další poptávku, nebo současná poptávka ještě nebyla plně pokryta.

### Pravidla týkající se akcí pro události zásobování
Když plánovací systém provádí výpočet shora dolů, ve kterém musí nabídka uspokojovat poptávku, je poptávka brána jako daná, to znamená, že leží mimo kontrolu plánovacího systému. Stranu nabídky však lze spravovat. Plánovací systém proto navrhne vytvoření nových objednávek dodávek, přeplánování stávajících a / nebo změnu množství objednávky. Pokud se stávající objednávka dodávky stane nadbytečnou, plánovací systém navrhne, aby ji uživatel zrušil.

Pokud chce uživatel vyloučit existující objednávku dodávky z návrhů plánování, může uvést, že nemá žádnou pružnost plánování (Pružnost plánování = Žádná) Poté bude nadbytečná nabídka z této objednávky použita k pokrytí poptávky, ale nebude navržena žádná další akce.

Obecně platí, že všechny dodávky mají pružnost plánování, která je omezena podmínkami každé z navrhovaných akcí.

- **Přeplánovat na**: Datum existující objednávky dodávky může být naplánováno tak, aby splňovalo datum splatnosti poptávky, pokud:

   - Představuje zásoby (vždy v den nula).
   - Má zakázku na zakázku spojenou s jinou poptávkou.
   - Leží mimo stránku přeplánování definovanou časovým segmentem.
   - Existuje užší nabídka, kterou lze použít.
   - Na druhou stranu se uživatel může rozhodnout, že nebude přeplánovat, protože:
   - Objednávka dodávky již byla vázána na jinou poptávku k předchozímu datu.
   - Potřebné přeplánování je tak minimální, že uživatel zjistí, že zanedbatelné.

- **Přeplánovat v**: Datum stávající objednávky na dodávku lze naplánovat, s výjimkou následujících podmínek:

   - Je přímo spojeno s nějakou další poptávkou.
   - Leží mimo stránku přeplánování definovanou časovým segmentem.

> [!NOTE]  
> Při plánování položky pomocí bodu přiobjednání lze v případě potřeby vždy naplánovat objednávku dodávky. To je běžné u dopředu naplánovaných objednávek dodávek spuštěných bodem přiobjednání.

- **Zvýšit množství**: Množství existující objednávky může být zvýšeno, aby byla uspokojována poptávka, pokud není objednávka dodávky přímo spojena s poptávkou propojením objednávky na objednávku.

> [!NOTE]  
> I když je možné zvýšit objednávku dodávky, může být omezena kvůli definovanému maximálnímu množství objednávky.

- **Snížení množství**: Existující objednávka dodávky s přebytkem ve srovnání se stávající poptávkou může být snížena, aby uspokojila poptávku.

> [!NOTE]  
> I když je možné množství snížit, stále může existovat určitý přebytek ve srovnání s poptávkou kvůli definovanému minimálnímu množství objednávky nebo násobku objednávky.

- **Zrušení**: Jako speciální událost akce snížení množství může být objednávka dodávky zrušena, pokud byla snížena na nulu.
- **Nový**: Pokud již neexistuje žádná objednávka na dodávku nebo nelze stávající změnit, aby splňovala potřebné množství v požadovaném termínu splatnosti, je navržena nová objednávka na dodávku.

### Stanovení množství dodávky
Parametry plánování definované uživatelem řídí navrhované množství každé objednávky dodávky.

Když plánovací systém vypočítá množství nové objednávky dodávky nebo změnu množství na stávající objednávce, může se navrhované množství lišit od toho, co je skutečně požadováno.

Pokud je vybráno maximální množství zásob nebo pevné množství objednávky, může být navrhované množství zvýšeno, aby bylo splněno toto pevné množství nebo maximální zásoby. Pokud zásada pro změnu pořadí používá bod pro opětovné objednání, může být množství zvýšeno alespoň tak, aby splňovalo bod pro opětovné objednání.

Navrhované množství lze upravit v tomto pořadí:

1. Až do maximálního množství objednávky (pokud existuje).
2. Až do minimálního množství objednávky.
3. Až na splnění nejbližšího násobku objednávky. (V případě chybného nastavení může toto porušit maximální množství objednávky.)

### Odkazy sledování objednávek během plánování objednávek
Pokud jde o sledování objednávek během plánování, je důležité zmínit, že plánovací systém mění uspořádání dynamicky vytvořených odkazů sledování objednávek pro kombinace zboží/varianta/umístění.

Existují pro to dva důvody:

- Plánovací systém musí být schopen své návrhy odůvodnit; že byla pokryta veškerá poptávka a že žádné objednávky na dodávky nejsou nadbytečné.
- Dynamicky vytvořené odkazy sledování objednávek je třeba pravidelně vyvažovat.

V průběhu času se odkazy na dynamické sledování objednávek nevyrovnají, protože celá síť pro sledování objednávek není přeskupena, dokud není událost poptávky nebo nabídky skutečně uzavřena.

Před vyrovnáním nabídky podle poptávky aplikace odstraní všechna existující propojení sledování objednávek. Pak během postupu vyrovnávání, když je uzavřena událost poptávky nebo nabídky, vytvoří nové propojení sledování objednávek mezi poptávkou a nabídkou.

> [!NOTE]  
> I když položka není nastavena pro dynamické sledování objednávek, plánovaný systém vytvoří vyvážené odkazy pro sledování objednávek, jak je vysvětleno výše.
## Uzavření poptávky a nabídky
Po provedení postupů vyvážení dodávek existují tři možné koncové situace:

* Bylo splněno požadované množství a datum událostí poptávky a jejich plánování může být uzavřeno. Událost nabídky je stále otevřená a může být schopna pokrýt další poptávku, takže postup vyrovnávání může začít znovu s aktuální událostí nabídky a další poptávkou.
* Objednávku nabídky nelze upravit tak, aby pokryla celou poptávku. Událost poptávky je stále otevřená, s určitým nekrytým množstvím, které může být pokryto další událostí dodávky. Aktuální událost dodávky je tedy uzavřena, takže vyrovnávací akt může začít znovu s aktuální poptávkou a další událostí dodávky.
* Veškerá poptávka byla pokryta; neexistuje žádná následná poptávka (nebo nebyla vůbec žádná poptávka). Pokud existuje přebytek nabídky, může být snížena (nebo zrušena) a poté uzavřena. Je možné, že další události dodávky existují dále v řetězci a měly by být také zrušeny.

Nakonec plánovací systém vytvoří odkaz na sledování objednávky mezi nabídkou a poptávkou.

### Vytvoření řádku plánování (navrhovaná akce)
Pokud je k revizi objednávky dodávek navržena nějaká akce – Nové, Změnit množství, Přeplánovat, Přeplánovat a Změnit množství nebo Zrušit – systém plánování vytvoří řádek plánování v sešitu plánování. Z důvodu sledování objednávky je řádek plánování vytvořen nejen při uzavření události nabídky, ale také v případě, že je uzavřena událost poptávky, i když je událost nabídky stále otevřená a může podléhat dalším změnám při zpracování další události poptávky. To znamená, že při prvním vytvoření může být řádek plánování znovu změněn.

Chcete-li minimalizovat přístup k databázi při zpracování výrobních zakázek a současně provádět nejméně náročnou úroveň údržby, může být plánovací řádek udržován ve třech úrovních:

* Vytvořte pouze řádek plánování s aktuálním datem splatnosti a množstvím, ale bez technologického postupu a komponent.
* Zahrnout TNG postup: plánovaný tng postup je stanoven včetně výpočtu počátečních a koncových dat a časů. To je náročné z hlediska přístupu k databázi. K určení data ukončení a splatnosti může být nutné tuto možnost vypočítat i v případě, že událost dodávky nebyla uzavřena (v případě  plánování popředu).
* Zahrnout rozpad kusovníku: to může počkat, až těsně před uzavřením události zásobování.

Tím se uzavírá popis toho, jak je plánovací systém načítán, upřednostňován a vyvážen poptávkou a nabídkou. Při integraci s touto aktivitou plánování dodávek musí systém zajistit, aby požadovaná úroveň zásob každého plánovaného zboží byla udržována v souladu se svými zásadami přiobjednání.

## Viz také
[Detaily návrhu: Centrální koncepce plánovacího systému](design-details-central-concepts-of-the-planning-system.md)   
[Detaily návrhu: Zpracování způsobu přiobjednání](design-details-handling-reordering-policies.md)   
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)
