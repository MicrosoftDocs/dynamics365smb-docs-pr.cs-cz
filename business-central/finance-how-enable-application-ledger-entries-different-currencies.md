---
title: Apply Entries in Different Currencies| Microsoft Docs
description: You can apply ledger entries in multiple currencies, for example, if you sell in one currency and receive payment in another.
services: project-madeira
documentationcenter: ''
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 10/01/2019
ms.author: edupont

---
# Povolení vyrovnávání položek v různých měnách
Pokud nakupujete od dodavatele v jedné měně a odešlete platbu v jiné měně, můžete vyrovnat platbu s nákupem.

Stejně tak, pokud prodáváte zákazníkovi v jedné měně a obdržíte platbu v jiné měně, můžete platbu vyrovnat prodejní fakturou.

Následující postup popisuje, jak nastavit vyrovnání položek dodavatele na stránce **Nastavení nákupu a závazků**. Nastavení je podobné pro položky zákazníka na stránce **Nastavení prodeje a pohledávek.**

## Povolení vyrovnávání položek dodavatele v různých měnách
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení prodeje a poheldávek** a vyberte související odkaz.
2. V poli **Vyrovnání  mezi měnami** a vyberte následující možnosti.

| Možnost | Popis |
| --- | --- |
| Žádné | Vyrovnání mezi měnami není povoleno. |
| EMU | Vyrovnání mezi měnami EMU je povoleno. |
| Všechno | Vyrovnání mezi všemi měnami je povoleno. |

## Nastavení účtů účetní osnovy pro rozdíly zaokrouhlení při měnovém vyrovnání
Pokud vyrovnáte položky v různých měnách, musíte nastavit účty hlavní knihy, na které chcete zaúčtovat rozdíly zaokrouhlování.

> Před tím, než dokončíte vyrovnávání musítě mít tyto účty založeny a nastaveny. Pro více informací navštivtě [Porozumění financím a účetní osnově](finance-general-ledger.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Účto skupiny zákazníků** a vyberte související odkaz.
2. V polích **MD účet  zaok. vyrovnání měny** a **Dal účet. zaok. vyrovnání měny** zadejte příslušné účty hlavní knihy a zaúčtujte rozdíly zaokrouhlování.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Účto skupiny dodavatele** a vyberte související odkaz.
4. V polích **MD účet  zaok. vyrovnání měny** a **Dal účet. zaok. vyrovnání měny** zadejte příslušné účty hlavní knihy a zaúčtujte rozdíly zaokrouhlování.

## Viz také
[Správa závazků](payables-manage-payables.md)  
[Správa pohledávek](receivables-manage-receivables.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
