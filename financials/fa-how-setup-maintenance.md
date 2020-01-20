---
title: Nastavení údržby Dlouhodobého majetku | Microsoft Docs
description: 'Chcete-li spravovat opravy a servis dlouhodobého majetku, určíte obecné informace o údržbě, kódy pro typ práce a účet pro účtování pro náklady.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'repair, service'
ms.date: 06/02/2017
ms.author: sgroespe
---
# <a name="set-up-fixed-asset-maintenance"></a>Nastavení údržby dlouhodobého majetku
Ke správě údržby dlouhodobého majetku musíte nejprve nastavit nějaké obecné informace o údržbě, účet pro zaúčtování nákladů údržby a kódy údržby pro typy práce, jako je např. služba rutiny nebo oprava.

## <a name="to-set-up-general-maintenance-information"></a>Nastavení obecných informací o údržbě
Pokud nastavíte pole pro údržbu, můžete účtovat výdaje za údržbu z deníku dlouhodobého majetku.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), vstupte do **Dlouhodobý majetek** a poté vyberte související odkaz.
2. Vyberte dlouhodobý majetek, pro který chcete definovat pojistné krytí, a pak vyberte akci **Upravit** .
3. Na pevné záložce **Údržba** vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Pro nastavení kódů údržby
Když účtujete náklady na údržbu z obecného deníku, vyplníte pole **Kód údržby** k zaznamenání, k jaké údržbě došlo, např. služba rutiny nebo oprava.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), vstupte do **Údržba** a poté vyberte související odkaz.
2. V okně **Údržba** nastavte kódy pro různé typy údržbářských prací.

## <a name="to-set-up-maintenance-expense-accounts"></a>Nastavení účtů nákladů údržby
K účtování nákladů za údržbu musíte nejprve zvolit číslo účtu v okně **Účto skupiny DM**.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), vstupte do **Účto skupiny projektů** a poté vyberte související odkaz.
2. Vyplňte pole **Účet nákladů údržby** pro každou účto skupinu.

> [!NOTE]  
>   Chcete-li definovat, že náklady na údržbu jsou přidělovány oddělením nebo projektům, nastavte alokační klíče. Pro více informací navštivte [Nastavení obecných funkcí dlouhodobého majetku](fa-how-setup-general.md).

## <a name="see-also"></a>Viz také
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Dlouhodobý majetek](fa-manage.md)  
[Finance](finance.md)  
[Vítejte v [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
