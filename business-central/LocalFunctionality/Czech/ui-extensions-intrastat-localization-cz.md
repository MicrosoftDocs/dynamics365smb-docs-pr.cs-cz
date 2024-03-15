---
title: Intrastat Localization for Czech (Extension)  
description: Companies in the European Union (EU) are required to report trade with other countries/regions in the EU through Intrastat reporting or VAT Information Exchange System.
author: v-pejano
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.search.keywords: Czech, Intrastat, CZ
ms.date: 09/30/2023
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Czech Intrastat

[!INCLUDE[intrastat-2022w2](../../includes/intrastat-2022w2.md)]

Dynamics 365 Business Central poskytuje funkce, které umožňují shromažďovat statistiky o obchodu se zbožím mezi členskými státy EU a připravit soubor výkazu Intrastat k odeslání. Aplikace Intrastat CZ rozšiřuje aplikaci Intrastat Core o funkcionality pro vykazování obchodu se zbožím podle České legislativy. Pro používání této aplikace je tedy potřeba mít nejprve nainstalovanou aplikaci Intrastat Core.

## Hlavní funkcionality

- Nastavení hlášení Intrastat
- Nastavení zboží a dlouhodobého majetku pro vykazování Intrastatu
- Nastavení Kontrolního seznamu hlášení Intrastatu pro validaci pravidel Intrastatu
- Nastavení definice výměny dat pro vytváření exportů souborů Intrastatu
- Vytvoření a odeslání souboru výkazu pro Intrastat
- Odeslání výkazu Intrastat v souladu s požadavky ČR.

## Rozšíření nastavení

### Statistický údaj

Číselník je doplněn do řádků Hlášení Intrastat a do exportu výkazu.

### Dodací skupiny Intrastat

Číselník je doplněn do Způsobů dodávky, řádků Hlášení Intrastat a do exportu výkazu.

### Poplatky za zboží

Doplněno pole **Zahrnout do částky Intrastat** umožňující uživateli stanovit, které poplatky mají být zahrnuty do částky Intrastat. Použití či nepoužítí částky poplatku pro Intrastat je možno ovlivnit zpětně i pro již zaúčtované položky.

### Nastavení hlášení Intrastat

Nastavení hlášení Intrastat bylo doplněno o tato pole:

- **Typ zaokrouhlení intrastat** - určuje typ zaokrouhlování pro výpočet částek při vytváření hlášení Intrastat a umožňuje nastavit zaokrouhlení Nahoru, Dolu nebo Nejbližší.
- **Výchozí fyz. pohyb - Vratka** - Určuje výchozí hodnotu pole Fyzický pohyb pro prodejní a servisní vratky a vratky nákupu.
- **Typ transakce je povinný**
- **Spec. transakce je povinná**
- **Typ přepravy je povinný**
- **Způsob dodávky je povinný**

## Export výkazu

Export výkazu nové funkcionality využívá nastavení **Definice výměny dat**. Pro nový CZ Intrastat byla vytvořena nová definice, která dodržuje současnou podobu výkazu CZ Intrastatu.

## Viz také

[Česká lokální funkcionalita](czech-local-functionality.md)  
[Nastavení Intrastat](../../finance-how-setup-report-intrastat.md)  
[Použití Intrastat](../../finance-how-report-intrastat.md)  
