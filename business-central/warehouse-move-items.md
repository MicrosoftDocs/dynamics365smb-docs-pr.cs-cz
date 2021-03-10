---
    title: Move Items | Microsoft Docs
    description: While in inventory, items may need to be moved between bins to support the daily warehouse activities involved in keeping items flowing through the warehouse. Some movements happen in direct relation to internal operations, such as a production order that needs components delivered or end items put away. Other movements happen as mere warehouse space optimization or as ad-hoc movements to and from operations.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Přesouvání zboží
Skladová aktivita přesouvání zboží ve skladu se provádí různými způsoby v závislosti na tom, jak jsou nakonfigurovány funkce správy skladu. Složitost se může řadit od žádných funkcí skladu, přes základní konfigurace skladu pro zpracování objednávek pouze v jedné nebo více aktivitách, až po pokročilé konfigurace, kde všechny aktivity skladu musí být prováděny v směrovaném workflow. Pro více informací navštivte [Nastavení správy skladu](warehouse-setup-warehouse.md).

V jedné lokaci skladu může být nutné zboží přesouvat mezi přihrádky, aby se podpořily denní aktivity skladu spojené s udržováním zboží procházejících skladem. Některé přesuny se uskutecují v přímém vztahu k interním operacím, například výrobní zakázka, která vyžaduje dodání komponent nebo zaskladnění koncového zboží. K dalším přesunům dochází jako pouhá optimalizace skladových prostor nebo jako ad hoc přesuny do a z operací.

Další úkoly přesunu jsou pravidelné doplňování výdejní přihrádky nebo přihrádek dílny a úprava informací o obsahu přihrádky.

Přesunutí zboží do jiných lokací ovlivní položky zboží, a proto musí být provedeno objednávkou transferu. Pro více informací navštivte [Převádění zásob mezi lokacemi](inventory-how-transfer-between-locations.md).

Úkoly inventury, úpravy a přeřazení zboží související se skladem mohou zahrnovat skladové úkoly, které musí být provedeny u položek skladu před jejich synchronizací se souvisejícími položkami zboží. Pro více informací navštivte [Výpočet, úprava a překlasifikace zásob pomocí deníků](inventory-how-count-adjust-reclassify.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| **Viz** | **také** |
|------------|-------------|  
| Přesouvaní zboží mezi přihrádkami v základních konfiguracích skladu kdykoli a bez původních dokladů. | [Přesun zboží v základních konfiguracích skladu](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md) |
| Sešit přesunu skladu se používá k přesunu zboží v pokročilých konfiguracích skladu, a to jak pro původní doklady, tak pro Ad Hoc. | [Přesun zboží v pokročilých konfiguracích skladu](warehouse-how-to-move-items-in-advanced-warehousing.md) |
| Přineste komponenty zboží do interních operací v základních konfiguracích skladu, jak je požadováno původním dokladem pro tyto operace. | [Přesuňte komponenty do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) |
| Naplánujte, které přihrádky se mají naplnit nebo vyprázdnit, aby se zachoval efektivní tok, například vyprázdnění velkokapacitního skladovacího prostoru před velkým příjmem. | [Naplánujte pohyby skladu v sešitech](warehouse-how-to-plan-warehouse-movements-in-worksheets.md) |
| Aktualizujte frekvenci, s jakou musí být přihrádky, například přihrádky vyskladnění, doplněny v důsledku kolísání poptávky. | [Výpočet doplnění přihrádky](warehouse-how-to-calculate-bin-replenishment.md) |
| Restrukturalizujte svůj sklad pomocí nových kódů přihrádek a nových charakteristik přihrádky a případně je přesuňte. | [Restrukturalizace skladů](warehouse-how-to-restructure-warehouses.md) |

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)    
[Zásoby](inventory-manage-inventory.md)    
[Nastavení správy skladu](warehouse-setup-warehouse.md)       
[Správa montáže](assembly-assemble-items.md)      
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]