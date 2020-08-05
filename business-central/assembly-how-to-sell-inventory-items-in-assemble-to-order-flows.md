---
    title: How to Sell Inventory Items in Assemble-to-Order Flows | Microsoft Docs
    description: If the item is set up for card of assemble-to-order, then the default sales order process assumes that the item is not in inventory and must be assembled for that specific sales order. Therefore, a linked assembly order is automatically created when you add the item to a sales order line.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: kit, kitting
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Prodej skladového zboží podle montáže na zakázku
Pokud pole **Způsob montáže** na kartě zboží montáže obsahuje **Montáž-na-zakázku**, pak výchozí proces prodejní objednávky předpokládá, že zboží není ve skladu a musí být sestaveno pro tuto konkrétní prodejní objednávku. Proto je propojená montážní zakázka automaticky vytvořena při přidání zboží do řádku prodejní objednávky. Pro více informací navštivte [Prodej zboží montáže na zakázku](assembly-how-to-sell-items-assembled-to-order.md). Pokud je však část množství prodejní objednávky již k dispozici ve skladu, můžete snížit množství montážní zakázky změnou pole **Mn.  k montáži na zakázku** na řádku prodejní objednávky.

Tento scénář je vzácný, protože se očekává, že zboží montáže na zakázku bude vždy přizpůsobeno a pravděpodobnost, že toto zboží je ve skladu v konfiguraci, kterou požaduje jiný zákazník, je nízká. Pokud však společnost z důvodu vrácení nebo zrušení objednávky sestaví množství na zakázku, mělo by být toto množství vyzvednuto a prodáno před sestavením nového.

> [!NOTE]
> Na prodejních objednávkách neexistuje žádná funkce, která automaticky upozorní nebo pomůže odečíst množství objednávek, které jsou již k dispozici. Místo toho je nutné sledovat informace o dostupnosti, například na záložce **Detaily prodejního řádku**.

Podobná funkčnost je k dispozici, pokud prodáváte zboží montáže ze zásob a část nebo celé množství není k dispozici a může být dodáno prostřednictvím montážní zakázky. Pro více informací navštivte [Prodej zboží montáže na zakázku a skladového zboží dohromady](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]
> Určitá pravidla se vztahují na pole **K  dodání** na řádcích prodejní objednávky, které obsahují kombinaci množství montáže na zakázku a množství zásob. Pro více informací navštivte sekci Kombinované scénáře v [Princip montáže na zakázku a montáže na sklad](assembly-assemble-to-order-or-assemble-to-stock.md).

V tomto postupu nahradíte množství sestavení na zakázku množstvím zásob na řádku prodejní objednávky. Mezi tyto kroky patří zjištění, že dostupnost existuje. Můžete pozorovat odečtení tohoto množství z propojené montážní zakázky a následné rezervace množství zásob, abyste se ujistili, že je toto množství vyskladněno a dodáno pro objednávku.

## Prodej skladového zboží podle montáže na zakázku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Vytvořte prodejní objednávku. Pro více informací navštivte [Prodej produktů](sales-how-sell-products.md).
3. Na řádku prodejní objednávky pro zboží montáže na zakázu zadejte do pole **Množství** požadované množství.
4. Na záložce **Detaily prodejního řádku** určete, zda je k dispozici celé požadované množství nebo některé z požadovaných množství.
5. Do pole **Mn.  k montáži na zakázku** odečtěte dostupné množství tak, aby bylo k objednávce sestaveno pouze nedostupné množství. Pole **Rezervované množství** je odpovídajícím způsobem sníženo, aby se zohlednilo, že propojení zakázka-na-zakázku nebo rezervace se vztahuje pouze na množství, které má být sestaveno.
6. Na záložce **Řádky** vyberte **Funkce** a poté vyberte akci **Rezervovat**.
7. Na stránce **Rezervace** vyberte řádek nebo žádky položky zboží, které obsahují dostupná množství, zvolte akci **Rezervace z akt.řádku** a pak zvolte tlačítko **OK**.

   Na stránce **Prodejní objednávky** ukazuje pole **Rezervované množství**, že je rezervováno celé množství řádku objednávky. Pole **Mn.  k montáži na zakázku** stále odráží dílčí množství, které musí být sestaveno.

8. Uvolněte prodejní objednávky pro výdej skladového zboží a pro sestavení nedostupných položek. Pro více informací navštivte [Montáž zboží](assembly-how-to-assemble-items.md).

> [!CAUTION]
> Pole **Kód přihrádky** na prodejní objednávce může být předvyplněno podle pole **Kód dod. přihr. montáže-na-zák.** nebo podle pole **Kód přihrádky z montáže** na kartě lokace. V takovém případě může být pole **Kód přihrádky** na řádku prodejní objednávky nesprávné, při této kombinaci množství montáže na zakázku a montáže na sklad. Je vhodné podívat se do pole **Kód přihrádky** a zajistit, aby lokace fungovala pro všechna množství. Případně zadejte dvě různá množství na samostatných řádcích prodejní objednávky.

## Viz také
[Správa montáže](assembly-assemble-items.md)  
[Rezervovace zboží](inventory-how-to-reserve-items.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
