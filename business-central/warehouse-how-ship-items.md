---
    title: How to Ship Items | Microsoft Docs
    description: Depending on your warehouse configuration, you can either record shipment on the related outbound business document, such as a sales order,  directly, or you can use warehouse shipment documents that respect a workflow and integrate to various warehouse activities.
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
# Odesílání zboží
Při odesílání zboží ze skladu, který není nastaven pro zpracování dodávky ze skladu, jednoduše zaznamenáte dodávku do souvisejícího obchodního dokladu, například prodejní objednávky, servisní zakázky, objednávky nákupní vratky nebo výstupní objednávky transferu.

Při odeslání zboží ze skladu, který je nastaven pro zpracování dodávky ze skladu, můžete zboží odeslat pouze na základě původních dokladů, které ostatní jednotky společnosti vydaly do skladu k akci.

> [!NOTE]
> Pokud váš sklad používá překládání a přihrádky, můžete pro každý řádek zobrazit počet zboží, které bylo vloženo do přihrádky přeložení. Aplikace vypočítává tato množství automaticky při každé aktualizaci polí v dodávke. Pokud se jedná o zboží, které se vztahuje k dodávce, kterou připravujete, můžete vytvořit vyskladnění pro všechny řádky a dokončit dodávku. Pro více informací navštivte [Přeložení zboží](warehouse-how-to-cross-dock-items.md).

## Odesílání zboží pomocí prodejní objednávky
Následující text popisuje, jak přijímat zboží s nákupní objednávkou. Kroky jsou podobné pro objednávky nákupní vratky, servisní zakázky a výstupní objednávky transferu.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Otevřete existující prodejní objednávku nebo vytvořte novou. Pro více informací navštivte [Prodej produktů](sales-how-sell-products.md).
3. Do pole **Množ. dodání**, zadejte přijaté množství.

   Hodnota v poli **Dodané  množství** je aktualizována. Pokud se jedná o částečnou dodávku, je hodnota nižší než hodnota v poli **Množství**.
4. Vyberte akci **Účtovat**.

## Odesílání zboží pomocí dodávky ze skladu
Nejprve vytvořte doklad dodávky z původního obchodního dokladu. Poté vyberte zadané zboží pro dodávku.

### Vytvoření dodávky ze skladu
Dodávku ze skladu obvykle vytvoří zaměstnanec odpovědný za expedici zboží.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dodávky ze skladu** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.

   Vyplňte pole na záložce **Obecné**. Při načtení řádků původního dokladu se některé informace zkopírují na každý řádek.

   Pro konfiguraci skladu s řízeným zaskladněním a vyskladněním, pokud má lokace výchozí zónu a přihrádku pro dodávky, jsou pole **Kód zóny** a **Kód přihrádky** vyplněna automaticky, ale můžete je podle potřeby změnit.

   > [!NOTE]
   > Pokud chcete dodávat zboží s jinými kódy třídy skladu, než je kód třídy přihrádky v poli **Kód přihrádky** v hlavičce dokladu, musíte před načtením řádků zdrojového dokladu pro zboží odstranit obsah pole **Kód přihrádky** v hlavičce.
3. Vyberte akci **Kopie pův.dokladů**. Otevře se stránka **Původní doklady**.

   Z nové nebo otevřené dodávky ze skladu můžete použít stránku **Výběr filtru původu skladu** k načtení vydaných řádků původního dokladu, které definují zboží, které má být dodáno.

   1. Vyberte akci **Použít filtry pro kopii pův. dokl.**.
   2. Chcete-li nastavit nový filtr, zadejte do pole **Kód** popisný kód a poté vyberte akci **Upravit**.
   3. Vyplněním příslušných polí filtru určete typ řádků původního dokladu, které chcete načíst.
   4. Vyberte akci **Start**.
   Všechny vydané řádky původního dokladu, které splňují kritéria filtru, jsou nyní vloženy na stránku **Dodávka ze skladu**, ze které jste aktivovali funkci filtru.

   Kombinace filtrů, které definujete, se uloží na stránce **Výběr filtru původu skladu**, dokud je příště nebudete potřebovat. Můžete vytvořit neomezený počet kombinací filtrů. Kritéria můžete kdykoli změnit výběrem akce **Upravit**.

