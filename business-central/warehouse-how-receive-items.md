---
    title: How to Receive Items | Microsoft Docs
    description: When items arrive at a warehouse that is set up for warehouse receipt processing, you must retrieve the lines of the released source document that triggered their receipt.
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
# Příjem zboží
Když zboží dorazí do skladu, který není nastaven pro zpracování příjemky skladu, jednoduše zaznamenáte příjemku na související obchodní doklad, například nákupní objednávku, objednávku prodejní vratky nebo příchozí objednávku transferu.

Když zboží dorazí do skladu, který je nastaven pro zpracování příjmu na sklad, musíte načíst řádky vydaného původního dokladu, který spustil jejich příjem. Pokud máte přihrádky, můžete buď přijmout původní přihrádku, která je vyplněna, nebo pokud zboží nebylo nikdy předtím použito ve skladu, vyplňte přihrádku, kde má být zboží zaskladněno. Poté musíte vyplnit množství přijatého zboží a zaúčtovat příjemku.

## Příjem zboží s nákupní objednávkou
Následující text popisuje, jak přijímat zboží s nákupní objednávkou. Kroky jsou podobné u objednávek prodejní vratky a objednávek transferu.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.
2. Otevřete existující nákupní objednávku nebo vytvořte novou. Pro více informací navštivte [Záznam nákupu](purchasing-how-record-purchases.md).
3. Do pole **K  příjmu** zadejte přijaté množství.

