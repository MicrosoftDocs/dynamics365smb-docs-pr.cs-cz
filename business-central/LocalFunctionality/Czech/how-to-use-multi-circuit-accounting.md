---
title: Czech Local Functionality - Multi Circuit Accounting 
description: The following topics describe the local functionality Multi Circuit Accounting in the Czech version of Business Central.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: CZ, Czech, Localization, Finance  
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Skupiny finančních účtů - Více-okruhové účtování 

Dle účetních standardů může účetní jednotka účtovat v rámci vícero účetních okruhů (Finanční, Podrozvahové a Vnitropodnikové účetnictví). Lze takto označit účty, které jsou pro Vás relevantní.

Pro nastavení účetních okruhů v systému:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
2. Otevřete kartu vybraného finančního účtu.
3. Na kartě finančního účtu, v zálože Obecné vyberte v poli **Skupina finančního účtu** jednu z možností:
    - Finanční účet
    - Vnitropodnikový účet
    - Podrozvahový účet
4. Po nastavení kartu zavřete.

Při účtování pak dochází ke kontrole a systém zastaví účtování v případě, že je účtováno na finanční účty z různých účetních okruhů v rámci jedné účetní transakce.

## Viz také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](../../finance.md)
