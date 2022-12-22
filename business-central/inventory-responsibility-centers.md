---
title: How to Work with Responsibility Centers
description: Responsibility center as administrative centers help companies set up user-specific views of sales and purchase documents related exclusively to each center.
author: SorenGP

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.search.forms: 5714, 5715
ms.date: 06/16/2021
ms.author: edupont

---
# Práce s Centry odpovědnosti

Centra odpovědnosti poskytují schopnost zvládnout administrativní centra. Centrum odpovědnosti může být nákladové středisko, ziskové středisko, investiční centrum nebo jiné centrum správy definované společností. Příkladem center odpovědnosti je prodejní kancelář, nákupní oddělení pro několik lokací a kancelář pro plánování továren. Například pomocí této funkce mohou společnosti nastavit uživatelsky specifické pohledy na prodejní a nákupní doklady související výhradně s konkrétním centrem odpovědnosti.

Použití více lokací společně s odpovědnými centry poskytuje možnost řídit obchodní operace nejflexibilnějším a zároveň optimálním způsobem.

Více lokací umožňuje společnostem spravovat své zásoby na více místech pomocí jedné databáze. Základními kameny této části jsou dva koncepty, lokace a skladovací jednotky. Lokace je definována jako místo, které zpracovává fyzické umístění a množství zboží. Koncept je dostatečně široký, aby zahrnoval lokace, jako jsou závody nebo výrobní zařízení, jakož i distribuční centra, sklady, předváděcí místnosti a servisní vozidla. Skladová jednotka je definována jako zboží na konkrétní lokaci a/nebo jako varianta. Pomocí skladových jednotek mohou společnosti s více pobočkami přidávat informace o doplňování, adresy a některé finanční účetní informace na úrovni umístění. Výsledkem je, že mají schopnost doplňovat varianty stejného zboží pro každou lokaci, jakož i objednávat zboží pro každou lokaci na základě informací o doplňování pro konkrétní lokaci.

## Zřídit Centrum odpovědností

1. Vyberte ![Žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete delat"), zadejte **Centra odpovědnosti** a pak zvolte související odkaz.
2. Vyberte akci **Nový**.
3. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   Pokud pro správu vaší společnosti používáte centra odpovědnosti, může být užitečné mít výchozí středisko odpovědnosti pro vaši společnost.
4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Informace o společnosti** a vyberte související odkaz.
5. Do pole **Centrum odpovědnosti** zadejte kód centra odpovědnosti.

Tento kód bude použit ve všech dokladech o nákupu, prodeji nebo servisu, pokud uživatel, zákazník nebo prodejce nemá žádné výchozí centrum odpovědnosti. V jakémkoli prodejním, nákupním nebo servisním dokladu můžete zadat jiné centrum odpovědnosti než výchozí.

> [!NOTE]  
> Když na doklad zadáte kód centra odpovědnosti, ovlivní to adresu, rozměry a ceny na dokladu.

## Přiřazení center odpovědnosti uživatelům

Můžete nastavit uživatele tak, aby v jejich každodenních rutinách aplikace načítala pouze doklady relevantní pro jejich konkrétní pracovní oblasti. Uživatelé jsou obvykle spojeni s jedním centrem odpovědnosti a pracují pouze s doklady souvisejícími s konkrétními oblastmi aplikace v tomto konkrétním centru.

Chcete-li to nastavit, přiřaďte centra odpovědnosti uživatelům ve třech funkčních oblastech: Nákup, Prodej a Správa služeb.

1. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Nastavení uživatelů** a poté vyberte související odkaz.
2. Na stránce **Nastavení uživatele** vyberte uživatelů, kterému chcete přiřadit centrum odpovědnosti. Pokud uživatel není v seznamu, musíte zadat ID uživatele do pole **ID uživatele**.
3. Do pole **Filtr prod.  centra  odpovědnosti** zadejte centrum odpovědnosti, kde bude mít uživatel úkoly související s prodejem
4. Do pole **Filtr nák.  centra  odpovědnosti** zadejte centrum odpovědnosti, kde bude mít uživatel úkoly související s nákupem.
5. Do pole **Filtr servis. centra  odpovědnosti** zadejte centrum odpovědnosti, kde bude mít uživatel úkoly související se správou služeb.

> [!NOTE]  
> Uživatelé mohou prohlížet pouze ty zaúčtované doklady, které se týkají jejich vlastního centra odpovědnosti. Mohou však zobrazit všechny položky hlavní knihy a přejít na další zaúčtované doklady z položek hlavní knihy.

## Viz také

[Nastavení zásob](inventory-setup-inventory.md)    
[Nastavení řízení skladu](warehouse-setup-warehouse.md)    
[Zásoby](inventory-manage-inventory.md)    
[Řízení skladu](warehouse-manage-warehouse.md)    
[Podrobnosti o designu: Řízení skladu](design-details-warehouse-management.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]