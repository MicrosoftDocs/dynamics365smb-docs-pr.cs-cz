---
title: Depreciate or Amortize FA| Microsoft Docs
description: You must define how you will write-down, depreciate, or amortize each of your fixed assets.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 04/01/2020
ms.author: sgroespe

---
# Odpis nebo amortizace dlouhodobého majetku
Odpisy se používají k rozdělení nákladů na dlouhodobý majetek, jako jsou stroje a zařízení, po dobu jejich odpisovatelnosti. Pro každý dlouhodobý majetek je nutné definovat, jak bude odepsán.

Existují dva způsoby, jak zaúčtovat odpisy:

* Automaticky spuštěním dávkové úlohy **Výpočet odpisů**.
* Ručně pomocí finančního deníku dlouhodobého majetku.

[!INCLUDE[d365fin](includes/d365fin_md.md)] může vypočítat denní odpisy, které umožňují vypočítat odpisy pro libovolné období. Můžete tedy analyzovat aktuální provozní výsledky například na měsíční, čtvrtletní nebo roční bázi. Výpočet používá standardní rok 360 dní a standardní měsíc 30 dní. Pro více informací navštivte [Metody odpisování](fa-depreciation-methods.md).

Používá-li dlouhodobý majetek více oddělení, lze těmto oddělením automaticky přidělit pravidelné odpisy podle uživatelsky definované alokační tabulky.

Nesprávné položky odpisů můžete zrušit pomocí dávkové úlohy **Storno položek DM**. Poté můžete zaúčtovat správné množství opětovným spuštěním dávkové úlohy **Výpočet odpisů**. Chyby, které opravíte, jsou zaúčtovány jako chybné položky dlouhodobého majetku.

Indexace se používá k úpravě hodnot pro obecné změny cenové hladiny. Pro přepočet odpisových částek můžete použít dávkovou úlohu **Indexace dlouhodobého majetku**.

## Automatický výpočet odpisů
Jednou za měsíc nebo kdykoli se rozhodnete, můžete spustit dávkovou úlohu **Výpočet odpisů**. Dávková úloha ignoruje dlouhodobý majetek, který byl prodán, je blokován nebo neaktivní, nebo používa metodu ručního odpisu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výpočet odpisů** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vyberte tlačítko **OK**.

   Dávková úloha vypočítá odpisy a vytvoří řádky ve finančním deníku dlouhodobého majetku.

4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky DM** a poté vyberte související odkaz.

   Na stránce **Finanční deník DM** v poli **Počet  dní odpisu** můžete vidět, kolik dní odpisů bylo vypočteno.
5. Vyberte akci **Účtovat**.

