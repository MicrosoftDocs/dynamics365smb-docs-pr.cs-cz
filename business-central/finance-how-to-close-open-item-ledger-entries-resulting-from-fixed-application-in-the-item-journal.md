---
    title: How to Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal | Microsoft Docs
    description: You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction. For example, to correct the outbound transaction or to process its return.
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
# Uzavření otevřených položek zboží, které vyplývají z pevného vyrovnání z deníku zboží
Pomocí pole **Vyrovnává položku** na stránce **Deník zboží** můžete vytvořit pevné vyrovnání mezi příchozí transakcí a původní odchozí transakcí. Například k opravě odchozí transakce nebo ke zpracování jejího vrácení. Pro více informací navštivte Vyrovnání položky.

> [!IMPORTANT]
> Pevné vyrovnání vytvořené tímto způsobem používá pouze náklady, nikoli množství. V souladu s tím zaúčtovaná kladná položka zboží nezavře vyrovnávanou odchozí položku a sama zůstane otevřená. To platí i v případě, že zaúčtujete pevné vyrovnání o kladnou položku, která nebyla uzavřena pomocí pravidelné kladné položky, pak záporné i kladné položky zůstanou otevřené.
> To také znamená, že období zásob nelze uzavřít, pokud taková položka existuje.
> 
Následující postup ukazuje, jak uzavřít tyto položky provedením dvou opravných účtování v deníku zboží.

## Zavření otevřených položek zboží, které jsou výsledkem pevného vyrovnání v deníku zboží

1. Pomocí pole **Vyrovnává položku** zaúčtujte kladnou úpravu s odpovídajícím množstvím. Tím se uzavře původní záporná položka pevného vyrovnání.
2. Pomocí pole **Vyrovnává položku** odešlete zápornou úpravu. Tím se uzavře původní opravná pozitivní položka s pevným vyrovnáním.

## Viz také
[Odebrat a znovu vyrovnat položky zboží](finance-how-to-remove-and-reapply-item-entries.md)  
[Zpracování prodejní vratky nebo stornování](sales-how-process-sales-returns-cancellations.md)  
[Nastavení oceňování zásob a nákladů](finance-set-up-inventory-valuation-and-costing.md)  
[Správa nákladů zásob](finance-manage-inventory-costs.md)  
[Detaily návrhu: Metody ocenění](design-details-costing-methods.md)
