---
    title: Design Details - Integration with Inventory | Microsoft Docs
    description: The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.
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
# Detaily návrhu: Integrace zásob
Oblast aplikace Správa skladu a Zásob vzájemně komunikují pomocí fyzických inventur a v úpravách zásob nebo skladu.

## Fyzická inventura
Stránka **Whse. Phys. Inventory Journal** je použita se stránkou **Phys. Inventory Journal** pro všechna umístění ve skladu. Zásoby na úrovni přihrádky se vypočítají a pro zaměstnance skladu je následně k dispozici vytištěný seznam. Seznam ukazuje, v které přihrádce musí být zboží spočítáno.

Zaměstnanec skladu zadá spočítané množství na stránce **Whse. Phys. Inventory Journal** a poté zaúčtuje deník.

Pokud je napočítané množství větší než množství na řádku deníku, bude pro tento rozdíl zaúčtován jako přesun z adjustační přihrádky do právě počítané přihrádky. Tím se zvýší množství v počítané přihrádce a sníží se množství v adjustační přihráce.

Pokud je počítané množství menší než množství na řádku deníku, přesun tohoto rozdílu se zaúčtuje z počítané přihrádky do adjustační přihrádky. Tím se sníží množství v počítané přihrádce a zvýší se množství ve výchozí adjustační přihrádce.

V pokročilých konfiguracích skladu je hodnota v poli **Množství (Vypočítané)** načtena z položek zboží a hodnota **Množství (fyz. inventura)** je načteno z položek skladu, s výjimkou obsahu adjustační přihrádky. Políčko **Množství** určuje rozdíl mezi prvními dvěma poli, který by se měl rovnat obsahu adjustační přihrádky.

Při zaúčtování deníku fyzické inventury se aktualizují zásoby a výchozí adjustační přihrádka.

### Úpravy skladu v položkách zboží
Použijte stránku **Deníky zboží** a funkci **Výpočet adjustace skladu** pro úpravu zásob v požkách zboží v souladu s úpravou, která byla provedena u množství zboží v přihrádce skladu. Chcete-li vytvořit propojení mezi zásobami a skladem, musíte definovat výchozí adjustační přihrádku daného skladu.

Výchozí adjustační přihrádka eviduje zboží ve skladu při zaúčtování zvýšení zásob. Pokud však zaúčtujete snížení, sníží se také množství ve výchozí adjustační přihrádce. V obou případech se vytvoří položky zboží a položky skladu.

> [!NOTE]  
> Adjustační přihrádka není započítana do kalkulace dostupnosti.

Chcete-li upravit obsah přihrádky, můžete použít deník zboží skladu, ze kterého můžete zadat číslo zboží, kód zóny, kód přihrádky a množství, které chcete upravit.

Pokud zadáte kladné množství a zaúčtujete řádek, zásoby v přihrádce se zvýší a množství výchozí adjustační přihrádky se odpovídajícím způsobem sníží.

## Viz také
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)   
[Detaily návrhu: Dostupnost ve skladu](design-details-availability-in-the-warehouse.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]