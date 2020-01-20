---
title: Správa montáže | Microsoft Docs
description: 'Podporujte společnosti, které dodávají produkty svým zákazníkům, kombinováním komponent v jednoduchých procesech bez nutnosti výrobní funkčnosti, ale s funkcemi pro sestavení zboží, které jsou integrovány s existujícími funkcemi, jako například prodej, plánování, rezervace a skladování.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'kit, kitting'
ms.date: 12/20/2018
ms.author: sgroespe
---
# <a name="assembly-management"></a>Správa montáže
Podporujte společnosti, které dodávají produkty svým zákazníkům, kombinováním komponent v jednoduchých procesech bez nutnosti výrobní funkčnosti, ale s funkcemi pro sestavení zboží, které jsou integrovány s existujícími funkcemi, jako například prodej, plánování, rezervace a skladování.[!INCLUDE[d365fin](includes/d365fin_md.md)]  

 Sestavené zboží je definováno jako prodejní zboží skládající se z kusovínku montáže. Pro více informací navštivte [Práce s kusovníkem](inventory-how-work-BOMs.md).

 Montážní zakázky jsou interní objednávky, stejně jako objednávky výrobní zakázky, které se používají ke správě procesu montáže a k propojení požadavků pr prodej s dodatenými aktivitami skladu. Montážní zakázky se liši od jiných druhů objednávek, protože při zaúčtování zahrnují jak výstup tak spotřebu. Hlavička montážní zakázky se chová podobně jako řádek prodejní objednávky a řádky montážní zakázky se chovají podobně jako řádky deníku spotřeby.  

 Aby byla podporována strategie včasných inventur a schopnost přizpůsobit produkty požadavkům zákazníků, mohou být montážní zakázky automaticky vytvořeny a propojeny, jakmile je vytvořen řádek prodejní objednávky. Vazba mezi prodejní poptávkou a montážní zakázkou umožňuje zpracovatelům prodejních objednávek přizpůsobit průběžné zboží k montáži., přislíbit dodací data podle dostupnosti komponent a zaúčtovat výstup a dodávku sestaveného zboží přímo prodejní objednávky. Pro více informací navštivte [Prodej zboží montáže na zakázku](assembly-how-to-sell-items-assembled-to-order.md).  

 Na jednom řádku prodejní objednávky můžete prodat množství, které je k dispozici, a musí být vyskladněno ze skladu společně s množstvím, které musí být sestaveno dle objednávky. Existují určitá pravidla, kterými se řídí rozdělování těchto množství, aby se zajistilo, že množství na zakázku má přednost před množstvím zásob v částečném přepravním zboží. Pro více informací navštivte  sekci “Kombinované scénáře” [Porozumění Montáže na zakázku a montáž na sklad](assembly-assemble-to-order-or-assemble-to-stock.md).  

 Existují speciální funkce, které řídí přepravu množství montáže na zakázku. Když je množství montáže na zakázku připraveno k odeslání, odpovědný pracovník skladu zaúčtuje vyskladnění pro dotyčné řádky prodejní objednávky. To naopak vytvoří skladový pohyb zásob komponent, zaúčtuje výstup montáže a dodávku prodejní objednávky. Pro více informací navštivte  sekci "Zpracování zboží montáže na zakázku a vyskladnění zásob" v [Vyskladnění zboží pomocí vyskladnění zásob](warehouse-how-to-pick-items-with-inventory-picks.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.   

|**Viz**|**také**|  
|------------|-------------|  
|Přečtěte si o rozdílu mezi montáží zboží těsně před odesláním prodejních objednávek a montáží zboží, které jsou určeny ke skladování.|[Princip montáže na zakázku a montáže na sklad](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Vyplněním polí na kartách lokace a v nastavení zásob definujte způsob toku zboží do a z oddělení montáže.|[Nastavení základních lokací s provozními oblastmi](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Přizpůsobení montáže zboží požadavku zákazníka během prodejního procesu a převedení na prodej, je-li přijat.|[Nabídka prodeje montáže na zakázku](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Kombinováním komponent můžete vytvořit zboží v jednoduchém procesu, na zakázku nebo na sklad.|[Montáž zboží](assembly-how-to-assemble-items.md)|  
|Prodej zboží montáže, které momentálně není k dispozici vytvořením propojení montáže na zakázku pro dodání úplného nebo částečného množství prodejní objednávky.|[Prodejn zboží montáže na obejdnávku](assembly-how-to-sell-items-assembled-to-order.md)|
|Pokud je některé zboží montáže na zakázku již na skladě, odečtěte toto množství z montážní zakázky a rezervujte je na skladu.|[Prodej skladového zboží podle montáže na zakázku](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Pokud prodáváte zboží montáže ze skladu a všechny položky nejsou k dispozici, zahajte montážní zakázku, abyste automaticky dodali část nebo celé množství prodejní objednávky.|[Prodej Zboží montáže na zakázku a skladového zboží dohromady](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Vytvoření upravené zboží montáže pro hromadné prodejní objednávky před pravidelným vytvořením skutečných prodejních objednávek dle smlouvy paušální objednávky.|[Vytvoření hromadné montážky zakázky](assembly-how-to-create-blanket-assembly-orders.md)|
|Vrácení zaúčtované montážní zakázky, například proto, že zakázka byla s chybami, které je nutné opravit.|[Vrácení účtování montáže](assembly-how-to-undo-assembly-posting.md)|
|Zjistětě více o rozdílu mezi kusovníkem montáže a výrobním kusovníkem a souvisejicími rozdíly ve zpracování|[Práce s kusovníkem](inventory-how-work-BOMs.md)|
|Zjistěte více o tom, jak se zpracovává spotřeba montážní zakázka a výstup při při účtování a jak jsou odvozené náklady na zboží a zdroje dále jak jsou zpracovávány a distribuovány do hlavní knihy.|[Podrobnosti návrhu: Účtování montážní zakázky](design-details-assembly-order-posting.md)|  

## <a name="see-also"></a>Viz také  
[Práce s kusovníkem](inventory-how-work-BOMs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Podporbnosti návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s[!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
