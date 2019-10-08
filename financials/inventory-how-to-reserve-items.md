---
title: Jak rezervovat zboží | Microsoft Docs
description: 'Můžete si rezervovat zboží pro prodejní objednávky, nákupní objednávky a výrobní objednávky. Zboží můžete rezervovat ve skladu nebo jako vstup na otevřených řádcích dokladů.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/14/2017
ms.author: sgroespe
---
# <a name="reserve-items"></a>Rezervace zboží
Můžete si rezervovat položky pro prodejní, nákupní, servisní, montážní a výrobní objednávky. Zboží můžete rezervovat ve skladu nebo jako vstup na otevřených řádcích dokladů nebo deníků. Práce provádíte v okně **Rezervace**.

Každý řádek v okně **Rezervace**, který si otevřete pro rezervování zboží, zobrazuje informace o jednom typu řádku (prodej, nákup, deník) nebo položky skladu. Řádky popisují, kolik zboží je možné rezervovat z každého typu řádku nebo položky.

## <a name="to-reserve-items-for-sales"></a>Rezervace zboží k prodeji
Následující text popisuje, jak rezervovat zboží z prodejní objednávky. Kroky jsou podobné při objednávkách nákupu, servisu i montáže.  
1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Prodejní objednávky** a pak vyberte související odkaz.  
2.  Na prodejní objednávce vyberte na záložce **Řádky** funkci **Rezervovat**. Otevře se okno **Rezervace**.  
3. Vyberte řádek, ze kterého chcete zboží rezervovat.  
4. Vyberte jednu z následujících akcí.  

    |**Funkce**|**Popis**|
    |------------------|---------------------|  
    |**Auto rezervace**|Automatická rezervace položek v okně **Rezervace**.|  
    |**Rezerva z aktuálního řádku**|Chcete-li rezervovat zboží z dokladu na vybraném řádku.|  
    |**Zrušení Rezervace z aktuálního řádku**|Chcete-li zrušit rezervovat zboží z dokladu na vybraném řádku.|

> [!NOTE]  
>  Pokud existují řádky sledovaného zboží pro prodejní objednávku, rezervační systém vás provede zvláštními kroky. Pro více informací navštivte „Rezervace konkrétního sériového čísla nebo čísla šarže“.  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Rezervace zboží pro řádek výrobní zakázku  
Můžete si objednat zboží pro výrobní zakázky. Musíte rozlišovat mezi řádky výrobní zakázky, což znamená nadřazeným zbožím, a komponenty výrobní zakázky.

V následujícím postupu je použita pevně plánovaná výrobní zakázka.   
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Pevně plánovaná výr.zakázka** a pak vyberte související odkaz.  
2. Otevřete pevně plánovanou výrobní zakázku, pro kterou chcete rezervovat nadřazené zboží.  
3. Vyberte příslušný řádek výrobní zakázky.  
4. Na záložce **Řádky** vyberte funkci **Rezervace**.
5. V okně **Rezervace** vyberte řádek **Prodejní řádek, Objednávka** a poté vyberte akci **Rezervace z akt.řádku**.  

Množství, které jste zadali do řádku pevně plánované výrobní zakázky, je nyní rezervováno.

## <a name="to-reserve-items-for-production-order-components"></a>Rezervace zboží pro komponenty výrobní zakázky  
Můžete si objednat zboží pro výrobní zakázky. Musíte rozlišovat mezi řádky výrobní zakázky, což znamená nadřazeným zbožím, a komponenty výrobní zakázky.

V následujícím postupu je použita pevně plánovaná výrobní zakázka.    
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Pevně plánovaná výr.zakázka** a pak vyberte související odkaz.  
2. Otevřete pevně plánovanou výrobní zakázku, pro kterou chcete rezervovat komponenty zboží.  
3. Vyberte příslušný řádek výrobní zakázky.  
4. Na záložce **Řádky** vyberte **Řádek** a pak vyberte **Komponenty**.  
5. Vyberte příslušný řádek komponenty.  
6. Na záložce **Řádky** vyberte funkci **Rezervace**.  
7. V okně **Rezervace** vyberte řádek a poté vyberte akci **Rezervace z akt.řádku**.  

