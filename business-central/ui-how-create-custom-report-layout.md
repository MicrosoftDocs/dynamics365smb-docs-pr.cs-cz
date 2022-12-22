---
title: Create and Modify Custom Layouts for Reports and Documents
description: Learn how to create customized layouts to personalize the appearance of a report when viewed, printed, or saved.
author: SorenGP

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/06/2022
ms.author: edupont

---
# (Zastaralé) Vytvoření a úprava vlastní rozvržení sestavy

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

Ve výchozím nastavení mají sestavy vestavěné rozvržení sestav. Rozložení může být buď rozvržení sestavy RDLC, rozvržení sestavy aplikace Word nebo obojí. Předdefinovaná rozvržení nelze upravovat, ale můžete vytvářet vlastní rozvržení. Sestava může mít více vlastních rozvržení sestavy

> [!NOTE]  
> V [!INCLUDE[prod_short](includes/prod_short.md)], se termín "sestava" vztahuje také na doklady určené pro externí použití, jako jsou prodejní faktury a potvrzení objednávek, které zasíláte zákazníkům jako soubory PDF..

Chcete-li vytvořit vlastní rozvržení, zkopírujte existující vlastní rozvržení nebo přidejte nové vlastní rozvržení. Vlastní rozvržení jsou často založena na vestavěném rozložení. Když přidáte nové vlastní rozvržení, můžete přidat typ rozvržení sestavy RDLC nebo Word nebo obojí. Nové vlastní rozvržení bude založeno na předdefinovaném rozvržení sestavy, pokud je k dispozici. Pokud pro typ neexistuje žádné předdefinované rozvržení, vytvoří se nové prázdné rozvržení. Budete muset upravit a navrhnout toto prázdné rozvržení od nuly. Pro více informací o rozvržení sestav RDLC a Word, vestavěných a vlastních sestavách běžte na [Správa Rozvržení Sestav](ui-manage-report-layouts.md).

> [!TIP]
> Pomocí účetního schímat získáte přehled o finančních údajích uložených v účtové osnově. Další informace naleznete v tématu [Příprava finančního výkaznictví s účetními schématy a kategoriemi účtů](bi-how-work-account-schedule.md).

Po definování vlastních rozložení sestav je můžete vybrat na stránkách Karty zákazníka a Karty dodavatele. Rozvržení budou použita při vytváření dokladů pro zákazníky nebo dodavatele. Další informace naleznete v tématu [Definování rozvržení dokladů pro zákazníky a dodavatele](ui-define-customer-vendor-document-layouts.md).

K přidání obsahu do e-mailových zpráv můžete také použít vlastní rozvržení sestavy. Rozvržení sestav může například ušetřit čas a pomoci zajistit konzistenci tím, že při komunikaci se zákazníky znovu použije stejný obsah. Chcete-li použít vlastní rozvržení sestavy pro e-mail, typ souboru pro rozvržení musí být Word. Nelze použít typ souboru RDLC. Pro více informací navštivte <g2> Nastavení opakovaně použitelných e-mailových textů a rozvržení</g2>.

## Vytvoření vlastního rozvržení

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výběr rozvržení sestav** a poté vyberte související odkaz.

   Na stránce **Výběr rozvržení sestav** jsou uvedeny všechny přehledy, které jsou k dispozici ve společnosti specifikované v poli **Název společnosti** v horní části stránky.
2. V poli **Název společnosti** vyberte společnost, pro kterou chcete vytvořit rozvržení sestavy.
3. Vyberte řádek pro sestavu, pro kterou chcete vytvořit rozvržení, a pak zvolte akci **Vlastní rozvržení**.

   Otevře se stránka **Vlastní rozvržení sestav** a zobrazí se všechna vlastní rozvržení, která jsou k dispozici pro vybranou sestavu.
4. Pokud chcete vytvořit kopii existujícího vlastního rozvržení, vyberte existující vlastní rozvržení v seznamu a poté vyberte akci **Kopírovat**.

   Kopie vlastního rozvržení se zobrazí na stránce **Vlastní rozvržení sestav** a v poli *Popis* obsahuje slova **Kopírovat z**
