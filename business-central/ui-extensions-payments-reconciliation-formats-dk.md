---
title: Používání rozšíření Payments and Reconciliations (DK) | Microsoft Docs
description: 'Toto rozšíření usnadňuje export souborů, které jsou předem naformátovány tak, aby splňovaly bankovní požadavky na elektronická podání.'
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'extension, bank, formats'
ms.date: 10/01/2018
ms.author: bholtorf
---

# <a name="the-payments-and-reconciliations-dk-extension"></a>Rozšíření Payments and Reconciliations (DK)
Proveďte rychlé a bezchybné platby exportováním souborů, které jsou speciálně formátovány pro výměny s dodavatelem nebo bankou. Tyto soubory urychlují procesy platby a odsouhlasení a eliminují chyby, ke kterým může dojít, když ručně zadáváte informace na webové stránce banky.  

Toto rozšíření podporuje formáty souborů pro několik dánských bank. Při exportu platebních údajů do souboru rozšíření doplní data do formátu, který vaše banka vyžaduje. Formáty například zahrnují Bankdata-V3, BEC, SDC and FIK, které používá mnoho různých bank, a některé, které jsou více specializovány pro určité banky, například Danske Bank a Nordea. Rozšíření také zahrnuje některé formáty pro import a odslouhlasení bankovních výpisů.  

> [!Note]
> Chcete-li toto rozšíření používat, musíte znát formát, který vaše banka nebo prodejce vyžaduje. Některé banky nebo prodejci poskytují tyto informace na svých webových stránkách, ale možná budete muset kontaktovat jejich zákaznický servis, abyste získali tyto informace.  

## <a name="supported-bank-formats"></a>Podporované formáty bank
Toto rozšíření může pro platební soubory použít následující formáty souborů:  

* BANKDATA-V3  
* BEC-INDLAND  
* BEC-CSV  
* DANSKEBANK-CMKV  
* DANSKEBANK-CMKXKSX  
* DANSKEBANK  
* FIK71  
* NORDEA-ERHVERV-CSV  
* NORDEA  
* NORDEA-UNITEL-V3  
* SDC  
* SDC-CVS  

## <a name="to-set-up-the-extension"></a>Pro nastavení rozšíření
Začněte několika kroky.  

* Povolte export platebních údajů. Toto není snadno dostupné z důvodu ochrany vašich dat.  
* Nastavte nákup a závazky tak, abyste na fakturách nevyžadovali externí čísla dokumentů. V případě potřeby můžete použít referenční číslo pro odkaz na konkrétní fakturu.  
* Zadejte způsob platby pro každého dodavatele. Způsoby plateb definují způsob, jakým platíte faktury od dodavatele. Například banka, hotovost, šek nebo účet.  
* Určete typ formátu, který se použije pro každý z vašich bankovních účtů. Například NORDEA, DANSKEBANK, SDC atd.  

Kromě toho musíte přiřadit dodavatele k domácí **Obecné obch.účto** skupině a k **Účto skupině dodatavatele**. Nastavení země/oblasti pro dodavatele musí být Dánsko (DK). Pro další informace navštivte [Nastavení skupin účtování](finance-posting-groups.md).  

### <a name="to-allow-included365finincludesd365fin_mdmd-to-export-payment-data"></a>Pro umožnění [!INCLUDE[d365fin](includes/d365fin_md.md)] exportovat data platby
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Deník plateb** a poté vyberte související odkaz.  
2. Na stránce **Upravit deník plateb** zvolte dávku **Banka**.  
3. Zaškrtněte políčko **Povolen export úhrad**.  

### <a name="to-specify-a-payment-method-for-a-vendor"></a>Pro určení způsobu platby pro dodavatele
Následující tabulka ukazuje kombinace platebních metod FIK a ŽIRO, které [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje.

||Typ 01 | Typ 04 | Typ 71 | Typ 73 |
|----|---|---|---|---|
|Číslo žirového účtu nebo číslo FIK kreditora? | Číslo žirového účtu | Číslo žirového účtu | Číslo FIK kreditora | Číslo FIK kreditora|
|Umožňuje zprávu příjemci? | Ano |Ne |Ne | Ano |
|Obsahuje referenční číslo platby? | Ne | Ano, 16 číslic. | Ano, 15 číslic. | Ne|

1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Dodavatelé** a poté vyberte související odkaz.  
2. Otevřete kartu, rozbalte záložku **Platby** a v poli **Způsob platby** zvolte způsob platby.  
3. V závislosti na vašem výběru musíte vyplnit další pole. Popis kombinací viz tabulka výše.  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a>Pro určení formátu, který se použije pro bankovní účet
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.  
2. Otevřete kartu pro bankovní účet.  
3. V poli **Formát exportu plateb**, zvolte formát vašeho exportovaného souboru.  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a>Výběr platebních informací FIK nebo ŽIRO pro faktury dodavatele
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktury** a poté vyberte související odkaz.
2. Vyberte dodavatele. Pamatujte, že se musí jednat o dánského prodejce s adresou v Dánsku.
3. Vytvořte fakturu. Pole **Způsob platby** a **Číslo dodavatele** jsou vyplněna na základě nastavení v kartě dodavatele. Můžete je změnit, pokud chcete.
4. Do pole **Platební reference** zadejte 15místné číslo z faktury dodavatele.  

    > [!Tip]
    > Musíte přidat pouze posledních 11 číslic tohoto čísla. [!INCLUDE[d365fin](includes/d365fin_md.md)] přidá čtyři nuly na začátek čísla.  

5. Zaúčtujte fakturu.

## <a name="to-use-the-extension-to-export-payment-data"></a>Pro použití rozšíření pro export dat platby
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Deník plateb** a poté vyberte související odkaz.  
2. Vyberte akci **Navrhnout platební deníky dodavatele**.  

    > [!Tip]
    > Pokud chcete exportovat pouze konkrétní platby, použijte možnosti filtrování dat.  

3. V případě potřeby můžete přidat filtry a exportovat pouze konkrétní platby.  
4. V poli **Typ platby v bance** Zvolte **Elektronická platba**.  
5. Zvolte akci **Exportovat**.  

## <a name="see-also"></a>Viz také
[Přizpůsobení Business Central pro [!INCLUDE[d365fin](includes/d365fin_md.md)] pomocí rozšíření](ui-extensions.md)  
[Vytvoření záznamu SEPA – příkaz k inkasu a jeho export do bankovního souboru](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)  
[Nastavení SEPA – příkaz k inkasu](finance-how-to-set-up-sepa-direct-debit.md)  
[Účtování přijaté platby SEPA – příkaz k inkasu](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Sběr plateb pomocí SEPA – příkaz k inkasu](finance-collect-payments-with-sepa-direct-debit.md)  
[Práce s finančními deníky](ui-work-general-journals.md)  
