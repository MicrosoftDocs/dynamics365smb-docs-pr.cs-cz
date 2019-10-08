---
title: Naplánování spouštění sestavy k určitému datu a času | Microsoft Docs
description: 'Zjistěte, jak zadat sestavu do fronty úloh a naplánovat její zpracování ke konkrétnímu datu a času.'
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report'
ms.date: 10/01/2018
ms.author: jswymer
---
# <a name="working-with-reports-and-batch-jobs"></a>Práce se sestavami a dávkovými úlohami
Sestava shromažďuje informace na základě zadaného souboru kritérií a organizuje a prezentuje je ve snadno čitelném a tisknutelném formátu. Existuje mnoho sestav, ke kterým máte v rámci aplikace přístup. Tyto sestavy obvykle obsahují informace týkající se kontextu stránky, na které se právě nacházíte. Například stránka **Zákazníci** obsahuje sestavy pro 10 nejlepších zákazníků, statistiky prodeje a další.

Dávkové úlohy dělají víceméně to samé jako sestavy, ale za účelem provedení procesu. Například dávková úloha **Vytvořit upomínky** vytvoří upomínkové dokumenty pro zákazníky s opožděnými platbami.  

> [!NOTE]
> Toto téma se týká převážně „sestavy“, ale podobné informace platí i pro dávkové úlohy.

Sestavy můžete najít v záložce **Sestavy** na vybraných stránkách, nebo můžete použít ![vyhledávací žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), abyste našli sestavy podle jména.


## <a name="specifying-the-data-to-include-in-the-report"></a>Specifikace údajů, které mají být zahrnuty do sestavy
Když otevřete sestavu, obvykle se zobrazí stránka, na které nastavíte různé možnosti a filtry, které určují, co se má do sestavy zahrnout. Tato stránka se nazývá dialog sestavy. Stránka dialogu sestavy například umožňuje vytvořit sestavu pro konkrétního zákazníka, určité časové období, nebo uspořádat pořadí informací v sestavě. Zde je příklad stránky dialogu sestavy:

![Možnosti sestavy](media/report_options.png "Možnosti sestavy")

> [!Caution]
> Oddíl **Zobrazit výsledky** na stránce dialogu poskytuje obecnou možnost filtrování sestav. Tyto filtry jsou volitelné.<br /><br /> Některé sestavy budou ignorovat všechny takové filtry, což znamená, že bez ohledu na to, jaký filtr je nastaven v části **Zobrazit výsledky**, je výstup sestavy stejný. Není možné poskytnout seznam obsahující informace o tom, která pole jsou ignorována v kterých sestavách, takže při jejich užívání s nimi budete muset experimentovat.<br /><br />
**Příklad**: Při použití dávkové úlohy **Vytvořit upomínky** bude filtr pro **Položky zákazníka** v poli **Úrovně poslední vydané upomínky** ignorován, protože filtry jsou pro danou dávkovou úlohu pevně stanoveny.

### <a name="SavedSettings"></a>Použití uloženého nastavení
U některých sestav, podle toho, jak jsou navrženy, může stránka sestavy zahrnovat sekci **Uložená nastavení**, která obsahuje jeden nebo více záznamů v poli **Použít výchozí hodnoty z**. Položky v tomto poli se nazývají *uložená nastavení*. Uložené nastavení je v podstatě předdefinovaná skupina možností a filtrů, které můžete použít pro sestavu před zobrazením náhledu nebo jejím odesláním do souboru. Uložená položka nastavení s názvem **Naposledy použité možnosti a filtry** je vždy k dispozici. Tato položka nastaví sestavu tak, aby použila možnosti a filtry, které byly použity při posledním prohlížení sestavy.

Použití uložených nastavení je rychlý a spolehlivý způsob, jak důsledně generovat sestavy obsahující správná data. Po nastavení pole **Použít výchozí hodnoty z** v položce uloženého nastavení můžete před zobrazením náhledu nebo uložením sestavy změnit libovolné možnosti a filtry. Provedené změny nebudou uloženy do vybrané položky uložených nastavení, ale do **Naposledy použitých možností a filtrů**.

