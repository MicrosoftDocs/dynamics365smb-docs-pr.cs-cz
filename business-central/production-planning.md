---
title: Plánování dodávek | Microsoft Docs
description: Připravte podrobný realizovatelný plán a harmonogram výroby pro prodejní a výrobní poptávky.
services: project-madeira
documentationcenter: ''
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 01/17/2020
ms.reviewer: v-zdbice
ms.author: sgroespe
---
# Plánování

Výrobní operace potřebné k přeměně vstupů na hotové výrobky musí být plánovány denně nebo týdně v závislosti na objemu a povaze produktů. [!INCLUDE[d365fin](includes/d365fin_md.md)] nabízí funkce, které poskytují předpokládané a skutečné požadavky z prodeje, montáže a výroby, stejně jako funkce pro plánování logistiky pomocí skladových jednotek a převodů mezi lokacemi.

> [!NOTE]
> Toto téma popisuje zejména plánování společností využívajících řízení výroby nebo montáže, kde výsledné realizační objednávky mohou být buď výrobní zakázky, montážní zakázky, objednávky transferu nebo nákupní objednávky. Hlavním rozhraním pro tuto plánovací práci je stránka **Sešity plánováním**.<br /><br />
> [!INCLUDE[d365fin](includes/d365fin_md.md)] také podporuje plánování pro velkoobchody, kde výsledné realizační objednávky mohou být pouze objednávky transferu a nákupní objednávky. Hlavním rozhraním pro tuto plánovací práci je stránka **Sešit požadavků**, která je v tomto tématu popsána nepřímo, protože většina funkcí plánování se vztahuje na oba sešity.

Dříve než můžete plánovat a realizovat výrobní zakázky, musíte konfigurovat výrobní kapacity, jako jsou například  kalendáře dílen, technologické postupy, výrobní kusovníky a strojní centra. Pro více informací navštivte [Nastavení výroby](production-configure-production-processes.md).

Plánování lze chápat jako přípravu požadovaných realizačních objednávek v nákupních, montážních nebo výrobních odděleních k uspokojení prodejních požadavků nebo požadavků na výrobky.Pro více informací navštivte [Nákup](purchasing-manage-purchasing.md), [Správa montáží](assembly-assemble-items.md) a [Výroba](production-manage-manufacturing.md).

Následující tabulka popisuje přehled úloh s odkazy na témata, které je popisují.

|**Funkce**|**Odkaz**|  
|------------|-------------|  
|Stručný úvod do způsobu, jakým lze plánovací systém použít ke zjišťování a stanovení priorit poptávky a k návrhu vyrovnaného plánu dodávek.|[O funkcích plánování](production-about-planning-functionality.md)|
|Porozumění, jak fungují všechny procesy plánovacího systému a jak upravit algoritmy, aby splňovaly požadavky plánování v různých prostředích.|[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)|
|Porozumění, jak logika plánování rozlišuje mezi poptávkou na lokacích podle nastavení SKJ a poptávkou bez kódů lokací.|[Plánování s lokacemi nebo bez nich](production-planning-with-without-locations.md)|
|Prognóza poptávky představovaná očekávanými prodeji a spotřebou výrobních komponent.|[Vytvoření prognózy poptávky](production-how-to-create-a-forecast.md)|  
|Automaticky vytváření výrobní zakázky z prodejní objednávky jedna k jedné tak, aby se pokryla přesná poptávka tohoto řádku prodejní objednávky.|[Vytváření výrobních zakázek z prodejních objednávek](production-how-to-create-production-orders-from-sales-orders.md)|
|Vytvoření projektové výrobní zakázky přímo z víceřádkové prodejní objednávky představující výrobní projekt.|[Plánování projektové objednávky](production-how-to-plan-project-orders.md)|
|Použití stránky **Plánování objednávek** k ručnímu plánování prodejní nebo výrobní poptávky po jednotlivých úrovních výrobního kusovníku.|[Plánování nové poptávky po objednávkách](production-how-to-plan-for-new-demand.md)|
|Pomocí stránky **Sešity plánování** můžete spustit jak možnosti MPS, tak MRP pro automatické vytvoření plánu dodávek na nejvyšší úrovni nebo podrobný plán dodávek na všech úrovních zboží.|[Spustit úplné plánování, MPS nebo MRP](production-how-to-run-mps-and-mrp.md)|
|Spuštěním sešitu požadavků se automaticky vytvoří podrobný plán dodávek, který pokryje poptávku po zboží, které je doplňováno pouze nákupem nebo převodem.|Stránka **Sešity požadavků**|  
|Zahájení nebo aktualizace výrobní zakázky jako hrubé naplánování operaci v hlavním plánu výroby.|[Přímé přeplánování nebo aktualizace výrobních zakázek](production-how-to-replan-refresh-production-orders.md)|
|Přepočítání kalendářů pracovního nebo strojního centra z důvodu změn plánováním.|[Výpočet kalendáře pracovního centra](production-how-to-create-work-center-calendars.md#to-calculate-a-work-center-calendar)|
|Sledování poptávky objednávky (sledované množství), prognózy, hromadné prodejní objednávky nebo plánovacích parametrů (nesledované množství), které vedly k danému řádku plánování.|[Sledování vztahů mezi poptávkou a dodávkou](production-how-track-demand-supply.md)|
|Zobrazení předpokládaných dostupných zásob zboží z různých pohledů a zjištění, které hrubé požadavky, plánované příjmy objednávek a další události v průběhu času ovlivňují dostupnost.|[Zobrazení dostupnosti zboží](inventory-how-availability-overview.md)|  
|Provedení vybraných aktivit plánování, jako je například změna nebo přidání řádků plánovacího sešitu v grafickém zobrazení plánu dodávek.|[Změna návrhů plánování v grafickém zobrazení](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## Viz také

[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)   
[Doporučené postupy: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
