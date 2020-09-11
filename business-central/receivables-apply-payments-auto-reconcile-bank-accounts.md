---
title: Reconcile Bank Accounts and Apply Payments | Microsoft Docs
description: Outlines tasks to reconcile your bank, receivables, and payables accounts, post cash receipts or expenses, and apply payments automatically.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2020
ms.author: sgroespe

---
# Automatické vyrovnávání plateb a odsouhlasení bankovních účtů
Musíte pravidelně sladit své bankovní účty, pohledávky a závazky použitím plateb evidovaných v bance s jejich souvisejícími otevřenými (nezaplacenými) fakturami a dobropisy nebo jinými otevřenými položkami v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Tuto úlohu můžete provést na stránce **Deníky odsouhlasení plateb** například importem bankovního výpisu nebo zdroje pro rychlou evidenci plateb. Platby jsou vyrovnány s otevřenými položkami zákazníků nebo dodavatelů na základě shod mezi textem platby a informacemi o položce. Před zaúčtováním deníku můžete zkontrolovat a změnit vyrovnání aplikace. Při zaúčtování deníku můžete zavřít všechny otevřené položky bankovního účtu související s vyrovnanými položami. Bankovní účet je automaticky vyrovnán, když jsou vyrovnány všechny platby.

Logika, která řídí způsob, jakým je text platby automaticky spárován s informacemi o položce, se nastavuje na nastránce **Pravidla vyrovnání plateb** jako pravidla s prioritou, které se dají upravit.

Můžete také odsouhlasit bankovní účty bez současného vyrovnání plateb. To provedete na stránce **Odsouhlasení bankovního účtu**. Pro více informací navštivte [Odsouhlasení bankovních účtů](bank-how-reconcile-bank-accounts-separately.md).

Chcete-li importovat bankovní výpisy jako bankovní zdroj, musíte nejprve nastavit a povolit službu Envestnet Yodlee Bank Feed a poté propojit své bankovní účty se souvisejícími online bankovními účty. Pro více informací běžte na [Nastavení služby Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md).

Případně můžete použít rozšíření AMC Banking 365 Fundamentals k převodu bankovního výpisu z libovolného formátu na datový typ, který můžete importovat do [!INCLUDE[d365fin](includes/d365fin_md.md)]. Další informace naleznete v části [Používání rozšíření AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| Viz | Také |
| --- | --- |
| Využití vyrování plateb k otevření položek zákazníků nebo dodavatelů importem bankovního výpisu a odsouhlasení bankovních účtů po vyrovnání všech plateb. | [Odsouhlasení plateb pomocí automatického vyrovnání](receivables-how-reconcile-payments-auto-application.md) |
| Ruční vyrovnání plateb prohlížením podrobných informací spojených dat a návrhy a doporučení pro otevřené položky, které se mají vyrovnat. | [Kontrol nebo vyrovnání plateb po automatickém vyrovnání](receivables-how-review-apply-payments-auto-application.md) |
| Vyřešte platby, které nelze automaticky vyrovnat na souvisejících položkách účetní knihy. Například proto, že částky se liší nebo protože související položka knihy neexistuje. | [Odsouhlasení plateb, které nemohou být vyrovnány automaticky](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| Propojte text plateb s konkrétními účty zákazníka, dodavatele nebo hlavní knihy tak, aby vždy zaúčtoval opakované příjmy v hotovosti nebo výdaje na tyto účty, pokud neexistují žádné doklady, na které by se vztahovaly. | [Namapovaný text o opakovaných platbách na účtech pro automatické odsouhlasení.](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |
| Nastavte pravidla, která určují, jak mají být platby/bankovní transakce automaticky vyrovnány s jejich souvisejícími otevřenými položkami při použití funkce **Vyrovnat automaticky** na stránce **Deník odsouhlasení plateb**. | [Nastavení pravidel pro automatické vyrovnání plateb](receivables-how-set-up-payment-application-rules.md) |

## Viz souvisejnící školení [Microsoft Learn](/learn/modules/use-journals-dynamics-365-business-central/index)

## Viz také
[Odsouhlasení bankovních účtů](bank-how-reconcile-bank-accounts-separately.md)  
[Správa pohledávek](receivables-manage-receivables.md)  
[Proej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
