---
    title: Migrate Customer Data | Microsoft Docs
    description: You can migrate existing customer data from an existing ERP system to Business Central using RapidStart Services. You can use Excel .xlsx files as the data carrier. You can also manually move the data by entering it directly into the company.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2019
    ms.author: sgroespe

---
# Migrace zákaznických dat
Existující data zákazníka můžete migrovat ze stávajícího ERP systému do [!INCLUDE[d365fin](includes/d365fin_md.md)] pomocí nástrojů pro migraci dat služby RapidStart Services. Jako datový nosič můžete použít soubory aplikace Excel. Data můžete také přesunout ručně tak, že je zadáte přímo do společnosti.

Sešit **Přehled migrace** a **konfigurační sešit** poskytují přístup k funkcím a zobrazením, které umožňují provádět všechny úkoly související s migrací dat. Doporučujeme migrovat vždy jednu tabulku, abyste mohli zpracovat závislosti na datech. Při migraci se také dotknete tabulek hlavních dat, které obsahují informace o zákaznících, dodavatelích, zboží, kontaktech a financích.

## Import konfiguračních balíčků
Když vytvoříte novou společnost, můžete importovat nastavení společnosti pro novou společnost. Importujete nastavení ze souboru .rapidstart, který dodává obsah balíčku v komprimovaném formátu. Bude importována odpovídající sada výchozích tabulek migrace dat. Datová sada obsahuje tabulky hlavních dat a tabulky nastavení. Prvním úkolem při migraci dat je vyhodnotit, zda výchozí nastavení migrace splňuje požadavky nové společnosti.

> [!NOTE]
> Nelze přejmenovat soubor, který již není konfiguračním balíčkem RapidStart Services, jako konfigurační soubor .rapidstart a zkuste jej importovat. Pokud se o to pokusíte, zobrazí se chybová zpráva.

Než začnete, ujistěte se, že jste v centru rolí implementátora služeb RapidStart.

> [!IMPORTANT]
> Při exportu a importu konfiguračních balíčků mezi dvěma podnikovými databázemi by databáze měly mít stejné schéma, aby se zajistilo úspěšné přenesení všech dat. To znamená, že databáze by měly mít stejnou tabulku a strukturu polí, ve kterých tabulky mají stejné primární klíče a pole mají stejné ID a datové typy.
> Můžete importovat konfigurační balíček, který byl exportován z databáze s jiným schématem, než je cílová databáze. Všechny tabulky nebo pole v konfiguračním balíčku, které chybí v cílové databázi nebudou importovány.
> Tabulky, které mají různé primární klíče a pole s odlišnými datovými typy, nebudou také úspěšně importovány. Pokud například konfigurační sada obsahuje tabulku **50000 zákazník** s primárním klíčem **Code20** a databáze, do které importujete sadu, obsahuje tabulku **50000 bankovní účet zákazníka** , který má primární klíč **Code20 + Code20** , data nebudou importována.

1. Otevřete novou společnost.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační balíčky** a poté vyberte související odkaz.
3. Vyberte tlačítko **Importovat balíček**. Vyhledejte souboru baličku rapidstart, který chcete importovat a poté zvolte tlačítko **Otevřít**. Během importu je obsah balíčku dekomprimován a je vytvořen záznam balíčku.

   Po dokončení importu můžete vidět počet konfiguračních tabulek, které byly importovány v poli **Počet  tabulek**.
4. Chcete-li si prohlédnout seznam konfiguračních tabulek, zvolte tlačítko **Pohled**.
5. Chcete-li balíček použít, zvolte tlačítko **Použít balíček**.

   > [!NOTE]
Informace o migraci dat jsou založeny na konfiguračních šablonách, pokud je zadáte. Chcete-li změnit seznam polí, musíte nejprve aktualizovat šablonu.

6. Chcete-li zkontrolovat výběr polí, vyberte tabulku a poté na záložce **Řádky** vyberte Tlačítko **Pole**. Porovnejte a zkontrolujte počet polí, která jsou k dispozici s počtem polí, jejichž data byla použita.

Pokud výběr tabulek nevyhovuje vašim potřebám, můžete vytvořit jeden nebo více nových souborů migrace dat. Pokud jsou soubory dostatečné, můžete pokračovat v migraci dat pomocí souborů aplikace Excel nebo XML.

