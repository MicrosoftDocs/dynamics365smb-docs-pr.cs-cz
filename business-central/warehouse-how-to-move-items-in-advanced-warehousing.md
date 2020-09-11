---
title: How to Move Items in advanced warehouse configurations | Microsoft Docs
description: In advanced warehouse configurations, that is, locations with directed put-away and pick, warehouse movements between bins are performed by a senior employee preparing warehouse movements in the movement worksheet and then creating the warehouse movements for warehouse employees to perform.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 04/01/2020
ms.author: sgroespe

---
# Přesouvání zboží v rozšířených konfiguracích skladu
V pokročilých konfiguracích skladu, tedy v lokacích s řízeným zaskladněním a vyskladněním, jsou přesuny skladu mezi přihrádky prováděny vedoucím zaměstnancem, který připravuje přesuny v sešitu přesunu a poté vytváří přesuny ve skladu pro zaměstnance skladu k provedení.

## Přesunutí zboží pomocí sešitu skladového přesunu
Stránka **Sešit přesunu** má dvě funkce, které mohou pomoci při automatickém vyplňování řádků. První je funkce **Vypočítat doplnění přihrádky**. Tato funkce používá pořadí přihrádek k navržení doplnění pro vysoce řazené přihrádky z přihrádek s nízkým pořadím. Druhou je funkce **Načíst obsah přihrádky**, která vyplní řádky sešitu celým obsahem přihrádky nebo přihrádek, které zadáte.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit přesunu** a poté vyberte související odkaz.
2. Podle potřeby zadejte informace o přesunu skladu na řádky sešitu.
3. Vyberte akci **Vytvořit přesun** a vytvořte doklad přesunu skladu, který pak může být registrován po dokončení přesunu.

### Zápis přesunu skladu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Přesuny** a poté vyberte související odkaz.
2. Otevřete přesun skladu, který chcete zpracovat.
3. Na řádcích typu akce **Vložit** určete, kde, kdy a které zboží má být přesunuto pomocí úpravy polí **Kód zóny**, **Kód přihrádky**, **Množ. ke zpracování** nebo **Datum vyřízení**.

   Pokud byl váš sklad nastaven tak, aby kódy přihrádek sledovaly fyzickou strukturu skladu, můžete odebrat množství několika zboží z po sobě jdoucích hromadných přihrádek a poté je umístit do dopředných výdejních přihrádek, které mohou být také blízko sebe.
4. Na řádcích typu akce **Vzít** zadejte v poli **Množ. ke zpracování** část množství obsahu přihrádky, který chcete přesunout. Všechna ostatní pole na řádcích typu akce **Vzít** jsou pouze pro čtení.
5. Chcete-li přesunout všechna navrhovaná množství, jak je uvedeno v poli **Množství** vyberte akci **Automat.vyplnit  množ.ke zprac.**.
6. Vyberte akci **Zápis**.

> [!NOTE]
> Pokud lokace používá řízené zaskladnění/vyskladnění, nemůžete ručně přesouvat zboží do nebo z přihrádek typu K příjmu, protože zboží v těchto přihrádkách musí být zapsáno jako zaskladněné, než jsou součástí dostupných zásob.

## Zápis přesunu zboží, ke kterému již došlo
Pokud lokace používá řízené zaskladnění a vyskladnění a potřebujete přesunout zboží do jiných přihrádek bez již existujícího zaskladnění, vyskladnění nebo přesunu, můžete zapsat správné umístění zboží ve skladu pomocí **Deníku  přeřazení skladu**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník  přeřazení skladu** a poté vyberte související odkaz.
2. Vyplňte pole **Číslo zboží**, **Z kódu zóny**, **Z kódu přihrádky**, **Do kódu zóny** a **Do kódu přihrádky**.
3. Vyberte akci **Zápis**.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
