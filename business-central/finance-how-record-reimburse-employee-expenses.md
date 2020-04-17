---
title: Record and Reimburse Employees' Business-Related Expenses | Microsoft Docs
description: Post employees' expenses with the general journal to the employee's account and later post a payment to the employee's bank account to reimburse for the business-related expense.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 10/01/2019
ms.author: sgroespe

---
# Evidence a uhrazení výdajů zaměstnance
[!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje transakce pro zaměstnance stejným způsobem jako u dodavatelů. V souladu s tím existují účto skupiny zaměstnanců, aby bylo zajištěno, že položky zaměstnance jsou zaúčtovány na příslušné účty v hlavní knize.

> [!NOTE]
> Zaměstnanecké transakce lze účtovat pouze v místní měně. Úhrady zaměstnancům nepodporují slevy a odchylky plateb.

Pokud zaměstnanci utratí své vlastní peníze během obchodní činnosti, můžete zaúčtovat výdaje na účet zaměstnance. Poté můžete zaměstnanci uhradit platbu na bankovní účet zaměstnance, podobně jako platíte dodavatelům.

## Evidence výdajů zaměstnance
Výdaje zaměstnanců účtujete na stránce **Finanční deník**.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky** a poté vyberte související odkaz.
2. Otevřete příslušný list finančního deníku. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).
3. V novém řádku deníku vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Opakujte krok 3 pro všechny výdaje, které zaměstnanec vynaložil.

   > [!TIP]
   > Pokud chcete zadat více řádků výdajů nad jedním řádkem zůstatkového účtu pro bankovní účet zaměstnance, potom zaškrtněte políčko **Navrhnout vyrovnávací částku** na řádku pro vaši dávku na stránce **Listy finančního deníku**. Poté je pole **Částka** na řádku rozvahového účtu automaticky vyplněno hodnotou, která je nutná k vyrovnání nákladů.
5. Chcete-li evidovat výdaje na účet zaměstnance, vyberte akci **Účtovat**.

## Proplacení nákladů zaměstnance
Zaměstnancům proplácíte náklady účtováním plateb na jejich bankovní účet na stránce **Deník plateb**.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky plateb** a poté vyberte související odkaz.
2. Otevřete příslušný list deníku plateb. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).
3. Podle potřeby vyplňte pole. Pro více informací navštivte [Provádění plateb](payables-make-payments.md).
4. Alternativně můžete vybrat akci **Návrh platby zaměstnance** chcete-li automaticky vložit řádky deníku pro nevyřízené náhrady zaměstnanců.
5. Vyberte akci **Účtovat** a zaznamenejte úhradu.

## Odsouhlasení úhrad se záznamy zaměstnanců
Platby zaměstnancům použijete na jejich související otevřené položky účetní knihy stejným způsobem jako u plateb dodavatelům, například na stránce **Deník odsouhlasení plateb** na základě souvisejících záznamů v bankovních výpisech. Pro více informací navštivte [Automatické použití plateb a odsouhlasení bankovních účtů](receivables-apply-payments-auto-reconcile-bank-accounts.md). Případně to můžete převést ručně na stránce **Záznamy zaměstnanců**. Pro více informací navštivte [Odsouhlasení platby dodavatele s deníkem plateb nebo z položek dodavatele](payables-how-apply-purchase-transactions-manually.md).

## Viz také
[Účtování transakcí přímo do hlavní knihy](finance-how-post-transactions-directly.md)  
[Práce s finančními deníky](ui-work-general-journals.md)  
[Účtování deníku storna a vrácení příjemky/dodávky](finance-how-reverse-journal-posting.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
