---
    title: About Production Orders | Microsoft Docs
    description: Production orders are used to manage the conversion of purchased materials into manufactured items. Production orders (job or work orders) route work through various facilities (work or machine centers) on the shop floor.
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
# Výrobní zakázky
Výrobní zakázky slouží ke správě přeměny zakoupených materiálů na vyráběné zboží. Výrobní zakázky vedou práce přes různá pracoviště nebo strojní centra v dílenském řízení.

Před zahájením výroby většina společností provádí plánování dodávek, obvykle jednou týdně, aby vypočítala, kolik výrobních zakázek a nákupních objednávek je třeba provést, aby se splnila poptávka po prodeji v daném týdnu. Nákupní objednávky dodávají komponenty, které jsou podle výrobního kusovníku potřebné k výrobě konečného zboží.

Výrobní zakázky jsou ústředními komponenty výrobní funkce aplikace a obsahují následující informace:

- Produkty plánované pro výrobu
- Materiály potřebné pro plánované výrobní zakázky
- Produkty, které byly právě vyrobeny
- Materiály, které již byly vybrány
- Produkty, které byly vyrobeny v minulosti
- Materiály použité v předchozích výrobních operacích

Výrobní zakázky jsou výchozím bodem pro:

- Plánování budoucí výroby
- Řízení aktuální výroby
- Sledování hotové výroby

## Vytvoření výrobní zakázky
Výrobní zakázky lze vytvářet na základě zpracování zboží po objednávkách a to ručně ze stránky **Výrobní zakázka** nebo je lze vygenerovat ze stránky **Plánování prod.objednávky** nebo **Plánování objednávek**. Ze stránky **Plánovací sešit** se vytvoří více objednávek.

Výrobní zakázky jsou vytvářeny pomocí informací z:

- Zboží
- Výrobní kusovníky
- Technologické postupy
- Strojní centra
- Pracovní centra

## Omezení tvorby výrobní zakázky
Výrobní zakázky jsou automaticky rezervovány a sledovány, pokud:

- Jsou vytvořeny z **Plánovacího sešitu**
- Jsou vytvořeny pomocí funkce Objednávka na stránce **Plánování prod.objednávky**
- Jsou vytvořeny ze stránky **Plánování objednávek**
- Jsou vytvořeny pomocí funkce **Přeplánovat** na výrobních zakázkách

Pro více informací navštivte [Sledování vztahů mezi poptávkou a dodávkou](production-how-track-demand-supply.md).

Výrobní zakázky vytvořené jinými prostředky nejsou automaticky rezervovány a sledovány.

## Stav výrobní zakázky
Stav výrobní zakázky určuje, jak se výrobní zakázka chová v rámci aplikace. Forma a obsah výroby jsou dány stavem objednávky. Výrobní zakázky se zobrazují na různých stránkách podle jejich stavu. Stav výrobní zakázky nelze změnit ručně. Musíte použít funkci **Změna stavu**.

### Simulovaná výrobní zakázka
Simulovaná výrobní zakázka je jedinečná na základě následujících vlastností:

- Jak již název napovídá, jedná se o simulaci a jejím hlavním účelem je poptávka a ocenění - například když oddělení výzkumu a vývoje chce získat odhad nákladů na navrhované zboží. Simulovaná výrobní zakázka slouží jako příklad výrobní zakázky.
- Nemá to vliv na plánování objednávek. Plánování (MPS a MRP) simulované výrobní zakázky nebere v úvahu ani je neovlivňuje. Simulovanou výrobní zakázku nelze použít jako šablonu, protože zmizí, když změníte její stav.

### Plánovaná výrobní zakázka
Plánovaná výrobní zakázka je jedinečná z důvodu následujících vlastností:

- Plánovanou výrobní zakázku můžete automaticky vytvořit z prodejní objednávky.
- Plánované výrobní zakázky jsou jako vydané výrobní zakázky a poskytují vstup do plánování požadavků na kapacitu zobrazením celkových požadavků na kapacitu podle pracovního nebo strojního centra.
- Plánovaná výrobní zakázka představuje nejlepší odhad budoucího zatížení pracovního centra nebo zatížení strojního centra na základě dostupných informací. Obvykle jsou generovány z plánování, ale lze je také vytvořit ručně. Vzhledem k tomu, že jsou výrobní zakázky vymazány během následných generací plánování, ruční vytváření není praktické.
- Jejich generování má za následek navrhované "plánované uvolnění objednávky"  ve výsledcích plánování, které zahrnuje množství, datum vydání a datum splatnosti. Logika plánovacího systému je založena na systému doplňování, zásadách přiobjednání a modifikátorů objednávek, s nimiž se setkává v procesu plánování požadavků.
- Chcete-li zobrazit jejich dopad, podívejte se na zatížení pro každé pracovní centrum nebo strojní centrum na technologickém postupu plánované výrobní zakázky.