## Vytvoření souboru migrace dat
Můžete vytvořit nové soubory pro migraci dat a přizpůsobit je tak, aby podporovaly vaše podnikání. Všimněte si, že soubor lze použít pouze k migraci pole, které má svou vlastnost **FieldClass** nastavenou na **Normal**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační balíčky** a poté vyberte související odkaz.
2. Vyberte a otevřete balíček, který chcete použít k migraci dat, a poté vyberte akci **Získat tabulky**. Otevře se stránka **Získat tabulky**.
3. Do pole **ID tabulky** zadejte číslo tabulky nebo vyberte tabulku ze seznamu, například tabulka 18, **Zákazník**. Pole **Název tabulky** je automaticky vyplněno.
4. Vyberte novou migrační tabulku a poté v záložce **Tabulky** vyberte tlačítko **Pole**. Otevře se stránka **Pole konfiguračního balíčku**.
5. Zrušte zaškrtnutí políčka **Zahrnout pole** pro všechna pole, která nechcete importovat, a pak zvolte možnost zahrnout **Nastavit Zahrnuto** nebo **Vymazat Zahrnuto** .

> [!IMPORTANT]
Pokud je ve výchozím nastavení zaškrtnuto políčko **Zahrnout pole<x4 />, je toto pole součástí primárního klíče. Výběr by neměl být vymazán, nebo se objeví chyby a záznam nepůjde importovat.
Pokud zahrnete pole, které má vztah k jiné tabulce, je automaticky zaškrtnuto políčko **Ověřit pole**. Ověření může mít za následek aktualizaci dalších polí v této a dalších tabulkách a provádí se v pořadí podle čísla pole.

Je vytvořena nová migrační tabulka.

## Export souborů migrace dat
Po stanovení tabulek, do kterých chcete přenést data zákazníků, exportujte soubory.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační balíčky** a poté vyberte související odkaz.
2. Vyberte a otevřete balíček, který chcete použít pro export.
3. Vyberte tabulku nebo tabulky, které chcete exportovat, a pak vyberte tlačítko **Exportovat do aplikace Excel** .
4. Uložte exportovaný soubor aplikace Excel.
5. Opakujte tento postup pro všechny příslušné tabulky migrace dat. Pokud vyberete více tabulek současně, bude export jejich dat do společného sešitu.

Pokud je tabulka prázdná, výsledný soubor migrace dat obsahuje prázdné buňky pro pole, která jste vybrali při výběru nebo vytvoření migračních tabulek pro novou společnost. Pokud vybraná migrační tabulka dat obsahuje data, bude exportována.

## Mapování hodnot, které mají být použity během importu
When you apply data that you have imported from Excel or from a RapidStart package, [!INCLUDE[d365fin](includes/d365fin_md.md)] treats and handles the mapping based on table relations:

- If you define a mapping directly for a field in a table, then [!INCLUDE[d365fin](includes/d365fin_md.md)] uses it.

- If the field has a relation to another table, [!INCLUDE[d365fin](includes/d365fin_md.md)] searches for the mapping defined for the primary key field in the related table. The related table, however, must be part of the configuration package.

- If mapping information is defined in both places, for the field directly and for the primary key in the related table, then [!INCLUDE[d365fin](includes/d365fin_md.md)] will search for the mapping in both places.

- If the same mappings are defined directly for a field and in the related table, but have different new values, the mapping that is defined directly for the field takes priority over the mapping that is defined for the table that the field is referencing.

