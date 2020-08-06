---
title: Create Incoming Documents From Documents| Microsoft Docs
description: You can create records of incoming documents, such as e-invoices, and manage OCR tasks, eCommerce, and document exchange.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: sgroespe

---
# Vytváření došlých dokladů přímo z dokladů a položek
Externí obchodní dokumenty můžete uložit v  [!INCLUDE[d365fin](includes/d365fin_md.md)] připojením souborů dokumentů k souvisejícím příchozím dokladům. Pokud doklad, například nákupní faktura, nezačíná svou existenci jako záznam došlého dokladu, můžete k němu později vytvořit a připojit záznam příchozího dokladu. Soubory došlých dokladů můžete také připojit k zaúčtovaným nákupním a prodejním dokladům a k položkám dodavatele, zákazníka a hlavní knihy pomocí FactBoxu **Připojené doklady**, například, the **Účtované nákupní faktury** a **Položka dodavatele**.

Na stránkách **Účetní osnova** a **Věcné položky**, můžete pomocí vyhledávací funkce najít položky hlavní knihy pro zaúčtované nákupní a prodejní doklady, které nemají došlý doklad a poté centrálně propojit existující záznamy nebo vytvořit nové s připojenými soubory dokladů. Pro více informací bežte [Vyhledávání účtovaných dokladů bez došlých dokladů](across-how-find-posted-documents-without-income-document-records.md).

Následující postupy ukazují, jak připojit soubor k existující nákupní faktuře, která nebyla vytvořena z došlého dokladu a jak připojit soubor k položce dodavatele. Připojení souboru k zaúčtovaným nákupním nebo prodejním dokladům funguje podobným způsobem.

## Vytvoření a připojení záznamu došlého dokladu k nákupní faktuře
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktury** a poté vyberte související odkaz.
2. Vyberte řádek nákupní faktury, ke kterému chcete připojit soubor, a pak zvolte funkci **Soubory došlého dokladu**.
3. Případně vyberte řádek nákupní faktury, ke které chcete připojit soubor, a poté vyberte akci **Připojit soubor**.
4. Na stránce **Vložit soubor** vyberte soubor, který představuje daný došlý doklad a pak zvolte **Otevřít**.

## Vytvoření a připojení záznamu došlého dokladu z položky dodavatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky dodavatele** a poté vyberte související odkaz.
2. Vyberte řádek pro položku dodavatele, ke které chcete připojit soubor a pak zvolte akci **Vytvořit došlý doklad ze souboru**.
3. Alternativně, vyberte řádek pro položku dodavatele, ke které chcete připojit souboru a pak zvolte akci **Připojit soubor**.
4. Na stránce **Vložit soubor** vyberte soubor, který představuje daný došlý doklad a pak zvolte **Otevřít**.

## Odebrání propojení záznamu došlého dokladu s zaúčtovaným dokladem
Přílohy souborů z nezaúčtovaných dokladů můžete kdykoli odebrat odstraněním souvisejícího záznamu došlého dokladu. Pokud je doklad zaúčtován, musíte nejprve odebrat propojení z souboru došlého dokladu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Došlé doklady** a poté vyberte související odkaz.
2. Vyberte řádek souboru došlého dokladu připojeného k zaúčtovanému dokladu, který chcete odebrat, a pak zvolte akci **Odebrat odkaz na záznam**.

Připojení k zaúčtovanému dokladu bude odebráno. Nyní můžete přistoupit k připojení dalšího souboru došlého dokladu k zaúčtovanému dokladu, tak jak je popsáno v tomto tématu.

## Viz také
[Proces došlých dokladů](across-process-income-documents.md)  
[Došlé doklady](across-income-documents.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
