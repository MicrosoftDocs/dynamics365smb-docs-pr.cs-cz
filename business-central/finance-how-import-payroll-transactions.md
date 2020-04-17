---
title: Import Payroll Transactions| Microsoft Docs
description: To manage salary, you import and post financial transactions from your payroll provider to the general ledger, using a payroll extension such as Ceridian or Quickbooks.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2019
ms.author: SorenGP

---
# Import mzdových transakcí
Chcete-li účtovat platby mezd a související transakce, musíte importovat a zaúčtovat finanční transakce provedené poskytovatelem mezd do hlavní knihy. Chcete-li to provést, nejprve importujte soubor, který obdržíte od poskytovatele mezd, na stránku **Finanční deník**. Potom namapujte externí účty v souboru mezd na příslušné účty hlavní knihy. Nakonec zaúčtujte mzdové transakce podle mapování účtu.

> [!NOTE]
> Pro použití této funkce je nutné nainstalovat a povolit rozšíření pro import mezd. Rozšíření Ceridian Payroll a Quickbooks Payroll File Import jsou předinstalovány v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro více informací navštivte [Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] Použití rozšíření](ui-extensions.md).

## Import mzdového souboru
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky** a poté vyberte související odkaz.
2. V příslušné dávke finančního deníku vyberte akci **Import mzdových transakcí**. Otevře se průvodce asistovaným nastavením.
3. Postupujte podle pokynů na stránce **Import mzdových transakcí**.

   > [!TIP]
   > V kroku mapování externích mzdových záznamů na finančních účtech budou mapování, která provedete, zapamatována při příštím importu stejných záznamů. To vám ušetří čas, protože nemusíte ručně vyplňovat pole **Číslo účtu** ve finančním deníku pokaždé, když importujete opakované transakce mezd.

   Když v průvodci nastavíte tlačítko **OK**, je stránka **Finanční denník** vyplněna řádky představujícími transakce, které soubor mezd obsahuje, a s příslušnými předvyplněnými účty v polích **Finanční účet** podle mapování provedených v průvodci.
4. Upravte nebo zaúčtujte řádky deníku stejně jako u jiných transakcí hlavní knihy. Pro více informací navštivte [Účtování transakcí přímo do hlavní knihy](finance-how-post-transactions-directly.md).

## Viz také
[Finance](finance.md)  
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] Použití rozšíření](ui-extensions.md)  
[Práce s finančními denníky](ui-work-general-journals.md)
