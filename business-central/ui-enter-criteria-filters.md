---
title: 'Řazení, vyhledávání a filtrování seznamů | Microsoft Docs'
description: 'Pracujte efektivně v seznamech tím, že prohledáváte data, řadíte sloupce a zpřesňujete výsledky pomocí výkonných symbolů filtru a klávesových zkratek.'
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.date: 01/09/2020
ms.reviewer: v-zdbice
ms.author: jswymer
---

# Řazení, vyhledávání a filtrování seznamů

Existuje několik věcí, které můžete udělat, aby vám pomohly prohlížet, najít a omezit záznamy v seznamu nebo v sestavě či XML portu. Patří sem řazení, vyhledávání a filtrování. Některé nebo všechny z nich můžete použít současně pro rychlé nalezení nebo analýzu vašich dat.

U sestav a XML portů můžete nastavit filtry jako v seznamech, aby bylo možné určit, která data mají být zahrnuta do sestavy nebo XML portu, ale nemůžete data řadit a prohledávat.

> [!TIP]
> Při prohlížení dat jako dlaždic můžete vyhledávat a používat základní filtrování. Chcete-li použít kompletní řadu výkonných funkcí pro třídění, vyhledávání a filtrování, vyberte ikonu ![Zobrazit jako seznam](media/ui_show_as_list_icon.png "Zobrazit jako seznam") pro zobrazení dat jako seznamu.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## Řazení

Řazení vám usnadňuje dostat rychlý přehled o vašich datech. Máte-li například mnoho zákazníků, můžete je řadit podle **Čísla zákazníka**, **Účto skupiny zákazníka**, **Kódu měny**, **Kódu zěmě/oblasti** nebo **DIČ**, abyste dostali přehled, který potřebujete.

Chcete-li seřadit seznam, můžete buď zvolit text záhlaví sloupce pro přepínání mezi vzestupným a sestupným pořadí, nebo zvolit malou šipku dolů v záhlaví sloupce a poté zvolit **Vzestupně** nebo **Sestupně**.  

> [!NOTE]  
> Řazení není podporováno pro obrázky, pole typu BLOB, dynamické filtry (FlowFilters) a pole, která nepatří do tabulky.  

## Vyhledávání

<!--## Searching by using the Quick Filter -->

V horní části každé stránky seznamu je ikona ![Prohledat seznam](media/ui-search/search-list.png "Prohledat seznam") **Hledat**, která poskytuje rychlý a snadný způsob, jak redukovat záznamy v seznamu a zobrazit pouze ty záznamy, které obsahují data, která chcete vidět.

Chcete-li hledat, jednoduše vyberte ikonu vyhledávání a potom do pole zadejte hledaný text. Můžete zadat písmena, čísla a další symboly.

### Doladění vyhledávání

Obecně se vyhledávání pokusí vyhledat text ve všech polích. Nerozlišuje mezi malými a velkými písmeny (case insensitive) a bude vyhledávat text umístěný kdekoli v poli (na začátku, na konci nebo uprostřed).

Přesnější vyhledávání však můžete provést pomocí následujících speciálních znaků:

- Chcete-li najít pouze hodnoty polí, které přesně odpovídají celému textu a velikosti písmen, umístěte hledaný text mezi jednoduché uvozovky `''` (například `'man'`).

- Chcete-li najít hodnoty polí, které začínají určitým textem a odpovídají velikosti písmen, umístěte `*` za hledaný text (například `man*`).

- Chcete-li najít hodnoty polí, které končí určitým textem a odpovídají velikosti písmen, umístěte `*` před hledaný text (například `*man`).

- Při použití `''` nebo `*` se při vyhledávání rozlišují malá a velká písmena. Pokud chcete, aby vyhledávání nerozlišovalo malá a velká písmena, umístěte `@` před hledaný text (například `@man*`).

V následující tabulce jsou uvedeny některé příklady, které vysvětlují, jak můžete vyhledávání použít.

