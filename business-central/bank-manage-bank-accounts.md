---
title: Správa Bankovních účtů | Microsoft Docs
description: Musíte pravidelně odsouhlasovat položky účetních položek se souvisejícími bankovními transakcemi na bankovních účtech.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="managing-bank-accounts"></a>Správa bankovních účtů
V pravidelných intervalech musíte odsouhlasit bankovní položky v [!INCLUDE[d365fin](includes/d365fin_md.md)] se souvisejícími bankovními transakcemi na bankovních účtech u vaší banky a pak musíte zaúčtovat zůstatek na vašem bankovním účtu. Tuto úlohu můžete provést jako součást zpracování plateb uvedených v bankovním výpisu v **Deník odsouhlasení plateb**. Případně můžete úlohu provést odděleně od zpracování platby, na kartě **Odsouhlasení bank. Účtu**, na které v levém podokně porovnáváte řádky s bankovními výpisy s položkami interních položek bankovních účtů v pravém podokně. Na obou stránkách můžete vyplnit informace o bankovním výpisu importem souboru a můžete použít návrhy automatického párování.

> [!NOTE]  
> V severoamerických verzích můžete bankovní odsouhlasení provádět také na **Odsouhlasení bank. účtu**. Stránka výkazu, která je vhodnější pro šeky a vklady, ale nenabízí import souborů výpisu z účtu. Pokud chcete používat tuto stránku **Odsouhlasení bank. účtu**, vypněte **Automatické odsouhlasení bank. účtu** pole Shoda na stránce **Nastavení financí**. Další informace naleznete v části „Odsouhlasit bankovní účty“ v části lokální funkce Spojených států.

Někdy je třeba převést částky mezi bankovním účtem v [!INCLUDE[d365fin](includes/d365fin_md.md)] tak, aby odrážely převody ve vaší bance. Tento úkol provedete na stránce **Finanční deník** různými způsoby v závislosti na měně finančních prostředků.

Než budete moci spravovat bankovní účty, musíte nastavit každý bankovní účet jako kartu bankovního účtu. Navíc musíte nastavit elektronické služby, které můžete použít pro import bankovních výpisů a export platebních souborů. Další informace naleznete v části [Nastavení bankovních účtů](bank-setup-banking.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, která je popisují.

| Viz | Také |
| --- | --- |
| Odsouhlasení bankovních účtů v souvislosti se zpracováním plateb v stránka **Deník odsouhlasení plateb**. |[Automatické aplikování plateb a odsouhlasení bankovních účtů](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Odsouhlaste bankovní účty, včetně položek v knize, jako samostatný úkol v stránka **Odsouhlasení bankovních účtů**. |[Odsouhlasení bankovních účtů zvlášť](bank-how-reconcile-bank-accounts-separately.md) |
| Zaúčtování převodu mezi bankovními účty ve stejné měně nebo v různých měnách. |[Převod bankovních prostředků](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Viz také
[Nastavení bankovnictví](bank-setup-banking.md)  
[Správa pohledávek](receivables-manage-receivables.md)  
[Správa závazků](payables-manage-payables.md)    
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Hlavní obchodní funkcionality](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
