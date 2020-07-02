---
    title: How to Enable Picking by FEFO | Microsoft Docs
    description: First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2019
    ms.author: sgroespe

---
# Povolení vyskladnění pomocí FEFO
First-Expired-First-Out (FEFO - První expiruje, první ven) je metoda třídění, která zajišťuje, že se nejdříve vyberou nejstarší položky, které mají nejstarší data vypršení platnosti.

Tato funkce funguje, pouze pokud jsou splněna následující kritéria:

- Zboží musí mít sériové číslo/číslo šarže.
- U zboží nastavením kódu sledování zboží je nutné vybrat pole **sledování skladu specifické pro s.č.** nebo **Sledování skladu specifické pro šarži**.
- Zboží musí být zaúčtováno do skladu s datem expirace.
- Na kartě lokace musí být zaškrtnuté políčko **Vyžadovat vyskladnění**.
- Na kartě lokace musí být zaškrtnuté políčko **Vyskladnění podle metody FEFO**.
- Na kartě umístění musí být zaškrtnuto políčko **Přihrádka nutná**.

Když jsou splněna všechna kritéria, jsou položky, které mají sériové číslo nebo šarži řazeny od nejstarších ve všech vyskladněních a přesunech zboží,  s výjimkou zboží, které používají sledování specifické pro SN nebo šarže.

> [!NOTE]
> Pokud některé zboží se sériovým číslem nebo číslem šarže používá specifické sledování, jsou pak nejprve respektovány a pod nimi jsou zbývající, nespecifická, sériová čísla nebo šarže uvedena podle FEFO..
<br /><br />
Pokud dvě zboží se sériovým číslem / číslem šarže mají stejné datum exspirace, program vybere zboží s nejnižší sériovým číslem nebo číslem šarže.
<br /><br />
Při vyskladnění zboží se sériovým číslem nebo číslem šarží v lokacích nastavených pro řízené zaskladnění a vyskladnění se podle FEFO počítá pouze množství na přihrádkách typu *Vyskladnění*.
<br /><br />
Pro povolení pohybů dle FEFO, musíte nechat volné políčko **Z přihrádky** buďto na **Přesunech** a nebo na **Sešitu přesunu**.
<br /><br />
Pokud je pole **Přísné účtování expirace** vybrané, bude do výběru zahrnuto pouze zboží, jehož platnost vypršela. To platí, i když nepoužíváte vyskladnění podle FEFO.

## Viz také
[Vyskladnění zboží](warehouse-pick-items.md)  
[Vyskladnění zboží pro dodávku ze skladu](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Vyskladnění zboží pomocí vyskladnění zásob](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
