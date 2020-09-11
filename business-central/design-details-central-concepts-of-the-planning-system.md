---
    title: Design Details - Central Concepts of the Planning System| Microsoft Docs
    description: The planning functions are contained in a batch job that first selects the relevant items and period to plan for and then suggests possible actions for the user to take based on the demand/supply situation and the items' planning parameters.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Detaily návrhu: Centrální koncepce plánovacího systému
Funkce plánování jsou obsaženy v dávkové úloze, která nejprve vybere příslušné zboží a období, pro které chcete plánovat. Poté, podle nízkoúrovňového kódu každého zboží (pozice kusovníku) vyvolá dávková úloha kódovou jednotku, která vypočítá plán dodávky vyvážením sad nabídky a poptávky a následně navrhnutím možných akcí, které má uživatel provést. Navrhované akce se zobrazí jako řádky v sešitu plánování, nebo v sešitu požadavků.

![Obsah stránky sešitu plánování](media/NAV_APP_supply_planning_1_planning_worksheet.png "Obsah stránky sešitu plánování")

Předpokládá se, že plánovač společnosti, například kupující nebo plánovač výroby, je uživatelem plánovacího systému. Plánovací systém pomáhá uživateli prováděním rozsáhlých, ale spíše jednoduchých výpočtů plánu. Uživatel se pak může soustředit na řešení složitějších problémů, například když se věci liší od normálu.

Systém plánování je poháněn očekávanou a skutečnou poptávkou zákazníků, jako jsou prognózy a prodejní objednávky. Spuštění výpočtu plánování bude mít za následek aplikaci navrhovaných konkrétních akcí, které má uživatel provést v souvislosti s možnými dodávkami od dodavatelů, montáže, či středisek dílen nebo převody z jiných skladů. Tyto navrhované akce by mohly být vytvoření nových objednávek dodávek, jako jsou nákupní nebo výrobní zakázky. Pokud již objednávky dodávek existují, navrhované akce by mohly být zvýšení nebo urychlení objednávek ke splnění změn v poptávce.

Dalším cílem plánování je zajistit, aby zásoby zbytečně nerostly. Pokud se poptávka sníží, plánovací systém navrhne, aby uživatel odložil, snížil množství nebo zrušil stávající objednávky dodávek.

MRP a MPS, Vypočítat plánovaný pohyb, nebo Vypočítat regenerační plán jsou všechny funkce v jedné kódové jednotce, které obsahují logiku plánování. Výpočet plánu dodávky však zahrnuje různé podsystémy.

Všimněte si, že systém plánování neobsahuje žádnou vyhrazenou logiku pro vyrovnání kapacity nebo jemné plánování. Proto se tato práce plánování provádí jako samostatná disciplína. Nedostatečná přímá integrace mezi oběma oblastmi také znamená, že podstatné změny kapacity nebo plánu budou vyžadovat opětovné spuštění plánování.

## Parametry plánování
Parametry plánování, které uživatel nastaví pro položku nebo skupinu položek, určují, které akce plánovací systém v různých situacích navrhne. Parametry plánování jsou definovány na každé kartě zboží, která určuje, kdy, kolik a jak doplňovat.

Parametry plánování lze také definovat pro jakoukoliv kombinaci zboží, varianty a umístění nastavením skladované jednotky (SKJ) pro každou potřebnou kombinaci a poté zadáním jednotlivých parametrů.

Pro více informací navštivte [Detaily návrhu: Zpracování způsobu přiobjednání](design-details-handling-reordering-policies.md) a [Detaily návrhu: Parametry plánování](design-details-planning-parameters.md).

## Počáteční datum plánování
Aby se zabránilo plánu dodávek, který zahrnuje otevřené objednávky v minulosti a navrhuje potenciálně nemožné akce, plánovací systém zachází se všemi daty před počátečním datem plánování jako se zamraženou zónou, kde platí následující zvláštní pravidlo:

Veškerá nabídka a poptávka před počátečním datem plánovacího období budou považovány za součást zásob nebo za dodané.

