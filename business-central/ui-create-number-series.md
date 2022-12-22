---
title: Create Number Series
description: Learn how to set up number series that assign unique ID codes to accounts and documents in Business Central.
author: edupont04


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.search.form: 456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31
ms.date: 03/24/2022
ms.author: edupont

---
# Vytváření Číselných řad

Pro každou společnost, kterou jste založili, musíte přiřadit jedinečné identifikační kódy k věcem jako jsou účty hlavní knihy, účty zákazníků a dodavatelů, faktury a další doklady. Číslování je důležité nejen pro identifikaci. Dobře navržený systém číslování také činí společnost lépe zvládnutelnou a snadno analyzovatelnou a může snížit počet chyb, ke kterým dochází při zadávání dat.

> [!Important]
> Ve výchozím nastavení nejsou mezery v číselných řadách povoleny, protože přesná historie finančních transakcí musí být ze zákona k dispozici pro audit, a proto musí následovat nepřerušovanou sekvenci bez smazaných čísel..
>
> Pokud chcete povolit mezery v určitých číselných řadách, nejprve se poraďte se svým auditorem nebo účetním manažerem, abyste se ujistili, že dodržujete zákonné požadavky ve vaší zemi. Další informace naleznete v části [Mezery v číselných řadách](#gaps-in-number-series).

> [!NOTE]  
> Doporučujeme používat stejné kódy číselných řad, jaké jsou uvedeny na stránce **Přehled číselných řad</f0> v demonstrační společnosti CRONUS. Kódy jako *P-INV+* vám nemusí dávat okamžitý smysl, ale [!INCLUDE[prod_short](includes/prod_short.md)] má řadu výchozích nastavení, která závisí na těchto kódech číselných řad.

Systém číslování vytvoříte nastavením jednoho nebo více kódů pro každý typ hlavních dat nebo dokladu. Můžete například nastavit jeden kód pro číslování zákazníků, jiný kód pro číslování prodejních faktur a jiný kód pro číslování dokladů ve finančních denících. Po nastavení kódu musíte nastavit alespoň jeden řádek číselné řady. Řádek číselné řady obsahuje takové informace, jako jsou první a poslední číslo v řadě a počáteční datum. Pro jeden kód číselné řady lze nastavit více než jeden řádek číselné řady, s odlišným počátečním datem pro každý řádek Řady se budou používat postupně, zahájením každé série v příslušné počáteční datum.

> [!NOTE]
> Maximální délka čísla v číselné řadě je 20 znaků. V některých situacích [!INCLUDE[prod_short](includes/prod_short.md)] připojí číslo s ID vygenerovaným systémem.< Například při použití dokladů, jako jsou faktury, k uplatnění transakcí, například plateb, generuje [!INCLUDE[prod_short](includes/prod_short.md)] identifikátory pro uplatněné transakce. Identifikátor se skládá z čísla z číselné řady a šestiznakového ID přiřazeného systémem, například -12345. Pokud očekáváte zpracování více než 9999 dokladů v bankovních nebo GIRO denících nebo deníkech pokladních příjmů, nastavte číselné řady pro tyto typy dokladů tak, aby obsahovaly méně než 14 znaků.

Obvykle nastavíte svou číselnou řadu tak, aby se nové pořadové číslo automaticky vkládalo na nové karty nebo doklady, které vytvoříte. Můžete ale nastavit řadu čísel tak, abyste mohli nové číslo zadat ručně. Toto lze specifikovat zaškrtnutím políčka **Ruční čísla**.

Pokud chcete použít více než jeden číselný kód řady pro jeden typ hlavních dat - například, pokud chcete použít různé číselné řady pro různé kategorie zboží - můžete použít vztahy číselných řad.

## Mezery v číselných řadách
Ne všechny záznamy, které vytvoříte v [!INCLUDE[prod_short](includes/prod_short.md)] jsou finanční transakce, které musí používat sekvenční číslování. Karty zákazníků, prodejní nabídky a aktivity skladu jsou příklady záznamů, kterým je přiřazeno číslo z číselné řady, ale nepodléhají finančnímu auditu a lze odstranit. U těchto číselných řad můžete zaškrtnout políčko **Povolit mezery v číselné řadě** na stránce **Řádky číselných řad**. Toto nastavení lze také změnit po vytvoření číselné řady. Pro více informací navštivte [Vytváření nových číslených řad](ui-create-number-series.md#to-create-a-new-number-series).

## Chování pole Číslo na dokladech a kartách

Na prodejních, nákupních dokladech včetně transferů a na všech kartách lze pole **Číslo** vyplnit automaticky z předdefinované číselné řady nebo jej můžete přidat ručně. Za určitých okolností je však pole **Číslo** neviditelné, abyste jej nemohli upravovat.

Pole **Číslo** lze vyplnit třemi způsoby:

1. Pokud pro daný typ dokladu nebo karty existuje pouze jedna číselná řada a je vybráno pole **Výchozí čísla** pro tuto číselnou řadu a není vybráno pole **Ruční čísla**, pole se automaticky vyplní dalším číslem v řadě. Pole **Číslo** nebude na kartě nebo dokladu viditelné.

   I když definujete pro zákazníky šablony s různými číselnými řadami a je číselná řada, která je definována na stránce **Nastavení prodeje a pohledávek**, nastavena tímto způsobem, pole **Číslo** bude na kartě zákazníka neviditelné bez ohledu na to, kterou šablonu použijete. Totéž platí pro jiné typy karet a dokladů.

   > [!NOTE]  
   > Pokud číselná řada nefunguje, například proto, že jí došla čísla, zobrazí se pole **Číslo** a vy můžete ručně zadat číslo nebo vyřešit problémy na stránce**Číselná řada**.

2. Pokud existuje více než jedna číselná řada pro daný typ dokladu nebo karty a pro aktuálně přiřazenou číselnou řadu není zaškrtnuto políčko **Výchozí čísla** zobrazí se pole **Číslo** a můžete vyhledat a vybrat číselnou řadu na stránce **Číselná řada**, kterou chcete použít. Další číslo v řadě se pak vloží do pole **Číslo**.

3. Pokud jste pro typ dokladu nebo karty nenastavili číselnou řadu nebo pokud je pro číselnou řadu vybráno pole **Ruční čísla** pak pole **Číslo** je viditelné a jakékoli číslo musíte zadat ručně. Můžete zadat maximálně 20 znaků, a to jak číslic, tak písmen.

Když otevřete nový doklad nebo kartu, pro kterou existuje číselná řada, pak se otevře příslušné **Nastavení číselných čad** kde můžete nastavit číselnou řadu pro daný typ dokladu nebo karty před pokračováním v zadávání dalších dat.

> [!NOTE]  
> Pokud potřebujete povolit ruční číslování například u nových karet zboží, , které byly vytvořeny procesem migrace dat, který ve výchozím nastavení skryl pole **Číslo**, bežte do **Nastavení zásob** a vyberte **Číslo zboží** a nastavte související číselnou řadu na **Ruční čísla**.

## Vytvoření nové číselné řady

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Číselná řada** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Na novém řádku vyplňte pole dle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vyberte akci **Řádky**.
5. Na stránce **Řádky číselné řady** vyplňte pole pro definování skutečného použití a obsahu číselné řady, kterou jste vytvořili v kroku 2.
6. Opakujte krok 5 pro tolik různých použití číselné řady, kolik potřebujete. Pole **Počáteční datum**definuje, který řádek číselné řady je aktivní.

> [!TIP]
> Chcete-li například umožnit uživatelům zadávat čísla ručně při evidenci nového zákazníka nebo dodavatele, vyberte pole **Ruční čísla** na samotné číselné řadě. Chcete-li zakázat ruční čísla smažte obsah pole.

Číselné řady můžete přiřadit k šablonám, které jste nastavili pro různé typy zákazníků a dodavatelů, které vaši prodejci a nákupčí nejčastěji přidávají do vašeho [!INCLUDE [prod_short](includes/prod_short.md)]. V takovém případě nastavte příslušné číselné řady, propojte je prostřednictvím vztahů a poté přidejte první číselnou řadu v příslušném vztahu na příslušnou stránku nastavení. Když poté uživatel vytvoří zákazníka, vybere příslušnou šablonu a novému zákazníkovi se přiřadí číslo z číselné řady definované pro danou šablonu.

## Vytvoření vztahů mezi číselnými řadami

Pokud jste nastavili více než jeden kód číselné řady pro stejný druh základní evidence nebo transakcí, můžete vytvořit vztahy mezi těmito kódy. Tato funkce vám může pomoci při rozhodování mezi kódy při použití čísla číselné řady. Při nastavování relace mezi skupinou číselných řad přidružíte všechny související řady k jednomu kódu číselné řady. Poté můžete tento kód zadat do pole v záložce **Číselné řady** na jedné z relevantních stránek nastavení, jako je **Nastavení prodeje a pohledávek**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Číselná řada** a poté vyberte související odkaz.
2. Vyberte řádek s číselnou řadou, pro kterou chcete vytvořit vztah, a pak zvolte **Vztah**.
3. Do pole **Kód řady** zadejte kód číselné řady, kterou chcete přiřadit k řadě vybrané v kroku 2.
4. Přidejte řádek pro každý kód, který chcete přiřadit k vybrané číselné řadě.
5. Zavřete stránku.

V případě že nyní nastavíte něco, co vyžaduje číslo, můžete použít vztahy, které jste vytvořili, k výběru mezi souvisejícími číselnými řadami.

## Nastavení místa použití číselných řad

Následující postup ukazuje, jak nastavit číselné řady pro oblast Prodeje. Kroky jsou podobné i pro další oblasti.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení prodeje a pohledávek** a poté vyberte související odkaz.
2. Na stránce **Nastavení prodeje a pohledávek** v záložce **Číselné řady** vyberte požadovanou číselnou řadu pro každou kartu nebo doklad.

Vybrané číslo bude nyní použito k vyplnění pole **Číslo** na příslušné kartě nebo dokladu podle nastavení, které jste provedli na řádku číselné řady.



## Podívejte se na související školení na webu [Microsoft Learn](/learn/modules/number-series-trail-codes-dynamics-365-business-central/index)

## Viz také
[Nastavení [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
