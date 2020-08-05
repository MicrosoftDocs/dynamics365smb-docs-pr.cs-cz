---
    title: How to Create Blanket Assembly Orders | Microsoft Docs
    description: Create blanket sales orders for customized assembly items before periodically making the actual sales orders according to the blanket order agreement.
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
# Vytvoření hromadné montážní zakázky
V průběhu procesu prodeje můžete pomocí správy montáže přizpůsobit zboží montáže požadavku zákazníka. Pro více informací navštivte [Prodej zboží montáže na zakázku](assembly-how-to-sell-items-assembled-to-order.md).

Stejně jako u jiných typů zboží můžete také vytvořit hromadné prodejní objednávky pro přizpůsobené zboží montáže před pravidelným prováděním skutečných prodejních objednávek podle smlouvy o hromadné objednávce. Tento proces zahrnuje několik dalších kroků při porovnání s vytvořením běžné hromadné prodejní objednávky a používá variantu propojené montážní zakázky, což je hromadná montážní zakázka.

> [!NOTE]
> Stejně jako u všech hromadních objednávek jsou množství u hromadních montážních zakázek pouze předpovědi a nejsou funkční, dokud nejsou převedeny na skutečné montážní zakázky. Proto funkce objednávek, jako je výpočet dostupnosti, rezervace a sledování zboží, není u hromadních montážních zakázek aktivní.

## Vytvoření hromadné montážní zakázky pro zboží montáže na zakázku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Hromadné prodejní objednávky** a poté vyberte související odkaz.
2. Vytvořte novou hromadnou prodejní objednávku s jedním řádkem pro zboží montáže. Pro více informací navštivte [Vytvoření hromadných prodejních objednávek](sales-how-to-create-blanket-sales-orders.md).
3. Do pole **Mn.  k montáži na zakázku** na řádku hromadné montážní zakázky zadejte celé množství.

   > [!NOTE]
   > Neměli byste vytvářet smlouvy o hromadných objednávkách pro částečné množství. Proto musíte zadat stejné množství, jaké jste zadali do pole **Množství** na řádku hromadné prodejní objednávky.

4. Vyberte akci **Montáž na zakázku** a potom vyberte akci **Řádky montáže na zakázku**. Případně vyberte pole **Mn.  k montáži na zakázku** na žádku.
5. Na stránce **Řádky montáže na zakázku** zkontrolujte nebo upravte řádky montážní zakázky podle smlouvy o hromadné objednávce, kterou jste uzavřeli se zákazníkem. Chcete-li zobrazit další informace, zvolte akci **Zobrazit doklad** a otevřete celou hromadní montážní zakázku. Obsah většiny polí nelze změnit a nelze jej zaúčtovat.
6. Pokud jste upravili řádky montážní zakázky podle smlouvy o hromadní objednávce, zavřete stránku **Řádky montáže na zakázku** a vraťte se na stránku **Hromadná prodejní objednávka**.
7. Pokud zákazník požádá o vytvoření prodejní objednávky na základě dohodnuté hromadní prodejní objednávky, vytvořte prodejní objednávku pro dohodnuté montážní zboží. Pro více informací navštivte [Vytvoření hromadných prodejních objednávek](sales-how-to-create-blanket-sales-orders.md).

Propojená hromadní montážní zakázka a veškeré úpravy jsou spojeny s touto novou prodejní objednávkou, aby se připravila na montáž zboží, které má být prodáno.

## Viz také
[Vytvoření hromadných prodejních objednávek](sales-how-to-create-blanket-sales-orders.md)  
[Správa montáže](assembly-assemble-items.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