Jinými slovy, se předpokládá, že plán minulosti je realizován podle daného plánu.

Pro více informací navštivte [Práce s objednávkami před počátečním datem plánování](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).

## Dynamické sledování zakázky (Doložení)
Dynamické sledování zakázky, se současným vytvářením zpráv o akcích v sešitu plánování, není součástí systému plánování dodávek v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tato funkce v reálném čase propojuje poptávku a množství, která by je mohla pokrýt, kdykoli je vytvořena nebo změněna nová poptávka nebo nabídka.

Pokud uživatel například zadá nebo změní prodejní objednávku, dynamický systém sledování objednávek okamžitě vyhledá vhodnou nabídku, která pokryje poptávku. To může být ze zásob, nebo z očekávané objednávky dodávky (jako je nákupní, nebo výrobní objednávka). Když je nalezen zdroj dodávky, systém vytvoří vazbu mezi poptávkou a dodávkou a zobrazí ji na stránkách pouze pro zobrazení, ke kterým je přístup z příslušných řádků dokladu. Pokud nelze najít vhodné dodávky, systém dynamického sledování objednávek vytvoří zprávy o akcích v sešitu plánování s návrhy plánu dodávek, které odrážejí dynamické vyvažování. Systém dynamického sledování zakázek proto nabízí velmi základní plánovací systém, který může pomoci jak plánovači, tak dalším rolím ve vnitřním dodavatelském řetězci.

Dynamické sledování zakázek lze proto považovat za nástroj, který pomáhá uživateli při posuzování, zda přijmout návrhy objednávek dodávek. Z nabídky může uživatel zjistit, která poptávka vytvořila nabídku, a ze strany poptávky, která nabídka by měla pokrýt poptávku.

