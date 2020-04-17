---
title: Review and Post the Year-End Closing Entry | Microsoft Docs
description: Describes how to open the journal you specified in the Close Income Statement batch job, and then review and post the year-end closing entry. 
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
# Účtování položky uzávěrky na konci roku
Po použití dávkové úlohy **Uzavření výsledovky**  ke generování závěrečné položky nebo položek na konci roku musíte otevřít deník, který jste určili v dávkové úloze, a poté zkontrolovat a zaúčtovat položky.

## Zaúčtování položky uzávěrky na konci roku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deník** a poté vyberte související odkaz.
2. Na stránce **Finanční deník** v poli **Název dávky** vyberte dávku, která obsahuje uzavírací položky.
3. Zkontrolujte položky.
4. Chcete-li deník zaúčtovat, zvolte akci **Účtovat**.

> [!NOTE]
> Pokud je zjištěna chyba, zobrazí se chybová zpráva. Pokud je účtování úspěšné, budou zaúčtované položky odstraněny z deníku. Po dokončení účtování se na každý účet výsledovky zaúčtuje položka tak, aby se jeho zůstatek stal nulovým a výsledek roku se přenesl do rozvahy.

## Viz také
[Uzavírání účetního období](year-close-account-periods.md)  
[Uzavírání knih](year-close-books.md)  
[Uzavírání účtů výsledovky](year-close-income-statement.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