> [!NOTE]
> Pokud je přijaté množství vyšší, než bylo objednáno v nákupní objednávce a prodejce byl nastaven tak, aby byli povoleny nadměrné příjmy, v poli **Množství** použijte pole **Nadměrný příjem**, které slouží ke zpracování nadměrného množství. Pro více informací navštivte [Příjem více zboží, než bylo objednáno](warehouse-how-receive-items.md#to-receive-more-items-than-ordered).
4. Vyberte akci **Účtovat**.

Hodnota v poli **Přijaté  množství** je aktualizována. Pokud se jedná o částečný příjem, je hodnota nižší než hodnota v poli **Množství**.

> [!NOTE]
> Pokud k zaúčtování příjemky použijete doklad skladu, nemůžete použít akci **Účtovat** na nákupní objednávce. Místo toho pracovník skladu již zaúčtoval množství objednávky jako přijaté. Pro více informací navštivte  [Příjem zboží pomocí příjemky na sklad](warehouse-how-receive-items.md#to-receive-items-with-a-warehouse-receipt).

## Příjem zboží pomocí příjemky na sklad
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Příjemky na sklad** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.

   Vyplňte pole na záložce **Obecné**. Při načtení řádků původního dokladu se některé informace zkopírují na každý řádek.

   Pro konfiguraci skladu s řízeným zaskladněním a vyskladněním, pokud má lokace výchozí zónu a přihrádku pro příjmy, jsou pole **Kód zóny** a **Kód přihrádky** vyplněna automaticky, ale můžete je podle potřeby změnit.

   > [!NOTE]
   > Pokud chcete přijímat zboží s jinými kódy třídy skladu, než je kód třídy přihrádky v poli **Kód přihrádky** v hlavičce dokladu, musíte před načtením řádků původního dokladu pro zboží odstranit obsah pole **Kód přihrádky** v hlavičce.
3. Vyberte akci **Kopie pův.dokladů**. Otevře se stránka **Původní doklady**.

   Z nové nebo otevřené příjemky skladu můžete použít stránku **Výběr filtru původu skladu** k načtení vydaných řádků původního dokladu, které definují, které zboží má být přijato nebo dodáno.

   1. Vyberte akci **Použít filtry pro kopii pův. dokl.**.
   2. Chcete-li nastavit nový filtr, zadejte do pole **Kód** popisný kód a poté vyberte akci **Upravit**.
   3. Vyplněním příslušných polí filtru určete typ řádků původního dokladu, které chcete načíst.
   4. Vyberte akci **Start**.
   Všechny vydané řádky původního dokladu, které splňují kritéria filtru, jsou nyní vloženy na stránku **Příjemka na sklad**, ze které jste aktivovali funkci filtru.

   Kombinace filtrů, které definujete, se uloží na stránce **Výběr filtru původu skladu**, dokud je příště nebudete potřebovat. Můžete vytvořit neomezený počet kombinací filtrů. Kritéria můžete kdykoli změnit výběrem akce **Upravit**.

4. Vyberte původní doklady, pro které chcete přijímat zboží, a pak zvolte tlačítko **OK**.

   Řádky původních dokladů se zobrazí na stránce **Příjemka na sklad**. Pole **K  příjmu** je vyplněno nevyřízeným množstvím pro každý řádek, ale množství můžete podle potřeby změnit. Pokud jste před získáním řádků odstranili obsah pole **Kód přihrádky** na záložce **Obecné**, musíte vyplnit příslušný kód přihrádky na každém řádku příjmu.

   > [!NOTE]
   > Vyplňte pole **K  příjmu** na všech řádcích s hodnotou nula a zvolte akci **Odstranit množ. k příjmu**. Chcete-li jej znovu vyplnit zbývajícím množstvím, zvolte akci **Automat.vyplnit množ. k příjmu**.

   > [!NOTE]
   > Nelze přijmout více zboží, než je uvedeno v poli **Zbývající  množ.** na řádku původního dokladu. Chcete-li získat více zboží, načtěte další původní doklad, který obsahuje řádek pro zboží, pomocí funkce filtru a získejte původní doklady se zbožím.

5. Zaúčtujte příjemku na sklad. Pole množství jsou aktualizována v původních dokladech a zboží je zaznamenáno jako součást zásob společnosti.

Pokud používáte zaskladnění, řádky příjmu jsou odeslány do skladu pomocí funkce zaskladnění. Zboží, přestože bylo přijato, nemůže být vybráno, dokud nebylo předtím zaskladněno. Přijaté zboží je označeno jako dostupné zásoby pouze po zaregistrování zaskladnění.

Pokud nepoužíváte zaskladnění, ale používáte přihrádky, zaskladnění se zaznamená v přihrádce určené na řádku původního dokladu.

> [!NOTE]
> Pokud používáte funkci **Účtovat a vytisknout**, odešlete příjemku a vytisknete instrukci zaskladnění, která vám ukáže, kam umístit zboží.
> Pokud vaše lokace používá řízené zaskladnění/vyskladnění, pak se šablony zaskladnění používají k výpočtu nejlepšího místa pro zaskladnění zboží. Toto je potom vytištěno na instrukci pro zaskladnění.
> 
## Příjem více zboží, než bylo objednáno
Pokud obdržíte více zboží, než jste si objednali, můžete je místo zrušení příjemky příjmout. Například může být levnější ponechat přebytek ve vašem skladu, než je vrátit, nebo vám prodejce může nabídnout slevu za jejich přijetí.

### Nastavení nadměrného příjmu
Je nutné definovat procento, o které povolíte překročení objednaného množství při příjmu. Definujete to prostřednictvím kódu nadměrného příjmu, který obsahuje procento v poli **Tolerance nadměrného příjmu %**. Poté kód přiřadíte kartám příslušného zboží nebo kartám dodavatelů.

Následující text popisuje, jak nastavit a přiřadit kód nadměrného příjmu ke zboží. Kroky jsou podobné i pro dodavatele.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Otevřete kartu zboží, o kterém máte podezření, že může být někdy doručeno v větším množství, než bylo objednáno.
2. Vyberte vyhledávací tlačítko v poli **Kód nadměrného příjmu**.
3. Vyberte akci **Nový**.
4. Na stránce **Kódy nadměrného příjmu** vytvořte jeden nebo více nových řádků, které definují různé zásady nadměrného příjmu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
5. Vyberte řádek a poté stiskněte tlačítko **OK**.

Kód nadměrného příjmu je nyní přiřazen ke zboží. Jakákoli nákupní objednávka nebo příjemka na sklad pro toto zboží nyní umožňuje příjem více než objednaného množství podle stanoveného procenta tolerance při převzetí.

> [!NOTE]
Můžete nastavit workflow schvalování, který vyžaduje, aby byly nadměrné příjmy schváleny před tím jako budou zpracovány. V takovém případě musíte na stránce **Kódy nadměrného příjmu** zaškrtnout políčko **Požadováno schválení**. Pro tento účel existuje ve standardních datech workflow vyhrazená reakce workflow **Schválení nadměrného příjmu**. Pro více informací navštivte [Vytvoření workflow](across-how-to-create-workflows.md).

### Provedení nadměrného příjmu
Na nákupních řádcích a řádcích příjmu skladu se pole **Množství nadměrného příjmu** používá k zaznamenávání nadměrně přijatého množství, což znamená množství, které překračují hodnotu objednaného množství v poli **Množství**.

Při zpracování nadměrného příjmu můžete zvýšit hodnotu v poli **K  příjmu** na skutečně přijaté množství. Pole **Množství nadměrného příjmu** je poté aktualizováno tak, aby ukazovalo nadměrné množství. Případně můžete zadat nadměrné množství do pole **Množství nadměrného příjmu**. Pole **K  příjmu** je pak aktualizováno tak, aby se zobrazilo objednané množství plus přebytek množství. Následující postup popisuje, jak vyplnit pole **K  příjmu**.

1. Na nákupní objednávce nebo v dokladu příjemky na sklad, kde je přijaté množství vyšší než objednané, zadejte skutečně přijaté množství do pole **K  příjmu**.

   Pokud je zvýšení v rámci tolerance určené přiřazeným kódem nadměrného příjmu, pole **Množství nadměrného příjmu** je aktualizováno tak, aby zobrazovalo množství, o které byla hodnota v poli **Množství** překročena.

   Je-li zvýšení nad stanovenou tolerancí, není přípustný příjem povolen. V takovém případě můžete prozkoumat, zda existuje jiný kód nadměrného příjmu, který to umožní. V opačném případě může být přijato pouze objednané množství a nadbytečné množství musí být zpracováno jinak, například jeho vrácením prodejci.

2. Zaúčtujte příjemku stejně jako u jakékoli jiné příjemky.

> [!NOTE]
[!INCLUDE[d365fin](includes/d365fin_md.md)] nezahrnuje funkce pro automatické zahájení finanční správy nadměrného příjmu. Musíte to zpracovat ručně po dohodě s prodejcem, například tím, že dodavatel předá novou nebo aktualizovanou fakturu.

## Viz související školení na [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
