---
title: Vytváření a správa neskladovaného zboží | Microsoft Docs
description: 'Popisuje, jak obchodovat s neinventarizovatelným zbožím nebo zbožím, které není ve vašem skladu vedeno.'
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 06/02/2017
ms.author: sgroespe
---
# <a name="work-with-nonstock-items"></a>Práce s neskladovaným zbožím
Můžete nabídnout svým zákazníkům určité zboží pro jejich pohodlí, které nechcete udržovat v zásobách, dokud je nezačnete prodávat. Chcete-li toto zboží ukládat do zásob, můžete ho převést na běžné karty zboží dvěma způsoby.

* Z karty neskladovaného zboží vytvořte novou kartu zboží založenou na šabloně.
* Z řádku prodejní objednávky typu **Zboží** s prázdným polem **Číslo* vyberte neskladované zboží. Karta zboží je automaticky vytvořena pro neskladované zboží.

> [!NOTE]  
>   Nemůžete vybrat neskladované zboží z okna **Prodejní faktura**. Můžete vybrat neskladované zboží z okna **Prodejní nabídka**, ale neskladované zboží nebude převedeno na normální, pokud použijete funkci **Objednat**.

Neskladové zboží má typicky číslo zboží dodavatele, který jej nabízí. Chcete-li povolit konverzi karty neskladovaného zboží na normální kartu zboží, musíte nejprve nastavit, jak bude převedeno číslování zboží dodavatele na vaše číslování zboží.   

## <a name="to-create-a-nonstock-item"></a>Vytvoření zboží z katalogu
Karty neskladovaného zboží mají mnohem méně informací než karty normálního zboží, protože je používáte pouze v nabídkách a jinými způsoby. Z tohoto důvodu je třeba je převést na normální kartu, než budete moci za ně zaúčtovat prodejní transakce.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Neskladované zboží** a pak vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-nonstock-item-numbers-are-converted-to-your-own-numbering"></a>Chcete-li nastavit, jak se čísla neskladovaných položek převedou na vlastní číslování
Chcete-li povolit konverzi karty neskladovaného zboží na kartu normálního zboží, musíte nejprve nastavit, jak bude číslování zboží prodejce převedeno na váš vlastní formát čísla zboží.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Nastavení neskl.zboží** a pak vyberte související odkaz.
2. Vyplňte pole podle potřeby.

## <a name="to-convert-a-nonstock-item-to-a-normal-item"></a>Chcete-li převést neskladované zboží na normální
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Neskladované zboží** a pak vyberte související odkaz.
2. Otevřete kartu pro neskladované zboží, které chcete převést na normální.
3. V okně **Karta neskladovaného zboží** vyberte akci **Vytvořit zboží**.

Nová karta zboží předvyplněná informacemi ze šablon neskladované zboží a odpovídající šablona zboží je vytvořena. Můžete vyplnit nebo upravit pole na nové kartě zboží podle potřeby. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).

## <a name="to-sell-a-nonstock-item-and-convert-it-to-a-normal-item"></a>Chcete-li prodávat neskladované zboží a převést jej na normální zboží
1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "Hledat ikonu stránky nebo sestavy"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Zvolte akci **Nový**. Vyplňte pole na záložce **Obecné** jako u každé prodejní objednávky. Pro více informací navštivte [Prodej produktů](sales-how-sell-products.md).
3. Na novém prodejním řádku v poli **Typ** vyberte **Zboží**, ale pole **Číslo**  ponechte prázdné.
4. Vyberte akci **Řádek** a poté vyberte akci **Vybrat neskladované zboží**.

    Neskladované zboží je převedeno na normální zboží. Nová karta zboží předvyplněná informacemi ze šablony neskladované zboží a odpovídající šablona zboží je vytvořena.
5. V okně **Neskladované zboží** vyberte neskladované zboží, které chcete prodat a potom vyberte tlačítko **OK**.
6. Po dokončení prodejní objednávky zvolte akci **Zaúčtovat**.

Můžete vyplnit nebo upravit pole na nové kartě zboží podle potřeby. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).

> [!NOTE]  
>   Záznam křížového odkazu zboží je automaticky vytvořen pro dodavatele zboží mezi číslem zboží dodavatele a novým číslem zboží.

## <a name="see-also"></a>Viz také
[Evidence nového zboží](inventory-how-register-new-items.md)  
[Vytvoření speciálních objednávek](sales-how-to-create-special-orders.md)|  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
