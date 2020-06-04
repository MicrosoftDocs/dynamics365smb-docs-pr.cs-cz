---
    title: How to Convert Existing Locations to Warehouse Locations | Microsoft Docs
    description: You can enable an existing inventory location to use zones and bins and to operate as a warehouse location.
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
# Převod existujících lokací na lokace skladu
Existujícímu skladovému místu můžete povolit použití zón a přihrádek a pro provoz jako na skladu.

Dávková úloha, která povolí skladové místo pro skladové operace, vytvoří počáteční stavy skladu pro adjustační přihrádku skladu pro všechno zboží, které mají v lokaci zásoby. Tyto počáteční stavy budou vyrovnané po zadání zboží fyzické inventury skladu po spuštění dávkové úlohy.

Zóny a přihrádky můžete vytvořit před nebo po převodu. Jediná přihrádka, kterou musíte vytvořit před převodem, je ta, která má být použita jako budoucí adjustační přihrádka.

> [!IMPORTANT]
> Chcete-li před převedením umístění pro manipulaci se skladem vymazat všechny záporné zásoby a všechny otevřené skladové doklady, spusťte sestavu a identifikujte položky se zápornými zásobami a otevřené skladové doklady pro dané umístění. Pro více informací navštivte Kontrola záporného stavu zásob.

## Povolení fungování existujícího umístění jako lokace skladu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vytvořit lokaci ve skladu** a poté vyberte související odkaz.
2. V poli **Kód lokace** zadejte umístění, které chcete povolit pro zpracování skladu.
3. Do pole **Kód adjustační přihrádky** zadejte přihrádku v místě, kde jsou uloženy nesynchronizované položky skladu. Pro více informací navštivte [Synchronizace upravených položek skladu se souvisejícími položkami zboží](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries)

   Při použití otevřených položek zboží pro zadané skladové místo jsou vytvořeny řádky deníku skladu, které tvoří součet všech kombinací čísel zboží, kód variant, kód měrné jednotky a v případě potřeby číslo šarže  a sériové číslo  v položkách zboží. Řádky deníku skladu jsou poté zaúčtovány. Toto zaúčtování vytvoří položky skladu, které umístí zásoby do adjustační přihrádky skladu. Nastaví se také **Kód adjustační přihrádky** na kartě lokace.

4. Chcete-li zjistit, které položky byly během dávkové úlohy přidány do adjustační přihrádky, spusťte sestavu **Adjustační přihrádka skladu** .
5. Po dokončení dávkové úlohy **Vytvořit lokaci ve skladu** provedete a zaúčtujete fyzickou inventuru skladu. Pro více informací navštivte [Počítání, adjustace a přeřazení zboží](inventory-how-count-adjust-reclassify.md).

> [!NOTE]
> Doporučujeme spustit dávkovou úlohu **Vytvořit lokaci ve skladu** v době, kdy to neovlivní každodenní práci v systému. Tato úloha zpracuje každou položku v tabulce **Položka zboží** a pokud existuje velký počet položek zboží, může úloha trvat několik hodin.

Pro skladová místa, která před převodem nepoužívaly doklady správy skladu, je nutné znovu otevřít a uvolnit všechny původní doklady, které byly částečně přijaty nebo částečně dodány před převodem.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení sprívy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
