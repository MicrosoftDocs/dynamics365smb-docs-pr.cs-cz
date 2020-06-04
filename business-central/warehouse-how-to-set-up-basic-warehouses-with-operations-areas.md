---
    title: How to Set Up Basic Warehouses with Operations Areas | Microsoft Docs
    description: If internal operation areas such as production or assembly exist in basic warehouse configurations where locations use the **Bin Mandatory** setup field and possibly the **Require Pick** and **Require Put-away** setup fields, then you use three basic warehouse documents to record your warehouse activities for internal operation areas.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2019
    ms.author: sgroespe

---
# Nastavení základních skladů s provozními oblastmi
Pokud v základních konfiguracích skladu existují vnitřní provozní oblasti, jako je výroba nebo montáž, kde skladová místa používají nastavení přihrádky pole **Přihrádka nutná**, případně **Vyžadovat vyskladnění** a **Vyžadovat zaskladnění**, můžete k evidenci aktivit skladu pro interní provozní oblasti použít následující základní doklady skladu:

- Stránku **Přesuny**.
- Stránku **Vyskladnění zásob**.
- Stránku **Zaskladnění zásob**.

> [!NOTE]
> Přestože se nastavení nazývá **Vyžadovat vyskladnění** a **Vyžadovat zaskladnění**, stále můžete účtovat příjmy a dodávky přímo ze zdrojových obchodních dokumentů na lokacích, kde zaškrtnete tyto políčka.

Chcete-li tyto stránky použít k interním operacím, například k vyskladnění a přesunu komponent do výroby, je třeba provést některé nebo všechny následující kroky nastavení podle toho, jakou kontrolu potřebujete:

- Povolte doklady vyskladnění zásob, přesunutí a zaskladnění.
- Definujte výchozí struktury přihrádek pro komponenty a koncové položky, které budou proudit do a z provozních zdrojů.
- Vytvořte do- a z- přihrádky vyhrazené pro konkrétní provozní zdroje, aby se zabránilo vyskladnění zboží výstupními doklady

Kódy přihrádek nastavené na kartách lokace definují výchozí tok skladu pro určité aktivity, například komponenty v oddělení montáže. Existují další funkce, které zajistí, že když jsou položky umístěny do určité přihrádky, nemohou být přesunuty nebo vydány do jiných aktivit. Pro více informací navštivte [Vytvoření dedikované přihrádky komponent](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).

Následující postupy jsou založeny na nastavení základních aktivit skladu v oblasti výroby. Kroky jsou podobné pro další oblasti činnosti, jako je montáž, servis a projekty.

> [!NOTE]
> V následujícím postupu je jako předběžná podmínka vybrána pole nastavení **Přihrádka nutná** na kartě lokace, protože se to považuje za základ pro jakoukoli úroveň správy skladu.

## Povolení skladových dokladů pro interní operace skladu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete kartu lokace, kterou chcete nastavovat.
3. V záložce **Sklad** vybráním políčka **Vyžadovat zaskladnění** označíte, že při uvolnění vstupního nebo interního původního dokladu s kódem přihrádky lze vytvořit zaskladnění zásob nebo doklad o přesunu zásob.
4. Zaškrtnutím políčka **Vyžadovat vyskladnění** označíte, že při vytvoření výstupního nebo interního zdrojového dokladu s kódem přihrádky je nutné vytvořit vyskladnění zásob nebo doklad o přesunu zásob.

## Definování výchozí struktury přihrádky v oblasti výroby
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete lokaci, kterou chcete nastavovat.
3. V záložce **Přihrádky** v poli **Kód přihrádky díly** zadejte kód přihrádky v oblasti výroby s množstvím komponent, z nichž může operátor na stroji spotřebovat, aniž by požádal o aktivitu skladu pro dodání do přihrádky. Zboží, které jsou umístěny v této přihrádce, se obvykle nastavují pro automatické účtování nebo vyčištění. To znamená, že pole **Metoda spotřeby** obsahuje **Ručně** nebo **Zpětně** .
4. Do pole **Kód přihrádky do výroby** zadejte kód přihrádky, kde jsou komponenty vyskladněné pro výrobu a umístěny ve výchozím nastavení dříve, než mohou být spotřebovány. Položky, které jsou umístěny v této přihrádce, jsou obvykle nastaveny pro ruční účtování spotřeby. To znamená, že pole **Metoda spotřeby** obsahuje **Ruční** nebo **Vyskladnění + dopředu** nebo **Vyskladnění + zpětně** pro vyskladnění a pohyby zásob.

   > [!NOTE]
   > Když použijete vyskladnění zásob,  pole **Kód přihrádky** na řádku komponenty výrobní zakázky definuje *Přihrádku*, ze které jsou komponenty při účtování spotřeby sníženy. Při použití pohybů zásob  pole **Kód přihrádky** na řádcích komponent výrobní zakázky definuje *umístění* operační oblasti, do které musí pracovník skladu komponenty umístit.

