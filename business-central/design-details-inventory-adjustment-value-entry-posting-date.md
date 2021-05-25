---
title: Posting date on value entries
description: Learn how the Adjust Cost - Item Entries batch job identifies and assigns a posting date to the value entries that the batch job is about to create.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 10/01/2020
ms.author: edupont

---
# Detaily návrhu: Zúčtovací datum adjustace položky ocenění
Tento článek poskytuje pokyny pro uživatele funkce Zásoby a ocenění v [!INCLUDE[prod_short](includes/prod_short.md)]. Článek poskytuje pokyny, jak dávková úloha **Adjustace nákladů položek zboží** identifikuje a přiřadí zúčtovací datum položkám ocenění, které se dávková úloha chystá vytvořit.

Nejprve je zkontrolován koncept procesu, jak dávková úloha identifikuje a přiřadí Datum zaúčtování k položce ocenění, která má být vytvořena. Poté jsou sdíleny některé scénáře, se kterými se v týmu podpory čas od času setkáme, a nakonec je zde shrnutí konceptů použitých od verze 3.0.

## Koncept
Od verze 5.0 přiřadí dávková úloha **Adjustace nákladů položek zboží** datum zaúčtování hodnotové položce, kterou se chystá vytvořit v následujících krocích:

1. Zpočátku je datum zaúčtování položky, která má být vytvořena, stejné datum jako položka, která se upravuje.

2. Zúčtovací datum je ověřeno podle skladových období a/nebo nastavení financí.

3. Přiřazení data zaúčtování; Pokud počáteční datum zaúčtování není v povoleném rozsahu data zaúčtování, přiřadí dávková úloha povolené datum zaúčtování buď z nastavení financí, nebo z období zásob. Pokud jsou definována skladová období i povolená zúčtovací data v nastavení financí, bude pozdější datum obou období přiřazeno k Adjustaci položky ocenění.

Podívejme se na tento proces více v praxi. Předpokládejme, že máme položku zboží prodeje. Zboží bylo odesláno 5. září 2013 a následující den bylo fakturováno.

![Stav položek zboží ve scénáři](media/helene/TechArticleAdjustcost1.png "Stav položek zboží ve scénáři")

Níže první položka ocenění (379) představuje dodávku a nese stejné datum zaúčtování jako nadřazená položka zboží.

Druhá položka ocenění (381) představuje fakturu.

Třetí položka ocenění (391) je adjustace fakturace položky ocenění (381)

![Stav položek ocenění ve scénáři](media/helene/TechArticleAdjustcost2.png "Stav položek ocenění ve scénáři")

Krok 1: Adjustace položky ocenění, která má být vytvořena, má přiřazeno stejné datum zaúčtování jako položka, kterou upravuje, ilustrovaná výše položkou ocenění 391.

Krok 2: Ověření počátečního přiřazeného data zaúčtování.

Dávková úloha **Adjustace nákladů položek zboží** určuje, zda je počáteční datum zaúčtování adjustace položky ocenění v povoleném rozsahu období účtování na základě období zásob a/nebo nastavení financí.

Podívejme se na výše uvedený prodej přidáním nastavení povolených rozsahů zúčtovacího data.

Skladová období:

![Skladová období ve scénáři](media/helene/TechArticleAdjustcost3.png "Skladová období ve scénáři")

První povolené zúčtovací datum je první den v prvním otevřeném období. 1. září 2013.

Nastavení financí

![Nastavení financí ve scénáři](media/helene/TechArticleAdjustcost4.png "Nastavení financí ve scénáři")

První povolené zúčtovací datum je datum uvedené v poli Povolit účto od: 10. září 2013.

Pokud jsou definována skladová období i povolená zúčtovací data v nastavení financí, bude pozdější datum těchto dvou období definovat povolenou oblast zúčtovacího data.

Krok 3: Přiřazení povoleného zúčtovacího data;

Počáteční přiřazené zúčtovací datum bylo 6. září, jak je znázorněno v kroku 1. Ve 2. kroku však dávková úloha (Adjustace nákladů položek zboží) identifikuje, že nejstarší povolené datum zaúčtování je 10. září, a tím přiřadí 10. září k adjustované položke ocenění.

