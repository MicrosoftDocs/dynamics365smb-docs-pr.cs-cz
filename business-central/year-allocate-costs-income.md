---
title: Overview of Tasks to Allocate Costs and Income | Microsoft Docs
description: Outlines the tasks to allocate an entry in a general journal to several different accounts when you post the journal.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont

---
# Přidělení nákladů a výnosů
Při účtování deníku můžete přiřadit položku ve finančním deníku několika různým účtům. Přidělení lze provést třemi různými metodami:

* Množství
* Procento (%)
* Částka

Funkce přidělení lze použít opakovaně pomocí finančních deníků a deníků dlouhodobého majetku.
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

Následující postupy popisují, jak připravit přidělení nákladů v periodickém finanční deníku pomocí definování alokačních klíčů Když jsou definovány alokační klíče, tak poté dokončíte a zaúčtujete deník jako jakýkoli jiný periodický finanční deník. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).

## Nastavení alokačních klíčů
Položku v periodickém finančním deníku můžete při účtování přidělit několika různým účtům. Přidělení lze vytvořit podle množství, procenta nebo částky.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Periodické fin. deníky** a poté vyberte související odkaz.
2. Klepnutím na pole **Název listu** otevřete stránku **Listy Finančního Deníku**.
3. Můžete buď upravit již existující přidělení v listech děníku, nebo vytvořit nový deník s patřičným přidělením.
   * Chcete-li vytvořit novou dávku, vyberte akci **Nový** a přejděte k dalšímu kroku.
   * Chcete-li změnit přidělení existujícího deníku, vyberte deník a přejděte ke kroku 7.
4. Do pole **Název** zadejte název dávky, například ČIŠTĚNÍ. Do pole **Popis** zadejte popis, například Deník pročištění výdajů.
5. Až budete hotovi, zavřete stránku. Otevře se nový, prázdný periodický deník.
6. Vyplňte pole v hlavičce.
7. Zvolte akci **Rozdělení**.
8. Přidejte řádek pro každé přidělení. Musíte vyplnit buď pole **Rozdělení %**, **Rozdělené množství** nebo **Částka**. Musíte také vyplnit pole **Číslo účtu** a pokud přidělujete transakci mezi globální dimenze, pole globální dimenze.
9. Pokud do řádku zadáte procento, automaticky se vypočítá částka v poli **Částka**. Tyto částky mají opačné znaménko než celková částka v poli **Částka** v periodickém deníku.
10. Po zadání řádků přidělení zvolte **OK** pro návrat na stránku **Periodický finanční deník**. **Rozdělená částka (USD)** je vyplněno a odpovídá poli **Částka**.
11. Zaúčtujte deník.

## Změna již nastaveného alokačního klíče
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Periodické fin. deníky** a poté vyberte související odkaz.
2. Na stránce **Periodický finanční deník** vyberte deník s rozdělením.
3. Vyberte řádek s rozdělením a poté vyberte akci **Rozdělení**.
4. Změňte příslušná pole a poté stiskněte tlačítko **OK**.

## Viz také
[Uzavírání roků a období](year-close-years-periods.md)  
[Práce s finančními deníky](ui-work-general-journals.md)    
[Účtování dokladů a deníků](ui-post-documents-journals.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]