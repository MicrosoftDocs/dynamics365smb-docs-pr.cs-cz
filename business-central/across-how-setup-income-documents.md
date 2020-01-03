---
title: Set Up Incoming Documents| Microsoft Docs
description: Use the Incoming Documents feature to create electronic documents, manage OCR tasks, import invoices, and convert image files.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe

---
# Nastavení Příchozích dokumentů
Pokud vytvoříte řádky finančního deníku ze záznamů příchozího dokumentu, musíte zadat na stránce **Nastavení příchozích dokumentů** šablonu deníku a dávku, které chcete použít.

Pokud nechcete, aby uživatelé vytvářeli faktury nebo řádky finančního deníku ze záznamů příchozího dokumentu, pokud nejsou dokumenty prvně schváleny, je nutné nastavit schvalovatele na stránce  **Schvalovatelé příchozího dokumentu**.

Chcete-li soubory PDF a obrázkové soubory převést do elektronických dokumentů, které lze převést například na nákupní faktury v [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte nejprve nastavit funkci OCR a povolit službu.

Když je nastavena funkce Příchozí dokumenty, můžete použít různé funkce pro kontrolu výdajů, správu úloh OCR a převod souborů příchozího dokumentu ručně nebo automaticky na příslušné dokumenty nebo řádky deníku. Externí soubory lze připojit v libovolné fázi procesu, včetně zaúčtovaných dokumentů a výsledných záznamů prodejce, zákazníka a položek hlavní knihy. Další informace naleznete v části [Zpracování došlých dokladů](across-process-income-documents.md).

## Nastavení funkcí Příchozích dokumentů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení příchozích dokumentů** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Nastavení schvalovatelů záznamů o příchozím dokumentu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení příchozích dokumentů** a poté vyberte související odkaz.
2. Na stránce **Nastavení příchozích dokumentů** zvolte akci **Schvalovatelé**.

   Stránka **Schvalovatelé příchozího dokumentu** ukáže všechny uživatele, kteří jsou nastaveni v [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. Vyberte jednoho nebo více uživatelů, kteří mohou schválit příchozí dokument předtím, než lze vytvořit související dokument nebo řádek deníku.

Pokud byli schvalovatelé nastaveni na stránce **Schvalovatelé příchozích dokumentů**, pouze tito uživatelé mohou schválit příchozí doklad, pokud je zaškrtnuto políčko **K vytvoření požadovat schválení** na stránce **Zpracování došlých dokladů**.

> [!NOTE]
> Toto nastavení schválení nesouvisí se schvalovanými Workflow. Pro více informací navštivte [Použití schvalování workflow](across-how-use-approval-workflows.md).

## Nastavení služby OCR
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení služby OCR**, a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Vaše přihlašovací údaje jsou automaticky šifrovány.

## Viz také
[Zpracování došlých dokladů](across-process-income-documents.md)
[Došlé doklady](across-income-documents.md)
[Nakupování](purchasing-manage-purchasing.md)
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
