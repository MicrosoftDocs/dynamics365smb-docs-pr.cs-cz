---
title: Nastavení atributů zboží a jejich přiřadění ke zboží | Microsoft Docs
description: 'Popisuje, jak například nastavit hodnoty atributů zboží, které lze použít jako vyhledávací slova, a přiřadit je ke zboží a kategoriím zboží.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'categories, search words, facets'
ms.date: 03/01/2019
ms.author: sgroespe
---
# <a name="work-with-item-attributes"></a>Práce s Atributy zboží
Když se zákazníci dotazují na položku, ať už v korespondenci nebo v integrovaném internetovém obchodu, mohou se zeptat nebo vyhledávat podle charakteristik, jako je výška a modelový rok. Chcete-li poskytnout tuto službu zákazníkům, můžete přiřadit hodnoty atributů zboží různého typu k vašemu zboží, které pak lze použít při hledání zboží.

Atributy zboží můžete také přiřadit kategoriím zboží, které se pak použijí na zboží, které používají kategorie zboží. Pro více informací navštivte [Kategorizace zboží](inventory-how-categorize-items.md).

> [!Tip]  
> Pokud ke zboží připojíte obrázky, rozšíření Image Analyzer dokáže detekovat atributy v obrázku a navrhnout atributy, abyste se mohli rozhodnout, zda je přiřadíte. Rozšíření je připraveno. Stačí jej povolit. Pro více informací navštivte [Rozšíření Image Analyzer](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>K vytvoření atributů zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Atributy zboží** a poté vyberte související odkaz.
2. Na stránce **Atributy zboží** vyberte akci **Nový**.
3. Na stránce **Atributy zboží** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Pokud zvolíte **Možnosti** v poli **Typ**, pak můžete zvolit akci **Hodnoty atributů zboží** k vytvoření hodnot pro atributy zboží. Pro další informace navštivte [Vytvoření hodnoty pro atributy zboží typu možnost](inventory-how-work-item-attributes.md#to-create-values-for-item-attributes-of-type-option).  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>K vytvoření hodnoty pro atributy zbpží typu Volba
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Atributy zboží** a poté vyberte související odkaz.
2. Na stránce **Atributy zboží**, vyberte atribut zboží typu **Možnost**, pro který chcete vytvořit hodnoty a pak zvolte akci **Hodnoty atributů zboží**.
3. Na stránce **Hodnoty atributů zboží** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>K přiřazení atributů zboží ke zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky** a poté vyberte související odkaz.
2. Na stránce **Zboží** vyberte zboží, ke kterému chcete přiřadit atributy zboží a potom vyberte akci **Atributy**.
3. Na stránce **Hodnoty atributů zboží** vyberte akci **Nový**.
4. Vyberte vyhledávací tlačítko v poli **Atribut** a vyberte existující atribut zboží. Nebo zvolte akci **Nový**, chcete-li nejprve vytvořit novou kategorii zboží, jak je vysvětleno v sekci [Vytvoření atributu zboží](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. Do pole **Hodnota** zadejte hodnotu atributu zboží, například "2010" pro atribut **Rok výroby modelu**.
6. U atributů zboží typu **Možnost** vyberte vyhledávací tlačítko v poli **Hodnota** a vyberte hodnotu atributu zboží. Nebo zvolte akci **Nový**, chcete-li nejprve vytvořit novou hodnotu atributu zboží, jak je vysvětleno v sekci [Vytvořit hodnoty atributů zboží typu Volba](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-items).
7. Opakujte kroky 4 až 6 pro všechny atributy zboží, které chcete přiřadit ke zboží.

## <a name="to-assign-item-attributes-to-item-categories"></a>Přiřadit atributy zboží ke kategoriím zboží.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kategorie zboží** a poté vyberte související odkaz.
2. Na stránce **Kategorie zboží** vyberte kategorii zboží, ke kterým chcete přiřadit atributy zboží, a potom vyberte akci **Upravit**.
3. Na stránce **Karta kategorie zboží** na záložce **Atributy** zvolte akci **Nový**.
4. Vyberte vyhledávací tlačítko v poli **Atribut** a vyberte existující atribut zboží. Nebo zvolte akci **Nový**, chcete-li nejprve vytvořit novou kategorii zboží, jak je vysvětleno v sekci [Vytvoření atributu zboží](inventory-how-work-item-attributes.md#to-create-item-attributes).
5. V poli **Výchozí hodnota** vyberte vyhledávací tlačítko a vyberte hodnotu atributu zboží.
6. Opakujte kroky 4 a 5 pro všechny atributy zboží, které chcete přiřadit ke kategorii zboží.

> [!NOTE]  
>   Atributy zboží pro nadřazené kategorie zboží budou zděděny do podřízených kategorií zboží. To je označeno políčkem **Zděděno z** na záložce s náhledem **Atributy**. Pro více informací navštivte [Kategorizace zboží](inventory-how-categorize-items.md).

## <a name="to-filter-by-item-attributes"></a>Filtrovat podle atributů zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky** a poté vyberte související odkaz.
2. Na stránce **Zboží** vyberte akci **Filtrovat podle atributů**.
3. Na stránce **Filtrovat zboží podle atributů** vyberte vyhledávací tlačítko v poli **Atribut** a vyberte atribut zboží.
4. V poli **Hodnota** vyberte tlačítko AssistEdit a vyberte hodnotu atributu pro filtrování zboží.

    > [!NOTE]  
    >   Hodnoty můžete vybrat pouze přímo pro atributy zboží, které mají fixní hodnoty, například Barva. Pro atributy položek, které mají proměnné hodnoty, jako je šířka, musíte zadat hodnotu atributu zboží výběrem podmínky nejprve. Viz krok 5.
5. V poli **Hodnota** pro atribut proměnné zboží zvolte vyhledávací tlačítko.
6. Na stránce **Určit hodnotu filtru** v poli **Podmínka** vyberte rozbalovací šipku a vyberte podmínku.
7. Do pole **Hodnota** zadejte hodnotu atributu pro filtrování položek.

    **Příklad**: Chcete-li filtrovat zboží, u kterého popis materiálu začíná "modrá", vyplňte následující pole: Pole **Atribut** : Popis materiálu, Pole **Podmínka**: Začíná s, Pole **Hodnota**: modrá.
8. Vyberte tlačítko **OK**.   

Zboží na stránce **Zboží** je filtrováno podle specifikované hodnoty atributu zboží.

## <a name="see-also"></a>Viz také
[Kategorizujte položky](inventory-how-categorize-items.md)    
[Zaevidujte nové zboží](inventory-how-register-new-items.md)  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
