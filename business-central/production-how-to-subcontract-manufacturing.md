---
    title: How to Subcontract Manufacturing | Microsoft Docs
    description: When the purchase order has been created from the subcontractor worksheet, then it can be posted.
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
# Subdodavatelská výroba
V mnoha výrobních společnostech je subdodavatelská výroba dodavateli běžná. Subdodávky mohou být vzácným jevem nebo mohou být nedílnou součástí všech výrobních procesů.

Aplikace poskytuje několik nástrojů pro správu subdodávek:

- Pracovní centra s přiřazeným dodavatelem: Tato funkce umožňuje nastavit pracovní centrum, které je spojeno s dodavatelem (subdodavatelem). Toto centrum se nazývá subdodavateléské pracovní středisko. Můžete zadat subdodavatelské pracovní středisko při TNG operaci, což vám umožní snadno zpracovat subdodavatelskou činnost. Kromě toho mohou být náklady na operaci určeny na úrovni TNG postupu nebo pracovního centra.
- Náklady pracovního centra na základě jednotek nebo času: Tato funkce umožňuje určit, zda jsou náklady spojené s pracovním střediskem založeny na době výroby nebo na paušálním poplatku za jednotku. Přestože subdodavatelé běžně používají k účtování svých služeb paušální poplatek za jednotku, program zvládne obě možnosti (výrobní čas i paušální poplatek za jednotku).
- Sešity subdodavatelů: Tato funkce vám umožní najít výrobní zakázky s materiálem připraveným k odeslání subdodavateli a automaticky vytvořit objednávky pro subdodavatelské operace z výrobních zakázek. Program pak automaticky zaúčtuje náklady nákupní objednávky do výrobní zakázky během zaúčtování nákupní objednávky. Do sešitu subdodavatelů lze přistupovat a používat pouze výrobní zakázky se stavem Vydaná.

## Subdodavatelská pracovní centra
Subdodavatelská pracovní centra jsou zřízena stejně jako běžná pracovní centra s dalšími informacemi. Jsou přiřazeny k TNG postupům stejným způsobem jako ostatní pracovní centra.

### Pole subdodavatelských pracovních středisek
Pole **Číslo subdodavatele** označuje pracovní středisko jako pracovní centrum subdodavatele. Můžete zadat číslo subdodavatele, který zásobuje pracovní centrum. Toto pole lze použít ke správě pracovních středisek, která nejsou interní, ale provádějí zpracování na základě smlouvy.

Pokud zadáte subdodavateli s dodavatelem jinou sazbu pro každý proces, vyberte pole **Zadaná pořizovací cena**. To vám umožní nastavit náklady na každém řádku technologického postupu a ušetřit čas pro opětovné zadávání jednotlivých nákupních objednávek. Náklady na řádku TNG postupu se používají při zpracování místo nákladů na pole nákladů pracovního centra. Výběr pole **Zadaná pořizovací cena** vypočítá náklady na dodavatele pomocí TNG postupu.

Pokud zadáváte subdodávky za jednu cenu na dodavatele, ponechte pole **Zadaná pořizovací cena** prázdné. Náklady budou nastaveny vyplněním pole **Nákupní cena** , **Nepřímé náklady %** a **Režijní náklady** .

### TNG postupy, které používají Subdodavatelská pracovní centra
Pracovní centra subdodávek lze použít pro operace v TNG postupech stejným způsobem jako běžná pracovní centra.

Můžete nastavit TNG postup, který používá externí pracovní středisko jako standardní operační krok. Alternativně můžete upravit TNG postup určité výrobní zakázky tak, aby zahrnoval vnější operaci. To může být nutné v případě nouze, jako je například server, který nepracuje správně, nebo během přechodného období vyšší poptávky, kde musí být práce, která je obvykle prováděna interně, zaslána subdodavateli.

Pro více informací navštivte [Vytvoření TNG postupů](production-how-to-create-routings.md).

## Výpočet sešitů subdodavatelů a vytvoření nákupních objednávek subdodávek
Po výpočtu sešitu subdodavatelů se vytvoří příslušný doklad, v tomto případě nákupní objednávka.

Funkce stránky **Sešit subdodavatelů** funguje podobně jako **Plánovací sešit** výpočtem potřebného zásobování, v tomto případě nákupních objednávek, které si v sešitě revidujete a pak vytvoříte pomocí funkce **Provést hlášené akce** .

