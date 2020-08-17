---
    title: Sell Assemble-to-Order Items and Inventory Items Together | Microsoft Docs
    description: If an assembly item is set up for assemble-to-stock, then the default sales order process assumes that the item is already assembled and can be picked from inventory, if it is available. But if a part (or all) of the quantity is not available, then you have the flexibility to create an assembly order for the remaining quantity on the fly.
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
# Prodej zboží montáže na zakázku a skladového zboží dohromady
Pokud pole **Způsob montáže**  na kartě zboží montáže obsahuje **Montáž-na-sklad**, pak výchozí proces prodejní objednávky předpokládá, že zboží je již sestaveno a může být vyskladněno ze skladu, pokud je k dispozici. Proto není automaticky vytvořena žádná montážní zakázka, která je propojena s řádkem prodejní objednávky. Pokud však není k dispozici součást (nebo celé) množství, máte možnost vytvořit montážní zakázku pro zbývající množství vyplněním pole **Mn.  k montáži na zakázku** na řádku prodejní objednávky. Tímto způsobem můžete sestavit zboží na zakázku, i když je ve výchozím nastavení nastaveno tak, aby bylo sestaveno na sklad.

Podobná flexibilita existuje při prodeji zboží, které má být sestaveno na zakázku, kde část množství, kterou chcete odečíst z montážní zakázky, je už ve skladu. Pro více informací navštivte [Prodej skladového zboží podle montáže na zakázku](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

> [!NOTE]
> Určitá pravidla se vztahují na pole **K  dodání** na řádcích prodejní objednávky, které obsahují kombinaci množství montáže na zakázku a množství zásob. Pro více informací navštivte sekci Kombinované scénáře v [Princip montáže na zakázku a montáže na sklad](assembly-assemble-to-order-or-assemble-to-stock.md).

> [!NOTE]
> Následující postup nezahrnuje standardní kroky prodejní objednávky, které je třeba provést před vytvořením montážní objednávky pro nedostupná množství.

## Prodej zboží montáže na zakázku a skladového zboží společně
1. Na řádku prodejní objednávky pro zboží, které je nastaveno tak, aby bylo sestaveno na sklad, zadejte množství do pole **Množství**, které přesahuje zásoby. Zobrazí se stránka **Kontrola dostupnosti**. Pro více informací navštivte [Zobrazení dostupnosti zboží](inventory-how-availability-overview.md).
2. Všimněte si pole **Celkové množství** (záporná hodnota), které zadáte v dalším kroku.
3. Do pole **Mn.  k montáži na zakázku** zadejte hodnotu z předchozího kroku.
4. Proveďte jakékoli změny s komponenty montáže. Pro více informací navštivte [Prodej zboží montáže na zakázku](assembly-how-to-sell-items-assembled-to-order.md).
5. Pokračujte uvolněním prodejní objednávky, přípravou na výdej skladového zboží a sestavením nedostupného zboží. Pro další informace o těchto standardních montážních krocích navštivte [Montáž zboží](assembly-how-to-assemble-items.md).

> [!CAUTION]
> Pole **Kód přihrádky** na prodejní objednávce může být předvyplněno podle pole **Kód dod. přihr. montáže-na-zák** nebo podle pole **Kód přihrádky z montáže** na kartě lokace. V takovém případě může být pole **Kód přihrádky** na řádku prodejní objednávky nesprávné, při této kombinaci množství montáže na zakázku a montáže na sklad. Je vhodné zkontrolovat pole **Kód přihrádky** a ujistěte se, že lokace funguje pro všechna množství. Případně zadejte dvě různá množství na samostatných řádcích prodejní objednávky.

## Viz také
[Správa montáže](assembly-assemble-items.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
