---
    title: Design Details - Changing Costing Methods for Items
    description: Learn how to assign a different costing method to an item although you have already used the item in transactions.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: costing methods, costing, item cost
    ms.date: 06/08/2021
    ms.author: bholtorf

---

# Detaily návrhu: Změna metody ocenění pro zboží

V [!INCLUDE[prod_short](includes/prod_short.md)], nelze změnit metodu ocenění pro zboží po zahrnutí zboží do transakce. Například poté, co jste zboží koupili nebo prodali. Pokud byla zboží přiřazena nesprávná metoda ocenění, je možné, že problém nezjistíte, dokud neprovedete finanční výkaznictví.

Toto téma popisuje, jak tuto situaci vyřešit. Doporučeným přístupem je nahradit zboží, které má nesprávnou metodu ocenění, novým zbožím a použít montážní zakázku k převodu zásob ze starého zboží na nové.

> [!NOTE]
> Použití montážních zakázek umožňuje, aby bylo ocenení vždy aktivní, i když je třeba zaúčtovat neuhrazené nákupní faktury nebo poplatky za dopravu. Kromě toho vám umožňuje vrátit zpět převod a v případě potřeby získat množství původního zboží zpět.

> [!TIP]
> Abyste se s procesem seznámili, doporučujeme vám zahájit proces převodu s jedným zbožím nebo malou sadou zboží.

## O metodách ocenění

Metody ocenění řídí výpočty nákladů při nákupu, přijetí ve skladu a prodeji zboží. Metody ocenění ovlivňují načasování částek zaznamenaných v NNPZ, které ovlivňují hrubý zisk. Právě tento tok vypočítává NNPZ. Náklady na prodané zboží (NNPZ) a tržby se používají k určení hrubého zisku takto:

*ghrubý zisk* = *tržby - NNPZ*

Při nastavování skladového zboží je nutné přiřadit metodu ocenění. Metoda se může lišit v souvislosti s firmou nebo konkrétním zbožím, takže je důležité vybrat tu správnou. [!INCLUDE[prod_short](includes/prod_short.md)] podporuje následující metody ocenľní:

* Průměrná
* Metoda FIFO
* Metoda LIFO
* Standardní
* Specifikcá

Pro více informace navštivte [Detaily návrhu: Metody ocenění](design-details-costing-methods.md).

## Použití montážních zakázek ke změně přiřazení metody ocenění

Tato část popisuje následující kroky pro změnu metody ocenění přiřazené ke zboží:

1. Definujte výchozí metodu ocenění.
2. Identifikujte zboží, pro které chcete změnit metodu ocenění, a přečíslujte je.
3. Vytvořte nové zboží se starým schématem číslování a zkopírujte kmenová data v dávce.
4. Ručně zkopírujte související kmenová data ze stávajícího zboží do nového zboží.
5. Určete množství zásob, které chcete převést z původního zboží na nové.
6. Převeďte zásoby na nové zboží.
7. Zpracování množství zásob, která jsou přidělena poptávce.
8. Zablokuje další použití původního zboží.

### Definování výchozí metody ocenění

Chcete-li se vyhnout budoucím chybám, můžete zadat výchozí metodu ocenění pro nové zboží. Kdykoli někdo vytvoří nové zboží, [!INCLUDE[prod_short](includes/prod_short.md)] navrhne výchozí metodu ocenění. Výchozí metodu zadáte v poli **Výchozí metoda ocenění** na stránce **Nastavení zásob**.

### Identifikujte zboží, pro které chcete změnit metodu ocenění, a přečíslujte je

Možná budete chtít dát svým novým zbožím stejná čísla jako těm, které nahrazují. Chcete-li to provést, změňte čísla stávajícího zboží. Pokud je například existující číslo zboží "P1000", můžete ho změnit na "X-P1000". Jedná se o ruční změnu, kterou musíte provést pro každé zboží.

### Vytvoření nového zboží se starým schématem číslování a zkopírování kmenových dat v dávce

