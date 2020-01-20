---
title: Jak nastavit přepravce | Microsoft Docs
description: Můžete nastavit kód pro každého z vašich přepravců a zadat o nich informace.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/23/2017
ms.author: sgroespe
---
# <a name="set-up-shipping-agents"></a>Nastavení přepravců
Můžete nastavit kód pro každého z vašich přepravců a zadat o nich informace.  

Pokud pro přepravce zadáte internetovou adresu a přepravce poskytuje služby sledování zásilek na internetu, můžete použít funkci automatického sledování zásilek. Pro více informací navštivte [Sledování balíčků](sales-how-track-packages.md).

Při nastavování přepravců na prodejních objednávkách můžete také určit služby, které každý přepravce nabízí.  
Pro každého přepravce můžete nastavit neomezený počet služeb a pro každou službu můžete zadat dobu dodávky.  

Po přiřazení služby přepravce k řádku prodejní objednávky bude doba dodávky služby zahrnuta do výpočtu příslibu vyřízení objednávky pro tento řádek. Pro více informací navštivte [Výpočet data přislíbení objednávky](sales-how-to-calculate-order-promising-dates.md).

## <a name="to-set-up-a-shipping-agent"></a>Nastavení přepravce  
1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Přepravci** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  
3. Vyberte akci **Služby přepravce**.
4. V **Služby přepravce**, vyplňte pole podle potřeby.

> [!NOTE]  
>  Pokud na řádku objednávky odstraníte přepravce, odstraní se také kód služby přepravce. Obsah polí, která byla částečně založena na službě přepravce, se přepočítá.  

## <a name="see-also"></a>Viz také
[Sledování balíčků](sales-how-track-packages.md)    
[Správa skladů](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)     
[Správa montáže](assembly-assemble-items.md)    
[Podrobnosti návrhu: Správa skladů](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
