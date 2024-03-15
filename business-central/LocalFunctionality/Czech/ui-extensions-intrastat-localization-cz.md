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

# České hlášení Intrastatu

[!INCLUDE[intrastat-2022w2](../../includes/intrastat-2022w2.md)]

Dynamics 365 Business Central poskytuje funkce, které umožňují shromažďovat statistiky o obchodu se zbožím mezi členskými státy EU a připravit soubor výkazu Intrastat k odeslání. Aplikace Intrastat CZ rozšiřuje aplikaci Intrastat Core o funkcionality pro vykazování obchodu se zbožím podle České legislativy. Pro používání této aplikace je tedy potřeba mít nejprve nainstalovanou aplikaci Intrastat Core.

## Hlavní funkcionality

- Nastavení hlášení Intrastat
- Nastavení zboží a dlouhodobého majetku pro vykazování Intrastatu
- Nastavení Kontrolního seznamu hlášení Intrastatu pro validaci pravidel Intrastatu
- Nastavení definice výměny dat pro vytváření exportů souborů Intrastatu
- Vytvoření a odeslání souboru výkazu pro Intrastat
- Odeslání výkazu Intrastat v souladu s požadavky ČR.

## Rozšíření nastavení pro Intrastat CZ

- **Statistický údaj** - číselník je doplněn do řádků Hlášení Intrastat a do exportu výkazu.
- **Dodací skupiny Intrastat** - číselník je doplněn do Způsobů dodávky, řádků hlášení Intrastat a do exportu výkazu.
- **Poplatky za zboží** - doplněno pole **Zahrnout do částky Intrastat** umožňující uživateli stanovit, které poplatky mají být zahrnuty do částky Intrastat. Použití či nepoužítí částky poplatku pro Intrastat je možno ovlivnit zpětně i pro již zaúčtované položky.
- **Karta zboží** je pro účely Intrastatu doplněna o pole **Specifický pohyb** a **Statistický údaj**.

## Nastavení hlášení Intrastat

Nastavení hlášení Intrastat bylo doplněno o tato pole:

- **Typ zaokrouhlení intrastat** - určuje typ zaokrouhlování pro výpočet částek při vytváření hlášení Intrastat a umožňuje nastavit zaokrouhlení Nahoru, Dolu nebo Nejbližší.
- **Výchozí fyz. pohyb - Vratka** - Určuje výchozí hodnotu pole Fyzický pohyb pro prodejní a servisní vratky a vratky nákupu.  
- **Typ transakce je povinný** - kontroluje vyplnění hodnoty při účtování dokladů
- **Spec. transakce je povinná** - kontroluje vyplnění hodnoty při účtování dokladů
- **Typ přepravy je povinný** - kontroluje vyplnění hodnoty při účtování dokladů
- **Způsob dodávky je povinný** - kontroluje vyplnění hodnoty při účtování dokladů

## Použití Hlášení Intrastat

- Funkce **Získat řádky hlášení Intrastat** naplní řádky hlášení Intrastatu se zohledněním použití či nepoužítí částky poplatků za zboží a způsobu zaokrouhlení částek.
- **Kontrolní sestava** provede standardní kontroly hlášení Intrastatu včetně doplněných kontrol na povinná pole Typ transakce, Spec. transakce, Typ přepravy a Způsob dodávky.
- **Vytvořit soubor** vyexportuje hlášení Intrastat. Export výkazu využívá nastavení **Definice výměny dat**, která dodržuje současnou podobu výkazu CZ Intrastatu. Definice výměny dat umožňuje export dat uživatelsky upravovat.

## Viz také

[Česká lokální funkcionalita](czech-local-functionality.md)  
[Nastavení Intrastat](../../finance-how-setup-report-intrastat.md)  
[Použití Intrastat](../../finance-how-report-intrastat.md)  
