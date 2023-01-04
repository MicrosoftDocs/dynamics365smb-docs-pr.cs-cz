---
title: Manage Warehouse Activities
description: After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse.
author: SorenGP


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5774, 5776, 5777, 5785, 5793, 5797, 7318, 7364, 7401, 8909, 9000, 9008, 9009, 9050, 9053, 9056
ms.date: 06/25/2021
ms.author: edupont

---
# Správa skladu

Po přijetí zboží a před jeho odesláním probíhá řada interních skladových činností, jejichž cílem je zajistit efektivní tok ve skladu a organizovat a udržovat zásoby společnosti.

Typické skladové činnosti zahrnují zaskladnění zboží, přesuny zboží uvnitř skladu nebo mezi sklady a vychystávání zboží pro montáž, výrobu nebo expedici. Montáž zboží k prodeji nebo inventarizace může být také považována za skladovou činnost, ale ty jsou zahrnuty jinde. Pro více informací navštivte [Správa montáže](assembly-assemble-items.md).

Ve velkých skladech lze tyto různé manipulační úkoly oddělit podle oddělení a integraci řídit pomocí řízeného pracovního postupu. V jednodušších zařízeních je tok méně formalizovaný a skladové činnosti se provádějí pomocí tzv. vyskladňování a zaskladňování zboží. Další informace o základních a pokročilých konfiguracích skladu naleznete v části [Detaily návrhu: Přehled skladu](design-details-warehouse-overview.md).

Než budete moci provádět činnosti skladu, musíte nastavit systém pro příslušnou složitost zpracování skladu. Pro více informací navštivte [Nastavení správy skladu](warehouse-setup-warehouse.md).

Úkoly inventury, úpravy a přeřazení zboží související se skladem mohou zahrnovat skladové úkoly, které musí být provedeny u položek skladu před jejich synchronizací se souvisejícími položkami zboží. Pro více informací navštivte [Výpočet, úprava a přeřazení zásob](inventory-how-count-adjust-reclassify.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| **Viz** | **také** |
|------------|-------------|  
| Evidence příjmu (včetně převzetí) zboží na lokacích, a to buď pouze pomocí nákupního příkazu v případě jednoduchého nastavení skladu, nebo pomocí skladové příjemky v případě poloautomatizovaného nebo plně automatizovaného skladového zpracování na místě. | [Příjem zboží](warehouse-how-receive-items.md) |
| Obejití procesů vyskladnění a zaskladnění, abyste urychlili položku přímo z příjmu nebo výroby do expedice. | [Přeožení zboží](warehouse-how-to-cross-dock-items.md) |
| Zaskladnění zboží z nákupů, vrácených prodejů, převodů nebo výstupů z výroby podle nakonfigurovaného skladového procesu. | [Zaskladnění zboží](warehouse-put-away-items.md) |
| Přesouvání zboží mezi přihrádkami | [Přesouvání zboží](warehouse-move-items.md) |
| Vychystávání položek, které mají být odeslány, přeneseny nebo spotřebovány při montáži či výrobě, podle nakonfigurovaného skladového procesu. | [Vyskladňování zboží](warehouse-pick-items.md) |
| Evidence expedice zboží ze skladových míst, a to buď pouze s prodejní objednávkou v případě jednoduchého nastavení skladu, nebo se skladovou dodávkou v případě poloautomatizovaných nebo plně automatizovaných skladových procesů na místě. | [Dodání zboží](warehouse-how-ship-items.md) |

## Viz také

[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]