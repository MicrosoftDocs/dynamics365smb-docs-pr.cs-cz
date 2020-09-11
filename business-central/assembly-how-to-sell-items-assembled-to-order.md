---
    title: How to Sell Items Assembled to Order | Microsoft Docs
    description: If the item is set up for assemble-to-order, then the item is not expected to be in inventory, and it must be assembled specifically to a sales order. When you enter the item on a sales order line, then an assembly order is automatically created and linked to the sales order.
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
# Prodej zboží montáže na obejdnávku
Pokud je pole **Způsob montáže** na kartě zboží pro zboží montáže nastaveno na **Montáž-na-zakázku**, neočekává se, že by zboží bylo na skladě a musí být sestaveno konkrétně do prodejní objednávky. Když zadáte zboží na řádku prodejní objednávky, pak je automaticky vytvořena montážní zakázka, která je propojena s prodejní objednávkou.

> [!NOTE]
> Pokud je již některé zboží montáže na zakázku v zásobách, můžete si toto množství odečíst z montážní zakázky a rezervovat ho ze zásob. Pro více informací navštivte [Prodej skladového zboží podle montáže na zakázku](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

V tomto postupu zpracováváte prodej zboží, které bude sestaveno podle specifikací požadovaných zákazníkem. Mezi tyto kroky patří zahájení řádku prodejní objednávky, přizpůsobení zboží montáže úpravou jeho komponent a zdrojů, kontrola dostupnosti za účelem stanovení data dodání a uvolnění prodejní objednávky, která má být sestavena a okamžitě dodána.

> [!NOTE]
> Následující postup nezahrnuje standardní kroky prodejní objednávky před krokem, ve kterém zadáte zboží montáže na zakázku na řádku prodejní objednávky.

## Prodej zboží, které je sestaveno na zakázku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Vytvořte prodejní objednávku. Pro více informací navštivte [Prodej produktů](sales-how-sell-products.md).
3. Do pole **Číslo** zadejte zboží, které je nastaveno k sestavení na zakázku.
4. V poli **Kód lokace** definujte, ze které lokace bude zboží prodáno. Proces sestavení proběhne v této lokaci.
5. Do pole **Množství** zadejte, kolik jednotek se má prodat.

   > [!NOTE]
   > Pokud není k dispozici jedna nebo více komponent požadovaného množství zboží montáže, otevře se stránka s podrobnými informacemi o dostupnosti. Pro více informací navštivte Dostupnost montáže.

   Montážní zakázka je nyní automaticky vytvořena a propojena s řádkem prodejní objednávky. Datum splatnosti této montážní zakázky je synchronizován s datem dodávky řádku prodejní objednávky.

   Množství, které se má prodat, se zkopíruje do pole **Mn.  k montáži na zakázku**, což znamená, že nastavení zboží očekává, že celé množství na prodejním řádku bude sestaveno na zakázku. Množství, které můžete sestavit, můžete snížit, například pokud víte, že některé zboží je již k dispozici. Pro více informací navštivte [Prodej skladového zboží podle montáže na zakázku](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

6. Chcete-li uvést, že zákazník chce další zboží v sadě, vyberte na záložce **Řádky** akci **Řádek**, vyberte **Montáž na zakázku** a poté vyberte akci **Řádky montáže na zakázku**, chcete-li zobrazit a změnit standardní komponenty montáže. Případně zvolte pole **Mn.  k montáži na zakázku**.
7. Na stránce **Řádky montáže na zakázku** vytvořte nový řádek typu **Zboží** pro požadovaný další obsah sady. Řádek představuje další komponentu montáže.

   Můžete také upravit objednávku zvýšením množství jedného standardního zboží v sadě. To lze provést zvýšením hodnoty v poli **Množství za** na konkrétním řádku montážní zakázky.

   > [!NOTE]
   > Stránka **Řádky montáže na zakázku** obsahuje pouze základní pole, které může prodejce použít k přizpůsobení seznamu komponent, přidání čísel sledování zboží nebo k vyřešení problémů s dostupností komponent. Chcete-li zobrazit další informace o montážní zakázce, například počáteční datum zakázky, zvolte akci **Zobrazit doklady**. Tím se otevře úplné zobrazení montážní zakázky, která je propojena s řádkem prodejní objednávky. Obsah většiny polí v hlavičce montážní zakázky nelze změnit a nelze z ní zaúčtovat výstup montáže, protože je nutné použít zaúčtování dodávky řádku prodejní objednávky.
   > V záhlaví propojených montážních zakázek lze změnit pouze pole **Počáteční datum**, aby montážní pracovníci mohli určit datum, které je dřívější než datum splatnosti, kdy zahájí proces. Všechna pole na řádcích připojené montážní zakázky lze změnit tak, aby pracovníci skladu mohli během procesu zadávat údaje o spotřebě.
   > 
8. Zkontrolujte nebo reagujte na problémy s dostupností komponent. Vyberte například dostupné náhradní zboží nebo vytvořte pozdější datum splatnosti.
9. Zavřete stránku **Řádky montáže na zakázku**. Propojená montážní zakázka je nyní připravena začít sestavovat přizpůsobené zboží do data splatnosti.
10. Na prodejní objednávce vyberte akci **Vydat** a informujte oddělení montáže, že proces montáže může začít.
11. V oddělení montáže proveďte kroky sestavení zboží, které se v tomto postupu prodávají. Pro více informací navštivte [Montáž zboží](assembly-how-to-assemble-items.md).

## Viz také
[Správa montáže](assembly-assemble-items.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