![Stav položek ocenění ve scénáři 2](media/helene/TechArticleAdjustcost5.png "Stav položek ocenění ve scénáři 2")

Nyní jsme zkontrolovali koncept přiřazení zúčtovacího data položkám ocenění vytvořeným dávkovou úlohou Adjustace nákladů položek zboží.

Pojďme pokračovat v kontrole některých scénářů, na které v týmu podpory čas od času narazíme ve vztahu k přiřazeným datům zúčtování v dávkové úloze Adjustace nákladů položek zboží a v souvisejícím nastavení.

## Scénáře

### Scénář I: „Zúčtovací datum není ve vašem rozsahu povolených zúčtovacích dat ...“
Jedná se o scénář, kdy se uživateli zobrazí zmíněná chybová zpráva při spuštění dávkové úlohy Adjustace nákladů položek zboží.

V předchozí části, popisující koncept přiřazení zúčtovacího data, je záměrem dávkové úlohy Adjustace nákladů položek zboží vytvořit položku ocenění se zúčtovacím datem 10. září.

![Chybové hlášení o zúčtováním datu](media/helene/TechArticleAdjustcost6.png "Chybové hlášení o zúčtováním datu")

Sledujeme nastavení uživatele:

![Nastavení povolených zúčtovacích dat uživatelem](media/helene/TechArticleAdjustcost7.png "Nastavení povolených zúčtovacích dat uživatelem")

Uživatel má v tomto případě povolené rozsahy zúčtovacího data od 11. září do 30. září, a proto není povoleno zaúčtovat adjustaci položky ocenění se zúčtovacím datem 10. září.

![Přehled nastavení zúčtovacího data](media/helene/TechArticleAdjustcost8.png "Přehled nastavení zúčtovacího data")

Článek znalostní báze [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) popisuje další scénáře související s uvedenou chybovou zprávou.

### Scénář II: Zaúčtování data na adjustaci položky ocenění versus zúčtovací datum na položce způsobující adjustaci, jako je přecenění nebo poplatek za zboží.

### Scénář přecenění:
Předpoklady:

Nastavení zásob:

- Automatické účtování nákladů=Ano

- Automatická adjustace nákladů=Vždy

- Typ výpočtu prům.poř. ceny=Zboží

- Období průměrných nákladů=Den

Nastavení financí

- Povolit účto od = 1. leden 2014

- Povolit účto do = prázdné

Nastavení uživatelů:

- Povolit účto od = 1. prosinec 2013.

- Povolit účto do = prázdné

##### Testování scénáře

1. Vytvoření zboží TEST:

   Základní měrná jednotka = KS

   Metoda ocenění = Průměrná

   Vyberte volitelné účto skupiny.

2. Otevřete Deník zboží, vytvořte a zaúčtujte řádek následujícím způsobem:

   Zúčtovací datum = 15. prosinec 2013

   Zboží = TEST

   Typ položky = Nákup

   Množství = 100

   Jednotková cena = 10

3. Otevřete Deník zboží, vytvořte a zaúčtujte řádek následujícím způsobem:

   Datum = 20. prosinec 2013

   Zboží = TEST

   Typ položky = Výdej

   Množství = 2

4. Otevřete Deník zboží, vytvořte a zaúčtujte řádek následujícím způsobem:

   Datum = 15. leden 2014

   Zboží = TEST

   Typ položky = Výdej

   Množství = 3

5. Otevřete Deník přecenění, vytvořte a zaúčtujte řádek následujícím způsobem:

   Zboží = TEST

   Vyrovnává položku = vyberte položku nákupu zaúčtovanou v kroku 2. Datum zaúčtování přecenění bude stejné jako položka, kterou upraví.

   Pořizovací cena (přeceněná) = 40

Byly zaúčtovány následující položky zboží a položky ocenění:

![Přehled výsledných položek zboží a položek ocenění 1](media/helene/TechArticleAdjustcost9.png "Přehled výsledných položek zboží a položek ocenění 1")

![Přehled výsledných položek zboží a položek ocenění 2](media/helene/TechArticleAdjustcost10.png "Přehled výsledných položek zboží a položek ocenění 2")

