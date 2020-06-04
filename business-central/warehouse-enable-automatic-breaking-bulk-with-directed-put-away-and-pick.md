---
    title: Automatic Breaking Bulk with Directed Put-away and Pick | Microsoft Docs
    description: For locations that use directed put-away and pick, you can break a larger unit of measure into smaller units of measure, when it creates warehouse instructions that fulfill the needs of source documents, production orders, or internal picks and put-aways.
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
# Povolení automatického rozdělení zboží s řízeným zaskladněním a vyskladněním
Pro lokace, které používají řízené zaskladnění a vyskladnění, [!INCLUDE[d365fin](includes/d365fin_md.md)] může v různých situacích automaticky rozbalovat, to znamená, rozdělit větší měrnou jednotku na menší měrné jednotky při vytváření skladových úkonů, které splňují potřeby původních dokladů, výrobních zakázek nebo interních vyskladnění a zaskladnění. Rozbalení také znamená shromáždění menších měrných jednotek, je-li to nutné, k uspokojení odchozích požadavků, a to tak, že se větší měrná jednotka ve zdrojovém dokladu nebo výrobní zakázce rozdělí na menší měrné jednotky, které jsou ve skladu k dispozici.

## Rozbalení ve vyskladnění
Pokud chcete skladovat zboží v několika různých měrných jednotkách a umožnit jejich automatické kombinování podle potřeby ve výdejním procesu, vyberte na kartě lokace pole **Povolit rozbalení**.

Pro splnění úkolu program automaticky vyhledá zboží ve stejné měrné jednotce. Pokud však tento formulář zboží nenajde a toto pole je vybráno, program navrhne, abyste do měrné jednotky, která je potřebná, dali větší měrnou jednotku.

Pokud systém může najít pouze menší měrné jednotky, navrhne vám, abyste shromáždili zboží ke splnění množství v dodávce nebo výrobní zakázce. Ve skutečnosti rozdělí větší měrnou jednotku zdrojového dokumentu na menší jednotky pro výdej.

## Rozbalení v zaskladnění
V zaskladnění program automaticky navrhne řádky v měrné jednotce zaskladnění, například kusy, i když zboží dorazí v jiné měrné jednotce.

## Rozbalení v přesunech
Program také automaticky rozbaluje při přesunech doplnění, pokud je vybráno pole **Povolit rozbalení** na záložce **Možnosti** na stránce **Vypočítat doplnění přihrádky**.

Výsledky procesu převodu lze zobrazit z jedné měrné jednotky do jiné jako přechodné řádky rozbalení v pokynech pro zaskladnění, vyskladnění nebo přesun.

> [!NOTE]
> Pokud vyberete pole **Nastavit filtr rozbalení** v záhlaví instrukce skladu, program skryje řádky rozbalení, kdykoli bude celá měrná jednotka zcela použita. Pokud je například je na paletě 12 kusů a vy použijete všech 12 kusů, vyskladnění bude brát jednu paletu a umístí 12 kusů. Pokud však potřebujete vybrat pouze 9 kusů, řádky rozbalení nebudou skryty ani v případě, že jste vybrali pole **Filtr rozbalení ** , protože zbývající tři kusy je třeba umístit do skladu.

> [!NOTE]
> Pokud chcete, aby vaše měrné jednotky fungovaly optimálně ve skladu, také ve spojení s funkcemi rozbalení, měli byste se pokusit:
> - Nastavte základní měrnou jednotku pro zboží jako nejmenší měrnou jednotku, kterou očekáváte ve vašich skladových procesech.
> - Nastavte alternativní měrné jednotky pro zboží jako násobky základní měrné jednotky.


## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
