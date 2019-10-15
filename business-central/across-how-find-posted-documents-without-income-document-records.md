---
title: Vyhledávání dokumentů bez příloh | Microsoft Docs
Description: 'You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="find-posted-documents-without-incoming-document-records"></a>Vyhledání zaúčtovaných dokumentů bez záznamů příchozího dokumentu
Ze stránky **Účtová osnova** a **Věcných položek** můžete pomocí vyhledávací funkce vyhledat položky hlavní knihy pro zaúčtované nákupní a prodejní dokumenty, které nemají záznamy příchozího dokumentu a poté centrálně odkazovat na existující záznamy nebo vytvářet nové dokumenty s přiloženými soubory.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Vyhledání zaúčtovaných dokumentů bez záznamů příchozího dokumentu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
2. Vyberte řádek pro finanční účet, kde jsou položky hlavní knihy, které chcete zaúčtovat jako nákupní a prodejní dokumenty bez záznamů příchozího dokumentu a pak zvolte akci **Zaúčtován doklad bez došlého dokladu**.
3. Alternativně zvolte akci **Položky**.
4. Na stránce **Položky hlavní knihy** zvolte akci **Zaúčtován doklad bez došlého dokladu**.

Okno **Zaúčtován doklad bez došlého dokladu** otevře zaúčtované nákupní a prodejní dokumenty bez záznamů příchozího dokumentu reprezentovány položkami hlavní knihy ve finančním účtu, který pro toto okno otevřete. Stránka může ukázat maximálně 1000 řádků. Ve výchozím nastavení pole **Filtr data** omezuje řádky na položky s daty zveřejnění od začátku účetního období do data práce.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Připojení nalezených dokumentů k existujícím záznamům došlého dokladu
1. Na stránce **Zaúčtované dokumenty bez příchozího dokumentu** vyberte řádek pro zaúčtovaný dokument, který chcete připojit k existujícímu záznamu příchozího dokumentu a pak zvolte akci **Vybrat došlý doklad**.
2. Na stránce **Došlé doklady** vyberte záznam došlého dokumentu, který chcete připojit k zaúčtovanému dokumentu a pak zvolte tlačítko **OK**.
3. V okně **Zaúčtované doklady bez došlého dokumentu** vyberte záznam příchozího dokument, který je nyní připojen k zaúčtovanému dokumentu, jak můžete vidět v okně s fakty **Soubory došlého dokladu**.

Pokud na stránce **Došlé doklady** neexistuje příslušný záznam příchozího dokumentu, můžete jej vytvořit. Další informace naleznete v části [Vytvořit záznam došlého dokladu](across-how-create-income-document-records.md) Záznam.

## <a name="see-also"></a>Viz také
[Proces Došlého dokumentu](across-process-income-documents.md)  
[Došlé doklady](across-income-documents.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