Dávková úloha Adjustace nákladů položek zboží rozpoznala změnu nákladů a upravila záporné úpravy.

**Kontrola zúčtovacího data u vytvořených adjustovaných položek ocenění:** Nejbližší povolené zúčtovací datum, ke kterému se dávková úloha Adjustace nákladů položek zboží musí vztahovat, je 1. ledna 2014, jak je uvedeno v nastavení financí.

**Záporná úprava v kroku 3:** přiřazené datum zaúčtování je 1. ledna, poskytnuté nastavením financí. Datum zaúčtování položky ocenění v rozsahu adjustace je 20. prosinec 2013. Podle nastavení financí datum není v povoleném rozsahu období účtování. Proto je adjustaci položky ocenění přiřazeno datum zaúčtování uvedené v poli Povolit účto od v nastavení financí.

**Záporná úprava v kroku 4:** přiřazené zúčtovací datum je 15. ledna. Položka ocenění v rozsahu adjustace má zúčtovací datum 15. ledna, které je v povoleném rozsahu zúčtovacího data podle nastavení financí.

Adjustace provedené pro negativní úpravu v kroku 3 způsobí diskusi. Příznivé datum zaúčtování pro adjustaci položky ocenění by bylo 20. prosince nebo alespoň do konce prosince, protože v prosinci bylo zaúčtováno přecenění způsobující změnu NNPZ.

Chcete-li v prosinci dosáhnout adjustaci záporné úpravy v kroku 3, musí být v nastavení financí, pole Povolit účto od nastaveno na datum v prosinci.

**Závěr:**

Se zkušenostmi z tohoto scénáře, s ohledem na nejvhodnější nastavení povoleného rozsahu zúčtovacího data pro společnost, může být užitečné následující: Pokud je povoleno zaúčtování změn hodnoty zásob v období prosinec, v tomto případě by mělo být nastavení, které společnost používá pro povolené rozsahy zúčtováního dat, v souladu s tímto rozhodnutím. Nastavení pole Povolit účto od v Nastavení financí s uvedením 1. prosince by umožnilo předání přehodnocení provedené v prosinci ovlivněným výstupním položkám ve stejném období.

Skupiny uživatelů, které nemají povoleno účtovat v prosinci, ale v lednu, což bylo pravděpodobně zamýšleno v tomto scénáři jako omezené nastavením financí, by měly být místo toho řešeno prostřednictvím nastavení uživatele.

### Scénář účtování poplatku za zboží:
Předpoklady:

Nastavení zásob:

- Automatické účtování nákladů=Ano

- Automatická adjustace nákladů=Vždy

- Typ výpočtu prům.poř. ceny=zboží

- Období průměrných nákladů=Den

Nastavení financí

- Povolit účto od = 1. prosinec 2013.

- Povolit účto do = prázdné

Nastavení uživatelů:

- Povolit účto od = 1. prosinec 2013.

- Povolit účto do = prázdné

##### Testování scénáře

1. Vytvořte poplatek za zboží:

   Základní měrná jednotka = KS

   Metoda ocenění = Průměrná

   Vyberte volitelné účto skupiny.

2. Vytvořte novou nákupní objednávku.

   Nákup od dodavatele: 10000

   Zúčtovací datum = 15. prosinec 2013

   Číslo faktury dodavatele: 1234

   Na řádku nákupní objednávky:

   Zboží = POPLATEK

   Množství = 1

   Nákupní cena = 100

   Zaúčtujte příjem a fakturu.

3. Vytvořit novou prodejní objednávku:

   Zákazník-číslo: 10000

   Zúčtovací datum = 16. prosinec 2013

   Na řádku prodejní objednávky:

   Zboží = POPLATEK

   Množství = 1

   Jednotková cena = 135

   Zaúčtujte dodávku a fakturu.

4. Nastavení financí

   Povolit účto od = 1. leden 2014

   Povolit účto do = prázdné