5. V záložce **Přihrádky** v poli **Kód přihrádky z výroby** zadejte kód přihrádky v oblasti výroby, ve které jsou dokončené koncové položky převzaty ve výchozím nastavení, když proces zahrnuje aktivitu skladu. V základních konfiguracích skladu je aktivita zaznamenána jako zaskladnění zásob nebo přesun zásob.

Nyní, řádky komponenty výrobní zakázky s výchozím kódem přihrádky vyžadují, aby byly do této složky umístěny předem spotřebované komponenty. Dokud však nebudou komponenty spotřebovány z této přihrádky, mohou z této přihrádky vybírat nebo spotřebovávat další požadavky na komponenty, protože jsou stále považovány za dostupný obsah přihrádky. Chcete-li zajistit, aby byl obsah přihrádky k dispozici pouze pro požadavek na komponentu, který používá tuto výrobní přihrádku, musíte na řádku vyplnit kód přihrádky na **Vyhrazená** na řádku pro tento kód přihrádky na stránce **Přihrádky**, kterou otevřete z karty lokace.

Tento vývojový diagram ukazuje, jak je vyplněno pole <x1 />Kód přihrádky<x2 /> na řádcích komponent výrobní zakázky podle vašeho nastavení.

![Vývojový diagram toku přihrádky](media/binflow.png "BinFlow")