4. Vyberte původní doklady, pro které chcete zboží dodat, a pak zvolte tlačítko **OK**.

Řádky původních dokladů se zobrazí na stránce **Dodávka ze skladu**. Pole **K  dodání** je vyplněno zbývajícím množstvím pro každý řádek, ale toto množství můžete podle potřeby změnit. Pokud jste před získáním řádků odstranili obsah pole **Kód přihrádky** na záložce **Obecné**, musíte vyplnit příslušný kód přihrádky na každém řádku dodávky.

> [!NOTE]
> Nelze odeslat více zboží, než je množství v poli **Zbývající  množ.** na řádku původního dokladu. Chcete-li odeslat více zboží, načtěte jiný původní doklad, který obsahuje řádek pro zboží, pomocí funkce filtru k získání původních dokladů se zbožím.

Pokud máte řádky, které chcete dodat, můžete zahájit proces, který odešle řádky zaměstnancům skladu k vyskladnění.

### Vyskladnění a odesílání
Pracovník ve skladu odpovědný za vyskladnění obvykle vytvoří doklad o vyskladnění nebo otevře již vytvořený doklad o vyskladnění.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dodávky ze skladu** a poté vyberte související odkaz.
2. Vyberte dodávku ze skladu, pro kterou chcete vytvořit vyskladnění a pak zvolte akci **Vytvořit vyskladnění**.
3. Vyplňte pole na stránce požadavku a pak zvolte tlačítko **OK**. Je vytvořen zadaný doklad vyskladnění.

   Případně otevřete existující vyskladnění.
4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění** a poté vyberte související odkaz. Vyberte vyskladnění ze skladu, na kterém chcete pracovat.

   Pokud je sklad nastaven na použití přihrádek, byly řádky vyskladnění převedeny na řádky akce Vzít a Vložit.

   Řádky můžete třídit, přiřadit zaměstnance k vyskladnění, nastavit filtr rozbalení, pokud používáte řízené zaskladnění a vyskladnění, a vytisknout pokyny k vyskladnění.

5. Proveďte skutečné vyskladnění zboží a vložte jej do určené přepravné přihrádky nebo do přepravní oblasti, pokud přihrádky nemáte.
6. Vyberte akci **Zápis vyskladnění**.

   Pole **K  dodání** a **Stav dokladu** v záhlaví dodacího dokladu jsou aktualizovány. Zboží, které jste vyskladnili, již není k dispozici pro výdej pro jiné dodávky nebo pro interní operace.
7. Vytiskněte si přepravní doklady, připravte balíky zásilek a zaúčtujte zásilku.

Pro více informací o vyskladnění u dodávek ze skladu navštivte [Vyskladnění zboží pro dodávku ze skladu](warehouse-how-to-pick-items-for-warehouse-shipment.md).

Sešit vyskladnění můžete také použít k tomu, abyste do jedné instrukce (pro několik dodávek) vytvořili několik pokynů vyskladnění a tím zvýšili efektivitu vyskladnění ze skladu. Pro více informací navštivte [Plánování v sešitech vyskladnění](warehouse-how-to-plan-picks-in-worksheets.md).

> [!NOTE]
> Pokud čekáte na konkrétní zboží, které dorazí do skladu, a používáte funkci přeložení, pak [!INCLUDE[d365fin](includes/d365fin_md.md)] vypočítá pro každou dodávku nebo řádek sešitu vyskladnění množství zboží, které je v přihrádce přeložení. Toto pole se aktualizuje pokaždé, když opustíte a znovu otevřete doklad nebo list dodávky. Pro více informací navštivte [Přeložení zboží](warehouse-how-to-cross-dock-items.md).

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
