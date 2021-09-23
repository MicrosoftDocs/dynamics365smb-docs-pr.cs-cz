---
title: Czech Local Functionality - Inventory Movement Templates
description: The following topics describe the local functionality Inventory Movement Templates in the Czech version of Business Central.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Inventory, Localization, CZ
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---


# Šablony pohybů zásob

Pohyby zboží pořízené v denících zboží musí být účtovány s předepsaným **Účtem adjustace zásob**, který odpovídá danému typu pohybu. Do řádků deníku zboží bylo doplněno pole pro výběr šablony pohybu zásob.  

## Definice vlastní šablony pro účtování pohybů zásob

V rámci šablony je možné nastavit typ skladového pohybu (výdej, příjem, transfer, atp.) a obecnou obchodní účto skupinu (ta určuje finanční kontace účtování daného skladového pohybu do účetní části systému).
Tato nastavení jsou automaticky kopírována do řádku deníku zboží na základě zvolené šablony pohybu zásob.
Šablony skladového pohybu je možné využít především při účtování pohybů v deníku zboží a deníku projektů. Další využití mají při účtování rozdílů fyzické inventury zboží.

Pro vytvoření nové šablony:
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony pohybu zásob** a poté vyberte související odkaz.
2. Na přehledu Šablon pohybu zásob použijte funkci **Nový**.
3. Do pole **Název** zadejte název pro daný pohyb, dále do popisu vypište krátký popis, k čemu pohyb slouží.
4. Ve sloupci **Typ položky** vyberte skladový pohyb.
5. V posledním kroku vyberte patřičnou účtoskupinu do pole **Obecná obchodní účto skupina**.
6. Po vyplnění sloupců přehled zavřete.

## Definice a použití vlastní šablony pro účtování zásob

Příklad definice skladové pohybu pro typu MANKO:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony pohybu zásob** a poté vyberte související odkaz.
2. Na přehledu Šablon pohybu zásob použijte funkci **Nový**.
3. Do pole **Název** zadejte název pro daný pohyb, například **MANKO**. Dále do popisu vypište krátký popis, k čemu pohyb slouží.
4. Ve sloupci **Typ položky** vyberte pohyb, v tomto příkladu **Výdej**.
5. V posledním kroku vyberte patřičnou účtoskupinu do pole **Obecná obchodní účto skupina**, pro příklad s mankem například **Z-MANKO**.
6. Po vyplnění sloupců přehled zavřete.
## Použití Šablony v deníku zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník zboží** a poté vyberte související odkaz.
2. Založte nový řádek deníku.
3. Zobrazte nové pole **Šablona skladového pohybu**.
4. V poli **Šablona skladového pohybu** vyberte šablonu vytvořenou v předchozím kroku.
5. Zkontrolujte pole **Typ položky** a **Obecná obch. účto skupina**, zda se doplnili dle nastavení v minulém kroku.

## Použití šablony v řádku objednávky fyz. inventury 
 1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Objednávky fyzické inventury** a poté vyberte související odkaz.
2. Na přehledu Objednávek fyzické inventury zvolte tlačítko **Nový**.
3. Vyplňte pole **Popis** dle potřeby.
4. Použijte funkci **Výpočet řádků** s potřebnými parametry.
    - Lokace
    - Číslo
5. Použijte funkci **Vytvořit nový Záznam**.
6. Z objednávky fyz. inventury otevřete vytvořený záznam.
7. Na řádku vyplňte **Množství** a dále použijte funkci **Dokončit**.
8. Poté se vraťte na přehled **Objednávky fyzické inventury**, kde na vybraném záznamu použijte funkci **Vypočítat očekávané množství** a poté **Dokončit**.

## Viz také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[Česká lokální funkcionalita](czech-local-functionality.md)  