## Definování výchozí struktury přihrádek v oblasti montáže
Komponenty pro montážní zakázky nemohou být vydány nebo zaúčtovány s vyskladněním zásob. Místo toho použijte stránku **Přesuny**. Pro více informací navštivte [Přesouvání komponent do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

Při Vyskladnění a odesílání prodejních řádků, které jsou smontovány pro objednávku, musíte při vytváření řádků vyskladnění zásob dodržet určitá pravidla. Pro více informací navštivte  sekci "Zpracování zboží montáže na zakázku a vyskladnění zásob" ve Vyskladnění zboží pomocí vyskladnění zásob.

Pro více informací navštivte [Správa montáže](assembly-assemble-items.md).

### Nastavení automatického vytvoření přesunu při vyskladnění zásob pro montážní zakázku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení montáže** a poté vyberte související odkaz.
2. Zaškrtněte políčko **Vytvořit pohyby automaticky**.

### Nastavit přihrádky montáže, ve které jsou komponenty ve výchozím nastavení umístěny, než mohou být spotřebovány
Hodnota v tomto poli je automaticky vložena do pole **Kód přihrádky** na řádcích montážní zakázky, když je toto umístění zadáno do pole **Kód lokace** na řádku montážní zakázky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete lokaci, kterou chcete nastavovat.
3. Vyplňte pole **Kód přihrádky na montáž**.

### Nastavení přihrádky montáže, do které se při dokončení montáže zaúčtuje hotové zboží
Hodnota v tomto poli je automaticky vložena do pole **Kód přihrádky** v hlaviček montáže, když je tento kód lokace vyplněn do pole ** Kód lokace** v hlavičce montážní zakázky4.

Kódy přihrádek nastavené na kartách lokace definují výchozí tok skladu pro specifické aktivity skladu, jako je například spotřeba komponent v oblasti montáže. Existují další funkce, které zajistí to, že případě umístění zboží do výchozí přihrádky, nemohou být přesunuty nebo vydány do jiných aktivit.

> [!NOTE]
> Toto nastavení je možné pouze v přídadě, že je na lokaci nastaveno "Přihrádka nutná".

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete lokaci, kterou chcete nastavovat.
3. Vyplňte políčko **Kód přihrádky z montáže**.

### Nastavení přihrádky, do níž je dokončené zboží montáže zaúčtováno, jakmile jsou montáže propojené prodejní objednávky
Z této přihrádky je zboží montáže odesláno okamžitě, prostřednictvím vyskladnění, k naplnění prodejní objednávky.

> [!NOTE]
> Toto pole nelze používat, pokud je na lokaci nastaveni řízené zaskladnění a vyskladnění.

Kód přihrádky se kopíruje z řádku prodejní objednávky do hlavičky montážní zakázky, aby bylo sděleno pracovníkům montáže, kam mají umístit výstup pro expedici. Zkopíruje se také do řádku vyskladnění, aby bylo možné sdělit pracovníkům skladu, odkud je mají převzít.

> [!NOTE]
> Kód dod. přihr. montáže na zakázku zůstává vždy prázdný. Při zaúčtování prodejního řádku montáže na zakázku je obsah přihrádky nejprve pozitivně upraven pomocí výstupu montáže. Ihned poté je negativně upraveno s dodaným množstvím.

Hodnota v tomto poli je automaticky vložena do pole Kód přihrádky na řádcích prodejní objednávky, které obsahují množství v poli **Množství  montáže na zakázku** nebo pokud jsou prodány **Montáž na zakázku** v poli **Systém doplnění**.

Pole**Kód dod.   přihrádky montáže na zakázku** je prázdné, místo toho se použije **Kód přihrádky z montáže**. Pokud jsou obě pole nastavení prázdná, použije se v řádcích **Kód přihrádky<x6 /> na řádcích prodejních objednávek naposledy použitá přihrádka s obsahem.

Stejný kód přihrádky se pak zkopíruje do pole **Kód přihrádky** na řádku vyskladnění zásob, který spravuje dodávku množství montážní zakázky. Pro více informací navštivte  sekci "Zpracování zboží montáže na zakázku a vyskladnění zásob" ve Vyskladnění zboží pomocí vyskladnění zásob.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete lokaci, kterou chcete nastavovat.
3. Vyplňte pole **Kód dod. přihr.  montáže na zakázku**.

## Vytvoření vyhrazených přihrádek komponent
Můžete určit, že množství v přihrádce je chráněno proti vyskladnění pro jiné požadavky než pro poptávku z jejich aktuálního účelu.

Množství v vyhrazených zásobnících může být stále rezervováno Proto jsou množství ve vyhrazených přihrádkách zahrnuta do pole **Celkové dostupné množství** na stránce **Rezervace**.

Například, pracovní centrum nastaveno s kódem přihrádky v poli **Kód přihrádky do výroby**. Řádky komponenty výrobní zakázky s tímto kódem přihrádky vyžadují, aby byly do tohoto kódu umístěny předem vyprazdňované komponenty. Dokud však nebudou komponenty spotřebovány z této přihrádky, mohou z této přihrádky vybírat nebo spotřebovávat další požadavky na komponenty, protože jsou stále považovány za dostupný obsah přihrádky. Chcete-li se ujistit, že obsah přihrádky je k dispozici pouze pro požadavek, který používá tuto přihrádku pro výrobu, musíte vybrat pole **Vyhrazeno** na řádku pro přihrádku na stránce **Přihrádky**, kterou otevřete z karty lokace.

Vytvoření vyhrazené přihrádky poskytuje podobnou funkci jako použití typů přihrádek, které jsou k dispozici pouze v rozšířeném skladu. Pro více informací navštivte <x3/>Nastavení typu přihrádky<x4/>.

> [!Caution]
> Zboží ve vyhrazené přihrádce nená chráněno proti vyskladnění a spotřebě jako výrobníí komponenty na kartě vyskladnění.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz. Vyberte lokaci, kterou chcete aktualizovat.
2. Vyberte tlačítko **Přihrádky**.
3. Vyberte pole **Vyhrazeno** pro každou přihrádku, kterou chcete použít výhradně pro určité interní operace a kde chcete, aby množství bylo rezervováno pro tuto interní operaci, jakmile je tam umístěno.

> [!NOTE]
> Přihrádka musí být prázná, předtám než můžete vybrat nebo smazat pole **Vyhrazeno**.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
