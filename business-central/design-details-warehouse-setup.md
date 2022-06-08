---
    title: Design Details - Warehouse Setup
    description: Warehouse functionality contains different levels of complexity, which is largely defined by the bin setup on location cards.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 06/15/2021
    ms.author: edupont

---
# Detaily návrhu: Nastavení skladu

Funkčnost skladu v [!INCLUDE[prod_short](includes/prod_short.md)] obsahuje různé úrovně složitosti, jak jsou definovány licenčními oprávněními v nabízených granulích. Úroveň složitosti řešení skladu je do značné míry definována nastavením přihrádky na kartách lokací, která je zase řízena licencí, takže přístup k polím nastavení přihrádky je definován licencí. Kromě toho objekty aplikace v licenci určují, který dokument uživatelského rozhraní se má použít pro podporované aktivity skladu.
<!--
The following warehouse-related granules exist:  

- Basic Inventory (4010)  
- Bin (4170)  
- Put Away (4180)  
- Warehouse Receipt (4190)  
- Pick (4200)  
- Warehouse Shipment (4210)  
- Warehouse Management Systems (4620)  
- Internal Picks and Put-aways (4630)  
- Automated Data Capture System (4640)
- Bin Setup (4660)  

For more information about each granule, see [[!INCLUDE[prod_short](includes/prod_short.md)] Price Sheets](https://go.microsoft.com/fwlink/?LinkId=238341) (requires PartnerSource account). -->

Následující tabulka ukazuje, které granule jsou nutné k definování různých úrovní složitosti skladu, které dokumenty uživatelského rozhraní podporují každou úroveň a které kódy lokace odrážejí tyto úrovně v [!INCLUDE[prod_short](includes/prod_short.md)] demonstrační databázi.

[!INCLUDE [locations-cronus](includes/locations-cronus.md)]

| Úroveň složitosti | Popis | Dokument uživatelského rozhraní | Příklad lokace | Minimální požadavek na granule |
|----------------|-----------|-----------|---------------|---------------------------|  
| 1 | Žádná vyhrazená aktivita skladu.<br /><br /> Účtování příjmu/dodávky z objednávek. | Pořadí | MODRÝ | Základní zásoby |
| 2 | Žádná vyhrazená aktivita skladu.<br /><br /> Účtování příjmu/dodávky z objednávek.<br /><br /> Je vyžadován kód přihrádky. | Objednávka s kódem přihrádky | STŘÍBRNÝ | Základní zásoby/přihrádky |
| 3 <br /><br /> **NOTE**: I když se nastavení nazývá **Vyžadovat vyskladnění** a **Vyžadovat zaskladnění**, stále můžete účtovat příjemky a dodávky přímo ze zdrojových obchodních dokladů na místech, kde zaškrtnete tato políčka. | Základní aktivita skladu, zakázka-na-zakázku.<br /><br /> Účtování příjmu/dodávky z dokladu zaskladnění/vyskladnění zásob. <br /><br /> Je vyžadován kód přihrádky. | Zaskladnění zásob/Přesun zásob/Vyskladnění zásob s kódem přihrádky | (STŘÍBRNÝ + Vyžadovat zaskladnění nebo Vyžadovat zaskladnění) | Základní zásoby/Přihrádka/Zaskladnění/Vyskladnění |
| 4 | Pokročilá aktivita skladu pro více objednávek.<br /><br /> Konsolidované účtování příjmu/dodávky na základě registrací zaskladnění/vyskladnění. | Příjemka na sklad/Zaskladnění/Vyskladnění/Dodávka ze skladu/Sešit vyskladnění | ZELENÁ | Základní zásoby/Příjemka na sklad/Zaskladnění/Vyskladnění/Dodávka ze skladu |
| 5 | Pokročilá aktivita skladu pro více objednávek.<br /><br /> Konsolidované účtování příjmu/dodávky na základě registrací zaskladnění/vyskladnění.<br /><br /> Je vyžadován kód přihrádky. | Příjemka na sklad/Zaskladnění/Vyskladnění/Dodávka ze skladu/Sešit vyskladnění/Sešit zaskladnění s kódem přihrádky | (ZELENÁ + Přihrádka povinná) | Základní zásoby/Přihrádka/Příjemka na sklad/Zaskladnění/Vyskladnění/Dodávka ze skladu |
| 6 <br /><br /> **Note**: Tato úroveň se označuje jako "SSS", protože vyžaduje nejpokročilejší granule, Systém správy skladu. | Pokročilá aktivita skladu pro více objednávek<br /><br /> Konsolidované účtování příjmu/dodávky na základě registrací zaskladnění/vyskladnění<br /><br /> Kód přihrádky je vyžadován.<br /><br /> Kód zóny/třídy je nepovinný.<br /><br /> Pracovníci skladu řízeni pomocí workflow<br /><br /> Plánování doplnění přihrádky<br /><br /> Pořadí přihrádky<br /><br /> Nastavení přihrádky podle kapacity<br /><br /> Drážkování <!-- Hand-held device integration --> | Příjemka na sklad/Zaskladnění/Vyskladnění/Dodávka ze skladu/Skladový přesun/Sešit vyskladnění/Sešit zaskladnění/Interní  vyskladnění/Interní zaskladnění s kódem přihrádky/třídy/zóny<br /><br /> Různé sešity pro správu přihrádek<br /><br /> ADCS obrazovky | BÍLÝ | Základní zásoby/Přihrádka/Zaskladnění/Příjemka na sklad/Vyskladnění/Dodávka ze skladu/Systém správy skladu/Interní vyskladnění a zaskladnění/Nastavení přihrádky/<!-- Automated Data Capture System/ -->Nastavení přihrádky |

Příklady použití dokladů uživatelského rozhraní na úrovni složitosti skladu naleznete v tématu [Detaily návrhu: Vstupní procesy skladu](design-details-inbound-warehouse-flow.md).

## Přihrádky a jejich obsah

Přihrádka je úložné zařízení určené k tomu, aby obsahovalo samostatné součásti. Jedná se o nejmenší kontejnerovou jednotku v [!INCLUDE[prod_short](includes/prod_short.md)]. Množství zboží v přihrádce se označuje jako obsah přihrádky. Vyhledávání v poli **Zboží** nebo **Kód přihrádky** na libovolném řádku dokladu souvisejícího se skladem zobrazuje vypočítanou dostupnost zboží v přihrádce.

Obsah přihrádky může být dán vlastností Pevná, Vyhrazená nebo Výchozí, která definuje, jak lze obsah přihrádky použít. Přihrádky s žádnou z těchto vlastností se označují jako plovoucí přihrádky.

Pevná přihrádka obsahuje zboží, které je přiřazeno k danému kódu přihrádky. Vlastnost Pevná přihrádka zajišťuje, že i když je obsah přihrádky na okamžik vyprázdněn, obsah přihrádky nezmizí, a přihrádka je proto znovu vybrána, jakmile je doplněna.

Vyhrazená přihrádka obsahuje obsah přihrádky, který lze vybrat pouze pro vyhrazený prostředek, jako je například strojové centrum, které používá danou přihrádku. Další obsah, který není vyskladnění, například odchozí množství při zaúčtování dodávky, lze stále spotřebovat z vyhrazené přihrádky. Ve vyhrazené přihrádce je chráněn pouze obsah přihrádky považován za algoritmus **Vytvořit vyskladnění**.

Vlastnost Výchozí přihrádka používá systém k navrhování přihrádek pro činnosti skladu. Na lokacách SSS se nepoužívá vlastnost Výchozí přihrádka. V lokacích, kde jsou požadovány přihrádky, se vlastnost používá v příchozích tocích k určení umístění zboží. V odchozích tocích se vlastnost používá k určení, odkud má být zboží odváděno.

> [!NOTE]  
> Pokud je odchozí zboží umístěno v několika přihrádkách, pak je zboží nejprve převzato z jiných než výchozích přihrádek, aby se vyprázdnil obsah přihrádky, a pak je zbývající zboží převzato z výchozí přihrádky.

Na zboží na lokaci může být pouze jedna výchozí přihrádka.

## Typ přihrádky

V instalacích SSS můžete omezit aktivity skladu, které jsou pro přihrádku povoleny, tak, že ji přiřadíte typ přihrádky. Existují následující typy přihrádek:

| Typ přihrádky | Popis |
|------------------|---------------------------------------|  
| PŘÍJEM | Zboží zaúčtované jako přijaté, ale dosud nezaskladněné. |
| DODÁVKA | Zboží vybrané pro skladové řádky, ale dosud nebyly zaúčtovány jako dodávané. |
| VYSKL | Typicky zboží, které má být uloženo ve velkých měrných jednotkách, ale které nechcete zpřístupňovat pro vyskladnění. Protože se tyto přihrádky nepoužívají k vyskladnění, a to ani u výrobních objednávek a ani u zásilek, může být používání přihrádky typu Zaskladnění omezené, ale tento typ přihrádky může být užitečný, pokud jste zakoupili velké množství zboží. Přihrádky tohoto typu by měly mít vždy nižší pořadí přihrádek, takže když jsou přijaté položky zaskladněny, jsou nejprve vyřazeny další přihrádky ZASKLVYSKL s vyšším pořadím. Pokud používáte tento typ přihrádky, musíte pravidelně provádět doplňování přihrádky tak, aby položky uložené v těchto přihrádkách byly také k dispozici v přihrádkách typu ZASKLVYSKL nebo VYSKL. |
| VYSKL | Zboží, které má být použito pouze pro vyskladnění. Doplnění těchto přihrádek lze uskutečnit pouze přesunem, nikoli zaskladněním. |
| VYSKLZASKL | Zboží v přihrádkách, které jsou navrženy pro funkce vyskladněni a zaskladnění. Přihrádky tohoto typu pravděpodobně mají rozdílné pořadí přihrádek. Můžete nastavit své přihrádky jako objemné s nížším pořadím přihrádek ve srovnání s běžnými přihrádkami nebo přihrádkami pro vyskladnění. |
| KVAL | Tato přihrádka se používá pro úpravy zásob, pokud tuto přihrádku zadáte na kartě lokace v poli **Kód adjustační přihrádky**. Můžete také nastavit přihrádky tohoto typu pro vadné předměty a kontrolované položky. Položky můžete přesunout do tohoto typu přihrádky, pokud chcete, aby byly nepřístupné pro obvyklý tok položek. **Note:** Na rozdíl od všech ostatních typů přihrádek nemá typ přihrádky **KVAL** ve výchozím nastavení žádné zaškrtávací políčko pro manipulaci se zbožím. To znamená, že veškerý obsah, který umístíte do přihrádky KVAL, je z toků zboží vyloučen. |

Pro všechny typy přihrádek, s výjimkou VYSKL, VYSKLZASKL a ZASKL, není pro přihrádku povolena žádná jiná aktivita, než je definována typem přihrádky. Například přihrádku typu  **K příjmu** lze použít pouze k přijímání zboží nebo k vyskladnění zboží.

> [!NOTE]  
> Lze provést pouze přesun do přihrádek typu K PŘÍJMU a KVAL. Podobně lze z přihrádek typu DODÁVKA a KVAL uskutechovat pouze pohyby.

## Pořadí přihrádky

V pokročilém skladu můžete automatizovat a optimalizovat způsob sběru zboží v sešitech zaskladnění a vyskladnění podle přihrádek pro řazení, aby bylo zboží navrženo k sebraní nebo umístění podle kritérií pořadí pro optimální využití skladového prostoru.

Procesy zaskladnění jsou optimalizovány podle pořadí přihrádek navržením přihrádek s vyšším pořadím před přihrádky s nižším pořadím. Podobně jsou procesy vyskladnění optimalizovány tak, že nejprve navrhují zboží z obsahu přihrádky s vysokým pořadím přihrádky. Kromě toho se navrhuje doplňování přihrádek z přihrádek s nižším pořadím do přihrádek s vyšším pořadím.

Pořadí přihrádek spolu s informacemi o obsahu přihrádky jsou základní vlastnosti, které uživatelům umožňují ukládat zboží ve skladu.

## Nastavení přihrádky
V pokročilém nastavení skladu lze přihrádky nastavit s hodnotami kapacity, jako je množství, celkový objem a hmotnost, aby bylo možné řídit, které zboží a jak je tohl zboží uloženo v přihrádce.

Na každé kartě zboží můžete přiřadit měrnou jednotku (MJ) pro zboží, jako jsou kusy, palety, litry, gramy nebo krabice. Můžete mít také základní MJ pro zboží a zadat větší MJ, která je na ní založena. Můžete například definovat paletu, která se rovná 16 kusům, z toho kus je základní MJ.

Chcete-li nastavit maximální množství určitého zboží, které má být uloženo v jednotlivé přihrádce, a zboží má více než jednu MJ, musíte nastavit maximální množství pro každou MJ, která existuje na kartě zboží. V souladu s tím, pokud bylo zboží nastaveno tak, aby se s ním nakládalo po kusech a paletách, pak pole **Max.  množství** na stránce **Obsah přihrádky** pro toto zboží musí být také v kusech a paletách. V opačném případě není povolené množství pro tuto přihrádku vypočteno správně.

Před nastavením omezení kapacity pro obsah přihrádky se musíte nejprve ujistit, že na kartě zboží byla nastavena MJ a dimenze zboží.

> [!NOTE]  
> Pouze v instalacích SKL je možné pracovat s více MJ. U všech ostatních konfigurací může být obsah přihrádky pouze v základní MJ. Ve všech transakcích s MJ vyšší než základní MJ zboží se množství převede na základní MJ.

## Zóna

V pokročilých nastaveních skladu lze přihrádky seskupovat do zón, aby bylo možné řídit workflow skladových činností.

Zónou může být přijímací zóna nebo zóna skladování a každá zóna se může skládat z jedné nebo více přihrádek.

Většina vlastností přiřazených zóně bude ve výchozím nastavení přiřazena k přihrádce vytvořené z této zóny.

## Třída
V pokročilém nastavení skladu můžete přiřadit kódy tříd skladu ke zboží, přihrádkám a zónám, abyste mohli řídit, kde jsou uloženy různé třídy zboží, například zmrazené zboží. Zónu můžete rozdělit do několika tříd skladu. Například zboží v přijímající zóně může být uloženo jako zmrazené, nebezpečné nebo může mít jinou třídu.

Při práci s třídami skladu a výchozí přihrádkou pro příjem/dodávku je nutné ručně vyplnit příslušné přihrádky v řádcích příjemky a dodávky skladu.

U příchozích toků je kód třídy zvýrazněn pouze na příchozích řádcích, kde kód třídy zboží neodpovídá výchozí přihrádce příjmu. Pokud nejsou přiřazeny správné výchozí přihrádky, nelze množství přijmout.

## Lokace

Lokace je fyzická struktura nebo místo, kde jsou zásoby přijímány, skladovány a odesílány, případně uspořádány do přihrádek. Lokací může být sklad, služební vůz, předváděcí místnost, závod nebo plocha v závodě.

## FEFO (První expiruje, první ven)

Pokud zaškrtnete políčko **Vybrat na základě metody FEFO** na záložce **Použití přihrádek** na kartě lokace, budou položky sledování zboží vyskladněny podle data vypršení platnosti. Zboží s nejbližšími daty vypršení platnosti je vyskladněno jako první.

Aktivity skladu ve všech dokladech vyskladnění a přesunu jsou seřazeny podle FEFO, pokud předmětné zboží již nemá přiřazená sériová čísla/čísla šarží. Pokud již má sériové číslo/číslo šarže přiřazeno část množství na řádku, zbývající množství, které se má vyskladnit, je tříděno podle FEFO.

Při vyskladnění podle FEFO je dostupné zboží, kterého platnost vyprší jako první a toto zboží je shromážděno v dočasném seznamu sledování zboží na základě data vypršení platnosti. Pokud mají dva zboží stejné datum vypršení platnosti, je nejprve vybráno zboží s nejnižší šarží nebo sériovým číslem. Pokud jsou čísla šarže nebo sériová čísla stejná, bude nejprve vybráno zboží, které bylo zaregistrováno jako první. Pro tento dočasný seznam sledování zboží FEFO se použijí standardní kritéria pro výběr zboží v přihrádce vyskladnění, například Pořadí přihrádek a Hromadné přerušení.

## Šablona pro zaskladnění

Šablonu pro zaskladnění lze přiřadit ke zboží a lokaci. Šablona pro zaskladnění určuje sadu pravidel s prioritou, která musí být respektována při vytváření zaskladnění. Šablona pro zaskladnění může například vyžadovat, aby bylo zboží umístěno do přihrádky s obsahem přihrádky, který odpovídá MJ, a pokud nelze najít podobnou přihrádku s dostatečnou kapacitou, musí být zboží umístěno do prázdné přihrádky.

## Viz také

[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)     
[Detaily návrhu: Dostupnost ve skladu](design-details-availability-in-the-warehouse.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]