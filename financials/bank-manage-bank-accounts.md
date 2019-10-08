---
title: Správa Bankovních účtů | Microsoft Docs
description: Musíte pravidelně odsouhlasovat položky účetních položek ve finančním sektoru se souvisejícími bankovními transakcemi na bankovních účtech.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
---
# <a name="managing-bank-accounts"></a>Správa bankovních účtů
V pravidelných intervalech musíte odsouhlasit bankovní položky v [!INCLUDE [d365fin](includes/d365fin_md.md)] se souvisejícími bankovními transakcemi na bankovních účtech u vaší banky a pak musíte zaúčtovat zůstatek na vašem bankovním účtu. Tuto úlohu můžete provést jako součást zpracování plateb uvedených v bankovním výpisu v **Deník odsouhlasení plateb**. Případně můžete úlohu provádět odděleně od zpracování plateb v **Odsouhlasení bankovních účtů**, které podporuje kontrolu položek knihy. V obou případech vyplníte okna importováním bankovního výpisu do [!INCLUDE [d365fin](includes/d365fin_md.md)].

Někdy je třeba převést částky mezi bankovním účtem v [!INCLUDE [d365fin](includes/d365fin_md.md)] tak, aby odrážely převody ve vaší bance. Tento úkol provedete v okně **Finanční deník** různými způsoby v závislosti na měně finančních prostředků.

Než budete moci spravovat bankovní účty, musíte nastavit každý bankovní účet jako kartu bankovního účtu. Navíc musíte nastavit elektronické služby, které můžete použít pro import bankovních výpisů a export platebních souborů. Další informace naleznete v části [Nastavení bankovních účtů](bank-setup-banking.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| Viz | Také |
| --- | --- |
| Odsouhlaste bankovní účty v souvislosti se zpracováním plateb v okně **Deník odsouhlasení plateb**. |[Automatické aplikování plateb a odsouhlasení bankovních účtů](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Odsouhlaste bankovní účty, včetně položek v knize, jako samostatný úkol v okně **Odsouhlasení bankovních účtů**. |[Odsouhlasení bankovních účtů zvlášť](bank-how-reconcile-bank-accounts-separately.md) |
| Zaúčtování převodu mezi bankovními účty ve stejné měně nebo v různých měnách. |[Převod bankovních prostředků](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Viz také
[Nastavení bankovnictví](bank-setup-banking.md)  
[Správa pohledávek](receivables-manage-receivables.md)  
[Správa závazků](payables-manage-payables.md)    
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Hlavní obchodní funkcionality](ui-across-business-areas.md)  

## [!INCLUDE [d365fin](includes/free_trial_md.md)]  
## [!INCLUDE [d365fin](includes/training_link_md.md)]
