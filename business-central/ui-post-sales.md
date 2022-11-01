---
title: Posting Sales Documents
description: Learn about the different posting functions to post sales documents, and how you can update posted documents.
author: SorenGP


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: 130, 142, 1350
ms.date: 04/01/2021
ms.author: edupont

---
# Účtování prodeje

V nabídce  **Účtování** v prodejním dokladu si můžete vybrat mezi následujícími účtovacími funkcemi:

* **Účtovat**
* **Účtovat a nový**
* **Účtovat a Odeslat**
* **Náhled účtování**
* **Dávkové účtování**
* **Testovací sestava**

> [!NOTE]
> U prodejních objednávek můžete také vidět možnosti související s funkcí prodejních záloh. Další informace naleznete v tématu [ Fakturace záloh](finance-invoice-prepayments.md).

Jakmile vyplníte všechny řádky a zadáte všechny informace o prodejní objednávce, můžete ji zaúčtovat. Tím se vytvoří dodávka a faktura.

Po zaúčtování prodejní objednávky se aktualizuje účet zákazníka, věcné položky a položky zboží.

Pro každou prodejní objednávku se v tabulce **Věcná položka** vytvoří záznam o prodeji. Položka je také vytvořena na účtu zákazníka v **Položkách ákazníka<f0> a věcné položky se vytvoří na příslušném účtu pohledávek. Kromě toho může odeslání objednávky vést k zadání DPH a zápisu věcných položek pro částku slevy. Zveřejnění záznamu o slevě závisí na obsahu pole **Účtování slevy** na stránce **Nastavení prodeje a pohledávek**.

Pro každou řádek prodejní objednávky bude v tabulce **Položka zboží** vytvořena věcná položka (pokud prodejní řádky obsahují čísla položek) nebo bude věcná položka vytvořena v tabulce **Věcná položka** (pokud prodejní řádky obsahují účet hlavní knihy). Kromě toho jsou prodejní objednávky vždy zaznamenány v tabulkách **Hlavička prodejní dodávky** a **Hlavička prodejní faktury**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Můžete buď účtovat, nebo účtovat a odeslat. Pokud se rozhodnete účtovat a odeslat, vygeneruje se soubor PDF, který pak můžete odeslat. Můžete také zvolit funkci **Dávkové účtování**, která vám umožní zaúčtovat několik objednávek současně. Další informace naleznete v tématu [Dávkové účtování dokladů](ui-batch-posting.md).

## Zobrazení položek

Po dokončení účtování budou zaúčtované řádky z objednávky odstraněny. Po dokončení účtování se zobrazí zpráva. Poté budete moci zobrazit zaúčtované položky na různých stránkách, které obsahují zaúčtované položky, například **Zák. zákazníka**, **Věcné položky**, **Položky zboží**, **Účtované prodejní dodávky** a **Účtované prodejní faktury**.

Ve většině případů můžete otevřít položky z příslušné karty nebo dokladu. Například na stránce **Karta zákazníka** vyberte akci **Položky zákazníka**.

## Úprava položek

Můžete upravit některá pole na zaúčtovaných nákupních dokladech, jako je pole **Číslo sledování zásilky**. Další informace naleznete v tématu [Úprava účtovaných dokladů](across-edit-posted-document.md). U kritičtějších polí, která ovlivňují audit, je třeba účtování vrátit nebo zrušit. Další informace naleznete v tématu [Zpětné účtování deníku a Vrácení příjemek/dodávek zpět](finance-how-reverse-journal-posting.md).

## Podívejte se na související školení na webu [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)

## Viz také

[Prodej](sales-manage-sales.md)  
[Dávkové účtování dokladů](ui-batch-posting.md)  
[Úprava účtovaných dokladů](across-edit-posted-document.md)  
[Odesílání dokladů pomocí e-mailu](ui-how-send-documents-email.md)  
[Oprava nebo zrušení nezaplacených prodejních faktur](sales-how-correct-cancel-sales-invoice.md)  
[Vyhledávání stránek a informací pomocí Řekněte mi](ui-search.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
