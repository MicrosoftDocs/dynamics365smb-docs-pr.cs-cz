---
title: Analyze Actual Versus Budget| Microsoft Docs
description: Describes how to analyze actual amounts versus budgeted amounts.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2020
ms.author: sgroespe

---
# Analýza skutečných částek proti částkám rozpočtu
V rámci shromažďování, analýzy a sdílení údajů o vaší společnosti zobrazíte skutečné částky ve srovnání s částkami rozpočtu pro všechny účty a za několik období.

Chcete-li analyzovat částky rozpočtu, musíte nejprve vytvořit finanční rozpočty. Pro více informací navštivte [Vytvoření finančních rozpočtů](finance-how-create-budgets.md).

## Zobrazení finančního rozpočtu
V rozpočtu s dimenzemi můžete filtrovat položky a zobrazit konkrétní rozpočty.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční rozpočty** a poté vyberte související odkaz.
2. Na stránce **Finanční rozpočty** otevřete rozpočet, který chcete zobrazit.
3. V horní části stránky vyplňte pole podle potřeby, abyste určili, co se má zobrazit. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Pokud jste v poli **Zobrazit jako řádky** nebo **Zobrazit jako sloupce** vybrali **Období**, pak musíte vyplnit pole **Zobrazit podle**. Pokud jste nevybrali **Období** v poli **Zobrazit jako řádky** nebo **Zobrazit jako sloupce** zadejte příslušné období do pole **Filtr data**.

> [!NOTE]
> Do výpočtu jsou zahrnuty pouze položky z rozpočtu hlavní knihy s kódy filtrů, které zadáte do záložky **Filtry**. Položky rozpočtu s jinými kódy filtrů nebo bez kódů filtrů nejsou zahrnuty. Dokud filtr zůstane na stránce, rozpočet zobrazí pouze položky rozpočtu s těmito kódy filtrů.

> [!TIP]
> Pokud chcete upravit rozpočet, můžete upravit položky rozpočtu. Vyberte částku a zobrazte základní položky rozpočtu hlavní knihy.

## Zobrazení skutečných částek a částek rozpočtu pro všechny účty
Můžete zobrazit rozpočty hlavní knihy a porovnat je se skutečnými čísly v několika oblastech [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
2. Na stránce **Účetní osnova** vyberte akci **Saldo/rozpočet**.
3. V horní části stránky vyplňte pole podle potřeby, abyste určili, co se má zobrazit.
4. Chcete-li zobrazit specifikaci, která tvoří zobrazenou částku, vyberte pole.

> [!NOTE]
> Filtry, které nastavíte v záhlaví stránky, budou použity na položky hlavní knihy a také na položky rozpočtu.

Sloupce vlevo obsahují graf účtů. Z pěti sloupců na pravé straně první čtyři sloupce zobrazují skutečné částky, částky rozpočtů a částky MD pro každý účet. Pátý sloupec zobrazuje proporcionální vztah mezi skutečnými a rozpočtovými částkami na účtu hlavní knihy.

> [!TIP]
> Pomocí pole **Zobrazit podle** na stránce **Saldo/rozpočet** vyberte délku období. Pomocí pole **Zobrazit jako** vyberte způsob výpočtu částek, **Pohyb** nebo **Saldo do data**. Vyberte akci **Předchozí období** nebo **Další období** pokud chcete období změnit.

## Zobrazení skutečných částek a částek rozpočtu za několik období
Místo zobrazení skutečných částek a částek rozpočtu pro všechny účty v jednom období můžete zobrazit několik období pro jeden účet.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
2. Na stránce **Účetní osnova** vyberte příslušný účet hlavní knihy a poté vyberte akci **Saldo/rozpočet účtu**.
3. V horní části stránky vyplňte pole podle potřeby, abyste určili, co se má zobrazit.
4. Chcete-li zobrazit specifikaci zobrazené částky, zvolte pole.

## Viz Související školení na [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## Viz také
[Business Intelligence](bi.md)  
[Práce s účetní schémou](bi-how-work-account-schedule.md)  
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Věcné položky a Účetní osnova](finance-general-ledger.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
