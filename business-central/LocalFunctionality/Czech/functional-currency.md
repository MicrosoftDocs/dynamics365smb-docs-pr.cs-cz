---
title: Functional Currency – Czechia
description: This document explains the concept of functional currency and its application in Business Central.
author: v-pejano
ms.author: v-pejano
ms.reviewer: v-pejano
ms.search.keywords: CZ, Czech, Currency, Finance, Accounting, Functional Currency, Exchange Rates
ms.topic: article
ms.date: 08/28/2024
ms.search.form: 118
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Funkční měna

V rámci novely Zákona č. 563/1991 Sb., o účetnictví platné od 1.1.2024 se zavádí pojem funkční měna jako měna účetnictví. Funkční měnou se rozumí měna primárního ekonomického prostředí, ve kterém účetní jednotka působí a může být jiná než měna česká. Funkční měna účetní jednotky se určuje na základě kritérií pro určení funkční měny podle mezinárodních účetních standardů IFRS upravených právem Evropské unie.  

Pokud se společnost rozhodne realizovat účetnictví v cizí měně, pak pro ostatní evidence a výkazy, které musí být v české měně, použije funkcionalitu Přídavné měny pro hlášení. Ta ale řeší pouze vznik věcných položek a položek DPH, ale ne následné vykazování. Celé DPH výkaznictví musí proběhnout v české měně (CZK), proto byly přizpůsobeny funkcionality pro vykazování jako jsou:

- Náhled výkazu DPH
- Kontrolní hlášení DPH
- Statistika Kontrolního hlášení DPH
- Souhrnné hlášení (VIES)
- Export výkazu DPH
- Export Kontrolního hlášení DPH
- Export Souhrnného hlášení
- Tisk výkazu DPH (Report 11769)
- Tisk Záznamní povinnosti (Podklad pro DPH) a Seznamu daňových dokladů (Report 11756)
- Testovací sestava Kontrolního hlášení DPH (Report 31103)
- Testovací sestava Souhrnného hlášení (Report 31064)

Do nákupních a prodejních dokladů byla přidána nová pole Kurz DPH k přídavné měně (MD/PM), aby bylo možné v případě potřeby kurz měny upravit. Obdobná funkčnost je doplněna i na nákupních a prodejních zálohách. Současně byl upraven tisk dokladových sestav.

## Viz Také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
[Finance](../../finance.md)  

## [!INCLUDE[prod_short](../../includes/free_trial_md.md)]  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]