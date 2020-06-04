---
    title: How to Set Up Warehouse Employees | Microsoft Docs
    description: Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.
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
# Nastavení zaměstnanců skladu
Každý uživatel, který provádí aktivity skladu, musí být nastaven jako zaměstnanec skladu a přiřazený k jedné výchozí lokaci, potenciálně více nevýchozím lokacím. Toto uživatelské nastavení filtruje všechny aktivity skladu v databázi do místa zaměstnance, takže zaměstnanec může provádět pouze aktivity skladu ve výchozím umístění. Uživatele lze přiřadit k dalším nevýchozím lokacím, pro které může zaměstnanec zobrazit řádky aktivit, ale neprovádět aktivity.

## Nastavení zaměstnanců skladu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaměstnanci skladu** a poté vyberte související odkaz.
2. Vyberte tlačítko **Nový**.
3. Vyberte pole **ID Uživatele** a pak vyberte uživatele, který má být přidán jako zaměstnanec skladu. Klikněte na tlačítko **OK**.
6. V poli **Kód lokace** vyberte, kde bude uživatel pracovat.
7. Zaškrtněte políčko **Výchozí** a definujte místo jako jediné místo, kde zaměstnanec může provádět skladové činnosti.
8. Tyto kroky opakujte pro přiřazení dalších zaměstnanců k umístěním nebo přiřazení jiných než výchozích umístění k existujícím zaměstnancům skladu.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení sprívy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
