---
title: Czech Local Functionality - Internal Financial Documents
description: The following topics describe Internal Financial Documents - the local functionality in the Czech version of Business Central. Users perform General Ledger operations and must have the possibility to print documents for these operations with the layout in compliance with the legal requirements.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Finance, Localization, CZ
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---


# Interní účetní doklady

Uživatelé provádějí účetní operace a musí mít možnost tisknout takové dokumenty s účetními operacemi, které vzhledem i obsahem vyhovují požadavkům legislativy.

Z výše uvedených důvodů tato funkce poskytuje následující sestavy:

## Finanční deník - Test
Report, který slouží pro kontrolu zadaného interního dokladu před zaúčtováním z Finančního deníku.  
### Supštění sestavy Finanční deník - Test
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony finančního děníku** a poté vyberte související odkaz.
2. Vyberte šablonu finančního deníku a vyplňte v poli **ID sestavy 11722 - Finanční deník - Test**.
3. Přehled šablon finančního deníku můžete zavřít.
4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky** a poté vyberte související odkaz.
5. Vyberte šablonu deníku.
6. Vyplňte řádky deníku interními transakcemi a poté spusťtě sestavu Finanční deník - Test pomocí tlačítka **Testovací sestava** a zkontrolujte výstup reportu.

## Obecný účetní doklad
Report, který slouží ke kontrole a tisku zaúčtované účetní operace. Report je možné tisknout včetně dimenzí. 

### Spuštění sestavy Obecný účetní doklad
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony finančního děníku** a poté vyberte související odkaz.
2. Vyberte šablonu finančního deníku a vyplňte v poli **ID účtovací sestavy 11766 - Obecný účetní doklad**.
3. Přehled šablon finančního deníku můžete zavřít.
4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky** a poté vyberte související odkaz.
5. Vyberte šablonu deníku.
6. Vyplňte řádky deníku interními transakcemi.
7. **Pro spuštění při účtování** použijte funkci **Účtovat a vytisknout** a zkontrolujte výstup reportu.
8. **Pro ruční spuštění** postupujte následovně:
    - Spustit a zkontrolovat výstup reportu Obecný účetní doklad s parametrem včetně dimenzí.
    - Spustit a zkontrolovat výstup reportu Obecný účetní doklad podle čísla věcné položky.
    - Spustit a zkontrolovat výstup reportu Obecný účetní doklad podle čísla dokladu.

## Viz Také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](../../finance.md)  