>[!NOTE]
>Pokud jste administrátor, můžete vytvořit a spravovat uložená nastavení sestav pro všechny uživatele. Pro více informací se podívejte na [ Správa uložených nastavení sestav](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Nastavení možností a filtrů
Pokud chcete dále omezit nebo přesně určit data, která jsou obsažena v sestavě, můžete nastavit další možnosti a filtry.

Filtry umožňují zobrazit data na základě konkrétních kritérií. Filtry jsou seskupeny podle celku, do kterého patří, jako je například **Zákazník** na obrázku výše. Filtr definujete nastavením pole **Kde** v poli, na kterém chcete filtrovat, a přidáním kritérií do pole **je:**. Například na obrázku výše je jediný filtr, který vytvoří sestavu pro zákazníka, jehož **Číslo** je **01121212**.

Další filtry můžete přidat nastavením polí **Přidat**. Pokud máte více než jeden filtr, budou do přehledu zahrnuty pouze výsledky, které splňují kritéria pro všechny filtry.

V závislosti na typu pole, které filtrujete, můžete určit kritéria filtru, která budou hledat přesnou shodu, částečnou shodu, rozsah hodnot a další. Další informace o nastavení filtrů naleznete v části:
-   [Filtrování](ui-enter-criteria-filters.md#FilterCriteria)
-   [Práce s kalendářními daty a časy](ui-enter-date-ranges.md)

## <a name="previewing-a-report"></a>Náhled sestavy
Chcete-li zobrazit sestavu v internetovém prohlížeči, zvolte **Náhled**. Chcete-li zobrazit řádek nabídek, najeďte myší na sestavu.  

![Panel nástrojů náhledu sestavy](media/report_viewer.png "Panel nástrojů náhledu sestavy")

Pomocí řádku nabídek můžete:

-   Procházet stránkami
-   Přiblížit a oddálit
-   Změnit velikost, aby se obsah vešel na stránku
-   Označit text

    Můžete zkopírovat text ze sestavy a poté ho vložit někam jinam, například do stránky v [!INCLUDE[d365fin](includes/d365fin_md.md)] nebo do aplikace Microsoft Word.  Pomocí myši stiskněte a přidržte místo, kde chcete začít, a potom pohybem myši vyberete jedno nebo více slov, vět nebo odstavců. Poté můžete stisknout pravé tlačítko myši a vybrat **Kopírovat**. Vybraný text můžete vložit kamkoli budete chtít.
-   Posun dokumentu

    Viditelnou část sestavy můžete přesunout libovolným směrem, abyste si mohli prohlédnout jiné oblasti nebo sestavu. To je užitečné, pokud jste přiblížili zobrazení, aby jste viděli podrobnosti.  Pomocí myši stiskněte a podržte tlačítko myši kdekoli v náhledu zprávy a poté pohněte myší.

-   Stahujte do souboru PDF v počítači nebo síti.
-   Tisk


## <a name="saving-a-report"></a>Uložení sestavy
Sestavu můžete uložit do dokumentu PDF, dokumentu Microsoft Word nebo dokumentu Microsoft Excel tak, že vyberete možnost **Odeslat do**  a poté provedete výběr.

## <a name="ScheduleReport"></a> Plánování spuštění sestavy
Můžete naplánovat spuštění sestavy v konkrétní datu a čase. Naplánované sestavy se zadávají do fronty úloh a zpracovávají se v naplánovaném čase, podobně jako u jiných úloh. Můžete si vybrat, zda chcete sestavu pouze zpracovat, nebo zpracovanou sestavu uložit do souboru, jako Excel, Word nebo PDF, případně ji vytisknout na vybranou tiskárnu. Pokud se rozhodnete uložit sestavu do souboru, bude zpracovaná sestava odeslána do **Schránky sestav** ve vašem Centru rolí, kde si ji můžete prohlédnout.

Můžete naplánovat sestavu při jejím otevření. Zvolíte akci **Plánovat** a poté zadáte informace, jako tiskárna, čas a datum. Sestava je následně přidána do fronty úloh a bude spuštěna ve specifikovaném čase. Po zpracování sestavy bude položka odstraněna z fronty úloh. Pokud jste zpracovanou sestavu uložili do souboru, bude k dispozici v oblasti **Schránka sestav**.

## <a name="PrintReport"></a>Tisk sestavy
Sestavu můžete vytisknout tlačítkem **Tisk** na stránce možností, která se zobrazí při otevření sestavy, nebo z řádku nabídek v Náhledu.

## <a name="changing-the-layout-and-look-of-a-report"></a>Změna rozložení a vzhledu sestavy
Rozložení sestavy řídí, co se v sestavě zobrazí, jak je uspořádána a jak je stylizována. Pokud chcete přepnout na jiné rozložení, navštivte [Změna aktuálně používaného rozložení sestavy](ui-how-change-layout-currently-used-report.md). Pokud si chcete přizpůsobit své vlastní rozložení sestavy, navštivte [Vytvoření a úprava vlastního rozložení sestavy](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Viz také
[Určete výběr tiskárny pro sestavy](ui-specify-printer-selection-reports.md)  
[Správa rozvržení sestav a dokumentů](ui-manage-report-layouts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
