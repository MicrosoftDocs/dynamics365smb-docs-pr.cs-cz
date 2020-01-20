---
title: Nastavení Karty lokace a definování Trasy transferu | Microsoft Docs
description: 'Pro každou lokaci, kam ukládáte skladové zboží, například sklad nebo centrum distribuce, vytvořte kartu umístění a nastavte trasy pro transfery zboží mezi lokacemi.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, distribution center'
ms.date: 01/25/2018
ms.author: SorenGP
---
# <a name="set-up-locations"></a>Nastavení Lokací
Pokud kupujete, skladujete nebo prodáváte zboží na více než jednom místě nebo skladu, musíte nastavit každou lokaci pomocí karty lokace a definovat trasy transferu.

Poté můžete vytvořit řádky dokladů pro konkrétní lokaci, zobrazit dostupnost podle lokace a převést zásoby mezi lokacemi. Pro více informací navštivte [Správa skladu](inventory-manage-inventory.md).

## <a name="to-create-a-location-card"></a>Vytvoření Karty lokace
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Lokace** a pak vyberte související odkaz.
2. Zvolte akci **Nový**.
3. V okně **Karta lokace** vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Opakujte kroky 2 a 3 pro každou lokaci, kde chcete vést inventář zásob.

> [!NOTE]  
> Mnoho polí na kartě lokace odkazuje na manipulaci se zbožím v procesech vstupního a výstupního skladu. Pro více informací navštivte [Nastavení správy skladu](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>Vytvoření trasy transferu
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Trasy transferu** a pak vyberte související odkaz.
2. Případně z jakéhokoli okna **Karty lokace** vyberte akci **Trasy transferu**.
3. Zvolte akci **Nový**.
4. V okně **Karta lokace** vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nyní můžete přenášet skladové zboží mezi dvěma lokacemi. Pro více informací navštivte [Převádění zásob mezi lokacemi](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Viz také
[Správa zásob](inventory-manage-inventory.md)  
[Převádění zásob mezi lokacemi](inventory-how-transfer-between-locations.md)    
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)
