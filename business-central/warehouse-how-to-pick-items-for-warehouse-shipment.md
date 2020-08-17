---
    title: How to Pick Items for Warehouse Shipment | Microsoft Docs
    description: When the location is set up to require warehouse pick processing as well as warehouse shipment processing, you use the warehouse pick documents to create and process pick information prior to posting the warehouse shipment.
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
# Vyskladnění zboží pro dodávku ze skladu
Pokud je lokace nastavena tak, aby vyžadovala zpracování vyskladnění a zpracování dodávky ze skladu, použijte doklady vyskladnění k vytvoření a zpracování informací o vyskladnění před zaúčtováním dodávky ze skladu.

Doklad vyskladnění nelze vytvořit od začátku, protože aktivita vyskladnění je vždy součástí workflow, a to buď ve vyžádaném nebo nabízeném scénáři.

Doklady vyskladnění můžete vytvořit tak, že otevřete prázdný doklad o dodávce ze skladu, zjistíte zdrojové doklady, které jsou vydány v dodávce, a poté pro tyto dodávky vytvoříte řádky pro vyskladnění skladu. Pomocí funkcí **Kopie pův.dokladů** nebo **Použití filtrů pro kopie pův.dokladů** můžete zjistit zdrojové doklady, které jsou připraveny k odeslání.

Případně můžete použít stránku **Sešit vyskladnění**  k vytažení a vytvoření řádků vyskladnění v dávkovém režimu. Pro více informací navštivte [Plánování v sešitech vyskladnění](warehouse-how-to-plan-picks-in-worksheets.md).

Doklady vyskladnění můžete také vytvořit nabízeným způsobem ze stránky **Dodávka ze skladu** výběrem možnosti **Vytvořit vyskladnění**.

> [!NOTE]
> Vyskladnění ddávek ze skladu u zboží, které je spojeno s dodanou prodejní objednávkou, probíhá podle stejných kroků jako u pravidelných vyskladnění zboží k dodání, jak je popsáno v tomto tématu. Počet řádků vyskladnění pro množství, které má být dodáno, však může být vyšší, protože vybíráte komponenty, nikoli zboží montáže.
> Řádky vyskladnění jsou vytvořeny pro hodnotu v poli **Zůstatek (množství)** na řádcích montážní zakázky, která je spojena s řádkem prodejní objednávky, který je dodán. Tím zajistíte, že všechny komponenty jsou vyskladněny v jedné akci.
> Pro více informací navštivte sekci “Zpracování zboží montáže na zakázku v dodávkách ze skladu”.
Pro informace o vyskaldnění komponent pro montážní zakázky včetně situací, kdy zboží montáže není splatné u prodejní dodávky, navštivte [Vyskladnění pro výrobu nebo montáž](warehouse-how-to-pick-for-production.md).

## Vyskladnění zboží pro dodávku ze skladu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění** a poté vyberte související odkaz.

   Pokud potřebujete pracovat na konkrétním vyskladnění, vyberte vyskladnění ze seznamu nebo seznam vyfiltrujte a vyhledejte vyskladnění, která vám konkrétně byla přiřazena. Otevřete kartu vyskladnění.
2. Pokud je pole **Přiřazené ID uživatele** prázdné, zadejte své ID, abyste se v případě potřeby identifikovali.
3. Proveďte skutečné vyskladnění zboží.

   Pokud je sklad nastaven na použití přihrádek, použijí se výchozí přihrádky zboží k navržení, odkud má být zboží odebráno. Pokyny se zobrazují jako dva samostatné řádky, alespoň jeden pro každý typ akce, Vzít a Vložit.

   Pokud je sklad nastaven na použití řízeného zaskladnění a vyskladnění, použije se pořadí přihrádek k výpočtu nejvhodnějších přihrádek, ze kterých se má zboží vyskladnit, a tyto přihrádky jsou pak navrženy na řádcích vyskladnění. Pokyny se zobrazují jako dva samostatné řádky, alespoň jeden pro každý typ akce, Vzít a Vložit.

4. Po provedení vyskladnění a umístění zboží do oblasti pro odeslání nebo přihrádky pro dodání zvolte akci **Zápis vyskladnění**.

Osoba odpovědná za dodávku může nyní přinést zboží do doku dodávky a zaúčtovat dodávku, včetně souvisejícího původního dokladu, na stránce **Dodávka ze skladu**. Pro více informací navštivte [Odesílání zboží](warehouse-how-ship-items.md).

Kromě vyskladnění pro zdrojové doklady, jak je popsáno v tomto tématu, můžete vkládat a brát zboží mezi přihrádky bez odkazu na zdrojové doklady. Pro více informací navštivte [Vyskladnění a zaskladnění bez zdrojového dokumentu](warehouse-how-to-create-put-aways-from-internal-put-aways.md).

## Zpracování zboží montáže na zakázku v dodávkách ze skladu
V scénářích sestavení na zakázku, se pole **K  dodání** na řádcích dodávky ze skladu používá k zaznamenání počtu jednotek montáže. Zadané množství se poté zaúčtuje jako výstup sestavy při dodávke ze skladu.

U ostatních řádků dodávky ze skladu je hodnota v poli **K  dodání** od začátku nulová.

Když pracovníci odpovědní za montáž dokončí montáž dílů nebo celé množství montáže na zakázku, zaznamenají je do pole **K  dodání** na řádku dodávky ze skladu a poté vyberou akci **Účtovat dodávku**. Výsledkem je, že odpovídající výstup sestavy je zaúčtován, včetně spotřeby komponent. Prodejní dodávka pro množství je zaúčtována pro prodejní objednávku.

Na montážní zakázce můžete zvolit **Řádek dod. ze skladu  mont. zakázky** pro přístup k řádku dodávky ze skladu. To je vhodné pro pracovníky, kteří obvykle nepoužívají stránku **Dodávka ze skladu**.

Po zaúčtování dodávky ze skladu jsou aktualizována různá pole na řádku prodejní objednávky, aby se zobrazoval průběh ve skladu. Následující pole jsou také aktualizovány, aby bylo možné zobrazit, kolik množství montáže na zakázku zbývá sestavit a odeslat:

- **Montáž-na-zakázku sklad.  zbývající množství**
- **Montáž-na-zakázku sklad.  zbývající  množství  (základ)**

> [!NOTE]
V kombinovaných scénářích, ve kterých musí být část množství nejprve sestavena a jiná musí být dodána ze zásob, jsou vytvořeny dva řádky pro dodávku ze skladu. Jeden je pro množství montáže na zakázku a druhý pro množství zásob.

> V takovém případě je množství montáže na zakázku zpracováno tak, jak je popsáno v tomto tématu, a množství zásob je zpracováno jako jakýkoli jiný řádek běžné dodávky ze skladu. Pro více informací o kombinovaných scénářích navštivte [Princip montáže na zakázku a montáže na sklad](assembly-assemble-to-order-or-assemble-to-stock.md).

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
