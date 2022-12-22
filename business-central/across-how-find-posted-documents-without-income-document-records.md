---
title: Find Posted Documents without Incoming Documents
description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
author: SorenGP


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont

---
# Vyhledání zaúčtovaných dokladů bez záznamů došlého dokladu
Na stránkách **Účetní osnova** a **Věcné položky** můžete pomocí funkce vyhledávání najít záznamy věcné položky pro zaúčtované nákupní a prodejní doklady, které nemají záznamy o došlých dokladech a poté centrálně propojte existující záznamy nebo vytvořte nové s připojenými soubory dokladů.

## Vyhledání zaúčtovaných dokladů bez záznamů došlého dokladu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
2. Vyberte řádek pro finanční účet, kde jsou věcné položky, které chcete zaúčtovat jako nákupní a prodejní doklady bez záznamů příchozího dokladu a pak zvolte akci **Zaúčtovat doklad bez došlého dokladu**.
3. Alternativně zvolte akci **Položky**.
4. Na stránce **Věcné položky** zvolte akci **Zaúčtovat doklady bez došlých dokladů**.

Otevře se stránka **Zaúčtované doklady bez došlého dokladu** zobrazující zaúčtované nákupní a prodejní doklady bez záznamů došlého dokladu reprezentovaných věcných položek na finančním účtě, pro který jste stránku otevřeli. Stránka může ukázat maximálně 1000 řádků. Standardně tedy pole **Filtr data** obsahuje filtr, který omezuje řádky na záznamy s daty účtování od začátku účetního období do pracovního data.

## Připojení nalezených dokladů k existujícím záznamům došlého dokladu
1. Na stránce **Zaúčtované doklady bez došlého dokladu** vyberte řádek pro zaúčtovaný doklad, který chcete připojit k existujícímu záznamu došlého dokladu, a poté zvolte akci **Vybrat došlý doklad**.
2. Na stránce **Došlé doklady** vyberte záznam došlého dokladu, který chcete propojit s nalezeným zaúčtovaným dokladem, a poté klepněte na tlačítko **OK**.
3. Na stránce **Zaúčtované doklady bez došlého dokladu** je nyní vybraný záznam došlého dokladu připojen k zaúčtovanému dokladu, jak můžete vidět ve FactBoxu **Soubory došlých dokladů**.

Pokud na stránce **Došlé doklady** neexistuje relevantní záznam došlého dokladu, můžete jej vytvořit. Další informace naleznete v části [Vytvoření záznamů došlých dokladů](across-how-create-income-document-records.md).

## Viz také
[Zpracování došlých dokladů](across-process-income-documents.md)    
[Došlé doklady](across-income-documents.md)    
[Nákup](purchasing-manage-purchasing.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]