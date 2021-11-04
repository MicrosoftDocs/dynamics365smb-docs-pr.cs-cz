---
title: Advance Payments activation and upgrade
description: This section describes Advance Payments Localization for Czech extension functionality.
author: v-pejano

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Advance Payments, Localization
ms.date: 10/01/2021
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Vytvoření zálohové faktury z objednávky  

Zálohu je možné založit i prostřednictvím objednávky. Pro založení zálohy postupujte následujícím způsobem:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz. V případě nákupu hledejte **Nákupní objednávky**.
2. Vytvořte novou prodejní objednávku.
3. Po založení objednávky (vč. řádků) spusťte funkci **Vytvořit zálohu** z sekce **Záloha**. 
4. V dialogovém okně pro vytvoření zálohy zvolte **Kód zálohy** (návaznost do tabulky Šablona záloh) a způsob vytvoření zálohy. Můžete zadat % zálohy nebo přímo částku, na kterou chcete zálohu vytvořit.  
Pokud zvolíte možnost **Navrhnout podle řádku**, vytvoří se záloha 1:1 podle řádků objednávky, tedy kolik řádků obsahuje objednávka, tolik jich bude i v záloze. Pokud není volba N**avrhnout podle řádku zaškrtnuta**, částky se do zálohy nakumulují podle sazeb a DPH účto skupin použitých v řádcích objednávky.
5. Po potvrzení vytvoření zálohy se otevře karta zálohy. Je možné ji zkontrolovat, příp. upravit, vytisknout a vydat, aby byla připravena k úhradě.

Z přehledu **Prodejní zálohové faktury** (v případě nákupu Nákupní zálohové faktury) je možné pomocí funkce **Propojené doklady** zobrazit doklad (objednávku), se kterým je záloha propojena.


## Viz také

[Zálohové platby pro Česko (rozšíření)](ui-extensions-advance-payments-localization-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
[Finance](../../finance.md)
