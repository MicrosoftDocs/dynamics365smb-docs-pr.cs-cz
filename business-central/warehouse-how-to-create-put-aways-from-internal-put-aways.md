---
    title: How to Create Put-aways from Internal Put-aways | Microsoft Docs
    description: After items have been put away and before they are picked to fulfill the needs of a production order or shipment, they are stored in the warehouse as part of available inventory.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Zaskladnění a vyskladnění bez zdrojového dokladu
Po zaskladnění zboží a před jejich vyskladněním za účelem splnění potřeb výrobní zakázky nebo dodávky je zboží uloženo ve skladu jako součást dostupných zásob.

Mohou nastat situace, kdy zboží musí být dočasně odebráno z přihrádek pro vyskladnění, například tehdy, kdy toto zboží slouží jako demonstrační modely v prodejní prezentaci. Toto zboží je stále ve vlastnictví společnosti a je součástí zásob, ale není k dispozici pro vyskladnění. Jsou zapsány v přihrádce pro zvláštní účely, kterou pro tento účel vytvoříte; technicky je zboží ve skladu, ale fyzicky může být v konferenční nebo demonstrační místnosti.

V jiných situacích může výrobní jednotka neočekávaně potřebovat několik dílů pro proces. Zboží pro výrobní přihrádky můžete vyskladnit pomocí interního vyskladnění. Po skončení procesu a vytvoření výstupu zaúčtujete spotřebu zboží a vyprázdníte výrobní přihrádku, což zase sníží množství zboží v lokaci.

Podobně může být zboží vráceno do skladu, aby bylo zaskladněné. Zboží může být také odebráno z dostupných zásob pro výrobní zakázku co znamená, že nebylo vůbec použito. Aby bylo opět součástí dostupných zásob, musí být toto zboží zaskladněno do přihrádky.

**Interní zaskladnění** umožňují provádět zaskladnění bez nutnosti odkazování se na konkrétní zdrojový doklad. Můžete snadno nastavit všechny informace, které potřebujete k vytvoření instrukce skladu zaskladnění.

> [!NOTE]
> Pokud nepoužíváte interní zaskladnění a vyskladnění, lze tyto úpravy provést pomocí metod pro přesun zboží z přihrádky do přihrádky nebo pomocí zaúčtování úprav množství v přihrádce.
> Pokud lokace používá řízené zaskladnění a vyskladnění, a proto používá typy přihrádek, nelze ručně přesunout zboží do nebo z přihrádky typu K PŘÍJMU, protože zboží, které je v přihrádce typu K PŘÍJMU, musí být registrováno jako zaskladnění, než je součástí dostupných zásob.
> 
## Vytvoření interního vyskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník  vyskladnění** a poté vyberte související odkaz.
2. Vyplňte pole **Číslo** a **Do kódu přihrádky** na záložce **Obecné**. Pole **Do kódu přihrádky** určuje přihrádku, ze které chcete zboží získat. Pro výrobní účely by tato přihrádka byla vstupní výrobní přihrádka nebo otevřená přihrádka dílny. Pro jiné účely zvolte typ přihrádky Do kódu přihrádky, který se nepoužívá pro vyskladnění, s největší pravděpodobností pracovní, expediční nebo speciální přihrádky.
3. Vyberte zboží v poli **Číslo zboží** a vyplňte množství, které chcete vyskladnit.
4. Vyberte akci **Vytvořit vyskladnění**. Instrukce vyskladnění je nyní připravena k provedení pro zaměstnance skladu.

## Vytvoření interního zaskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník  zaskladnění** a poté vyberte související odkaz.
2. Vyplňte pole **Číslo** a **Z kódu přihrádky** na záložce **Obecné**. Pole **Z kódu přihrádky** určuje přihrádku, ve které se nachází zboží vrácené do skladu, případně z výroby.
3. Vyplňte čísla zboží a množství na řádcích.
4. Vyberte akci **Vytvořit vyskladnění**. Instrukce pro zaskladnění do skladu je nyní připravena k provedení pro zaměstnance skladu.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