5. Vytvořte novou nákupní objednávku.

   Nákup od dodavatele: 10000

   Zúčtovací datum = 2. leden 2014

   Číslo faktury dodavatele: 2345

   Na řádku nákupní objednávky:

   Poplatek za zboží = JB-PŘEPRAVA

   Množství = 1

   Nákupní cena = 3

   Přiřaďte poplatek za zboží k nákupní příjemke z kroku 2.

   Zaúčtujte příjem a fakturu.

   ![Přehled výsledných položek zboží a položek ocenění 3](media/helene/TechArticleAdjustcost11.png "Přehled výsledných položek zboží a položek ocenění 3")

6. V pracovní den 3. ledna dorazí nákupní faktura obsahující dodatečný poplatek za zboží provedený v kroku 2. Tato faktura má datum dokladu 30. prosince 2013 a je proto zaúčtována s datem zaúčtování 30. prosince 2013.

   Vytvořte novou nákupní objednávku.

   Nákup od dodavatele: 10000

   Zúčtovací datum = 30. prosinec 2013

   Číslo faktury dodavatele: 3456

   Na řádku nákupní objednávky:

   Poplatek za zboží = JB-PŘEPRAVA

   Množství = 1

   Nákupní cena = 2

   Přiřaďte poplatek za zboží k nákupní příjemke z kroku 2.

   Zaúčtujte příjem a fakturu.

![Přehled výsledných položek zboží a položek ocenění 4](media/helene/TechArticleAdjustcost12.png "Přehled výsledných položek zboží a položek ocenění 4")

Zpráva o ocenění zásob se vytiskne k datu 31. prosince 2013

![Obsah sestavy Hodnota zásob](media/helene/TechArticleAdjustcost13.png "Obsah sestavy Hodnota zásob")

**Shrnutí scénáře:**

Popsaný scénář končí zprávou Hodnoty zásob ukazující Množství = 0, zatímco Hodnota = 2. Poplatek za zboží zaúčtovaný v kroku 11 je součástí hodnoty zvýšení zásob v prosinci, zatímco pokles zásob ve stejném období není ovlivněn.

Nastavení financí, ve kterém bylo uvedeno Povolit účto od 1. ledna, byla dobrá věc pro první poplatek za zboží. Ve stejném období byly zaznamenány náklady na zvýšení i snížení zásob. U druhého poplatku za zboží však nastavení financí způsobí, že změna v NNPZ bude rozpoznána v období po.

**Závěr:**

Pro firmy není příliš dobré, aby sestava Hodnota zásob demonstrovala množství = 0, zatímco hodnota <> 0. V tomto případě je také obtížnější vyjádřit optimální nastavení, protože nákupní faktury přicházejí ve stejný den, ale řeší různá období nebo dokonce fiskální roky. Přechod do nového fiskálního roku obvykle vyžaduje určité plánování a v rámci toho je třeba vzít v úvahu pohled na proces Adjustace nákladů položek zboží rozpoznávající NNPZ.

V tomto scénáři by jednou z možností mohlo být nastavení financí, konkrétně pole Povolit účto od na datum v prosinci o několik dní později a odložit zaúčtování prvního poplatku za zboží, aby bylo možné zaúčtovat všechny náklady za předchozí období/fiskální rok, se spuštěním dávkové úlohy Adjustace nákladů položek zboží a poté přesunout povolené zúčtovací datum do nového období/fiskálního roku. První poplatek za zboží se zúčtovacím datem 2. ledna by pak mohl být zaúčtován.

## Historie dávkové úlohy Adjustace nákladů položek zboží
Níže je uveden souhrn konceptu přiřazení zúčtovacího data adjustace položek ocenění dávkovou úlohou Adjustace nákladů položek zboží od verze 3.0.

### Od verze 3.0..3.70.A
Ve formuláři požadavku dávkové úlohy Adjustace nákladů položek zboží existuje zúčtovací datum, které má uživatel zadat. Dávková úloha prochází všemi nezbytnými změnami a vytváří položky cenění s datem zaúčtování zadaným ve formuláři žádosti. Doporučené zúčtovací datum je dnešní datum.

