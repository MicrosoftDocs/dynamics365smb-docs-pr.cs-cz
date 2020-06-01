---
title: Export Your Business Central Data to Excel| Microsoft Docs
description: You can export your financial reports and business intelligence data from Business Central  to Excel, or open your data in Excel.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, reporting, financial report, business intelligence, BI, Excel
ms.date: 01/13/2020
ms.author: edupont

---
# Export vašich obchodních dat do Excelu
Pokud chcete pracovat s vašimi daty z [!INCLUDE[d365fin](includes/d365fin_md.md)] v Excelu, můžete v Excelu otevřít všechny seznamy a pracovat s nimi. Podobně, pokud chcete zrušit předplatné [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete exportovat data do Excelu, abyste si je mohli zachovat.

## Otevření seznamů v aplikaci Excel
Data můžete otevírat v Excelu z libovolného deníku, seznamu nebo sešitu. Jednoduše otevřete požadovanou stránku a poté zvolte **Otevřít v apliaci Excel**. Otevřete například seznam Zákazníků (hledejte **Zákazníci**) a poté akci **Otevřít v aplikaci Excel** . Váš prohlížeč vás vyzve k otevření nebo uložení vygenerovaného sešitu aplikace Excel.

> [!NOTE]
> Tuto možnost použijte, pokud nechcete provádět změny a nahrát tyto změny zpět do [!INCLUDE[d365fin](includes/d365fin_md.md)].

Každý seznam obsahuje několik sloupců a export do Excelu bude zahrnovat všechny sloupce, které jsou v aktuálním zobrazení. Chcete-li přidat nebo odebrat sloupce před otevřením seznamu v aplikaci Excel, stačí otevřít místní nabídku pro libovolný sloupec a určit, které sloupce chcete zobrazit. Tento seznam sloupců se u většiny seznamů liší a odráží strukturu databáze, ve které jsou data uložena. Pokud si nejste jisti, jaký typ dat určitý sloupec obsahuje, můžete je přidat do svého zobrazení a pak se rozhodnout, zda je chcete znovu odebrat.

### Úpravy dat v Excelu
Váš [!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje doplněk pro Excel, takže můžete upravovat data v Excelu. Pro více informací běžte na [Analýza finančních výkazů v aplikaci Excel](finance-analyze-excel.md)

## Export dat do jiných finančních systémů
Pokud se rozhodnete zrušit předplatné aplikace [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete exportovat data do aplikace Excel a přenést do nového finančního systému.

Samozřejmě můžete exportovat všechny stránky, ale to může být více, než skutečně potřebujete. Zvažte export následujících základních tabulek a nezapomeňte přidat všechny sloupce, jak je popsáno výše:

* Účetní osnova
* Zákazníci
* Dodavatelé
* Banky
* Zboží

Pokud chcete také všechny své finanční transakce, jedná se o velké množství dat, takže export bude často trvat déle než několik minut. Finanční transakce jsou zobrazeny na stránce **Věcné položky**.

Doporučujeme také zvážit export dat z následujících stránek:

* Položky zákazníka
* Položky dodavatele
* Položky bankovního účtu
* Položky zboží
* Nastavení obecného účtování
* Účto skupiny zákazníků
* Účto skupiny dodavatele
* Účto skupiny zboží
* Účto skupiny bankovního účtu
* Finanční rozpočty
* Položky finančního rozpočtu
* Prodejní nabídky
* Prodejní faktury
* Nákupní faktury
* Kontakty
* Prodejci

> [!NOTE]  
> Pokud jste založili více než jednu společnost v [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte exportovat data z každé společnosti.

## Viz související školení v programu [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Viz také
[Zrušení předplatného [!INCLUDE[d365fin](includes/d365fin_md.md)]](admin-cancel.md)  
[Import obchodních dat z jiných finančních systémů](across-import-data-configuration-packages.md)  
[Analýza finančních výkazů v Microsoft Excel](finance-analyze-excel.md)  
[Finance](finance.md)  
[Obecné obchodní Funkcionality](ui-across-business-areas.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
