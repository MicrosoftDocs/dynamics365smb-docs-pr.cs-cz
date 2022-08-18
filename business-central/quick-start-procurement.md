---
title: Procurement Quick Start (contains video)
description: Learn how to fill in the first critical fields about vendors in Business Central so that you can start purchasing products and services.
author: jill-kotel-andersson

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: 26, 27, 50, 56
ms.date: 09/29/2021
ms.author: edupont

---

# Rychlý začátek nákupu

Abyste mohli nakupovat produkty a služby, musíte nejprve založit a nastavit dodavatele. Jakmile to provedete, můžete začít evidovat nákupní objednávky a přijímat faktury.

## Nastavení dodavatelů

Následující video ukazuje, jak nastavit dodavatele v [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

### Založení nového dodavatele

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

Další informace a další kroky, které můžete udělat při zakládání a nastavení dodavatelů, naleznete v tématu [Evidence nových dodavatelů](purchasing-how-register-new-vendors.md).

## Vytváření nových nákupních objednávek

Když nakupujete něco od dodavatele, máte dvě možnosti. První a nejjednodušší je vytvořit nákupní fakturu. Nákupní objednávky je však nutné použít, pokud váš nákupní proces vyžaduje, abyste zaznamenali částečné příjmy množství objednávky, například proto, že celé množství nebylo k dispozici u dodavatele.

Následující video ukazuje, jak vytvořit nákupní objednávku v [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### Vytvoření nákupní objednávky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté zvolte související odkaz.

2. Na stránce **Nákupní objednávky**, vyberte funkci **Nový** k vytvoření nové nákupní objednávky.

3. Do pole **Název dodavatele** zadejte název existujícího dodavatele.

   Ostatní pole v **Nákupní hlavičcce** jsou nyní vyplněna standardními informacemi o vybraném dodavateli.

4. Podle potřeby vyplňte další zbývající pole na stránce **Nákupní objednávka**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   Nyní jste připraveni vyplnit řádky nákupní objednávky zbožím nebo zdroji, které jste zakoupili od dodavatele.

5. V záložce **Řádky** v poli **Číslo zboží** zadejte číslo inventární zboží nebo služby.

6. V poli **Množství** zadejte počet položek, které mají být zakoupeny.

   Pole **Částka na řádku** je aktualizováno tak, aby zobrazovalo hodnotu v poli **Nákupní cena** vynásobenou hodnotou v poli **Množství**.

7. V poli **Sleva objednávky** zadejte částku, která má být odečtena od hodnoty uvedené v poli **Celkem včetně. DPH** v dolní části objednávky.

8. Když obdržíte zakoupené zboží nebo služby, zvolte **Účtovat**.

Další informace a další kroky, které můžete udělat při zakládání nákupních objednávek, navštivte [Nakupování](purchasing-manage-purchasing.md).

## Vytvoření nákupní faktury

Vytvoření nákupní faktury pro zaznamenání nákladů na nákupy a pro sledování závazků. Vytvoření nákupní faktury je podobné jako vytvoření nákupní objednávky

### Jak vytvořit a zaúčtovat nákupní fakturu

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktury** a poté vyberte související odkaz.
2. Na stránce **Nákupní faktury** vyberte akci **Nový** pro vytvoření nové nákupní faktury.
3. Do pole **Dodavatel** zadejte název existujícího dodavatele.

   Ostatní pole na stránce **Nákupní faktura** se sama vyplní standardními informacemi o vybraném dodavateli.

4. Podle potřeby vyplňte i zbývající pole na stránce **Nákupní faktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   Nyní jste připraveni vyplnit řádky nákupní faktury zbožím nebo zdroji, které jste zakoupili od dodavatele.

5. V záložce **Řádky** v poli **Číslo zboží** zadejte číslo inventární zboží nebo služby.
6. V poli **Množství** zadejte počet položek, které mají být zakoupeny.

   Pole **Částka na řádku** je aktualizováno tak, aby zobrazovalo hodnotu v poli **Nákupní cena** vynásobenou hodnotou v poli **Množství**.

7. V poli **Fakturační sleva** zadejte částku, která má být odečtena od hodnoty uvedené v poli**Celkem včetně DPH** v dolní části faktury.

8. Když obdržíte zakoupené zboží nebo služby, zvolte **Účtovat**.

Nákup se nyní promítne do zásob, účetních knih zdrojů a finančních záznamů a je aktivována platba dodavatele. Nákupní faktura je odstraněna ze seznamu nákupních faktur a nahrazena novým dokladem v seznamu zaúčtovaných nákupních faktur.

Další informace a další kroky, které můžete udělat při zakládání nákupních objednávek, navštivte [Evidence nákupů pomocí nákupních faktur](purchasing-how-record-purchases.md).

## Viz také

[Business Central Quick Starts](quick-start-business-central.md)  
[Přehed nakupování](Purchasing-manage-purchasing.md)  
[Evidence nákupů pomocí nákupních faktur](purchasing-how-record-purchases.md)
