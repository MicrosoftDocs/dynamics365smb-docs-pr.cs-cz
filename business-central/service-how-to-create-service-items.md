---
title: Vytváření Předmětů servisu | Microsoft Docs
description: 'Když obdržíte neevidované zboží pro servis, můžete jej evidovat jako předmět servisu.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="create-service-items"></a>Vytváření předmětů servisu
V [!INCLUDE[d365fin](includes/d365fin_md.md)] se termín „předmět servisu“ vztahuje na vybavení nebo zboží, které vyžaduje servis. Při vytváření servisní zakázky určíte zboží, které vyžaduje servis. V zakázce můžete propojit předmět servisu se zbožím v zásobách nebo se skupinou předmětů servisu.    

Když obdržíte zboží, které vyžaduje servis, můžete jej zaevidovat jako předmět servisu. Toho lze dosáhnout několika způsoby. Například můžete vytvořit předmět servisu na stránce **Předměty servisu**, nebo v rámci jiného procesu, například při práci se servisní zakázkou.   

## <a name="to-create-a-service-item"></a>Vytvoření předmětu servisu  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Předměty servisu** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Vytvoření předmětů servisu uvnitř servisní zakázky  
Když obdržíte zboží, které chcete zaregistrovat jako předměty servisu, na servis, můžete jej vytvořit jako předměty servisu na stránkách **Servisní zakázky** nebo **Nabídka servisu**.  

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Servisní zakázky** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Zvolte akci **Vytvořit předmět servisu**.  

    K předmětu servisu je přiřazeno číslo a je vytvořena karta předmětu servisu. Pole **Číslo předmětu servisu** je vyplněno číslem nového předmětu servisu.

## <a name="to-create-a-service-item-when-shipping-items"></a>Vytvoření předmětu servisu při dopravě zboží  
Při odeslání zboží zaúčtováním buď servisních zakázek nebo servisních faktur, je expedované zboží automaticky zaregistrováno jako předměty servisu, pokud je splněna následující podmínka. Položky musí patřit do skupiny předmětů servisu se zaškrtnutým políčkem **Vytvořit položku servisu**. Pokud má zboží registrovaná sériová čísla na stránce řádků sledování zboží, jsou tyto informace při vytváření předmětů servisu zkopírovány automaticky do pole **Sériové číslo**.  

Následující postup ukazuje, jak vytvořit předměty servisu při odeslání zboží v rámci servisní zakázky.  

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Servisní zakázky** a poté vyberte související odkaz.  
2. Otevřete příslušnou servisní zakázku.  
3. Zvolte akci **Účtovat** nebo **Účtovat a Vytisknout**.  
4. Zvolte akci **Odeslat** nebo **Odeslat a fakturovat**.  
5. Předměty servisu jsou automaticky vytvořeny pro zboží v zakázce za předpokladu, že patří do skupiny předmětů servisu, kterou jste nastavili pro vytváření předmětů servisu. Pokud jste zaregistrovali konkrétní sériová čísla na stránce **Řádky sledování zboží**, budou přiřazena k těmto předmětům servisu.  

> [!NOTE]  
>  Pokud je položka kusovník a rozbalili jste ho, jsou rozbalené položky kusovníku zpracovány stejným způsobem jako běžné zboží. Předměty servisu jsou vytvářeny na základě podmínky skupiny předmětů servisu, případně podmínky sériových čísel. Navíc, pokud je předmět servisu vytvořen pro rozbalenou položku kusovníku, která je tvořena jinými komponenty kusovníku, jsou tyto položky vytvořeny jako komponenty předmětu servisu pro rozbalený předmět servisu kusovníku.  
>   
>  Pokud je zboží kusovník a nemáte rozbalený kusovník, vytvoří se pro něj předmět servisu na základě podmínky skupiny předmětů servisu, případně podmínky sériových čísel.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Vložení počátečního poplatku k předmětu servisu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Servisní úlohy** a poté vyberte související odkaz.
2. Zvolte akci **Sešit předmětu servisu**.
3. Zvolte řádek servisu, poté zvolte **Akce**, vyberte **Funkce**, a následně akci **Vložit poč.poplatek**.  

    S počátečním poplatkem je vložen servisní řádek typu **Náklady**. Počáteční poplatek se vztahuje na vybraný předmět servisu.

## <a name="see-also"></a>Viz také  
[Nastavení Předmětů servisu a Komponent předmětů servisu](service-how-setup-service-items.md)  
[Nastavení Správy servisu](service-setup-service.md)  
[Správa servisu](service-service.md)  