### Pevně plánovaná výrobní zakázka
Pevně plánovaná výrobní zakázka je jedinečná z důvodu následujících vlastností:

- Z prodejní objednávky můžete automaticky vytvořit pevně plánovanou výrobní zakázku.
- Pevně plánovaná výrobní zakázka funguje jako zástupný symbol v plánu pro některé budoucí práce.
- Pevně ​​plánovanou výrobní zakázku lze vygenerovat z plánování, vytvořit ji ručně nebo z prodejních objednávek. Během následného plánování pak nejsou vymazány.
- Jejich generování má za následek navrhované „plánované uvolnění objednávky“ ve výsledcích plánování, které zahrnuje: množství, datum vydání a datum splatnosti. Logika plánovacího systému je založena na systému doplňování, zásadách přiobjednání a modifikátorů objednávek, s nimiž se setkává v procesu plánování požadavků.
- Chcete-li zobrazit jejich dopad, podívejte se na zatížení pro každé pracovní centrum nebo strojní centrum na trase pevně plánované výrobní zakázky.

### Vydaná výrobní zakázka
Vydaná výrobní zakázka je jedinečná na základě následujících vlastností:

- Vydanou výrobní zakázku můžete automaticky vytvořit z prodejní objednávky.
- Pokud byla výrobní zakázka vydána, nemusí to nutně znamenat, že materiály byly vyskladněny nebo že se úloha fyzicky přesunula do první operace.
- V prostředí MTO (Vyrobit-na-zakázku) není neobvyklé vytvořit vydanou výrobní zakázku bezprostředně po zadání prodejní objednávky.
- Skutečnou spotřebu materiálu a výstup produktu lze zaznamenat ručně pomocí vydané výrobní zakázky. Kromě toho dochází k automatickému vyprázdnění spotřeby a výstupu produktu pouze u vydaných výrobních zakázek.

### Dokončená výrobní zakázka
Dokončená výrobní zakázka je jedinečná na základě následujících vlastností:

- Dokončena výrobní zakázka je obvykle ta, která již byla vyrobena.
- Dokončení výrobní zakázky je důležitým úkolem při dokončení životního cyklu nákladů vyráběného zboží. Dokončením výrobní zakázky lze náklady upravit a odsouhlasit.
- Dokončené výrobní zakázky se používají pro statistické vykazování a pro podporu schopnosti zpětného sledování k jiným objednávkám (například prodej, výroba a nákup). Možnost zpětného sledování k dokončené výrobní zakázce umožňuje zkontrolovat podrobnou historii.
- Dokončené výrobní zakázky nelze nikdy změnit.

## Provádění výrobní zakázky
Jakmile je výrobní zakázka vytvořena a naplánována, musí být vydána do dílenského řízení, aby byla provedena. Při provádění objednávky zaznamenáváte:

- Vybírané nebo spotřebované materiály
- Kolik času bylo věnováno práci na zakázce
- Vyrobené množství nadřazené položky

Tyto informace lze zaznamenávat ručně nebo prostřednictvím automatického vykazování podle nastavení zboží v poli Metoda spotřeby.

### Spotřeba materiálu
Tato aplikace nabízí řadu možností, jak může výrobní společnost chtít zaznamenat spotřebu materiálu. Například může být spotřeba materiálu zaznamenána ručně, což by mohlo být žádoucí, pokud dochází k častým náhradám komponent nebo k vyšším než očekávaným zmatkům.

Spotřeba materiálů může být zpracována prostřednictvím deníku spotřeby, ale může být také zaznamenána automaticky pomocí aplikace, známé jako automatické vykazování. Metody vykazování jsou:

- Ručně
- Dopředu
- Zpětně

Ruční vykazování spotřeby používá deník spotřeby k určení výdeje materiálu.

Vykazování dopředné spotřeby předpokládá, že očekávané množství všech materiálů pro celou objednávku je spotřebováno při dodání výrobní zakázky, pokud nepoužijete kódy vazby TNG postupu. Při použití kódů vazby TNG postupu se materiál spotřebovaný po začátku operačního kroku zaznamená do deníku výstupu. Chcete-li předat vyprázdnění celé výrobní zakázky, musíte provést dvě věci:

- U všeho zboží v kusovníku nejvyšší úrovně výroby musí být na příslušné kartě zboží vybrána možnost předběžného vyprazdňování.
- Všechny kódy vazby TNG postupu ve výrobním kusovníku musí být odebrány.

Sestava zpětné spotřeby zaznamenává skutečné množství veškerého vyskladněného nebo spotřebovaného materiálu při změně stavu výrobní zakázky na *Dokončeno*, pokud nepoužíváte kódy vazby TNG postupu. Při použití kódů vazby TNG postupu je materiál spotřebován po zaznamenání množství nadřazeného zboží pro provozní krok v deníku výstupu.