In the following procedures, you should review in advance which values you want to retain during the migration process. To perform the following procedures, you need data migration files (.xlsx) that you have exported from [!INCLUDE[d365fin](includes/d365fin_md.md)]. For more information, see [To export data migration files](admin-migrate-customer-data.md#to-export-data-migration-files).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační balíčky** a poté vyberte související odkaz.
2. Open the package for the company in question.
3. Select the table for which you want to map values, and then, on the **Tables** tab, choose the **Fields** action.
4. For each field that you want to map, choose the **Mapping** action.
5. In the **Old Value** field, enter the value that you want to change. In the **New Value** field, enter the value that you want the old value to be changed to. Choose the **OK** button.
6. Import the customer data. For more information, see [To import customer data](admin-migrate-customer-data.md#to-import-customer-data).
7. In the **No. of Package Errors** field, see if there are any errors reported. If there are, drill down to see the errors. The **Config. Package Records** page opens.
8. Choose the **Show Error** action. You will receive the following error: **XX is not a valid option. Valid options are: XX**. Choose the **OK** button.
9. To apply the mapping that you have set up, choose the **Apply Data** action.

### Mapping Example
The following example illustrates how [!INCLUDE[d365fin](includes/d365fin_md.md)] implements mapping definitions.

1. Create a configuration table that has a **Salesperson/Purchaser** table. Define a mapping for the **Code** field.
2. Add additional tables to the package, for example, **Customer** and **Vendor**. These tables both reference the **Salesperson/Purchaser** table through the **Salesperson Code** and **Purchaser Code** fields respectively.
3. When you apply data, the mapping that you provided for the **Code** field in the the **Salesperson/Purchaser** table will also be considered during the processing of the **Salesperson Code** and **Purchaser Code** fields.

## To add additional values to [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační balíčky** a poté vyberte související odkaz.
2. Select the table for which you want to add additional values, and then, on the **Tables** tab, choose the **Fields** action.
3. For the fields for which you want [!INCLUDE[d365fin](includes/d365fin_md.md)] to permit additional values during migration, select the **Create Missing Codes** check box.
4. Import the customer data. For more information, see [To import customer data](admin-migrate-customer-data.md#to-import-customer-data).

## To clean up and process data before applying data
In some cases, you may want to clean up customer data and process it before you apply it to the database. To do that, you can use the **Config. Package - Process** batch job to fix issues, such as:

- Convert dates and decimals to the format required by the regional settings on a user's computer.
- Remove leading/trailing spaces or special characters.

When you have run the batch job, use the following procedure to process the data.

1. Open the configuration package for the company.
2. Choose the **Process Data** action.
3. To apply the mapping that you have set up, choose the **Apply Data** action.

## To migrate customer data
When you have exported a migration table, your next step is to enter the customer’s legacy data. To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel. You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.

For assistance with XML, enable the **Developer** tab of the Excel ribbon, and then choose the **Source** action to see the XML schema of your migration table as represented in Excel.

The following procedure is based on an Excel worksheet that you have created for migration. For more information, see [To export data migration files](admin-migrate-customer-data.md#to-export-data-migration-files).

> [!IMPORTANT]
Do not change the columns in the Excel worksheets. If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. In Excel, open the exported data file. There is a worksheet with the name of the table.
2. Rename Sheet1 to indicate that the worksheet will be used to transform the data. Copy the header row without its formatting from the exported table to the new worksheet.
3. On a third worksheet, copy all your customer data. Rename the sheet to be called e.g. Legacy Data.
4. Make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.
5. When you have mapped all of the data, copy the range of data onto the table worksheet.
6. Save the file and make sure that you do not change the file type.

You are now ready to import the data migration files that contain customer legacy data into [!INCLUDE[d365fin](includes/d365fin_md.md)].

## To import customer data
When the customer data has been entered in the data migration files in Excel, you import the files into [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Open the **Config. Package Card** page.
2. Select the table for which you want to import data, and then, on the **Tables** tab, choose the **Import from Excel** action.
3. Locate and open the file that you want to import data from.
4. On the **Config. Package Import Preview** page, review the content that will be imported.

   The **Config. Package Import Preview** page provides an overview of the Excel file content to be imported. It also indicates if a new configuration package is created or the existing one is updated, and if new configuration package lines (tables) are created or existing ones are updated.
5. Choose the **Import** action

Data from the file is imported into the configuration package tables. In the **No. of Package Records** field, you can see the number of records that have been imported. In addition, you can see the number of migration errors.

## To validate customer data
Customer data must be validated before you apply the records to the [!INCLUDE[d365fin](includes/d365fin_md.md)] database.

> [!NOTE]
In most cases, invalid data is not created in the database. However, the application can occasionally be blocked if an imported migration table contains errors.

1. On the **Migration Overview** page, review the **No. of Migration Errors** field to see whether any errors occurred during import.
2. If there are errors, select the migration table, and then, on the **Tables** tab, choose the **Errors** action. The **Invalid** check box is selected for each record that has an error.
3. To review errors, select a line, and then choose the **Show Error** action.

   The **Error Text** field contains the reason for the error. The **Field Caption** field contains the caption of the field that contains the error.
4. To correct an error or otherwise make an update, on the **Migration Overview** page, choose the **Migration Record** action, and then, on the **Migration Record** page, correct the record with the error.

When you make a correction, the record is removed from the list of records on the **Migration Data Errors** page.

You are now ready to apply the customer’s data to the database.

## To apply customer data
When you have imported all data migration records that are valid and have no errors, you can apply the records to the [!INCLUDE[d365fin](includes/d365fin_md.md)] database.

1. Open the **Configuration Packages** page.
2. Select the table for the data migration file that you want to apply, and then choose the **Apply Data** action.

You can see the number of database records that have been created in the **No. of Database Records** field. You can verify that the correct records have been created by choosing the link in the **No. of Database Records** field.

The customer’s company database is now set up and basic data is imported. Your next steps in the implementation process are to train users, define processes, create additional data, customize reports, and so on.

## Viz také
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Administrace](admin-setup-and-administration.md)
