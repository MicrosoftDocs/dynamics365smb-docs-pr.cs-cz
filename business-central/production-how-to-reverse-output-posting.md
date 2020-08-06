---
    title: How to Reverse Output Posting | Microsoft Docs
    description: There are times when output posting must be reversed. An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.
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
# Stornování účtování výstupu
Jsou chvíle, kdy musí být zaúčtování výstupu stornováno. Příkladem toho by bylo, kdyby došlo k chybě zadávání dat a nesprávné množství výstupu by bylo zaúčtováno do výrobní zakázky.

## Stornování účtování výstupu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník výstupu** a poté vyberte související odkaz. Vyberte dávku.
2. Podle potřeby vyplňte pole. Pro více informací navštivte [Dávkové zaúčtování výstupu a spuštění](production-how-to-post-output-quantity.md).
3. V poli **Vyrovnává položku** vyberte přidruženou položku zboží. Tím se stornuje kapacita a položky zboží.
4. Zaúčtujte stornování zaúčtováním deníku.

Výstupy deníku jsou zaúčtovány do účetní knihy jako pozitivní úprava.

## Viz také
[Výroba](production-manage-manufacturing.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
