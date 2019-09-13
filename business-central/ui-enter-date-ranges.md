---
title: Zadávání dat a časů v Business Central | Microsoft Docs
description: 'Naučte se, jak zadávat data a časy, včetně různých tipů na produktivitu, jako jsou zkratky, výrazy a rozsahy. Filtrujte seznamy nebo sestavy podle konkrétního data nebo časového období.'
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dates, reporting, filter, calendar, shorthand, range'
ms.date: 10/01/2018
ms.author: jswymer
---

# <a name="working-with-calendar-dates-and-times"></a>Práce s daty kalendáře a časy

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] nabízí několik způsobů, jak zadávat data a časy, včetně výkonných funkcí, které urychlují zadávání dat, nebo pomáhají psát složité výrazy kalendáře. V celé aplikaci jsou různá místa, kde můžete do polí zadat data a časy. Například u prodejní objednávky můžete nastavit datum odeslání. Při filtrování seznamů nebo dat sestavy můžete zadat data a časy a vytyčit pouze údaje, které vás zajímají.

## <a name="check-your-region-and-language-settings"></a>Zkontrolujte nastavení oblasti a jazyka

Stránka [**Má nastavení**](https://businesscentral.dynamics.com?page=9176 "Přejděte přímo na stránku uživatelských nastavení v Business Central") specifikuje **Oblast** a **Jazyk** , které používáte v aplikaci. Toto nastavení ovlivňuje způsob zadávání dat a časů. 

-   Nastavení **Oblast** určuje způsob zobrazení nebo formátování dat, časů, čísel a měn.

-   U vzorů dat, která zahrnují slova, musí jazyk použitých slov odpovídat nastavení **Jazyka**

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] používá gregoriánský kalendářní systém.

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a>Vkládání data

Do datového pole můžete zadat datum pomocí standardního formátu pro vaše nastavení regionu. Různé regiony mohou používat různé oddělovače mezi dny, měsíci a lety. Například některé regiony používají pomlčky (mm-dd-rrrr) a jiné používají lomítka (mm/dd/rrrr). Můžete však použít libovolné oddělovače, dokonce i mezeru a datum se automaticky změní, aby se použily oddělovače, které odpovídají vašemu regionu.

Nezapomeňte, že formát, ve kterém jsou data zobrazena v tištěných sestavách nebo e-mailech, není ovlivněn vaším osobním výběrem oblasti.

Pro produktivnější práci s daty a časy můžete použít kteroukoli z metod nebo formátů, které jsou popsány v následujících částech. 

### <a name="picking-dates-from-the-calendar"></a>Vybírání dat z kalendáře

Libovolné pole zobrazující ikonu kalendáře může být nastaveno pomocí výběru kalendářního data. Chcete-li zobrazit výběr data kalendáře, aktivujte ikonu kalendáře nebo v poli stiskněte klávesovou zkratku Ctrl + Home.

![Datová pole](media/ui-date-field.png "Příklad datového pole")

