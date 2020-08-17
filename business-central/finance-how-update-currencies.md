---
title: Update Currency Exchange Rates| Microsoft Docs
description: Track amounts in different currencies using currency codes, and let Business Central help you adjust exchange rates of posted entries with an external service.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 01/13/2020
ms.author: sgroespe

---
# Aktualizace směnných kurzů
Vzhledem k tomu, že společnosti působí ve stále více zemích a oblastech, stává se důležitějším možnost, obchodování a vykazování finančních údajů ve více než jedné měně. Musíte nastavit kód pro každou měnu, kterou používáte, pokud nakupujete nebo prodáváte v jiné měně, než je vaše místní, máte pohledávky a závazky v jiných měnách nebo zaznamenáváte finanční transakce v různých měnách.

Finance jsou nastaveny tak, aby používaly lokální měnu (LM), ale můžete je nastavit tak, aby používaly i jinou měnu s přiřazeným aktuálním směnným kurzem. Označením druhé měny jako takzvané druhé měny pro vykazování v [!INCLUDE[d365fin](includes/d365fin_md.md)] bude automaticky zaznamenávat částky v lokální měně i v této druhé měně pro vykazování na každou věcnou položku a další položky, například položky DPH. Pro více informací navštivte [Nastavení přídavné měny pro hlášení](finance-how-setup-additional-currencies.md).

## Úprava směnných kurzů
Vzhledem k tomu, že směnné kurzy neustále kolísají, musí být pravidelně upravovány další měnové ekvivalenty ve vašem systému. Pokud tyto úpravy nejsou provedeny, částky, které byly převedeny ze zahraničních (nebo dodatečných) měn a zaúčtovány do hlavní knihy v lokální měně, mohou být zavádějící. Kromě toho musí být denní položky zaúčtované před vstupem denního směnného kurzu do aplikace aktualizovány po zadání denních informací o směnném kurzu.

Dávková úloha **Úprava směnných kurzů** se používá k úpravě směnných kurzů zaúčtovaných položek zákazníků, dodavatelů a bankovních účtů. Může také aktualizovat další částky měny vykazování u položek hlavní knihy. Směnné kurzy můžete také automaticky upravit pomocí služby. Pro více informací navštivte [Nastavení Služby směnného kurzu](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

### Vliv na zákazníky a dodavatele
U účtů zákazníků a dodavatelů upravuje dávková úloha měnu pomocí směnného kurzu platného v den účtování, který je uveden v dávkové úloze. Dávková úloha vypočítá rozdíly pro jednotlivé měnové zůstatky a zaúčtuje částky na účet hlavní knihy, který je určen na poli **Účet nerealizovaných zisků** nebo na poli **Účet nerealizovaných ztrát** na stránce **Měny**. Vyrovnávací položky jsou automaticky zaúčtovány na účet pohledávek/závazků v hlavní knize.

Dávková úloha zpracuje všechny otevřené položky zákazníka a položky dodavatele. Pokud u položky existuje kurzový rozdíl, dávková úloha vytvoří novou podrobnou položku zákazníka nebo dodavatele, která odráží upravenou částku v položce zákazníka nebo dodavatele.

#### Dimenze položek odběratele a dodavatele
Položkám úprav jsou přiřazeny diminze z položek účetní knihy zákazníka a dodavatele a úpravy jsou zaúčtovány podle kombinace hodnot dimenzí.

### Dopad na bankovní účty
U bankovních účtů upravuje dávková úloha měnu pomocí směnného kurzu platného v den účtování, který je uveden v dávkové úloze. Dávková úloha vypočítá rozdíly pro jednotlivé bankovní účty, které mají kód měny, a účtuje hodnoty na účet hlavní knihy, který je uveden v poli **Účet realizovaných zisků** nebo na poli **Účet realizovaných ztrát** na stránce **Měny**. Vyrovnávací položky se automaticky zaúčtují na bankovní účty hlavní knihy, které jsou uvedeny ve Účto skupinách bankovního účtu. Dávková úloha vypočítá jednu položku na měnu pro účto skupinu.

#### Dimenze položek bankovního účtu
Položky úpravy pro účet hlavní knihy bankovního účtu a pro účet zisků a ztrát jsou přiřazeny výchozí dimenze bankovního účtu.

### Vliv na finanční účty
Pokud účtujete v přídavné měně pro hlášení, můžete nechat dávkovou úlohu vytvořit nové položky hlavní knihy pro úpravy měny mezi LM a další měnou pro hlášení. Dávková úloha vypočítá rozdíly pro každou položku hlavní knihy v závislosti na obsahu pole **Úprava směnného kurzu** pro každý účet hlavní knihy.

##### Dimenze v položkách finančního účtu
Položkám úprav jsou přiřazeny výchozí dimenze z účtu, na které jsou zaúčtovány.

> [!Important]
> Před použitím dávkové úlohy musíte zadat vyrovnávací kurzy, které se používají k úpravě zůstatků v cizí měně. To provedete na stránce **Směnné kurzy měn** <br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## Nastavení Služby směnného kurzu
Pomocí externí služby můžete udržovat směnné kurzy aktuální, například FloatRates.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Služby směnného kurzu**, a poté vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Na stránce **Služba směnného kurzu**, vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Zaškrtněte pole **Povolit** pro spuštění služby.

## Aktualizace směnných kurzů prostřednictvím služby směnného kurzu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Měny** a poté vyberte související odkaz.
2. Vyberte akci **Aktualizovat směnné kurzy**.

Hodnota v poli **Směnný kurz** na stránce **Měny** je aktualizována nejnovějším směnným kurzem.

## Viz související kurzy na [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## Viz také
[Nastavení přídavné měny pro hlášení](finance-how-setup-additional-currencies.md)  
[Uzavírání roků a období](year-close-years-periods.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
