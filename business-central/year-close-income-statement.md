---
title: Close Income Statement Accounts | Microsoft Docs
description: At year closing, you must run the Close Income Statement batch job to close the accounting periods that make up the fiscal year.
services: project-madeira
documentationcenter: ''
author: jswymer

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2019
ms.author: jswymer

---
# Uzavírání účtů výsledovky
Když skončí fiskální rok, musíte uzavřít období, která jej tvoří. Chcete-li to provést, spusťte dávkovou úlohu **Uzavření výsledovky**. Tato úloha převede výsledek roku na účet v rozvaze a uzavře účty výsledovky. To lze provést vytvořením řádků v deníku, které pak můžete zaúčtovat.

## Spuštění dávkové úlohy Uzavření výsledovky
1. Zavřete fiskální rok. Před spuštěním dávkové úlohy musí být fiskální rok uzavřen. Pro více informací navštivte [Uzavírání účetního období](year-close-account-periods.md).
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uzavření výsledovky** a poté vyberte související odkaz.
3. Zvolte tlačítko **OK** a spusťte dávkovou úlohu.

## Dávková úloha Uzavření výsledovky
Dávková úloha zpracuje všechny obecné účty typu výsledovka a vytvoří položky, které zruší jejich příslušné zůstatky. To znamená, že každá položka je součtem všech položek financí na účtu ve fiskálním roce. Tyto nové položky jsou umístěny do deníku, ve kterém musíte zadat protiúčet a účet nerozděleného zisku v rozvaze před zaúčtováním. Při zaúčtování deníku je položka zaúčtována na každý účet výsledovky tak, aby se její zůstatek stal nulovým a současně byl výsledek roku převeden do rozvahy.

Deník musíte zaúčtovat sami. Dávková úloha neúčtuje položky automaticky, s výjimkou případů, kdy se používá další měna pro hlášení. Při použití další měny vykazování dávková úloha zaúčtuje položky přímo do hlavní knihy.

Datum na řádcích, které dávková úloha vloží do deníku, je vždy konečným datem pro fiskální rok. Datum uzávěrky je fiktivní datum mezi posledním dnem starého fiskálního roku a prvním dnem nového roku. Výhodou zaúčtování v den uzávěrky je to, že udržujete správné zůstatky pro běžná data fiskálního roku.

Dávkovou úlohu **Uzavření výsledovky**  lze použít několikrát. Pokud dávkovou úlohu spustíte znovu, můžete účtovat v předchozím fiskálním roce, a to i po uzavření účtů výsledovky.

## Viz také
[Uzavírání knih](year-close-books.md)  
[Účtování položky konce roku](year-how-post-year-end-close-entry.md)  
[Otevření nového fiskálního roku](finance-how-open-new-fiscal-year.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