Vytvořte nové zboží pomocí aktuálního číselného schématu. S výjimkou pole **Metoda ocenění** by nové zboží mělo obsahovat stejná kmenová data jako stávající zboží. Chcete-li přenést kmenová data pro zboží a související data z jiných prvků, použijte akci **Kopírovat zboží** na stránce **Karta zboží**. Pro více informací navštivte [Kopírování existujícího zboží pro vytvoření nového zboží](inventory-how-copy-items.md).

Po vytvoření nového zboží a přenosu kmenových dat přiřaďte správnou metodu ocenění.

### Ruční zkopírování souvisejících kmenových dat z původního zboží do nového zboží

Aby bylo nové zboží plně užitečné, musíte ručně zkopírovat některá kmenová data z jiných oblastí, jak je popsáno v následující tabulce.

| Oblast | Co kopírovat | Jak jej zkopírovat |
|---------|---------|---------|
| Zásoby | Skladové jednotky (SKJ) | Zkontrolujte, zda je pro původní zboží zadána SKJ. Pokud byly parametry plánování zadány pro každou kartu SKJ, musíte ručně vytvořit SKJ pro nové zboží. Pokud parametry nejsou specifikovány, můžete použít dávkovou úlohu **Vytvořit skladovou jednotku** ze stránky **Karta zboží** a data vytvořit. |
|     | Náhrady zboží | Zkontrolujte, zda jsou pro původní zboží definovány nějaké náhrady zboží. Pokud existují, přeneste tato data do nového zboží. Chcete-li zobrazit náhradní zboží, použijte akci **Náhrady** na stránce **Karta zboží**. |
|     | Analytické sestavy | Prohlédněte si sestavy Analýza zboží, Analýza prodeje a Analýza nákupu. Pro ty, které odkazují na původní zboží, můžete buď vytvořit novou sestavu analýzy s odkazem na nové zboží (zachování původní sestavy analýzy pro použití jako historie), nebo upravit sestavy tak, aby odkazovaly na nové zboží. |
|     | Standardní deníky | Zkontrolujte, zda standardní deníky odkazují na původní zboží, a v případě potřeby přeneste tato data do nového zboží. Tyto informace se nacházejí ve standardních denících, které jsou k dispozici v deníku zboží. |
| Prodej | Procento zálohy prodeje | Zkontrolujte, zda jsou pro původní zboží definována procenta prodejní zálohy, a přeneste tato data do nového zboží. Chcete-li zobrazit procenta zálohy, na stránce **Karta zboží** zvolte **Prodej** a poté **Procentní části zálohy**. |
| Nákup | Procento zálohy nákupu | Zkontrolujte, zda jsou pro původní zboží definována procenta nákupní zálohy, a přeneste tato data do nového zboží. Chcete-li zobrazit procenta zálohy, na stránce **Karta zboží** zvolte **Nákup** a poté **Procentní části zálohy**. |
| Sklad | Obsah přihrádky | Zkontrolujte obsah přihrádky definovaný pro původní zboží. Pokud sloupce, například Min. Množství, Max. Množství,Výchozí a Vyhrazeno byly zadány jednotlivě, pak musíte ručně vytvořit obsah přihrádky pro nové zboží. Pokud tomu tak není, není nutná žádná akce. [!INCLUDE[prod_short](includes/prod_short.md)] bude uchovávat záznamy při registraci skladových dokladů a deníků. |
| Projekt | Ceny projektu | Zkontrolujte, zda jsou ceny projektů definovány pro původní zboží a přeneste tato data do nového zboží. Tyto informace jsou k dispozici na stránce **Karta projektu** v části **Detaily projektu – poč. cen** v **Okně s fakty**. |
| Služba | Odbornosti v oblasti prostředků služeb | Zkontrolujte, zda jsou pro původní zboží definovány Odbornosti v oblasti prostředků služeb, a přeneste tato data do nového zboží. Chcete-li zobrazit odbornost zdrojů, použijte akci **Odbornosti zdroje** na sránce **Karta zboží**. |
|     | Komponenty předmětu servisu | Zkontrolujte, zda jsou komponenty definovány pro původní předmět servisu a přeneste tato data do nového zboží. Chcete-li zobrazit komponenty předmětu servisu, na stránce **Karta zboží** otevřete pomocí akce **Předmět servisu** seznam souvisejících předmětů servisu a poté zvolte akci **Komponenty**. |
| Výroba | Výrobní kusovníky | Zkontrolujte, zda některé výrobní kusovníky obsahují původní zboží a nahraďte ji novým zbožím. Chcete-li nahradit původní zboží, na stránce **Výrobní kusovníky** zvolte akci **Výměna zboží výr. kusovníku**. |
| Montáž | Kusovníky montáže | Zkontrolujte, zda některé kusovníky montáže obsahují původní zboží a ručně jej nahraďte novým zbožím. |

