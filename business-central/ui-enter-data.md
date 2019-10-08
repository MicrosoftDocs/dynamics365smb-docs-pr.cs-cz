---
title: Jak zadávat data do polí | Microsoft Docs
description: 'Existuje mnoho obecných funkcí, které vám pomohou rychle a snadno zadávat data. V tomto textu jsou popsány obecné funkce pro zadávání dat.'
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/01/2018
ms.author: jswymer
---

# <a name="entering-data"></a>Vkládání dat
Existuje mnoho obecných funkcí, které vám pomohou rychle a snadno zadávat data. V tomto textu jsou popsány obecné funkce pro zadávání dat.  

Příklady v tomto článku používají demonstrační data.

## <a name="mandatory-fields"></a>Povinná pole
Při zadávání dat na stránkách jsou některá pole označena červenou hvězdičkou. Červená hvězdička znamená, že pole musí být vyplněno, aby se dokončil určitý proces, který pole používá, jako je účtování transakce, která používá hodnotu v poli.  

Přestože pole obsahuje červenou hvězdičku, nemusíte být nuceni vyplnit pole dříve, než budete pokračovat do jiných polí nebo zavřete stránku. Červená hvězdička slouží pouze jako připomenutí, že vám bude zablokováno dokončení určitého procesu.  


## <a name="finding-data-as-you-type"></a>Hledání dat při psaní  
 Když začnete psát znaky do pole, zobrazí se rozevírací seznam a zobrazuje možné hodnoty pole. Seznam se při psaní více znaků mění a při zobrazení můžete vybrat správnou hodnotu.  

 Mnoho polí má tlačítko se šipkou dolů, které si můžete zvolit. Pomocí šipky získáte seznam dat, která jsou k dispozici pro zadávání do pole. Tlačítko má dvě funkce v závislosti na typu pole:  

-   Vyhledat - Zobrazí informace z jiné tabulky, které můžete zadat do pole. Můžete si vybrat část dat najednou.  

-   Rozevírací nabídka - Zobrazí sadu možností, které pro dané pole existují. Můžete vybrat pouze jednu z možností.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards on the **Items** page, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Zadávání množství výpočtem  
 Při zadávání čísel do polí množství, například do pole **Množství** na řádku deníku zboží, můžete místo součtu množství zadat vzorec.  

## <a name="examples"></a>Příklady:  

-   Pokud zadáte 19+19, pole se vypočítá na hodnotu 38.  

-   Pokud zadáte 41-9, pole se vypočítá na hodnotu 32.  

-   Pokud zadáte 12*4, pole se vypočítá na hodnotu 48.  

-   Pokud zadáte 12/4, pole se vypočítá na hodnotu 3.  

## <a name="entering-negative-numbers"></a>Zadávání záporných čísel
Záporná čísla můžete zadat dvěma způsoby. Číslo -20,5 lze zadat jako:  

-   -20,5  

    nebo
-   20,5-  

 V obou případech bude částka zaznamenána jako -20,5.  

 Pokud je poslední znak výrazu **+** nebo **-**, bude celý výraz zaznamenán s tímto znaménkem. Příklad: **10-20+** bude mít výsledek 10 a ne -10.  

## <a name="entering-dates-and-times"></a>Zadávání dat a časů
Můžete zadat data a časy do všech polí, která jsou specificky přiřazena k datům (datová pole). Můžete zadat data s oddělovači nebo bez nich.

