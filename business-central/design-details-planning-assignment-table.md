---
    title: Design Details - Planning Assignment Table | Microsoft Docs
    description: This topic provides insight into what happens when you change how you plan for an item.
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
# Detaily návrhu: Tabulka přiřazení plánování
Všechno zboží by měly být plánovány, ale není důvod pro výpočet plánu pro zboží, pokud nedošlo ke změně ve struktuře poptávky nebo nabídky od posledního výpočtu plánu.

Pokud uživatel zadal novou prodejní zakázku nebo změnil stávající, existuje důvod k přepočítání plánu. Mezi další důvody patří změna v prognóze nebo požadované množství bezpečných zásob. Změna kusovníku přidáním nebo odebráním komponenty by s největší pravděpodobností znamenala změnu, ale pouze pro položku komponenty.

Pro více skladových míst se přiřazení provádí na úrovni zboží podle kombinace skladového místa. Pokud byla například prodejní objednávka vytvořena pouze v jedné lokaci, aplikace přiřadí zboží v tomto konkrétním skladovém místě k plánování.

Důvodem pro výběr zboží pro plánování je otázka výkonu systému. Pokud nenastane žádná změna ve struktuře nabídky-poptávky, plánovací systém nenavrhne žádné kroky, které mají být podniknuty. Bez přiřazení plánování by systém musel provést výpočty pro všechny položky, aby zjistil, na co se plánuje, a to by vyčerpalo systémové prostředky.

Tabulka **Přiřazení plánováním** sleduje události poptávky a nabídky a přiřadí příslušné zboží pro plánování. planning. Sledovány jsou následující události:

* Nová prodejní objednávka, prognóza, komponenta, nákupní objednávka, výrobní zakázka, montážní zakázka nebo objednávka transferu.
* Změna zboží, množství, umístění, varianty nebo data v prodejní objednávce, prognóze, komponentě, nákupní objednávce, výrobní zakázce, montážní objednávce nebo v objednávce transferu.
* Zrušení prodejní objednávky, prognózy, komponenty, nákupní objednávky, výrobní zakázky, objednávky sestavy nebo objednávky transferu.
* Spotřeba jiných než plánovaných položek.
* Produkce jiného zboží, než bylo plánováno.
* Neplánované změny ve skladu.

U těchto přímých přesunů nabídky a poptávky systém sledování objednávek a zasílání zpráv o akci udržuje tabulku přiřazení plánování a uvádí jako důvod akce plánovací důvod.

Následující změny v kmenových datech mohou také způsobit nerovnováhu při plánování:

* Změna stavu na Certifikované v hlavičce výrobního kusovníku (pro všechno zboží používající tuto hlavičku).
* Smazaný řádek (podřízené zboží).
* Změna stavu na Certifikované v hlavičce technologického postupu (pro všechno zboží používající tento postup).
* Změny v následujících polích karty zboží.
* Minimální zásoby nebo Bezpečná průběžná doba.
* Výpočet dodací doby.
* Bod přiobjednání.
* Číslo výrobního kusovníku. (a všechno podřízené zboží starého kusovníku).
* Číslo TNG postupu
* Způsob přiobjednání

V těchto případech nová funkce správa přiřazení plánováním, udržuje tabulku a uvádí důvod plánování jako Čistá změna.

Následující změny nezpůsobují změny v přiřazení plánování:

* Kalendáře
* Další parametry plánování na kartě zboží

Při výpočtu MPS nebo MRP platí následující omezení:

* MPS: Plánovací systém kontroluje, zda položka nese předpověď poptávky nebo prodejní objednávku. Pokud ne, položka není zahrnuta do plánu.
* MRP: Pokud plánovací systém zjistí, že zboží je doplňováno plánovacím řádkem MPS nebo objednávkou dodávek MPS, bude zboží vynecháno z plánování. Zahrnuta je však veškerá poptávka po příslušných komponent.

## Viz také
[Detaily návrhu: Vyvažování poptávky a nabídky](design-details-balancing-demand-and-supply.md)   
[Detaily návrhu: Používání způsobu přiobjednání](design-details-handling-reordering-policies.md)   
[Detaily návrhu: Plánování transferů](design-details-transfers-in-planning.md)   
[Detaily návrhu: Plánovací parametry](design-details-planning-parameters.md)