> [!IMPORTANT]
> Pokud je nová metoda ocenění Pevná, měli byste zadat hodnotu do pole **Pevná pořizovací cena** na stránce **Karta zboží**. Na stránce **Sešit pevné ceny** můžete odpovídajícím způsobem nastavit podíly nákladů. Pro více informací navštivte [Aktualizace pevná pořizovací ceny](finance-how-to-update-standard-costs.md).

### Určete množství zásob, které se má převést z původního zboží na nové zboží

> [!NOTE]
> Tento krok nebere v úvahu množství, která jsou zahrnuta v neodeslaných objednávkách. Pro více informací navštivte [Zpracování množství zásob, které jsou přiděleny poptávce](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand).

Použijte Deník fyzické inventury k vytvoření seznamu množství ve skladu. V závislosti na nastavení lokací skladu použijte jednu z následujících možností:

* Deník fyzické inventury
* Deník fyzické inventury skladu

Oba deníky mohou vypočítat množství zásob zboží, včetně lokace, varianty, přihrádky a umístění úložiště. Pro více informací navštivte [Počítání, úprava a reklasifikace zásob pomocí deníků](inventory-how-count-adjust-reclassify.md).

### Převeďte zásoby na nové zboží

Vytvořte a zaúčtujte montážní zakázky pro převod nákladů a množství zásob z původního zboží na nové zboží. Montážní zakázky mohou převést jedno zboží na druhé při zachování nákladů. To pomáhá zajistit, aby čisté součty pro účet zásob a NNPZ nebyly ovlivněny (s výjimkou případů, kdy je nová metoda oceněné standardní, v takovém případě mohou být náklady rozděleny na účty odchylek). Pro více informací navštivte [Správa montáže](assembly-assemble-items.md).

Při vytváření montážních zakázek použijte informace z Deníku fyzické inventury nebo Deníku fyzické inventury skladu. Následující tabulky popisují informace ve zprávách, které je třeba zadat do záhlaví a řádků v montážní zakázce.

#### Záhlaví

| Pole | Hodnota, kterou chcete zadat |
|---------|---------|
| Číslo zboží | Číslo nového zboží. |
| Množství | Množství v deníku fyzické inventury.<br> **NOTE:** Množství vypočítaná deníky fyzické inventury nezahrnují množství, která jsou na objednávkách, které ještě nebyly odeslány. |
| Kód varianty | Stejné jako v deníku fyzické inventury. |
| Kód lokace | Stejné jako v deníku fyzické inventury. |
| Kód měrné jednotky | Stejné jako v deníku fyzické inventury. |
| Kód přihrádky | Stejné jako v deníku fyzické inventury. |

#### Řádky

| Pole | Hodnota, kterou chcete zadat |
|---------|---------|
| Typ | Číslo |
| zboží | Číslo původního zboží. |
| Množství za | 1 |
| Kód varianty | Stejné jako v deníku fyzické inventury. |
| Kód lokace | Stejné jako v deníku fyzické inventury. |
| Kód měrné jednotky | Stejné jako v deníku fyzické inventury. |

> [!NOTE]
> Montážní zakázka může zpracovávat pouze jednu jednotku SKJ zboží najednou. Je nutné vytvořit montážní zakázku pro každou kombinaci SKJ, která má množství ve skladu.

