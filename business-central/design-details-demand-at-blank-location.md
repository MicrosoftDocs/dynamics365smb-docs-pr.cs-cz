---
    title: Design Details - Demand and Supply | Microsoft Docs
    description: This topic introduces the concept of demand, which is the common term used for any kind of gross demand, such as a sales order and component need from a production order.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: design, demand, supply, inventory, planning
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Detaily návrhu: Popávka bez lokace
Když uživatel vytvoří požadavek, například řádek prodejní objednávky, program uživateli umožní někdy zadat kód lokace a jindy zase ne, tj. použít prázdné místo.

Pro poptávku, kdy není vyplněn kód lokace pracuje přímo, když:

- Řádky poptávky vždy obsahují kódy lokace a systém plně používá skladové jednotky, včetně příslušného nastavení lokace.
- Řádky poptávky nikdy nenesou kódy lokací a systém nepoužívá skladové jednotky ani žádné nastavení skladového místa (viz poslední scénář v následující části).

Pokud však poptávka někdy obsahuje kódy lokací a jindy zase ne, systém plánování bude dodržovat určitá pravidla v závislosti na nastavení.

## Poptávka v lokaci
Když plánovací systém detekuje poptávku v lokaci, bude se chovat různými způsoby v závislosti na třech kritických hodnotách nastavení. Během plánování systém kontroluje tři hodnoty nastavení a podle toho plánuje.

1. Je políčko **Lokace nutná** zaškrtnuté?

   Pokud ano, tak:

2. Existuje karta skladové jednotky pro vybrané zboží?

   Pokud ano, tak:

   Položka je plánována podle parametrů plánování na kartě skladové jednotky.

   Pokud ne, pak:

3. Obsahují Komponenty v poli lokace požadovaný kód lokace?

Pokud ano, tak:

Zboží je plánováno podle parametrů plánování na kartě zboží.

Pokud ne, pak:

Zboží je plánováno podle: Způsob přiobjednání = Dávka-pro-Dávku, Včetně zásob = Ano, všechny ostatní parametry plánování = Prázdný, položky využívající Způsoby přiobjednání = Objednávka zůstane pomocí objednávky spolu s ostatními nastaveními.

> [!NOTE]
> Výjimečné nastavení plánování, které je výstupem jako poslední reakce ve výše uvedeném kroku 3, je dále označováno jako „minimální alternativa“. Toto nastavení plánování pokrývá pouze přesnou poptávku a všechny ostatní parametry plánování jsou ignorovány.

Informace o variantách této logiky plánování naleznete níže, v části Scénáře.

## Poptávka bez lokace
I když je vybráno pole **Lokace nutná** program umožní vytvoření řádků poptávky bez kódu lokace, také označovaného jako bez lokace. Jedná se o odchylku pro systém, protože má různé hodnoty nastavení vyladěné na práci s lokacemi (viz výše) a v důsledku toho plánovací modul nevytvoří řádek plánování pro takový řádek poptávky.

Pokud není vybranáno pole **Lokace nutná** ale existují některé z hodnot nastavení lokace, je také považováno za odchylku a plánovací systém bude reagovat pomocí "minimální alternativy": Položka je plánována podle: Způsob přiobjednání = Dávka-pro-Dávku (Objednávka zůstává objednávkou), Včetně zásob = Ano, všechny ostatní parametry plánovánív = Prázdný.

## Scénáře
Následující scénáře popisují varianty poptávky v prázdném umístění a způsob, jakým systém plánování překládá na "minimální alternativu".

### Nastavení 1:
Lokace nutná = Ano

SKJ je nastavené pro ČERVENÝ

Komponenty na lokaci = MODYRÝ

#### Příklad 1.1: Poptávka v lakaci ČERVENÝ
Položka je plánována podle parametrů plánování na kartě skladové jednotky.

#### Príklad 1.2: Poptávka v lokaci MODRÝ
Zboží je plánována podle: Způsob přiobjednání = Dávka-pro-Dávku, Včetně zásob = Ano, všechny ostatní parametry plánování = Prázdné

#### Příklad 1.3: Poptávka je lokaci ZELENÝ
Zboží je plánována podle: Způsob přiobjednání = Dávka-pro-Dávku, Včetně zásob = Ano, všechny ostatní parametry plánování = Prázdné

#### Příklad 1.4: Poptávka bez lokace
Zboží není plánována, protože na řádku poptávky není definováno žádné umístění.

### Nastavení 2:
Lokace nutná = Ano

Neexistují SKJ

Komponenty na lokaci = MODYRÝ

#### Příklad 2.1: Poptávka v lakaci ČERVENÝ
Zboží je plánována podle: Způsob přiobjednání = Dávka-pro-Dávku, Včetně zásob = Ano, všechny ostatní parametry plánování = Prázdné

#### Príklad 2.2: Poptávka v lokaci MODRÝ
Zboží je plánováno podle parametrů plánování na kartě zboží.

### Nastavení 3:
Lokace nutná = Ne

Neexistují SKJ

Komponenty na lokaci = MODYRÝ

#### Příklad 3.1: Poptávka v lakaci ČERVENÝ
Zboží je plánována podle: Způsob přiobjednání = Dávka-pro-Dávku, Včetně zásob = Ano, všechny ostatní parametry plánování = Prázdné

#### Príklad 3.2: Poptávka v lokaci MODRÝ
Zboží je plánováno podle parametrů plánování na kartě zboží.

#### Příklad 3.4: Poptávka bez lokace
Zboží je plánována podle: Způsob přiobjednání = Dávka-pro-Dávku, Včetně zásob = Ano, všechny ostatní parametry plánování = Prázdné

### Nastavení 4:
Lokace nutná = Ne

Neexistují SKJ

Komponenty na lokaci = PRÁZDNÝ

#### Príklad 4.2: Poptávka v lokaci MODRÝ
Zboží je plánována podle: Způsob přiobjednání = Dávka-pro-Dávku, Včetně zásob = Ano, všechny ostatní parametry plánování = Prázdné

#### Příklad 4.4: Poptávka bez lokace
Zboží je plánováno podle parametrů plánování na kartě zboží.

Jak je znázorněno v posledním scénáři, jediný způsob, jak získat správný výsledek pro řádek poptávky bez kódu lokace, je zakázat všechny hodnoty nastavení vztahující se k umístění. Podobně jediný způsob, jak získat stabilní výsledky plánování pro poptávku v lokacích, je použití skladových jednotek. Proto pokud společnosti často plánují poptávku na lokacích, důrazně se doporučuje používat skladové jednotky.

## Viz také
[Detaily návrhu: Vyvažování poptávky a nabídky](design-details-balancing-demand-and-supply.md)   
[Detaily návrhu: Koncept plánovacího systému](design-details-central-concepts-of-the-planning-system.md)   
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)
