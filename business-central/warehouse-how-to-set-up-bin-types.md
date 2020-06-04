---
title: Jak nastavit typ přihrádek | Microsoft Docs
description: 'Tok zboží můžete řídit prostřednictvím přihrádek, které jste definovali pro konkrétní skladové činnosti. Každé přihrádce přiřadíte její základní tokové aktivity, tím nadefinujete způsob a druh jakým způsobem se přihrádka používá.'
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
# <a name="set-up-bin-types"></a>Nastavení typu přihrádky
Tok zboží můžete řídit prostřednictvím přihrádek, které jste definovali pro konkrétní skladové činnosti. Každé přihrádce přiřadíte její základní tokové aktivity, tím nadefinujete způsob a druh jakým způsobem se přihrádka používá.  

Existuje šest typů. Můžete provozovat svůj sklad se všemi možnými typy přihrádek, nebo si můžete vybrat, zda chcete pracovat pouze s typy zásobníků PŘÍJEM, VYSKLZASKL, DODAVKA a KVAL. Tyto čtyři typy PŘIHRÁDEK umožňují provádět návrhy, které podporují tok zboží a umožňují zaznamenávat nesrovnalosti v zásobách.  

## <a name="to-set-up-the-bin-types-you-want-to-use"></a>Nastavení typu přihrádky, které chcete použít  
1.  Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Typy přihrádek** a poté vyberte související odkaz.  
2.  V okně **Typy přihrádek** vytvořte 10 místný kód pro typ přihrádky.  
3.  Vyberte činnosti, které lze provádět s každým typem přihrádky.  

> [!NOTE]  
>  Typy přihrádek jsou použitelné pouze v případě, že používáte ve vašem skladu řízené vyskladnění a zaskladnění.  

Typ přihrádky určuje pouze způsob, jakým se přihrádka používá při zpracování toku zboží ve skladu. Návrhy pro jakýkoli doklad skladu můžete vždy přepsat a zboží můžete přesouvat do nebo z libovolné přihrádky provedením pohybu skladu.  

Níže jsou uvedeny typy přihrádek, které můžete vytvořit.  

|Typ přihrádky|Popis|  
|------------------|---------------------------------------|  
|PŘÍJEM|Zboží evidované jako zaúčtované příjmy, ale dosud nezaskladněné.|  
|DODAVKA|Zboží vybrané pro skladové řádky, ale dosud nebyly zaúčtovány jako dodávané.|  
|VYSKL|Typicky zboží, které má být uloženo ve velkých měrných jednotkách, ale které nechcete zpřístupňovat pro vyskladnění. Protože se tyto přihrádky nepoužívají k vyskladnění, a to ani u výrobních objednávek a ani u zásilek, může být používání přihrádky typu Zaskladnění omezené, ale tento typ přihrádky může být užitečný, pokud jste zakoupili velké množství zboží. Přihrádky tohoto typu by měly mít vždy nižší prioritu přihrádek, takže když jsou přijaté položky zaskladněny, jsou nejprve vyřazeny další přihrádky ZASKLVYSKL s vyšší prioritou. Pokud používáte tento typ přihrádky, musíte pravidelně provádět doplňování přihrádky tak, aby položky uložené v těchto přihrádkách byly také k dispozici v přihrádkách typu ZASKLVYSKL nebo VYSKL.|  
|ZASKL|Zboží, která mají být použita pouze pro vyskladnění, například pro zboží s blížícím se datem vypršení platnosti, které jste přesunuli do tohoto typu přihrádky. Do těchto přihrádek ukládáte s vyšší prioritou, takže jsou navrženy tak, aby se vyskladnili jako první.|  
|VYSKLZASKL|Zboží v přihrádkách, které jsou navrženy pro funkce vyskladněni a zaskladnění. Přihrádky tohoto typu pravděpodobně mají rozdílné pořadí přihrádek. Můžete nastavit své přihrádky jako objemné s nížším prioritou přihrádek ve srovnání s běžnými přihrádkami nebo přihrádkami pro vyskladnění.|  
|KVAL|Tato přihrádka se používá pro skladovou ajdustaci. Pokud nastavíte tuto přihrádku na kartě lokace v poli **Kód adjustační přihrádky**. Můžete také nastavit přihrádky tohoto typu pro vadné předměty a kontrolované položky. Položky můžete přesunout do tohoto typu přihrádky, pokud chcete, aby byly nepřístupné pro obvyklý tok položek.<br /><br /> **POZNÁMKA:** Na rozdíl od všech ostatních typů přihrádek nemá typ přihrádky **KVAL** ve výchozím nastavení zaškrtávací políčka pro manipulaci se zbožím. To znamená, že veškerý obsah, který umístíte do přihrádky KVAL, je z toků zboží vyloučen.|  

## <a name="see-also"></a>Viz také
[Správa skladů](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)     
[Správa montáže](assembly-assemble-items.md)    
[Podrobnosti návrhu: Správa skladů](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
