---
    title: How to Batch Post Consumption | Microsoft Docs
    description: If the flushing method is **Manual**, you must post the components manually, using a consumption journal.
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
# Dávkové účtování spotřeby
Pokud je metoda vyprázdnění nastavena na **Ruční**,  je nutné zaúčtovat komponenty ručně pomocí deníku spotřeby.

Můžete také nastavit systém tak, aby automaticky účtoval (*vyprazdňoval*) komponenty při spuštění nebo dokončení výrobních zakázek. Pro více informací navštivte [Povolit vyprázdnění komponent podle operace výstupu](production-how-to-flush-components-according-to-operation-output.md).

## Zaúčtování spotřeby pro jeden nebo více řádků výrobní zakázky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník spotřeby** a poté vyberte související odkaz.
2. Vyplňte pole údaji o výrobní zakázce a údaji o spotřebě. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   Pokud je umístění ve skladu, kde jsou komponenty uloženy, nastaveno na použití přihrádek, ale nevyžaduje zpracování vyskladnění, přiřaďte k řádku deníku kód přihrádky, který označuje, odkud má být zboží ve skladu odebráno. Pro více informací navštivte [Vyskladnění pro výrobu nebo montáž v základních konfiguracích skladu](warehouse-how-to-pick-for-production.md).
3. Vyberte akci **Účtovat** abyste zaúčtovali spotřebu. Související položky zboží jsou sníženy.

## Viz také
[Výroba](production-manage-manufacturing.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