> [!NOTE]
> K výrobním zakázkám se stavem **Vydané** lze získat přístup a použít je z sešitu subdodavatelů listu.

### Výpočet sešitu subdodavatelů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešity subdodavatelů** a poté vyberte související odkaz.
2. Chcete-li vypočítat sešit, zvolte talčítko **Výpočítat subdodávky** .
3. Na stránce **Vypočítat subdodávky** nastavte filtry pro subdodavatelské operace nebo pracovní centra, kde jsou prováděny, aby se vypočítaly pouze příslušné výrobní zakázky.
4. Klikněte na tlačítko **OK**.

   Prohlédněte si řádky na stránce **Sešity subdodavatelů** . Informace v tomto sešitě pocházejí z výrobní zakázky a řádků TNG postupu výrobní zakázky a načíta se do nákupní objednávky při vytvoření tohoto dokladu. Řádek můžete odstranit zesešitu bez ovlivnění původních informací, stejně jako u ostatních sešitů. Informace se znovu objeví při příštím spuštění funkce **Vypočítat subdodávky<x4 />.

### Vytvoření nákupní objednávky subdodávky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešity subdodavatelů** a poté vyberte související odkaz.
2. Na kartě **Akce** ve skupině **Proces** vyberte tlačítko **Provést hlášené akce..**.
3. Vyberte pole **Tisk Objednávek**k vytištění nákupní objednávky po jejím vytvoření.
4. Klikněte na tlačítko **OK**.

Pokud jsou všechny subdodavatelské operace odeslány do stejné lokace dodavatele, je vytvořena pouze jedna objednávka.

Řádek sešitu, který byl převeden na objednávku, je z listu odstraněn. Jakmile je nákupní objednávka vytvořena, již se v sešitě neobjeví.

## Účtování nákupních objednávek subdodávek
Jakmile byly vytvořeny nákupní objednávky subdodavatele, lze je zaúčtovat. Přijetí objednávky zaúčtuje záznam výrobní kapacity do výrobní zakázky a fakturace objednávky zaúčtuje přímé náklady na objednávku do výrobní zakázky.

Když je nákup zaúčtován tak, jak byl přijat, je výstupní položka deníku automaticky zaúčtována pro výrobní zakázku. Toto platí pouze v případě, že operace subdodávek je poslední operací na TNG postupu výrobní zakázky.

> [!CAUTION]
> Zaúčtování výstupu automaticky pro probíhající výrobní zakázku při přijetí subdodávek nemusí být žádoucí. Důvodem může být, že očekávané výstupní množství, které je zaúčtováno, může být odlišné od skutečného množství a že zúčtovací datum automatického výstupu je zavádějící.
> Aby se předešlo tomu, že očekávaný výstup výrobní zakázky bude zaúčtován při přijetí subdodavatelských nákupů, ujistěte se, že operace subdodavatele není poslední. Alternativně vložte novou poslední operaci pro konečné výstupní množství.
> 
## Zaúčtování nákupní objednávky subdodávek
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.
2. Otevřete nákupní objednávku vytvořenou ze sešitu subdodavatelů.

   Na řádcích objednávek se zobrazují stejné informace jako v sešitu. **Číslo  montážní zakázky**, **Číslo  řádku výrobní zakázky**, **Číslo operace** a pole **Číslo pracovního centra** jsou vyplněna údaji ze zdrojové výrobní zakázky.

3. Vyberte tlačítko **Účtovat**.

Když je nákup zaúčtován tak, jak byl přijat, je výstupní položka deníku automaticky zaúčtována pro výrobní zakázku. Toto platí pouze v případě, že operace subdodávek je poslední operací na TNG postupu výrobní zakázky.

> [!CAUTION]
Není možné požadovat automatické účtování výstupu pro probíhající výrobní zakázku při přijetí subdodávek. Důvodem může být, že očekávané výstupní množství, které je zaúčtováno, může být odlišné od skutečného množství a že zúčtovací datum automatického výstupu je zavádějící.
Aby se předešlo tomu, že očekávaný výstup výrobní zakázky bude zaúčtován při přijetí subdodavatelských nákupů, ujistěte se, že operace subdodavatele není poslední. Alternativně vložte novou poslední operaci pro konečné výstupní množství.

Když je nákupní objednávka zaúčtována jako fakturovaná, jsou přímé náklady nákupní objednávky zaúčtovány do výroby.

## Viz také
[Výroba](production-manage-manufacturing.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
