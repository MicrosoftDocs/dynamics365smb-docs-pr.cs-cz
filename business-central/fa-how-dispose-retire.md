---
title: Dispose or Retire FA| Microsoft Docs
description: You must post a disposal value when you scrap, sell, or retire a fixed asset.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 04/01/2020
ms.author: sgroespe

---
# Likvidace nebo vyřazení dlouhodobého majetku
Pokud prodáváte nebo jinak vyřazujete dlouhodobý majetek, musí být za účelem výpočtu a zaznamenání zisku nebo ztráty zaúčtována hodnota vyřazení. Položka vyřazení musí být poslední položkou zaúčtovnou pro dlouhodobý majetek. U částečně vyřazeného dlouhodobého majetku můžete zaúčtovat více než jednu položku vyřazení. Součet všech zaúčtovaných částek likvidace musí být částka Dal.

> [!NOTE]
> Pokud vyměňujete dlouhodobý majetek za jiný, musíte zaznamenat jak prodej starého aktiva (vyřazení), tak nákup nového (akvizice). Pro více informací navštivte [Získání dlouhodobého majetku](fa-how-acquire.md).

## Zaúčtování vyřazení z finančního deníku dlouhodobého majetku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deník DM** a poté vyberte související odkaz.
2. Vytvořte počáteční řádek deníku a vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. V poli **Typ účtování DM** vyberte **Vyřazení**.
4. Vyberte akci **Vložit protiúčet  DM**. Druhý řádek deníku je vytvořen pro protiúčet, který je nastaven pro zaúčtování vyřazení.

   > [!NOTE]
   > Krok 4 funguje, pouze pokud jste nastavili následující položky: Na stránce **Karta účto skupiny DM** pro účto skupinu dlouhodobého majetku musí pole **Účet vyřazení DM** obsahovat účet Dal hlavní knihy a pole **Protiúčet  vyřazení** musí obsahovat účet hlavní knihy, na který chcete zaúčtovat vyrovnávací položky. Pro více informací navštivte [Nastavení účto skupin dlouhodobého majetku](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Vyberte akci **Účtovat**.

Pokud prodáváte nebo likvidujete část dlouhodobého majetku, musíte majetek před zaznamenáním transakce vyřazení rozdělit. Pro více informací navštivte [Převod, Rozdělení nebo Kombinování dlouhodobého majetku](fa-how-trans-split-combine.md).

## Zobrazení položek vyřazení
Při prodeji nebo vyřazení dlouhodobého majetku je hodnota vyřazení zaúčtována do hlavní knihy, kde můžete zobrazit výsledek.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dlouhodobý majetek** a poté vyberte související odkaz.
2. Vyberte dlouhodobý majetek, pro který chcete zobrazit položky, a pak zvolte akci **Knihy odpisů**.
3. Vyberte knihu odpisů, pro kterou chcete zobrazit položky, a pak zvolte akci **Položky**.
4. V poli **Kategorie účtování DM** vyberte řádek s hodnotou **Vyřazení** a potom vyberte akci **Navigovat**.
5. Na stránce **Navigovat** vyberte řádek položky hlavní knihy a pak zvolte akci **Zobrazit**.

Otevře se stránka **Věcné položky**, kde můžete zobrazit položky, ve kterých bylo vyřazení zaúčtováno.

## Viz také
[Dlouhodobý majetek](fa-manage.md)  
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