|Kritéria vyhledávání|Najde...|
|--------------------|------- |
|`man`<br />nebo <br />`Man`|Všechny záznamy s poli, které obsahují text **man** bez ohledu na malá a velká písmena. Například **Manchester**, **manual** nebo **Sportsman**.|
|`'Man'`|Všechny záznamy s poli, které obsahují text **Man** s ohledem na malá a velká písmena.|
|`Man*`|Všechny záznamy s poli, které začínají textem <b>Man</b> s ohledem na malá a velká písmena. Například **Manchester**, ale ne **manual** nebo **Sportsman**.|
|`@Man*`|Všechny záznamy s poli, které začínají na **man** bez ohledu na malá a velká písmena. Například **Manchester**, **manual**, ale ne **Sportsman**.|
|`@*man`|Všechny záznamy, které končí na **man** bez ohledu na malá a velká písmena. Například  **Sportsman**, ale ne **Manchester** nebo **manual**.|

> [!TIP]
> Stisknutím F3 můžete aktivovat nebo deaktivovat vyhledávací pole. Další informace naleznete v [Klávesové zkratky](keyboard-shortcuts.md#KeyboardFilter).

## <a name="filtering"> </a>Filtrování

Filtrování poskytuje pokročilejší a všestrannější způsob řízení, které záznamy se zobrazují v seznamu nebo jsou zahrnuty do sestavy či XML portu. Mezi vyhledáváním a filtrováním existují dva hlavní rozdíly, jak je popsáno v následující tabulce.

||**Vyhledávání**|**Filtrování**|
|--|------------|------------|
|**Použitelná pole**|Prohledává všechna pole, která jsou viditelná na stránce.|Filtruje jedno nebo více polí jednotlivě a vybírá z kteréhokoli pole v tabulce, včetně polí, která nejsou na stránce viditelná.|
|**Shoda**|Zobrazuje záznamy s poli, která odpovídají hledanému textu, bez ohledu na malá a velká písmena nebo umístění tohoto textu.|Zobrazuje záznamy, kde pole přesně odpovídá filtru a rozlišuje velká a malá písmena, pokud nejsou zadány speciální symboly filtru.|

Filtrování umožňuje zobrazit záznamy pro konkrétní účty nebo zákazníky, data, částky a další informace zadáním kritérií filtru. Zobrazí se pouze záznamy, které odpovídají kritériím, se zobrazí v seznamu nebo jsou zahrnuty do sestavy, dávkové úlohy či XML portu. Pokud zadáte kritéria pro více polí, zobrazí se pouze záznamy, které odpovídají všem kritériím.

U seznamů jsou filtry zobrazeny na podokně filtrů, který se po aktivaci zobrazí na levé straně seznamu. U sestav, dávkových úloh a XML portů jsou filtry viditelné přímo na stránce dialogu.

### Filtrování pomocí polí typu Volba (Option)

U „běžných“ polí, která obsahují data, datum nastavení nebo obchodní data, můžete nastavit filtry výběrem dat i zadáním hodnot filtru a pomocí symbolů můžete definovat pokročilá kritéria pro filtrování. Další informace naleznete v části [Zadávání kritérií filtru](ui-enter-criteria-filters.md#entering-filter-criteria).

Pro pole typu **Option** však můžete nastavit filtr pouze výběrem jedné nebo více možností z rozevíracího seznamu dostupných voleb. Příkladem pole typu Volba (Option) je pole **Stav** na stránce **Prodejní objednávky**.

### Nastavení filtrů v seznamech

V seznamech nastavujete filtry pomocí podokna filtrů. Chcete-li zobrazit podokno filtru pro seznam, vyberte rozevírací šipku vedle názvu stránky a poté vyberte akci **Zobrazit podokno filtru**. Případně stiskněte **Shift+F3**.

Chcete-li zobrazit podokno filtru pro sloupec v seznamu, vyberte rozevírací šipku a poté vyberte akci **Filtr**. Případně stiskněte **Shift+F3**. Otevře se podokno filtru s vybraným sloupcem zobrazeným jako pole filtru v sekci **Seznam filtrů podle**.

Podokno filtru zobrazuje aktuální filtry seznamu a umožňuje vybrat vlastní filtry do jednoho nebo více polí výběrem akce **+ Filtr**.

Podokno filtru je rozděleno do tří částí: **Pohledy**, **Filtrovat seznam** a **Filtrovat součty**:

- **Pohledy**

  Některé seznamy obsahují sekci **Pohledy**. Pohledy jsou varianty seznamu, které byly předkonfigurovány pomocí filtrů. V seznamu můžete definovat a uložit tolik pohledů, kolik chcete, a tato zobrazení budou k dispozici na jakémkoli zařízení, ke kterému se přihlásíte. Další informace viz [Ukládaní a přizpůsobení zobrazení seznamů](ui-views.md).

- **Filtrovat seznam dle**

   Zde přidáte filtry na konkrétní pole, abyste snížili počet zobrazených záznamů. Chcete-li přidat filtr, vyberte akci **+ Filtr**, zadejte název pole, podle kterého chcete seznam filtrovat, nebo vyberte pole z rozevíracího seznamu.

- **Filtrovat součty dle**

  Některé seznamy, které zobrazují vypočtená pole, například částky a množství, budou zahrnovat sekci **Filtrovat součty dle**, kde můžete upravit různé dimenze, které ovlivňují výpočty. Chcete-li přidat filtr, vyberte akci **+ Filtr**, zadejte název pole, podle kterého chcete seznam filtrovat, nebo vyberte pole z rozevíracího seznamu.

 > [!NOTE]
 > Filtry v sekci **Filtrovat součty dle** jsou řízeny pomocí FlowFilters při návrhu stránky. Technické informace viz [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Jednoduchý filtr můžete nastavit přímo v seznamu pomocí podokna filtrů, konkrétně filtru, který zobrazuje pouze záznamy se stejnou hodnotou jako ve vybrané buňce. Vyberte buňku v seznamu, vyberte rozevírací šipku a poté vyberte akci **Filtr na tuto hodnotu**. Případně stiskněte **Alt+F3**.

### Nastavení filtrů v sestavách, dávkových úlohách a XML portech

U sestav a XML portů jsou filtry viditelné přímo na stránce dialogu. Na stránce dialogu se zobrazí poslední použité filtry podle vašeho výběru v poli **Použít výchozí hodnoty z**. Další informace naleznete v části [Používání uložených nastavení](ui-work-report.md#SavedSettings).

Hlavní část **Filtr** zobrazuje výchozí pole filtru, která používáte k vymezení záznamů, které mají být zahrnuty do sestavy nebo XML portu. Chcete-li přidat filtr, vyberte akci **+ Filtr**, zadejte název pole, podle kterého chcete filtrovat, nebo vyberte pole z rozevíracího seznamu.

V sekci **Filtrovat součty dle** můžete upravit různé dimenze, které ovlivňují výpočty v sestavě nebo XML portu. Chcete-li přidat filtr, vyberte akci **+ Filtr**, zadejte název pole, podle kterého chcete filtrovat, nebo vyberte pole z rozevíracího seznamu.

## <a name="entering-filter-criteria"> </a>Zadávání kritérií filtru

V podokně filtru i na stránce dialogu zadáte kritéria filtru do pole pod filtrovaným polem.

Typ filtrovacího pole určuje, která kritéria můžete zadat. Například filtrování pole s pevnými hodnotami vám umožní pouze vybrat z těchto hodnot. Další informace o speciálních symbolech filtrů naleznete v části [Kritéria filtrů](#FilterCriteria) a [Tokeny filtrů](#FilterTokens).

Sloupce, které již mají filtry, jsou v záhlaví sloupce označeny ikonou ![Filter icon](media/ui-search/filter-icon.png "Ikona filtru"). Chcete-li odebrat filtr, vyberte rozevírací šipku a poté vyberte akci **Vymazat filtr**.

> [!TIP]
> Zrychlete vyhledávání a analýzu dat pomocí kombinací klávesových zkratek. Například vyberte pole, použijte **Shift+Alt+F3** k přidání tohoto pole do podokna filtru, zadejte kritéria filtru, použijte **Ctrl+Enter** pro návrat do řádků, vyberte jiné pole a použijte k tomu filtru **Alt+F3**. Další informace viz [Klávesové zkratky](keyboard-shortcuts.md#KeyboardFilter).

### <a name="FilterCriteria"> </a>Kritéria a symboly filtrů

Při zadávání kritérií můžete použít všechna čísla a písmena, která můžete v poli normálně použít. Kromě toho můžete k dalšímu filtrování výsledků použít speciální symboly (nebo operátory). Následující tabulky ukazují symboly, které lze použít ve filtrech. Další informace o datech a časech naleznete také v části [Práce s kalendářními daty a časy](ui-enter-date-ranges.md) for more detailed information.

> [!IMPORTANT]  
> Mohou nastat případy, kdy hodnoty polí obsahují tyto symboly a chcete je filtrovat. Chcete-li to provést, musíte do uvozovek ('') zahrnout vzorec filtru, který obsahuje symbol. Pokud například chcete filtrovat záznamy, které začínají textem *S&R*, je vzorec filtru `'S&R*'`.

Následující oddíly popisují, jak používat různé operátory.

> [!NOTE]
> Pokud je v jednom filtru více než 200 operátorů, systém za účelem zpracování automaticky seskupí některé vzorce v závorkách `()`. To nemá žádný vliv na filtr ani na výsledky.

#### (..) Interval

|Ukázka vzorce|Zobrazené záznamy|
|-----------------------|-----------------------|
|`1100..2100`|Čísla 1100 až 2100|
|`..2500`|Do 2500 včetně|
|`..31 12 00`|Data do 31.12.00 včetně|
|`P8..`|Informace pro účetní období 8 a následující|
|`..23`|Od začátku do 23. aktuálního měsíce v aktuálním roce 23:59:59|
|`23..`|Od 23. aktuálního měsíce aktuálního roku 0:00:00 do konce času|
|`22..23`|Od 22. aktuálního měsíce aktuálního roku 0:00:00 do 23. aktuálního měsíce aktuálního roku 23:59:59|

#### (&#124;) Buď a nebo

|Ukázka vzorce |Zobrazené záznamy|
|-----------------------|-----------------------|
|`1200|1300`|Čísla 1200 nebo 1300|

#### (<>) Není rovno

|Ukázka vzorce|Zobrazené záznamy|
|-----------------------|-----------------------|
|`<>0`|Všechna čísla kromě 0 <br /><br /> Volba SQL serveru umožňuje kombinovat tento symbol s vzorceem zástupných znaků. Například <>A* znamená, že se nerovná žádnému textu, který začíná na A.|

#### (>) Větší než

|Ukázka vzorce|Zobrazené záznamy|
|-----------------------|-----------------------|
|`> 1200`|Čísla větší než 1200|

#### (> =) Větší než nebo rovno

|Ukázka vzorce|Zobrazené záznamy|
|-----------------------|-----------------------|
|`>=1200`|Čísla větší nebo rovnající se 1200|

#### (<) Menší než

|Ukázka vzorce|Zobrazené záznamy|
|--------------|--------------------|
|`<1200`|Čísla menší než 1200|

#### (?=) Menší než nebo rovno

|Ukázka vzorce|Zobrazené záznamy|
|--------------|-------------------------------|
|`<=1200`|Čísla menší než nebo rovno 1200|

#### (&) A

|Ukázka vzorce|Zobrazené záznamy|
|--------------|---------------------------------|
|`>200&<1200`|Čísla větší než 200 a zároveň menší než 1200|

#### ('') Přesná shoda znaků

|Ukázka vzorce|Zobrazené záznamy|
|-------------|-------------------------------- |
|`'man'|Text, který přesně odpovídá vzorce man a rozlišuje velká a malá písmena.|

#### (@) Nerozlišující malá a velká písmena

|Ukázka vzorce|Zobrazené záznamy|
|-------------|-----------------|
|`@man*`|Text, který začíná man a nerozlišuje velká a malá písmena.|

#### (*) Neomezený počet neznámých znaků

|Ukázka vzorce|Zobrazené záznamy|
|-------------|---------------------------------- |
|`*Co*`|Text, který obsahuje “Co“ a rozlišuje malá a velká písmena.|
|`*Co`|Text, který končí na “Co“ a rozlišuje malá a velká písmena.|
|`Co*`|Text, který začíná na “Co“ a rozlišuje malá a velká písmena.|

> [!NOTE]  
> Nemůžete použít `*` při filtrování pole Volba (Option), například pole **Stav** na prodejních objednávkách. Chcete-li zadat filtr pro tento typ pole, můžete zadat číselnou hodnotu jako parametr filtrování. Například v poli **Stav** na prodejní objednávce, která má hodnoty **Otevřeno**, **Vydáno**, **Čeká na schválení** a **Čeká na zálohu** použijte hodnoty `0`, `1`, `2` a `3` k filtrování těchto možností.

#### (?) Jeden neznámý znak

|Ukázka vzorce|Zobrazené záznamy|
|-------------|----------------------------|
|`Hans?n`|Text jako Hansen nebo Hanson|

#### Vzorce v kombinovaném formátu

|Ukázka vzorce|Zobrazené záznamy|
|-------------|------------------------------- |
|`5999|8100..8490`|Obsahuje všechny záznamy s číslem 5999 nebo číslem z intervalu 8100 až 8490.|
|`..1299|1400..`|Obsahuje záznamy s číslem menším nebo rovným 1299 nebo číslem rovnajícím se 1400 nebo větším (všechna čísla kromě 1300 až 1399).|
|`>50&<100`|Obsahuje záznamy s čísly, které jsou větší než 50 a menší než 100 (čísla 51 až 99).|

### <a name="FilterTokens"> </a>Tokeny filtru

Při zadávání kritérií filtru můžete také psát slova se zvláštním významem, která se nazývají tokeny filtru. Po zadání tokenového slova je slovo nahrazeno hodnotou nebo hodnotami, které představuje. Usnadňuje se tím filtrování snížením potřeby přejít na jiné stránky a vyhledat hodnoty, které chcete do filtru přidat. Níže uvedené tabulky popisují některé tokeny, které můžete zadat jako kritéria filtru.

> [!TIP]
> Vaše organizace může používat vlastní tokeny. Chcete-li se dozvědět více o kompletní sadě tokenů, které máte k dispozici, nebo přidat další vlastní tokeny, obraťte se na svého správce. Pro více informací navštivte [Přidání tokenů filtru](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### (%me nebo %userid) Záznamy, které jsou přiřazeny vám

Použijte `%me` nebo `%userid` při filtrování polí, která obsahují ID uživatele, například pole **Přiřazené ID uživatele**, pro zobrazení všech záznamů, které jsou vám přiřazeny.

|Ukázka vzorce|Zobrazené záznamy|
|-------------------|---------------------------------|
|`%me`<br />nebo<br />`%userid`|Záznamy, které jsou přiřazeny k vašemu uživatelskému účtu.|

#### (%mycustomers) Zákazníci v Mí zákazníci

Pomocí `%mycustomers` v poli **Číslo zákazníka** zobrazíte všechny záznamy pro zákazníky, kteří jsou zahrnuti do seznamu **Mí zákazníci** v centru rolí.

|Ukázka vzorce|Zobrazené záznamy|
|-------------|------------------------------------|
|`%mycustomers`|Zákazníci v **Mí zákazníci** ve vašem centru rolí.|

#### (%myitems) Zboží v Mé zboží

Pomocí `%myitems` v poli **Číslo zboží** zobrazíte všechny záznamy pro zboží, které jsou zahrnuty do seznamu **Mé zboží** v centru rolí.

|Ukázka vzorce|Zobrazené záznamy|
|-------------|---------------------------------------|
|`%myitems`|Zboží v **Mé zboží** ve vašem centru rolí.|

#### (%myvendors) Dodavatelé v Mí dodavatelé

Pomocí `%myvendors` v poli **Číslo dodavatele** zobrazíte všechny záznamy pro dodavatele, které jsou zahrnuty do seznamu **Mí dodavatelé** v centru rolí.

|Ukázka vzorce|Zobrazené záznamy|
|-------------|------------------------------------ |
|`%myvendors`|Dodavatelé v **Mí dodavatelé** ve vašem centru rolí.|

## Viz také

[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ukládaní a přizpůsobení zobrazení seznamů](ui-views.md)  
[Časté dotazy týkající se vyhledávání a filtrování](ui-search-filter-faq.md)
v