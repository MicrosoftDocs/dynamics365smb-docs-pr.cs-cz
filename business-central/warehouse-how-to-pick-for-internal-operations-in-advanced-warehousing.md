---
    title: How to Pick for Internal Operations in Advanced Warehouse Configurations | Microsoft Docs
    description: In advanced warehouse configurations where the location is set up to use picking as well as shipping, you can pick components for production and assembly activities with the **Warehouse Pick** page.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Vyskladnění pro výrobu nebo montáž v rozšířených konfiguracích skladu
V pokročilých konfiguracích skladu, kde je lokace nastavena na použití vyskladnění i dodání, můžete vyskladnit komponenty pro výrobní a montážní aktivity pomocí stránky **Vyskladnění**.

Případně můžete použít stránku **Sešit přesunu** k ad hoc přesunu zboží mezi přihrádky, což znamená bez odkazu na původní dokument. Pro více informací navštivte [Přesouvání zboží v rozšířených konfiguracích skladu](warehouse-how-to-move-items-in-advanced-warehousing.md).

Informace o vyskladnění zboží pro interní operace v základních lokacích skladu, které jsou nastaveny pouze pro vyskladnění, naleznete v tématu [Přesouvání komponent do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Doklad vyskladnění nelze vytvořit od začátku, protože aktivita vyskladnění je vždy součástí workflow, a to buď ve vyžádaném nebo nabízeném scénáři.

Doklad vyskladnění můžete vytvořit výběrem možnosti **Vytvořit  vyskladnění** v původním dokladu, například vydané montážní objednávky nebo dodávky ze skladu. Pro více informací navštivte [Vyskladnění zboží](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Případně můžete vytvořit doklad vyskladnění tažným způsobem pomocí stránky **Sešit vyskladnění** ke zjištění požadavků vyskladnění, a to jak pro dodávku, tak pro interní operace, a pak vytvořit požadované doklady vyskladnění.

Následující postup vysvětluje scénář, kdy vyskladníte komponenty pro vydanou výrobní zakázku pomocí stránky **Sešit vyskladnění**. Postup platí také pro montážní zakázku.

Chcete-li vytvořit požadavky na vyskladnění, a to jak pro vyžádaný nebo nabízený scénář, musí být vydány dotyčné původní doklady. Vydejte původní doklady pro interní operace následujícími způsoby.

| Původní doklad | Metoda vydání |
|---------------------|--------------------|  
| Výrobní zakázka | Změňte typ objednávky na vydanou výrobní zakázku. |
| Montážní zakázka | Změňte stav na Vydáno. |

## Vyskladnění komponent pomocí sešitu vyskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit vyskladnění** a poté vyberte související odkaz.
2. Vyberte akci **Kopie dokladů skladu** a pak vyberte řádky komponenty z vydané výrobní zakázky.
3. Zkontrolujte řádky, seřaďte je, abyste zajistili efektivní zaokrouhlení vyskladnění, a v případě potřeby je zkombinujte s jinými řádky sešitu, abyste co nejlépe využili čas zaměstnance.
4. Vyberte akci **Vytvořit vyskladnění**.
5. Definujte způsob vytvoření dokladů vyskladnění a způsob řazení řádků vyskladnění vyplněním polí na stránce **Vytvořit vyskladnění**.
6. Vyberte tlačítko **OK**. Doklady vyskladnění jsou vytvořeny s řádky vyskladnění pro každou komponentu, která je požadována v interní operaci.

Pokud je interní provozní oblast, například výrobní dílna, nastavena s výchozí přihrádkou pro umístění komponent, které mají být použity v operaci, pak je tento kód přihrádky vložen do řádků Vložit na dokladu vyskladnění, aby bylo možné dát pracovníkům skladu pokyn, kam mají zboží umístit. Pro více informací navštivte pole **Kód přihrádky do výroby** nebo **Kód přihrádky na montáž**.

## Naplnění přihrádky spotřeby
Tento vývojový diagram ukazuje, jak je pole **Kód přihrádky** na řádcích komponent výrobní zakázky vyplněno podle nastavení lokace.

![Vývojový diagram přihrádky](media/binflow.png "BinFlow")

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
