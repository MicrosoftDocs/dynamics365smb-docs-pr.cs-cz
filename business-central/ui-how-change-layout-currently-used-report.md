---
title: Změna vzhledu sestavy výběrem jiného rozvržení | Microsoft Docs
description: Pro sestavu můžete použít různá rozvržení a přepínat mezi nimi pro změnu vzhledu sestavy.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.date: 10/01/2018
ms.author: jswymer
---
# <a name="change-which-layout-is-currently-used-on-a-report"></a>Změna rozvržení, které se v sestavě aktuálně používá
V sestavě lze nastavit více než jedno rozvržení sestavy, které pak můžete podle potřeby přepínat.

V závislosti na rozvrženích, která jsou k dispozici pro sestavu, můžete zvolit použití vestavěného rozvržení sestavy typu RDLC, vestavěného rozvržení sestavy typu Word nebo vlastní rozvržení. Pro více informací o rozvržení sestav RDLC a Word, vestavěných a vlastních sestavách viz [Správa Rozvržení Sestav](ui-manage-report-layouts.md).

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>Pro změnu rozvržení použitého v sestavě
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výběr Rozvržení Sestav** a poté vyberte související odkaz.  
   Na stránce **Výběr rozvržení sestav** jsou uvedeny všechny sestavy dostupné pro společnost, která je uvedena v poli Společnost v horní části okna. Pole Vybrané rozvržení určuje rozvržení, které se aktuálně používá v sestavě.
2. Nastavte pole **Společnost** v horní části stránky na společnost, která obsahuje sestavu.
3. Chcete-li změnit rozvržení používané sestavou, nastavte pole **Vybrané rozvržení** v řádku seznamu pro sestavu na jednu z následujících možností:
   * RDLC (vestavěné), používá pro sestavu vestavěné rozvržení sestavy typu RDLC.
   * Word (vestavěné), používá pro sestavu vestavěné rozvržení sestavy typu Word.
   * Vlastní typ, používá v sestavě vlastní rozvržení.  
     Ve FactBoxu rozvržení sestavy můžete vidět, jaká vlastní rozvržení jsou pro sestavu k dispozici. Pokud pro sestavu neexistují žádná vlastní rozvržení, musíte nejprve nějaké vytvořit. Pokud zvolíte tuto možnost, přejděte k dalšímu postupu pro zvolení vlastního rozvržení, které chcete použít.

    > [!NOTE]  
    >   Pokud zvolíte **RDLC (vestavěné)** nebo **Word (vestavěné)** a zobrazí se chybová zpráva, že sestava nemá rozvržení zadaného typu, musíte zvolit jinou možnost rozvržení nebo vytvořit vlastní rozvržení sestavy pro typ, který chcete použít.

Pokud jste vybrali vestavěné rozvržení sestav RDLC nebo Word, nebude vyžadována žádná další akce a rozvržení bude použito při příštím spuštění sestavy.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Pro nastavení vlastního rozvržení v sestavě
1. Na stránce **Vlastní rozvržení sestav** určíte, které vlastní rozvržení se má v sestavě použít. Pokud není stránka **Vlastní rozvržení sestav** otevřena, vyberte v poli **Popis rozvržení sestavy** vyhledávací tlačítko.
2. Na stránce **Vlastní rozvržení sestav** vyberte řádek pro vlastní rozvržení, které chcete použít, a poté zavřete stránku.

Vrátíte se na stránku **Výběr rozvržení sestav**. Název vybraného vlastního rozvržení se zobrazí v poli **Popis vlastního rozvržení**. Vlastní rozvržení bude použito při příštím spuštění sestavy.

## <a name="see-also"></a>Viz také
[Správa Rozvržení Sestav](ui-manage-report-layouts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
