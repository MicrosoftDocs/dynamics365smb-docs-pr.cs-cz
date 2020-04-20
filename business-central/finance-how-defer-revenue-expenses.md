---
title: Defer Revenues and Expenses| Microsoft Docs
description: To recognize revenues and expenses in periods other than the period in which the transaction was posted, you can automatically defer or postpone them over a specified schedule.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 10/01/2019
ms.author: sgroespe

---
# Odložení příjmů a výdajů
Chcete-li uznat příjmy nebo výdaje v jiném období, než je období, ve kterém byla transakce zaúčtována, můžete použít funkce automaticky odložit výnosy a výdaje nad zadaný plán.

Chcete-li rozdělit příjmy nebo výdaje v příslušných účetních obdobích, nastavte šablonu odkladu pro zdroj, položku nebo účet hlavní knihy, do kterého se budou účtovat příjmy nebo výdaje. Když zaúčtujete související prodejní nebo nákupní doklad, příjmy nebo výdaje se odloží do příslušných účetních období, v souladu s plánem odkladu, který se řídí nastavením v šabloně odkladu a datem zaúčtování.

## Nastavení finančního účtu pro časově rozlišení
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vyplňte pole podle potřeby k vytvoření finančního účtu pro odložené příjmy. Pro více informací navštivte [Hlavní kniha a účetní osnova](finance-general-ledger.md).
4. Opakováním kroků 2 a 3 vytvořte nový finanční účet pro odložené výdaje.

U obou typů odkladů vyberte v poli **Typ** hodnotu **Rozvaha** a odpovídajícím způsobem pojmenujte účty, například „Nezaslaný příjem“ pro odložené příjmy a „Neuhrazené výdaje“. pro odložené výdaje.

## Nastavení šablony časového rozlišení
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony časového rozlišení** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Podle potřeby vyplňte pole.
4. V poli **Metoda  výpočtu** určete způsob výpočtu pole **Částka** pro každé období na stránce **Plán časového rozlišení**. Můžete si vybrat mezi následujícími možnostmi:

   * **Lineární**: Pravidelné odložené částky se počítají podle počtu periody, rozdělené podle délky periody.
   * **Stejně za období**: Periodické odložené částky se počítají podle počtu period rovnoměrně rozložených podle období.
   * **Dní za období**: Částky periodického odkladu se počítají podle počtu dní v období.
   * **Uživatelsky definovaná**: Částky periodického odkladu se nepočítají. Na stránce Časový plán odkladu musíte ručně vyplnit pole **Částka** pro každé období. Další informace naleznete v části „Změna plánu časového rozlišení z prodejní faktury“.
5. V poli **Popis období** zadejte popis, který bude zobrazen u položek pro účtování odložení. Můžete zadat následující zástupné kódy pro typické hodnoty, které budou vloženy automaticky při zobrazení popisu období.

   * %1 = Číslo dne zúčtovacího data období
   * %2 = Číslo týdne zúčtovacího data období
   * %3 = Číslo měsíce zúčtovacího data období
   * %4 = Název měsíce zúčtovacího data období
   * %5 = Název účetního zúčtovacího data období
   * %6 = Fiskální rok zúčtovacího data období

Příklad: Zúčtovací datum je 02/06/2016. Pokud zadáte „Odložené výdaje pro %4 %6“, bude zobrazený popis „Odložené výdaje za únor 2016“.

## Přiřazení šablony časového rozlišení ke zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony časového rozlišení** a poté vyberte související odkaz.
2. Otevřete kartu pro zboží, u níž musí být příjmy nebo výdaje odloženy na účetní období, kdy bylo zboží prodáno nebo zakoupeno.
3. V poli **Výchozí šablona časového rozlišení** vyberte příslušnou šablonu.

## Změna plán časového rozlišení z prodejní faktury
> [!NOTE]
> Kroky v tomto postupu jsou stejné jako při změně plánu časového rozlišení z nákupní faktury.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktury** a poté vyberte související odkaz.
2. Vytvořte prodejní fakturu pro zboží, které má přiřazenu šablonu časového rozlišení. Pro více informací navštivte [Faktury prodeje](sales-how-invoice-sales.md).

   Všimněte si, že jakmile na řádku faktury zadáte zboží (nebo zdroj nebo účet hlavní knihy), pole **Kód časového rozlišení** je vyplněno kódem přiřazené šablony časového rozlišení.
3. Vyberte akci **Plán časového rozlišení**.
4. Na stránce **Plán časového rozlišení** změňte nastavení v záhlaví nebo hodnoty na řádcích, například odložte částku do dalšího účetního období.
5. Vyberte akci **Vypočítat plán**.
6. Vyberte tlačítko **OK**. Plán časového rozlišení je aktualizován pro prodejní fakturu. Související šablona časového rozlišení se nezmění.

## Zobrazení náhledu, jak budou odložené příjmy nebo výdaje zaúčtovány do hlavní knihy
> [!NOTE]
> Kroky v tomto postupu jsou stejné jako při náhledu způsobu účtování odkladů výdajů.

1. Na stránce **Prodejní faktury** vyberte akci **Náhled účtování**.
2. Na stránce **Náhled účtování** vyberte akci **Věcné položky** a poté vyberte akci  **Zobrazit související položky**.

Věcné položky, které mají být zaúčtovány na určený účet odkladu, například Nezaslaný příjem, jsou označeny popisem, který jste zadali do pole **Popis období** v šabloně odkladu, například “ Odložené výdaje za únor 2016 “.

## Kontrola zaúčtovaných odkladů v sestavě Souhrn časového rozlišení prodeje
> [!NOTE]
> Kroky v tomto postupu jsou stejné jako při prohlížení sestavy Souhrn časového rozlišení nákupu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Souhrn časového rozlišení prodeje** a poté vyberte související odkaz.
2. Na stránce **Souhrn časového rozlišení prodeje** zadejte do pole **Zůstatek k** datum, do kterého chcete zobrazit odložené výnosy.
3. Vyberte tlačítko **Náhled**.

## Viz také
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Práce s finančními deníky](ui-work-general-journals.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
