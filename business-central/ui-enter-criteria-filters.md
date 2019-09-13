---
title: 'Řazení, vyhledávání a filtrování seznamů | Microsoft Docs'
description: 'Pracujte efektivně v seznamech tím, že prohledáváte data, řadíte sloupce a zpřesňujete výsledky pomocí výkonných symbolů filtru a klávesových zkratek.'
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.date: 10/01/2018
ms.author: jswymer
---
# <a name="sorting-searching-and-filtering-lists"></a>Řazení, vyhledávání a filtrování seznamů
Existuje několik věcí, které můžete udělat, aby vám pomohly prohlížet, najít a redukovat záznamy v seznamu. Patří sem řazení, vyhledávání a filtrování. Některé nebo všechny z nich můžete použít současně pro rychlé nalezení nebo analýzu vašich dat.

> [!TIP]
> Při prohlížení dat jako dlaždic můžete vyhledávat a používat základní filtrování. Chcete-li použít celou řadu výkonných funkcí pro třídění, vyhledávání a filtrování, vyberte ikonu ![Zobrazit jako seznam](media/ui_show_as_list_icon.png "Zobrazit jako seznam šipka doleva") pro zobrazení dat jako seznamu.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Řazení
Řazení vám usnadňuje dostat rychlý přehled o vašich datech. Máte-li například mnoho zákazníků, můžete je řadit podle **Čísla zákazníka**, **Účto skupiny zákazníka**, **Kódu měny**, **Kódu zěmě/oblasti** nebo **Čísla registrace DPH**, abyste dostali přehled, který potřebujete.

Chcete-li seřadit seznam, můžete buď zvolit text záhlaví sloupce pro přepínání mezi vzestupným a sestupným pořadí, nebo zvolit malou šipku dolů v záhlaví sloupce a poté zvolit **Vzestupně** nebo **Sestupně**.  

> [!NOTE]  
>   Řazení není podporováno pro obrázky, pole typu BLOB, dynamický filtr a pole, která nepatří do tabulky.  

## <a name="searching"></a>Vyhledávání
<!--## Searching by using the Quick Filter --> V horní části každé stránky seznamu je ikona ![Prohledat seznam](media/ui-search/search-list.png "ikona Prohledat seznam")**Hledat**, která poskytuje rychlý a snadný způsob, jak redukovat záznamy v seznamu a zobrazit pouze ty záznamy, které obsahují data, která chcete vidět.

Chcete-li hledat, jednoduše vyberte ikonu vyhledávání a potom do pole zadejte hledaný text. Můžete zadat písmena, čísla a další symboly.

### <a name="fine-tune-the-search"></a>Doladění vyhledávání
Obecně se vyhledávání pokusí shodovat text ve všech polích; nerozlišuje mezi malými a velkými písmeny a bude odpovídat textu umístěnému kdekoli v poli (na začátku, na konci nebo uprostřed).

Přesnější vyhledávání však můžete provést pomocí následujících speciálních znaků:

- Chcete-li najít pouze hodnoty polí, které přesně odpovídají celému textu a velikosti písmen, umístěte hledaný text mezi jednoduché uvozovky `''` (například `'man'`).

- Chcete-li najít hodnoty polí, které začínají určitým textem a odpovídají případu, umístěte `*` za hledaný text (například `man*`).

- Chcete-li najít hodnoty polí, které končí určitým textem a odpovídají případu, umístěte `*` za hledaný text (například `*man`).

- Při použití `''` nebo `*` se při vyhledávání rozlišují malá a velká písmena. Pokud chcete, aby vyhledávání nerozlišovalo malá a velká písmena, umístěte `@` před hledaný text (například `@man*`).

V následující tabulce jsou uvedeny některé příklady, které vysvětlují, jak můžete vyhledávání použít.


<!--
In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.-->

<!--
The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options. Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.  

* If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.  
* If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.
-->
<!--

|Search Criteria|Interpreted as...|Finds...|
|---------------|----------------|----------|
|`man`<br />or <br />`Man`|Contains the text; case insensitive|All records with fields that contain the text **man**, regardless of the case.|
|`'Man'`|Entire text match; case sensitive.|All records with fields that only contain **Man** exactly.|
|`Man*`|Starts with the text; case sensitive.|All records with fields that start with the text <b>Man</b> exactly.|
|`@Man*`|Starts with the text; case insensitive.|All records with fields that start with **man**, regardless of the case.|
|`@*man`|Ends with the text; case insensitive.|All records that end with **man**, regardless of the case.|
-->

