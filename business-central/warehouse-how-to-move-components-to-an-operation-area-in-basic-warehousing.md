---
    title: How to Move Components to an Operation Area in Basic Warehouse Configurations | Microsoft Docs
    description: If item processing operations occur at your warehouse location, then you may have to move items between internal bins to respond to internal source documents, such as production, assembly, or service orders at the location.
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
# Přesouvání komponent do provozní oblasti v základních konfiguracích skladu
Pokud v lokaci skladu dochází k operacím zpracování zboží, budete pravděpodobně muset přesunout zboží mezi interními přihrádky, abyste mohli reagovat na interní zdrojové doklady, jako jsou výrobní, montážní nebo servisní zakázky v lokaci.

> [!NOTE]
> Pro informace o přesouvání zboží mezi přihrádky bez zdrojových dokladů viz Interní přesuny.

V pokročilých konfiguracích skladu, což jsou lokace, která používají nastavení pole **Řízené zaskladnění/vyskladnění**, můžete použít stránku **Sešit přesunu** k přesunutí zboží mezi přihrádky. Pro více informací navštivte [Přesun zboží v rozšířených konfiguracích skladu](warehouse-how-to-move-items-in-advanced-warehousing.md).

V základních konfiguracích skladu, což jsou lokace, která používají nastavení polí **Přihrádka nutná** a **Vyžadovat vyskladnění**, můžete zapsat přesun zboží do interních oblastí operací na základě interních zdrojových dokladů následujícími způsoby:

- Pomocí stránky **Přesun zásob**.
- Pomocí stránky **Vyskladnění zásob**.

> [!NOTE]
> Vyskladnění zásob účtuje také záporné položky zboží jako spotřebu a je podporováno pouze pro komponenty výroby. Pro více informací navštivte stránku Vyskladnění zásob.

Podrobné informace o přesouvání zásob naleznete na stránce Přesun zásob.

Počáteční přesun zásob mohou vytvořit dvě různé role. Pracovník montáže jej například může vytvořit z vydané montážní zakázky tak, aby se zobrazil v seznamu prací prováděných pracovníkem skladu. Chcete-li vytvořit přesun zásob pro řádky montážní zakázky, které jsou připraveny k přesunutí komponent do určených přihrádek, použije pracovník montáže funkci **Vytvořit přesun zásob**.

Alternativně ji pracovník skladu může vytvořit tak, že odkazuje na příslušnou vydanou montážní zakázku. To je popsáno v následujícím postupu.

> [!NOTE]
> Pokud jde o přesun pro montážní zakázky, kde je zboží sestaveno do prodejní objednávky, pak můžete definovat, že doklad přesunu skladu se automaticky vytvoří, když vytvoříte doklad o vyskladnění zásob, který vezme hotové zboží montáže a zaúčtuje dodávku. Chcete-li toto nastavení nastavit, vyberte na stránce **Nastavení montáže** pole **Vytvořit pohyby automaticky**.
> Pro více informací o montážních zakázkách a základních konfiguracích skladu navštivte [Zpracování zboží montáže na zakázku s vyskladněním zásob](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).
> 
Tento postup ukazuje, jak vytvořit přesun zásob ze stránky **Přesun zásob** pomocí odkazu na vydanou montážní zakázku jako na zdrojový doklad. Postup je stejný, když přesouváte komponenty pro výrobní zakázky a servisní zakázky.

## Přesun komponent do provozní oblasti v základních konfiguracích skladu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Přesun zásob** a poté vyberte související odkaz.
2. Na záložce **Obecné** vyplňte pole **Číslo**. Můžete vybrat z číselné řady stisknutím klávesy Enter.
3. Do pole **Kód lokace** zadejte lokaci, kde k přesunu dochází.
4. Vyberte akci **Kopie pův.dokladů**. Případně vyplňte pole **Původní doklad** a poté v poli **Číslo původu** vyberte tlačítko **AssistEdit**.
5. Na stránce **Původní doklady** vyberte montážní zakázku, pro kterou chcete součásti přesunout, a pak zvolte tlačítko **OK**.

   Pro každou potřebnou komponentu, kterou lze přesunout, se na stránce **Skladové přesuny** vygeneruje jeden řádek Vzít a jeden řádek Vložit. Všechna pole kromě **Množ. ke zpracování** jsou předvyplněny podle řádků původního dokladu. Pole **Mn.  ke zpracování** je nastaveno na nulu, dokud nezadáte množství, které jste skutečně přesunuli.

   Kód přihrádky můžete změnit na řádku Vzít, ale pouze podle dostupnosti. Pokud zvolíte tlačítko **AssistEdit** v poli **Kód přihrádky** na řádku Vzít, otevře se stránka **Obsah přihrádky** a ta zobrazí pouze přihrádky kde je komponenta k dispozici.

   Kód přihrádky na řádku Vložit nelze změnit. Akceptován je pouze kód přihrádky, který je definován na řádku komponenty původního dokladu. To podporuje princip, že role (v tomto postupu je to pracovník montáže), která požaduje komponentu, ví, kde musí být komponenta umístěna. Pokud chcete komponenty umístit do jiné přihrádky, musíte nejprve změnit kód přihrádky na řádku komponenty a poté znovu vytvořit řádky přesunu zásob.
6. Do pole **Množ. ke zpracování** zadejte úplné nebo částečné množství, které jste skutečně přesunuli. Hodnota na řádcích Vzít a Vložit musí být stejná. Jinak nemůžete přesun zapsat.

   > [!NOTE]
Stejně jako v jiných činnostech ve skladu můžete řádek Vložit rozdělit výběrem akce **Akce** a následným výběrem akce **Rozdělit řádek**. V takovém případě se součet dvou rozdělených řádků musí rovnat množství na řádku Vzít.

7. Až budete připraveni zapsat přesuny, které jste provedli, zvolte akci **Zaznamenat  skladový přesun**.

   Položky skladu jsou vytvořeny tak, že komponenty nyní existují v přihrádkách určených na řádcích montážní zakázky.

   > [!NOTE]
Na rozdíl od toho, kdy přesunete komponenty pomocí vyskladnění zásob, spotřeba nebude zaúčtována, když zaregistrujete přesun zásob. Tento krok musí být proveden samostatně zaúčtováním výstupu a spotřeby montážní objednávky. Pro více informací navštivte Montážní zakázka.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
