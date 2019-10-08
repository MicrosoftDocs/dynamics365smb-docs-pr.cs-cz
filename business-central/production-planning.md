---
title: Plánování dodávek | Microsoft Docs
description: Připravte podrobný realizovatelný plán a harmonogram výroby po dokončení montáže pro prodej a poptávku po výrobě.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="planning"></a>Plánování
Výrobní operace potřebné k přeměně vstupů na hotové zboží musí být plánovány denně nebo týdně v závislosti na objemu a povaze produktů. [!INCLUDE[d365fin](includes/d365fin_md.md)]nabízí funkce, které poskytují očekávané a skutečné požadavky z prodeje, montáže a výroby, stejně jako funkce pro plánování distribuce pomocí skladových jednotek a transferů lokací.

> [!NOTE]
> Toto téma popisuje zejména plánování společností zapojených do řízení výroby nebo montáže, kde výsledné objednávky dodávek mohou být buď výrobní, montážní, převodní nebo nákupní objednávky. Hlavním rozhraním pro tuto plánovací práci je stránka **Sešity plánováním** .

> [!INCLUDE[d365fin](includes/d365fin_md.md)]také podporuje plánování dodávek pro velkoobchody, kde výsledné objednávky dodávek mohou být pouze Transfer a nákupní objednávky. Hlavním rozhraním pro tuto plánovací práci je stránka **Sešit požadavků**, která je v tomto tématu popsána nepřímo, protože většina funkcí plánování se vztahuje na oba pracovní listy.

Dříve než můžete plánovat a provádět výrobní zakázky, musíte konfigurovat výrobní kapacity, jako jsou například vytváření kalendářů dílny, technologické postupy, výrobní kusovníky a strojní centra. Pro více informací navštivte [Nastavení výroby](production-configure-production-processes.md).

Plánování lze považovat za přípravu požadovaných objednávek dodávek v sestavení nebo výrobních oblastech k uspokojení poptávky. Pro více informací navštivte [Správa výroby](assembly-assemble-items.md) a [Výroba](production-manage-manufacturing.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.   

|**Viz**|**také**|  
|------------|-------------|  
|Stručný úvod do způsobu, jakým lze plánovací systém použít ke zjišťování a stanovení priorit poptávky a k návrhu vyrovnaného plánu dodávek.|[O funkcích plánování](production-about-planning-functionality.md)|
|Porozumění, jak fungují všechny aspekty plánovacího systému a jak upravit algoritmy, aby splňovaly požadavky plánování v různých prostředích.|[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)|
|Porozumění, jak logika plánování rozlišuje mezi poptávkou v lokacích podle nastavení SKJ a poptávky bez kódů lokací.|[Plánování s lokacemi nebo bez nich](production-planning-with-without-locations.md)|
|Prognóza poptávky představovaná očekávanými prodejními a výrobními komponentami.|[Vytvoření prognózy poptávky](production-how-to-create-a-forecast.md)|  
|Vytvořit automaticky one-to-one výrobní zakázku z prodejní objednávky tak, aby se pokryla přesná poptávka tohoto řádku prodejní objednávky.|[Vytvoření výrobní zakázky z prodejních objednávek](production-how-to-create-production-orders-from-sales-orders.md)|
|Vytvoření projektové výrobní zakázky přímo z víceřádkové prodejní objednávky představující výrobní projekt|[Plánování projektové objednávky](production-how-to-plan-project-orders.md)|
|Stránka **Plánování objednávek** slouží k ručnímu plánování prodeje nebo výroby po jednotlivých úrovních výrobního kusovníku.|[Plán nové objednávky poptávky podle objednávky](production-how-to-plan-for-new-demand.md)|
|Pomocí stránky **Sešity plánování** můžete spustit jak možnosti MPS, tak MRP pro automatické vytvoření plánu dodávky na vysoké úrovni nebo podrobný plán dodávek na všech úrovních položek.|[Spustit úplné plánování, MPS nebo MRP](production-how-to-run-mps-and-mrp.md)|
|Spuštěním sešitu požadavků se automaticky vytvoří podrobný plán dodávek, který pokryje poptávku po zboží, které jsou doplněny pouze nákupem nebo převodem.|Stránka **Sešity požadavků**|  
|Zahájení nebo aktualizace výrobní zakázky jako hrubě naplánované operace v hlavním plánu výroby|[Příme přeplánování nebo aktualizace výrobních zakázek](production-how-to-replan-refresh-production-orders.md)|
|Přepočítání pracovního nebo strojního centra z důvodu změn plánováním|[Výpočet kalendáře pracovního centra](production-how-to-create-work-center-calendars.md#to-calculate-a-work-center-calendar)|
|Sledování poptávky objednávky (sledované množství), prognózy, hromadné prodejní objednávky nebo parametru plánování (Nesledované množství), které vedly k danému řádku plánování.|[Sledování vztahů mezi poptávkou a nabídkou](production-how-track-demand-supply.md)|
|Zobrazení předpokládaných dostupných zásob zboží podle různých zobrazení a zjištění, které hrubé požadavky, příjmy plánovaných objednávek a další události v průběhu času ovlivňují.|[Zobrazení dostupnosti zboží](inventory-how-availability-overview.md)|  
|Provedení vybraných aktivit plánování, jako je například změna nebo přidání řádků plánovacího sešitu, v grafickém zobrazení plánu dodávek.|[Změna návrhů plánování v grafickém zobrazení](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a>Viz také
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)<x1 />    
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)   
[Doporučené postupy: lánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s[!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
