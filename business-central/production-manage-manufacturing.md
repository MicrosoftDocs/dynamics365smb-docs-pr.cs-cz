---
title: Provádění výroby | Microsoft Docs
description: 'Pokud je poptávka plánována a materiál byl vydán podle výrobních kusovníků, mohou být skutečné výrobní operace spouštěny a spouštěny v pořadí definovaném v TNG postupu výrobní zakázky.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/15/2018
ms.author: sgroespe
---
# <a name="manufacturing"></a>Výroba
> [!NOTE]
> Funkce popsané v tomto tématu a dílčích tématech jsou viditelné pouze v uživatelském rozhraní, pokud máte **Premium experience** . Pro více informací navštivte [Změna funkcí, které jsou zobrazeny](ui-experiences.md).

Pokud je poptávka plánována a materiál byl vydán podle výrobních kusovníků, mohou být skutečné výrobní operace spouštěny a spouštěny v pořadí definovaném v TNG postupu výrobní zakázky.  

Důležitou součástí provádění výroby z hlediska systému je zaúčtovat výstup výroby do databáze za účelem vykazování průběhu a aktualizace zásob s dokončovým zbožím. Účtování výstupu lze provést ručně, vyplněním a zaúčtováním řádků deníku po operacích výroby. Nebo to lze provést automaticky pomocí zpětného odvádení. V takovém případě je spotřeba materiálu automaticky zaúčtována společně s výstupem při změně výrobní zakázky na dokončenou.  

Jako alternativu k dávkám deníku pro účtování výstupu pro více výrobních zakázek můžete použít stránku **Deník Výroby** k zaúčtování spotřeby a/nebo výstupu pro jednu linku výrobní zakázky.

Dříve než můžete začít vyrábět zboží, musíte provést různé nastavení, například pracovní střediska, technologické postupy a výrobní kusovníky. Pro více informací navštivte [Nastavení výroby](production-configure-production-processes.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.   

|**Viz**|**také**|  
|------------|-------------|  
|Porozumění jak výrobní zakázky fungují.|[O výrobních zakázkách](production-about-production-orders.md)|
|Ruční vytváření výrobních zakázek.|[Vytváření výrobních zakázek](production-how-to-create-production-orders.md)|
|Zadávání všech nebo vybraných operací ve výrobní zakázce subdodavateli.|[Subdodavatelská výroba](production-how-to-subcontract-manufacturing.md)|
|Zaznamenání a zaúčtování výstupu výroby spolu se spotřebou materiálu a časem pro jeden řádek vydané výrobní zakázky.|[Zaúčtování spotřeby a výstupu pro jeden řádek vydané výrobní zakázky](production-how-to-register-consumption-and-output.md)|  
|Dávkové zaúčtování množství komponent použitých pro operaci v deníku, které mohou zpracovávat více plánovaných výrobních zakázek.|[Dávkové účtování spotřeby](production-how-to-post-consumption.md)|
|Účtování množství hotového zboží a čas strávený na operaci v deníku, který dokáže zpracovat více vydaných výrobních zakázek.|[Dávkové zaúčtování výstupu a spuštění](production-how-to-post-output-quantity.md)|
|Vrácení výstupu, například z důvodu chyby v zadání dat a nesprávné částky  |[Reverzivní účtování výstupu](production-how-to-reverse-output-posting.md)|  
|Účtování několika zboží vyrobených v každé dokončené operaci, které nelze zařadit jako dokončený výstup, ale jako vyřazovaný materiál.|[Účtování odpadu](production-how-to-post-scrap.md)|
|Zobrazení zatížení dílny v důsledku plánovaných a vydaných výrobních zakázek.|[Zobrazit zatížení v pracovních a strojních centrech](production-how-to-view-the-load-on-work-centers.md)|      
|Stránka **Deník kapacit** slouží k zaúčtování spotřebovaných kapacit, které nejsou přiřazeny k výrobní zakázce, například k údržbě.|[Účtování kapacit](production-how-to-post-capacities.md)|  
|Výpočet a úprava nákladů na dokončené výrobní položky a spotřebované komponenty pro finanční odsouhlasení|[O nákladech na dokončenou výrobní zakázku](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Viz také  
[Nastavení výroby](production-configure-production-processes.md)  
[Plánování](production-planning.md)<x1 />      
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s[!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
