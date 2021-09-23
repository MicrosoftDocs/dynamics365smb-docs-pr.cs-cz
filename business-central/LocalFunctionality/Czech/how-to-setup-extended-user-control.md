---
title: Czech Local Functionality Extended User Control 
description: The majority of companies in the Czech Republic request the following improvements to be implemented in user setup and control.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Finance, Localization, CZ
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Rozšířené uživatelské kontroly


Funkcionalita rozšířených uživatelských kontrol umožňuje nastavit pomocí **Nastavení uživatelů** v kombinaci s **Řádky nastavení uživatelů** různé kontroly, omezení a přístupy. Tento nástroj může sloužit k dodatečnému nastavení, kde vše nelze pokrýt uživatelskými právy, nebo k velice specifickému nastavení vybraného uživatele.

Mezi typický příklad může být omezení účtování příjmu na vybranou lokaci, účtování na vybrané dimenze nebo jen kontrola data účtování dokladu.

Příklad možností naleznete níže:

|Kontrola|Popis|
|-|-|
|**Nastavení filtru centra odpovědnosti** | Nastavení Centra odpovědnosti hotovosti pro pokladní operace. |
|**Kontrolovat data dokladu**| Kontrola při účtování proti pracovnímu nebo systémovému datu. |
|**Kontrolovat zúčtovací datum** | Kontrola při účtování proti pracovnímu nebo systémovému datu. |
|**Kontrolovat přístup k platebním příkazům** | Kontrolova povolených Bankovních účtů pro platební příkazy (nastavení v řádcích). |
|**Kontrolovat přístup k bankovním výpisům** | Kontrola povolených Bankovních účtů pro bankovní výpisy (nastavení v řádcích). |
|**Kontrolovat bankovní účty** | Povolené pro účtování (nastavení v řádcích). |
|**Kontrolovat přístup k šablonám deníku** | Kontrola povolené šablony pro všechny druhy deníků (nastavení v řádcích). |
|**Kontrolovat hodnoty dimenzí** | Povolení pro účtování (nastavení v řádcích). |
|**Kontrolovat skladové lokace** | Povolení pro účtování zvlášť pro zvýšení množství a snížení množství (nastavení v řádcích). |
|**Kontrolovat skladové lokace** | Povolení pro vydání zvlášť pro zvýšení množství a snížení množství (nastavení v řádcích). |
|**Kontrolovat použití šablon skladového pohybu** | Kontrola při účtování v deníku zboží. |
|**Povolit účtování do uzavřeného období** | Umožňuje účtovat do již uzavřeného období. |
|**Povolit dokončení projektu** | Umožňuje dokončit projekty. |
|**Povolit storno vyrovnání zboží** | Umožňuje storno při vyrovnávání zboží. |

## Nastavení kontrol (Kontrola účtování příjmu na vybrané lokaci)
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení uživatelů** a poté vyberte související odkaz.
2. Vyberte uživatele, kterému chcete nastavit nebo upravit kontroly a klikněte na funkci **Karta**.
3. V záložce účtování vyberte jednu z možností, například pole **Kontrolovat kód lokace**. 
4. Na **Kartě nastavení uživatelů** vyberte funkci **Řádky** pro definici kontrolované hodnoty.
5. Na stránce **Řádky nastavení uživatelů** můžete vybírat, co se má kontrolovat. V tomto případě například **Lokace (Zvýšení množství)** a vyberte patřičnou lokaci.
6. Po tomto nastavení v kombinaci se zapnutou kontrolou na **Kartě nastavení uživatelů** bude uživateli dovoleno účtovat příjem zboží na vybranou lokaci.
7. Pokud budete chtít kontrolu vypnout, stačí pouze na **Kartě nastavení uživatelů** vybrat pole dané kontroly a odebrat výběr, v tomto případě **Kontrolovat kód lokace**.
8. Po nastavení kontrol můžete stránku zavřít.


## Viz také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[Česká lokální funkcionalita](czech-local-functionality.md)  
