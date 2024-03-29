---
title: Czech Local Functionality - Exchange Rates Adjustment Feature | Microsoft Docs
description: Companies in the Czech Republic request some improvements in the Exchange Rates Adjustment feature in the Czech version of Business Central.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Finance, Localization, CZ
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Úprava směnných kurzů (Přepočet pohledávek, závazků, bankovních účtů a pokladen)

Většina firem v České republice požaduje následující vylepšení, která mají být realizována v oblasti úpravy směnných kurzů při přepočtu pohledávek a závazků:

- Možnost řídit úpravu směnných kurzů samostatně pro bank. účty, zákazníky a dodavatele
- Možnost účtovat úpravu směnného kurzu v detailu nebo souhrnně dle měny
- Možnost spustit úpravu směnných kurzů jako simulaci (bez účtování) v testovacím režimu

Ve standardní sestavě Úprava směnných kurzů je nyní možné:

- Nastavit bankovní účet, zákazníka nebo dodavatele jako filtr
- Vybrat úpravu jen pro zákazníky nebo dodavatele nebo bankovní účty
- Zvolit testovací režim
- Vybrat sumarizaci položek
- Vybrat způsob přenosu dimenzí

Úprava směnných kurzů rovněž obsahuje změněný princip výpočtu pro realizované zisky a ztráty na základě Zákona o daních z příjmů. Tato funkce vypočítá realizovaný zisk nebo ztrátu proti naposledy upraveným částkám.
Tato funkce ve standardní verzi Microsoft [!INCLUDE[d365fin](../../includes/d365fin_long_md.md)] nejdříve odúčtuje nerealizovaný zisk nebo ztrátu a pak vypočítá realizovaný zisk nebo ztrátu. Výpočet je proveden proti částce v původním kurzu při zpracování platby a faktury.
Nový princip výpočtu zpracovává odchylky oproti aktuálně upravenému směnnému kurzu.
Úprava směnných kurzů byla rozšířena i o český modul zálohy.

![Úprava směnných kurzů](Media/exchange-rates-adjustment.png)

## Použití úpravy směnných kurzů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Úprava směnných kurzů rozšířená** a poté vyberte související odkaz.
2. Otevře se Vám stránka **Úprava směnných kurzů rozšířená** - náhled sestavy před spuštěním.
3. Sestavě můžete nastavit vstupní parametry jako:
    - Počáteční a Koncové datum
    - Text položky
    - Zúčtovací datum
    - Možnost úpravy:
        - Dodavatele
        - Zákazníka
        - Bankovní účty a pokladny
        - Finanční účty pro přídavnou měnu pro hlášení
    - Možnost Účtovat
    - Sumarizovat položky
    - Možnost přenášet dimenze
    - Nastavit filtry:
        - Měny
        - Bankovního účtu a pokladny
        - Zákazníka
        - Dodavatele
4. Sestavu následně spusťte.


## Viz také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](../../finance.md)  