|Kritéria vyhledávání|Najde...|
|---------------|----------|
|`man`<br />nebo <br />`Man`|Všechny záznamy s poli, které obsahují text **man** bez ohledu na malá a velká písmena. Například **Manchester**, **manual** nebo **Sportsman**. |
|`'Man'`|Všechny záznamy s poli, které obsahují text **Man** s ohledem na malá a velká písmena.|
|`Man*`|Všechny záznamy s poli, které začínají textem <b>Man</b> s ohledem na malá a velká písmena. Například **Manchester**, ale ne **manual** nebo **Sportsman**.|
|`@Man*`|Všechny záznamy s poli, které začínají na **man** bez ohledu na malá a velká písmena. Například **Manchester**, **manual**, ale ne **Sportsman**.|
|`@*man`|Všechny záznamy, které končí na **man** bez ohledu na malá a velká písmena. Například  **Sportsman**, ale ne **Manchester** nebo **manual**.|

> [!TIP]
> Stisknutím F3 můžete aktivovat a deaktivovat vyhledávací pole. Další informace naleznete v [Klávesové zkratky](keyboard-shortcuts.md#KeyboardFilter).

## <a name="filtering"></a>Filtrování
Filtrování poskytuje pokročilejší a všestrannější způsob řízení, které záznamy se zobrazují v seznamu. Mezi vyhledáváním a filtrováním existují dva hlavní rozdíly, jak je popsáno v následující tabulce.

|| **Vyhledávání** | **Filtrování** |
|--|----------|------------|
| **Použitelná pole** | Prohledává všechna pole, která jsou viditelná na stránce. | Filtruje jedno nebo více polí jednotlivě a vybírá z kteréhokoli pole v tabulce, včetně polí, která nejsou na stránce viditelná. |
| **Odpovídající** | Zobrazuje záznamy s poli, která odpovídají hledanému textu, bez ohledu na malá a velká písmena nebo umístění tohoto textu. | Zobrazuje záznamy, kde pole přesně odpovídá filtru a rozlišuje velká a malá písmena, pokud nejsou zadány speciální symboly filtru.

Filtrování umožňuje zobrazit záznamy pro konkrétní účty nebo zákazníky, data, částky a další informace zadáním kritérií filtru. Zobrazí se pouze záznamy, které odpovídají kritériím. Pokud zadáte kritéria pro více polí, zobrazí se pouze záznamy, které odpovídají všem kritériím.

### <a name="working-in-the-filter-pane"></a>Práce v podokně filtru
Podokno filtru zobrazuje aktuální filtry seznamu a umožňuje vám nastavit vlastní filtry na jedno nebo více polí. Následující obrázek ukazuje příklad podokna filtru pro seznam prodejních nabídek.

![Přehled podokna filtru](media/filter-pane-overview.png "Ikona filtru")

Chcete-li zobrazit podokno filtru, použijte klávesovou zkratku **Shift+F3**. U seznamů v Centru rolí můžete také vybrat šipku dolů vedle nadpisu stránky na navigační liště nad seznamem a poté zvolit **Zobrazit podokno filtru**.

![Zobrazit podokno filtru](media/open-filter-pane.png "Zobrazit podokno filtru")

Podokno filtru je rozděleno do tří sekcí: **Zobrazení**, **Filtrovat seznam podle** a **Filtrovat součty podle**:

- **Zobrazení**

  Některé seznamy budou zahrnovat sekci **Zobrazení**. Zobrazení jsou variace seznamu, které byly předkonfigurovány pomocí filtrů. Chcete-li přepnout do jiného zobrazení seznamu, jednoduše vyberte jiný odkaz. Filtry můžete v zobrazení dočasně změnit, ale změny se neuloží natrvalo.

- **Filtrovat seznam podle**

  V sekci **Filtrovat seznam podle** můžete přidat filtry do konkrétních polí, abyste snížili počet zobrazených záznamů. Chcete-li přidat filtr, vyberte **+ Filtr**, zvolte pole, které chcete filtrovat z libovolného pole v tabulce, a do pole zadejte kritéria filtru.

- **Filtrovat součty podle**

  Některé seznamy, které zobrazují vypočtená pole, například částky a množství, budou zahrnovat sekci **Filtrovat součty podle**, kde můžete upravit různé kóty, které ovlivňují výpočty. Můžete například rychle analyzovat svou účetní osnovu filtrováním částek do konkrétního období, nebo si můžete zobrazit součty prodejních objednávek pouze z konkrétního skladu.

  Chcete-li přidat filtr, vyberte **+ Filtr**, zvolte jednu z předdefinovaných dimenzí a poté do pole přidejte kritéria filtru.

  > [!NOTE]
  > Filtry v sekci **Filtrovat součty podle** jsou řízeny pomocí dynamických filtrů v návrhu stránky. Pro další informace navštivte [Dynamické filtry](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Zadání kritérií filtru v podokně filtru
Chcete-li vybrat pole, které chcete filtrovat, proveďte jednu z následujících akcí:
  - V podokně filtru vyberte **+ Pole**. Zadejte název pole, které chcete filtrovat, nebo vyberte pole z nabídky, která zobrazuje všechna pole v tabulce.

  - V záhlaví sloupce vyberte šipku dolů a pak zvolte **Filtr...**. Tím se otevře podokno filtru a sloupec se přidá do podokna filtru.

Nyní můžete do pole zadat nebo vybrat kritéria filtru. Typ pole, které filtrujete, určuje, která kritéria můžete zadat. Například filtrování pole s pevnými hodnotami vám umožní pouze vybrat z těchto hodnot. Pro více informací o speciálních symbolech filtrů navštivte [Kritéria filtru](#FilterCriteria) a [Tokeny filtru](#FilterTokens).

Sloupce, které již mají filtry, jsou označeny ![ikona filtru](media/ui-search/filter-icon.png "ikona filtru") v záhlaví sloupce. Chcete-li odebrat filtr, vyberte záhlaví sloupce a poté zvolte **Vymazat filtr**.


### <a name="entering-filter-criteria-without-the-filter-pane"></a>Zadání kritérií filtru bez podokna filtru
Jednoduché filtry můžete určit přímo v seznamu, aniž byste museli používat podokno filtru.
S libovolným polem vybraným v řádku použijte klávesovou zkratku **Alt+F3** pro zobrazení pouze záznamů se stejnou hodnotou. Poté můžete vybrat další pole a znovu použít stejnou zkratku k dalšímu zdokonalování filtrů. Pokud je vybrané pole již filtrováno, pomocí **Alt+F3** se tento filtr vymaže.

> [!TIP]
> Urychlete vyhledávání a analýzu dat pomocí kombinací klávesových zkratek. Například vyberte pole, použijte **Shift+Alt+F3** k přidání tohoto pole do podokna filtru, zadejte kritéria filtru, použijte **Ctrl+Enter** pro návrat do řádků, vyberte jiné pole a použijte **Alt+F3** k filtrování této hodnoty.
Další informace naleznete v [Klávesové zkratky](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"> </a>Filtrujte kritéria a symboly
Při zadávání kritérií můžete použít všechna čísla a písmena, která můžete v poli normálně použít. Kromě toho můžete použít speciální symboly k dalšímu filtrování výsledků. Následující tabulky ukazují symboly, které lze použít ve filtrech. Další informace o datech a časech naleznete také v [Práce s daty a časy kalendáře](ui-enter-date-ranges.md).

> [!IMPORTANT]  
>  Mohou se vyskytnout případy, kdy hodnoty polí obsahují tyto symboly a vy je chcete filtrovat. Chcete-li toto provést, musíte do uvozovek ('') zahrnout výraz filtru, který obsahuje symbol. Pokud například chcete filtrovat záznamy, které začínají textem *S&R*, výraz je filtru `'S&R*'`.  

### <a name="-interval"></a>(..) Interval

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`1100..2100`|Čísla 1100 až 2100|  
|`..2500`|Až do 2500 včetně|  
|`..12 31 00`|Data do 12 31 00 včetně|  
|`P8..`|Informace za účetní období 8 a následující|  
|`..23`|Od počátečního data do 23-aktuální měsíc-aktuální rok 23:59:59|  
|`23..`|Od 23-aktuální měsíc-aktuální rok 0:00:00 do konce času|  
|`22..23`|Od 22-aktuální měsíc-aktuální rok 0:00:00 do 23-aktuální měsíc-aktuální rok 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) Buď/nebo  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`1200|1300`|Čísla s 1200 nebo 1300|  

### <a name="-not-equal-to"></a>(<>) Není rovno  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`<>0`|Všechny čísla kromě 0<br /><br /> Možnost SQL Server umožňuje kombinovat tento symbol s výrazem zástupných znaků. Například <>A* znamená nerovnost žádnému textu, který začíná na A.|  

### <a name="-greater-than"></a>(>) Větší než  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`>1200`|Čísla větší než 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Větší než nebo rovno  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`>=1200`|Čísla větší než nebo rovno 1200|  

### <a name="-less-than"></a>(<) Menší než  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`<1200`|Čísla menší než 1200|  

### <a name="-less-than-or-equal-to"></a>(?=) Menší než nebo rovno  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`<=1200`|Čísla menší než nebo rovno 1200|  

### <a name="-and"></a>(&) A  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`>200&<1200`|Čísla větší než 200 a zároveň menší než 1200|  

### <a name="-an-exact-character-match"></a>('') Přesná shoda znaků  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`'man'`|Text, který přesně odpovídá výrazu man a rozlišuje velká a malá písmena.|  

### <a name="-case-insensitive"></a>(@) Nerozlišující malá a velká písmena  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`@man*`|Text, který začíná man a nerozlišuje velká a malá písmena.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Neomezený počet neznámých znaků

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`*Co*`|Text, který obsahuje “Co“ a rozlišuje malá a velká písmena.|  
|`*Co`|Text, který končí na “Co“ a rozlišuje malá a velká písmena.|  
|`Co*`|Text, který začíná na “Co“ a rozlišuje malá a velká písmena.|  

> [!NOTE]  
>   Nemůžete použít `*` při filtrování na pole voleb (výčtového typu), například pole **Stav** na prodejních objednávkách. Chcete-li zadat filtr pro tento typ pole, můžete zadat číselnou hodnotu jako parametr filtrování. Například v poli **Stav** na prodejní objednávce, která má hodnoty **Otevřeno**, **Vydáno**, **Čeká na schválení** a **Čeká na zálohu** použijte hodnoty `0`, `1`, `2` a `3` k filtrování těchto možností.

### <a name="-one-unknown-character"></a>(?) Jeden neznámý znak  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`Hans?n`|Text jako Hansen nebo Hanson|  

### <a name="combined-format-expressions"></a>Výrazy v kombinovaném formátu  

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Obsahuje všechny záznamy s číslem 5999 nebo číslem z intervalu 8100 až 8490.|  
|`..1299|1400..`|Obsahuje záznamy s číslem menším nebo rovnajícím se 1299 nebo číslem rovnajícím se 1400 nebo větším (všechna čísla kromě 1300 až 1399).|  
|`>50&<100`|Obsahuje záznamy s čísly, které jsou větší než 50 a menší než 100 (čísla 51 až 99).|  


## <a name="FilterTokens"> </a>Tokeny filtru
Při zadávání kritérií filtru můžete také psát slova se zvláštním významem, která se nazývají tokeny filtru. Po zadání tokenového slova je slovo nahrazeno hodnotou nebo hodnotami, které představuje. Usnadňuje se tím filtrování snížením potřeby přejít na jiné stránky a vyhledat hodnoty, které chcete do filtru přidat. Níže uvedené tabulky popisují některé tokeny, které můžete zadat jako kritéria filtru.

> [!TIP]
> Vaše organizace může používat vlastní tokeny. Chcete-li se dozvědět více o kompletní sadě tokenů, které máte k dispozici, nebo přidat další vlastní tokeny, obraťte se na svého správce. Pro více informací navštivte [Přidání tokenů filtru](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).


### <a name="me-or-userid-records-assigned-to-you"></a>(%me nebo %userid) Záznamy, které jsou přiřazeny vám

Použijte `%me` nebo `%userid` při filtrování polí, která obsahují ID uživatele, například pole **Přiřazené ID uživatele**, pro zobrazení všech záznamů, které jsou vám přiřazeny.

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`%me`<br />nebo<br />`%userid`|Záznamy, které jsou přiřazeny k vašemu uživatelskému účtu. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Zákazníci v Mí zákazníci

Pomocí `%mycustomers` v poli **Číslo zákazníka** zobrazíte všechny záznamy pro zákazníky, kteří jsou zahrnuti do seznamu **Mí zákazníci** v centru rolí.

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`%mycustomers`|Zákazníci v **Mí zákazníci** ve vašem centru rolí. |  

### <a name="myitems-items-in-my-items"></a>(%myitems) Zboží v Mé zboží 

Pomocí `%myitems` v poli **Číslo zboží** zobrazíte všechny záznamy pro zboží, které jsou zahrnuty do seznamu **Mé zboží** v centru rolí.

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`%myitems`|Zboží v **Mé zboží** ve vašem centru rolí. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Dodavatelé v Mí dodavatelé

Pomocí `%myvendors` v poli **Číslo dodavatele** zobrazíte všechny záznamy pro dodavatele, které jsou zahrnuty do seznamu **Mí dodavatelé** v centru rolí.

|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|`%myvendors`|Dodavatelé v **Mí dodavatelé** ve vašem centru rolí. |  


## <a name="see-also"></a>Viz také
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Časté dotazy týkající se vyhledávání a filtrování](ui-search-filter-faq.md)
