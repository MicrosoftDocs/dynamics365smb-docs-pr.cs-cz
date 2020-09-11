---
title: Create Records of Incoming Documents| Microsoft Docs
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
# Vytvoření záznamu došlého dokladu
Na stránce **Došlé doklady** můžete pomocí různých funkcí prohlížet účtenky, spravovat úlohy OCR a ručně nebo automaticky převádět soubory příchozích dokladů na příslušné doklady nebo řádky deníku. Externí soubory lze připojit v libovolné fázi procesu, včetně zaúčtovaných dokladů a výsledných položek dodavatele, zákazníka a financí.

Chcete-li zaznamenat externí doklad v [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte nejprve vytvořit nebo dokončit záznam došlého dokladu. Můžete to udělat ručně, nebo můžete vyfotografovat externí doklad a pak vytvořit záznam došlého dokladu s připojeným obrázkovým souborem.

Předtím než můžete použít funkce Došlých dokladů, musíte provést požadované nastavení. Pro více informací navštivte [Nastavení došlých dokladů](across-how-setup-income-documents.md).

## Schválení nebo odmítnutí došlých dokladů
Pokud chcete povolit uživatelům vytvářet faktury nebo řádky finančního deníku ze záznamů došlého dokladu, dokud nejsou schváleny, můžete nastavit toho, kdo musí schválit záznamy předtím, než budou zpracovány.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Došlé doklady** a poté vyberte související odkaz.
2. Vyberte řádek dokumentu, který chcete schválit nebo odmítnout a pak zvolte akci **Schválit** nebo **Odmítnout**.

Pokud schválíte došlý doklad, je vybráno zaškrtávací políčko **Vydat** v řádku doělého dokladu. Uživatel, který je pověřen tvorbou například nákupních faktur, může zpracovat záznam.

## Vytvoření záznamu došlého dokladu pořízením fotografie
> [!NOTE]  
> Následující postup platí pouze pro klienty tabletu a telefonu [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Na panelu aplikace zvolte dlaždici **Vytvořit příchozí dokument z fotoaparátu** a pak pokračujte na krok 4.
2. Alternativně, na panelu aplikace zvolte tlačítko možnosti, vyberte **Došlé doklady** a pak zvolte **Vše**.
3. Na stránce **Došlých dokladů** vyberte tlačítko se třemi tečkami a pak zvolte **Vytvoořit z kamery** Fotoaparát na tabletu nebo telefonu je aktivován.
4. Udělejte fotku dokladů například nákupní účtenku, který chcete zpracovat jako příchozí doklad a potom klepněte na tlačítko **OK**.

   Vytvoří se nový záznam došlého dokladu s připojeným obrázkem.

## Připojení obrázku k záznamu došléh dokladu pomocí fotografie
> [!NOTE]  
> Následující postup platí pouze pro klienty tabletu a telefonu [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Na panelu aplikace zvolte tlačítko možnosti, zvolte **Došlé doklady** a pak zvolte **Vše**.
2. Otevře se karta pro existující záznam došlého dokladu.
3. na stránce **Došlé doklady** vyberte tlačítko se třemi tečkami a zvolte **Připojit obrázek z fotoaparátu**. Fotoaparát na tabletu nebo telefonu je aktivován.
4. Udělejte fotku dokladů například nákupní účtenku, který chcete zpracovat jako příchozí doklad a potom klepněte na tlačítko **OK**.

   Obrázek je připojen k záznamu došlého dokladu.

## Vytvoření záznamu došlého dokladu ručně
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Došlé doklady** a poté vyberte související odkaz.
2. Vyberte akci **Vytvořit ze souboru**.
3. Na stránce **Vložit soubor** vyberte soubor a poté zvolte **Otevřít**. Soubor je automaticky připojen.
4. Alternativně vyberte **Nový**.
5. Chcete-li připojit soubor, zvolte **Připojit soubor**.
6. Na stránce **Vložit soubor** vyberte soubor, který představuje daný došlý doklad a pak zvolte **Otevřít**.
7. Na stránce **Došlé doklady** vyplňte pole dle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Viz také
[Proces došlých dokladů](across-process-income-documents.md)  
[Došlé doklady](across-income-documents.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
