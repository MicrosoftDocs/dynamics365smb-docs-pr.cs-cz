---
title: Správa zásob| Microsoft Docs
description: 'Popisuje, jak spravovat fyzické produkty, se kterými obchodujete, například manipulaci se zásobami ve vašem skladu.'
documentationcenter: ''
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.date: 01/15/2020
ms.reviewer: v-zdbice
ms.author: sgroespe
---

# Zásoby

Pro každý fyzický produkt, se kterým obchodujete, musíte vytvořit kartu zboží typu **Zásoby**. Zboží, které nabízíte zákazníkům, ale neuchovávejte je v zásobách, můžete evidovat jako zboží katalogu, které můžete v případě potřeby převést na skladové zboží. Množství zboží ve skladu můžete zvýšit nebo snížit zaúčtováním přímo do položek zboží, například po fyzické inventuře nebo pokud neevidujete nákupy.

Zvýšení a snížení zásob se automaticky zaznamenává také při účtování nákupních a prodejních dokladů. Pro více informací navštivte [Zpracování nákupu](purchasing-how-record-purchases.md), [Prodej produktů](sales-how-sell-products.md)a [Fakturace prodeje](sales-how-invoice-sales.md). Převody mezi lokacemi mění množství zásob ve skladech vaší firmy.

Chcete-li zlepšit přehled o zboží a usnadnit jejich vyhledání, můžete zboží kategorizovat a přiřadit jim atributy pro vyhledávání a řazení.

> [!NOTE]
> Fyzické pohyby zboží se označují jako aktivity skladu. Pro více informací navštivte [Správa skladu](warehouse-manage-warehouse.md).

Plánování zboží pro splnění poptávky je zahrnuto jako součást funkcionality plánování zásob. Další informace viz [Plánování](production-planning.md).

## <a name="inventory-reconciliation"></a>Odsouhlasení zásob

Při účtování skladových transakcí, jako jsou prodejní dodávky, nákupní faktury nebo adjustace zásob, se změněné náklady na zboží zaznamenávají do položek ocenění zboží. Pro zohlednění této změny hodnoty zásob ve finančních knihách jsou náklady na zásoby automaticky zaúčtovány na související účty zásob ve financích. Pro každou skladovou transakci, kterou účtujete, jsou příslušné hodnoty zaúčtovány na účet zásob, účet adjustace a účet nákladů na prodané zboží ve financích. Pro více informací navštivte [Odsouhlasení nákladů na zboží s financemi](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

I když jsou náklady na zásoby automaticky zaúčtovány do financí, je stále nutné zajistit, aby náklady na zboží byly předány do souvisejících transakcí prodeje, zejména v situacích, kdy zboží prodáváte dříve, než fakturujete nákup tohoto zboží. Tento proces se označuje jako adjustace nákladů. Náklady na zboží jsou automaticky adjustovány při účtování transakcí zboží, ale můžete také spustit úpravu nákladů na zboží ručně. Pro více informací navštivte [Adjustace nákladů zboží](inventory-how-adjust-item-costs.md).

| Funkce | Odkaz |
|---|----|
|Vytvořte kartu zboží pro skladové zboží, se kterým obchodujete.|[Evidence nového zboží](inventory-how-register-new-items.md)|
|Strukturujte nadřazené zboží, které prodáváte jako sadu sestávající z komponent nebo které sestavujete na zakázku nebo na sklad.|[Práce s kusovníkem](inventory-how-work-BOMs.md)|
|Udržujte si přehled o zboží a zlepšete hledání a řazení zboží jeho uspořádáním do kategorií.|[Kategorizace zboží](inventory-how-categorize-items.md)|
|Přiřaďte atributy různých typů Vašemu zboží, které vám pomůžou řadit a vyhledávat zboží.|[Práce s Atributy zboží](inventory-how-work-item-attributes.md)|
|Vytvořte speciálních karty zboží pro zboží, které nabízíte zákazníkům, ale neevidujete pro ně zásoby.|[Práce se zbožím katalogu](inventory-how-work-nonstock-items.md)|
|Proveďte fyzickou inventuru Vašich zásob s pomocí **Objednávek fyzické inventury** a **Záznamů fyzické inventury**.|[Doklady pro inventarizace zásob](inventory-how-count-inventory-with-documents.md)|
|Proveďte fyzickou inventuru, udělejte úpravy zásob pomocí výdeje nebo příjmu, či změňte informace, jako je lokace nebo číslo šarže v položkách zboží.|[Výpočet, úprava a přeřazení skladových zásob](inventory-how-count-adjust-reclassify.md)|
|Zobrazte si dostupnost zboží dle lokací, dle období, prodejní nebo nákupní události nebo jeho použití v montážních nebo výrobních kusovnících.|[Zobrazení dostupnosti zboží](inventory-how-availability-overview.md)|
|Převádějte zboží mezi lokacemi pomocí objednávek transferu nebo pomocí deníku přeřazení zboží.|[Transfer zásob mezi lokacemi](inventory-how-transfer-between-locations.md)|
|Rezervujte zásoby nebo přijímané zboží pro prodejní objednávky, nákupní objednávky, servisní zakázky, montážní zakázky nebo výrobní zakázky.|[Rezervace zboží](inventory-how-to-reserve-items.md)|
|Nastavte si popisů zboží dle dodavatele nebo zákazníka, abyste mohli snadno a rychle vkládat popis zboží do obchodních dokladů.|[Použití křížových odkazů zboží](inventory-how-use-item-cross-refs.md)|
|Přiřaďte sériová čísla nebo čísla šarží k jakémukoli výstupnímu nebo vstupnímu dokladu nebo řádku deníku, například pro sledování zboží v případě vratky.|[Práce se sériovými čísly a čísly šarží](inventory-how-work-item-tracking.md)|
|Zjistěte, kde bylo v dodavatelském řetězci použito sériové číslo nebo čísla šarže, například v případě reklamace.|[Trasování zboží](inventory-how-to-trace-item-tracked-items.md)|
|Zablokujte zboží pro zadávání do prodejních nebo nákupních řádků nebo pro účtování v libovolné transakci.|[Blokace zboží](inventory-how-block-items.md)|
|Spravujte obchodní operace v prodejních kancelářích, nákupních odděleních nebo kancelářích pro plánování výroby na více místech.|[Práce s centry zodpovědnosti](inventory-responsibility-centers.md)|

## Viz také

[Správa skladů](warehouse-manage-warehouse.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
