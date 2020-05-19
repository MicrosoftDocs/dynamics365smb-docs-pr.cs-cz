---
title: Nastavení pracovních výkazů a jejich schvalování | Microsoft Docs
description: 'Nastavujete pracovní výkazy pro zaznamenávání času spotřebovaného na projekty a použití zdrojů, které vám pomohou se správou projektů, správou zaměstnanců a kapacitou'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff, resource'
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="set-up-time-sheets"></a>Nastavení pracovních výkazů
Pracovní výkazy v [!INCLUDE[d365fin](includes/d365fin_md.md)] zpracovávají evidenci času v týdenních přírůstcích po sedmi dnech. Používáte je ke sledování času použitého na projekty a můžete je použít k záznamu jednoduché registrace času zdroje. Než budete moci používat pracovní výkazy, musíte je nejprve nastavit.

Poté, co jste nastavili, jak bude vaše organizace používat pracovní výkazy, můžete určit, zda a jak budou pracovní výkazy schválovány. V závislosti na potřebách vaší organizace můžete určit:

* Jednoho nebo více uživatelů jako správce pracovního výkazu a schvalovatele všech pracovních výkazů.
* Schvalovatele pracovního výkazu pro každý zdroj.

Pokud jste nastavili pracovní výkazy, můžete vytvořit pracovní výkazy pro zdroje, přiřadit je k řádkům plánování projektů a účtovat pracovní výkazy. Pro více informací navštivte [Použití pracovních výkazů](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Nastavení obecných informací pro pracovní výkazy
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Nastavení zdrojů**, a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. V poli **Schválení pracovního výkazu za projekt** vyberte jednu z následujících možností.

| Možnost | Popis |
| --- | --- |
| **Nikdy** |Uživatel v poli **ID schvalovatele pracovního výkazu** na kartě zdroje schvaluje pracovní výkaz. |
| **Vždy** |Uživatel v poli **Osoba odpovědná** na kartě projektu schvaluje pracovní výkaz. |
| **Pouze počítač** |Pokud je pracovní výkaz stroje spojen s projektem, schválí pracovní výkaz uživatel v poli **Osoba odpovědná** na kartě projektu. Pokud je časový rozvrh stroje spojen se zdrojem, pak pracovní výkaz schválí uživatel v poli **ID schvalovatele pracovního výkazu** na kartě zdroje. |

## <a name="to-assign-a-time-sheet-administrator"></a>Přiřazení správce pracovního výkazu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny uživatelů** a poté vyberte související odkaz.  
2. Přidejte nového uživatele, pokud seznam uživatelů nezahrnuje osobu, kterou chcete mít jako administrátora pracovního výkazu. Pro více informací navštivte [Správa uživatelů a oprávnění](ui-how-users-permissions.md).
3. Vyberte uživatele, který má být správcem pracovního výkazu, a poté zaškrtněte zaškrtávací políčko **Správce pracovního výkazu**.  

> [!TIP]  
>   Doporučujeme, abyste určili pouze jednoho uživatele, který bude administrátorem pracovního výkazu pro společnost. V následujícím postupu nastavíte vlastníka pracovního výkazu a schvalovatele, kde schvalovatel je přiřazen ke každému zdroji.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Pro přiřazení vlastníka pracovního výkazu a schvalovatele
1. Vyberte ikonu ![Žárovku, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Zdroje** a poté vyberte související odkaz.
2. Vyberte zdroj, pro který chcete nastavit schopnost používat pracovní výkazy, a poté zaškrtněte zaškrtávací políčko **Použij pracovní výkaz**.  
3. Do pole **ID vlastníka pracovního výkazu** zadejte ID vlastníka pracovního výkazu. Vlastník může do pracovního výkazu zadat využití času a odeslat jej ke schválení. Obecně platí, že pokud je zdrojem osoba, je tato osoba také vlastníkem.  
4. Do pole **ID schvalovatele pracovního výkazu**  zadejte ID schvalovatele pracovního výkazu. Schvalovatel může schválit, odmítnout nebo znovu otevřít pracovní výkaz.  

> [!NOTE]  
>   ID schvalovatele pracovního výkazu nelze změnit, pokud existují pracovní výkazy, které dosud nebyly zpracovány a mají stav **Odesláno** nebo **Otevřeno**.

## <a name="see-also"></a>Viz také
[Nastavení správy projektu](projects-setup-projects.md)  
[Správa projektu](projects-manage-projects.md)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)         
[Prodej](sales-manage-sales.md)      
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
