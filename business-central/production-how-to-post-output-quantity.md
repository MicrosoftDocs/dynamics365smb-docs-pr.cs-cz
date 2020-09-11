---
    title: How to Batch Post Production Output and Run Times| Microsoft Docs
    description: The output quantity represents the work progress in the form of the finished quantity.
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
# Dávkové zaúčtování výstupu a spuštění
Množství výstupu představuje průběh práce ve formě dokončeného množství.

> [!NOTE]
> Pouze v případě, že v poslední operaci zaúčtujete množství výstupu, jsou zásoby automaticky aktualizovány.

## Zaúčtování množství výstupu pro jeden nebo více řádků výrobní zakázky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník výstupu** a poté vyberte související odkaz.
2. Vyplňte pole údaji výrobní zakázky a výstupními daty. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pokud byla operace dokončena, vyberte pole **Dokončeno**.

   Pokud lokace skladu, kde má být zboží zaskladněné, používá přihrádky, ale nevyžaduje zpracování zaskladnění, přiřaďte k řádku deníku kód přihrádky a určete, kam má být zboží umístěno. Pro více informací navštivte [Zaskladnění výroby nebo výstupu montáže](warehouse-how-to-put-away-production-output.md).

4. Zvolte akci **Účtovat** pro zaúčtování operace. Množství výstupu bude zaúčtováno. Zboží je nyní k dispozici pro expedici.

## Zaúčtování časů spuštění pro jeden nebo více řádků výrobní zakázky
Doba běhu představuje průběh práce ve formě potřebné pracovní doby.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník výstupu** a poté vyberte související odkaz.
2. Vyplňte pole údaji výrobní zakázky a výstupními daty.
3. Po dokončení operace vyberte pole **Dokončeno**.
4. Vyberte akci **Účtovat**, chcete-li zaúčtovat čas strávený na operaci. Položky kapacity jsou aktualizovány pro použitá pracovní nebo strojní centra.

## Viz také
[Výroba](production-manage-manufacturing.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
