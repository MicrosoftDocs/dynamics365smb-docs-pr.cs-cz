---
    title: Planning With or Without Locations | Microsoft Docs
    description: Planning with or without location codes on demand lines is important to understand.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Plánování s lokacemi nebo bez nich
Pokud jde o plánování s a bez kódu lokací na řádcích poptávky, systém plánování pracuje přímým způsobem, když:

- Řádky poptávky vždy nesou kódy lokace a systém plně používá skladové jednotky, včetně příslušného nastavení skladového místa.
- Linky poptávky nikdy nenesou kódy lokace a systém nepoužívá SKJ ani žádné umístění (viz poslední scénář níže).

Pokud však řádky poptávky někdy obsahují kódy lokací a jindy ne, bude systém plánování dodržovat určitá pravidla v závislosti na nastavení.

## Poptávka v lokaci
Když plánovací systém detekuje poptávku v lokaci (řádek s kódem lokace), bude se chovat různými způsoby v závislosti na 3 kritických hodnotách nastavení.

Během plánovacího běhu systém kontroluje postupně 3 hodnoty nastavení a podle toho plánuje:

1. Je zaškrtnuto políčko **Lokace nutná**?

   Pokud ano, pak:

2. Existuje pro položku skladová položka?

   Pokud ano, pak:

   Položka je naplánována podle parametrů plánování na kartě SKJ.

   Pokud ne, pak:

3. Obsahuje pole **Komponenty na lokaci** požadovaný kód lokace?

   Pokud ano, pak:

   Položka je plánována podle parametrů plánování na kartě zboží.

   Pokud ne, pak:

   Položka je plánována podle: Způsobu přiobjednání =  *Dávka pro dávku*, Včetně zásob =  *Ano*, všechny ostatní parametry plánování = Prázdné (Položky používající zásady  *Objednávky* budou nadále používat  *Objednávku*, jakož i další nastavení.)

> [!NOTE]
> Tato minimální alternativa pokrývá pouze přesnou poptávku. Všechny definované parametry plánování jsou ignorovány.

Podívejte se na varianty v níže uvedených scénářích.

## Poptávka na "prázdné skladové místo"
I když je zaškrtnuto políčko **Lokace nutná**, systém umožní vytvoření řádků poptávky bez kódu lokace – označované také jako *Prázdné* umístění. Jedná se o odchylku pro systém, protože má různé hodnoty nastavení vyladěné na práci s lokacemi (viz výše) a v důsledku toho plánovací modul nevytvoří řádek plánování pro takový řádek poptávky. Pokud není vyplněno pole **Lokace nutná**, ale existuje některá z hodnot nastavení lokace, pak je to také považováno za odchylku a plánovací systém bude reagovat výstupem "minimální alternativy":
Položka je naplánována podle: Způsob přiobjednání =  *Dávka pro dávku* ( *Objednávka* zůstává *Objednávkou)*, Včetně zásob =  *Ano*, pro všechny ostatní parametry = Prázdné.

Podívejte se na varianty ve scénářích nastavení níže.

### Nastavení 1:

- Lokace nutná = *Ano*
- SKJ je nastavena pro  *ČERVENÝ*
- Komponenta v lokaci =  *MODRÝ*

#### Případ 1.1: Poptávka je v lokaci  *ČERVENÝ*

Položka je plánována podle parametrů plánování na kartě SKJ (včetně možného převodu).

#### Případ 1.2: Poptávka je v lokaci  *MODRÝ*

Položka je plánována podle parametrů plánování na kartě zboží.

#### Případ 1.3: Poptávka je v lokaci *ZELENÝ*

Položka je plánována podle: Zásady přiobjednání =  *Dávka pro dávku* (*Objednávka* zůstává  *Objednávkou*), Včetně zásob =  *Ano*, všechny ostatní parametry plánování = Prázdné.

#### Případ 1.4: Poptávka je v lokaci  *PRÁZDNÝ*

Položka není naplánována, protože na řádku poptávky není definováno žádné místo.

### Nastavení 2:

- Lokace nutná = *Ano*
- Neexistuje žádná SKJ
- Komponenta v lokaci =  *MODRÝ*

#### Případ 2.1: Poptávka je v lokaci  *ČERVENÁ* 

Položka je plánována podle: Zásady přiobjednání =  *Dávka pro dávku* (*Objednávka* zůstává  *Objednávkou*), Včetně zásob =  *Ano*, všechny ostatní parametry plánování = Prázdné.

#### Případ 2.2: Poptávka je v lokaci  *MODRÁ*

Položka je plánována podle parametrů plánování na kartě zboží.

### Nastavení 3:

- Lokace nutná = *Ne*
- Neexistuje žádná SKJ
- Komponenta v lokaci =  *MODRÝ*

#### Případ 3.1: Poptávka je v lokaci  *ČERVENÁ* 

Položka je plánována podle: Zásady přiobjednání =  *Dávka pro dávku* (*Objednávka* zůstává  *Objednávkou*), Včetně zásob =  *Ano*, všechny ostatní parametry plánování = Prázdné.

#### Případ 3.2: Poptávka je v lokaci  *MODRÁ* 

Položka je plánována podle parametrů plánování na kartě zboží.

#### Případ 3.3: Poptávka je v lokaci  *BLANK*

Položka je plánována podle: Zásady přiobjednání =  *Dávka pro dávku* (*Objednávka* zůstává  *Objednávkou*), Včetně zásob =  *Ano*, všechny ostatní parametry plánování = Prázdné.

### Nastavení 4:

- Lokace nutná = *Ne*
- Neexistuje žádná SKJ
- Komponenta v umístění =  *PRÁZDNÉ*

#### Případ 4.1: Poptávka je v lokaci  *MODRÝ* 

Položka je plánována podle: Zásady přiobjednání =  *Dávka pro dávku* (*Objednávka* zůstává  *Objednávkou*), Včetně zásob =  *Ano*, všechny ostatní parametry plánování = Prázdné.

#### Případ 4.2: Poptávka je na lokaci  *PRÁZDNÉ* 

Položka je plánována podle parametrů plánování na kartě zboží.

Jak můžete vidět z posledního scénáře, jediným způsobem, jak získat správný výsledek pro řádek poptávky bez kódu lokace, je zakázat všechny hodnoty nastavení týkající se umístění. Podobně jediným způsobem, jak získat stabilní výsledky plánování pro poptávku v lokalitách, je použití skladových jednotek.

Proto pokud často plánujete poptávku v lokalitách, důrazně se doporučuje používat funkci Skladové jednotky.

## Viz také
[Plánování](production-planning.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)  
[Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
