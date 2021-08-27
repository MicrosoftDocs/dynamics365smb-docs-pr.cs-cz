---
title: Czech Local Functionality - Advances features of physical inventory 
description: Companies need to distinguish the posting of inventory movements of the same goods so they require line-break of physical inventory Journal line.
author: v-makune

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Inventory, Localization, CZ
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---


# Rozšíření přípravy fyzické inventury  

Pro dodržování účetních standardů vyžadují společnosti odlišení účtování mank a přebytků v rámci fyzické inventury. 
Společnosti potřebují odlišit účtování inventarizačních pohybů zásob stejného zboží (např. mít jiné účtování pro manka v limitu a jiné pro manka nad limit). 

## Nastavení fyzické inventury (šablony)

Díky nastavení výchozích šablon skladového pohybu pro tyto pohyby zásob v Nastavení zásob, může uživatel snadno změnit Obecnou obchodní účto skupinu v závislosti na typu pohybu zásob.

1. Pomocí vyhledávací funkce ![Žárovky, která otevře funkci Řekněte mi, co chcete dělat (Alt + Q)](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat (Alt + Q)") vyhledejte **Nastavení zásob**.
2. Na stránce **Nastavení zásob** na záložke Fyzická inventúra vyplňte pole **Výchozí šablona pro příjem fyzické inventury** a **Výchozí šablona pro výdej fyzické inventury**.
3. Poté můžete stránku zavřít.

![Physical inventory - advances features](Media/advances_features_physical_inventory.png)
 
## Použití
### Šablona v deníku fyzické inventury
Šablona se automaticky vyplní do deníku fyzické inventury:
1. Pomocí vyhledávací funkce ![Žárovky, která otevře funkci Řekněte mi, co chcete dělat (Alt + Q)](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat (Alt + Q)") vyhledejte **Deník fyzické inventury**.
2. Na stránce **Deník fyzické inventury** klikněte na Akce -> Funkce -> **Vypočítat množství zásob...**
3. Vyplňte parametre podle potřeby (zbožím, které máte na skladu) a klikněte na možnost OK.
1. Pokud v poli **Množství (fyz.inventura)** změníte množství (zvýšíte nebo znížíte, podle reálního stavu), změní se hodnota v poli **Šablona pohybu zásob** na daném řádku podle toho, zda se jedná o Manko nebo Přebytek.

Poznámka: Automatické vyplnění pole **Šablona pohybu zásob** je přidáno i pro vytváření objednávek fyz. inventury.

### Funkce „Vložit nový prázdný řádek“
 Na stránce **Deník fyzické inventury** se nachází funkce **Vložit nový prázdný řádek**.

Pokud jste v deníku vytvořili řádek a spustili tuto funkci (Akce -> Funkce -> Vytvořit nový prázdný řádek), vytvoří se v deníku nový prázdný řádek z aktuálního řádku, na který je při spuštění umístěn kurzor. Takto vložený nový řádek bude mít stejné hodnoty jako zkopírovaný řádek, ale v polích Množství (vypočteno) a Množství (fyzický inventář) bude mít nový řádek nulovou hodnotu.



## Viz také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
