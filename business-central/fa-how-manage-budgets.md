---
title: Manage FA Budgets| Microsoft Docs
description: You set up information about future investments, disposals, and depreciation of fixed assets to help prepare budgets and forecasts.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 04/01/2020
ms.author: sgroespe

---
# Správa rozpočtů dlouhodobého majetku
Můžete nastavit rozpočty dlouhodobého majeteku. To vám například umožní zahrnout do sestav očekávané akvizice a prodeje.

K přípravě vaší výsledovky, rozpočtované rozvahy a hotovostního rozpočtu potřebujete informace o budoucích investicích, úbytcích a odpisech dlouhodobého majetku. Tyto informace můžete získat ze sestavy **Dlouhodobý majetek-očekávaná hodnota**. Před tiskem této zprávy musíte připravit rozpočet.

## Rozpočet nákladů na pořízení dlouhodobého majetku
Chcete-li připravit rozpočet, musíte nastavit karty dlouhodobého majetku pro dlouhodobý majetek, který chcete v budoucnu koupit. Dlouhodobý rozpočtový majetek je nastaven jako běžný dlouhodobý majetek, ale musí být nastaven tak, aby se nezaúčtoval do věcných položek.

Když účtujete náklady na pořízení, zadáte číslo rozpočtového dlouhodobého majetku do pole **Číslo rozpočtu DM**. Tím se zaúčtují náklady na pořízení s opačným znaménkem pro rozpočtový majetek. To znamená, že celkové náklady na pořízení rozpočtového majetku jsou rozdílem mezi rozpočtovými a skutečnými náklady na pořízení.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dlouhodobý majetek** a poté vyberte související odkaz.
2. Vyberte akci **Nový** a vytvořte novou kartu dlouhodobého majetku pro dlouhodobý majetek s rozpočtem.
3. Zaškrtnutím políčka **Rozpočtový majetek** zabráníte účtování do věcných položek.
4. Vyplňte zbývající pole, přiřaďte knihu odpisů a poté zaúčtujte první náklady na pořízení s rozpočtovaným dlouhodobým majetkem zadaným v poli **Číslo rozpočtu DM** na řádku deníku. Pro více informací navštivte [Získání dlouhodobého majetku](fa-how-acquire.md).

## Rozpočet na vyřazení dlouhodobého majetku
Pokud plánujete prodat majetek v rozpočtovém období, můžete zadat informace o prodejní ceně a datu prodeje.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dlouhodobý majetek** a poté vyberte související odkaz.
2. Vyberte dlouhodobý majetek, který má být vyřazen, a pak zvolte akci **Knihy odpisů**.
3. Na stránce **Knihy odpisů DM** vyplňte pole **Plánované datum vyřazení** a **Plánovaný výsledek vyřazení**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Zobrazení hodnot plánované likvidace
Chcete-li zobrazit hodnoty předpokládaného vyřazení a vypočítat zisk a ztrátu, můžete použít sestavu **Očekávaná hodnota DM**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Očekávaná hodnota DM** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole.
3. Vyberte tlačítko **Tisk** nebo **Náhled**.

## Odpisy rozpočtu
Sestavu **Dlouhodobý majetek-očekávaná hodnota** můžete použít k výpočtu budoucího odpisu. Sestava zobrazuje účetní hodnotu a akumulované odpisy na začátku vybraného období, změny během období a účetní hodnotu a akumulované odpisy na konci vybraného období.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dlouhodobý majetek-očekávaná hodnota** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole.
3. Chcete-li zobrazit celkové hodnoty pro veškerý majetek, zrušte zaškrtnutí políčka **Tisk dle DM**.
4. Záložku **Dlouhodobý majetek** ponechte prázdnou, aby byl zahrnut veškerý majetek. Do pole **Rozpočtový majetek** zadejte **Ne**, chcete-li vyloučit rozpočtový majetek, nebo  **Ano**, chcete-li zobrazit pouze rozpočtový majetek.
5. Vyberte tlačítko **Tisk** nebo **Náhled**.

## Viz také
[Dlouhodobý majetek](fa-manage.md)  
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
