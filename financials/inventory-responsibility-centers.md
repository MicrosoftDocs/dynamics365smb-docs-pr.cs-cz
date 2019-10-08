---
title: Jak pracovat s centry odpovědnosti | Microsoft Docs
description: 'Centra odpovědnosti poskytují schopnost spravovat administrativní střediska. Centrem odpovědnosti může být nákladové centrum, ziskové centrum, investiční centrum nebo jiné administrativní centrum definované společností.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2017
ms.author: sgroespe
---
# <a name="work-with-responsibility-centers"></a>Práce s Centry odpovědnosti
Centra odpovědnosti poskytují schopnost spravovat administrativní střediska. Centrem odpovědnosti může být nákladové centrum, ziskové centrum, investiční centrum nebo jiné administrativní centrum definované společností. Příkladem center odpovědnosti je prodejní kancelář, nákupní oddělení pro několik míst a kancelář pro plánování továren. Například pomocí této funkce mohou společnosti nastavit uživatelsky specifické pohledy na prodejní a nákupní doklady související výhradně s konkrétním centrem odpovědnosti.  

Použití více umístnění společně s odpovědnými centry poskytuje možnost řídit obchodní operace nejflexibilnějším a zároveň optimálním způsobem.

Více umístnění umožňuje společnostem spravovat své zásoby na více místech pomocí jedné databáze. Základními kameny této části jsou dva koncepty, umístění a skladovací jednotky. Umístění je definováno jako místo, které zpracovává fyzické umístění a množství zboží. Koncept je dostatečně široký, aby zahrnoval místa, jako jsou závody nebo výrobní zařízení, jakož i distribuční centra, sklady, předváděcí místnosti a servisní vozidla. Skladová jednotka je definována jako položka na konkrétním místě a/nebo jako varianta. Pomocí skladových jednotek mohou společnosti s více pobočkami přidávat informace o doplňování, adresy a některé finanční účetní informace na úrovni umístění. Výsledkem je, že mají schopnost doplňovat varianty téže položky pro každé místo, jakož i objednávat položky pro každé místo na základě informací o doplňování pro konkrétní umístění.  

Centra odpovědnosti rozšiřují funkčnost více umístění tím, že uživatelům umožňují spravovat administrativní centra. Centrem odpovědnosti může být nákladové centrum, ziskové centrum, investiční centrum nebo jiné administrativní centrum definované společností. Příkladem center odpovědnosti je prodejní kancelář, nákupní oddělení pro několik míst a kancelář pro plánování továren. Například pomocí této funkce mohou společnosti nastavit uživatelsky specifické pohledy na prodejní a nákupní doklady související výhradně s konkrétním centrem odpovědnosti.

## <a name="to-set-up-a-responsibility-center"></a>Zřídit Centrum odpovědností  
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Centra odpovědnosti** a pak vyberte související odkaz.  
2. Zvolte akci **Nový**.  
3. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

   Pokud pro správu vaší společnosti používáte centra odpovědnosti, může být užitečné mít výchozí středisko odpovědnosti pro vaši společnost.
4. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Informace o společnosti** a pak vyberte související odkaz.
5. Do pole **Centrum odpovědnosti** zadejte kód střediska odpovědnosti.

Tento kód bude použit ve všech dokumentech o nákupu, prodeji nebo servisu, pokud uživatel, zákazník nebo prodejce nemá žádné výchozí centrum odpovědnosti. V jakémkoli prodejním, nákupním nebo servisním dokumentu můžete zadat jiné centrum odpovědnosti než výchozí.

> [!NOTE]  
>  Když do dokumentu zadáte kód centra odpovědnosti, ovlivní to adresu, dimenze a ceny v dokumentu.  

## <a name="to-assign-responsibility-centers-to-users"></a>Přiřazení center odpovědnosti uživatelům  
Můžete nastavit uživatele tak, aby v jejich každodenních rutinách program načítal pouze dokumenty relevantní pro jejich konkrétní pracovní oblasti. Uživatelé jsou obvykle spojeni s jedním centrem odpovědnosti a pracují pouze s dokumenty souvisejícími s konkrétními oblastmi aplikace v tomto konkrétním centru.  

Chcete-li to nastavit, přiřaďte centra odpovědnosti uživatelům ve třech funkčních oblastech: Nákup, prodej a správa služeb.  

1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Nastavení uživatelů** a pak vyberte související odkaz.  
2.  V okně **Nastavení uživatele** vyberte uživatele, kterému chcete přiřadit centrum odpovědnosti. Pokud uživatel není na seznamu, musíte do pole **ID Uživatele** zadat ID uživatele.  
3.  V poli **Filtr prod. centra odpovědnosti**  zadejte centrum odpovědnosti, kde bude mít uživatel úkoly související s prodejem.  
4.  V poli **Filtr nák. centra odpovědnosti** zadejte centrum odpovědnosti, kde bude mít uživatel úkoly související s Nakupování.  
5.  V poli **Filtr servis. centra odpovědnosti**  zadejte centrum odpovědnosti, kde bude mít uživatel úkoly související se správou služeb.  

> [!NOTE]  
>  Uživatelé budou stále moci zobrazit všechny zaúčtované dokumenty a položky knihy, nejen ty, které se vztahují k jejich vlastnímu centru zodpovědnosti.

## <a name="see-also"></a>Viz také  
[Nastavení zásob](inventory-setup-inventory.md)  
[Nastavení Správy skladu](warehouse-setup-warehouse.md)
[Zásoby](inventory-manage-inventory.md)[Správa skladu](warehouse-manage-warehouse.md)  
[Správa skladů](warehouse-manage-warehouse.md)    
[Podrobnosti návrhu: Správa skladů](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