## Ruční zaúčtování odpisů z finančního deníku dlouhodobého majetku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deník DM** poté vyberte související odkaz.
2. Vytvořte počáteční řádek deníku a vyplňte pole podle potřeby.
3. V poli **Typ účtování DM** vyberte **Odpisy**.
4. Vyberte akci **Vložit protiúčet  DM**. Druhý řádek deníku je vytvořen pro protiúčet, který je nastaven pro zaúčtování odpisů. Pro více informací navštivte [Nastavení účto skupin dlouhodobého majetku](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Chcete-li deník zaúčtovat, vyberte akci **Účtovat**.

Pole **Účetní hodnota** na stránce **Karta DM** se odpovídajícím způsobem aktualizuje.

Pokud jste nastavili klíče přidělení dlouhodobého majetku pro přidělení částek různým oddělením nebo projektům, částky jsou přiděleny během účtování. Pro více informací navštivte [Nastavení obecných informací o dlouhodobém majetku](fa-how-setup-general.md).

## Správa koncové účetní hodnoty
V poli **Konečná účetní hodnota** na stránce **Knihy odpisů DM** můžete určit účetní hodnotu, kterou má mít dlouhodobý majetek v aktuální knize odpisů poté, co byl plně odepsán. Můžete to provést ručně nebo můžete vyplnit pole **Výchozí konečná úč.hodnota** na související stránce **Kniha odpisů**, která pak bude použita k automatickému vyplnění pole.

> [!NOTE]
> Pokud poslední odpisy znamenají, že pole **Účetní hodnota** na stránce **Karta DM** je nula, poslední odpisy se automaticky sníží o tuto částku.<br /><br />
> Pokud je hodnota v poli **Účetní hodnota** po posledním odpisování větší než nula, například kvůli problému se zaokrouhlením nebo protože existuje hodnota záchrany, je hodnota v poli **Konečná účetní hodnota** na stránce **Knihy odpisů DM** ignorována. Pro více informací navštivte [Zaúčtování hodnoty při vyřazení spolu s náklady na pořízení](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## Výpočet alokací ve finančním deníku dlouhodobého majetku
Pokud je dlouhodobý majetek používán několika odděleními, mohou být pravidelné odpisy automaticky přiděleny těmto oddělením podle uživatelem definované alokační tabulky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deník DM** poté vyberte související odkaz.
2. Vytvořte počáteční řádek a vyplňte pole podle potřeby.
3. V poli **Typ účtování DM** vyberte **Přidělení**.
4. Vyberte akci **Vložit protiúčet  DM**. Druhý řádek deníku je vytvořen pro protiúčet, který je nastaven pro zaúčtování přidělení.
5. Chcete-li deník zaúčtovat, vyberte akci **Účtovat**.

## Použití seznamů duplikací k přípravě na zaúčtování do více knih odpisů
Když vyplňujete řádky deníku k zaúčtování do knihy odpisů, můžete je duplikovat v samostatném deníku, abyste mohli zaúčtovat do jiné knihy odpisů. Pro více informací navštivte [Zaúčtování položek do různých knih odpisů](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Knihy odpisů** a poté vyberte související odkaz.
2. Otevřete knihu odpisů a potom zaškrtněte políčko **Část seznamu duplikací**.

> [!IMPORTANT]
> Pokud jste vybrali pole **Použít seznam duplikátů**, nepoužívejte v deníku číselné řady. Důvodem je, že číselná řada pro finanční deník dlouhodobého majetku neobsahuje číselnou řadu pro deník dlouhodobého majetku.

## Zaúčtování položek do různých knih odpisů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deník DM** poté vyberte související odkaz.
2. V deníku, se kterým chcete zaúčtovat odpisy, zaškrtněte políčko **Použít seznam duplikátů**.
3. Podle potřeby vyplňte zbývající pole.
4. Vyberte akci **Účtovat**.
5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky DM** a poté vyberte související odkaz.

   > [!NOTE]
   > Stránka **Deník dlouhodobého majetku** obsahuje nové řádky pro různé knihy odpisů podle seznamu duplikace.
6. Zkontrolujte nebo upravte řádky a poté vyberte akci **Účtovat**.

   > [!NOTE]
   > Dalším způsobem, jak duplikovat položku v samostatné knize, je zadat kód knihy odpisů do pole **Duplikát v knize odpisů**, když vyplníte řádek deníku.

Položky z jedné knihy odpisů do druhé můžete kopírovat pomocí dávkové úlohy **Kopie knihy odpisů**. Dávková úloha vytvoří řádky deníku v listu deníku, který jste zadali na stránce **Nastavení deníku DM**, do které chcete kopírovat. Další informace naleznete v následujícím postupu.

## Kopírování položek dlouhodobého majetku mezi knihami odpisů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Knihy odpisů** a poté vyberte související odkaz.
2. Otevřete příslušnou kartu knihy odpisů a zvolte akci **Kopie knihy odpisů**.
3. Na stránce **Kopie knihy odpisů** vyplňte pole podle potřeby.
4. Vyberte tlačítko **OK**.

Zkopírované řádky jsou vytvořeny buď v deníku finančního majetku dlouhodobého majetku, nebo v deníku dlouhodobého majetku v závislosti na tom, zda kniha odpisů, kterou kopírujete, má integraci do hlavní knihy.

## Viz také
[Dlouhodobý majetek](fa-manage.md)  
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
