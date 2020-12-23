---
title: Czech Local Functionality - Setup VAT date
description: This section describes Czech local functionality - VAT Date and Setup of the VAT Date Feature.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Finance, VAT, Localization, CZ
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---


# Datum DPH

Datum DPH je důležité pro daňové doklady podle § 28 zákona o DPH 235/2004 Sb. Datum DPH se může lišit od data zaúčtování nebo data dokladu. Datum DPH je důležité pole pro vykazování DPH.

Tato funkce se zaměřuje na zlepšení následujících oblastí:

## Nastavení použití Data DPH

- Obecné povolení používání Data DPH v systému.
- Výběr způsobů, jakým systém bude zobrazovat výchozí hodnotu Data DPH v různých oblastech (Zúčtovací datum nebo Datum dokladu).
- Období pro vykazování DPH a účetní období společnosti se mohou často lišit. Abychom umožnili uživatelům bezproblémově vykazovat a účtovat DPH podle období pro vykazování DPH a také vydávat interní a další statutární vykazování na základě účetních období, zavádí tato funkce nově Období DPH.
- Povolit účtování DPH od/do – zadání časové období v polích od/do, aby se zabránilo chybám účtování do uzavřených účetních a DPH období.

### Účtování transakcí s datem DPH  

Aby uživatel zaúčtoval transakce s použitím Data DPH, musí být schopen zadat datum DPH v aplikaci do hlaviček dokladů a řádků deníku.
Po zaúčtování je Datum DPH součástí zaúčtovaných dokladů, věcných položek a položek DPH.

### Výpočet a účtování vyrovnání DPH

Systém filtruje položky DPH na základě data DPH (místo Zúčtovacího data) výběrem DPH období a připraví sestavu ukazující, které položky budou převedeny na účet vyrovnání DPH. Výtisk obsahuje také informace o datu DPH.

## Viz Také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[Kontrolní hlášení DPH](how-to-create-vat-control-report.md)  
[Výkaz DPH](vat-statement.md)  
[Finance](../../finance.md)  
