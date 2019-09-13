---
title: Jak trasovat sledované zboží | Microsoft Docs
description: 'Můžete vidět, kde bylo sledované zboží použito, včetně toho, jak a kdy bylo přijaté nebo vyrobené, přenesené, prodané, spotřebované nebo vrácené. V databázi najdete také všechny aktuální instance konkrétního sériového čísla nebo čísla šarže. To provedete pomocí funkce Trasování zboží a Navigace.'
services: project-madeira
documentationcenter: ''
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
# <a name="trace-item-tracked-items"></a>Trasování sledovaného zboží
Můžete vidět, kde bylo sledované zboží použito, včetně toho, jak a kdy bylo přijato nebo vyrobeno, přeneseno, prodáno, spotřebováno nebo vráceno. V databázi najdete také všechny aktuální instance konkrétního sériového čísla nebo čísla šarže. To provedete pomocí funkce Trasování zboží a Navigace.  

 Tyto funkce mohou být zvláště užitečné při kontrole kvality, když potřebujete zjistit, kteří zákazníci obdrželi produkty s konkrétním číslem šarže nebo když potřebujete zjistit, z které šarže pochází vadná komponenta.  

 Na stránce **Trasování zboží** můžete sledovat pořadí vpřed a vzad v sledu transakcí zaúčtovaných pro sériové číslo nebo číslo šarže.  

 Na stránce **Navigace** nevidíte sled transakcí, ale můžete vidět všechny záznamy sériového čísla nebo čísla šarže, jak zaúčtované položky, tak otevřené záznamy.  

 Tyto dvě funkce lze použít v kombinaci transferem sledovaného sériového čísla nebo čísla šarže na stránku **Navigace** a dokončit tak kompletní scénář sledování. Pro více informací navštivte  [Návod:  Sledování sériových čísel nebo čísel šarže](walkthrough-tracing-serial-lot-numbers.md).  

## <a name="to-trace-item-tracked-items"></a>Trasování zboží  

1.  Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Trasování zboží** a poté vyberte související odkaz.  
2.  Do polí filtru v horní části stránky zadejte čísla konkrétních zboží nebo filtr na čísla zboží, které chcete sledovat.  
3.  V poli **Zobrazit komponenty** vyberte, zda chcete také zjistit, odkud komponenty pocházejí. Vaše možnosti v tomto poli jsou následující.  

    |Pole|Popis|  
    |----------------------------------|---------------------------------------|  
    |**Žádné**|Tuto možnost vyberte, pokud nechcete vidět žádné součásti.|  
    |**Se sledováním zboží**|Tuto možnost vyberte, pokud chcete vidět pouze komponenty, které mají číslo šarže nebo sériové číslo.|  
    |**Vše**|Tuto možnost vyberte, pokud chcete vidět všechny komponenty.|  

4.  V poli **Metoda sledování** vyberte metodu, kterou chcete použít pro trasování položky. Možnosti jsou následující  

    |Pole|Popis|  
    |----------------------------------|---------------------------------------|  
    |**Použití -> Původ**|Tato metoda sleduje zboží od místa, kde bylo použité do místa, odkud pochází. Například, pokud bylo vyrobené zboží prodáno zákazníkovi, stránka **Trasování zboží** zobrazí nejprve řádek prodejní dodávky, který pak můžete rozbalit a zjistit, ze které výrobní zakázky přišla.|  
    |**Původ -> Použití**|Tato metoda sleduje zboží od místa původu v zásobách do místa, kde bylo použito. Například, pokud bylo vyrobené zboží prodáno zákazníkovi, stránka **Trasování zboží** zobrazí nejprve hotovou výrobní objednávku, kterou pak můžete rozbalit a zobrazit prodejní dodávky, kde bylo zboží použito.|  

5.  Vyberte akci **Sledovat** pro spuštění sledování.  

> [!NOTE]  
>  Pokud jste obdrželi stejnou šarži u více transakcí, nemusí stránka **Trasování zboží** zobrazit všechny transakce. Zobrazeny jsou pouze použité transakce.  

> [!NOTE]  
>  Pokud již byla další trasa transakcí pod řádkem trasování zboží sledována jiným řádkem nad ní, je zaškrtnuto políčko **Již sledováno**. Pro zajištění jednoduššího pohledu nejsou takové řádky zobrazeny.  
>   
>  Chcete-li najít řádky pro trasování zboží, kde již byla sledována historie transakcí, zvolte tlačítko **Jít na Již-sledované**. Je vybrán příslušný řádek pro sledování zboží a všechny podkladové řádky jsou rozbaleny.  

## <a name="to-find-item-tracked-items-with-navigate"></a>Hledání zboží pomocí Navigace  

1.  Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Navigace** a poté vyberte související odkaz.  
2.  Na záložce **Sledování zboží** zadejte do polí **Sériové číslo** a **Číslo šarže** sledovací čísla zboží, která chcete sledovat.  
3.  Vyberte akci **Najít** a najděte všechny instance sériového čísla nebo čísla šarže v databázi.  

## <a name="see-also"></a>Viz také  
[Zásoby](inventory-manage-inventory.md)  
[Podrobnosti o designu: Trasování zboží](design-details-item-tracking.md)
[Podrobnosti návrhu - Trasování zboží a Rezervace](design-details-item-tracking-and-reservations.md)  
[Rezervace zboží](inventory-how-to-reserve-items.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Návod: Sledování zboží označeného sériovými čísly nebo čísly šarže](walkthrough-tracing-serial-lot-numbers.md)
