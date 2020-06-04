---
    title: How to Set Up Put-away Templates | Microsoft Docs
    description: With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.
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
# Nastavení šablon zaskladnění
Při funkci řízeného zaskladnění a vyskladnění se navrhne nejvhodnější přihrádka pro vaše zboží v kterémkoli daném okamžiku podle šablony zaskladnění, kterou jste pro sklad nastavili, pořadí přihrádek, které jste přihrádkám dali, a minimální a maximální množství, které jste nastavili pro pevné přihrádky.

Můžete nastavit počet šablon zaskladnění a vybrat jednu z nich, která bude řídit zaskladnění ve vašem skladu. Můžete také vybrat šablonu zaskladnění pro jakoukoliv položku nebo skladovou jednotku, která může mít zvláštní požadavky zaskladnění.

## Nastavení šablon zaskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony zaskladnění** a poté vyberte související odkaz.
2. Vyberte tlačítko **Nový**.
3. Zadejte kód, který je jedinečným identifikátorem šablony, kterou se chystáte vytvořit.
4. Zadejte krátký popis, pokud chcete.
5. Vyplňte první řádek požadavků přihrádky, které chcete splnit v jako první při navrhování zaskladnění.
6. Do druhého řádku zadejte požadavky na přihrádku, které jsou vaší druhou volbou při hledání přihrádky pro zaskladnění. Druhý řádek se použije pouze v případě, že nelze najít přihrádku, která splňuje požadavky prvního řádku.
7. Pokračujte v vyplňování řádků, dokud nevyplníte všechna přijatelná umístění přihrádky, které chcete v procesu zaskladnění použít.
8. Na posledním řádku šablony zaskladnění zaškrtněte políčko **Najít plovoucí přihrádku** .

Můžete vytvořit různé šablony zaskladnění a pak je použít podle svého uvážení. Šablonu zaskladnění, kterou jste vybrali pro zboží nebo skladovou jednotku je použita jako první. Pokud tato pole nejsou vyplněna, použije se šablona zaskladnění, kterou jste vybrali pro sklad v záložce **Použití přihrádek**.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení sprívy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