Množství, které jste zadali do řádku pevně plánované výrobní komponenty, je nyní rezervováno.

## <a name="to-change-a-reservation"></a>Změna rezervace  
Někdy můžete chtít změnit rezervaci zboží.   
1. Z řádku dokladu, ze kterého jste si rezervovali zboží, vyberte na záložce **Řádky** akci **Rezervovat**.  
2. V okně **Rezervace** vyberte akci **Položky rezervace**.
3. V okně **Položky rezervace** aktualizujte pole **Množství** na řádku, který chcete změnit.
4. Potvrďte následnou zprávu stisknutím tlačítka **OK**.

## <a name="to-cancel-a-reservation"></a>Zrušení rezervace  
Někdy můžete chtít zrušit rezervaci zboží.   
1. Z řádku dokumentu, ze kterého chcete zrušit rezervaci, vyberte na záložce **Řádky** akci **Rezervace**.  
2. V okně **Rezervace** vyberte akci **Položky rezervace**.  
3.  V okně **Položky rezervace** vyberte akci **Zrušení Rezervace**.  
4.  Potvrďte následnou zprávu stisknutím tlačítka **OK**.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Rezervace konkrétního sériového čísla nebo čísla šarže  
Z odchozích dokladů pro sledované položky, jako jsou prodejní objednávky nebo seznamy produkčních komponent, si můžete vyhradit konkrétní sériová čísla nebo čísla šarže. To může být relevantní, například, pokud potřebujete výrobní komponenty z konkrétní šarže, aby byla zajištěna konzistence s dřívějšími výrobními šaržemi, nebo protože zákazník požádal o specifické sériové číslo. Pro více informací navštivte [Práce se sériovými čísly a čísly šarže](inventory-how-work-item-tracking.md).

Toto je označováno jako konkrétní rezervace, protože si rezervujete z množství zboží X, které patří do šarže X. Pokud jednoduše rezervujete z množství zboží X, pak je to normální, nespecifická rezervace. Pro více informací navštivte [Podrobnosti návrhu - Sledování a rezervace zboží](design-details-item-tracking-and-reservations.md).

Následující postup je založen na prodejní objednávce.    
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Prodejní objednávky** a pak vyberte související odkaz.  
2. Vytvořte řádek prodejní objednávky pro sledované zboží.  
3. Přiřaďte sériové číslo a číslo šarže k řádku prodejní objednávky. Pro více informací navštivte [Práce se sériovými čísly a čísly šarže](inventory-how-work-item-tracking.md).
4. Na řádku prodejní objednávky vyberte funkci **Rezervace**.  
5. Chcete-li rezervovat konkrétní sériová čísla nebo čísla šarže, zvolte tlačítko **Ano**.  
6. V okně **Přehled sledování zboží** vyberte kombinaci sériového čísla a čísla šarže, kterou jste právě přiřadili.  
7. Klepnutím na tlačítko **OK** otevřete okno **Rezervace**, kde je uvedena pouze dodávka se sledovaným číslem zboží. Pokud existují nějaké nespecifické rezervace na kterémkoli z čísel sledovaných zboží, které jste pro tento řádek zadali, budete informováni o množství, které již bylo rezervováno.  
8. Vyberte akci **Auto rezervace** nebo **Rezervace z akt.řádku** a vytvořte rezervaci na konkrétních číslech sledovaného zboží.

## <a name="see-also"></a>Viz také
[Zásoby](inventory-manage-inventory.md)  
[Podrobnosti o designu: Rezervace, sledování objednávek a správy akcí](design-details-reservation-order-tracking-and-action-messaging.md)  
[Podrobnosti návrhu - Trasování zboží a Rezervace](design-details-item-tracking-and-reservations.md)  
[Práce se sériovými čísly a čísly šarží](inventory-how-work-item-tracking.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
