---
title: Set Up a VAT Statement | Microsoft Docs
description: Set Up a VAT Statement
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2020
ms.author: bholtorf

---
# Nastavení výkazů DPH

## Nastavení šablon výkazu DPH a názvů výkazu DPH
Finanční úřady mohou změnit své požadavky na účtování DPH. Šablony výkazu DPH a názvy výkazu DPH vám mohou pomoci připravit se na nadcházející změny a zajistit hladký přechod na nové požadavky. Šablony výkazu DPH můžete použít k nastavení různých sestav při výběru tisku výkazu. Každá šablona výkazu DPH může mít více názvů výkazu DPH, které zase definují výpočty a při změně požadavků můžete vytvořit nový název výkazu DPH. Jeden název může například vypočítávat DPH pro tento rok na základě aktuálních požadavků a jiný může počítat DPH na základě požadavků pro příští rok. Názvy jsou také způsob, jak si například udržet historii formátů výkazů DPH, tím je možno nahlédnout zpět, jak jste vypočítali DPH v předchozích letech.

## Definice výkazů DPH
Výkazy DPH umožňují vypočítat částku vyrovnání DPH za určité období, například kvartálně.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Výkazy DPH** a vyberte související odkaz.
2. Zvolte pole **Název** a poté vybete **Nový** na stránce **Názvy výkazů DPH**.
3. Vyplňte požadovaná pole. Obvykle chcete mít nastavení pro každou DPH účto skupinu nebo  DPH účto skupinu zboží a jejich kombinace. Pro čísla řádků má smysl používat stejná čísla nebo kódy jako ve vašem oficiálním výkazu DPH [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]


> [!Tip]
> Informace, které výkaz obsahuje, můžete filtrovat podle toho, co vyberete v poli **Typ**. **Sčítání účtů** je užitečný, pokud chcete DPH z určitého účtu.
> **Sčítání pol. DPH** získá DPH z účtů přiřazených k výběrům v **Typ. Obecného Účtování**, **DPH obchodní účto skupina**, a/nebo **DPH  účto skupina zboží**. **Sčítání řad**umožňuje zadat hodnotu nebo kritéria rychlého filtru do pole **Sčítání řad**. Pro více infortmací navštivte [Řazení, Vyhledávání a Seznam filtrování](ui-enter-criteria-filters.md). **Popis** se často používá k přidání poznámky k výkazu. Můžete jej například použít jako nadpis, když jste použili součet řádků.

## Náhled výkazu DPH
Po definování výkazu DPH můžete zobrazit jeho náhled a ujistit se, že vyhovuje vašim potřebám.
> [!Tip]
> Doporučuje se mít jednu část ve výkazu DPH s použitím **Typ** **Sčítání položek DPH** a další sekci níže pomocí **Typ** **Sčítání účtů** pro sladění částek založených na tabulce **DPH položky** ve srovnání s částkou na **účtech účetní osnovy**. K tomuto účelu můžete také použít sestavu **Fin. odsouhlasení DPH**.

1. Zvolte **Náhled**.
2. Zadáním filtru data omezíte výpis na konkrétní období. Další informace o tom, jak přizpůsobit stránku tak, aby zobrazovala filtr data, naleznete v části [Řazení, Vyhledávání a Seznam filtrování](ui-enter-criteria-filters.md).
3. Můžete vybrat různé možnosti a určit typ položek DPH, které mají být zahrnuty do výkazu.
4. Na řádcích, kde pole **Typ** obsahuje **Sčítání položek DPH** můžete zobrazit seznam položek DPH výběrem částky v poli **Částka sloupce**.
5. Pomocí personalizace můžete zobrazit další pole v řádcích. Například nerealizovaná základní částka a nerealizovaná částka DPH, pokud používáte nerealizovanou DPH.

## Viz také
[Nastavení daně z přidané hodnoty ](finance-setup-vat.md)  
[Nastavení nerealizované daně z přidané hodnoty](finance-setup-unrealized-vat.md)      
[Reportování DPH finančímu úřadu](finance-how-report-vat.md)  
[Práce s DPH v prodeji a nákupu](finance-work-with-vat.md)  
[Lokální funkcionality v Business Central](about-localization.md)