Při aktualizaci výrobní zakázky je metoda spotřeby zkopírována z karty zboží. Vzhledem k tomu, že metoda spotřeby pro každou komponentu výrobní zakázky určuje, jak a kdy je spotřeba zaznamenána, je důležité si uvědomit, že můžete změnit metodu spotřeby pro určité zboží přímo ve výrobní zakázce.

#### Automatické účtování spotřeby (Spotřeba)
Výhodou automatické spotřeby je to, že výrazně snižuje zadávání dat. Díky možnosti automatické spotřeby lze automatizovat celý proces záznamu spotřeby a výstupu. Nevýhodou použití automatické spotřeby je, že nemusíte přesně zaznamenávat, nebo dokonce znát množství zmatků. Metody automatického vykazování jsou:

- Dopředné vyprázdnění celé zakázky
- Dopředné vyprázdnění podle operace
- Zpětné vyprázdnění podle operace
- Zpětné vyprázdnění celé zakázky

#### Automatické vykazování - Dopředné vyprázdnění celé zakázky
Pokud využijete dopředné vyprázdnění výrobní zakázky na začátku zakázky, je chování aplikace velmi podobné ruční spotřebě. Hlavní rozdíl spočívá v tom, že ke spotřebě dochází automaticky.

- Celý obsah produkčního kusovníku je spotřebován a odečten ze zásob v době, kdy je vydána výrobní zakázka obnovena.
- Množství spotřeby je množství na montáž uvedené na výrobním kusovníku vynásobené počtem nadřazeného zboží, které zestavujete.
- Není nutné zaznamenávat žádné informace v deníku spotřeby, pokud má být všechno zboží vyprázdněno.
- Když spotřebováváte zboží ze zásob, nezáleží na tom, kdy jsou prováděny položky deníku výstupu, protože deník výstupu nemá žádný vliv na tento způsob účtování spotřeby.
- Nelze nastavit žádné kódy vazby TNG postupu.

Předběžné vyprazdňování celé objednávky je vhodné v produkčním prostředí s:

- Nízkým počtem vad
- Nízkým početem operací
- Vysokou spotřebou komponent v skorších operacích

#### Automatické vykazování - Dopředné vyprázdnění podle operace
Vyprázdnění podle operace vám umožňuje odečíst zásoby během konkrétní operace ve směrování nadřazeného zboží. Materiál je vázán na TNG pomocí kódů vazby TNG postupu, které odpovídají kódům vazby TNG použitým na komponenty v produkčním kusovníku.

Vyprázdnění probíhá při spuštění operace, která má stejný kód vazby TNG postupu. Spuštění znamená, že některé aktivity jsou zaznamenány v deníku výstupu pro tuto operaci. A tou aktivitou může být jen zadání času nastavení.

Množství vyprázdnění je pro množství na montáž uvedené na výrobním kusovníku vynásobené počtem vytvořeného nadřazeného zboží (očekávané množství).

Tato technika se nejlépe používá, když existuje mnoho operací a některé komponenty jsou potřeba až do pozdní montáže. Ve skutečnosti nastavení just-in-time (za běhu) nemusí mít ani zboží na skladě při zahájení RPO.

Materiál může být spotřebován během operací pomocí kódů vazby TNG postupu. Některé komponenty mohou být použity až po konečné montážní operaci a do té doby by neměly být staženy ze skladu.

#### Automatické vykazování - Zpětné vyprázdnění podle operace
Zpětné vyprázdnění podle operace zaznamenává spotřebu po zaúčtování operace do deníku výstupu.

Výhodou této metody je, že je znám počet nadřazených částí dokončených v operaci.

Materiál ve výrobním kusovníku je propojen se záznamy technologického postupu pomocí kódů vazby TNG postupu. Zpětné vyprázdnění probíhá, když je operace s určitým kódem vazby TNG postupu zaúčtována s dokončeným množstvím.

Množství vyprázdnění je pro množství na montáž uvedené na výrobním kusovníku vynásobené počtem nadřazeného zboží, které bylo v této operaci zaúčtováno jako výstupní množství. To se může lišit od očekávaného množství.

#### Automatické vykazování - Zpětné vyprázdnění celé zakázky
Tato metoda vykazování nebere v úvahu kódy vazeb TNG.

Dokud se stav vydané výrobní zakázky nezmění na *Dokončeno*, nebudou vyskladněny žádné komponenty. Množství vyprázdnění je množství na montáž uvedené na výrobním kusovníku vynásobené počtem nadřazeného zboží, které bylo dokončeno a umístěno do skladu.

