---
title: Reclassify Fixed Assets| Microsoft Docs
description: You reclassify a fixed asset to transfer it to a different department, split it up, or combine it with other fixed assets.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: sgroespe

---
# Převod, rozdělení nebo kombinování dlouhodobého majetku
Deník přeřazení dlouhodobého majetku se používá k převodu, rozdělení a kombinování dlouhodobého majetku. Výsledky přeřazení dlouhodobého majetku můžete zobrazit nebo vytisknout pomocí sestavy **Dlouhodobý majetek-úč.hodn.02**.

## Převod dlouhodobého majetku do jiného oddelení
Dlouhodobý majetek může být nutné převést do jiného oddelení, když například umístíte majetek do výrobního oddělení, když je ve výstavbě, a po dokončení jej přesunete do administrativního oddelení.

1. Nastavte nový dlouhodobý majetek. Do pole **Kód oddělení** zadejte nové oddělení.
2. K novému dlouhodobému majetku přiřaďte knihu odpisů dlouhodobého majetku. Pro více informací navštivte [Pořízení dlouhodobého majetku](fa-how-acquire.md).
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník  přeřazení DM** a poté vyberte související odkaz.
4. Vytvořte deník přeřazení, kde pole **Číslo DM** obsahuje původní dlouhodobý majetek a pole **Nové číslo DM** obsahuje nový dlouhodobý majetek, který má být přesunut.
5. Vyberte akci **Přeřadit**.

   Dva řádky jsou nyní vytvořeny ve finančním deníku dlouhodobého majetku pomocí šablony a dávky, které jste zadali na stránce **Nastavení deníku DM** pro zadanou knihu odpisů. Pro více informací navštivte [Nastavení odpisů dlouhodobého majetku](fa-how-setup-depreciation.md).
6. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky dlouhodobého majetku** a poté vyberte související odkaz.
7. Na stránce **Finanční deník DM** vyberte akci **Účtovat** pro zaúčtování přeřazení, které jste provedli v krocích 4 a 5.

Pokud jste zaúčtovali náklady na pořízení pro jeden majetek, můžete použít deník přeřazení dlouhodobého majetku k rozdělení nákladů na pořízení mezi několik majetků.

## Rozdělení dlouhodobého majetku na tři dlouhodobá aktiva
Jeden dlouhodobý majetek můžete rozdělit na více dlouhodobých aktiv, například když potřebujete rozdělit dlouhodobý majetek do tří různých oddělení. V takovém případě můžete například přesunout 25 procent nákladů na pořízení a odpisů původního dlouhodobého majetku na druhý dlouhodobý majetek a 45 procent na třetí majetek. Zbývajících 30 procent zůstane na původním dlouhodobém majetku.

1. Nastavte dva nové dlouhodobé majetky. Do pole **Kód oddělení** zadejte nové oddělení.
2. Přiřaďte knihy odpisů dlouhodobého majetku k novému dlouhodobému majetku. Pro více informací navštivte [Pořízení dlouhodobého majetku](fa-how-acquire.md).
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník  přeřazení DM** a poté vyberte související odkaz.
4. Vytvořte dva řádky deníku přeřazení, jeden pro každý nový dlouhodobý majetek.
5. Na prvním řádku zadejte druhý dlouhodobý majetek do pole **Nové číslo DM** a 25 do pole **Přeřadit %  pořízení**.
6. Na druhém řádku zadejte třetí dlouhodobý majetek do pole **Nové číslo DM** a 40 do pole **Přeřadit %  pořízení**.
7. Na obou řádcích zaškrtněte políčka **Přeřadit náklady pořízení** a **Přeřadit odpis**.
8. Vyberte akci **Přeřadit**.

   Dva řádky jsou nyní vytvořeny ve finančním deníku dlouhodobého majetku pomocí šablony a dávky, které jste zadali na stránce **Nastavení deníku DM** pro zadanou knihu odpisů. Pro více informací navštivte [Nastavení odpisů dlouhodobého majetku](fa-how-setup-depreciation.md).
9. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky dlouhodobého majetku** a poté vyberte související odkaz.
10. Na stránce **Finanční deník DM** vyberte akci **Účtovat** pro zaúčtování přeřazení, které jste provedli v krocích 4 až 8.

## Sloučení dvou dlouhodobých aktiv do jednoho
Můžete kombinovat více dlouhodobého majetku do jednoho dlouhodobého majetku, například při přesunu distribuovaného dlouhodobého majetku do jednoho oddělení. Pokud jste zaúčtovali náklady na pořízení a odpisy dlouhodobého majetku, který má být přesunut, budou tyto hodnoty sloučeny do jedinoho dlouhodobého majetku.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník  přeřazení DM** a poté vyberte související odkaz.
2. Vytvořte deník přeřazení, kde pole **Číslo DM** obsahuje dlouhodobý majetek, který má být přesunut nebo kombinován, a pole **Nové číslo DM** obsahuje dlouhodobý majetek, se kterým bude kombinován.
3. Ponechte pole **Přeřadit %  pořízení** prázdné pro přesunutí nebo sloučení celých nákladů na pořízení.
4. Zaškrtněte políčka **Přeřadit náklady pořízení** a **Přeřadit odpis**.
5. Vyberte akci **Přeřadit**.

   Dva řádky jsou nyní vytvořeny ve finančním deníku dlouhodobého majetku pomocí šablony a dávky, které jste zadali na stránce **Nastavení deníku DM** pro zadanou knihu odpisů. Pro více informací navštivte [Nastavení odpisů dlouhodobého majetku](fa-how-setup-depreciation.md).
6. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky dlouhodobého majetku** a poté vyberte související odkaz.
7. Na stránce **Finanční deník DM** vyberte akci **Účtovat** pro zaúčtování přeřazení, které jste provedli v krocích 2 až 5.

## Zobrazení změněných hodnot knihy odpisů z důvodu přeřazení dlouhodobého majetku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní hodnota DM 02** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole.
3. Vyberte tlačítko **Tisk** nebo **Náhled**.

## Viz také
[Dlouhodobý majetek](fa-manage.md)  
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
