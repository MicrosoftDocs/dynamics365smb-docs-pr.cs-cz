---
title: Konfigurace skladových procesů | Microsoft Docs
description: 'Distribuční strategie společnosti se odráží v konfiguraci jejích skladových procesů. To zahrnuje definování způsobu nakládání s různými položkami na různých místech skladu, jako je například stupeň kontroly přihrádek a rozsah workflow vyžadovaného mezi operacemi skladu.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/04/2018
ms.author: sgroespe
---
# <a name="setting-up-warehouse-management"></a>Nastavení správy skladu
Distribuční strategie společnosti se odráží v konfiguraci jejích skladových procesů. To zahrnuje definování způsobu nakládání s různými položkami na různých místech skladu, jako je například stupeň kontroly přihrádek a rozsah workflow vyžadovaného mezi operacemi skladu.  

 Následující tabulka popisuje sekvenci úloh s odkazy na témata, která je popisují.   

|**Viz**|**Také**|  
|------------|-------------|  
|Získejte přehled o možnostech základních a pokročilých funkcí skladu.|[Podrobnosti návrhu: Přehled skladů](design-details-warehouse-overview.md)|  
|Nastavte osm různých typů přihrádek, například Vyskladňovací přihrádka, pro definování činností, které se vztahují ke každému typu přihrádky.|[Nastavení typu přihrádky](warehouse-how-to-set-up-bin-types.md)|  
|Vytvářejte přihrádky, buď ručně nebo automaticky s informacemi, jako je název, číselná řada a kategorie podle šablony přihrádky.|[Vytváření přihrádky](warehouse-how-to-create-individual-bins.md)|  
|Definujte, které zboží chcete uložit do libovolné přihrádky a nastavte pravidla, která rozhodují, kdy se přihrádka naplní konkrétním zbožím.|[Vytvoření obsahu přihrádky](warehouse-how-to-set-up-bin-contents.md)|  
|Nastavte zboží tak, aby byla vždy umístěna do určité přihrádky.|[Přiřazení výchozí přihrádky ke zboží](warehouse-how-to-assign-default-bins-to-items.md)|
|Vytvořte šablony, které určují, kde a jak je zboží umístěno během řízeného zaskladnění.|[Nastavení šablon zaskladnění](warehouse-how-to-set-up-put-away-templates.md)|
|Nastavte uživatele jako zaměstnance skladu na konkrétních lokacích.|[Nastavení zaměstnanců skladu](warehouse-how-to-set-up-warehouse-employees.md)|
|Definujte různé typy přihrádek ve skladu a určete, kde je zboží umístěno podle jeho typu, pořadí nebo úrovně manipulace.|[Nastavení lokací pro použití přihrádek](warehouse-how-to-set-up-locations-to-use-bins.md)|
|U stávající lokace proveďte další nastavení, abyste ji mohli povolit pro činnosti skladu.|[Převod existující lokace do lokací skladu](warehouse-how-to-convert-existing-locations-to-warehouse-locations.md)|
|Umožněte vyskladnění, přesun a zaskladnění montážních nebo výrobních objednávek v základních konfiguracích skladu.|[Nastavení základních lokací s provozními oblastmi](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|  
|Nastavuje zboží a lokaci pro nejpokročilejší rozsah správy skladu, kde všechny činnosti musí následovat přesný pracovní postup.|[Nastavení zboží a lokace pro přímé zaskladnění a vyskladnění](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md)|  
|Definuje, kdy a jak je zboží ve skladu počítáno pro účely údržby nebo finančního výkaznictví.|[Výpočet, adjustace a reklasifikace skladu](inventory-how-count-adjust-reclassify.md)|
|Umožněte pracovníkům skladu rozdělit větší měrnou jednotku na menší měrné jednotky, aby splnili potřeby zdrojových dokumentů.|[Povolení automatického rozedělení zboží s řízeným zaskladněním a vyskladněním](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md)|  
|Nastavte sklad tak, aby automaticky navrhoval zboží, které má být vybráno a jehož trvanlivost exspiruje jako první.|[Povolení vyskladnění pomocí FEFO](warehouse-picking-by-fefo.md)|
|Získejte tipy, jak reorganizovat lokace, přihrádky nebo zóny, abyste získali efektivnější skladové činnosti.|[Restrukturalizace skladů](warehouse-how-to-restructure-warehouses.md)|
|Integrace čtečky čárových kódů do řešení správy skladu. Pouze pro on-premise řešení.|[Používejte automatizované systémy pro sběr dat (ADCS)](warehouse-use-automated-data-capture-systems-adcs.md)|

## <a name="see-also"></a>Viz také  
[Správa skladů](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Správa montáže](assembly-assemble-items.md)    
[Podrobnosti návrhu: Správa skladů](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
