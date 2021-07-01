---
    title: Handling Lot Sizes | Microsoft Docs
    description: This topic describes different ways to handle lot sizes. 
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2021
    ms.author: bholtorf

---

# Manipulace s velikostmi šarží ve výrobě
Pokud jde o množství, počet zboží, které ve výrobě vyrobíte, tak to nemusí odpovídat tomu, jak je prodáte. Můžete například vyrobit stovky položek v jedné sérii, ale prodávat každou položku zvlášť. Při konfiguraci TNG postupů a kusovníků je třeba vzít v úvahu několik nuancí týkajících se velikosti šarží. Toto téma popisuje, jaký vliv má velikost šarže na výpočet nákladů a plánování zdrojů.

## Měrné jednotky ve výrobním kusovníku
Přestože pro položku zadáte základní měrnou jednotku, může kusovník pro hotový výrobek používat jinou MJ. Například základní MJ pro položku může být KS, ale v kusovníku může být uvedena paleta nebo tuna. To se hodí v případě, že vaše stroje nebo surové komponenty určují objem. Například byste pravděpodobně nechtěli péct jeden koláček, protože je obtížné použít pouze část vejce. Místo toho upečete více koláčků, abyste snížili množství odpadu. Další informace naleznete v tématu [Vytváření výrobních kusovníků](production-how-to-create-production-boms.md).

## Velikost šarže na řádcích TNG postupu
Z hlediska TNG postupu můžete zadat velikost šarže na řádcích TNG postupu tak, aby odpovídala kapacitě strojů, které dané položky vyrábějí. Doba výroby pomocí TNG postupu se zkracuje úměrně velikosti dávky.

To funguje dobře, pokud je množství na výrobní objednávce faktorem velikosti šarže TNG postupu. Pokud se vám například na plech vejde 10 koláčků, měli byste jich upéct 10, 20, 30,... nikoli 5 ani 15.  Pokud se jedná o velké množství, je to mnohem menší problém.

Velikost šarže je také oblíbená ve výrobních prostředích, kde se výstup měří jako množství, které můžete vyrobit během pevného času. Příklad: Pokud je objem za 9 hodinovou směnu 25000 kubíků, můžete nastavit dobu provozu na 9 hodin a velikost dávky na 25000.
Množství výrobní zakázky se stává méně důležitým, protože na výrobní zakázce se doba chodu vypočítá jako doba chodu/velikost šarže, čímž se získá doba chodu na kus.

> [!NOTE]
> Hodnota zadaná v poli Velikost šarže nemá vliv na čas zadaný v poli **Doba seřízení** řádku TNG postupu. Nastavení se provede pouze jednou, i když existuje několik šarží. Například proto, abyste pro druhou várku koláčků nemuseli zahřívat troubu. Pro více informací navštivte [Vytvoření TNG postupů](production-how-to-create-routings.md).

## Velikosti šarží pro zboží a skladové jednotky
Velikosti šarží definované pro TNG postupy nejsou stejné jako velikosti šarží pro zboží nebo skladové jednotky. Tyto hodnoty se používají k jinému účelu a nemají vliv na výrobní kapacitu.

## Velikost šarže na zboží a na skladových jednotkách
Pro zboží a skladové jednotky mají velikosti šarží následující vliv na výpočet nákladů a plánování dodávek:

* Pokud pro výpočet standardních nákladů povolíte **Náklady vč.seřízení** na stránce **Nastavení výroby**, náklady na nastavení se přičtou ke standardním nákladům. Pokud zadáte velikost dávky, náklady na nastavení operace TNG postupu se sníží podle velikosti dávky. Pokud je například velikost šarže definovaná na kartě zboží na 10 a ohřev trouby trvá 15 minut, budou náklady na palivo přiřazeny k 10 koláčkům jako zhruba 1,5 minuty.

> [!NOTE]
> Z pohledu standardních nákladů a přidělování kapacity se s náklady na zřízení pracuje odlišně. Pokud vyrobené množství neodpovídá velikosti šarže definované na kartě zboží, vede to k odchylkám. Další informace naleznete v tématu [Správanákladů na zásoby](finance-manage-inventory-costs.md). <!--not sure that I got this part right seems to repeat the first example.-->

Pro plánování dodávek pracuje nastavení velikosti šarže u zboží s  **Výchozí doba prodlevy** na **stránce Nastavení výroby**. [!INCLUDE[prod_short](includes/prod_short.md)] bude ignorovat změny v poptávce, které jsou nižší výchozí doba prodlevy a nebude vytvářet návrhy plánování. Například v poli Výchozí doba prodlevy je uvedeno 15 a máme výrobní objednávku na 20 koláčků pro 20 hostů, ale jeden host se nemůže zúčastnit. [!INCLUDE[prod_short](includes/prod_short.md)] bude ignorovat jediného chybějícího hosta, protože je to pouze 10% velikosti dávky 10 definované na položce. Pokud však dva hosté nemohou přijít, [!INCLUDE[prod_short](includes/prod_short.md)] navrhne, abychom snížili množství objednávky, protože dva hosté představují 20% velikosti šarže. Další informace o plánování naleznete v tématu [Plánování](production-planning.md).

## Viz také
[Vytváření výrobních kusovníků](production-how-to-create-production-boms.md)  
[Práce s měrnými jednotkami výrobní dávky](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Vytváření TNG postupů](production-how-to-create-routings.md)  
[Přehled nákladů na zásoby](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]