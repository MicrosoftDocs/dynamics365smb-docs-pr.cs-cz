---
title: Správa dlouhodobého majetku | Microsoft Docs
description: Informace o funkcích dlouhodobého majetku a získání přehledu o způsobu práce s dlouhodobým majetkem
services: project-madeira
documentationcenter: ''
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'machinery, buildings'
ms.date: 01/17/2020
ms.author: sgroespe
---
# Dlouhodobý majetek

Funkcionalita dlouhodobého majetku v aplikaci [!INCLUDE [d365fin](includes/d365fin_md.md)] poskytuje přehled o dlouhodobém majetku a zajišťuje správné periodické odpisy. Umožňuje také sledovat náklady na údržbu, spravovat pojištění, účtovat transakce dlouhodobého majetku a generovat různé sestavy a statistiky.

Pro každý dlouhodobý majetek musíte nastavit kartu obsahující informace o majetku. Budovy nebo výrobní zařízení můžete nastavit jako hlavní majetek se seznamem komponent. Majetek můžete je seskupit různými způsoby, například podle třídy, střediska nebo umístění. Poté můžete začít pořizovat, udržovat a prodávat dlouhodobý majetek. Můžete také nastavit rozpočtovaný majetek. To umožňuje zahrnout jakékoli očekávané pořízení a prodeje v sestavách.

Ke sledování jak odpisů dlouhodobého majetku, tak ostatních finančních transakcí souvisejících s dlouhodobým majetkem, nastavíte jednu nebo více knih odpisů pro každý dlouhodobý majetek ve vaší společnosti. Odpis se provede spuštěním sestavy pro výpočet periodického odpisu, která vyplnění deník s výslednými hodnotami připravenými k zaúčtování. [!INCLUDE[d365fin](includes/d365fin_md.md)]podporuje několik odpisových metod. Pro více informací navštivte [Metody odpisu](fa-depreciation-methods.md). Pro každý dlouhodobý majetek můžete vytvořit více knih odpisů pro různé účely, například pro daňové vykazování či pro interní vykazování.

U každého majetku můžete zaznamenat náklady na údržbu a datum dalšího servisu. Sledování nákladů na údržbu může být důležité pro účely rozpočtování a pro rozhodování o tom, zda vyměnit dlouhodobý majetek.

Každý dlouhodobý majetek lze připojit k jedné nebo více pojistným smlouvám. Můžete proto snadno ověřit, že částky pojistných smluv jsou v souladu s hodnotou majetku pojištěného pojistnou smlouvou. Díky tomu je také snadné sledovat roční pojistné.

> [!NOTE]  
> Transakce dlouhodobého majetku můžete účtovat na stránce **Finanční deník DM** nebo na stránce **Deník dlouhodobého majetku** podle toho, zda se jedná o transakce pro finanční výkaznictví nebo pro interní správu. Nápověda k dlouhodobému majetku popisuje pouze způsob použití stránky **finanční deník DM** . Pro více informací navštivte sekci [Nastavení odpisů dlouhodobého majetku](fa-how-setup-depreciation.md).

Dříve než můžete začít spravovat dlouhodobý majetek, musíte nastavit výchozí hodnoty, účtování dlouhodobého majetku, účto skupiny, klíče rozdělení, deníky a typy účtování. Pro více informací navštivte sekci [Nastavení dlouhodobého majetku](fa-setup.md).

Následující tabulka popisuje přehled úloh s odkazy na témata, které je popisují.

| Funkce | Odkaz |
| --- | --- |
|Vytvoření dlouhodobého majetku, přiřazení metod odpisů, zaúčtování pořízení, hodnoty při vyřazení a tisk přehledů dlouhodobého majetku.|[Pořízení dlouhodobého majetku](fa-how-acquire.md)|
|Evidence servisních návštěv, účtování nákladů na údržbu a sledování nákladů na údržbu.|[Údržba dlouhodobého majetku](fa-how-maintain.md)|
|Aktualizace informací o pojištění, účtování nákladů na pořízení k pojistným smlouvám, úprava pojistného krytí, zobrazení statistiky pojištění a pojistných smluv.|[Pojištění dlouhodobého majetku](fa-how-insure.md)|
|Přeřazení dlouhodobého majetku, převod dlouhodobého majetku do různých lokací, rozdělení nebo kombinace majetku |[Převod, rozdělení nebo kombinování dlouhodobého majetku](fa-how-trans-split-combine.md)|
|Úprava hodnot dlouhodobého majetku, zaúčtování zhodnocení a znehodnocení.|[Přecenění dlouhodobého majetku](fa-how-revalue.md)|
|Výpočet odpisů, zaúčtování odpisů a analýza odpisů v sestavách dlouhodobého majetku.|[Odpisování nebo amortizace dlouhodobého majetku](fa-how-depreciate-amortize.md)|
|Zaúčtování transakcí vyřazení, zobrazení položek vyřazení a zaúčtování částečného vyřazení.|[Likvidace nebo vyřazení dlouhodobého majetku](fa-how-dispose-retire.md)|
|Správa rozpočtů dlouhodobého majetku, rozpočtování nákladů na pořízení, rozpočtování vyřazení dlouhodobého majetku a rozpočtování odpisů.|[Správa rozpočtů dlouhodobého majetku](fa-how-manage-budgets.md)|

## Viz také

[Nastavení dlouhodobého majetku](fa-setup.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]