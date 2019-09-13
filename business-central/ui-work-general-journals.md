---
title: Použití Finančních deníků k přímému účtování do hlavní knihy | Microsoft Docs
description: 'Další informace o používání deníků k účtování finančních transakcí na účty hlavní knihy a další účty, jako jsou účty bank a dodavatelů.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 03/01/2019
ms.author: sgroespe
---
# <a name="working-with-general-journals"></a>Práce s Finančními Deníky

Většina finančních transakcí je zaúčtována do hlavní knihy prostřednictvím vyhrazených obchodních dokumentů, jako jsou nákupní faktury a prodejní objednávky. Můžete však také zpracovat obchodní činnosti, jako je nákup, výplata nebo náhrada výdajů za zaměstnance, a to tak, že zaúčtujete řádky deníku v  různých denících v [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Většina deníků je založena na *Finančním deníku* a všechny transakce můžete zpracovat na stránce **Finančního deníku**. Pro více informací navštivte[Účtujte transakce přímo do hlavní knihy](finance-how-post-transactions-directly.md).  

Například můžete zaúčtovat výdaje zaměstnanců na výdaje spojené s podnikáním, abyste je mohli později uhradit. Pro více informací navštivte [Zaznamenávaní a uhrazovaní výdajů zaměstnanců](finance-how-record-reimburse-employee-expenses.md).

V mnoha případech však budete chtít pro registraci plateb používat deníky, které jsou optimalizovány pro konkrétní typy transakcí, jako je například **Deník plateb**. Pro více informací navštivte [Záznam plateb a vrácení peněz do deníku plateb](payables-how-post-payments-refunds.md).  

Finanční deníky používáte k zaúčtování finančních transakcí přímo na účty hlavní knihy a další účty, jako jsou bankovní účty, účty zákazníků, dodavatelů a zaměstnanců. Účtování pomocí finančního deníku vždy vytvoří položky na účtech hlavní knihy. To platí i tehdy, když například zaúčtujete řádek deníku na účet zákazníka, protože položka je zaúčtována na účet pohledávek hlavní knihy prostřednictvím účtovací skupiny.

Informace, které zadáte do deníku, jsou dočasné a mohou být změněny, zatímco jsou v deníku. Když zaúčtujete deník, informace se přenesou do záznamů na jednotlivých účtech, kde je nelze změnit. Můžete však použít nepublikované účtované položky a můžete zveřejňovat reverzní nebo opravné položky. Pro více informací navštivte [Reverzní účtovaní](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Používaní šablon a listů deníku

Existuje několik šablon finančního deníku. Každá šablona deníku je reprezentována vyhrazeným oknem s konkrétními funkcemi a poli, která jsou vyžadována pro podporu těchto funkcí, jako je například stránka **Deník odsouhlasení plateb** pro zpracování bankovních plateb a stránka **Deník Plateb** pro platby vašim dodavatelům nebo proplacení vašich zaměstnanců. Pro více informací navštivte [Provedení platby](payables-make-payments.md) a [Odsouhlasení platby zákazníků s Deníkem přijaté hotovosti nebo z Položek zákazníka](receivables-how-apply-sales-transactions-manually.md).

Pro každou šablonu deníku můžete nastavit vlastní osobní deník jako list deníku. Můžete například definovat vlastní list deníku pro deník plateb, který má vaše osobní rozvržení a nastavení. Následující tip je příkladem přizpůsobení deníku.

> [!TIP]  
> Pokud zaškrtnete políčko **Navrhnout vyrovnávací částku** na řádku pro váš list na stránce **Listy finančního deníku**, pak se pole **Částka** například na řádcích finančního deníku pro stejné číslo dokumentu automaticky vyplní hodnotou, která je nutná k vyrovnání dokumentu. Pro více informací navštivte [Nechat [!INCLUDE[d365fin](includes/d365fin_md.md)] Navrhnout hodnoty](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Porozumění hlavním a vyrovnávacím účtům
Pokud jste nastavili výchozí vyrovnávací účty pro listy deníku na stránce **Finanční deníky**, vyrovnávací účet bude vyplněn automaticky, když vyplníte pole **Číslo účtu**. Jinak vyplňte pole **Číslo účtu** i **Protiúčet. Pole Číslo účtu** ručně. Kladná částka v poli **Částka** je zaúčtovaná na hlavní účet a připsána na vyrovnávací účet. Záporná částka je připsána na hlavní účet a odúčtována na vyrovnávací účet.

> [!NOTE]  
>   DPH se počítá zvlášť pro hlavní účet a vyrovnávací účet, takže se mohou použít různé procentní sazby DPH.

## <a name="working-with-recurring-journals"></a>Práce s Periodickými deníky
Periodický deník je obecný deník se specifickými poli pro správu transakcí, které často účtujete, s malými nebo žádnými změnami, jako je nájemné, předplatné, elektřina a teplo. Pomocí těchto polí pro opakované transakce můžete účtovat pevné i variabilní částky. Můžete také určit automatické storno pro den po datu účtování. Můžete také použít alokační klíče k rozdělení opakujících se položek mezi různé účty. Pro více informací navštivte [Přidělení opakujících se částek deníku na několik účtů](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).

U opakujícího se deníku je třeba položky, které budou zveřejněny pravidelně, psát pouze jednou. To znamená, že účty, dimenze a hodnoty dimenzí atd., které zadáte, zůstanou po zaúčtování v deníku. Pokud jsou nutné úpravy, můžete je provést s každým účtováním.

### <a name="recurring-method-field"></a>Pole Metoda periody
Toto pole určuje, jak bude po zaúčtování zpracována částka na řádku deníku. Pokud například použijete stejnou částku při každém zaúčtovaní řádku, můžete částku ponechat. Pokud na řádku použijete stejné účty a text, ale částka se bude při každém účtování lišit, můžete částku po zaúčtovaní odstranit.

| Viz | také |
| --- | --- |
|Pevná|Částka na řádku deníku zůstane po zaúčtování.|
|Proměnná|Částka na řádku deníku bude po zaúčtování odstraněna.|
|Zůstatek|Zaúčtovaná částka na řádku účtu bude přidělena mezi účty určené pro řádek v tabulce Deníku rozdělení. Saldo na účtu bude tedy nastaven na nulu. Nezapomeňte vyplnit pole **Alokace %** na stránce **Alokace**. Pro více informací navštivte [Přidělení opakujících se částek deníku na několik účtů](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).|
|Reverzní neměnná|Částka na řádku deníku zůstane po zaúčtování a vyrovnávací položka bude zaúčtována následující den.|
|Reverzní proměnná|Částka na řádku deníku bude po zaúčtování odstraněna a vyrovnávací položka bude zaúčtována následující den.|
|Reverzní saldo|Zaúčtovaná částka na řádku účtu bude přidělena mezi účty určené pro řádek na stránce **Přidělení**. Saldo na účtu bude nastaven na nulu a následující den se zaúčtuje vyrovnávací položka.|

> [!NOTE]  
>  Pole DPH mohou být vyplněna buď na řádku periodického deníku, nebo na řádku deníku přidělení, ale nikoli na obou. To znamená, že je lze vyplnit na stránce **Alokace**, pouze pokud nejsou vyplněny odpovídající řádky v periodickém deníku.

### <a name="recurring-frequency-field"></a>Pole Frekvence periody
Toto pole určuje, jak často bude položka na řádku deníku zaúčtována. Je to pole Vzorec data a musí být vyplněno pro řádky periodického deníku. Pro více informací navštivte [Použití vzorců dat ](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Příklady:
Pokud musí být řádek deníku zaúčtován každý měsíc, zadejte „1M“. Po každém účtování bude datum v poli **Zúčtovací datum** aktualizovaný na stejné datum v příštím měsíci.

Chcete-li zaúčtovat položku v poslední den každého měsíce, můžete provést jednu z následujících akcí:

- Zaúčtujte první položku v poslední den měsíce zadáním 1D+1M-1D (1 den + 1 měsíc - 1 den). U tohoto vzorce se datum účtování vypočítá správně bez ohledu na to, kolik dní v měsíci je.

- Zaúčtujte první položku v libovolný den v měsíci zadáním 1M + CM. U tohoto vzorce bude datum účtování po jednom úplném měsíci + zbývajících dnech aktuálního měsíce.

### <a name="expiration-date-field"></a>Pole Datum expirace
Toto pole určuje datum, kdy bude řádek zaúčtován naposledy. Po tomto datu už řádek nebude účtován.

Výhodou použití tohoto pole je, že řádek nebude z deníku odstraněn okamžitě a stávající datum expirace můžete vždy nahradit pozdějším, takže můžete tento řádek použít i do budoucna.

Pokud je pole prázdné, řádek bude zaúčtovaný pokaždé, když položku zaúčtujete, dokud nebude odstraněn z deníku.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Přidělení částek periodického deníku na několik účtů
Na stránce **Periodický finanční deník** si můžete vybrat akci **Přidělení**, abyste viděli nebo spravovali, jak jsou částky na řádku periodického deníku přiděleny několika účtům a dimenzím. Všimněte si, že přidělení funguje jako řádek vyrovnávacího účtu pro řádek periodického deníku.

Stejně jako v periodickém deníku je třeba zadat přidělení pouze jednou. Přidělení zůstane v deníku přidělení i po zaúčtování, takže nemusíte zadávat částky a přidělení pokaždé, když zaúčtujete řádek periodického deníku.

Pokud je metoda periody v periodickém deníku nastavena na **Saldo** nebo **Reverzní saldo**, nebudou při nastavení účtu na nulu ignorovány žádné kódy hodnot dimenze v periodickém deníku. Pokud tedy na stránce **Přidělení** přidělíte opakující se řádek různým hodnotám dimenze, bude vytvořena pouze jedna reverzní položka. Pokud tedy přiřadíte řádek periodického žurnálu, který obsahuje kód hodnoty dimenze, pak na stránce **Přidělení** nesmíte zadat stejný kód. Pokud tak učiníte, budou hodnoty dimenze nesprávné.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Příklad: Přidělení plateb nájemného do různých oddělení
Platíte nájem každý měsíc, takže jste vložili částku nájemného na hotovostní účet na řádek periodického deníku. Na stránce **Přidělení** můžete rozdělit výdaje mezi několik oddělení (dimenze oddělení) podle počtu čtverečních metrů, které každé z nich zabírá. Výpočet je založen na procentuálním přídělu na každém řádku. Můžete zadat různé účty na různých řádcích přidělení (pokud se nájemné také rozdělí mezi několik účtů), nebo můžete zadat stejný účet, ale s různými kódy hodnot dimenze pro dimenzi oddělení na každém řádku.

## <a name="working-with-standard-journals"></a>Práce se standardními deníky
Pokud jste vytvořili řádky deníku, o kterých víte, že je budete pravděpodobně později vytvářet znovu, můžete je uložit jako standardní deník před zaúčtováním deníku. Tato funkce se vztahuje na deníky a finanční deníky.

> [!NOTE]  
>   Následující postup se vztahuje na deník položek, ale informace se vztahují také na finanční deník.

### <a name="to-save-a-standard-journal"></a>Uložení standardního deníku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník položky** a poté vyberte související odkaz.
2. Zadejte jeden nebo více řádků deníku.
3. Vyberte řádky deníku, které chcete znovu použít.
4. Vyberte akci **Uložit jako Standardní deníky**.
5. Na stránce **Uložit jako Standardní deníky ** definujte nový nebo existující Standardní deníky zboží, do kterého se mají řádky uložit.

    Pokud jste již vytvořili jeden nebo více standardních deníků položek a chcete jeden z nich nahradit novou sadou řádků deníku, v poli Kód vyberte požadovaný kód.
6. Stisknutím tlačítka **OK** potvrďte, zda chcete přepsat existující standardní deník zboží a nahradit veškerý jeho obsah.
7. Pokud chcete uložit hodnoty do pole **Jednotkové ceny** standardního deníku položek, vyberte pole **Uložit jednotkovou cenu**.
8. Vyberte pole **Uložit množství**, pokud chcete, aby program ukládal hodnoty do pole **Množství**.
9. Zvolte tlačítko **OK** pro uložení standardního deníku zboží.

Po dokončení ukládání standardního deníku se zobrazí stránka Deník položek, takže můžete pokračovat v jeho účtovaní, protože víte, že jej lze snadno znovu vytvořit, až budete muset zaúčtovat stejné nebo podobné řádky.

### <a name="to-reuse-a-standard-journal"></a>Opětovné použití standardního deníku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník položky** a poté vyberte související odkaz.
2. Vyberte akci **Získat standardní deníky**.

    Otevře se stránka Standardní deníky zboží, kde jsou zobrazeny kódy a popisy pro všechny existující standardní deníky.
3. Chcete-li zkontrolovat Standardní deníky zboží, než jej vyberete pro opětovné použití, vyberte akci **Zobrazit deník**.

    Veškeré změny, které provedete ve standardním deníku položek, jsou implementovány okamžitě. Budou tam příště, když otevřete nebo znovu použijete daný standardní deník. Proto byste si měli být jisti, že změna je natolik důležitá, aby se obecně použila. Jinak proveďte konkrétní změnu v deníku položek po vložení standardních řádků deníku. Viz krok 4.
4. Na stránce **Standardní deníky zboží** vyberte Standardní deníky zboží, který chcete opětovně použit a potom vyberte tlačítko **OK**.

    Nyní je deník položek vyplněn řádky, které jste uložili jako standardní deník. Pokud řádky deníku již existovaly v deníku položek, vložené řádky budou umístěny pod existující řádky deníku.

    Pokud jste při použití funkce **Uložení jako Standardní deníky zboží** nezaškrtli pole **Uložit jednotkovou cenu**, pak se pole **Jednotkové ceny** na řádcích vložených ze standardního deníku automaticky vyplní aktuální hodnotou položky a zkopíruje se z pole **Jednotkových nákladů** na kartě položky.

    > [!NOTE]  
    >   Pokud jste vybrali pole **Uložit jednotkovou cenu** nebo **Uložit množství**, měli byste se před účtováním deníku položky ujistit, že vložené hodnoty jsou správné pro tuto konkrétní úpravu.

    Pokud vložené řádky deníku položek obsahují uložené jednotkové částky, které nechcete zaúčtovat, můžete je rychle upravit na aktuální hodnotu položky následujícím způsobem.

6. Vyberte řádky deníku položek, které chcete upravit, a poté vyberte akci **Přepočítat jednotkovou cenu**. Tím se aktualizuje pole Jednotková ceny s aktuální jednotkovou cenou položky.
7. Zvolte akci **Účtovat**.

## <a name="to-renumber-document-numbers-in-journals"></a>Přečíslování čísel dokumentů v denících
Chcete-li se ujistit, že se neobjeví chyby účtování kvůli pořadí čísel dokumentů, můžete použít funkci **Přečíslovat čísla dokladů** před zaúčtováním deníku.

Ve všech denících, které jsou založeny na finančním deníku, je pole **Číslo dokladu** upravitelné, takže můžete zadat různá čísla dokladu pro různé řádky deníku nebo stejné číslo dokladu pro související řádky deníku.

Pokud je vyplněno pole **Číselné řady** v listu deníku, vyžaduje funkce účtování ve finančních denících, aby číslo dokladu na jednotlivých nebo seskupených řádcích deníku bylo v sekvenčním pořadí. Chcete-li se ujistit, že se neobjeví chyby účtování kvůli pořadí čísel dokumentů, můžete použít funkci **Přečíslovat čísla dokladů** před zaúčtováním deníku. Pokud byly související řádky deníku před použitím funkce seskupeny podle čísla dokumentu, zůstanou seskupeny, ale může jim být přiřazeno jiné číslo dokumentu.

Tato funkce funguje také na filtrovaných pohledech.

Jakékoli přečíslování čísel dokumentů bude respektovat související aplikace, například platební aplikaci, která byla vytvořena z dokumentu na řádku deníku na účet dodavatele. Proto pole **ID vyrovnání** a **Číslo vyrovnání dokladu** na příslušných položkách hlavní knihy mohou být aktualizovány.

Následující postup je založen na stránce **Finančního deníku**, ale vztahuje se na všechny ostatní deníky, které jsou založeny na finančním deníku, jako je například stránka **Deník plateb**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deník** a poté vyberte související odkaz.
2. Až budete připraveni zaúčtovat deník, vyberte akci **Přečíslovat čísla dokladů**.

Hodnoty v poli **Čísla dokladu** se v případě potřeby mění, takže číslo dokumentu na jednotlivých nebo skupinových řádcích deníku je v sekvenčním pořadí. Po přečíslování dokumentů můžete pokračovat v účtování deníku.

## <a name="see-also"></a>Viz také
[Zaúčtování transakce přímo do Hlavní knihy](finance-how-post-transactions-directly.md)  
[Reverzní účtovaní](finance-how-reverse-journal-posting.md)  
[Přidělení nákladů a výnosů](year-allocate-costs-income.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