![Příklad dynamického sledování zakázky](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Příklad dynamického sledování zakázky")

Pro více informací navštivte [Detaily návrhu: Rezervace, sledování zásilky a zasílání zpráv](design-details-reservation-order-tracking-and-action-messaging.md).

Ve společnostech s nízkým tokem zboží a méně pokročilými výrobními strukturami, může být vhodné použít dynamické sledování zakázky jako hlavní prostředek plánování dodávek. V rušnějších prostředích by však měl být systém plánování používán k zajištění řádně vyváženého plánu dodávek za všech okolností.

### Dynamické sledování zakázky nebo systéme plánování
Na první pohled může být obtížné rozlišit plánovací systém od dynamického sledování zakázek. Obě funkce zobrazují výstup ze sešitu plánování tím, že navrhují akce, které by měl plánovač provést. Způsob výroby tohoto výstupu se však liší.

Systém plánování se zabývá celým vzorem nabídky a poptávky zboží prostřednictvím všech úrovní hierarchie kusovníku podél časové osy, zatímco dynamické sledování zakázky řeší pouze situaci objednávky, která ji aktivovala. Při vyrovnávání poptávky a nabídky vytvoří systém plánování propojení v dávkovém režimu aktivovaném uživatelem, zatímco dynamické sledování objednávek vytvoří odkazy automaticky a průběžně, kdykoli uživatel zadá poptávku nebo dodávku v aplikaci, například prodejní objednávku nebo nákupní objednávku.

Dynamické sledování zakázek vytváří vazby mezi poptávkou a nabídkou při zadávání dat podle zásady "kdo dřív přijde ten dřív mele". To může vést k určitým poruchách v prioritách. Například prodejní objednávka zadaná jako první, s termínem splatnosti příští měsíc, může být propojena s dodávkou ve skladu, zatímco další prodejní objednávka splatná zítra může způsobit, že zpráva akce vytvoří novou nákupní objednávku, která ji zakryje, jak je znázorněno níže.

![Příklad sledování zakázky v plánování dodávek 1](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Příklad sledování zakázky v plánování dodávek 1")

Naproti tomu plánovací systém se zabývá veškerou poptávkou a nabídkou pro konkrétní zboží, v pořadí podle priority podle termínů splatnosti a typů objednávek, tj. "kdo dřív přijde ten dřív mele". Odstraní všechny odkazy sledování zakázek, které byly vytvořeny dynamicky a obnoví je podle priority termínu splnění. Po spuštění plánovacího systému, vyřeší všechny nerovnováhy mezi poptávkou a nabídkou, jak je znázorněno níže pro stejná data.

![Příklad sledování zakázky v plánování dodávek 2](media/NAV_APP_supply_planning_1_planning_graph.png "Příklad sledování zakázky v plánování dodávek 2")

Po spuštění běhu plánování nezůstanou v tabulce Položka hlášení akce žádné zprávy o akci, protože byly nahrazeny navrhovanými akcemi v sešitu plánováním.

Pro více informací navštivte Spojení sledování zakázky během plánování v [Vyvažování poptávky a nabídky

## Posloupnost a priorita v plánování
Při sestavování plánu je důležitá posloupnost výpočtů, aby byla práce provedena v přiměřeném časovém rámci. Kromě toho priority požadavků a zdrojů hrají důležitou roli při dosahování nejlepších výsledků.

Plánovací systém v [!INCLUDE[d365fin](includes/d365fin_md.md)] je řízen podle poptávky. Položky vysoké úrovně by měly být naplánovány před položkami nižší úrovně, protože plán pro položky vysoké úrovně může vygenerovat další poptávky po položkách nižší úrovně. To například znamená, že maloobchodní místa by měla být naplánována před plánovanými distribučními centry, protože plán pro maloobchodní lokace může zahrnovat další poptávky z distribučního centra. Na podrobné úrovni vyrovnávání to také znamená, že prodejní objednávka by neměla aktivovat novou objednávku dodávky, pokud je již uvolněná objednávka dodávky, může pokrýt prodejní objednávku. Stejně tak by nabídka s určitým číslem šarže neměla být přidělena na pokrytí obecné poptávky, pokud tuto konkrétní šarži vyžaduje jiná poptávka.

### Priorita položky / Kód nižší úrovně
Ve výrobním prostředí bude poptávka po dokončené, prodejné položce vést k odvozené poptávce po komponentech, které tvoří hotovou položku. Struktura kusovníku řídí strukturu komponent a může pokrývat několik úrovní polotovarů. Plánování položky na jedné úrovni způsobí odvozenou poptávku po komponentách na další úrovni atd. Výsledkem bude nakonec odvozená poptávka po zakoupených položkách. V důsledku toho systém plánování plánuje položky v pořadí podle jejich pořadí v celkové hierarchii kusovníku, počínaje dokončenými prodejnými položkami na nejvyšší úrovni a pokračujícím dolů prostřednictvím struktury produktu na položky nižší úrovně (podle kódu nižší úrovně).

![Plánování pro výrobní kusovník](media/NAV_APP_supply_planning_1_BOM_planning.png "Plánování pro výrobní kusovník")

Obrázky ilustrují, v jakém pořadí systém předkládá návrhy na objednávky dodávek na nejvyšší úrovni, a za předpokladu, že uživatel tyto návrhy přijme, také pro jakékoli položky nižší úrovně.

Pro další informace o úvahách výroby, navštivte [Načítání profilů zásob](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### Lokace / Priorita úrovně transferu
Společnosti, které působí na více než jedné lokaci, možná budou muset naplánovat každou lokaci zvlášť. Například úroveň bezpečného stavu zboží a její způsob přiobjednání se mohou v různých lokalitách lišit. V takovém případě musí být parametry plánování určeny pro zboží a také pro skladové místo.

To je podporováno s použitím SKJ, kde lze zadat jednotlivé parametry plánování na úrovni skladové jednotky. SKJ lze považovat za zboží na konkrétní lokaci. Pokud uživatel nedefinoval SKJ pro tuto lokaci, aplikace bude výchozí na parametry, které byly nastaveny na kartě zboží. Aplikace vypočítá plán pouze pro aktivní lokace, což je místo, kde existuje poptávka nebo nabídka pro dané zboží.

V zásadě lze s libovolným zbožím nakládat a pracovat na libovolné lokaci, ale přístup aplikace ke koncepci lokací je poměrně přísný. Například prodejní objednávka na jedné lokaci nemůže být splněna určitým množstvím na skladě na jiné lokaci. Množství na skladě musí být nejprve převedeno na lokaci uvedenou na prodejní objednávce.

![Plánování skladových jednotek](media/NAV_APP_supply_planning_1_SKU_planning.png "Plánování skladových jednotek")

Pro více informací navštivte [Detaily návrhu: Plánování transferů](design-details-transfers-in-planning.md).

### Priorita objednávky
V rámci dané SKJ, představuje požadované nebo dostupné datum nejvyšší prioritu; dnešní poptávka by měla být řešena před poptávkou nadcházejících dní. Kromě této určité priority se však různé typy poptávky a nabídky třídí podle důležitosti podnikání, aby se rozhodlo, která poptávka by měla být uspokojena před uspokojením jiné poptávky. Na straně nabídky bude priorita objednávky říkat, jaký zdroj dodávky by měl být použit před použitím jiných zdrojů dodávky.

Pro více informací navštivte [Upřednostňování objednávek](design-details-balancing-demand-and-supply.md#prioritizing-orders).

## Prognózy poptávky a hromadné objednávky
Prognózy i hromadné objednávky představují očekávanou poptávku. Hromadná objednávka, která pokrývá zamýšlené nákupy zákazníka za určité časové období, snižuje nejistotu celkové prognózy. Hromadná objednávka je prognóza specifická pro zákazníka nad nespecifikovanou prognózou, jak je znázorněno níže.

![Plánování s prognózami](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Plánování s prognózami")

Pro více informací navštivte sekci “Snížení předpovědi poptávky prodejními objednávkami” v [Načítání profilů zásob](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

## Přiřazení plánováním
Všechno zboží by mělo být plánováno, není však důvod vypočítat plán pro zboží, ledaže by došlo ke změně struktury poptávky nebo nabídky od posledního výpočtu plánu.

Pokud uživatel zadal novou prodejní objednávku nebo změnil existující, vznikne důvod přepočítat plán. Mezi další důvody patří změna v prognóze nebo požadované množství bezpečných zásob. Změna kusovníku přidáním nebo odebráním komponenty by s největší pravděpodobností znamenala změnu, ale pouze pro položku komponenty.

Plánovací systém sleduje tyto události a přiřazuje příslušné položky pro plánování.

Pro více lokací se přiřazení provádí na úrovni zboží podle kombinace lokace. Pokud byla například prodejní objednávka vytvořena pouze v jedné lokace, aplikace přiřadí zboží v této konkrétní lokaci k plánování.

Důvodem výběru zboží pro plánování je otázka výkonu systému. Pokud nedošlo k žádné změně ve struktuře poptávky a nabídky zboží, systém plánování nenavrhl žádné akce, které mají být podniknuty. Bez přiřazení plánování by systém musel provést výpočty pro všechny položky, aby zjistil, co plánovat, a to by vyčerpalo systémové prostředky.

Úplný seznam důvodů pro přiřazení zboží k plánování je uveden v [Detaily návrhu: Tabulka přiřazení plánování](design-details-planning-assignment-table.md) .

Možnosti plánování v [!INCLUDE[d365fin](includes/d365fin_md.md)] jsou:

- Vypočítat regenerační plán – Vypočítá všechno vybrané zboží, zda je to nutné nebo ne.
- Vypočítat plánovaný pohyb – Vypočítá pouze to vybrané zboží, u kterého došlo k určité změně ve struktuře poptávky a nabídky, a proto byly přiřazeny k plánování.

Někteří uživatelé se domnívají, že plánování čistých změn by mělo být prováděno průběžně, například při zadávání prodejních objednávek. To však může být matoucí, protože dynamické sledování zakázky a zasílání zpráv akcí se také počítají za běhu. Kromě toho, [!INCLUDE[d365fin](includes/d365fin_md.md)] nabízí kontrolu v reálném čase, která je k dispozici pro slib, která poskytuje varování pomocí vyskakovacích oken při zadávání prodejních objednávek, pokud poptávku nelze splnit podle současného plánu dodávek.

Kromě těchto aspektů systém plánování plánuje pouze pro ty položky, které uživatel připravil s příslušnými parametry plánování. Jinak se předpokládá, že uživatel naplánuje položky ručně nebo poloautomaticky pomocí funkce Plánování objednávek.

Pro více informací o postupech automatického plánování navštivte, [Detaily návrhu: Vyvažování poptávky a nabídky](design-details-balancing-demand-and-supply.md).

## Dimenze položky
Poptávka a nabídka mohou nést alternativní kódy a lokalizační kódy, které musí být respektovány, když plánovací systém vyrovnává poptávku a nabídku.

Systém považuje kódy variant a lokací za dimenze zboží na řádku prodejní objednávky, položky zboží, atd. Podle toho vypočítá plán pro každou kombinaci varianty a lokace, jako by kombinace byla samostatným číslo zboží.

Namísto výpočtu jakékoli teoretické kombinace varianty a umístění aplikace počítá pouze ty kombinace, které skutečně existují v databázi.

Pro více informací o tom, jak systém plánování zachází s kódy lokací na poptávce navštivte, [ Detaily návrhu: Poptávka v prázdném skladu](design-details-balancing-demand-and-supply.md).

## Atributy zboží
Kromě obecných dimenzí zboží, jako je číslo zboží, kód varianty, kód lokace a typ objednávky, může každá událost poptávky a dodávky nést další specifikace ve formě sériových čísel/čísel šarží. Plánovací systém plánuje tyto atributy určitým způsobem v závislosti na jejich úrovni specifikace.

Propojení mezi objednávkou a dodávkou je jiný typ atributu, který ovlivňuje systém plánování.

### Specifické atributy
Určité atributy na vyžádání jsou specifické a musí se přesně shodovat s odpovídající nabídkou. Existují následující dva specifické atributy:

- Požadovaná sériová čísla, nebo čísla šarže, která vyžadují určitou aplikaci (zaškrtávací políčko **Sledování sériových čísel** nebo **Sledování určité dávky** jsou vybrané na stránce **Karta kódu sledování zboží** pro kód sledování zboží, který je zbožím používán.)
- Odkazy na objednávky dodávek vytvořené ručně nebo automaticky pro konkrétní poptávku (odkazy zakázky na zakázku).

Pro tyto atributy použije plánovací systém následující pravidla:

- Poptávku se specifickými atributy lze splnit pouze dodávkou odpovídajících atributů.
- Nabídka se specifickými atributy může také uspokojit poptávku, která tyto atributy výslovně nevyžaduje.

Pokud tedy poptávku po konkrétních atributech nelze splnit zásobami nebo předpokládanými dodávkami, systém plánování navrhne novou objednávku dodávek, která pokryje tuto specifickou poptávku bez ohledu na parametry plánování.

### Nespecifické atributy
Sériová čísla nebo čísla šarže bez určitého sledování zboží mohou nést sériová čísla, nebo čísla šarží, která nemusí být použita na přesně stejné sériové číslo/číslo šarže, ale mohou být použita na libovolné sériové číslo/číslo šarže. To dává plánovacímu systému větší volnost při porovnávání například serializovanou poptávku s serializovanou dodávkou, obvykle v inventáři.

Poptávka-dodávky se sériovým číslem, číslem šarže, specifickým, nebo nespecifickým, jsou považovány za vysoko prioritní a jsou tedy osvobozeny od zamrzlé zóny, což znamená, že budou součástí plánování, i když jsou splatné před plánovaným datem zahájení.

Pro více informací navštivte část “Nakládání sériových čísel a čísla šarže podle úrovně zadání” v [Načítání profilů zásob](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

Pro více informací o tom jak plánovací systém vyrovnává atributy, navštivte [ Sériová čísla/čísla šarží a zakázka na zakázku odkazy jsou vyňaty ze zmrazené zóny ](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).

## Zakázka pro zakázku
Zásobování zakázky pro zakázku znamená, že položka je zakoupena, sestavena nebo vyrobena výhradně pro pokrytí konkrétní poptávky. Obvykle se to týká zboží typu A. Motivací pro výběr této zásady může být, že poptávka je vzácná, dodací lhůta je nevýznamná nebo se požadované atributy liší.

Dalším zvláštním případem, který používá propojení mezi objednávkami, je, když je objednávka sestavení propojena s prodejní objednávkou ve scénáři sestavení na objednávku.

Propojení mezi objednávkami jsou aplikované mezi nabídkou a poptávkou a to čtyřmi způsoby:

- Když plánované zboží používá zásadu přiobjednání Objednávka.
- Při použití způsobu výroby Zhotovit na objednávku k vytvoření víceúrovňových výrobních zakázek nebo výrobních zakázek typu projektu (výroba potřebných komponent ve stejné výrobní zakázce).
- Při vytváření výrobních objednávek pro prodejní objednávky pomocí funkce Plánování prod.objednávky.
- Při sestavování položky do prodejní objednávky. (Způsob montáže je nastaven na Montáž-na-objednávku.

V těchto případech systém plánování pouze navrhne objednat požadované množství. Po vytvoření bude objednávka nákupu, výroby nebo sestavy nadále odpovídat odpovídající poptávce. Pokud se například prodejní objednávka změní v čase nebo množství, systém plánování navrhne změnění odpovídající objednávky dodávky a to odpovídajícím způsobem.

Pokud existují spojení zakázky pro zakázku, plánovací systém nezahrnuje do vyrovnávacího procesu související dodávku ani inventář. Je na uživateli, aby vyhodnotil, zda by propojená zakázka měla být použita k pokrytí jiné nebo nové poptávky, a v takovém případě vymaže objednávku dodávky nebo si zarezervuje propojenou dodávku ručně.

Rezervace a odkazy pro sledování se přeruší, pokud se situace stane nemožnou, například přesunutím poptávky na datum dřívější než dodávka. Propojení mezi objednávkami se však přizpůsobuje jakýmkoli změnám v příslušné poptávce nebo nabídce, a proto není propojení nikdy přerušeno.

## Rezervace
Plánovací systém nezahrnuje do výpočtu žádná rezervovaná množství. Pokud byla například prodejní objednávka zcela nebo částečně rezervována proti množství ve skladu, nelze rezervované množství ve skladu použít k pokrytí jiné poptávky. Plánovací systém nezahrnuje tuto sadu poptávky a nabídky do svého výpočtu.

Systém plánování však bude stále zahrnovat rezervovaná množství v profilu předpokládaného skladu, protože všechna množství musí být zohledněna jak při předpokládání bodu přiobjednání, tak počet změn, které mají být k dispozici, a nesmí překročit maximální úroveň zásob. V důsledku toho zbytečné rezervace povedou ke zvýšeným rizikům, že úrovně zásob jsou nízké, protože logika plánování nerozezná vyhrazená množství.

Následující obrázek ukazuje, jak rezervace mohou bránit nejvhodnějšímu plánu.

![Plánování s rezervacemi](media/NAV_APP_supply_planning_1_reservations.png "Plánování s rezervacemi")

Pro více informací navštivte [Detaily návrhu: Rezervace, sledování zásilky a zasílání zpráv](design-details-reservation-order-tracking-and-action-messaging.md).

## Varování
První sloupec v sešitu plánování je pro pole upozornění. Na každém řádku plánování vytvořeném pro neobvyklou situaci se v tomto poli zobrazí výstražná ikona, na kterou může uživatel klepnout a získat další informace.

Dodávky na plánovacích řádcích s upozorněním se obvykle nezmění podle parametrů plánování. Místo toho plánovací systém pouze navrhuje dodávku, která pokryje přesné množství poptávky. Systém však může být nastaven tak, aby respektoval určité parametry plánování pro plánovací řádky s určitými varováními. Další informace naleznete v popisu těchto možností pro dávkové úlohy **Výpočet plánu - plán. sešit** a **Vypočítat plán-sešit požadavků**.

Varovné informace jsou zobrazeny na stránce **Nesledované prvky plánování**, která se také používá k zobrazení odkazů na sledování objednávek na neobjednané síťové entity. Existují následující typy upozornění:

- Nouzové
- Výjimka
- Pozor

![Upozornění v sešitu plánování](media/NAV_APP_supply_planning_1_warnings.png "Upozornění v sešitu plánování")

### Nouzové
Nouzové varování se zobrazuje ve dvou situacích:

- Pokud je zásoba záporná k počátečnímu datu plánování.
- Pokud existují datované nebo poptávané události.

Pokud jsou zásoby položky k počátečnímu datu plánování záporné, systém plánování navrhne nouzovou objednávku dodávky pro záporné množství, které má být doručeno k počátečnímu datu plánování. Text upozornění uvádí počáteční datum a množství nouzové objednávky. Pro více informací navštivte [Nakládání s předpokládaným záporným stavem zásob](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).

Všechny řádky dokladu s daty splatnosti před datem zahájení plánování jsou sloučeny do jedné objednávky nouzové dodávky, aby zboží dorazilo k počátečnímu datu plánování.

### Výjimka
Varování o výjimce se zobrazí, pokud plánované dostupné zásoby klesnou pod množství bezpečného materiálu. Plánovací systém navrhne objednávku na dodávky, které uspokojí poptávku v den splatnosti. Varovný text uvádí množství bezpečnostního materiálu a datum, kdy došlo k jeho porušení.

Porušení úrovně bezpečných zásob je považováno za výjimku, protože by nemělo nastat, pokud byl správně nastaven bod přiobjednání. Pro více informací navštivte [ Zpracování způsobu přiobjednání](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).

Obecně platí, že výjimečné návrhy objednávek zajišťují, že předpokládané dostupné zásoby nebudou nikdy nižší než úroveň zásob bezpečnosti. To znamená, že navrhované množství je dostatečné na pokrytí bezpečnostního materiálu, aniž by byly zohledněny parametry plánování. V některých scénářích však budou brány v úvahu modifikátory objednávky.

> [!NOTE]
> Plánovací systém může spotřebovat pojistnou zásobu záměrně a kterou poté ihned doplní. Pro více informací navštivte [Vyvažování poptávky a nabídky](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).

### Pozor
Upozornění je zobrazeno ve třech situacích:

- Počáteční datum plánování je dřívější než pracovní datum.
- Řádek plánování navrhuje změnu vydané nákupní nebo výrobní zakázky.
- Plánované zásoby přesahují úroveň přetečení ke dnu splatnosti. Pro více informací navštivte [Pod úrovni přetečení](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).

> [!NOTE]
> V plánování řádků s výstrahami není vybráno pole **Přijmout hlášené akce**, protože se očekává, že plánovač tyto řádky před provedením plánu dále prozkoumá.

## Protokoly chyb
Na stránce požadavku Vypočítat plán může uživatel vybrat pole **Ukončit a zobrazit první chybu** aby se zastavilo spuštění plánování, když narazí na první chybu. Současně se zobrazí zpráva s informacemi o chybě. Pokud dojde k chybě, budou v plánovacím sešitu zobrazeny pouze úspěšné řádky plánování provedené před výskytem chyby.

Pokud toto pole není vybráno, dávková úloha Vypočítat plán bude pokračovat, dokud nebude dokončena. Chyby dávkovou úlohu nepřeruší. Pokud existuje jedna nebo více chyb, aplikace po dokončení zobrazí zprávu, která říká, na kolik položek se chyba vztahuje. Stránka **Protokol chyb plánování**, kde se zobrazí další podrobnosti o chybě a odkazy na postižené dokumenty nebo instalační karty.

![Chybové zprávy v sešitu plánování](media/NAV_APP_supply_planning_1_error_log.png "Chybové zprávy v sešitu plánování")

## Pružnost plánování
Není vždy praktické plánovat stávající objednávku dodávek, například když byla zahájena výroba nebo jsou na konkrétní den najati další lidé, kteří tuto práci vykonají. Aby bylo možné určit, zda stávající plán může být plánovacím systémem změněn, mají všechny řádky objednávek dodávky pole Pružnost plánování s dvěma možnostmi: Neomezeno nebo Žádné. Pokud je pole nastaveno na Žádné, plánovací systém se nepokusí změnit řádek objednávky dodávek.

Pole může být ručně nastaveno uživatelem, v některých případech však bude nastaveno systémem automaticky. Skutečnost, že flexibilitu plánování může uživatel nastavit ručně, je důležitá, protože usnadňuje přizpůsobení použití této funkce různým pracovním postupům a obchodním případům.

Pro více informací o použití těchto polí naleznete v [Detaily návrhu: Plánování transferů](design-details-transfers-in-planning.md).

## Plánování objednávek
Základní nástroj pro plánován reprezentovaný stránkou **Plánování objednávek** je vytvořen pro manuální rozhodování. Nezohledňuje žádné parametry plánování, a proto se nebudeme v tomto dokumentu dále jim zabývat. Další informace o funkci Plánování objednávek, naleznete v nápovědě v [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Nedoporučuje se používat plánování objednávek, pokud společnost již používá sešity požadavků, nebo sešity plánování. Objednávky dodávek vytvořené prostřednictvím stránky **Plánování objednávek** mohou být během automatických spuštění plánování změněny nebo odstraněny. Důvodem je to, že automatické spuštění plánování používá parametry plánování a tyto nemusí být považovány uživatelem, který provedl ruční plán na stránce Plánování objednávek.

## Omezené zatížení
[!INCLUDE[d365fin](includes/d365fin_md.md)] je standardní ERP systém, nikoli expediční nebo dílenské řízení. Plánuje možné využití zdrojů poskytováním hrubého plánu, ale automaticky nevytváří a neudržuje podrobné plány na základě priorit nebo pravidel optimalizace.

Zamýšlené použití funkce Zdroje s limitovanou kapacitou je 1): aby se zabránilo přetížení konkrétních prostředků a 2): zajistit, že žádná kapacita nezůstane nepřidělená, pokud by mohla zvýšit dobu obratu výrobní zakázky. Tato funkce neobsahuje žádná zařízení ani možnosti pro stanovení priorit nebo optimalizaci operací, jak by se dalo očekávat v dispečerském systému. Může však poskytovat informace o hrubé kapacitě, které jsou užitečné, k identifikaci úzkých míst a zamezení přetížení zdrojů.

Při plánování se zdroji s omezenou kapacitou systém zajišťuje, aby žádný zdroj nebyl načten nad jeho definovanou kapacitu (Kritické zatížení). To se provádí přiřazením každé operace k nejbližšímu dostupnému časovému úseku. Pokud časový úsek není dostatečně velký na dokončení celé operace, operace bude rozdělena na dvě nebo více částí umístěných v nejbližších dostupných časových slotech.

> [!NOTE]
> V případě rozdělení provozu je nastavovací čas přiřazen pouze jednou, protože se předpokládá, že je provedeno nějaké ruční nastavení pro optimalizaci plánu.

Časová prodleva lze přidat k prostředkům, aby se minimalizovalo rozdělení operací. To umožňuje systému naplánovat zatížení na poslední možný den mírným překročením procenta kritického zatížení, pokud to může snížit počet rozdělených operací.

Tím je dokončen nástin centrálních konceptů týkajících se plánování dodávek v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Následující části tyto pojmy podrobněji zkoumají a umisťují je do kontextu základních plánovacích postupů, vyvažují poptávku a nabídku a používají způsob přiobjednání.

## Viz také
[Detaily návrhu: Plánování transferů](design-details-transfers-in-planning.md)  
[Detaily návrhu: Parametry plánování](design-details-planning-parameters.md)  
[Detaily návrhu: Tabulka přiřazení plánování](design-details-planning-assignment-table.md)  
[Detaily návrhu: Zpracování způsobu přiobjednání](design-details-handling-reordering-policies.md)  
[Detaily návrhu: Vyvažování poptávky a nabídky](design-details-balancing-demand-and-supply.md)
