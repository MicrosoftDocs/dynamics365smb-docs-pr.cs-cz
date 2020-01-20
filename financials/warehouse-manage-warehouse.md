---
title: Skladové aktivity | Microsoft Docs
description: 'Po přijetí zboží a před odesláním zboží probíhá řada interních činností skladu, aby byl zajištěn efektivní tok zboží přes sklad a aby byla organizována a udržována inventura společnosti.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/15/2017
ms.author: sgroespe
---
# <a name="warehouse-management"></a>Správa skladů
Po přijetí zboží a před odesláním zboží probíhá řada interních činností skladu, aby byl zajištěn efektivní tok zboží přes sklad a aby byla organizována a udržována inventura společnosti.

Typické skladové aktivity zahrnují zaskladnění zboží, přesouvání zboží uvnitř nebo mezi sklady a vyskladnění zboží pro montáž, výrobu nebo dodávku. Montáž zboží za účelem prodeje nebo inventarizace lze rovněž považovat za aktivity skladu, ale tyto položky jsou zahrnuty jinde. Pro více informací navštivte [Správa montáže](assembly-assemble-items.md).  

Ve velkých skladech lze tyto různé úlohy zpracování oddělit podle oddělení a integrace spravované řízeným pracovním postupem. V jednodušších instalacích je tok méně formální a aktivity skladu jsou prováděny pomocí takzvaných zaskladnění zásob a vyskladnění zásob. Další informace o základních a pokročilých konfiguracích skladu najdete v [Podrobnosti návrhu: Přehled skladů](design-details-warehouse-overview.md).

Před provedením aktivit skladu je nutné nastavit systém pro příslušnou složitost zpracování ve skladu. Pro více informací navštivte [Nastavení správy skladu](warehouse-setup-warehouse.md).

 Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.   

|**Viz**|**také**|  
|------------|-------------|  
|Zaznamenání příjmu zboží do skladových lokací, a to buď pouze s nákupní objednávkou, v jednoduchém nastavení skladů nebo s příjmem na sklad v případě polonebo plně automatizovaného zpracování skladu v lokaci.|[Příjem zboží](warehouse-how-receive-items.md)|
|Vynechání procesů zaskladnění a vyskladnění za účelem urychlení  příjmu zboží  přímo z objednávky nebo z výroby do expedice|[Položky přeložení](warehouse-how-to-cross-dock-items.md)|    
|Zaskladnění zboží přijatého z nákupů, prodejních vratek, transferů nebo výstupu výroby podle nakonfigurovaného procesu skladu|[Zaskladnění zboží](warehouse-put-away-items.md)|
|Přesun zboží mezi přihrádkami ve skladu|[Přesouvání zboží](warehouse-move-items.md)|
|Vyskladnění zboží, které má být dodáno, převedeno nebo spotřebováno v montáži nebo výrobě, podle konfigurovaného procesu skladu|[Vyskladnění zboží](warehouse-pick-items.md)|
|Poznamenejte si dodávku zboží ze skladových lokací, a to buď pouze s prodejní objednávkou, v jednoduchém nastavení skladu, nebo s dodávkou ze skladu, v případě polotovarů nebo plně automatizovaných skladových procesů v lokaci.|[Odeslání položek](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Viz také  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladů](warehouse-setup-warehouse.md)     
[Správa montáže](assembly-assemble-items.md)    
[Podporbnosti návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s[!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE [d365fin](includes/free_trial_md.md)]  
## [!INCLUDE [d365fin](includes/training_link_md.md)]