Viz také [Klávesové zkratky ve výběru dat v kalendáři](keyboard-shortcuts.md#calendarshortcuts)

### <a name="day-week-year-pattern"></a>Vzor den\-týden\-rok

Datum můžete zadat jako pracovní den následovaný číslem týdne a volitelně rokem. Například, `Mon25` nebo `mon25` znamená pondělí v 25. týdnu. Pokud nezadáte rok, použije se rok pracovního data.

Místo zadávání celého slova pro den v týdnu můžete zadat část slova od začátku. V případě konfliktů (jako je to s `s`, kde se může jednat o středu nebo sobotu) se dny vyhodnocují podle nastavení oblasti. Vstup je nejprve vyhodnocen proti `workdate` a také `today`, takže mějte toto na paměti při zkracování. Například, `t` již znamená dnes, takže to nemůže znamenat úterý nebo čtvrtek.

Schéma čísla týdne je vždy ISO 8601, kde týden 1 je týden se 4. lednem v týdnu, nebo týden s prvním čtvrtkem roku.

### <a name="digit-patterns"></a>Číselné vzory

Do datového pole můžete zadat dvě, čtyři, šest nebo osm číslic:

-   Pokud zadáte pouze dvě číslice, bude to interpretováno jako den a přidá se měsíc a rok pracovního dne.

-   Pokud zadáte čtyři číslice, bude to interpretováno jako den a měsíc a přidá se pouze rok daného pracovního roku. Pořadí dne a měsíce je určeno nastavením vaší oblasti. I v případě, že má vaše nastavení oblasti rok před dnem a měsícem, čtyři číslice jsou interpretovány jako den a měsíc.

-   Pokud je datum, které chcete zadat, v rozsahu 01/01/1930 až 31/31/2029, můžete zadat rok dvěma číslicemi; jinak zadejte rok čtyřmi číslicemi.

### <a name="today"></a>Dnes

Zadejte slovo pro `today`, v jazyce nastaveném v nastavení **Jazyk** které nastaví datum na aktuální datum. Místo zadávání celého slova můžete zadat část slova, počínaje od začátku, například jako `t`, nebo `tod` , pokud to není také začátek jiného slova.

### <a name="period"></a>Období

Chcete-li filtrovat konkrétní účetní období, zadejte do pole datum písmeno `p` nebo slovo `period` následováno číslem, které identifikuje účetní období, jako `p2` nebo `period4`. Účetní období je relativní k fiskálnímu roku aktuálního pracovního data, který je nastaven v Centru rolí. Například pokud je pracovní datum **03/21/20**, pak `p1` nebo jen `p` filtruje za první účetní období fiskálního roku 2020 (například `01/01/20..01/31/20`). `p15` filtruje za patnácté účetní období od začátku fiskálního roku 2020 (například `03/01/21..03/31/21`). 

Účetní období jsou definována na stránce **Účetní období**. Chcete-li zobrazit nebo změnit účetní období, otevřete stránku [zde](https://businesscentral.dynamics.com/?page=100).

### <a name="current-work-date"></a>Aktuální pracovní datum

Funkce pracovního data umožňuje zaznamenávat transakce pomocí data, které se liší od aktuálního data.

Slovo pro „pracovní datum“ v jazyce nastaveném v nastavení **Jazyk** nastaví datum na aktuálně nastavené pracovní datum, které je zadáno na stránce[**Má nastavení**](https://businesscentral.dynamics.com?page=9176 "Přejděte přímo na stránku s uživatelskými nastaveními v Business Central") Místo zadávání celého slova můžete zadat část slova počínaje od začátku, například „p“ nebo „pracovní“.

Pokud jste nedefinovali pracovní datum, použije se jako pracovní datum aktuální datum. Možná budete chtít použít pracovní datum, pokud máte mnoho transakcí s jiným než dnešním datem.

Viz také [Změna základních nastavení, například pracovního data](ui-change-basic-settings.md#work-date). 

### <a name="closing-date"></a>Datum uzávěrky

Když uzavřete fiskální rok, můžete použít data uzávěrky k označení, že položka je položkou uzávěrky. Datum uzávěrky je technicky mezi dvěma daty, například mezi 31. prosincem a 1. lednem.

Chcete-li určit, že datum je datum uzávěrky, vložte `C` těsně před datum, například `C123101`. To lze použít v kombinaci se všemi datovými vzory.

### <a name="examples"></a>Příklady:

Následující tabulka obsahuje příklady dat ve všech formátech. Předpokládá nastavení oblasti, které formátuje data podle: **rok.měsíc.den.**, týden začínající v pondělí a anglický jazyk.

|**Vstup**      |**Interpretace**      |
|---------------|------------------------|
|`2018.12.31.`|2018.12.31.|
|`181231`|2018.12.31.|
|`18.12.31.`|2018.12.31.|
|`18.12.31.`|2018.12.31.|
|`20181231`|2018.12.31.|
|`18/12,31`|2018.12.31.|
|`11`|pracovní datum rok.pracovní datum měsíc.11.|
|`1112`|pracovní datum rok.11.12.|
|`t` nebo `today`|dnešní datum|
|`p4`|časové období, které zahrnuje čtvrté účetní období, např. `04/01/20..04/30/20`|
|`w` nebo `workdate`|pracovní datum|
|`m` nebo `Monday`|Pondělí týdne pracovního data|
|`tu` nebo `Tuesday`|Úterý týdne pracovního data|
|`sa` nebo `Saturday`|Sobota týdne pracovního data|
|`s` nebo `Sunday`|Neděle týdne pracovního data|
|`t23`|Úterý 23. týdne roku pracovního data|
|`t 23`|Úterý 23. týdne roku pracovního data|
|`t-1`|Úterý 1. týdne roku pracovního data|

##  <a name="BKMK_SettingDateRanges"></a> Nastavení rozsahů

V seznamech, součtech a sestavách můžete nastavit filtry podle dat, časů a datových časů obsahujících počáteční hodnotu a případně koncovou hodnotu tak, aby zobrazovala pouze data obsažená v tomto rozsahu. Pro způsob nastavování časových období platí standardní pravidla.

|**Význam**|**Ukázkový výraz (Datum)**|**Data obsažená ve filtru**|
|-----------|---------------------|--------------------|
|Interval|`12 15 00..01 15 01`<br /><br />`..12 15 00`<br /><br />`p1..p4`|Záznamy s daty mezi a včetně 12 15 00 a 01 15 01.<br /><br />Záznamy s daty 12 15 00 nebo staršími.<br /><br />Časové období, které zahrnuje druhé, třetí a čtvrté účetní období, například `01/01/20..04/30/20`.|
|Buď/nebo|`12 15 00|12 16 00`|Záznamy s daty buď 12 15 00 nebo 12 16 00. Pokud jsou záznamy s daty v obou dnech, zobrazí se všechny.|
|Kombinace|`12 15 00|12 01 00..12 10 00`  \n`..12 14 00|12 30 00`|Záznamy s daty 12 15 00 nebo s daty mezi 12 01 00 a 12 10 00 včetně.  \n Záznamy s daty 12 14 00 nebo dřívějšími nebo daty 12 30 00 nebo novějšími, tj. všechny záznamy s výjimkou těch, které mají data mezi 12 15 00 a 12 29 00 včetně.|

Ve filtrech rozsahu dat můžete použít kterýkoli z platných formátů. Například `mon14 3..t 4p` aplikovaný na pole dat a časů bude výsledkem filtru od 3:00 v pondělí 14. týdnu aktuálního roku pracovního data, včetně, dodnes, do 16:00, včetně.

## <a name="using-date-formulas"></a>Použití vzorců dat
Vzorec data je krátká, zkrácená kombinace písmen a číslic, která určuje, jak vypočítat data. Vzorce data můžete zadat do různých výpočetních polí nebo filtrů.

> [!NOTE]
>  Ve všech polích vzorců dat je jeden den automaticky zahrnut jako den, kdy začíná období. Podle toho například, pokud zadáte `1W`, pak období je ve skutečnosti osm dní, protože je zahrnutý i dnešek. Chcete-li určit období sedmi dnů \(skutečný týden\) včetně data začátku období, musíte zadat `6D` nebo `1W-1D`.

Zde je několik příkladů, jak lze použít vzorce:

-   Vzorec data v poli frekvence periody v periodických denících určuje, jak často bude položka na řádku deníku zaúčtována.

-   Vzorec data v poli **Lhůta odkladu** pro určenou úroveň upomínky určuje časové období, které musí uplynout od data splatnosti \(nebo od data předchozí upomínky\), než bude upomínka vytvořena.

-   Vzorec data v poli **Výpočet splatnosti** určuje, jak vypočítat datum splatnosti na upomínce.

Vzorec data může obsahovat maximálně 20 znaků,spolu číslic i písmen. Můžete použít následující písmena, což jsou zkratky pro kalendářové jednotky.

|  Písmeno  |  Význam  |
|----------|----------------------|
|`C`|Aktuální|
|`D`|Dny\(\)|
|`W`|Týdny\(\)|
|`M`|Měsíce\(\)|
|`Q`|Čtvrtletí\(\)|
|`Y`|Roky\(\)|

Vzorec data můžete vytvořit třemi způsoby.

Následující příklad ukazuje, jak používat `C`, pro aktuální a časovou jednotku.

|  Výraz  |  Význam  |
|--------------|-----------|
|`CW`|Aktuální týden|
|`CM`|Aktuální měsíc|

Následující příklad ukazuje, jak používat číslo a časovou jednotku. Číslo nesmí být větší než 9999.

|  Výraz  |  Význam  |
|--------------|-----------|
|`10D`|10 dnů od dnešního dne|
|`2W`|2 týdny od dnešního dne|

Následující příklad ukazuje, jak používat časovou jednotku a číslo.

|  Výraz  |  Význam  |
|--------------|-----------|
|`D10`|Dalšího 10. dne v měsíci|
|`WD4`|Další čtvrtý den v týdnu \(čtvrtek\)|

Následující příklad ukazuje, jak můžete tyto tři formy kombinovat podle potřeby.

|  Výraz  |  Význam  |
|--------------|-----------|
|`CM+10D`|Aktuální měsíc \+ 10 dnů|

Následující příklad ukazuje, jak můžete použít znaménko mínus k označení data v minulosti.

|  Výraz  |  Význam  |
|--------------|-----------|
|`-1Y`|Před 1 rokem od dnešního dne|

> [!IMPORTANT]
>  Pokud lokace používá základní kalendář, pak se vzorec data, který zadáte, například pole **Doba dodávky**, interpretuje podle pracovních dnů kalendáře. Například `1W` znamená sedm pracovních dnů.
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a>Zadávání časů
Když zadáváte časy, můžete mezi jednotky vložit libovolné bezmezerové oddělovače, které chcete, ale pokud pro každou jednotku až do milisekund použijete dvojciferné číslice, není to nutné.

Musíte pouze napsat největší jednotky, které vyžadujete; zbytek bude nastaven na nulu. Můžete také vynechat jakýkoli indikátor AM / PM.

V následující tabulce jsou uvedeny různé způsoby zadávání časů a jejich interpretace. Předpokládá nastavení oblasti, které formátuje časy podle: **Hodiny:Minuty:Sekundy.Milisekundy.** a používá ukazatele AM a PM pro „AM“ a „PM“.

|**Vstup**      |**Interpretace**      |
|---------------|------------------------|
|`05:23:17`|5:23:17|
|`5`|05:00:00|
|`5AM`|05:00:00|
|`5P`|17:00:00|
|`12`|12:00:00|
|`12A`|0:00:00|
|`12P`|12:00:00|
|`17`|17:00:00|
|`5:30`|5:30:00|
|`0530`|5:30:00|
|`5:30:5`|5:30:05|
|`053005`|5:30:05|
|`5:30:5,50`|05:30:05.5|
|`053005050`|05:30:05.05|

Měli byste si být vědomi, že milisekundy jsou interpretovány jako desítkový zápis. Takže například `3`, `30` a `300` všechny znamenají 300 milisekund, zatímco `03` znamená `30` a `003` znamená 3 milisekundy.

Nemůžete použít `24:00` pro půlnoc nebo použít jakoukoli hodnotu větší než 24:00.

Slovo pro „čas“ v jazyce používaném v [!INCLUDE[d365fin](includes/d365fin_long_md.md)] bude vyhodnoceno na aktuální čas ve vašem počítači nebo mobilním zařízení. Můžete zadat libovolnou část slova počínaje od začátku, například `t` nebo `TIM`.

## <a name="entering-combined-dates-and-times"></a>Zadávání kombinovaných dat a časů
Když zadáte Datum/čas, které jsou kombinací data a času v jednom poli, musíte vložit mezeru mezi datem a časem. Část data může obsahovat pouze mezery ve formě oficiálního oddělovače data vašeho nastavení oblasti. Čas může obsahovat mezery kolem ukazatele AM / PM.

Je také možné zadat pouze datum do pole Datum/čas, ale není možné zadat pouze čas.

V následující tabulce jsou uvedeny některé příklady kombinací data a času. Nastavení oblasti v příkladech zobrazuje data ve formátu den\-měsíc\-rok, s použitím označení AM / PM, anglického jazyka a neděle jako začátku týdne.

|**Vstup**      |**Interpretace**      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|08\-01\-2016 05:48:12 PM|
|`131202 132455`|13\-12\-2002 13:24:55|
|`1-12-02 10`|01\-12\-2002 10:00:00|
|`1.12.02 5`|01\-12\-2002 5:00:00|
|`1.12.02`|01\-12\-2002 0:00:00|
|`11 12`|11\-pracovní datum měsíc\-pracovní datum rok 12:00:00|
|`1112 12`|11\-12\-pracovní datum rok 12:00:00|
|`t` nebo `today`|dnešní datum 00:00:00|
|`t 10:30`|dnešní datum 10:30:00|
|`t 3:3:3`|dnešní datum 3:03:03|
|`w` nebo `workdate`|pracovní datum 00:00:00|
|`m` nebo `Monday`|Pondělí týdne pracovního data 00:00:00|
|`tu` nebo `Tuesday`|Úterý týdne pracovního data 00:00:00|
|`sa` nebo `Saturday`|Sobota týdne pracovního data 00:00:00|
|`s` nebo `Sunday`|Sobota týdne pracovního data 00:00:00|
|`tu 10:30`|Úterý týdne pracovního data 10:30:00|
|`tu 3:3:3`|Úterý týdne pracovního data 3:03:03|
|`t23 t`|Úterý 23. týdne roku pracovního data, aktuální čas dne|
|`t23`|Úterý 23. týdne roku pracovního data|
|`t 23`|Dnes 23:00:00|
|`t-1`|Úterý 1. týdne roku pracovního data|

## <a name="entering-duration"></a>Zadávání doby trvání
Některá pole v aplikaci představují dobu trvání nebo množství uplynulého času namísto konkrétního data nebo času. Trvání zadáte jako číslo následované jeho měrnou jednotkou.

Zde jsou nějaké příklady.

|**Doba trvání**|**Měrná jednotka**|
|------------|-------------------|
|`2h`|2 hod|
|`6h 30 m`|6 hod 30 min|
|`6.5h`|6 hod 30 min|
|`90m`|1 hod 30 min|
|`2d 6h 30m`|2 dny 6 hod 30 min|
|`2d 6h 30m 56s 600ms`|2 dny 6 hod 30 min 56 sec 600 msec|

Můžete také zadat číslo, které bude automaticky převedeno na dobu trvání. Zadané číslo se převede podle výchozí měrné jednotky, která byla zadána pro pole trvání.

Chcete-li vidět, jaká měrná jednotka se používá v poli trvání, zadejte číslo a podívejte se, na kterou měrnou jednotku se převede.

Například pokud jsou měrnou jednotkou hodiny, číslo `5` se převede na 5 hodin.


## <a name="see-also"></a>Viz také
[Práce s [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Výpočet data pro nákupy](purchasing-date-calculation-for-purchases.md)  
[Zadávání kritérií ve filtrech ](ui-enter-criteria-filters.md)  
