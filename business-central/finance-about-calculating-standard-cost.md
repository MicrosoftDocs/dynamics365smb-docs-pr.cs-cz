---
    title: About Calculating Standard Cost | Microsoft Docs
    description: A standard cost system determines inventory unit cost based on some reasonable historical or expected cost. Studies of past and estimated future cost data can then provide the basis for standard costs.
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
# Výpočet pevné pořizovací ceny
Mnoho výrobních společností volí jako základ oceňování pevnou pořizovací cenu. To platí i pro společnosti, které provádějí výrobu, jako je montáž a skládaní souprav. Systém pevné pořizovací ceny určuje jednotkové náklady na základě některých přiměřených historických nebo očekávaných nákladů. Základem pro pevnou pořizovací cenu pak mohou být studie údajů o minulých a odhadovaných budoucích nákladech. Tyto náklady jsou zmrazeny, dokud nebude přijato rozhodnutí o jejich změně. Skutečné náklady na výrobu produktu se mohou lišit od odhadované pevné pořizovací ceny. Pro kontrolu jsou skutečné náklady porovnány s pevnou pořizovací cenou na konkrétní zboží a jsou identifikovány a analyzovány rozdíly nebo *odchylky*.

U zboží, které se doplňují nákupem, montáží a výrobou, lze zachovat pevnou pořizovací cenu. Pro každou metodu doplnění se pevná pořizovací cena může skládat z následujících prvků.

| Systém doplnění | Prvky pevné pořizovací ceny |
|--------------------------|----------------------------|  
| **Nákup** | Přímé náklady na materiál a režijní náklady na materiál, pokud jsou vyžadovány. |
| **Montáž** | Přímé náklady na materiál, přímé nebo fixní pracovní náklady a režijní náklady. |
| **Výrobní  zakázka** | Přímé náklady na materiál, mzdové náklady, náklady na subdodavatele a režijní náklady. |

## Nastavení pevných pořizovacích cen
Vzhledem k tomu, že pevná pořizovací cena na vyrobené nebo sestavené zboží se může skládat z více prvků nákladů, včetně materiálu, kapacity (práce) a přímých a režijních nákladů subdodavatele, musí být pro každý z těchto prvků stanovena pevná pořizovací cena.

Úkolem účetnictví pro společnost zpracovávající zboží pomocí pevné pořizovací ceny je:

- Odhadněte pevnou pořizovací cenu na hotové zboží a nastavte ji na kartě zboží.
- Zaznamenejte a přidělte skutečné náklady na klíčové prvky nákladů a zohledněte odchylky.

Pro určení přímých nákladů na hotové zboží musí být všechny náklady na součásti sečteny. Sestavené nebo vyrobené zboží může zahrnovat podsestavy, které jsou také sestaveny z více komponent.

Následující klíčové prvky nákladů tvoří celkové přímé náklady na hotové zpracované zboží:

- Náklady na materiál.
- Náklady na kapacitu.
- Náklady na subdodávky pouze pro vyráběné zboží.

### Náklady na materiál
Náklady na materiál jsou náklady spojené s podsestavami a nakoupenými surovinami. Jednotkové náklady na materiál se mohou skládat z přímých a nepřímých nákladových prvků.

- Přímé náklady na materiál představují fakturovanou částku za nakoupené suroviny nebo náklady na zpracování podsestavy.
- Nepřímé náklady na materiál, nebo *režijní náklady*, mohou představovat prvky, jako jsou účetní náklady na sklad pro hotové zboží po jejím vyrobení.

Nastavení nákladů na materiál pro nakoupené zboží, které ovlivňuje přímé a nepřímé náklady, závisí na metodě ocenění, kterou jste vybrali pro zadané zboží. Na kartě zboží nastavíte informace o nákladech pro každou metodu ocenění. Pro více informací navštivte [Registrace nového zboží](inventory-how-register-new-items.md).

Cena zmetků (pouze výroba) je dalším faktorem, který je třeba vzít v úvahu při výpočtu celkových nákladů na materiál. Pokud je určité množství suroviny vyřazeno při sestavení nebo výrobě zboží, obvykle to způsobuje zvýšení množství součástí, které jsou nutné k výrobě tohoto zboží. To zvyšuje náklady na materiál na součásti, které jsou spotřebovány při výrobě nadřazeného zboží. Můžete nastavit náklady na zmetky pro materiál na produkčním kusovníku nebo na TNG.

Náklady na materiál na vyrobené zboží lze znázornit dvěma způsoby, které odpovídají následujícím základům pro výpočet nákladů.

| Základ výpočtu nákladů | Výpočet nákladů na materiál |
|----------------------------|-------------------------------|  
| Jedna úroveň | Vyrobené zboží se rovná celkovým nákladům na všechno zakoupené nebo sestavené zboží na produkčním kusovníku tohoto zboží. |
| Více úrovní | Vyrobené zboží je součtem nákladů na materiál pro všechny podsestavy kusovníku a nákladů na všechno zakoupené zboží na výrobním kusovníku tohoto zboží. |

