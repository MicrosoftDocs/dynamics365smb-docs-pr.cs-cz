---
title: Sales Quick Start (contains video)
description: Learn how to fill in the first critical fields about products and customers in Business Central so that you can start your sales processes.
author: jill-kotel-andersson

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: edupont

---

# Rychlý start prodeje

Abyste mohli prodávat produkty a služby, musíte nejprve založit a nastavit zboží a zákazníky. Jakmile to provedete, můžete začít evidovat prodejní objednávky a odesílat faktury.

## Nastavení a založení zboží k prodeji

Toto video ukazuje, jak nastavit zboží pro prodej v [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### Založení nového zboží

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Další informace a další kroky, které můžete udělat při zakládání a nastavení zboží, naleznete v tématu [Evidence nového zboží](inventory-how-register-new-items.md).

## Nastavení zákazníků

Toto video ukazuje, jak nastavit nového zákazníka v [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### Nastavení nového zákazníka

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Další informace a další kroky, které můžete udělat při zakládání a nastavení zboží, naleznete v tématu [Evidence nového zákazníka](sales-how-register-new-customers.md)

## Vytvoření prodejní objednávky

Když něco prodáváte zákazníkovi, máte dvě možnosti. První a nejjednodušší je vytvořit prodejní fakturu. Pokud je však váš proces prodeje složitější, například pokud máte situace, kdy odesíláte pouze části objednaného množství, použijete prodejní objednávku.

### Vytvoření prodejní objednávky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
2. Vyberte **Nový** a vytvořte nový záznam.
3. Do pole **Zákazník** zadejte jméno existujícího zákazníka.

   Ostatní pole na stránce **Prodejní objednávka** se sama vyplní standardními informacemi o vybraném zákazníkovi.

4. Podle potřeby vyplňte další zbývající pole na stránce **Prodejní objednávka**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. V záložce **Řádky** v poli **Typ** vyberte typ zboží, poplatek nebo transakce, které budete účtovat zákazníkovi s řádkem prodeje.

6. Do pole **Číslo** zadejte číslo zboží nebo služby.

7. Do pole **Množství** zadejte počet položek, které mají být prodány.

8. Do pole **Řádková sleva** zadejte procentuální hodnotu, pokud chcete odběrateli poskytnout slevu na produkt.

9. Chcete-li přidat komentář k řádku objednávky, který zákazník může vidět na vytištěné prodejní objednávce, napište komentář do pole **Popis** na prázdném řádku.

10. Opakujte kroky 5 až 9 pro každou položku, kterou chcete prodat zákazníkovi.

11. Chcete-li odeslat pouze část objednaného množství, zadejte toto množství do pole **K dodání**. Hodnota se zkopíruje do pole **K. fakturaci**.

12. Chcete-li fakturovat pouze část dodaného množství, zadejte toto množství do pole **K fakturaci**. Množství musí být nižší než hodnota v poli **K dodání**.

13. Po dokončení řádků prodejní objednávky vyberte akci **Účtovat a Odeslat**.

Další informace a další kroky, které můžete udělat při zakládání prodejních objednávek navštivte [Prodej produktů pomocí podejní objednávky](sales-how-sell-products.md).

## Vytvoření prodejní faktury

Když vytvoříte a zaúčtujete prodejní fakturu, vytvoříte nejen fakturu, kterou odešlete zákazníkovi, ale také vytvoříte související položky množství a hodnoty v [!INCLUDE[prod_short](includes/prod_short.md)].

### Vytvoření a zaúčtování prodejní faktury

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktury** a poté vyberte související odkaz.

2. Vyberte **Nový** a vytvořte nový záznam.

3. Do pole **Zákazník** zadejte jméno existujícího zákazníka.

4. Podle potřeby vyplňte další zbývající pole na stránce **Prodejní faktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. V záložce **Řádky** v poli **Typ** vyberte typ zboží, poplatek nebo transakce, které budete účtovat zákazníkovi s řádkem prodeje.

6. V poli **Číslo** vyberte záznam, který chcete účtovat, podle hodnoty v poli **Typ**.

7. V poli **Množství** zadejte, kolik jednotek zboží, nákladů nebo transakcí bude řádek zaznamenávat pro odběratele.

8. Pokud chcete poskytnout slevu, zadejte procento do pole **Řádková sleva %**. Hodnota v poli **Částka na řádku** se odpovídajícím způsobem aktualizuje.

9. Opakujte kroky 5 až 8 pro každý produkt nebo poplatek, který chcete zákazníkovi fakturovat.

10. V poli **Fakturační sleva** zadejte částku, která má být odečtena od hodnoty uvedené v poli**Celkem včetně DPH**.

11. Po dokončení řádků prodejní faktury vyberte akci **Účtovat a odeslat**.

Další informace a další kroky, které můžete udělat při zakládání prodejních faktur, navštivte [Prodejní faktury](sales-how-invoice-sales.md)

## Viz také

[Business Central Quick Starts](quick-start-business-central.md)  
[Přehled Prodeje](sales-manage-sales.md)  
[Prodej produktů zákazníkovi pomocí prodejních objednávek](sales-how-sell-products.md)  
[Prodejní faktury](sales-how-invoice-sales.md)
