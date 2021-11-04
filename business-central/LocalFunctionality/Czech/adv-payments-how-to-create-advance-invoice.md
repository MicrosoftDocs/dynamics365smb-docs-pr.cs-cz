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

# Vytvoření zálohové faktury

Pro přímé založení zálohové faktury pustupujte následujícím způsobem:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní zálohové faktury** a poté vyberte související odkaz. V případě nákupu hledejte **Nákupní zálohové faktury**.
2. V přehledu založte nový doklad pomocí akce **Nový**.
3. V novém dokladu vyberte **Šablonu zálohy**, která bude použita pro číslování dokladů, způsobu práce s DPH, způsob účtování a další. 
4. Potvrďte pole **Číslo**, čímž je vytvořen doklad zálohy v příslušné číselné řadě. 
5. V kartě zálohy přiřaďte **Číslo zákazníka**.
6. V řádku zálohy zadejte **DPH účto skupinu zboží** a **Celkovou částku zálohy**.
7. Výchozí stav zálohy je **Nový**, tzn. je možné ji jakkoli měnit, není možné ji zaplatit nebo použít do faktury. Pomocí funkce **Vydat** v pásu akcí převeďte do stavu **K úhradě**. Záloha bude připravena k platbě.  
Vydáním vzniká v položkách zálohy **Původní položka** s datem podle zúčtovacího data v hlavičce zálohy a celkovou částkou zadanou v okamžiku vydání. Původní položka nemá účetní souvislost, slouží pro výpočet zbývající částky k úhradě.
8. Zálohu můžete vytisknout pomocí akce **Sestava – Záloha** nebo vygenerovat jako PDF přílohu pomocí akce **Sestava – Připojit jako PDF**.
9. Pokud je třeba zálohu upravit, je možné ji pomocí funkce **Znovu otevřít** převést opět do stavu **Nové** a upravovat.  
Automaticky se vytvoří i záporná **Původní položka** v položkách zálohy
10. Ve FactBoxu zálohy je možné průběžně sledovat zapsanou hodnotu zálohy, částku, kterou zbývá uhradit, zbývající částku k použití zálohy a celkovou evidenci zálohy z hlediska základu a částky DPH.

## Viz také

[Zálohové platby pro Česko (rozšíření)](ui-extensions-advance-payments-localization-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
[Finance](../../finance.md)
