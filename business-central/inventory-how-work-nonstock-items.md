---
title: Vytváření a správa katalog zboží | Microsoft Docs
description: 'Popisuje, jak obchodovat se zbožím, které je v seznamu položek vašich dodavatelů, ale nikoli ve vašem vlastním seznamu zboží.'
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: non-inventoriable
ms.date: 03/12/2019
ms.author: sgroespe
---
# <a name="work-with-catalog-items"></a>Práce s katalogem zboží
Můžete nabídnout svým zákazníkům určité zboží pro jejich pohodlí, které nechcete spravovat ve svém systému, dokud je nezačnete prodávat. Pokud chcete začít spravovat takové zboží ve vašem systému, můžete je převést na karty normálního zboží dvěma způsoby.

* Z karty katalogu zboží vytvořte novou kartu zboží založenou na šabloně.
* Z řádku prodejní objednávky typu **Zboží** s prázdným polem **Číslo** vyberte katalog zboží. Karta zboží je pak automaticky vytvořena pro zboží katalogu.

> [!NOTE]  
> Nemůžete vybrat katalog zboží ze stránky **Prodejní faktura**.<br /><br />
> Zboží katalogu můžete vybrat na stránce **prodejní nabídka**, ale zboží katalogu se při použití funkce **Vytvořit zakázku** nepřevede na normální zboží.

Zboží katalogu má typicky číslo zboží dodavatele, který jej nabízí. Chcete-li povolit konverzi karty zboží katalogu na normální kartu zboží, musíte nejprve nastavit, jak bude převedeno číslování položek dodavatele na vaše číslování položek.   

> [!Important]
> Zboží katalogu by se nemělo zaměňovat se zbožím mimo zásob, což je běžné zboží, které dostávají typ **Mimo zásoby**, aby je např. udržovaly mimo výpočty dostupnosti a kalkulace, protože se používají pouze interně a mají nízké náklady. Pro více informací navštivte [O typech zboží](inventory-about-item-types.md).

## <a name="to-create-a-catalog-item"></a>Vytvoření zboží katalogu
Karty zboží katalogu mají mnohem méně informací než karty normálního zboží, protože je používáte pouze na nabídkách a jinými způsoby. Z tohoto důvodu je třeba je převést na normální kartu, než budete moci za ně zaúčtovat prodejní transakce.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží katalogu** a poté vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-how-catalog-item-numbers-are-converted-to-your-own-numbering"></a>Nastavení převodu čísla zboží katalogu na vlastní číslování
Chcete-li povolit konverzi karty zboží katalogu na kartu normálního zboží, musíte nejprve nastavit, jak bude číslování zboží prodejce převedeno na váš vlastní formát čísla zboží.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení zboží katalogu** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby.

## <a name="to-convert-a-catalog-item-to-a-normal-item"></a>Převod zboží katalogu na normální
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží katalogu** a poté vyberte související odkaz.
2. Otevřete kartu pro zboží katalogu, které chcete převést na normální.
3. V okně **Karty zboží katalogu** vyberte akci **Vytvořit zboží**.

Vytvoří se nová karta zboží, která je předem vyplněna informacemi ze zboží katalogu a příslušné šablony zboží. Můžete vyplnit nebo upravit pole na nové kartě zboží podle potřeby. Pro více informací navštivte [Registrace nového zboží](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item"></a>Prodej zboží katalogu a převod na normální zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Zvolte akci **Nový**. Vyplňte pole na záložce **Obecné** jako u každé prodejní objednávky. Pro více informací navštivte [Prodej zboží](sales-how-sell-products.md).
3. Na novém Prodejním řádku v poli **Typ** vyberte **zboží**, ale pole **Číslo** ponechte prázdné.
4. Vyberte akci **Řádek** a poté vyberte akci **Vybrat zboží katalogu**.

    Zboží katalogu je převedeno na normální zboží. Vytvoří se nová karta zboží, která je předem vyplněna informacemi ze zboží katalogu a příslušné šablony zboží.
5. V okně **Zboží katalogu** vyberte zboží katalogu, které chcete prodat a potom vyberte tlačítko **OK**.
6. Po dokončení prodejní objednávky zvolte akci **Zaúčtovat**.

Můžete vyplnit nebo upravit pole na nové kartě zboží podle potřeby. Pro více informací navštivte [ Zaregistrování nového zboží](inventory-how-register-new-items.md).

> [!NOTE]  
>   Záznam křížového odkazu zboží je automaticky vytvořen pro dodavatele zboží mezi číslem zboží dodavatele a novým číslem zboží. Pro více informací navštivte [Použití křížových odkazů zboží](inventory-how-use-item-cross-refs.md).

## <a name="see-also"></a>Viz také
[Registrace nového zboží](inventory-how-register-new-items.md)  
[Vytvoření zvláštních objednávek](sales-how-to-create-special-orders.md)|  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
