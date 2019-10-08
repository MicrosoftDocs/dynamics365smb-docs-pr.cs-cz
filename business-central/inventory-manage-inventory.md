---
title: Správa zásob| Microsoft Docs
description: 'Popisuje, jak spravovat fyzické produkty, se kterými obchodujete, například manipulaci se zásobami ve vašem skladu.'
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, stock'
ms.date: 03/11/2019
ms.author: sgroespe
---

# <a name="inventory"></a>Zásoby
Pro každý fyzický produkt, se kterým obchodujete, musíte vytvořit kartu zboží typu **Zásoby**. Zboží, které nabízíte zákazníkům, ale neuchovávejte je v zásobách, můžete registrovat jako zboží katalogu, které můžete v případě potřeby převést na skladové zboží. Množství zboží ve skladu můžete zvýšit nebo snížit zaúčtováním přímo do položek zboží, například po fyzickém počítání nebo pokud nezaznamenujete nákupy.

Zvýšení a snížení zásob se přirozeně zaznamenává také při účtování nákupních a prodejních dokladů. Pro více informací navštivte [Zaznamenání nákupu](purchasing-how-record-purchases.md), [Prodej produktů](sales-how-sell-products.md)a [Fakturace prodeje](sales-how-invoice-sales.md). Převody mezi lokacemi mění množství zásob ve skladech vaší firmy.   

Chcete-li zvýšit přehled zboží a usnadnit jejich vyhledání, můžete zboží kategorizovat a udělit jim atributy pro vyhledávání a řazení.

> [!NOTE]
> Fyzické zpracování zboží se označuje jako aktivity skladu. Pro více informací navštivte [Správa skladu](warehouse-manage-warehouse.md).

## <a name="inventory-reconciliation"></a>Odsouhlasení zásob
Při účtování skladových transakcí, jako jsou prodejní dodávky, nákupní faktury nebo adjustace skladu, se změněné náklady na zboží zaznamenávají do položek ocenění zboží. Pro zohlednění této změny hodnoty zásob ve finančních knihách jsou náklady na zásoby automaticky zaúčtovány na související skladové účty v hlavní knize. Pro každou skladovou transakci, kterou účtujete, jsou příslušné hodnoty zaúčtovány na účet zásob, účet adjustace a účet COGS v hlavní knize. Pro více informací navštivte [Odsouhlasení nákladů na zboží s hlavní knihou](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

I když jsou náklady na zásoby automaticky zaúčtovány do hlavní knihy, je stále nutné zajistit, aby náklady na zboží byly předány na související transakci odchozího prodeje, zejména v situacích, kdy zboží prodáváte dříve, než vyfakturujete nákup tohoto zboží. To se označuje jako adjustace nákladů. Náklady na zboží jsou automaticky adjustovány při účtování transakcí zboží, ale můžete také upravit náklady zboží ručně. Pro více informací navštivte [Adjustace nákladů zboží](inventory-how-adjust-item-costs.md).

|Viz |také |
|---|----|
|Vytvoření karty zboží pro skladové zboží, se kterým obchodujete.|[Evidence nového zboží](inventory-how-register-new-items.md)|
|Struktura nadřazeného zboží, které prodáváte jako sady sestávající z komponent nadřazeného nebo které sestavujete na objednávku nebo na sklad.|[Práce s kusovníkem](inventory-how-work-BOMs.md)|
|Udržování přehledu zboží a pomoc při hledání a řazení zboží podle jejich uspořádáním v kategoriích.|[Kategorizace zboží](inventory-how-categorize-items.md)|
|Přiřazením atributů zboží různých typů zboží, která vám pomůžou řadit a vyhledávat zboží.|[Práce s Atributy zboží](inventory-how-work-item-attributes.md)|
|Vytvoření speciálních karet zboží pro zboží, které nabízíte zákazníkům, ale neudržují se pro něj zásoby.|[Práce se zbožím katalogu](inventory-how-work-nonstock-items.md)|
|Provádění fyzické inventury, provádění záporné nebo kladné úpravy a změna informací, jako je lokace nebo číslo šarže, u položek zboží.|[Výpočet, úprava a přeřazení skladových zásob](inventory-how-count-adjust-reclassify.md)|
|Zobrazení dostupnosti zboží dle lokací, dle období, prodejní nebo nákupní události nebo jejich použití v montážích nebo výrobních kusovnících.|[Zobrazení dostupnosti zboží](inventory-how-availability-overview.md)|
|Transfer skladového zboží mezi lokacemi s objednávkami transferu, pro správu skladu nebo pomocí deníku přeřazení zboží.|[Transfer zásob mezi lokacemi](inventory-how-transfer-between-locations.md)|
|Rezervace zásob nebo vstupního zboží pro prodejní objednávky, nákupní objednávky, servisní zakázky, montážní zakázky nebo výrobní zakázky.|[Rezervovace zboží](inventory-how-to-reserve-items.md)|
|Vytváření vlastních popisů zboží dodavatele nebo zákazníka, abyste mohli snadno vkládat popis zboží do obchodních dokladů.|[Použití křížových odkazů na položky](inventory-how-use-item-cross-refs.md)|
|Přiřazení sériových čísel nebo čísel šarží k jakémukoli výstupnímu nebo vstupnímu dokladu nebo řádku deníku, například ke sledování zboží v případě navrácení.|[Práce se sériovými čísly a čísly šarží](inventory-how-work-item-tracking.md)|
|Nastavení vlastního popisu zboží dodavatele nebo zákazníka tak, aby bylo možné rychle vložit popis zboží do obchodních dokladů.|[Použití křížových odkazů na zboží](inventory-how-use-item-cross-refs.md)|
|Zjištění, kde bylo v dodavatelském řetězci použito sériové číslo nebo čísla šarže, například v situacích reklamace.|[Sledování zboží - Sledované zboží](inventory-how-to-trace-item-tracked-items.md)|
|Zablokování zboží, které má být zadáno v prodejních nebo nákupních řádcích nebo zaúčtovány v libovolné transakci.|[Blokace zboží](inventory-how-block-items.md)|
|Správa obchodních operací v prodejních kancelářích, nákupních odděleních nebo kancelářích pro plánování závodu na více místech.|[Práce s centry zodpovědnosti](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Viz také  
[Správa skladů](warehouse-manage-warehouse.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)    
[Práce s[!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
