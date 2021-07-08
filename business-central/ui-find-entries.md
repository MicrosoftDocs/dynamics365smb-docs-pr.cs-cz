---
title: Finding entries | Microsoft Docs
description: This article describes how to documents and entries that are related
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 04/01/2021
ms.author: jswymer
---
# Hledání souvisejících položek pro zaúčtovaných dokladů

V tomto článku se dozvíte, jak najít doklady a položky, které spolu souvisejí, na základě běžných informací, jako jsou:

- Číslo dokladu nebo zúčtovací datum
- Typ obchodního kontaktu, číslo nebo číslo externího dokladu
- Sériové číslo zboží nebo číslo šarže

Tato funkce je užitečná pro vyhledání položek, které byly výsledkem určitých transakcí. Při hledání podle čísla dokladu můžete vytisknout souhrn ze sestavy Položky dokladu.

## Začínáme

Funkce hledání položek je snadno dostupná na většině stránek, které zobrazují zaúčtované doklady nebo zaúčtované položky dokladů - pro seznamy i karty. Prvním krokem je tedy otevření jedné z těchto stránek. Potom vyberte akci **Najít položky** nebo zmáčkněte klávesy Alt+G.

Stránka **Najít položky** obsahuje všechny související doklady a položky založené na čísle dokladu a zúčtovacím datu. Stránka je rozdělena do tří částí:

- V horní části jsou zobrazena pole a akce, které používáte k filtrování hledání.
- Prostřední část zobrazuje související doklady na základě vyhledávání.
- V dolní části jsou zobrazeny informace o zdrojovém dokladu, který byl nalezen vyhledáváním.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## Vyhledávání položek

Záznamy můžete hledat na základě informací o dokladu, obchodním kontaktu nebo odkazu na položku. Chcete-li změnit hledání,  vybrte **Akce**, **Hledat podle** poté jednu z následujících akcí:

| Akce | Popis |
|------|-----------|
| Hledat podle dokladu | Zobrazte záznamy na základě konkrétního čísla dokladu nebo data zaúčtování. |
| Hledat podle obchodního vztahu | Zobrazí položky na základě konkrétního typu kontaktu, čísla kontaktu a/nebo podle čísla externího dokladu. Můžete zadat informace o dokladu přiřazené dodavatelem nebo zákazníkem. Dostupná pole použijte k vyhledání dokladů dodavatele pomocí čísel, která dodavatel přiřadil dokladům. |
| Hledat podle odkazu zboží | Zobrazení položek na základě sériového čísla nebo čísla šarže. Můžete zadat číslo šarže nebo sériové číslo nebo filtrovat podle čísla šarže nebo sériového čísla, které chcete vyhledat. Tato akce je užitečná pro zjištění, kde bylo použito konkrétní sledovací číslo zboží, od kterého dodavatele pochází nebo kterému zákazníkovi bylo prodáno. |

Po provedení výběru zadejte příslušné vyhledávací informace do polí v horní části. Chcete-li pomoci, použijte tooltipy. Po dokončení spusťte vyhledávání pomocí tlačítka **Najít**. Pokud změníte některý z filtrů, musíte znovu použít funkci **Najít**.

> [!TIP]
> Několik příkladů použití **Najít položky** naleznete v [Sledování zboží - Sledované zboží](inventory-how-to-trace-item-tracked-items.md) a [Návod:Sledování zboží - Sledované zboží](walkthrough-tracing-serial-lot-numbers.md).

## Zobrazit související školení na webu [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## Viz také

[Práce s Business Central](ui-work-product.md)  
[Přidání tlačítka na stránku ve Vašem Centru rolí](ui-bookmarks.md)  
[Sledování zboží - Sledované zboží](inventory-how-to-trace-item-tracked-items.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]