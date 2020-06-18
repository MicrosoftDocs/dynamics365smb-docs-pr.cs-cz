---
title: Create Interactions on Contacts and Segments| Microsoft Docs
description: Describes how to create interactions for communication that you have with your contacts and segments in Business Central, for example, direct mail.
services: project-madeira
documentationcenter: ''
author: jswymer

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2020
ms.author: jswymer

---
# Vytváření interakcí s kontakty a na segmentech
Můžete vytvořit interakce pro záznam všech interakcí a komunikací, které máte se svými kontakty a segmenty, například cílená pošta.

Před vytvořením interakcí musíte nastavit šablony interakcí. Pro více informací navštivte [Nastavení šablon interakce](marketing-interactions.md).

## Vytvoření interakce
1. Otevřete položku protokolu kontaktu, prodejce nebo interakce.
2. Vyberte akci **Vytvořit interakci**.
3. Vyplňte pole a vyberte tlačítko **OK**.

> [!NOTE]
> Pokud potřebujete před dokončením interakce provést další úkol, můžete zvolit **Storno** a dokončit interakci později. Tím se odloží interakce.

## Dokončení a odstranění odložených interakcí
1. Otevřete položku protokolu kontaktu, prodejce nebo interakce.
2. Zvolte **Odložené interakce**.
3. Vyberte interakci, kterou chcete dokončit, a pak zvolte akci **Pokračovat**.

## Vytvoření interakce na segmentu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Segmenty** a poté vyberte související odkaz.
2. Na stránce **Segment** v části **Interakce** vyplňte pole a určete, kterou interakci chcete segmentu přiřadit.

   Po přiřazení interakce k segmentu můžete přizpůsobit interakci pro každý konkrétní kontakt v rámci segmentu, například výběrem jiné šablony interakce na řádcích na stránce **Segment**.
3. Chcete-li zaznamenat segment a interakce, vyberte akci **Protokol**. Otevře se stránka **Protokolovat segment**.
4. Pokud chcete vytvořit nový segment obsahující stejné kontakty, zaškrtněte políčko **Vytvořit segment sledování**. Chcete-li vytvořit segment sledování, musíte mít na stránce **Nastavení marketingu** zadanou číselnou řadu pro segmenty.

Interakce se zaznamená pro každý kontakt v rámci segmentu v tabulce **Položka protokolu interakce** a segment se zaznamená do protokolu. Protokolované segmenty naleznete na stránce **Protokolovaný segment**.

Pokud jste zaškrtli políčko **Vytvořit segment sledování**, vytvoří se nový segment, který bude obsahovat stejné kontakty jako právě přihlášený segment.

## Viz také
[Interakce záznamu](marketing-interactions.md)  
[Správa kontaktů](marketing-contacts.md)  
[Správa prodejních příležitostí](marketing-manage-sales-opportunities.md)  
[Práce s Business Central](ui-work-product.md)
