---
title: Amend or Cancel Unpaid Purchase Invoices | Microsoft Docs
description: Explains how to correct, cancel, or undo a posted purchase invoice and automatically create a purchase credit memo.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2020
ms.author: sgroespe

---
# Opravit nebo zrušit nezaplacené nákupní faktury
Zaúčtovanou nákupní fakturu můžete opravit nebo zrušit. To je užitečné, pokud chcete opravit chybu při psaní nebo pokud chcete změnit nákup v rané fázi procesu objednávky.

Pokud jste již zaplatili za produkty na zaúčtované nákupní faktuře, nemůžete je opravit nebo zrušit z samotné zaúčtované faktury. Místo toho musíte ručně vytvořit nákupní dobropis k obrácení nákupu, volitelně spravovaný s objednávkou nákupní vratky. Pro více informací navštivte [Zpracování nebo zrušení nákupní vratky](purchasing-how-process-purchase-returns-cancellations.md).

Na stránce **Účtované nákupní faktury** můžete vybrat tlačítko **Opravit** nebo tlačítko **Zrušit**. Když opravíte nebo zrušíte zaúčtovanou nákupní fakturu, nákupní dobropis se použije na všechny věcné položky a položky inventury, které byly vytvořeny při zaúčtování původní nákupní faktury. Tím dojde k obrácení zaúčtované nákupní faktury ve vašich finančních záznamech a ponechání opravného zaúčtovaného dobropisu na nákup pro váš revizní záznam. V následujícím textu je popsáno použití funkce **Opravit** a **Zručit**.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## Oprava zaúčtované nákupní faktury
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované nákupní faktury** a poté vyberte související odkaz.
2. Vyberte zaúčtovanou nákupní fakturu, kterou chcete opravit.

   > [!NOTE]
   > Pokud je zaškrtnuto políčko **Zrušeno**, nemůžete opravenou zaúčtovanou fakturu opravit, protože již byla opravena nebo zrušena.
3. Na stránce **Účtované nákupní faktury** zvolte **Opravit**.

   Vytvoří se nová nákupní faktura se stejnými informacemi, kde můžete provést opravu. Pro více informací navštivte [Záznam nákupů](purchasing-how-record-purchases.md). Pole **Zrušeno** na původní zaúčtované nákupní faktuře se změní na **Ano**.

   Nákupní dobropis je automaticky vytvořen a zaúčtován, aby se zrušila původní zaúčtovaná nákupní faktura.
4. Zvolte **Zobrazit opravný dobropis** pro zobrazení dobropisu zaúčtovaného nákupu, který ruší původní zaúčtovanou fakturu za nákup.

## Zrušení zaúčtované nákupní faktury
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované nákupní faktury** a poté vyberte související odkaz.
2. Vyberte zaúčtovanou nákupní fakturu, kterou chcete zrušit.

   > [!NOTE]
   > Pokud je zaškrtnuto políčko **Zrušeno**, nemůžete zrušit zaúčtovanou nákupní fakturu, protože již byla zrušena nebo opravena.
3. Na stránce **Účtovaná nákupní faktura** zvolte **Zrušit**.

   Nákupní dobropis je automaticky vytvořen a zaúčtován, aby se zrušila původní zaúčtovaná nákupní faktura. Pole **Zrušeno** na původní zaúčtované nákupní faktuře se změní na **Ano**.
4. Zvolte **Zobrazit opravný dobropis** pro zobrazení dobropisu zaúčtovaného nákupu, který ruší původní zaúčtovanou fakturu za nákup.

### Podporováno částečné zaúčtování faktury
Pokud zrušení souvisí s částečným zaúčtováním faktury, je původní řádek nákupní objednávky aktualizován tak, aby odrážel zrušené fakturované množství. Hodnoty pole **K  fakturaci** a **Fakturované  množství** na příslušném řádku objednávky se resetují na hodnoty před částečným účtováním.

## Viz také
[Nákup](purchasing-manage-purchasing.md)  
[Záznam nákupu](purchasing-how-record-purchases.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
