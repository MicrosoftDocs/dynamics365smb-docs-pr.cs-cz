---
    title: Set Up Directed Put-away and Pick | Microsoft Docs
    description: When you set up a warehouse location for directed put-away and pick, you have new functionality available to you to help run the warehouse in the most efficient way possible.
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
# Nastavení zboží a lokací pro přímé zaskladnění a vyskladnění
Když nastavíte lokaci pro řízené zaskladnění a vyskladnění, máte k dispozici nové funkce, které vám pomohou spustit sklad co nejefektivnějším způsobem. Chcete-li tuto funkci plně využít, zadejte další informace o zboží, které pak pomohou provést výpočty nezbytné k tomu, aby navrhli nejúčinnější způsoby provádění skladových aktivit. Pro více informací navštivte [Detaily návrhu: Nastavení skladu](design-details-warehouse-setup.md).

## Nastavení zboží pro řízené zaskladnění a vyskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Otevřete kartu zboží, které chcete nastavit pro řízené zaskladnění a vyskladnění.
3. V záložce **Sklad** na kartě lokace, vyplňte políčka, která definují, jak by se mělo se zbožím v rámci skladu manipulovat.
4. Vyberte tlačítko **Měrné jednotky**.
5. Na stránce **Měrné jednotky zboží**, vyplněním polí definujte různé měrné jednotky, ve kterých může být zboží zpracováváno, včetně výšky, šířky, délky, objemu a hmotnosti pro měrnou jednotku.
6. Vyberte tlačítko **Obsah přihrádky**.
7. Na stránce **Obsah přihrádky**, definujte lokaci a přihrádku, ke které by mělo být zboží přiřazeno. Políčko **Výchozí** se nepoužívá, pokud je na lokaci nastaveno řízené zaskladněni a vyskladnění.

## Aktivace řízeného zaskladnění a vyskladnění
Řízené zaskladnění a vyskladnění umožňuje přístup k rozšířeným funkcím konfigurace skladu, které mohou výrazně zvýšit efektivitu a spolehlivost dat. Abyste mohli tuto funkci využívat, musíte nejprve nastavit několik parametrů ve vašem skladu.

Chcete-li použít funkci řízeného zaskladnění a vyskladnění, musíte aktivovat funkčnost na kartě lokace.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Vyberte lokaci, kde chcete použít řízené zaskladnění a vyskladnění, a pak zvolte tlačítko **Úpravy**
3. V záložce **Sklad** vyberte políčka **Řízené vyskladnění a zaskladnění**.

Na kartě lokace není nutné vyplňovat žádná další pole, dokud nebude potřeba dalšího nastavení.

> [!NOTE]
> Nemůžete nastavit na skladě použití přihrádek, pokud má sklad otevřené položky.

Dalším krokem je definování typu přihrádek, které chcete používat. Pro více informací navštivte <x3/>Nastavení typu přihrádky<x4/>. Typ přihrádky určuje způsob použití dané přihrádky při zpracování toku zboží ve skladu. Typ přihrádky můžete přiřadit zóně i přihrádce.

Můžete také definovat kódy tříd skladu, pokud sklad přepravuje zboží, které potřebuje různé skladovací podmínky. Kódy tříd skladu se používají při navrhování umístění zboží v přihrádkách. Kódy tříd skladu přiřadíte skupinám produktů, které jsou poté přiřazeny zboží, skladovým jednotkám nebo zónám a přihrádkám, které mohou vyhovovat podmínkám skladování vyžadovaným kódy tříd skladu.

Nyní jste připraveni nastavit zóny, pokud je chcete provozovat ve skladu. Použití zón snižuje počet polí, která je třeba vyplnit při nastavování přihrádek, protože přihrádky vytvořené v rámci zón dědí z této zóny několik vlastností. Zóny mohou také usnadnit novým nebo dočasným zaměstnancům orientaci ve vašem skladu. Všimněte si, že tok je řízen přihrádkami, proto je možné pracovat s přihrádkami a pouze s jednou zónou.

## Nastavení zóny ve skladu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Vyberte lokaci, kde chcete nastavit zónu, a otevřete kartu lokace a pak zvolte tlačítko **Zóny**.
3. Na kartě **Zóny**, vyplňte potřebná políčka. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Když změníte parametr zóny, všechny přihrádky vytvořené v této zóně budou mít nové vlastnosti, ale původní přihrádky nebudou změněny.

> [!NOTE]
> Pokud chcete pracovat bez zón, musíte vytvořit jednu zóny, která bude nenadefinovaná, tedy kromě kód zóny.

Dalším krokem při nastavení skladu je definování přihrádek. Pro více informací navštivte [Nastavení lokací pro použití přihrádek](warehouse-how-to-set-up-locations-to-use-bins.md).

Dále je nutné vytvořit šablony zaskladnění a období inventury. Pro více informací navštivte [Nastavení šablon zaskladnění](warehouse-how-to-set-up-put-away-templates.md).

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
