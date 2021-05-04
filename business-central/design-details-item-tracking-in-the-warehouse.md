---
    title: Design Details - Item Tracking in the Warehouse | Microsoft Docs
    description: Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers. However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Sledování zboží ve skladu
Zpracování sériových čísel a čísel šarží je především úlohou skladu a proto mají všechny vstupní a výstupní skladové doklady standardní funkce pro přiřazování a výběr čísel sledování zboží.

Protože je však rezervační systém založen na položkách zboží, doklady aktivit skladu, které evidují pouze položky skladu, nejsou plně podporovány. Vzhledem k tomu, že rezervace a čísla sledování zboží lze zpracovat pouze na úrovni lokace, nikoli na úrovni přihrádky a zóny, nelze stránku **Řádky sledování zboží** otevřít z dokladů aktivit skladu. Totéž platí pro stránku **Rezervace**

Poté, co bylo ke zboží ve skladu přidáno sériové číslo nebo číslo šarže, lze ji volně přesunout a přeradit ve skladu pomocí nezávislé struktury sledování položky, která nesouvisí s rezervačním systémem. **Sériové číslo** a **Číslo šarže.** jsou přístupná přímo na řádcích dokladu skladu. Když je sériové číslo nebo číslo šarže později účtováno, je synchronizováno s rezervačním systémem jako součást běžné úpravy přihrádky Pro více informací navštivte [Detaily návrhu: Integrace se zásobami](design-details-integration-with-inventory.md).

Rezervační systém však při výpočtu dostupnosti bere v úvahu aktivity skladu. Například zboží, které je přiděleno vyskladnění nebo zapsané, tedy vyskladněné, nelze rezervovat. Pro více informací navštivte  [Detaily návrhu: Dostupnost skladu](design-details-availability-in-the-warehouse.md).

## Viz také
[Detaily návrhu: Sledování zboží](design-details-item-tracking.md)  
[Detaily návrhu: Integrace se zásobami](design-details-integration-with-inventory.md)  
[Detaily návrhu: Dostupnost skladu](design-details-availability-in-the-warehouse.md)  
[Detaily návrhu: Design sledování zboží](design-details-item-tracking-design.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]