5. Pokud chcete přidat nové vlastní rozvržení založené na vestavěném rozvržení, postupujte takto:
   1. Vyberte akci **Nový**. Zobrazí se stránka **Vložit rozvržení sestavy**. Pole **ID** a **Název** jsou automaticky vyplněny.
   2. Chcete-li přidat vlastní typ rozvržení sestavy aplikace Word, zaškrtněte políčko **Vložit rozvržení Wordu**.
   3. Chcete-li přidat vlastní typ rozvržení sestavy RDLC, zaškrtněte políčko **Vložit RDLC rozvržení**.
   4. Zvolte tlačítko **OK**.

   Nové vlastní rozvržení se zobrazí na stránce **Vlastní rozvržení sestav**. Pokud je nové rozvržení založeno na vestavěném rozvržení, bude v poli **Popis** uvedeno **Kopírovat z Vestavěné rozvržení**. Pokud pro sestavu nebylo žádné vestavěné rozvržení, má nové rozvržení v poli **Popis** slova **Nové rozvržení**, což znamená, že vlastní rozvržení je prázdné.
6. Ve výchozím nastavení je pole **Název společnosti** prázdné, což znamená, že vlastní rozvržení bude k dispozici pro sestavu ve všech společnostech. Chcete-li zpřístupnit vlastní rozvržení pouze v určité společnosti, zvolte **Upravit** a poté nastavte pole **Název společnosti** na požadovanou společnost.

Vlastní rozvržení bylo vytvořeno. Nyní můžete upravit vlastní rozvržení podle potřeby.

> [!TIP]
> Výsledky sestavy můžete exportovat do souboru aplikace Excel pro zobrazení celé datové sady, včetně všech sloupců, ale bez rozvržení. Soubor aplikace Excel vám může pomoci ověřit, zda sestava vrací očekávaná data nebo diagnostikovat problémy. Pro více informací navštivte [Analýza dat sestav pomocí Excelu](report-analyze-excel.md).

## <a name="ModifyCustomLayout"></a>Úprava vlastního rozvržení

Chcete-li změnit rozvržení sestavy, musíte nejprve exportovat rozvržení sestavy jako soubor do umístění v počítači nebo síti. Poté otevřete exportovaný dokument a proveďte změny. Po dokončení změn importujete rozvržení sestavy.

### Úprava vlastního rozvržení

1. Vlastní rozvržení exportujete ze stránky **Vlastní rozvržení sestav**. Pokud tato stránka ještě není otevřené, vyhledejte a otevřete stránku **Výběr rozvržení sestav**, vyberte sestavu, která má rozvržení, které chcete upravit, a poté vyberte akci **Vlastní rozvržení**
2. Na stránce **Vlastní rozvržení sestav** vyberte rozvržení, které chcete upravit, vyberte akci **Exportovat rozvržení** a poté zvolte **Uložit** nebo **Uložit jako**, chcete-li dokument rozvržení sestavy uložit do umístění v počítači nebo síti.
3. Otevřete dokument rozvržení sestavy, který jste právě uložili, a proveďte změny.

   Pokud měníte rozvržení aplikace Word, otevřete dokument rozvržení v aplikaci Word. Pro více informací navštivte [Práce s rozvržením aplikace Word](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   Rozložení sestavy RDLC je pokročilejší než rozložení sestavy Word. Další informace o úpravě rozvržení sestavy RDLC naleznete v tématu [Navrhování rozvržení sestav RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

   Po dokončení nezapomeňte změny uložit.

4. Vraťte se na stránku **Vlastní rozvržení sestav**, vyberte rozvržení sestavy, které jste exportovali a upravili, a poté vyberte akci **Importovat rozvržení**.

5. V dialogovém okně **Import** zvolte **Vybrat** aby jste našli a vybrali dokument, který definuje rozvržení sestavy a poté zvolte **Otevřít**.

> [!IMPORTANT]
> Nezapomeňte importovat dokument rozvržení sestavy, který jste upravili. V opačném případě nebude nové rozložení sestavy k dispozici.

<!--
##  <a name="MakeChangesToLayout"></a> Create and Modify Custom Report Layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word, like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding Fonts in Word Layouts for Consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. For more information about embedding fonts in Word, see [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing Label and Data Fields in Word Layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field that you want to delete, and then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is a more advanced and requires some knowledge of the report dataset. For information about adding fields for data, labels, data, and images, see [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## Podívejte se na související školení na webu [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## Viz také

[Správa rozvržení sestav](ui-manage-report-layouts.md)  
[Změna aktuáního rozvržení sestavy](ui-how-change-layout-currently-used-report.md)  
[Import a Export vlastního rozvržení sestav](ui-how-import-and-export-report-layout.md)  
[Práce se sestavamy, dávkovými úlohami a XMLporty](ui-work-report.md)  
[Příprava finančních výkazů s účtovým rozvrhem a kategoriemi účtů](bi-how-work-account-schedule.md)
[Business Intelligence](bi.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]