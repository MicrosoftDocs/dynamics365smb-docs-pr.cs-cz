---
title: Post Intercompany Documents and Journals| Microsoft Docs
description: Use intercompany documents to post transactions with your intercompany partners.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 10/01/2019
ms.author: sgroespe

---
# Práce s vnitropodnikovými doklady a deníky
K účtování transakcí s vašimi partnery v rámci společnosti používáte vnitropodnikové doklady nebo deníky. Když ve společnosti zaúčtujete vnitropodnikový doklad nebo řádek deníku, vytvoří se odpovídající řádek dokladu nebo deníku ve vnitropodnikové poště k odeslání, kterou můžete přenést na svého partnera. Váš partner pak může zaúčtovat odpovídající transakci ve své společnosti, aniž by musel znovu zadávat data.

U prodejních a nákupních dokladů zajišťuje kód vnitropodnikového partnera na příslušném odběrateli nebo dodavateli, že všechny objednávky a faktury vytvořené v případě transakcí s těmito společnostmi budou v partnerské společnosti vytvářet odpovídající doklady a vést ke správnému přiřazení účtů.

U řádku vnitropodnikového finančního deníku nemusíte specifikovat účty pro jednotlivou sadu knih, ale jednoduše uveďte identifikaci partnerské společnosti. Odpovídající řádky vnitropodnikového finančního deníku jsou pak vytvořeny v partnerské společnosti, což vede k vyrovnání účetních knih obou společností zapojených do transakce.

## Vyplnění a odeslání vnitropodnikové prodejní objednávky
Před zaúčtováním můžete odeslat prodejní a nákupní objednávky a vratky. Faktury a dobropisy nelze odeslat, dokud nejsou zaúčtovány.

Následující postup popisuje, jak vyplnit a odeslat vnitropodnikovou prodejní objednávku. Stejné kroky se vztahují na vnitropodnikové objednávky a vratky a na zaúčtované vnitropodnikové faktury a dobropisy.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Vyberte **Nový** a vytvořte novou prodejní objednávku. Pro více informací navštivte [Prodávání produktů](sales-how-sell-products.md).
3. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Ujistěte se, že zákazník je vnitropodnikový partner.
5. Chcete-li objednávku odeslat před zaúčtováním, vyberte akci **Odeslat vnitropodnikovou prodejní objednávku**.

> [!NOTE]
> Pokud provedete krok 4, bude prodejní objednávka přesunuta do vaší vnitropodnikové pošty k odeslání, kde ji můžete odeslat později. Pro více informací navštivte [Správa vnitropodnikové doručené pošty a pošty k odeslání](intercompany-how-manage-intercompany-inbox.md).

## Vyplnění a zaúčtování vnitropodnikového deníku
Když ve vaší společnosti zaúčtujete řádek vnitropodnikového finančního deníku, vytvoří se odpovídající řádek deníku ve vnitropodnikové poště k odeslání, kterou můžete převést na svého partnera. Váš partner pak může zaúčtovat odpovídající transakci ve své společnosti, aniž by musel znovu zadávat data.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodnikové finanční deníky** a poté vyberte související odkaz.
2. Otevřete příslušný list deníku. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).
3. Podle potřeby vyplňte pole.
4. Do pole **Číslo fin.účtu vnitrop.  partnera** zadejte vnitropodnikový účet hlavní knihy, na který bude částka zaúčtována ve společnosti vašeho partnera.

   > [!NOTE]
   > Toto pole musí být vyplněno na řádku s bankovním účtem nebo účtem hlavní knihy v poli **Číslo účtu** nebo **Číslo  protiúčtu**.
5. Vyberte akci **Účtovat**.

Příslušné položky jsou zaúčtovány ve vaší společnosti a ve vnitropodnikové poště k odeslání je vytvořen deník s odpovídajícími položkami, které můžete odeslat partnerské společnosti. Pro více informací navštivte [Správa vnitropodnikové doručené pošty a pošty k odeslání](intercompany-how-manage-intercompany-inbox.md).

## Viz také
[Správa vnitropodnikových transakcí](intercompany-manage.md)  
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Práce s finančními deníky](ui-work-general-journals.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