> [!NOTE]  
> Způsob zadání data a času závisí na nastavení **Oblasti**. Pro další informace navštivte [Změna základního nastavení](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Vkládání data  
 Do datového pole můžete zadat dvě, čtyři, šest nebo osm číslic:  

-   Pokud zadáte pouze dvě číslice, bude to interpretováno jako den a přidá se měsíc a rok pracovního dne.  

-   Pokud zadáte čtyři číslice, bude to interpretováno jako den a měsíc a přidá se pouze rok daného pracovního roku.  

-   Pokud je datum, které chcete zadat, v rozsahu 01/01/1930 až 31/31/2029, můžete zadat rok dvěma číslicemi; jinak zadejte rok čtyřmi číslicemi.  

 Můžete také zadat datum jako pracovní den následovaný číslem týdne a volitelně rokem (například Mon25 znamená pondělí v týdnu 25).  

 Místo zadání konkrétního data můžete zadat jeden ze dvou kódů.  

|Kód|Výsledek|  
|--------------|----------------|  
|t|Toto je dnešní datum (systémové datum pro počítač).|  
|w|Toto je pracovní datum nastavený v aplikaci. Chcete-li změnit pracovní datum, viz [Změna základních nastavení](ui-change-basic-settings.md). Možná budete chtít použít pracovní datum, pokud máte mnoho transakcí s jiným než dnešním datem.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a>Zadávání časů  
 Když zadáte časy, můžete mezi jednotky vložit libovolný znak oddělovače, který však není nutný. Nemusíte psát minuty, sekundy nebo AM / PM.  

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

## <a name="entering-datetimes"></a>Zadávání dat a časů  
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
|t nebo dnes|dnešní datum 00:00:00|  
|t čas|dnešní aktuální datum|  
|t 10:30|dnešní datum 10:30:00|  
|t 3:3:3|dnešní datum 3:03:03|  
|w nebo pracovní datum|pracovní datum 00:00:00|  
|m nebo pondělí|Pondělí aktuálního týdne 00:00:00|  
|tu nebo úterý|Úterý aktuálního týdne 00:00:00|  
|we nebo středa|Středa aktuálního týdne 00:00:00|  
|th nebo čtvrtek|Čtvrtek aktuálního týdne 00:00:00|  
|f nebo pátek|Pátek aktuálního týdne 00:00:00|  
|s nebo sobota|Sobota aktuálního týdne 00:00:00|  
|su nebo neděle|Neděle aktuálního týdne 00:00:00|  
|tu 10:30|Úterý aktuálního týdne 10:30:00|  
|tu 3:3:3|Úterý aktuálního týdne 3:03:03|  

## <a name="entering-duration"></a>Zadávání doby trvání  
 Trvání zadáte jako číslo následované jeho měrnou jednotkou.  

 Zde jsou nějaké příklady.  

|Doba trvání|Měrná jednotka**|  
|------------------|-------------------------|  
|2h|2 hod|  
|6h 30 m|6 hod 30 min|  
|6.5h|6 hod 30 min|  
|90m|1 hod 30 min|  
|2d 6h 30m|2 dny 6 hod 30 min|  
|2d 6h 30m 56s 600ms|2 dny 6 hod 30 min 56 sec 600 msec|  

 Můžete také zadat číslo a ono se automaticky převede na dobu trvání. Zadané číslo se převede podle výchozí měrné jednotky, která byla zadána pro pole trvání.  

 Chcete-li vidět, jaká měrná jednotka se používá v poli trvání, zadejte číslo a podívejte se, na kterou měrnou jednotku se převede.  

 Číslo 5 se převede na 5 hodin, pokud je měrnou jednotkou hodina.  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Použití vzorců dat  
 Vzorec data je krátká, zkrácená kombinace písmen a číslic, která určuje, jak vypočítat data. Vzorce data můžete zadat do různých polí pro výpočet data a do opakujících se frekvenčních polí v opakujících se denících.  

> [!NOTE]  
>  Ve všech polích vzorců dat je jeden den automaticky zahrnut jako den, kdy začíná období. Pokud tedy například zadáte 1W, pak je tato doba ve skutečnosti osm dní, protože je zahrnuta i dnes. Chcete-li určit období sedmi dnů (jeden skutečný týden) včetně data začátku období, musíte zadat 6D nebo 1W-1D.  

 Zde je několik příkladů, jak lze použít vzorce:  

-   Vzorec data v poli frekvence periody v periodických denících určuje, jak často bude položka na řádku deníku zaúčtována.  

-   Vzorec data v poli Lhůta odkladu pro určenou úroveň připomenutí určuje časové období, které musí uplynout od data splatnosti (nebo od data předchozího připomenutí) před vytvořením připomenutí.  

-   Vzorec data v poli Výpočet splatnosti určuje, jak vypočítat datum splatnosti pro připomenutí.  

 Vzorec pro výpočet data může obsahovat maximálně 20 znaků, číslic i písmen. Pro specifikaci času můžete použít následující písmena, které jsou zkratkami.  

|||  
|-|-|  
|C|Aktuální|  
|D|Den (dny)|  
|W|Týden (týdny)|  
|M|Měsíc (měsíce)|  
|Q|Čtvrtletí|  
|Y|Rok (roky)|  

 Vzorec data můžete vytvořit třemi způsoby.  

 Následující příklad ukazuje, jak se dá vytvořit datum pomocí C-aktuální a časové jednotky.  

|||  
|-|-|  
|CW|Aktuální týden|  
|CM|Aktuální měsíc|  

 Následující příklad ukazuje, jak se dá vytvořit datum pomocí C-aktuální a časové jednotky. Číslo nesmí být větší než 9999.  

|||  
|-|-|  
|10D|10 dnů od dnešního dne|  
|2W|2 týdny od dnešního dne|  

 Následující příklad ukazuje, jak se dá vytvořit datum pomocí časové jednotky a čísla.  

|||  
|-|-|  
|D10|Dalšího 10. dne v měsíci|  
|WD4|Další 4. den v týdnu (čtvrtek)|  

 Následující příklad ukazuje, jak můžete tyto tři formy kombinovat podle potřeby.  

|||  
|-|-|  
|CM+10D|Aktuální měsíc + 10 dní|  

 Následující příklad ukazuje, jak můžete použít znaménko mínus k označení data v minulosti.  

|||  
|-|-|  
|-1Y|Před 1 rokem od dnešního dne|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Viz také  
 [Třídění, Vyhledávání a Filtrování Seznamů](ui-enter-criteria-filters.md)  
 [Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
