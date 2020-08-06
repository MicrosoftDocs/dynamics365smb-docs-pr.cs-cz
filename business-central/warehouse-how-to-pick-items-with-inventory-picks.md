---
    title: How to Pick Items with Inventory Picks | Microsoft Docs
    description: If a location is set up to require pick processing but not shipment processing, you use the inventory pick documents to record and post picking and shipping information for your source documents.
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
# Vyskladnění zboží pomocí vyskladnění zásob
Pokud je lokace nastavena tak, aby vyžadovala zpracování vyskladnění, ale ne zpracování dodávky, použijte stránku **Vyskladnění zásob** k zaznamenání a zaúčtování informací o vyskladnění a dodání pro původní doklady. Výstupní původní doklad může být prodejní objednávka, objednávka nákupní vratky, výstupní objednávka transferu nebo výrobní zakázka, jejíž komponenty jsou připraveny k vyskladnění.

> [!NOTE]
> Komponenty pro montážní objednávky nelze vyskladnit nebo zaúčtovat pomocí vyskladnění zásob. Místo toho použijte stránku **Přesun zásob**. Pro více informací navštivte [Přesouvání komponent do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

> Při vyskladnění a dodání množství na prodejním řádku, které je sestaveno na objednávku, musíte při vytváření řádků vyskladnění zásob dodržovat určitá pravidla. Pro více informací navštivte sekci „Zpracování zboží sestaveného na objednávku ve vyskladnění zásob“.

Vyskladnění zásob můžete vytvořit třemi způsoby:

- Vytvořte vyskladnění ve dvou krocích tak, že nejprve požádáte o vyskladnění zásob vydáním původního dokladu. To je signalizace pro sklad, že původní doklad je připraven k vyskladnění. Vyskladnění zásob lze pak vytvořit na stránce **Vyskladnění zásob** na základě původního dokladu.
- Vytvořte vyskladnění zásob přímo ze samotného původního dokladu.
- Pomocí dávkové úlohy můžete vytvořit vyskladnění zásob pro několik původních dokladů současně.

## Žádost o vyskladnění zásob pomocí vydání původního dokladu
U prodejních objednávek, objednávek nákupní vratky a výstupních objednávek transferu vytvoříte požadavek skladu pomocí vydání objednávky. Následující text popisuje, jak to provést z prodejní objednávky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Vyberte prodejní objednávku, kterou chcete vydat, a poté vyberte akci **Vydat**.

U výrobních zakázek automaticky vytvoříte požadavek skladu pro vyskladnění komponent, nazývaný *spotřeba*, když se stav výrobní zakázky změní na **Vydaná** nebo když je vytvořena vydána výrobní zakázka. Pro více informací navštivte [Vyskladnění pro výrobu nebo montáž](warehouse-how-to-pick-for-production.md).

Po vytvoření požadavku na sklad může zaměstnanec skladu přiřazený ke zboží k vyskladnění vidět, že původní doklad je připraven k vyskladnění, a může vytvořit nový doklad vyskladnění na základě požadavku skladu.

## Vytvoření vyskladnění zásob na základě původního dokladu
Nyní, když je požadavek vytvořen, může pracovník skladu vytvořit nové vyskladnění zásob na základě vydaného původního dokladu.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění zásob** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. V poli **Původní doklad** vyberte typ původního dokladu, pro který chcete zboží vyskladnit.
4. V poli **Číslo původu** vyberte původní doklad.
5. Případně zvolte akci **Kopie původ.dokladu**, chcete-li vybrat doklad ze seznamu výstupních půdovních dokladů, které jsou připraveny k vyskladnění v lokaci.
6. Zvolte tlačítko **OK**, chcete-li vyplnit řádky vyskladnění podle vybraného původního dokladu.

## Vytvoření vyskladnění zásob z původního dokladu
1. V původním dokladu, kterým může být prodejní objednávka, objednávka nákupní vratky, výstupní objednávka transferu nebo výrobní zakázka, zvolte akci **Vytvořit zaskl./vyskl.zásob**.
2. Zaškrtněte políčko **Vytvořit vyskladnění  zásob**.
3. Vyberte tlačítko **OK**. Poté bude vytvořeno nové vyskladnění zásob.

## Vytvoření více vyskladnění zásob s pomocí dávkové úlohy
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vytvořit zaskl. /vyskl.zásob** a poté vyberte související odkaz.
2. Na záložce **Požadavek skladu** použijte pole **Původní doklad** a **Číslo původu** k filtrování určitých typů dokladů nebo rozsahů čísel dokladů. Například můžete vytvářet vyskladnění pouze pro prodejní objednávky.
3. Na záložce **Možnosti** zašktněte políčko **Vytvořit vyskladnění  zásob**.
4. Vyberte tlačítko **OK**. Poté jsou vytvořeny zadané vyskladnění zásob.

> [!NOTE]
> Při vyskladnění a dodání množství prodejních řádků, které jsou sestaveny na objednávku, byste měli při vytváření řádků pro vyskladnění zásob dodržovat určitá pravidla. Pro více informací navštivte sekci „Zpracování zboží sestaveného na objednávku ve vyskladnění zásob“.
> V základních konfiguracích skladu je zboží sestavené do prodejních objednávek vyskladněno ze související prodejní objednávky, jak je vysvětleno v tomto tématu. Pro více informací navštivte „Zpracování zboží sestaveného na objednávku ve vyskladnění zásob“.
> 
## Zaznamenání vyskladnění zásob
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění zásob** a poté vyberte související odkaz.
2. V poli **Kód přihrádky** na řádcích vyskladnění je přihrádka, ze které musí být zboží vyskladněno, navržena podle výchozí přihrádky zboží. V případě potřeby můžete přihrádku na této stránce změnit.
3. Proveďte vyskladnění a zadejte informace o skutečném zaskladněném množství do pole **Množ. ke zpracování**.

   Pokud je nutné vyskladnění zboží pro jeden řádek z více než jedné přihrádky, například proto, že není k dispozici v určené přihrádce, použijte funkci **Rozdělit řádek** na záložce **Řádky**. Pro více informací o rozdělení řádků navštivte [Rozdělení řádků aktivit skladu](warehouse-how-to-split-warehouse-activity-lines.md).
4. Po provedení vyskladnění vyberte akci **Účtovat**.

Proces účtování zaúčtuje dodání řádků zdrojového dokladu, které byly vyskladněny, nebo v případě výrobních zakázek proces účtování zaúčtuje spotřebu. Pokud lokace používá přihrádky, účtování také vytvoří položky skladu pro zaúčtování změn množství přihrádky.

## Odstranění řádků vyskladnění zásob
Pokud zboží na vyskladnění zásob není k dispozici, můžete tyto řádky vyskladnění zásob po zaúčtování odstranit a potom odstranit i doklad vyskladnění zásob. Zdrojový doklad, například prodejní objednávka nebo výrobní zakázka, bude mít zbývající zboží, které má být vyskladněno, které lze získat prostřednictvím nového vyskladnění zásob později, jakmile bude zboží k dispozici.

> [!WARNING]
Tento proces není možný, pokud jsou v původním dokladu uvedena sériová čísla/čísla šarže. Pokud například řádek prodejní objednávky obsahuje sériové číslo/číslo šarže, bude tato specifikace sledování zboží odstraněna, pokud bude odstraněn řádek vyskladnění zásob pro sériové číslo/číslo šarže.
Pokud mají řádky vyskladnění zásob sériová čísla/čísla šarží, která nejsou k dispozici, není nutné dané řádky odstranit. Místo toho musíte změnit pole **Množ. ke zpracování** na nulu, zaúčtovat skutečné vyskladnění a potom odstranit doklad vyskladnění zásob. Tím je zajištěno, že řádky vyskladnění zásob pro tato sériová čísla/čísla šarží lze později znovu vytvořit z prodejní objednávky.

## Zpracování zboží montáže na zakázku pomocí vyskladnění zásob
Stránka **Vyskladnění zásob** se také používá k vyskladnění a dodání pro prodej, kde musí být zboží sestaveno před jejich odesláním. Pro více informací navštivte [Prodej zboží montáže na obejdnávku](assembly-how-to-sell-items-assembled-to-order.md).

Zboží, které má být dodáno, není fyzicky přítomno v přihrádce, dokud není sestaveno a zaúčtováno jako výstup do přihrádky v oblasti montáže. To znamená, že vyskladnění zboží montáže na zakázku k odeslání se řídí zvláštním postupem. Z přihrádky pracovníci skladu převezou zboží montáže do dodacího prostoru a poté zaúčtují vyskladnění zásob. Zaúčtovaná vyskladnění zásob pak zaúčtuje výstup sestavy, spotřebu komponenty a prodejní dodávku.

Můžete nastavit [!INCLUDE[d365fin](includes/d365fin_md.md)] pro automatické vytvoření přesunu zásob při vytvoření vyskladnění zásob pro zboží montáže. Chcete-li to povolit, musíte na stránce **Nastavení montáže** vybrat pole **Vytvořit pohyby automaticky**. Pro více informací navštivte [Přesouvání komponent do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Řádky vyskladnění zásob pro prodejní zboží jsou vytvořeny různými způsoby v závislosti na tom, zda žádné, některé nebo všechna množství prodejního řádku jsou smontovány na zakázku.

V běžném prodeji, kde používáte vyskladnění zásob k zaúčtování dodávky množství zásob, je pro každý řádek prodejní objednávky vytvořen jeden řádek vyskladnění zásob nebo několik položek, pokud je zboží umístěno do různých přihrádek. Tento řádek vyskladnění je založen na množství v poli **K  dodání**.

Při montáži na zakázku, kde je na zakázku sestaveno celé množství na objednávce, je pro toto množství vytvořen jeden řádek pro vyskladnění zásob. To znamená, že hodnota v poli Množství k montáži je stejná jako hodnota v poli **K  dodání**. Na řádku je vybráno pole **Montáž na zakázku**.

Pokud je pro lokaci nastaven výstupní tok montáže, pak hodnota v poli **Kód dod. přihr. montáže-na-zák.** nebo hodnota v poli **Kód přihrádky z montáže**  v tomto pořadí je vložena do pole **Kód přihrádky** na řádku vyskladnění zásob.

Pokud na řádku prodejní objednávky není zadán žádný kód přihrádky a pro lokaci není nastaven žádný výstupní tok montáže, je pole **Kód přihrádky** na řádku vyskladnění zásob prázdné. Pracovník skladu musí otevřít stránku **Obsah přihrádky** a vybrat přihrádku, ve které je sestaveno zboží montáže.

V kombinovaných scénářích, kde musí být nejprve sestavena část množství a další musí být vyskladněna ze skladu, jsou vytvořeny minimálně dva řádky vyskladnění zásob. Jeden řádek vyskladnění je pro množství montáže na zakázku. Druhý řádek vyskladnění závisí na tom, které přihrádky mohou vyplnit zbývající množství ze skladu. Kódy přihrádek na dvou řádcích jsou vyplněny různými způsoby, jak je popsáno pro dva různé typy prodeje. Pro více informací navštivte sekci “Kombinované scénáře” v [Princip montáže na zakázku a montáže na sklad](assembly-assemble-to-order-or-assemble-to-stock.md).

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
