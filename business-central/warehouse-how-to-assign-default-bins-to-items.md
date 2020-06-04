---
    title: How to Assign Default Bins to Items | Microsoft Docs
    description: If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier. When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.
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
# Přiřazení výchozí přihrádky ke zboží
Pokud používáte přihrádky v lokaci, přiřazení výchozích přihrádek k vašemu zboží může proces expedice, příjmu a přesunu podstatně zjednodušit. Pokud je ke zboží přiřazena výchozí přihrádka, je tato přihrádka navržena pokaždé, když zahájíte transakci pro toto zboží. Výchozí přihrádky jsou definovány na stránce**Obsah přihrádky** .

## Přiřazení výchozí přihrádky ke zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit vytvoření obsahu přihrádky** a poté vyberte související odkaz.
2. Vyplňte kód přihrádky a informace o zboží pro každou přihrádku, kterou chcete nastavit pro zboží jako výchozí. Ujistěte se, že jste vybrali pole **Výchozí**.
3. Vyberte tlačítko **Vytvořit obsah přihrádky**. Pro zboží jsou nyní přiřazeny výchozí přihrádky.

> [!NOTE]
> Pokud je zboží zaskladněno, a pokud zboží nemá přiřazenou výchozí přihrádku, nastaví se jako výchozí ta, kde je zaskladněno.

## Změna výchozí přihrádky zboží
Pravděpodobně bude nutné změnit přiřazení výchozí přihrádky pro zboží nebo přiřadit výchozí přihrádku novému zboží.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Obsah přihrádky** a poté vyberte související odkaz.
2. V poli **Filtr lokace** vyberte příslušný kód lokace.
3. Najděte aktuální výchozí položku obsahu přihrádky pro zboží a zrušte zaškrtnutí políčka **Výchozí přihrádka** .
4. Najděte řádek s obsahem přihrádky, pro který chcete novou výchozí přihrádku. Zaškrtněte políčko **Výchozí přihrádka**.

> [!NOTE]
> Pokud je zboží zaskladěné poprvé a nemá přiřazenou výchozí přihrádku, systém přiřadí přihrádku, ve které je zboží zaskladněno jako výchozí.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení sprívy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
