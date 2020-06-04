---
    title: How to Set Up Locations to Use Bins | Microsoft Docs
    description: Bins represent the basic warehouse structure and are used to make suggestions about the placement of items. When you have created your bins, you can define very specifically the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.
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
# Nastavení lokací pro použití přihrádek
Přihrádky představují základní skladovou strukturu a používají se k navrhování umístění zboží. Pokud jste vytvořili své přihrádky, můžete velmi přesně definovat obsah, který chcete umístit do každé přihrádky, nebo přihrádka může fungovat jako plovoucí přihrádka bez zadaného obsahu.

Chcete-li použít funkci přihrádky v lokaci, aktivujte nejprve funkčnost na **kartě lokace**. Pak navrhnete tok zboží v lokaci určením kódů přihrádek v polích nastavení, které představují různé toky.

> [!NOTE]
> Předtím než nastavníte kódy přihrádek na kartě lokace, musí být již přihrádky vytvořeny. Pro více informací navštivte [Vytvoření přihrádek](warehouse-how-to-create-individual-bins.md).

## Nastavení lokace pro použití přihrádek
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Vyberte lokaci, kde chcete používat přihrádky.
3. Vyberte tlačítko **Úpravy**.
4. V záložce **Sklad**, vyberte políčko **Přihrádka nutná**.
5. Pokud pro lokaci nepoužíváte řízené zaskladnění a vyskladnění, vyplňte pole **Volba výchozí přihrádky**, kterou by měl systém použít při přiřazování výchozí přihrádky ke zboží.
6. Otevřete kartu lokace, pro kterou chcete vytvořit přihrádky.
7. V **záložce** s náhledem přihrádky vyberte přihrádky, které chcete použít jako výchozí pro příjemky, dodávky, dále pro vstupní, výstupní a  otevřené přihrádky dílny.
8. Kódy přihrádek, které zde vyplníte se automaticky zobrazí v hlavičkách a řádcích různých skladových dokladů. Výchozí přihrádky definují všechna počáteční a koncová umístění zboží ve skladu.
9. Pokud používáte řízené zaskladnění a vyskladnění, vyberte přihrádku pro adjustaci skladu. Kód přihrádky v poli **Kód adjustační přihrádky ** určuje virtuální přihrádku, do níž se zaznamenávají nesrovnalosti v zásobách, když evidujete zjištěné rozdíly zaznamenané v deníku zboží skladu nebo rozdíly vypočtené při evidenci fyzické inventury skladu.
10. Vyplňte políčka v záložce **Použití přihrádek** pokud jsou pro váš sklad relevantní Nejdůležitější políčka jsou **Použití kapacity přihrádky**, **Povolit rozbalení** a **Šablony zaskladnění**.
11. V záložce **Sklad**, vyplňte políčka **Doba  vyskladnění**, **Doba  zaskladnění** a **Kód základního kalendáře**. Pro více informací navštivte sekci [Nastavení základního kalendáře](across-how-to-assign-base-calendars.md).

## Plnění spotřební přihrádky 
Tento vývojový diagram ukazuje, jak **Kód přihrádky** je na řádcích komponenty výrobní zakázky plněn podle nastavení lokace.

![Vývojový diagram toku přihrádky](media/binflow.png "BinFlow")

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení sprívy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
