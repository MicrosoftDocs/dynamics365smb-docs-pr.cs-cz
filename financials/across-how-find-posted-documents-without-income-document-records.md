---
title: Vyhledávání dokumentů bez příloh | Microsoft Docs
Description: 'You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/02/2017
ms.author: sgroespe
---
# <a name="find-posted-documents-without-incoming-document-records"></a>Vyhledání zaúčtovaných dokumentů bez záznamů příchozího dokumentu
Z okna **Účtová osnova** a **Položek hlavní knihy** můžete pomocí vyhledávací funkce vyhledat položky hlavní knihy pro zaúčtované nákupní a prodejní dokumenty, které nemají záznamy příchozího dokumentu a poté centrálně odkazovat na existující záznamy nebo vytvářet nové dokumenty s přiloženými soubory.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>Vyhledání zaúčtovaných dokumentů bez záznamů příchozího dokumentu
1. Zvolte pravém horním rohu zvolte ikonu ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png ""), zadejte **Účetní osnova** a pak vyberte související odkaz.
2. Vyberte řádek pro finanční účet, kde jsou položky hlavní knihy, které chcete zaúčtovat jako nákupní a prodejní dokumenty bez záznamů příchozího dokumentu a pak zvolte akci **Zaúčtovat dokumenty bez příchozího dokumentu**.
3. Alternativně zvolte akci **Položky knihy**.
4. V okně **Položky hlavní knihy** zvolte akci **Zaúčtovat dokumenty bez příchozího dokumentu**.

Okno **Zaúčtované dokumenty bez příchozího dokumentu** otevře zaúčtované nákupní a prodejní dokumenty bez záznamů příchozího dokumentu reprezentovány položkami hlavní knihy ve finančním účtu, který pro toto okno otevřete. Okno může ukázat maximum 1000 řádků. Ve výchozím nastavení pole **Filtr data** omezuje řádky na položky s daty zveřejnění od začátku účetního období do data práce.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Připojení nalezených dokumentů k existujícím záznamům příchozího dokumentu
1. V okně **Zaúčtované dokumenty bez příchozího dokumentu** vyberte řádek pro zaúčtovaný dokument, který chcete připojit k existujícímu záznamu příchozího dokumentu a pak zvolte akci **Vybrat příchozí dokument**.
2. V okně **Příchozí dokumenty** vyberte záznam příchozího dokumentu, který chcete připojit k zaúčtovanému dokumentu a pak zvolte tlačítko **OK**.
3. V okně **Zaúčtované dokumenty bez příchozího dokumentu** vyberte záznam příchozího dokument, který je nyní připojen k zaúčtovanému dokumentu, jak můžete vidět v okně s fakty **Soubory příchozího dokumentu**.

Pokud v okně **Došlé doklady** neexistuje příslušný záznam příchozího dokumentu, můžete jej vytvořit. Další informace naleznete v části [Vytvořit záznam došlého dokumentu](across-how-create-income-document-records.md) Záznam.

## <a name="see-also"></a>Viz také
[Proces Došlého dokumentu](across-process-income-documents.md)  
[Došlé doklady](across-income-documents.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
