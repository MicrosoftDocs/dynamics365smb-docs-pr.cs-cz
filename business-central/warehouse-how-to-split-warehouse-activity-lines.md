---
    title: How to Split Warehouse Activity Lines | Microsoft Docs
    description: In warehouse put-aways, movements, or picks, and in inventory put-aways and inventory picks, bins are suggested for the picking or putting away of items. The actual quantity in the bin suggested may not be sufficient, or there is not enough room in the suggested bin to put away the required quantity. In these cases, you need to split the line, so that the items for one line are either taken from or placed into more than one bin.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Rozdělení řádků aktivit skladu
Při zaskladnění, přesunech nebo vyskladnění a ve skladových zaskladnění a vyskladnění zásob se přihrádky navrhují pro vyskladnění nebo zaskladnění zboží. Skutečné množství v navrhované přihrádce nemusí být dostatečné nebo v navrhované přihrádce není dostatek místa pro zaskladnění požadovaného množství. V těchto případech je třeba řádek rozdělit, aby bylyo zboží pro jeden řádek odebráno nebo umístěno do více než jedné přihrádky.

Následující postup platí pro doklady skladu, jako je zaskladnění, přesun a řádky vyskladnění nebo řádky zaskladnění zásob, přesun a vyskladnění.

## Rozdělení řádků aktivit skladu
1. Otevřete řádek aktivity skladu, kde se pokoušíte zpracovat nedostatečné množství.
2. V poli **Množ. ke zprac.** zadejte snížené množství, které jste schopni zpracovat.
3. Na záložce **Řádky** vyberte akci **Akce**, poté vyberte akci **Funkce** a pak vyberte akci **Rozdělit řádek**. Zobrazí se nový řádek, který je kopií původního řádku, kromě toho, že pole **Množ. ke zprac.** obsahuje množství, které jste odebrali z původního řádku.
4. Přiřaďte tomuto novému řádku příslušnou přihrádku, pokud používáte zónu řízeného zaskladnění a vyskladnění, nebo pokračujte v rozdělování řádku podle potřeby, dokud nenajdete vhodné přihrádky pro celé množství.

> [!NOTE]  
> Pokud lokace používá řízené zaskladnění a vyskladnění a rozdělujete řádky, musíte být obeznámeni a mít možnost vybrat si přihrádku, která odpovídá požadavkům na skladování zboží a splňuje obecné požadavky dokladu skladu. Například byste nerozdělili řádek na dokladu vyskladnění a neuložili by jste některé položky do hromadného úložiště.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)    
[Zásoby](inventory-manage-inventory.md)    
[Nastavení správy skladu](warehouse-setup-warehouse.md)       
[Správa montáže](assembly-assemble-items.md)      
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]