---
title: Nastavení sestav pro tisk na konkrétních tiskárnách | Microsoft Docs
description: Naučte se o určování tiskárny pro sestavu a použití stránky Výběry tiskáren.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 10/01/2018
ms.author: solsen
---
# <a name="specify-printer-selection-for-reports"></a>určení výběru tiskárny pro sestavy
Tato stránka je prázdná, protože nelze nastavit konkrétní tiskárny pro konkrétní sestavy. Pracujeme na řešení tohoto problému.

Pokud chcete v současné době sestavu vytisknout, musíte ji nejprve stáhnout jako dokument PDF kliknutím na tlačítko **Odeslat do**. Poté vyberte typ souboru, který chcete stáhnout, a zvolte možnost **Dokument PDF**. Nyní můžete dokument PDF okamžitě otevřít a vytisknout jej, nebo ho uložit a vytisknout později.

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** page to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a>Viz také
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Spuštění dávkové úlohy](ui-how-run-batch-jobs.md)  
[Odeslat dokumenty e-mailem](ui-how-send-documents-email.md)  
