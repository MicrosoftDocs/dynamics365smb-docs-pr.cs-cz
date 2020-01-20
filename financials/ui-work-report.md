---
title: Naplánování spouštění sestavy k určitému datu a času | Microsoft Docs
description: 'Zjistěte, jak zadat sestavu do fronty úloh a naplánovat její zpracování ke konkrétnímu datu a času.'
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report'
ms.date: 07/06/2017
ms.author: jswymer
---
# <a name="working-with-reports"></a>Práce se sestavami
Sestava shromažďuje informace na základě zadaného souboru kritérií a organizuje a prezentuje je ve snadno čitelném a tisknutelném formátu. Existuje mnoho sestav, ke kterým máte v rámci aplikace přístup. Tyto sestavy obvykle obsahují informace týkající se kontextu stránky, na které se právě nacházíte. Například stránka **Zákazníci** obsahuje sestavy pro 10 nejlepších zákazníků, statistiky prodeje a další.

Sestavy můžete najít v kartě **Sestavy** na vybraných stránkách, nebo pomocí vyhledávání dle názvu. Když otevřete sestavu, zobrazí se vám stránka, která vám umožní specifikovat informace (možnosti a filtry), určující, co chcete do zprávy zahrnout. V závislosti na sestavě můžete určit časové období nebo konkrétní záznam, jako je například zákazník nebo pořadí řazení. Zde je příklad:

![Možnosti sestavy](media/report_options.png "Možnosti sestavy")

## <a name="previewing-a-report"></a>Náhled sestavy
Chcete-li zobrazit sestavu v internetovém prohlížeči, zvolte **Náhled**. Chcete-li zobrazit řádek nabídek, najeďte myší na sestavu.  

![Panel nástrojů náhledu sestavy](media/report_viewer.png "Panel nástrojů náhledu sestavy")

Pomocí řádku nabídek můžete:

- Procházet stránkami
- Přiblížit a oddálit
- Změnit velikost, aby se obsah vešel do okna
- Označit text

  Můžete zkopírovat text ze sestavy a poté ho vložit někam jinam, například do stránky v [!INCLUDE [d365fin](includes/d365fin_md.md)] nebo do aplikace Microsoft Word.  Pomocí myši stiskněte a přidržte místo, kde chcete začít, a potom pohybem myši vyberete jedno nebo více slov, vět nebo odstavců. Poté můžete stisknout pravé tlačítko myši a vybrat **Kopírovat**. Vybraný text můžete vložit kamkoli budete chtít.
- Posun dokumentu

  Viditelnou část sestavy můžete přesunout libovolným směrem, abyste si mohli prohlédnout jiné oblasti nebo sestavu. To je užitečné, pokud jste přiblížili zobrazení, aby jste viděli podrobnosti.  Pomocí myši stiskněte a podržte tlačítko myši kdekoli v náhledu zprávy a poté pohněte myší.

- Stahujte do souboru PDF v počítači nebo síti.
- Tisk


## <a name="saving-a-report"></a>Uložení sestavy
Sestavu můžete uložit do dokumentu PDF, dokumentu Microsoft Word nebo dokumentu Microsoft Excel tak, že vyberete možnost **Odeslat do**  a poté provedete výběr.

## <a name="ScheduleReport"></a> Plánování spuštění sestavy
Můžete naplánovat spuštění sestavy v konkrétní datu a čase. Naplánované sestavy se zadávají do fronty úloh a zpracovávají se v naplánovaném čase, podobně jako u jiných úloh. Můžete si vybrat, zda chcete sestavu pouze zpracovat, nebo zpracovanou sestavu uložit do souboru, jako Excel, Word nebo PDF, případně ji vytisknout na vybranou tiskárnu. Pokud se rozhodnete uložit sestavu do souboru, bude zpracovaná sestava odeslána do **Schránky sestav** ve vašem Centru rolí, kde si ji můžete prohlédnout.

Můžete naplánovat sestavu při jejím otevření. Zvolíte akci **Plánovat** a poté zadáte informace, jako tiskárna, čas a datum. Sestava je následně přidána do fronty úloh a bude spuštěna ve specifikovaném čase. Po zpracování sestavy bude položka odstraněna z fronty úloh. Pokud jste zpracovanou sestavu uložili do souboru, bude k dispozici v oblasti **Schránka sestav**.

## <a name="PrintReport"></a>Tisk sestavy
Sestavu můžete vytisknout tlačítkem **Tisk** na stránce možností, která se zobrazí při otevření sestavy, nebo z řádku nabídek v Náhledu.

## <a name="using-saved-settings"></a>Použití uloženého nastavení
Sestava může obsahovat jeden nebo více záznamů v poli **Uložená nastavení**. *Uložená nastavení* jsou v podstatě předdefinované skupiny možností a filtrů, které můžete použít pro sestavu před zobrazením náhledu nebo jejím odesláním do souboru. Použití uložených nastavení je rychlý a spolehlivý způsob, jak důsledně generovat sestavy obsahující správná data.

Uložená položka nastavení s názvem **Naposledy použité možnosti a filtry** je vždy k dispozici. Tato položka nastaví sestavu tak, aby použila možnosti a filtry, které byly použity při posledním prohlížení sestavy.

>[!NOTE]
>Pokud jste administrátor, můžete vytvořit a spravovat uložená nastavení sestav pro všechny uživatele. Pro více informací se podívejte na [ Správa uložených nastavení sestav](reports-saving-reusing-settings.md).

## <a name="changing-the-layout-and-look-of-a-report"></a>Změna rozložení a vzhledu sestavy
Rozložení sestavy řídí, co se v sestavě zobrazí, jak je uspořádána a jak je stylizována. Pokud chcete přepnout na jiné rozložení, navštivte [Změna aktuálně používaného rozložení sestavy](ui-how-change-layout-currently-used-report.md). Pokud si chcete přizpůsobit své vlastní rozložení sestavy, navštivte [Vytvoření a úprava vlastního rozložení sestavy](ui-how-create-custom-report-layout.md).

## <a name="see-also"></a>Viz také
[Určete výběr tiskárny pro sestavy](ui-specify-printer-selection-reports.md)  
[Správa rozvržení sestav a dokumentů](ui-manage-report-layouts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
