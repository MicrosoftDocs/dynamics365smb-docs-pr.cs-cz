---
title: Record Billable and Budgeted Usage of Job Resources| Microsoft Docs
description: Describes how to record the consumption or usage of items or resources on jobs to facilitate project management.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, consumption
ms.date: 10/01/2019
ms.author: sgroespe

---
# Zaznamenání spotřeby pro projekty
Na stránce **Řádky plánování projektu**, můžete zkontrolovat a zaznamenat použití na různých částech vašeho projektu, která se automaticky aktualizuje, když upravujete a přenášíte informace mezi projekty a deníky projektů nebo fakturami projektu. To vyžaduje, abyste nastavili projekt tak, aby byla možnost **Použít propojení spotřeby jako výchozí** zapnuta. Pro více informací navštivte [Nastavení projektů](projects-how-setup-jobs.md).

Například pro řádky plánování typu **Rozpočet**, můžete zadat množství zdroje a určit, jaké množství se má převést do deníku úlohy. Pokud je typ řádku plánování **Fakturovatelné**, můžete zadat množství zdroje a uvést, jaké množství chcete převést na fakturu. Porovnáním množství, které bylo převedeno do deníku nebo faktury se zbývajícím množstvím, můžete rychle zkontrolovat informace o spotřebě.

Následující postupy popisují, jak zaznamenat skutečné (fakturovatelné) nebo rozpočtové ceny a náklady na projekt. Pro více informací o odhadu rozpočtovaných hodnot během plánování navštivte [Správu rozpočtů projektu](projects-how-manage-budgets.md).

## Záznam spotřeby řádku plánování projektu typu Budget
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Vyberte příslušnou úlohu a pak zvolte akci **Řádky plánování projektu**.
3. Vyberte řádek plánování projektu typu **Rozpočet**, nebo **Rozpočet a fakturovatelné** pro který chcete spotřebu zaznamenat.
4. Na poli **Množství k transferu do deníku**, zadejte číslo, které chcete převést. Výchozí množství je hodnota, která se zadává do pole **Množství**.

   Pole **Zbývající množství** zobrazuje množství, které zbývá pro dokončení projektu a bude přeneseno do deníku.
5. Vyberte akci **Vytvořit projekt Řádky projektu**.
6. Na stránce **Transfer projektu - řádek plánování projektu**, vyplňte pole podle potřeby a poté vyberte tlačítko **OK**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Zvolte akci **Otevřít deník projektu**.
8. Na stránce **Deník projektů**, vyberte příslušný řádek a poté vyberte akci **Účtovat**.
9. Na stránce **Řádky plánování projektu**, zkontrolujte zaznamenané využití sledováním polí **Množství**, **Zbývající množství**, a **Množství k transferu do deníku**.
10. Opakujte kroky 3 až 8, abyste zaznamenali další využití.

## Záznam spotřeby řádku plánování projektu typu Fakturovatelné
V další úloze také zaznamenáte spotřebu, ale pro řádek plánování projektu typu **Fakturovatelné**. Obvykle v tomto případě fakturujete využití, ale můžete jej také do deníku převést. Pokud tak však učiníte, vytvoří se řádek plánování projektu typu **Rozpočet**, který odpovídá fakturovatelnému řádku. Pro více informací navštivte [Správu rozpočtů projektu](projects-how-manage-budgets.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Vyberte příslušnou úlohu a pak zvolte akci **Řádky plánování projektu**.
3. Vyberte řádek plánování projektu typu **Fakturovatelné** pro který chcete zaznamenat využití.
4. Na poli **Množství k transf. k fakturaci.** zadejte číslo, které chcete převést. Výchozí množství je hodnota, která se zadává do pole **Množství**.

   Pole **Množství k fakturaci** zobrazuje množství, které zbývá do dokončení projektu a bude vyfakturováno.
5. Zvolte akci **Vytvořit prodejní fakturu**.
6. Na stránce **Transfer projektu do prodejní faktury**, vyplňte pole podle potřeby a poté vyberte tlačítko **OK**.
7. Na stránce **Řádky plánování projektu**, vyberte příslušný řádek a poté vyberte akci **Účtovat**.
8. Zkontrolujte zaznamenané využití sledováním polí **Množství**, **Množství k fakturaci**, **Množství  k transf. k fakturaci** a pokud je zaúčtována prodejní faktura **Fakturované množství**.
9. Opakujte kroky 3 až 8, abyste zaznamenali další využití.
10. Chcete-li zkontrolovat související zaúčtovanou prodejní fakturu, zvolte akci **Prodejní faktury/Dobropisy**.
11. Na stránce **Faktury projektu**, vyberte příslušnou fakturu a poté vyberte akci **Otevřená prodejní faktura/dobropis**.

## Vytvoření řádků deníku projektu z řádků plánování projektu
Až budete připraveni k zaúčtování finančních informací pro projekty, musíte vytvořit řádky deníku projektů, které můžete zaúčtovat.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Vyberte příslušný otevřený projekt a poté vyberte akci **Řádky plánování projektu**.
3. Na stránce **Řádky plánování projektu**, na příslušném řádku plánování projektu v poli **Množství k transferu do deníku**, zadejte množství, které chcete přenést do deníku projektu.
4. Vyberte akci **Vytvořit projekt Řádky projektu**.
5. Na stránce **Transfer projektu - řádek plánování projektu**, vyplňte pole podle potřeby.
6. Zvolte tlačítko **OK**. Vytvoří se řádky deníku projektu
7. Chcete-li převod ověřit, otevřete příslušný list deníku projektů a zkontrolujte položky.
8. Po dokončení řádků deníku projektů zvolte akci **Účtovat**.

## Ruční vytvoření řádků deníku projektů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky projektů** a poté vyberte související odkaz.
2. V poli **Název listu**, zvolte příslušný list deníku projektů.
3. Na novém řádku zadejte číslo dokladu, číslo projektu, číslo úlohy projektu, typ a množství spotřebovaného typu.
4. Po dokončení řádků deníku projektů zvolte akci **Účtovat**.

## Kontrola řádků plánování pro položku projektu
Po zaúčtování řádků deníku projektů můžete zobrazit řádky plánování, které jsou přidruženy k položkám deníku projektu, které byly zaúčtovány.

> [!NOTE]
> To vyžaduje, aby bylo pro projekt zaškrtnuto políčko **Použít propojení spotřeby jako výchozí**, nebo aby bylo ve výchozím nastavení pro všechny projekty ve vaší organizaci. Pro více informací navštivte [Nastavení projektů](projects-how-setup-jobs.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky projektů** a poté vyberte související odkaz.
2. Vyberte příslušný deník projektů a pak zvolte akci **Položky hlavní knihy**.
3. Na stránce **Položky projektu**, zvolte akci **Zobrazit připojené řádky plánování projektu**.

## Viz také
[Správa projektů](projects-manage-projects.md)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