Zpětné vyprázdnění celé výrobní zakázky vyžaduje stejné nastavení jako pro dopřední vyprázdnění: Metoda vykazování musí být nastavena na zpětnou hodnotu na každé kartě zboží pro všechny položky v rámci nadřazeného kusovníku, které mají být vykázány. Kromě toho musí být všechny kódy vazby TNG odebrány z výrobního kusovníku.

### Výstup výroby
Tato aplikace vám kromě zaznamenávání vyrobeného množství umožňuje sledovat, kolik času strávíte prací na výrobní zakázce. Tyto informace vám mohou pomoci přesněji určit výrobní náklady. Výrobci, kteří používají systém standardních nákladů, mohou také chtít zaznamenávat skutečné informace, aby jim pomohli vyvinout lepší standardy.

Výstup může být zpracován prostřednictvím deníku výstupu, ale může být také zaznamenán automaticky pomocí aplikace. Aplikace zkopíruje metodu vyprázdnění z karty strojního nebo pracovního centra do postupu výrobní zakázky při aktualizaci. Stejně jako u spotřeby materiálu existují tři způsoby vykazování výstupu:

- Ručně
- Dopředu
- Zpětně

Ruční metoda používá deník výstupu k určení spotřebovaného času a vyrobeného množství.

Dopřední metoda zaznamenává očekávaný výstup (a čas), který je automaticky zaznamenán při vydání výrobní zakázky. Kódy vazby TNG postupu nejsou faktorem ve výstupu předběžného vyprazdňování.

Zpětná metoda zaznamenává očekávaný výstup (a čas), který je automaticky zaznamenán na konci výrobní zakázky. Kódy vazby TNG postupu nejsou faktorem výstupu zpětného vyprázdnění.

### Účtování spotřeby a výstupu
Pro spotřebu i výkon můžete použít libovolnou kombinaci automatického vyprázdnění a ručně zaznamenaných informací. Například můžete chtít automaticky přeposílat vyprázdněné komponenty, ale stále můžete použít záznam deníku spotřeby. Podobně můžete chtít automaticky zaznamenat výstup, ale použít deník výstupu k zaznamenání zbytku nadřazeného zboží nebo dodatečného času stráveného na objednávce.

Nakonec, pokud zadáte spotřebu a výstup ručně, je třeba určit pořadí, ve kterém budete zaznamenávat tyto informace. Nejprve můžete zaznamenat spotřebu a pomocí metody klávesových zkratek zadat informace, které jsou založeny na očekávaném množství výstupu. Nebo můžete nejprve zadat výstup pomocí funkce **Rozbalit postup**. Poté byste zaznamenali spotřebu na základě skutečného množství výstupu.

### Deník výroby
Deník výroby kombinuje funkce deníku spotřeby a deníků výstupů do jednoho deníku, který je přístupný přímo z vydané výrobní zakázky.

Účelem deníku výroby je poskytnout jediné rozhraní pro registraci spotřeby a výstupu z výrobní zakázky.

Deník výroby má jednoduché zobrazení a poskytuje možnost:

- Snadné zaznamenání výstupu a spotřeby související s výrobní zakázkou
- Propojení komponenty s operacemi
- Propojení dat skutečné operace se standardními odhady na řádcích TNG postupu výrobní zakázky a komponenty
- Zaúčtování a vytisknutí přehledu registrovaných provozních dat pro výrobní zakázku

Deník výroby provádí mnoho stejných funkcí jako deníky Spotřeby a Výstupu. Dimenze, Sledování zboží a Obsah přihrádky jsou zpracovány stejným způsobem jako v denících spotřeby a výstupu.

Deník výroby se však liší od deníků spotřeby a výstupu následujícími způsoby:

- Je volán přímo z řádku vydané výrobní zakázky a přednastaven s příslušnými údaji.
- To vám umožní definovat, které typy komponent zpracovat na základě filtru metody vyprázdnění v deníku.
- Množství a časy již zaúčtované pro zakázku jsou zobrazeny v dolní části deníku jako skutečné položky.
- Pole, ve kterých je zadávání dat irelevantní, jsou prázdná a nelze je upravovat.
- Uživatel může nastavit způsob, jakým jsou množství výstupu v deníku přednastavena - například, že poslední operace musí mít jako výstupní množství nulu.
- Pokud deník ukončíte bez zaúčtování změn, zobrazí se zpráva požadavku, která vám umožní zůstat v deníku.
- Zobrazuje operace a komponenty společně v logické struktuře, která poskytuje přehled o výrobním procesu.

V deníku výroby jsou množství spotřeby zaúčtována jako záporné položky zboží, množství výstupu je zaúčtováno jako kladné položky a vynaložené časy jsou zaúčtovány jako položky kapacity.

## Viz také
[Výroba](production-manage-manufacturing.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