> [!NOTE]
> V případě lokací skladu může být nutné vytvořit vyskladnění zboží před zaúčtováním montážní zakázky. Chcete-li to prozkoumat, zkontrolujte nastavení pro vyskladnění na stránce **Karta lokace**. Pro více informací navštivte [Nastavení zboží a lokací pro přímé zaskladnění a vyskladnění](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md).

### Zpracování množství zásob, která jsou přidělena poptávce

V ideálním případě by zásoby pro původní zboží měly po převodu skladových množství klesnout na nulu. Mohou však existovat nevyřízené objednávky, výkazy a deníky (viz tabulka níže), které stále vyžadují množství původního zboží. Množství může být také blokováno rezervací nebo sledováním zboží.

**Příklad**
áme 1000 kusů ne skladu, a 20 kusů je vyhrazeno pro prodejní objednávku, která ještě nebyla odeslána. V takovém případě se můžete rozhodnout ponechat si 20 kusů ve starém zboží, abyste mohli splnit nevyřízenou objednávku.

> [!NOTE]
> Existují funkční oblasti, které mohou ovlivnit množství, jak je uvedeno v tabulce níže, takže může být složité najít správné množství. Chcete-li být v bezpečí, pomocí výše uvedeného příkladu se můžete rozhodnout ponechat 100 ks. a převíst zbývajících 900 ks.  Dalším způsobem, jak to udělat, by bylo zpracovat doklady a deníky tak, aby zůstalo jen několik zvládnutelných. Další alternativou je převést celé množství do nového zboží a poté převést část zpět do původního zboží pomocí montážní zakázky.

V následující tabulce jsou uvedeny funkční oblasti, kde mohou být nevyřízená množství.

| Oblast | Kde hledat nevyřízená množství |
|---------|---------|
| Prodej | Prodejní doklady, včetně objednávek, vratek, faktur, nabídek, hromadných objednávek a dobropisů |
| Zásoby | Deníky zboží, rezervace, sledování zboží a sešit pevné ceny nákladů |
| Nákup | Nákupní doklady, včetně objednávek, vratek, faktur, nabídek, hromadných objednávek a dobropisů |
| Plánování | Sešit požadavků, plánovací sešit a plánování objednávek |
| Sklad | Objednávky transferu, dodávky ze skladu, deníky skladu a vyskladnění, zaskadnění a skladové pohyby, interní zaskladnění a vyskladnění a sešit vytvoření přihrádky |
| Montáž | Montážní doklady, včetně objednávek, vratek a hromadných objednávek |
| Projekty | Řádky plánování projektu a řádky deníku projektu |
| Služba | Servisní doklady a servisní smlouvy |
| Výroba | Výrobní zakázky (plánované, pevně plánované a vydané) |

### Zablování dalšího použití původního zboží

Pokud jsou zásoby pro původní zboží nulové, můžete zboží zablokovat, abyste zabránili jejímu použití v nových transakcích. Chcete-li zboží zablokovat, na stránce **Karta zboží** zapněte přepínač **Blokováno**. Pro více informací navštivte [Blokování položek z prodeje nebo nákupu](inventory-how-block-items.md).

## Shrnutí

Změna metody ocenění u zboží, které bylo použité v transakcích, je proces, nikoli standardní akce v [!INCLUDE[prod_short](includes/prod_short.md)]. Kroky popsané v tomto tématu můžete použít jako šablonu pro proces.

Proces může být časově náročný, protože existuje několik manuálních kroků. Pokud si však uděláte čas na jeho dokončení, minimalizujete dopad chyb na hlavní knihu.

Doporučujeme následující:

1. Vyhodnoťte proveditelnost procesu tím, že vezmete jedno, nebo možná několik, reprezentativních zboží v celém procesu.
2. Zvažte kontaktování zkušeného partnera, který vám může s procesem pomoci.

## Viz také

[Detaily návrhu: Metody ocenění](design-details-costing-methods.md)    
[Přehled](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]