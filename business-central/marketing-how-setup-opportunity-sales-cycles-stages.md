---
title: Set Up Opportunity Sales Cycles and Cycle Stages| Microsoft Docs
description: Describes how to define sales stages, from initial contact to closing, to create a sales cycle and assign it to opportunities in Business Central.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2020
ms.author: jswymer

---
# Nastavení prodejních cyklů příležitostí a fází prodejního cyklu
Než začnete používat prodejní příležitosti, musíte nastavit prodejní cykly a fáze prodejního cyklu. Prodejní cyklus je tvořen řadou fází, které probíhají od počátečního kontaktu po uzavření prodeje. Každá fáze může mít určité požadavky, které musí být splněny, například požadavek na prodejní nabídku, než se příležitost dostane do další fáze. Můžete také určit, zda lze fázi přeskočit. Můžete nastavit tolik prodejních cyklů, kolik potřebujete, a můžete nastavit tolik fází prodejního cyklu, kolik je potřeba.

Implementace prodejních cyklů příležitostí zahrnuje nastavení prodejního cyklu, definování různých fází cyklu a následné přiřazení cyklu příležitostem. Součástí nastavení prodejního cyklu může být také přiřazení příslušné činnosti nebo úkolů příležitosti.

Toto téma také popisuje, jak nastavit úkoly a aktivity a jak přiřadit úkoly k aktivitám. Pro více informací navštivte [Nastavení aktivit s úkoly](marketing-how-setup-opportunity-sales-cycles-stages.md).

## Nastavení kódů prodejního cyklu příležitosti
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní cykly** a poté vyberte související odkaz. Otevře se stránka **Prodejní cykly** a zobrazí se seznam všech existujících prodejních cyklů.
2. Vyberte akci **Nový** a podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Tyto kroky opakujte a nastavte tolik prodejních cyklů, kolik chcete. Poté, co jste nastavili prodejní cykly příležitosti, možná budete chtít nastavit různé fáze v rámci každého cyklu.

## Definování fází prodejního cyklu příležitosti
1. Na stránce **Prodejní cykly** vyberte prodejní cyklus příležitosti, pro který chcete nastavit fáze, a pak zvolte akci **Fáze**. Otevře se stránka **Fáze prodejního cyklu**.
2. Vyberte akci **Nový** a zadejte novou fázi prodejního cyklu.

Tyto kroky opakujte a nastavte v rámci prodejního cyklu tolik fází, kolik chcete.

## Přiřazení fázových cyklů příležitostem
Po přidání fázových cyklů příležitostí můžete začít přidávat prodejní příležitosti a potom přiřadit fázový cyklus příležitostem nastavením pole **Kód prodejního cyklu**. Pro více informací navštivte [Vytvoření prodejních příležitostí](marketing-how-create-opportunities.md).

## Nastavení aktivit s úkoly
V aktivitách můžete kombinovat více úkolů, například úkolů, z nichž každý představuje jeden krok. Úkoly aktivity jsou vzájemně propojeny vzorcem data. Aktivity můžete přiřadit příležitostem, prodejcům nebo kontaktům.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Aktivity** a poté vyberte související odkaz.
2. Vyberte akci **Nový** a podle potřeby vyplňte pole.
3. Na záložce **Řádky** vyplňte pole podle potřeby pro definování jedné nebo více úkolů v aktivitě.

## Přiřazení úkolů nebo činností úkolů příležitostem
Když jste nastavili úkol, můžete jej přiřadit k obchodní příležitosti a tím přiřadit činnost, ke které úkol patří.

> [!NOTE]
> Tento postup popisuje, jak přiřadit úkoly aktivity příležitostem. Kroky jsou podobné, když přiřazujete úkoly prodejcům a kontaktům.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Příležitosti** a poté vyberte související odkaz.
2. Vyberte příležitost a poté vyberte akci **Úlohy**.
3. Na stránce **Přehled úloh** vyberte akci **Vytvořit úlohu**.
4. Na stránce **Vytvořit úlohu** vyplňte pole podle potřeby.

   Všimněte si v poli **Příležitost**, že je automaticky přiřazena k dané příležitosti.
5. Vyberte tlačítko **OK**.
6. Na stránce **Přehled úloh**  vyberte nový úkol a poté vyberte akci **Přiřadit aktivity**.
7. Na stránce **Přiřadit aktivity** vyplňte pole podle potřeby a poté vyberte tlačítko **OK**.

## Viz také
[Zpracování prodejních příležitostí](marketing-processing-sales-opportunities.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
