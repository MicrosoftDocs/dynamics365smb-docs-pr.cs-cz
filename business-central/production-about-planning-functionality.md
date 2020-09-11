---
    title: About Planning Functionality | Microsoft Docs
    description: The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# O funkcích plánování
Plánovací systém bere v úvahu všechna data o nabídce a poptávce, výsledky porovnává a vytváří návrhy pro vyvažování nabídky, aby byla uspokojena poptávka.

Podrobné informace naleznete v [Detaily návrhu: Plánování dodávek](design-details-supply-planning.md).

> [!NOTE]
> Pro všechna pole, která jsou uvedena v tomto tématu, si přečtěte popisy, abyste porozuměli jejich funkci. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Poptávka a nabídka
Plánování má dva prvky: poptávku a nabídku. Ty musí být udrženy v rovnováze, aby bylo zajištěno, že poptávka bude uspokojená včas a nákladově efektivním způsobem.

- Poptávka je běžný termín používaný pro jakýkoli druh hrubého požadavku, jako je prodejní objednávka, servisní objednávka, potřeba součásti od montážních nebo výrobních objednávek, výstupní transfer, plošná objednávka nebo předpověď. Kromě toho aplikace umožňuje některé další technické typy poptávky - například zápornou výrobní nebo nákupní objednávku, záporné zásoby a nákupní vratku.
- Nabídka je běžné slovo používané pro jakýkoli druh doplňování, jako jsou zásoby, nákupní objednávka, Montážní zakázka, výrobní objednávka, nebo vstup transferu. Odpovídajícím způsobem, může existovat záporná prodejní nebo servisní zakázka, záporná potřeba komponent nebo prodejní vratka – to vše nějakým způsobem také představuje dodávku.

Dalším cílem plánování je zajistit, aby zásoby zbytečně nerostly. V případě klesající poptávky systém plánování navrhne odložení, snížení množství nebo zrušení existujících objednávek doplnění.

## Výpočet plánování
Plánovací systém je řízen očekávanou a skutečnou poptávkou zákazníka, stejně jako parametry pro přiobjednání zásob. Spuštění výpočtu plánování bude mít za následek, že aplikace navrhne konkrétní akce (Zprávy akcí), které se budou brát v souvislosti s možným doplněním od dodavatelů, převody mezi sklady nebo výrobou. Pokud již existují objednávky doplnění, navrhované akce by mohly být zvýšení nebo urychlení objednávek ke splnění změn v poptávce.

Základem plánovací rutiny je výpočet hrubého zisku. Síťové požadavky řídí plánované uvolňování objednávek, které jsou naplánovány na základě informací o TNG postupech (vyrobené položky) nebo dodací lhůty karty zboží (zakoupené položky). Množství plánovaného uvolnění objednávky jsou založena na výpočtu plánování a jsou ovlivněna parametry nastavenými na jednotlivých kartách zboží.

## Plánování s Ručními Objednávkami transferu
Jak můžete vidět z pole **Systém doplnění** na kartě SKJ, systém plánování lze nastavit tak, aby vytvářel převodní příkazy pro vyvážení nabídky a poptávky mezi lokacemi.

Jako doplněk k těmto automatizovaným převodním příkazům, může být někdy nutné provést obecný přesun množství zásob do jiného umístění bez ohledu na existující poptávku. Za tímto účelem byste ručně vytvořili převodní příkaz k převodu množství, které chcete přesunout. Aby se zajistilo, že se plánovací systém nebude pokoušet manipulovat s tímto příkazem pro ruční přenos, musíte v řádcích transferu nastavit **Pružnost plánování** na řádku převodu na žádné.

Pokud naopak chcete, aby plánovací systém přizpůsobil množství a data převodních příkazů existující poptávce, musíte nastavit pole **Pružnost plánování** na výchozí hodnotu, Neomezená.

## Parametry plánování
Parametry plánování určují, kdy, kolik a jak doplnit na základě různých nastavení na kartě zboží (nebo skladové jednotce -SKJ) nastavení výroby.

Na kartě položky nebo kartě SKJ existují následující parametry plánování:

