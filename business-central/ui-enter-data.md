---
title: Jak zadávat data do polí v Business Central | Microsoft Docs
description: Informace o obecných funkcích, které vám pomohou zadávat data do polí.
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/14/2020
ms.reviewer: v-zdbice
ms.author: sgroespe
---

# Zadávání dat

Existuje mnoho obecných funkcí, které vám pomohou rychle a snadno zadávat data. V tomto textu jsou popsány obecné funkce pro zadávání dat.  

Příklady v tomto článku používají demonstrační data.

## Klávesové zkratky

Existuje několik klávesových zkratek, které vám umožní pracovat „bez myši“ a urychlit zadávání dat, zejména s velkým množstvím položek a úkoly s opakovanými zadáváním.

Další informace o klávesových zkratkách naleznete v části [Klávesové zkratky](keyboard-shortcuts.md). V tomto článku je několik zkratek popsáno.

## <a name="QuickEntry"></a>Zrychlení zadávání dat pomocí rychlého vstupu

**Rychlý vstup** je funkce určená pro zadávání dat při používání klávesnice. **Rychlý vstup** funguje na polích (jako na stránkách karet) a v seznamech (řádky a sloupce). Je výhodný, když provádíte úkoly s opakované zadávání, které vyžadují postupné vytváření více záznamů, například šarže na prodejní objednávce nebo registraci nového zboží.

Možná jste už obeznámeni s použitím klávesy **Tab** pro posun z jednoho pole na stránce do dalšího editovatelného pole. Nevýhodou použití **Tab** je to, že vždy jde postupně do dalšího pole. <!-- i v případě, že pole není možné upravovat nebo se vyplňuje jen zřídka.--> **Rychlý vstup** umožňuje tuto cestu změnit. Pomocí **Rychlého vstup** můžete pomocí klávesy **Enter** procházet pouze ta pole, která vás zajímají, přeskakovat needitovatelná pole a pole, která obvykle nevyplňujete. Tohoto chování jste si již možná všimli na některých stránkách. Důvodem je, že aplikace již určuje, která pole mají být zahrnuta při stisknutí **Enter** a která přeskočit. **Rychlý vstup** můžete upravit přizpůsobením pracovního prostoru a optimalizovat tak způsob zadávání dat pro každou stránku.

### Jak funguje rychlý vstup

Každé pole lze označit buď jako *zahrnuté do Rychlého vstupu* nebo *vyjmuté z Rychlého vstupu*. Pole, která jsou zahrnuta v **Rychlém vstupu**, budou zahrnuta do cesty, když stisknete **Enter** a pole, která jsou vyloučena z **Rychlého vstupu**, nebudou.

