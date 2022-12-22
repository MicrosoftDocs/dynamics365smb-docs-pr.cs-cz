---
title: Post Purchase Documents
description: Learn about the different posting functions to post purchase documents, and how to update posted documents.
author: SorenGP


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: 
ms.date: 06/24/2021
ms.author: edupont

---
# Účtování nákupů
Na nákupním dokladu si můžete vybrat mezi následujícími akcemi účtování:

* **Účtovat**
* **Náhled účtování**
* **Post and Print**
* **Testovací sestava**
* **Dávkové účtování**

Při zaúčtování nákupního dokladu se aktualizuje účet dodavatele, věcné položky, položky zboží a položky zdrojů.

Pro každý nákupní doklad se vytvoří nákupní záznam v tabulce **Věcná položka**. Položka se také vytvoří na účtu dodavatele v tabulce **Položka dodavatele** a věcná položka se vytvoří na příslušném účtu závazků. Kromě toho může zaúčtování nákupu vést k položce DPH a věcné položce pro částku slevy. Zveřejnění záznamu o slevě závisí na obsahu pole **Účtování slevy** na stránce **Nastavení nákupu a závazků**.

Pro každý řádek nákupu budou vytvořeny následující položky:
- Položka v tabulce **Položky zboží** pokud je řádek nákupu typu **zboží**.
- Položka v tabulce **Věcná položka** pokud jsou nákupní řádky typu **Finanční účet**
- Položka v tabulce **Položky zdrojů** pokud je řádek nákupu typu **zdroj**.

Kromě toho jsou nákupní doklady vždy zaznamenány v **Hlavičce Nák. Příjemky** a **Hlavičce Nák. Faktury**.

Než začnete účtovat, můžete si vytisknout testovací sestavu, která obsahuje všechny informace o nákupní objednávce a naznačuje případné chyby. Chcete-li sestavu vytisknout, zvolte **Účtování**, a poté zvolte **Testovací sestava**.

> [!IMPORTANT]  
> Když zaúčtujete objednávku na zboží, můžete vytvořit příjemku i fakturu. To lze provést současně nebo nezávisle. Můžete také vytvořit částečný příjem a částečnou fakturu vyplněním **Množství k příjmu** a **Množství k fakturaci** na jednotlivých řádcích nákupní objednávky před zaúčtováním. Všimněte si, že nelze vytvořit fakturu za něco, co nebylo přijato. To znamená, že před fakturací musíte mít zaznamenanou příjemku, nebo se musíte rozhodnout zda přijímat a fakturovat současně.

Můžete buď účtovat, nebo účtovat a odeslat. Pokud se rozhodnete účtovat a vytisknout, po zaúčtování objednávky se vytiskne sestava. Můžete také zvolit funkci **Dávkové účtování**, která vám umožní zaúčtovat několik objednávek současně. Další informace naleznete v tématu [Dávkové účtování dokladů](ui-batch-posting.md).

## Zobrazení položek
Po dokončení účtování budou zaúčtované nákupní řádky z objednávky odstraněny. Po dokončení účtování se zobrazí zpráva. Poté budete moci zobrazit zaúčtované položky na různých stránkách, které obsahují účtované položky, jako jsou stránky**Položky dodavatele**, **Věcné položky**, **Položky zboží**, **Položky zdrojů**, **Nákupní příjemky** a **Účtované nákupní faktury**.

Ve většině případů můžete otevřít věcné položky z dané karty nebo dokumentu. Například na stránce **Karta dodavatele** vyberte akci **Položky dodavatele**.

## Úprava položek
Můžete upravit některá pole na zaúčtovaných nákupních dokladech, jako je pole **Platební reference**. Další informace naleznete v tématu [Úprava účtovaných dokladů](across-edit-posted-document.md). U kritičtějších polí, která ovlivňují audit, je třeba účtování vrátit nebo zrušit. Další informace naleznete v tématu [Zpětné účtování deníku a Vrácení příjemek/dodávek zpět](finance-how-reverse-journal-posting.md).

## Podívejte se na související školení na webu [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## Viz také
[Úprava účtovaných dokladů](across-edit-posted-document.md)  
[Dávkové účtování dokladů](ui-batch-posting.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Účtování dokladů a deníků](ui-post-documents-journals.md)  
[Úprava nebo zrušení nezaplacených nákupních faktur](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Vyhledávání stránek a informací pomocí Řekněte mi](ui-search.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]