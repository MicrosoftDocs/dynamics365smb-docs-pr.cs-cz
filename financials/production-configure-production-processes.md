---
title: Konfigurace výrobních procesů | Microsoft Docs
description: 'Chcete-li převést materiál na vyráběné koncové zboží, musí být v systému nastaveny výrobní prostředky, jako jsou kusovníky, rutiny, obsluha strojů a stroje.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/04/2017
ms.author: sgroespe
---
# <a name="setting-up-manufacturing"></a>Nastavení výroby
Chcete-li převést materiál na vyráběné koncové zboží, musí být v systému nastaveny výrobní prostředky, jako jsou kusovníky, rutiny, obsluha strojů a stroje.

Operátoři a stroje jsou v systému zastoupeny jako strojní centra, která mohou být organizována v pracovních centrech a skupinách pracovních center. Když jsou tyto prostředky vytvořeny, mohou být načteny pomocí operací podle definované položky materiálu (kusovník) a struktury procesu (TNG) a podle kapacity stroje nebo pracovního centra.
 Můžete také nastavit výrobní kapacitu každého zdroje. Kapacita je definována pracovní dobou dostupnou ve stroji a pracovních centrech a řídí se kalendáři pro každou úroveň. Kalendář pracovního centra určuje pracovní dny a hodiny, směny, svátky a nepřítomnosti, které určují hrubou dostupnou kapacitu pracovního centra( typicky měřenou v minutách). To vše je určeno definovanými hodnotami účinnosti a kapacity.  

Když jste nastavili výrobu můžete plánovat a provádět výrobní zakázky. Další informace naleznete v [Plánování](production-planning.md) a [Výroba](production-manage-manufacturing.md)  

 Následující tabulka popisuje posloupnost úkolů s odkazy na témata, která je popisují.   

|**Viz**|**na**|  
|------------|-------------|  
|Nakonfigurujte výrobní funkce, jako je definování pracovní doby v dílně a výběr zásad plánování.|Stránka **Výrobní nastavení**.|  
|Definujte standardní pracovní týden ve výrobním oddělení z hlediska počátečních a konečných časů každého pracovního dne a související pracovní směny.|[Vytvářejte kalendáře dílny](production-how-to-create-work-center-calendars.md)|  
|Uspořádejte pevné hodnoty a požadavky na výrobní zdroje jako pracovní centra nebo strojní střediska k řízení jejich produkce prováděné výroby.|[Nastavení pracovních a strojových center](production-how-to-set-up-work-and-machine-centers.md)|
|Organizujte výrobní operace v požadovaném pořadí a přiřaďte je pracovním nebo strojním centrům s požadovanou pracovní dobou.|[Vytvoření postupů](production-how-to-create-routings.md)|
|Uspořádejte výrobní komponenty nebo podsestavy pod vyrobenou nadřazenou položku a certifikujte kusovník k provedení v pracovních střediscích.|[Vytvoření Výrobních kusovníků](production-how-to-create-production-boms.md)|
|Ujistěte se, že je k dispozici správné množství komponentů, pokud jsou vyráběné položky skladovány v jedné měrné jednotce, ale vyráběny jsou v jiné.|[Práce s výrobními dávkovými jednotkami míry](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|Definujte skupiny položek výroby s podobnými výrobními procesy, abyste ušetřili spotřebu. Například čtyři kusy té stejné položky mohou být vyrobeny z jednoho listu a 10 kusů jiné položky současně.|[Práce se skupinami výrobků](production-how-work-family.md)|
|Pomocí standardních úkolů můžete zjednodušit vytváření tras rychlým připojením dalších informací k opakujícím se operacím.|[Nastavit standardní směrovací linky](production-how-set-up-standard-routing-lines.md)|  
|Připravte pracovní střediska a rutiny, které budou představovat subdodavatelské výrobní operace.|[Výrobní subdodávky](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a>Viz také
[Výroba](production-manage-manufacturing.md)    
[Plánování](production-planning.md)   
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