### Verze 3.70.B..4.0
Ve formuláři žádosti u dávkové úlohy Adjustace nákladů položek zboží je datum zaúčtování vstupu, které má uživatel zadat, v uzavřeném období. Dávková úloha proběhne všemi nezbytnými změnami a vytvoří položky ocenění s datem zaúčtování  nadřazené položky zboží (datum dodávky prodeje). Pokud zúčtovací datum nadřazené položky zboží není v povoleném rozsahu zúčtovacího data, bude zúčtovací datum uveden jako zúčtovací datum položky uzavřeného období, které je přiřazeno adjustované položce ocenění. Datum je považováno za uzavřené období, pokud je dřívější než datum v poli Povolit účto od v nastavení financí.

### Od verze 5.0:
Ve formuláři požadavku dávkové úlohy Adjustace nákladů položek zboží již není uvedeno datum zaúčtování. Dávková úloha prochází všemi nezbytnými změnami a vytváří položky ocenění s datem zaúčtování položky ocenění, kterou upravuje. Pokud zúčtovací datum není v povoleném rozsahu zúčtovacího data, bude použito zúčtovací datum v poli Povolit účto od v nastavení financí nebo pokud jsou použita skladová období, bude použito pozdější datum těchto dvou dat. Viz výše popsaný koncept.

## Dávková úloha zobrazení historie účtování nákladů na zboží
Dávková úloha Účtování nákladů na zboží úzce souvisí s dávkovou úlohou Adjustace nákladů položek zboží, proto je zde shrnuta a sdílena také historie této dávkové úlohy.

### Od verze 3.0..3.70.A
Ve formuláři požadavku účtování nákladů na zboží je zúčtovací datum, které má uživatel zadat. Dávková úloha prochází všechny položky ocenění v rámci filtru, pokud je nějaký nastaven, a vytváří položky zboží se zúčtovacím datem zadaným ve formuláři požadavku.

### Verze 3.70.B..4.0
Ve formuláři žádosti účtování nákladů na zboží je k dispozici pole Zúčtovací datum položky uzavřeného období. Aplikace použije datum, které zadáte do tohoto pole, jako datum zaúčtování pro položky zboží, které vytvoří pro položky ocenění, jejichž data zaúčtování jsou v uzavřených účetních obdobích. V opačném případě budou mít položky zboží stejné zúčtovací datum jako původní položky ocenění. Datum je považováno za uzavřené období, pokud je dřívější než datum v poli Povolit účto od v nastavení financí. Pokud účtujete po účto skupinách, budou mít položky zboží datum účtování, které je uvedeno v poli Datum účtování ve formuláři žádosti.

Ve verzi 3 a 4 dávková úloha prohledá všechny položky ocenění, aby zjistila, zda existují nějaké položky ocenění, u kterých se částka nákladů (skutečná) liší od nákladů zaúčtovaných do věcných položek. Pokud je zjištěn rozdíl, bude rozdílná částka zaúčtována v položce zboží. Pokud se používá zaúčtování očekávaných nákladů, odpovídající pole jsou zpracována stejným způsobem.

![Skutečné náklady versus očekávané náklady](media/helene/TechArticleAdjustcost14.png "Skutečné náklady versus očekávané náklady")

### Od verze 5.0:
Ve formuláři požadavku dávkové úlohy Účtování nákladů na zboží již není uvedeno zúčtovací datum. Věcná položka je vytvořena se stejným datem zaúčtování jako odpovídající položka ocenění. Aby bylo možné dokončit dávkovou úlohu, musí povolený rozsah zúčtovacího data povolit zúčtovací datum vytvořené položky. Pokud tomu tak není, je nutné dočasně znovu otevřít povolené období účtování změnou nebo odebráním dat v polích Povolit účto od a do v nastavení financí. Aby se předešlo problémům s odsouhlasením, je nutné, aby datum zaúčtování věcné položky odpovídalo datu zaúčtování položky ocenění.

Dávková úloha prohledá tabulku 5811 - Položka ocenění k zaúčtování, aby identifikovala položky ocenění v rozsahu pro zaúčtování do věcných položek. Po úspěšném spuštění se tabulka vyprázdní.

## Viz také
[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)    
[Detaily návrhu: Vyrovnání zboží](design-details-item-application.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]