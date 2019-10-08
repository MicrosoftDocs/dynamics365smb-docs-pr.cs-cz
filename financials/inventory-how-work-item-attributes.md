---
title: Nastavení atributů zboží a jejich přiřadění ke zboží | Microsoft Docs
description: 'Popisuje, jak například nastavit hodnoty atributů zboží, které lze použít jako vyhledávací slova, a přiřadit je ke zboží a kategoriím zboží.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'categories, search words, facets'
ms.date: 06/02/2017
ms.author: sgroespe
---
# <a name="work-with-item-attributes"></a>Práce s Atributy zboží
Když se zákazníci dotazují na položku, ať už v korespondenci nebo v integrovaném internetovém obchodu, mohou se zeptat nebo vyhledávat podle charakteristik, jako je výška a modelový rok. Chcete-li poskytnout tuto službu zákazníkům, můžete přiřadit hodnoty atributů zboží různého typu k vašemu zboží, které pak lze použít při hledání zboží.

Atributy zboží můžete také přiřadit kategoriím zboží, které se pak použijí na zboží, které používají kategorie zboží. Pro více informací navštivte [Kategorizace zboží](inventory-how-categorize-items.md).

> [!Tip]  
> Pokud ke zboží připojíte obrázky, rozšíření Image Analyzer dokáže detekovat atributy v obrázku a navrhnout atributy, abyste se mohli rozhodnout, zda je přiřadíte. Rozšíření je připraveno. Stačí jej povolit. Pro více informací navštivte [Rozšíření Image Analyzer pro Microsoft Business Central](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>K vytvoření atributů zboží
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Atributy zboží** a pak vyberte související odkaz.
2. V okně **Atributy zboží** vyberte akci **Nové**.
3. V okně **Atributy zboží** vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Pokud zvolíte **Možnosti** v poli **Typ**, pak můžete zvolit akci **Hodnoty atributů zboží** k vytvoření hodnot pro atributy zboží. Další informace naleznete v části "K vytvoření hodnot pro atributy zboží typu Volba".  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>K vytvoření hodnoty pro atributy zbpží typu Volba
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Atributy zboží** a pak vyberte související odkaz.
2. V okně **Atributy zboží**, vyberte atribut zboží typu **Možnost**, pro který chcete vytvořit hodnoty a pak zvolte akci **Hodnoty atributů zboží**.
3. V okně **hodnoty atributů zboží** vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>K přiřazení atributů zboží ke zboží
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Položky** a pak vyberte související odkaz.
2. V okně **Zboží** vyberte zboží, ke kterému chcete přiřadit atributy zboží a potom vyberte akci **Atributy**.
3. V okně **Hodnoty atributů zboží** vyberte akci **Nové**.
4. Vyberte vyhledávací tlačítko v poli **Atribut** a vyberte existující atribut zboží. Nebo zvolte akci **Nové**, chcete-li nejprve vytvořit nový atribut zboží, jak je vysvětleno v sekci "Vytvořit atributy zboží".
5. Do pole **Hodnota** zadejte hodnotu atributu zboží, například "2010" pro atribut **Rok výroby modelu**.
6. U atributů zboží typu **Možnost** vyberte vyhledávací tlačítko v poli **Hodnota** a vyberte hodnotu atributu zboží. Nebo zvolte akci **Nové**, chcete-li nejprve vytvořit novou hodnotu atributu zboží, jak je vysvětleno v sekci "Vytvořit hodnoty atributů zboží typu Volba".
7. Opakujte kroky 4 až 6 pro všechny atributy zboží, které chcete přiřadit ke zboží.

## <a name="to-assign-item-attributes-to-item-categories"></a>Přiřadit atributy zboží ke kategoriím zboží.
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Kategorie zboží** a pak vyberte související odkaz.
2. V okně **Kategorie zboží** vyberte kategorii zboží, ke kterým chcete přiřadit atributy zboží, a potom vyberte akci **Upravit**
3. V okně **Karta kategorií zboží** na záložce s náhledem **Atributy** zvolte akci **Nové**.
4. Vyberte vyhledávací tlačítko v poli **Atribut** a vyberte existující atribut zboží. Nebo zvolte akci **Nové**, chcete-li nejprve vytvořit nový atribut zboží, jak je vysvětleno v sekci "Vytvořit atributy zboží".
5. V poli **Výchozí hodnota** vyberte vyhledávací tlačítko a vyberte hodnotu atributu zboží.
6. Opakujte kroky 4 a 5 pro všechny atributy zboží, které chcete přiřadit ke kategorii zboží.

> [!NOTE]  
>   Atributy zboží pro nadřazené kategorie zboží budou zděděny do podřízených kategorií zboží. To je označeno políčkem **Zděděno z** na záložce s náhledem **Atributy**. Pro více informací navštivte [Kategorizace zboží](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Filtrovat podle atributů zboží
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Položky** a pak vyberte související odkaz.
2. V okně **Zboží** vyberte akci **Filtrovat podle atributů**.
3. V okně **Filtrovat zboží podle atributů** vyberte vyhledávací tlačítko v poli **Atribut** a vyberte atribut zboží.
4. V poli **Hodnota** vyberte tlačítko AssistEdit a vyberte hodnotu atributu pro filtrování zboží.

    > [!NOTE]  
   >   Hodnoty můžete vybrat pouze přímo pro atributy zboží, které mají fixní hodnoty, například Barva. Pro atributy položek, které mají proměnné hodnoty, jako je šířka, musíte zadat hodnotu atributu zboží výběrem podmínky nejprve. Viz krok 5.
5. V poli **Hodnota** pro atribut proměnné zboží zvolte vyhledávací tlačítko.
6. V okně **Určit hodnotu filtru** v poli **Podmínka** vyberte rozbalovací šipku a vyberte podmínku.
7. Do pole **Hodnota** zadejte hodnotu atributu pro filtrování položek.

    **Příklad**: Chcete-li filtrovat zboží, u kterého popis materiálu začíná "modrá", vyplňte následující pole: Pole **Atribut** : Popis materiálu, Pole **Podmínka**: Začíná s, Pole **Hodnota**: modrá.
8. Vyberte tlačítko **OK**.   

Zboží v okně **Zboží** je filtrováno podle specifikované hodnoty atributu zboží.

## <a name="see-also"></a>Viz také
[Kategorizujte položky](inventory-how-categorize-items.md)    
[Zaevidujte nové zboží](inventory-how-register-new-items.md)  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
