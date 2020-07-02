---
title: Apply Payments to Related Documents and Post Them| Microsoft Docs
description: Describes how to record payments that you make to vendors and refunds that you make to customers.  
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: edupont

---
# Platby záznamů a refundace v deníku plateb

Na stránce **Deníky plateb** se zaznamenávají platby, které provedete dodavatelům a refundace, které provedete zákazníkům. Když zaúčtujete řádek platebního deníku, zaplacená částka se zaznamená na určený systémový bankovní účet. Poté musíte podniknout kroky k provedení skutečného převodu peněz z příslušného bankovního účtu.

Deník plateb je finanční deník, který je optimalizován pro provádění plateb. Řádky můžete rychle přidat ručně, můžete nechat [!INCLUDE[d365fin](includes/d365fin_md.md)] navrhnout platby dodavatelům a platbu můžete použít na zaúčtované dokumenty. I když provádíte platby, do pole **Částka dokumentu** zadejte kladnou částku. V závislosti na typu dokladu pro řádek deníku je tato částka převedena na zápornou částku v podkladových transakcích. Tímto způsobem je rychlejší přidávat řádky deníku ručně. Pokud dáváte přednost zadání záporných částek, můžete personalizovat platební deník tak, aby místo toho zobrazoval pole **Částka**.

- Použití plateb na faktury nebo dobropisy

   Pokud vyplníte pole **Číslo vyrovnání  dokladu** s fakturou nebo dobropisem, které musí být zaplaceno nebo vráceno, pak je daný dokument nastaven na zaplacený při zveřejnění deníku. Tento postup se označuje jako "aplikovaný". Jako alternativu k použití během účtování platby můžete použít stránky **Vyrovnané položky dodavatele** a **Vyrovnané položky zákazníků** poté, co jste provedli účtování plateb. Pro více informací navštivte například [Odsouhlasení platby dodavatele s deníkem plateb nebo z položek účetní knihy](payables-how-apply-purchase-transactions-manually.md).

- Získání navrhovaných plateb dodavatelům nebo zaměstnancům

   Funkce **Navrhnout platby dodavateli** a **Navrhnout platby zaměstnanci** mohou pomoci automaticky vyplnit řádky deníku plateb podle priority dodavatele a termínu splnění. Pro více informací navštivte [Návrh platby dodavateli](payables-how-suggest-vendor-payments.md). S touto funkcí je pole **Číslo vyrovnání  dokladu** vždy vyplněno.

- Tisk šeků a předkládaní elektronické platby vaší bance

   Kromě záznamu o provedení platby můžete také použít stránku **Deníky plateb** k odeslání platby pro další zpracování vaší bankou. Pro více informací navštivte [Provádění platby šekem](payables-how-work-checks.md) a [Provádění elektronické platby](payables-how-export-payments-bank-file.md).

## Provádění platby v deníku plateb

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Deníky plateb** a poté vyberte související odkaz.
2. Otevřete list deníku, který je vyhrazen pro platby.
3. Pokud víte, kdo má zaplatit nebo vrátit peníze, vyplňte pole ručně. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Chcete-li také použít platbu na související fakturu nebo dobropis, vyberte pole **Číslo vyrovnání dokladu** na stránce **Vyrovnat položky dodavatele** a vyberte příslušnou fakturu nebo dobropis, pak klepněte na tlačítko **OK**.

   Mnoho polí, například **Částka dokumentu** a **Termín splnění**, je nyní vyplněno informacemi z vybraného dokumentu.
5. Případně použijte funkci **Navrhnout platby dodavateli**. Všechny řádky týkající se informací a částek jsou poté zapsány do řádků deníku. Pro více informací navštivte [Navrhnout platby dodavateli](payables-how-suggest-vendor-payments.md).

   Zprávy vás provedou správným vyplněním požadovaných polí.
6. Po dokončení všech řádků platebního deníku vyberte akci **Účtovat**.

## Viz také
[Provádění platby šekem](payables-how-work-checks.md)  
[Provádění elektronické platby](payables-how-export-payments-bank-file.md)  
[Správa závazků](payables-manage-payables.md)  
[Nastavení bankovnictví](bank-setup-banking.md)  
[Export souboru kladných plateb](finance-how-positive-pay.md)  
[Práce s finančním deníkem](ui-work-general-journals.md)  
[Přizpůsobení pracovního prostoru](ui-personalization-user.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
