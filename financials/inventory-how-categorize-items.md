---
title: Uspořádaní zboží do kategorií | Microsoft Docs
description: 'Abyste mohli vyhledávat a hledat zboží, můžete přiřadit atributy zboží a uspořádat zboží do kategorií.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'category, search, attribute, facet'
ms.date: 03/01/2019
ms.author: sgroespe
---
# <a name="categorize-items"></a>Kategorizace zboží
Chcete-li udržovat přehled o vašem zboží, který vám může pomoc při řazení a hledání zboží, je vhodné ho uspořádat v kategoriích zboží.

Chcete-li vyhledat zboží podle vlastností, můžete přiřadit atributy zboží ke zboží a také ke kategoriím zboží. Pro více informací navštivte [Práce s atributy zboží](inventory-how-work-item-attributes.md).

## <a name="to-create-an-item-category"></a>Vytvoření kategorie zboží
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Kategorie zboží** a pak vyberte související odkaz.
2. V okně **Kategorie zboží**, vyberte akci **Nový**.
3. V okně **Karta kategorie zboží** na záložce **Hlavní** vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Na záložce **Atributy** zadejte všechny atributy zboží pro kategorii zboží. Pro více informací navštivte sekci “Přiřadit atributy zboží ke kategorii zboží“ v [Práce s atributy zboží](inventory-how-work-item-attributes.md)

> [!NOTE]  
>   Pokud kategorie zboží obsahuje nadřazenou kategorii zboží, jak je uvedeno v poli **Nadřazená kategorie**, pak jakékoli atributy zboží, které jsou přiřazeny této nadřazené kategorii zboží, jsou předem vyplněny na záložce **Atributy**.

> [!NOTE]  
>   Atributy zboží, které přiřadíte ke kategorii zboží, se automaticky použijí na zboží, ke kterému je kategorie zboží přiřazena.

## <a name="to-assign-an-item-category-to-an-item"></a>Přiřazení kategorie zboží ke zboží
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Položky** a pak vyberte související odkaz.
2. Otevřete kartu pro zboží, které chcete přiřadit ke kategorii zboží.
3. Vyberte vyhledávací tlačítko v poli **Kód kategorie zboží** a vyberte existující kategorii zboží. Nebo zvolte akci **Nový**, chcete-li nejprve vytvořit novou kategorii zboží, jak je vysvětleno v sekci [Vytvoření kategorie zboží](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="see-also"></a>Viz také
[Práce s atributy zboží](inventory-how-work-item-attributes.md)  
[Evidence nového zboží](inventory-how-register-new-items.md)  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
