---
title: Založení Bankovních účtů | Microsoft Docs
description: Můžete spárovat bankovní účty z výpisy z banky.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream'
ms.date: 09/26/2017
ms.author: sgroespe
---
# <a name="set-up-bank-accounts"></a>Nastavení bankovních účtů
Použití bankovní účtů v [!INCLUDE [d365fin](includes/d365fin_md.md)] slouží ke sledování vašich bankovních transakcí. Účty mohou být denominovány v místní měně nebo v cizí měně. Po nastavení bankovních účtů můžete použít také možnost kontroly tisku.

## <a name="to-set-up-bank-accounts"></a>Založení Bankovních účtů
1. Vyberte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "ikonu Vyhledat stránku nebo sestavu"), zadejte **Bankovní účty**a poté vyberte související odkaz.
2. V okně **Bankovní účty** vyberte akci **Nový**.
3. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Chcete-li vyplnit pole **Saldo** počáteční bilancí, musíte zaúčtovat položku bankovního účtu s danou částkou. Můžete to provést odsouhlasením bankovního účtu. Pro více informací běžte na [Odsouhlasení bankovních účtů separátně](bank-how-reconcile-bank-accounts-separately.md). Případně můžete počáteční stav implementovat jako součást vytváření obecných dat v nových společnostech pomocí nastavení asistovaného **Migrace dat**. Další informace naleznete v [Vítejte v [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md).

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a>Založení bankovního účtu pro import nebo export bankovních souborů.
Pole na záložce s náhledem **Transfer** v okně **Karta bankovního účtu** souvisejí s importem a exportem bankovních zdrojů a souborů. Další informace naleznete v [Nastavení služby převodu Bankovních dat](bank-how-setup-bank-data-conversion-service.md) a [Nastavení služby Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Vyberte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "ikonu Vyhledat stránku nebo sestavu"), zadejte **Bankovní účty**a poté vyberte související odkaz.
2. Otevřete kartu Bankovního účtu, který budete exportovat nebo importovat pomocí služby pro transfer bankovních dat.
3. Na záložce s náhledem **Transfer** vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Různé služby exportu souborů a jejich formáty vyžadují různé hodnoty nastavení v okně **Karta bankovního účtu** . Při pokusu o export souboru budete informováni o chybných nebo chybějících hodnotách nastavení. Proto si pozorně přečtěte krátký popis polí nebo se podívejte na související témata procedur. Například export platebního souboru pro severoamerický elektronický převod finančních prostředků (EFT) vyžaduje, aby byly vyplněny pole **Číslo posledního poukazu na úhradu** i pole **Číslo převodu**. Další informace naleznete v části [Export plateb do Bankovních dokladů](payables-how-export-payments-bank-file.md).

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a>Založení bankovního účtu pro export bankovních dokladů.
Pole na záložce s náhledem **Transfer** v okně **Karta bankovního účtu dodavatele** souvisejí s exportem bankovních prostředků a souborů. Další informace naleznete v [Nastavení služby převodu Bankovních dat](bank-how-setup-bank-data-conversion-service.md) a [Export plateb do Bankovních dokladů](payables-how-export-payments-bank-file.md).

1. Vyberte ikonu ![Vyhledat stránku nebo přehled](media/ui-search/search_small.png "ikonu Vyhledat stránku nebo přehled"), zadejte **Dodavatelé**a poté vyberte související odkaz.
2. Otevřete kartu dodavatele, jehož bankovní účet exportujete do bankovních souborů plateb.
3. Vyberte akci **Bankovní účty**.
4. V okně **Karta bankovního účtu dodavatele** na záložce s náhledem **Transfer** vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Viz také
[Nastavení bankovnictví](bank-setup-banking.md)  
[Správa bankovních účtů](bank-manage-bank-accounts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