### Náklady na kapacitu
Náklady na kapacitu jsou náklady spojené s interními náklady na práci a stroje. Tyto náklady musíte nastavit pro každý zdroj (ve správě montáže) a pracoviště nebo strojní centrum na TNG (ve výrobě). Stejně jako u materiálů můžete identifikovat přímé i nepřímé prvky nákladů na kapacitu. Například přímými náklady na pracovní centrum může být stanovená prodejní sazba za provedení určité funkce. Nepřímé náklady na pracovní středisko mohou představovat některé obecné výrobní náklady, jako je osvětlení, topení atd. Stejně jako u nákladů na materiál můžete vyjádřit režii kapacity jako procento nepřímých nákladů nebo pevnou režijní sazbu.

Nastavení nákladů na kapacitu sestaveného zboží se skládá z následujících prvků:

- Přímé a nepřímé jednotkové náklady na zdroj.
- Typ použití fixního nebo přímého zdroje.

Nastavení kapacitních nákladů vyrobeného zboží se skládá z následujících prvků:

- Přímé a nepřímé jednotkové náklady na stroj nebo pracovní středisko.
- Nastavení času a velikosti dávky.

Chcete-li vypočítat standardní náklady na kapacitu, musíte stanovit standardní časové sazby, které jsou nutné k provádění operací na strojových a pracovních centrech. Celková doba dokončení operace se obvykle skládá z nastavení, doby běhu a čekání a času přesunu.

Sazby nastavujete pro každý typ času pro každý stroj nebo pracovní centrum na individuálním TNG.

> [!NOTE]
> Zatímco pro každé vyrobené zboží platí časy běhu, pro každou šarži platí časy nastavení. Proto je nutné nastavit pro každou operaci nad velikosti dávky dobu TNG postupu. Velikost dávky určíte v odpovídajícím poli na záložce **Objednávání** na kartě zboží.

Chcete-li zadat čas nastavení pro TNG pro plánování, ale nezahrnout tyto náklady do výpočtu pevné pořizovací ceny, zrušte zaškrtnutí políčka **Náklady vč. seřízení** na stránce **Nastavení výroby**.

Na jednoúrovňovém základě se jedná o pracovní náklady, které jsou nutné k výrobě dokončeného zboží a jsou určeny v TNG postupu vyráběného zboží. Na víceúrovňové úrovni se jedná o náklady na kapacitu, které jsou určeny pro každé jednotlivě vyrobené zboží, které je součástí kusovníku nadřazeného zboží.

### Náklady na subdodavatele
Náklady na subdodavatele jsou náklady spojené se službami, které jsou poskytovány externími prodejci nebo subdodavateli společnosti. Podobně jako u materiálu a kapacity mohou náklady na subdodavatele zahrnovat přímé i režijní částky. Přímé náklady na subdodavatele představují skutečný poplatek za každou jednotku poskytovaných služeb. Například režijní náklady na subdodavatele mohou představovat náklady na dopravu a manipulaci, které společnosti vzniknou v rámci subdodavatelské objednávky.

Protože subdodávka je outsourcovaná kapacita, nastavujete náklady na přímé i nepřímé subdodavatelské služby na kartě pracovního centra, která představuje subdodavatelskou operaci.

## Aktualizace pevné pořizovací ceny
Chcete-li aktualizovat nebo vypočítat pevnou pořizovací cenu dokončeného zboží, použijte funkci z karty zboží.

Proces aktualizace nebo výpočtu pevné pořizovací ceny se obvykle skládá z následujících úkolů:

1. Aktualizace nákladů na úrovni komponenty a kapacity. Pro více informací navštivte dávkovou úlohu **Navrhnout pevnou cenu zboží** a **Navrhnout pevnou pořizovací cenu kapacity**.
2. Konsolidace a zahrnutí nákladů na komponenty a kapacity pro výpočet celkových montážních nebo výrobních nákladů na položky. Pro více informací navštivte [Výpočet pevné pořizovací ceny na zboží montáže](inventory-how-work-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).
3. Implementace pevné pořizovací ceny, která je zadána při spuštění předchozích dávkových úloh. Pevná pořizovací cena se projeví až po jejich zavedení. Pro více informací navštivte dávkovou úlohu **Provést změnu pevné ceny**.
4. Provedení změn k aktualizaci pole **Jednotková cena** na kartě zboží a provedení přecenění skladu. Pro více informací navštivte [Přeceňování zásob](inventory-how-revalue-inventory.md).

## Viz také
[Detaily návrhu: Metody ocenění](design-details-costing-methods.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)  
[Aktualizace standardních nákladů](finance-how-to-update-standard-costs.md)  
[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)
