---
title: 'Definování, které došlé dokumenty půjde vidět | Microsoft Docs'
description: 'Upravte výchozí zobrazení příchozích dokumentů, například elektronických faktur, a vylepšete tak přehled o zpracovaných a nezpracovaných záznamech.'
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
# <a name="manage-many-incoming-document-records"></a>Správa mnoha záznamů příchozích dokumentů
Při vytváření nebo zpracování záznamů příchozího dokumentu může počet řádků v stránka **Došlé dokumenty** narůstat do té míry, až v ní ztratíte přehled. Proto můžete nastavit záznamy příchozího dokumentu na možnost Zpracovat, abyste jej mohli odstranit z výchozího zobrazení. Když zvolíte akci **Ukázat vše** můžete zobrazit jak zpracované, tak nezpracované záznamy.

> [!NOTE]  
>   Nemůžete upravovat informace, připojovat soubory ani provádět jiné procesy na záznamech příchozího dokumentu, které jsou nastaveny na hodnotu Zpracováno. Nejprve je musíte nastavit na Nezpracováno.

Zaškrtávací políčko **Zpracováno** je automaticky vybráno na záznamech příchozího dokumentu, které byly zpracovány, ale také můžete vybrat nebo zrušit zaškrtnutí políčka ručně. V závislosti na vašem obchodním procesu může být záznam příchozího dokumentu zpracován, pokud byl pro něj vytvořen související dokument nebo byl připojen soubor.

> [!NOTE]  
>   Když otevřete Stránka **Došlé dokumenty** pomocí akce **Moje Došlé dokumenty** v centru rolí se zobrazí ve výchozím nastavení pouze nezpracované záznamy příchozího dokumentu. Toto je v tomto tématu označováno jako "výchozí zobrazení".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Odebrání záznamů příchozího dokumentu z výchozího zobrazení
1. V Stránka **Došlé dokumenty** vyberte jeden nebo více řádků pro záznamy příchozího dokumentu, které chcete z výchozího zobrazení odstranit.
2. Zvolte akci **Nastavit na zpracované**.

    Záznamy příchozího dokumentu jsou z výchozího zobrazení odstraněny a na řádcích je zaškrtnuto políčko **Zpracováno**.

> [!NOTE]  
>   Tuto akci můžete provést také pro jednotlivé záznamy na stránce **Karta příchozího dokumentu**.

## <a name="to-view-all-incoming-document-records"></a>Zobrazení všech záznamů příchozího dokumentu
1. Na stránce **Příchozí dokumenty** zvolte akci **Ukázat vše**.

Zobrazí se všechny záznamy příchozího dokumentu, včetně těch, ve kterých není zaškrtnuto políčko **Zpracováno**.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Přidání záznamů příchozího dokumentu do výchozího zobrazení
1. Na stránce **Příchozí dokumenty** zvolte akci **Ukázat vše**.
2. Vyberte jeden nebo více řádků pro záznamy příchozího dokumentu, které chcete zobrazit ve výchozím zobrazení.
3. Zvolte akci **Nastavit na nezpracovanou**.  

> [!NOTE]  
>   Tuto akci můžete provést také pro jednotlivé záznamy na stránce **Karta došlého dokumentu**.

## <a name="see-also"></a>Viz také
[Proces Došlého dokumentu](across-process-income-documents.md)  
[Došlé doklady](across-income-documents.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
