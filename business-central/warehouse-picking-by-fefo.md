---
    title: How to Enable Picking by FEFO | Microsoft Docs
    description: First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.
    author: SorenGP

    
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2021
    ms.author: edupont

---
# Povolení vyskladnění pomocí FEFO
First-Expired-First-Out (FEFO) je metoda třídění, která zajišťuje, že se nejdříve vyberou nejstarší položky, které mají nejstarší data vypršení platnosti.

Tato funkce funguje, pouze pokud jsou splněna následující kritéria:

- Zboží musí mít sériové číslo/číslo šarže.
- U zboží nastavením kódu sledování zboží je nutné vybrat pole **Sledovánísériových čísel** nebo **Sledováníčísla šarže**.
- Zboží musí být zaúčtováno do skladu s datem expirace.
- Na kartě lokace musí být zapnuto **Vyždovat vyskladnění**, **Vyskladnění podle FEFO** a **Přihrádka nutná**.

Když jsou splněna všechna kritéria, jsou položky, které mají sériové číslo nebo šarži řazeny od nejstarších ve všech vyskladněních a přesunech zboží,  s výjimkou zboží, které používají sledování specifické pro SN nebo šarže.

> [!NOTE]  
> Pokud některé zboží se sériovým číslem nebo zboží s čísly šarže používají specifické sledování, pak jsou tyto položky respektovány jako první a pod nimi jsou uvedena zbývající nespecifická sériová čísla/čísla šarží podle FEFO.
> <br /><br />
> Pokud má 2 kusy zboží se sériovým číslem nebo číselem šarže stejné datum expirace, pak aplikace vybere položku s nejnižším sériovým číslem nebo číslem šarže.
> <br /><br />
> Při vyskladnění zboží se sériovým číslem nebo číslem šarže v lokacích nastavených pro řízené zaskladnění a vyskladnění se polde FEFO vyskladní zboží pouze na přihrádkách typu *Vyskladnění*.   
> <br /><br />
> Chcete-li povolit pohyby podle FEFO, ponechte pole **Z přihrádky** na stránce **Pohyb zásob** nebo na stránce **Sešity přesunu** prázdné.  
> <br /><br />
> Pokud je na stránce **Kódy sledování zboží** vybráno pole **Přísné účtování expirace**, budou do vyskladnění zahrnuto pouze zboží, které není prošlé a řádky budou seřazeny podle zásady FEFO.

## Viz také
[Vyskladnění zboží](warehouse-pick-items.md)   
[Vyskladnění zboží pro dodávku ze skladu](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Vyskladnění zboží pomocí vyskladnění zásob](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]