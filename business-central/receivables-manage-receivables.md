---
title: Overview of Tasks to Manage Receivables | Microsoft Docs
description: Outlines tasks to manage receivables and apply payments to customer or vendor ledger entries.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 01/13/2020
ms.author: sgroespe

---
# Správa pohledávek
Pravidelným krokem v jakémkoli finančním cyklu je odsouhlasení bankovních účtů, které vyžadují, abyste k uzavření zaplacených prodejních faktur a nákupu dobropisů použili na položky zákazníků nebo prodejců příchozí platby.

Zatímco většina zákazníků v prostředích B2B zaplatí nějaký čas po dodání a ponechá zaúčtované prodejní faktury otevřené oddělení účtů pohledávek po přijetí platby, některé prodejní faktury lze zaplatit okamžitě, například pomocí PayPal. Tyto faktury jsou okamžitě použity jako zaplacené, když jsou zaúčtovány, a proto se nezobrazují jako platby, které mají být zpracovány v AR. Pro více informací navštivte, například [Prodejní faktury](sales-how-invoice-sales.md).

V [!INCLUDE[d365fin](includes/d365fin_md.md)], je jedním z nejrychlejších způsobů jak zaregistrovat platby stránka **Deník odsouhlasení plateb** a to pomocí importu bankovního výpisu. Platby se aplikují na otevřené položky zákazníků nebo dodavatelů na základě datových shod mezi textem platby a vstupními informacemi. Před účtováním deníku si můžete shody zkontrolovat nebo změnit a při zaúčtování deníku uzavřít položky bankovního účtu pro položky hlavní knihy. Bankovní účet je odsouhlasen, když jsou uplatněny všechny platby.

Existují další stránky, kde můžete buď použít platby, nebo odsouhlasit bankovní účty:

* Stránka **Odsouhlasení bank. účtu**, kde odsouhlasíte bankovní účty porovnáním importovaných řádků bankovního výpisu s položkami bankovního účtu systému. Zde můžete také odsouhlasit platby šeku. Pro více informací navštivte [Odsouhlasení bankovních účtů](bank-how-reconcile-bank-accounts-separately.md). Zde nemůžete použít platby.
* Stránka **Registrace plateb**, kde můžete ručně použít platby přijaté jako hotovost, šek nebo bankovní transakci na vygenerovaný seznam nezaplacených prodejních dokladů. Všimněte si, že tato funkce je k dispozici pouze pro prodejní doklady. Zde nemůžete použít odchozí platby a nemůžete tedy odsouhlasit bankovní účty.
* Na stránce **Deníky přijaté hotovosti**, kde ručně účtujete příjmy na příslušnou hlavní knihu, zákazníka nebo jiný účet zadáním platebního řádku. Příjem nebo refundaci můžete vyrovnat na jednu nebo více otevřených položek před zaúčtováním deníku přijaté hotovosti nebo z položek zákazníka. Zde nelze odsouhlasit bankovní účty.

**Deník odsouhlasení plateb** a stránka **Odsouhlasení bankovního účtu** používají logiku automatického párování, kterou můžete nastavit na stránce **Pravidla vyrovnání plateb**. Pro více informací navštivte [Nastavení pravidel pro automatické vyrovnání plateb](receivables-how-set-up-payment-application-rules.md).

Mezi další aspekty správy pohledávek patří shromažďování neuhrazených zůstatků, včetně finančních poplatků a upomínek, a nastavení bankovních účtů, aby bylo možné automaticky vybírat platby z jejich účtu.

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| Pro | Navštivte |
| --- | --- |
| Použijte platby k otevření záznamů odběratelů nebo dodavatelů na základě importovaného souboru výpisu nebo zdroje a při použití všech plateb sjednejte bankovní účet. | [Automatické vyrovnání plateb a odsouhlasení bankovních účtů](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Použijte platby k otevření položek zákazníka na základě seznamu nezaplacených prodejních dokladů na stránce **Platební registrace**. | [Odsouhlasení plateb zákazníků ze seznamu nezaplacených prodejních dokladů](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Účtujte příjemky nebo refundace zákazníkům v deníku přijaté hotovosti a použijte je na položky zákazníků, buď z deníku, nebo ze zaúčtovaných položek. | [Odsouhlasení plateb zákazníků s deníkem přijaté hotovosti nebo z položek zákazníka](receivables-how-apply-sales-transactions-manually.md) |
| Připomeňte zákazníkům částky po splatnosti, vypočítejte úroky a finanční náklady a spravujte pohledávky. | [Inkaso nevyrovnaných zůstatků](receivables-collect-outstanding-balances.md) |
| Se souhlasem zákazníka inkasujte platby přímo z jeho bankovního účtu, pouze v měně euro. | [Sběr plateb pomocí SEPA – příkaz k inkasu](finance-collect-payments-with-sepa-direct-debit.md) |
| Zablokujte zákazníka, aby nemohl být zadáván do dokumentů nebo účtován, například z důvodu platební neschopnosti. | [Blokace zákazníků](receivables-how-block-customers.md) |
| Ujistěte se, že znáte náklady zaslaných položek přiřazením dodatečných nákladů na položky, jako jsou náklady na dopravu, fyzickou manipulaci, pojištění a dopravu, které vám vzniknou po prodeji. | [Použít poplatky za zboží na účet pro dodatečné obchodní náklady](payables-how-assign-item-charges.md) |
| Nastavte toleranci, podle které systém uzavře fakturu, i když platba, včetně jakékoli slevy, nepokrývá celou částku faktury. | [Práce s odchylkami plateb a skont](finance-payment-tolerance-and-payment-discount-tolerance.md) |
| Předpovídejte, kdy budou platby za prodejní doklady provedeny pozdě. | [Předpovědi pozdních plateb](ui-extensions-late-payment-prediction.md) |

## Viz související kurzy na [Microsoft Learn](/learn/paths/process-customer-vendor-payments-dynamics-365-business-central/)

## Viz také
[Prodej](sales-manage-sales.md)  
[Správa závazků](payables-manage-payables.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
