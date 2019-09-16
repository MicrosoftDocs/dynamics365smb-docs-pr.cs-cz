---
title: Nastavení osvědčených postupů - Způsob přiobjednání | Microsoft Docs
description: 'Pole Způsob přiobjednání na kartě zboží nabízí čtyři různé plánovací metody, které určují jak bude každý individuální plánovací parametr reagovat.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="setup-best-practices-reordering-policies"></a>Nastavení osvědčených postupů: Způsob přiobjednání
Pole **Způsob přiobjednání** na kartě zboží nabízí čtyři různé plánovací metody, které určují jak bude každý individuální plánovací parametr reagovat.  

Jedním z nejlépe osvědčených postupů pro výběr způsobu přiobjednání zboží, je podle klasifikace ABC. Když používáte klasifikaci ABC pro řízení zásob a plánování zásob, je zboží spravováno podle tří různých tříd v závislosti na jejich hodnotě a objemu vzhledem k celkové zásobě. V následující tabulce je uvedeno rozdělení hodnot a objemu tří tříd.

|Třída|Procento z celkového objemu zásob|Procento z celkové hodnoty zásob|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|20|20|
|C|60-70|10-30|

Klasifikace ABC uvádí, že úsilí a peníze lze ušetřit použitím volnějšího řízení zboží s nízkou hodnotou a nízkým objemem než na položky s vysokou hodnotou a vysokým objemem. Následující ilustrace nastiňuje, jaký způsob přiobjednání se v [!INCLUDE[d365fin](includes/d365fin_md.md)] nejlépe hodí pro položky A, B, nebo C.

![Klasifikace ABC](media/abc_classification.png "abc_classification")

Následující tabulka obsahuje osvědčené postupy pro výběr mezi čtyřmi zásadami.  

|Možnosti nastavení|Osvědčený postup|Komentář|  
|------------------|-------------------|-------------|  
|**Pořadí**|Použítí pro položky A.<br /><br /> Použití pro položky vyrobené na zakázku.<br /><br /> Při výrobě, kde je použito zboží nejvyšší úrovně, drahé komponenty a podsestavy.<br /><br /> Použití pro zboží, které je zakoupeno jako přímá dodávka zboží a speciální objednávky.<br /><br /> Nepoužívejte, pokud neakceptujete automatickou rezervaci.|Zboží skupiny A, jako jsou například kožené pohovky v obchodě s nábytkem, jsou to předměty vysoké hodnoty s nízkou a nepravidelnou rychlostí objednávky, kde není možné je mít na skladě, nebo se požadované atributy liší. Nejlepší způsob přiobjednání je tedy ten, který je plánován na každou poptávku zvlášť.|  
|**Dávka-pro-dávku**|Použítí pro položky B.<br /><br /> Při výrobě, použijte pro komponenty, které se vyskytují ve více kusovnících. Tím je zajištěno, že nákupní objednávky jsou kombinovány u stejného dodavatele, takže lze vyjednat lepší ceny.<br /><br /> Použijte, pokud si nejste jisti, kterou politiku pro přeskupování vybrat.|Položky B, jako jsou jídelní židle, mají pravidelnou a poměrně vysokou rychlost objednávky, ale také vysoké přepravní náklady. Nejlepší politika pro přeskupování zboží B je proto taková, která je ekonomickým spojením poptávky v cyklu změny pořadí.<br /><br /> 80 procent zboží může použít tuto zásadu.<br /><br /> Lze úspěšně použít bez parametrů plánování.|  
|**Opraveno Množství.**|Použítí pro položky C.<br /><br /> Kombinujte s parametry pro změnu pořadí.<br /><br /> Při výrobě použijte kritické komponenty.<br /><br /> Nepoužívejte, pokud je zboží často rezervováno.|Zboží skupiny C, jako například čajové šálky, jsou položky nízké hodnoty s vysokou a pravidelnou rychlostí objednávky. Nejlepší politika pro přeskupování zboží C je proto taková, která garantuje nepřetržitou dostupnost a zůstáním nad bodem přiobjednání.<br /><br /> Pokud si uživatel rezervuje množství pro určitou vzdálenou poptávku, bude plánovací základna narušena. I když je plánovaná úroveň zásob přijatelná s ohledem na pořadí, množství nemusí být kvůli rezervaci k dispozici.|  
|**Maximální množství**|Používejte pro položky C s vysokými skladovými náklady, nebo s omezením skladování.<br /><br /> Kombinujte s jedním nebo více modifikátory objednávek (minimální / maximální množství objednávky nebo více objednávek najednou).|Zboží skupiny C, jako například čajové šálky, jsou položky nízké hodnoty s vysokou a pravidelnou rychlostí objednávky. Nejlepší politika pro přeskupování zboží C je proto taková, která garantuje nepřetržitou dostupnost a zůstáním nad bodem přiobjednání, ale pod maximálním množstvím zásob<br /><br /> Chcete-li změnit navrhovanou objednávku, můžete chtít snížit množství objednávky na stanovené maximální množství objednávky, zvýšit na určité minimální množství objednávky nebo zaokrouhlit nahoru, aby bylo možné splnit určený násobek objednávky. **Poznámka:**  Pokud je použit s bodem přiobjednání, zůstává inventář mezi bodem přiobjednání a maximálním množstvím.|  

## <a name="see-also"></a>Viz také  
 [Nastavení osvědčených postupů: Plánovač dodávek](setup-best-practices-supply-planning.md)   
 [Podrobnosti návrhu: Způsob přiobjednání](design-details-reordering-policies.md)   
 [Podrobnosti návrhu: Zakázka](design-details-order.md)   
 [Podrobnosti návrhu: Dávka-pro-dávku](design-details-lot-for-lot.md)   
 [Podrobnosti návrhu: Pevné přiobj.množ](design-details-fixed-reorder-qty.md)   
 [Podrobnosti návrhu: Maximální množství](design-details-maximum-qty.md)   
 [Osvědčené postupy při nastavení komplexních oblasti aplikace](set-up-complex-application-areas-using-best-practices.md)  
 [Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