Když dokončíte zadávání dat do pole, stačí stisknout **Enter** pro potvrzení změn a přejít na další pole. Pokud chcete změnit směr a přejít na předchozí pole, stiskněte **Shift+Enter**. Další informace o klávesových zkratkách naleznete v části [Klávesové zkratky](keyboard-shortcuts.md#QuickEntry).

#### Tipy a triky

Následující část obsahuje několik užitečných informací o používání funkce **Rychlý vstup**.

- Je k dispozici pro všechna editovatelná pole.
- Funguje také ve sloupcích a řádcích.
- Nebrání v přístupu k jiným prvkům stránky, jako jsou akce. Ty jsou stále přístupné pomocí **Tab** a **Shift+Tab**.
- Záložky nemusí být rozbaleny, aby funkce **Rychlý vstup** fungovala. Pokud je další pole rychlého vstupu umístěno ve sbalené záložce, záložka se automaticky rozbalí a nastaví na určené pole.
- **Rychlý vstup** funguje bez ohledu na to, zda jsou pole povinná. Je tedy dobré zajistit, aby byla do rychlého vstupu zahrnuta povinná pole.
- Ve výchozím nastavení je většina polí automaticky zahrnuta do rychlého vstupu. Zpočátku bude vaším úkolem pravděpodobně vyloučit pole z **Rychlého vstupu**.

### Změna polí rychlého zadání

Chcete-li změnit pole, která jsou zahrnuta nebo vyloučena z rychlého vstupu na stránce, použijete přizpůsobení.

1. Zahajte přizpůsobení výběrem ikony ![Nastavení](media/ui-experience/settings_icon_small.png "Ikona nastavení pro centrum rolí") a poté akci **Přizpůsobit**.
2. Vyberte pole, které chcete změnit, nebo v seznamech vyberte odpovídající záhlaví sloupce a poté vyberte buď **Zahrnout do rychlého vstupu** nebo **Vyjmout z rychlého vstupu**.

Další informace o přizpůsobení naleznete v části [Přizpůsobení pracovního prostoru](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Povinná pole

Při zadávání dat na stránkách jsou některá pole označena červenou hvězdičkou. Červená hvězdička znamená, že pole musí být vyplněno, aby se dokončil určitý proces, který pole používá, jako je účtování transakce, která používá hodnotu v poli.  

Přestože pole obsahuje červenou hvězdičku, nejste nuceni vyplnit pole dříve, než budete pokračovat do jiných polí nebo zavřete stránku. Červená hvězdička slouží pouze jako připomenutí, že vám bude zablokováno dokončení určitého procesu.  

## <a name="finding-data-as-you-type"></a>Hledání dat při psaní

 Když začnete psát znaky do pole, zobrazí se rozevírací seznam a zobrazuje možné hodnoty pole. Seznam se při psaní více znaků mění a při zobrazení můžete vybrat správnou hodnotu.  

 Mnoho polí má tlačítko se šipkou dolů, které můžete zvolit. Pomocí šipky získáte seznam dat, která jsou k dispozici pro zadávání do pole. Tlačítko má dvě funkce v závislosti na typu pole:  

- Vyhledat - Zobrazí informace z jiné tabulky, které můžete zadat do pole. Můžete vybrat jen jeden záznam dat.  

- Rozevírací nabídka - Zobrazí sadu možností, které pro dané pole existují. Můžete vybrat pouze jednu z možností.  

## Kopírování a vkládání polí a řádků - Nejčastější dotazy

Můžete zkopírovat jeden nebo více řádků ze seznamu nebo jedno pole na stránce a potom vložit, co jste zkopírovali, na stejnou stránku, jinou stránku nebo externí dokument (například Microsoft Excel a e-mail Outlook). Stručně řečeno, chcete-li kopírovat, stiskněte klávesy **CTRL+C** (cmd+C v MacOS) na klávesnici. Chcete-li vložit, stiskněte klávesy **CTRL+V** (cmd+V v systému MacOS).

V seznamu zkopírujete pole ve stejném sloupci řádku výše a vložíte jej do aktuálního řádku stisknutím klávesy **F8**.

Další informace naleznete v části [Nejčastější dotazy týkající se kopírování a vkládání](ui-copy-paste.md).

## Filtrování řádkových záznamů

Chcete-li zahájit filtrování, vyberte v horní části seznamu ikonu ![Filter pane icon](media/open-filter-pane-icon.png "Ikona podokna filtru") nebo stiskněte **Shift+F3** a otevřete podokno filtru. S podoknem filtru pracujete stejně jako v kterémkoli jiném seznamu. Další informace viz [Řazení, vyhledávání a filtrování](ui-enter-criteria-filters.md#Filtering).

Filtrování je zvláště užitečné při prohlížení a analýze delších dokumentů. Představte si například, že otevřete zaúčtovanou prodejní fakturu a filtrujete řádkové záznamy tak, aby se zobrazovaly všechny řádkové záznamy, které mají individuální slevu vyšší než 5%, nebo filtrujete, aby se zobrazovaly pouze příslušenství pro kola s názvem „pro“ v popisu.

## <a name="Focus"></a>Režim detailu pro řádkové záznamy

Při práci na dokumentech, které obsahují část s řádky, například na stránce prodejní objednávky nebo faktury, můžete přepnout zobrazení tak, aby se zaměřovalo pouze na řádkové záznamy. Část řádkových záznamů se poté rozbalí, takže zabírá téměř celý pracovní prostor a skrývá další části stránky kromě oblasti akcí v horní části. To vám dává lepší přehled o řádkových záznamech a poskytuje více prostoru pro práci s nimi.

To je zvláště výhodné při práci s velkými seznamy řádkových záznamů a při rychlém zadávání dat. Další výhodou je, že poskytuje také pokročilé možnosti filtrování, jako v jiných seznamech, takže procházení a vyhledávání v řádkových záznamech je ještě snazší.

### Zapnutí a vypnutí režimu detailu

Chcete-li zapnout režim detailu na řádkové záznamy, klepněte kdekoli v části řádkové položky a poté v pravém horním rohu vyberte ![Ikona režimu detailu](media/focus-mode.png "Ikona režimu detailu") nebo stiskněte **Ctrl+Shift+F12**.

Chcete-li přepnout zpět do normálního zobrazení, zvolte ![Ikona režimu detailu](media/focus-mode.png "Ikona režimu detailu") nebo stiskněte znovu **Ctrl+Shift+F12**.

## Multitasking na více stránkách

Při práci na více úkolech najednou nebo při přerušení aktuální úlohy, například při příchozím hovoru, můžete otevřít kartu nebo stránku dokumentu v novém okně. To vám umožní ponechat otevřené okno pro probíhající úlohu, zatímco v jednom nebo více dalších oknech spustíte nebo dokončíte další úkol.

Chcete-li otevřít aktuální kartu nebo dokument v novém okně, zvolte ![Otevřít nové okno](media/open-new-window-icon.png "Ikona Otevřít nové okno") v pravém horním rohu, nebo stiskněte **Alt+Shift+W**.

> [!NOTE]
> Když otevřete další stránky z karty nebo dokumentu, který je otevřen v novém okně, tyto stránky se otevřou v novém okně, i když nezvolíte ![Otevřít nové okno](media/open-new-window-icon.png "Ikona Otevřít nové okno").

> [!NOTE]
> Pokud pracujete v prohlížeči Safari, blokování automaticky otevíraných oken může způsobit, že se nové okno neotevře. V takovém případě zadejte URL produktu jako povolený web. Další informace naleznete v části [Změnit předvolby v prohlížeči Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).

## <a name="entering-quantities-by-calculation"></a>Zadávání množství výpočtem

 Při zadávání čísel do polí množství, například do pole **Množství** na řádku deníku zboží, můžete místo součtu množství zadat vzorec.  

## Příklady:  

- Pokud zadáte 19+19, pole se vypočítá na hodnotu 38.  

- Pokud zadáte 41-9, pole se vypočítá na hodnotu 32.  

- Pokud zadáte 12*4, pole se vypočítá na hodnotu 48.  

- Pokud zadáte 12/4, pole se vypočítá na hodnotu 3.  

## <a name="entering-negative-numbers"></a>Zadávání záporných čísel

Záporná čísla můžete zadat dvěma způsoby. Číslo -20,5 lze zadat jako:  

- -20,5  

    nebo
- 20,5-  

 V obou případech bude částka zaznamenána jako -20,5.  

 Pokud je poslední znak výrazu **+** nebo **-**, bude celý výraz zaznamenán s tímto znaménkem. Příklad: **10-20+** bude mít výsledek 10 a ne -10.  

## <a name="entering-dates-and-times"></a>Zadávání dat a časů

Můžete zadat data a časy do všech polí, která jsou určena pro data (datová pole). Můžete zadat data s oddělovači nebo bez nich.

> [!NOTE]  
> Způsob zadání data a času závisí na nastavení **Oblasti**. Pro další informace navštivte [Změna základního nastavení](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Vkládání data  

 Do datového pole můžete zadat dvě, čtyři, šest nebo osm číslic:  

- Pokud zadáte pouze dvě číslice, bude to interpretováno jako den a přidá se měsíc a rok pracovního dne.

- Pokud zadáte čtyři číslice, bude to interpretováno jako den a měsíc a přidá se pouze rok daného pracovního roku.  

- Pokud je datum, které chcete zadat, v rozsahu 01.01.1930 až 31.12.2029, můžete zadat rok dvěma číslicemi, jinak zadejte rok čtyřmi číslicemi.  

Můžete také zadat datum jako pracovní den následovaný číslem týdne a volitelně rokem (například po25 znamená pondělí v týdnu 25).  

Místo zadání konkrétního data můžete zadat jeden ze dvou kódů.  

|Kód|Výsledek|  
|--------------|----------------|  
|d|Toto je dnešní datum (systémové datum pro počítač).|
|o|Toto určuje účetní období, kde o znamená první účetní období, o2 znamená druhé účetní období atd.|
|p|Toto je pracovní datum nastavený v aplikaci. Chcete-li změnit pracovní datum, viz [Změna základních nastavení](ui-change-basic-settings.md). Možná budete chtít použít pracovní datum, pokud máte mnoho transakcí s jiným než dnešním datem.|
|u|Určuje, že datum po u je uzávěrkové datum, například u311201|

### <a name="entering-times"></a>Zadávání časů

 Když zadáte časy, můžete mezi jednotlivé části vložit libovolný znak oddělovače, který však není nutný. Nemusíte psát minuty, sekundy nebo AM/PM.  

 V následující tabulce jsou uvedeny různé způsoby zadávání časů a jejich interpretace.  

|Vstup|Interpretace|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|5:30:00|  
|0530|5:30:00|  
|05:30:5|5:30:05|  
|053005|5:30:05|  
|05:30:5,50|05:30:05.5|  
|053005050|05:30:05.05|  

 Pokud nezadáte oddělovač, musíte pro každou jednotku času zadat dvě číslice.  

### <a name="entering-datetimes"></a>Zadávání dat a časů

Při zadávání dat a časů je nutné zadat mezeru mezi datem a časem.  

Následující tabulka uvádí různé způsoby, jak můžete zadat data a časy a jak jsou interpretovány.  

|Vstup|Interpretace|  
|---------------|------------------------|  
|131202 132455|13-12-02 13:24:55|  
|1-12-02 10|01-12-02 10:00:00|  
|1.12.02 5|01-12-02 5:00:00|  
|1.12.02|01-12-02 0:00:00|  
|11 12|11-aktuální měsíc-aktuální rok 12:00:00|  
|1112 12|11-12 - aktuální rok 12:00:00|  
|d nebo dnes|dnešní datum 00:00:00|  
|d čas|dnešní aktuální datum a čas|  
|d 10:30|dnešní datum 10:30:00|  
|d 3:3:3|dnešní datum 3:03:03|  
|p nebo pracovní|pracovní datum 00:00:00|  
|po nebo pondělí|Pondělí aktuálního týdne 00:00:00|  
|út nebo úterý|Úterý aktuálního týdne 00:00:00|  
|st nebo středa|Středa aktuálního týdne 00:00:00|  
|čt nebo čtvrtek|Čtvrtek aktuálního týdne 00:00:00|  
|pá nebo pátek|Pátek aktuálního týdne 00:00:00|  
|so nebo sobota|Sobota aktuálního týdne 00:00:00|  
|ne nebo neděle|Neděle aktuálního týdne 00:00:00|  
|út 10:30|Úterý aktuálního týdne 10:30:00|  
|út 3:3:3|Úterý aktuálního týdne 3:03:03|  

## <a name="entering-duration"></a>Zadávání doby trvání  

Trvání zadáte jako číslo následované jeho měrnou jednotkou.  

Zde jsou nějaké příklady.  

|Doba trvání|Měrná jednotka|  
|------------------|-------------------------|  
|2h|2 hod|  
|6h 30m|6 hod 30 min|  
|6.5h|6 hod 30 min|  
|90m|1 hod 30 min|  
|2d 6h 30m|2 dny 6 hod 30 min|  
|2d 6h 30m 56s 600ms|2 dny 6 hod 30 min 56 sec 600 msec|  

Můžete také zadat číslo a ono se automaticky převede na dobu trvání. Zadané číslo se převede podle výchozí měrné jednotky, která byla zadána pro pole trvání.  

Chcete-li vidět, jaká měrná jednotka se používá v poli trvání, zadejte číslo a podívejte se, na kterou měrnou jednotku se převede.  

Číslo 5 se převede na 5 hodin, pokud je měrnou jednotkou hodina.  

## <a name="using-date-formulas"></a>Použití vzorců dat  
 Vzorec data je krátká, zkrácená kombinace písmen a číslic, která určuje, jak vypočítat data. Vzorce data můžete zadat do různých polí pro výpočet data a do opakujících se frekvenčních polí v opakujících se denících.  

> [!NOTE]  
> Ve všech polích vzorců dat je jeden den automaticky zahrnut jako den, kdy začíná období. Pokud tedy například zadáte 1T, pak je tato doba ve skutečnosti osm dní, protože je zahrnuta i dnes. Chcete-li určit období sedmi dnů (jeden skutečný týden) včetně data začátku období, musíte zadat 6D nebo 1T-1D.  

 Zde je několik příkladů, jak lze použít vzorce:  

- Vzorec data v poli Frekvence periody v periodických denících určuje, jak často bude položka na řádku deníku zaúčtována.  

- Vzorec data v poli Lhůta odkladu pro určenou úroveň připomenutí určuje časové období, které musí uplynout od data splatnosti (nebo od data předchozího připomenutí) před vytvořením připomenutí.  

- Vzorec data v poli Výpočet splatnosti určuje, jak vypočítat datum splatnosti pro připomenutí.  

 Vzorec pro výpočet data může obsahovat maximálně 20 znaků, číslic i písmen. Pro specifikaci času můžete použít následující písmena, které jsou zkratkami.  

|||  
|-|-|  
|B|Aktuální|  
|D|Den (dny)|  
|T|Týden (týdny)|  
|M|Měsíc (měsíce)|  
|K|Čtvrtletí|  
|R|Rok (roky)|  

Vzorec data můžete vytvořit třemi způsoby.  

Následující příklad ukazuje, jak se dá vytvořit datum pomocí B-aktuální a časové jednotky.  

|||  
|-|-|  
|BT|Aktuální týden|  
|BM|Aktuální měsíc|  

Následující příklad ukazuje, jak se dá vytvořit datum pomocí B-aktuální a časové jednotky. Číslo nesmí být větší než 9999.  

|||  
|-|-|  
|10D|10 dnů od dnešního dne|  
|2T|2 týdny od dnešního dne|  

Následující příklad ukazuje, jak se dá vytvořit datum pomocí časové jednotky a čísla.  

|||  
|-|-|  
|D10|Dalšího 10. dne v měsíci|  
|TD4|Další 4. den v týdnu (čtvrtek)|  

Následující příklad ukazuje, jak můžete tyto tři formy kombinovat podle potřeby.  

|||  
|-|-|  
|BM+10D|Aktuální měsíc + 10 dní|  

Následující příklad ukazuje, jak můžete použít znaménko mínus k označení data v minulosti.  

|||  
|-|-|  
|-1R|Před 1 rokem od dnešního dne|  

## Viz také

 [Řazení, vyhledávání a filtrování](ui-enter-criteria-filters.md)  
 [Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
