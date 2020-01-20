---
title: Nastavení rozsahu dat v Business Central | Microsoft Docs
description: 'Zjistěte, jak získat přehled pro zobrazení dat z konkrétních časových období použitím rozsahu dat v Business Central.'
documentationcenter: ''
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'dates, reporting, filter'
ms.date: 05/29/2017
ms.author: edupont
---
# <a name="entering-date-ranges"></a>Zadávání rozsahu dat 
Můžete nastavit filtry obsahující počáteční a konečné datum tak, aby zobrazovaly pouze data obsažená v daném rozsahu dat nebo časovém intervalu. Pro nastavení rozsahu dat platí zvláštní pravidla. Vezměme si příklad **Nejlepších 10 zákazníků** :

![Nastavení rozsahu dat na stránce požadavku pro seznam 10 nejlepších zákazníků](./media/ui-enter-date-ranges/customer-top10-list.png)

Zde můžete omezit přehled na rozsah dat, jako jsou například poslední 2 týdny nebo celkově 6 týdnů, nebo libovolné časové období. Chcete-li nastavit rozsah dat, zadejte data, a poté použijte buď **..** Nebo **|** pro nastavení rozsahu. V našem příkladu byste pro zobrazení prvních 10 zákazníků za první dva týdny v květnu nastavili filtr dat na *05 01 17..05 14 17*.
Zde je několik dalších příkladů:

| Význam | Příklady: | Zahrnuté položky |
|---|---|---|
|Rovná se | 12 15 16 |Pouze ty zaúčtované 15. prosince 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Zaúčtováno v termínech mezi a včetně 15. prosince 2016 a 15. ledna 2017.<br /><br />Zaúčtováno 15. prosince 2016 nebo dříve.|
|Buď/nebo|12 15 16&#124;12 16 16|Zaúčtováno 15. prosince nebo 16. prosince 2016. Pokud jsou položky zaúčtované v obou dnech, zobrazí se všechny.|

Můžete také kombinovat různé typy formátů.

| Příklady: | Zahrnuté položky |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Položky zaúčtované buď 15. prosince 2016, nebo v období mezi a včetně 1. prosince 2016 a 31. května 2017. |
|..12 14 16&#124;12 30 16.. | Položky zaúčtované 14. prosince nebo dříve nebo položky zaúčtované 30. prosince nebo později - to značí všechny položky kromě těch, které byly zaúčtovány v termínech mezi a včetně 15. a 29. prosince.  |

Upozorňujeme, že jsme zde použili US formát dat MMDDYY. Jakmile bude [!INCLUDE [d365fin](includes/d365fin_md.md)] k dispozici na jiných trzích, budete moci používat formáty, na které jste zvyklí.

## <a name="see-also"></a>Viz také
[Práce s [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Zadávání kritérií ve filtrech ](ui-enter-criteria-filters.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)
