---
    title: How to Quote an Assemble-to-Order Sale | Microsoft Docs
    description: You can use assembly management to customize an assembly item to a customer’s request during the sales process.
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
# Nabídka prodeje montáže na zakázku
V průběhu procesu prodeje můžete pomocí správy montáže přizpůsobit zboží montáže požadavku zákazníka. Pro více informací navštivte [Prodej zboží montáže na zakázku](assembly-how-to-sell-items-assembled-to-order.md).

Stejně jako při prodeji jiného typu zboží můžete také vytvořit prodejní nabídku pro přizpůsobené zboží montáže před převodem na prodejní objednávku. Tento proces zahrnuje několik dalších kroků při porovnání s vytvořením pravidelné prodejní nabídky a používá variantu propojené montážní zakázky, což je montážní nabídka.

> [!NOTE]
> Stejně jako u všech typů nabídek se množství v montážní nabídce nepoužívá v dostupnosti, plánování nebo rezervaci.

## Vytvoření prodejní nabídky pro zboží montáže na zakázku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní nabídka** a poté vyberte související odkaz.
2. Vytvořte řádek prodejní nabídky s jedním řádkem pro montážní zboží. Pro více informací navštivte [Vytvoření prodejní nabídky](sales-how-make-offers.md).
3. Do pole **Mn.  k montáži na zakázku** zadejte celé množství.

   > [!NOTE]
   > Neměli byste uvádět částečné množství. Proto musíte zadat stejné množství, které jste zadali do pole **Množství** na řádku prodejní nabídky.

4. Na záložce **Řádky** zvolte **Řádek** pak **Montáž na zakázku** a pak vyberte **Řádky montáže na zakázku**. Případně zvolte pole **Mn.  k montáži na zakázku** na řádku.
5. Na stránce **Řádky montáže na zakázku** zkontrolujte nebo upravte řádky montážní zakázky podle nabídky, kterou zákazník požaduje. Chcete-li zobrazit další informace, vyberte akci **Zobrazit doklad** a otevřete tak celou objednávku hromadné nabídky. Obsah většiny polí nelze změnit a nelze jej zaúčtovat.
6. Pokud jste upravili řádky montážní zakázky podle nabídky, zavřete stránku **Řádky montáže na zakázku** a vraťte se na stránku **Prodejní nabídka**.
7. Pokud zákazník nabídku přijme, vytvořte prodejní objednávku pro nabízené montážní zboží. Pro více informací navštivte [Vytvoření prodejní nabídky](sales-how-make-offers.md). Propojená montážní nabídka a všechna vlastní nastavení jsou propojena s novou prodejní objednávkou, aby se připravila na montáž zboží, které má být prodáno.

## Viz také
[Správa montáže](assembly-assemble-items.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
