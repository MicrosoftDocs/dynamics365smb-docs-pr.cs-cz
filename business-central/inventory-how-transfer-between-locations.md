---
title: Převod zboží mezi skladovými místy ve skladu | Microsoft Docs
description: 'Popisuje, jak přesunout zásoby z jednoho místa nebo skladu na jiné, buď pomocí deníku přeřazení, nebo pomocí objednávek transferu.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'move, warehouse'
ms.date: 03/01/2019
ms.author: SorenGP
---
# <a name="transfer-inventory-between-locations"></a>Převádění zásob mezi lokacemi
Skladové položky můžete převádět mezi lokacemi vytvořením objednávky transferu. Alternativně můžete použít deník přeřazení zboží.

U objednávky transferu odesíláte odchozí přenos z jedné lokace a obdržíte vstup transferu na jiné lokaci. To vám umožní spravovat činnosti související se skladováním a poskytuje větší jistotu, že množství zásob jsou správně aktualizována.

V deníku přeřazení jednoduše vyplňte pole **Kód lokace** a **Kód nové lokace**. Při účtování deníku se položky zboží upravují na příslušných lokacích. U této metody nejsou skladové aktivity řízeny.

> [!NOTE]  
>   Pokud máte zboží zaznamenané ve vašich zásobách bez lokalizačního kódu, například od doby, kdy jste měli pouze jeden sklad, nemůžete tyto položky převádět pomocí objednávky transferu. Místo toho musíte použít deník přeřazení k přeřazení zboží z prázdného kódu lokace do skutečného kódu lokace.  Pro více informací navštivte v kroku 3 [Přenos zboží pomocí deníku přeřazení zboží](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).

Chcete-li přenášet zboží, musí být nastaveny lokace a trasy transferu. Pro více informací navštivte [Nastavení lokací](inventory-how-setup-locations.md).

## <a name="to-transfer-items-with-a-transfer-order"></a>Přenos zboží pomocí objednávky transferu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Objednávky transferu** a poté vyberte související odkaz.
2. Na stránce **Objednávky transferu** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Pokud jste při nastavování trasy transferu vyplnili pole **Kód na cestě**, **Kód přepravce** a **Kód služby přepravce** na stránce **Detaily spec.transferu**, automaticky se vyplní odpovídající pole v objednávce transferu.

    Když vyplníte pole **Kód služby přepravce**, vypočítá se datum přijmu v převodu na místo připočtením doby odeslání kódu služby přepravce k datu odeslání.

    Jako pracovník skladu v převodu z lokace pokračujte v přepravě zboží.
3. Vyberte akci **Účtovat**, možnost **Dodat** a poté stiskněte tlačítko **OK**.

    Zboží je nyní přenášené mezi určenými lokacemi podle specifikovaných tras přenosu.

    Jako pracovník skladu ve skladu z převodu z lokace pokračujte v přijímání zboží.
4. Vyberte akci **Účtovat**, možnost **Příjem** a poté stiskněte tlačítko **OK**.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Přenos zboží pomocí deníku přeřazení zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky  přeřazení zboží** a poté vyberte související odkaz.
2. Na stránce **Deníku  přeřazení zboží** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Do pole **Kódu lokace** zadejte lokaci, kde je zboží aktuálně uložené.

    > [!NOTE]  
    >   Chcete-li přenést zboží, které nemají kód lokace, ponechte pole **Kód lokace** prázdné.
4. Do pole **Kód nové lokace** zadejte lokaci, do které chcete zboží přenést.
5. Zvolte akci **Zaúčtovat**.

## <a name="see-also"></a>Viz také
[Spravovat zásoby](inventory-manage-inventory.md)  
[Nastavení lokací](inventory-how-setup-locations.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
[Obecná obchodní funkcionalita](ui-across-business-areas.md)
