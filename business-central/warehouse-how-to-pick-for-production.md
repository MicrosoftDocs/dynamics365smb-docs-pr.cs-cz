---
    title: How to Pick for Production in Basic Warehouse Configurations | Microsoft Docs
    description: When your warehouse location requires pick processing but does not require shipment processing, use the **Inventory Pick** page to organize and record the picking of components.
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
# Vyskladnění pro výrobu nebo montáž v základních konfiguracích skladu
Způsob zaskladnění komponent pro výrobní nebo montážní zakázky závisí na tom, jak je sklad nastaven pro lokace. Pro více informací navštivte [Nastavení správy skladů](warehouse-setup-warehouse.md).

V základních konfiguracích skladu, kde lokace vyžaduje zpracování vyskladnění, ale ne zpracování dodávky, použijete stránku **Vyskladnění zásob** k uspořádání a zaznamenání vyskladnění komponent.

V základních konfiguracích skladu musíte vyskadnit zboží pro montážní zakázky pomocí stránky **Přesun zásob**. Pro více informací navštivte [Zpracování zboží montáže na objednávku pomocí vyskladnění zásob](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).

V pokročilých konfiguracích skladu, kde lokace vyžadují vyskladnění i dodávky, použijete stránku **Vyskladnění** k uvedení komponent do výrobních nebo montážních zakázek. Pro více informací navštivte [Vyskladnění pro výrobu nebo montáž v pokročilých konfiguracích skladu](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

> [!NOTE]
> Mezi vyskladněním a přesunem zásob existují následující důležité rozdíly:
> - Když zapíšete vyskladnění skladu pro interní operaci, například pro výrobu, bude současně zaúčtována spotřeba vybraných komponent. Při zapsání přesunu zásob pro interní operaci zaznamenáváte pouze fyzický přesun požadovaných komponent do přihrádky v oblasti operace bez zaúčtování spotřeby.
> - Při použití vyskladnění zásob, je pole **Kód přihrádky** na řádku komponenty výrobní zakázky nastaveno jako typ přihrádky *Vzít*, ze které se komponenty při účtování spotřeby sníží. Při použití přesunů zásob, je pole **Kód přihrádky** na řádcích komponent výrobní zakázky nastaveno jako typ přihrádky *Vložit* v operační oblasti, kam musí pracovník skladu umístit komponenty.


Předpokladem systému pro výdej nebo přesunutí komponent pro původní doklady je, že existuje požadavek na výstupní sklad, který upozorňuje oblast skladu na potřebu komponenty. Požadavek na výstupní sklad je vytvořen při každé změně stavu výrobní zakázky na Vydáno nebo při vytvoření vydané výrobní zakázky.

## Vyskladnění komponent v základních konfiguracích skladu
V základních konfiguracích skladu, kde je lokace nastavena tak, aby používala pouze vyskladnění, můžete vyskladnit komponenty pro výrobní aktivity pomocí stránky **Vyskladnění zásob**. Pro více informací navštivte [Vyskladnění zboží pomocí vyskladnění zásob](warehouse-how-to-pick-items-with-inventory-picks.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění zásob** a poté vyberte související odkaz.
2. Chcete-li získat přístup k komponentám výrobní zakázky, zvolte akci **Kopie pův.dokladů** a pak vyberte vydanou výrobní zakázku.
3. Proveďte vyskladnění a zaznamenejte skutečné informace o vyskladnění do pole **Vyskladněné  množství**.
4. Až budou řádky připraveny k zaúčtování, zvolte akci **Účtovat**. Účtování vytvoří potřebné položky skladu a zaúčtuje spotřebu zboží.

Můžete také vytvořit **Vyskladnění zásob** přímo z vydané výrobní zakázky. Vyberte akci **Vytvořit zaskl./vyskl.zásob** zaškrtněte políčko **Vytvořit vyskladnění  zásob** a pak vyberte tlačítko **OK**.

Případně můžete použít stránku **Přesun zásob** k ad hoc přesunu zboží mezi přihrádky, což znamená bez odkazu na původní doklad.
Pro více informací navštivte [Přesouvání komponent do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

### Zpracování zboží montáže na zakázku pomocí vyskladnění zásob
Stránka **Vyskladnění zásob** se také používá k vyskladnění a dodání pro prodej, kde musí být zboží sestaveno před jejich odesláním. Pro více informací navštivte [Prodej zboží montáže na obejdnávku](assembly-how-to-sell-items-assembled-to-order.md).

Zboží, které má být dodáno, není fyzicky přítomno v přihrádce, dokud není sestaveno a zaúčtováno jako výstup do přihrádky v oblasti montáže. To znamená, že vyskladnění zboží montáže na zakázku k odeslání se řídí zvláštním postupem. Z přihrádky pracovníci skladu převezou zboží montáže do dodacího prostoru a poté zaúčtují vyskladnění zásob. Zaúčtovaná vyskladnění zásob pak zaúčtuje výstup sestavy, spotřebu komponenty a prodejní dodávku.

Můžete nastavit [!INCLUDE[d365fin](includes/d365fin_md.md)] pro automatické vytvoření přesunu zásob při vytvoření vyskladnění zásob pro zboží montáže. Chcete-li to povolit, musíte na stránce **Nastavení montáže** vybrat pole **Vytvořit pohyby automaticky**. Pro více informací navštivte [Přesouvání komponent do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Řádky vyskladnění zásob pro prodejní zboží jsou vytvořeny různými způsoby v závislosti na tom, zda žádné, některé nebo všechna množství prodejního řádku jsou smontovány na zakázku.

V běžném prodeji, kde používáte vyskladnění zásob k zaúčtování dodávky množství zásob, je pro každý řádek prodejní objednávky vytvořen jeden řádek vyskladnění zásob nebo několik položek, pokud je zboží umístěno do různých přihrádek. Tento řádek vyskladnění je založen na množství v poli **K  dodání**.

Při montáži na zakázku, kde je na zakázku sestaveno celé množství na objednávce, je pro toto množství vytvořen jeden řádek pro vyskladnění zásob. To znamená, že hodnota v poli Množství k montáži je stejná jako hodnota v poli **K  dodání**. Na řádku je vybráno pole **Montáž na zakázku**.

Pokud je pro lokaci nastaven výstupní tok montáže, pak hodnota v poli **Kód dod. přihr. montáže-na-zák.** nebo hodnota v poli **Kód přihrádky z montáže**  v tomto pořadí je vložena do pole **Kód přihrádky** na řádku vyskladnění zásob.

Pokud na řádku prodejní objednávky není zadán žádný kód přihrádky a pro lokaci není nastaven žádný výstupní tok montáže, je pole **Kód přihrádky** na řádku vyskladnění zásob prázdné. Pracovník skladu musí otevřít stránku **Obsah přihrádky** a vybrat přihrádku, ve které je sestaveno zboží montáže.

V kombinovaných scénářích, kde musí být nejprve sestavena část množství a další musí být vyskladněna ze skladu, jsou vytvořeny minimálně dva řádky vyskladnění zásob. Jeden řádek vyskladnění je pro množství montáže na zakázku. Druhý řádek vyskladnění závisí na tom, které přihrádky mohou vyplnit zbývající množství ze skladu. Kódy přihrádek na dvou řádcích jsou vyplněny různými způsoby, jak je popsáno pro dva různé typy prodeje. Pro více informací navštivte sekci “Kombinované scénáře” v [Princip montáže na zakázku a montáže na sklad](assembly-assemble-to-order-or-assemble-to-stock.md).

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