- Období prodlevy
- Množství prodlevy
- Způsob přiobjednání
- Bod přiobjednání
- Maximální zásoby
- Úroveň přetečení
- Časový interval
- Období shromáždění šarží
- Období přeplánování
- Přiobjednané množství
- Bezpečná průběžná doba
- Minimální zásoby
- Způsob montáže
- Způsob výroby

Na kartě položky nebo kartě SKJ existují následující modifikátory objednávky:

- Minimální množství objednávky
- Maximální množství objednávky
- Násobek objednávky

Pole globálního nastavení plánování na stránce **Nastavení výroby** obsahují:

- Dynamický kód nižší úrovně
- Aktuální prognóza poptávky
- Použití prognózy na místech
- Výchozí bezp.průběžná doba
- Prázdná úroveň přetečení
- Kombinovaný výpočet MPS/MRP
- Komponenty v lokaci
- Výchozí doba prodlevy
- Výchozí doba utlumení

Pro více informací navštivte [Detaily návrhu: Parametry plánování](design-details-planning-parameters.md).

## Další důležitá pole plánování
### Pružnost plánování
U většiny objednávek dodávek, jako jsou výrobní zakázky, můžete na řádcích zvolit **Neomezeno**, nebo **Žádné** a to, v poli **Flexibilita plánování**

To určuje, zda je dodávka reprezentovaná řádkem výrobní zakázky zvažována plánovacím systémem při výpočtu zpráv akcí.
Pokud pole obsahuje **Neomezeno**, pak bude plánovacím systémem brán v úvahu při zpracování akce hlášení. Pokud pole obsahuje **Žádné**, pak je řádek pevný, neměnný a systém plánování ho nebere v úvahu při zpracování akce hlášení.

### Varování
Informační pole **Varování** na stránce **Sešity plánování** vás informuje o jakékoliv plánovacím řádku vytvořeném pro neobvyklou situaci s textem, kterou si uživatel může vybrat, aby si přečetl další informace.  Existují následující typy upozornění:

- Nouzové
- Výjimka
- Pozornost
- Nouzové

Nouzové varování se zobrazuje ve dvou situacích:

- Zásoby jsou záporné k počátečnímu datu plánování.
- Existují neaktuální nabídky nebo poptávky.

Pokud jsou zásoby položky k počátečnímu datu plánování záporné, systém plánování navrhne nouzovou objednávku dodávky pro záporné množství, které má být doručeno k počátečnímu datu plánování. Text upozornění uvádí počáteční datum a množství nouzové objednávky.

Všechny řádky dokladu s daty splatnosti před datem zahájení plánování jsou sloučeny do jedné objednávky nouzové dodávky, aby zboží dorazilo k počátečnímu datu plánování.

### Výjimka
Varování o výjimce se zobrazí, pokud plánované dostupné zásoby klesnou pod množství bezpečného materiálu.

Plánovací systém navrhne objednávku na dodávky, které uspokojí poptávku v den splatnosti. Varovný text uvádí množství bezpečnostního materiálu a datum, kdy došlo k jeho porušení.

Porušení úrovně bezpečných zásob je považováno za výjimku, protože by nemělo nastat, pokud byl správně nastaven bod přiobjednání.

> [!NOTE]
> Dodávka na plánovacích řádcích s výjimkami se obvykle nemění podle parametrů plánování. Místo toho plánovací systém pouze navrhuje dodávku, která pokryje přesné množství poptávky. Můžete však nastavit běh plánování tak, aby respektoval určité parametry plánování pro plánování řádků s určitými varováními. Pro více informací navštivte “Parametry plánování Respektování výjimek varování” v části Vypočet plánu- Plán. sešit

### Pozornost
Varování pozornosti se zobrazuje ve dvou situacích:

- Počáteční datum plánování je dřívější než pracovní datum.
- Řádek plánování navrhuje změnit uvolněnou nákupní nebo výrobní zakázku.

> [!NOTE]
> V plánování řádků s výstrahami není vybráno pole **Přijmout hlášené akce**, protože se očekává, že plánovač tyto řádky před provedením plánu dále prozkoumá.

## Viz také
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)  
[Plánování](production-planning.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
