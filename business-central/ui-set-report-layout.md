---
title: Setting the Report Layout
description: Learn how to set the layout that's used on a report when previewing and printing.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 03/07/2022
ms.author: jswymer
---
# Nastavení rozvržení používaného sestavou

> **PLATÍ PRO:** Business Central online, Business Central on-premises 2022 release wave 1 a novější. Pro starší verze přejděte [sem](ui-how-change-layout-currently-used-report.md).

Rozvržení sestavy určuje vzhled sestavy. Určuje, která datová pole datové sady sestavy se zobrazí, jak jsou uspořádána, stylizována a další. Sestava může mít více než jedno rozvržení, mezi kterými pak můžete podle potřeby přepínat.

Pokud je v aplikaci více společností, rozvržení jsou nastavena na základě jednotlivých společností. Takže stejná sestava v jedné společnosti může mít jiné rozvržení v jiné společnosti.

## Začínáme

Existují dva způsoby, jak nastavit rozvržení, které sestava používá. Jedním ze způsobů je stránka **Výběr rozvržení sestav**. Druhý způsob je ze stránky **Rozvržení sestav**. Každá stránka má výhody, například:

- Na stránce **Výběr rozvržení sestav** se zobrazí seznam všech sestav.

   Tato stránka ukazuje, jaké je aktuální rozvržení sestavy Navíc můžete nastavit rozvržení v různých společnostech, aniž byste museli přepínat mezi společnostmi.

- Stránka **Rozvržení sestav** zobrazuje všechna dostupná rozvržení pro každou sestavu v aktuální společnosti.

   Je snadné najít konkrétní rozvržení seřazením nebo filtrováním seznamu. Jakmile rozvržení najdete, můžete ho nastavit pro sestavu s jedním výběrem.

   > [!NOTE]
   > Stránku **Rozvržení sestav** nelze použít pro rozvržení aplikací Word a RDLC, která byly vytvořeny pomocí starší funkce **Vlastního rozvržení**. Ve skutečnosti tato vlastní rozvržení ani neuvidíte na stránce **Rozvržení sestav**. Tyto rozvržení je možné nastavit pouze pomocí stránky **Výběr rozvržení sestav**.

## Nastavení rozvržení ze stránky Rozvržení sestav

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Najděte rozvržení v seznamu, vyberte jej a poté v horní části stránky vyberte akci **Nastavit výchozí**.

## Nastavení rozvržení ze stránky Výběr rozvržení sestav

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výběr rozvržení sestav** a poté vyberte související odkaz.

   Na stránce jsou uvedeny všechny sestavy, které jsou k dispozici pro společnost, která je zadána v poli **Společnost** v horní části stránky. Pole **Popis rozvržení** určuje rozložení, které sestava aktuálně používá.
2. Nastavte pole **Společnost** v horní části na společnost, která obsahuje sestavu.
3. Najděte a vyberte sestavu v seznamu a proveďte jeden z následujících kroků:

   - Pokud je rozvržení, na které chcete přepnout, jiného typu než aktuální rozvržení, vyberte pole **Typ rozvržení** a pak vyberte typ rozvržení, které chcete v sestavě nastavit.
   - Pokud chcete rozvržení, které chcete přepnout na stejný typ jako aktuální rozvržení, vyberte nahoře akci **Vybrat rozvržení**.

4. Na stránce **Rozvržení sestav** vyberte rozvržení a poté vyberte **OK**.

## Návrat k původnímu výchozímu rozvržení

Sestavy jsou navrženy tak, aby používaly vvýchozí rozvržení. Zpět na původní výchozí rozložení můžete přepnout ze stránky **Výběr rozvržení sestav**. Stačí vybrat sestavu a poté v horní části stránky vybrat akci **Obnovit výchozí výběr**.

## Viz související školení na webu [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## Viz také

[Správa rozvržení sestav](ui-manage-report-layouts.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]