---
title: Optional Activities for Closing Periods | Microsoft Docs
description: This topic outlines the optional processes and activities for closing accounting periods in Business Central.  
services: project-madeira
documentationcenter: ''
author: jswymer

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 10/01/2019
ms.author: jswymer

---
# Uzavírací období
[!INCLUDE[d365fin](includes/d365fin_md.md)] vás nenutí k uzavření období, ale existuje mnoho aktivit na konci období (na konci měsíce), které můžete udělat. Toto téma poskytuje přehled volitelných procesů a činností pro uzávěrková období.

## Finance
* Určete období účtování uživatele pro celý systém.

   Toto určuje data, mezi kterými povolujete účtování. V závislosti na vaší firmě můžete povolit účtování na začátku období nebo ke konci. Pro více informací navštivte [Určení zúčtovacího období](finance-how-specify-posting-periods.md).
* Proveďte všechny nezbytné opravy financí.
* Aktualizujte a zaúčtujte periodické deníky.
   <!--* Process Consolidations-->
* Spusťte účetní schémata takto:
   * Otevřete stránku **Účetní schéma** a poté vyberte akci **Tisk**.

## Prodej a pohledávky
* Zaúčtujte všechny prodejní objednávky, faktury, dobropisy a objednávky vratek.
* Zaúčtujte všechny deníky přijaté hotovosti.
* Aktualizujte a zaúčtujte periodické deníky, které se vztahují k prodejům a pohledávkám.
* Odsouhlaste pohledávky v hlavní knize.
* Spusťte dávkovou úlohu **Odstranit fakt.prod.objednávky**.

## Nákupy a závazky
* Zaúčtujte všechny objednávky, faktury, dobropisy a objednávky vratek.
* Zaúčtujte všechny deníky plateb.
* Aktualizujte a zaúčtujte periodické deníky, které souvisejí s nákupy a závazky.
* Spusťte sestavu **Splatné závazky** a odsouhlaste závazky do hlavní knihy.
* Spusťte dávkovou úlohu **Odstranit fakt. nák. objednávky**.

Dlouhodobý majetek
* Účtování všech nákladů na údržbu bylo zaúčtováno prostřednictvím deníků nebo faktur s dlouhodobým majetkem.
* Zaúčtujte opravy.
* Zaúčtujte zhodnocení.
* Zaúčtujte odpisy.
* Aktualizujte a zaúčtujte periodický deník DM.

Vnitropodnik
* Zpracování vnitropodnikových transakcí

## Výpočet a zpracování DPH
* Kompletní daňové přiznání.

## Viz také
[Uzavírání roků a období](year-close-years-periods.md)  
[Uzavírání knih](year-close-books.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
