---
title: open item ledger entries
description: Learn why the inventory level is zero although open item ledger entries exist.
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
# Detaily návrhu: Známé prolémy vyrovnávání zboží
Tento článek řeší problém, kdy je úroveň skladového minima nulová, i když v [!INCLUDE[prod_short](includes/prod_short.md)] existují otevřené položky zboží.

Článek začíná uvedením typických příznaků problému, následovaných základy vyrovnání zboží na podporu popsaných důvodů tohoto problému. Na konci článku je alternativní řešení pro řešení těchto otevřených položek zboží.

## Projevy problému
Typické projevu problému, kdy je úroveň skladového minima nulová, i když existují otevřené položky zboží, jsou následující:

- Při pokusu o uzavření období zásob se zobrazí následující zpráva: „Zásoby nelze zavřít, protože u jedného nebo více zboží existuje záporný stav zásob.“

- Situace položky zboží, kdy je otevřena jak výstupní položka zboží, tak i související vstupní položka zboží.

   Viz následující příklad situace položky zboží.

   | Číslo položky | Zúčtovací datum | Typ položky | Typ dokladu | Číslo dokladu | Číslo zboží | Kód lokace | Množství | Částka nákladů (skutečná) | Fakturované množství | Zbývající množství | Otevřít |
   |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
   | 333 | 28.01.2018 | Prodej | Prodejní dodávka | 102043 | TEST | MODRÝ | -1 | -10 | -1 | -1 | Ano |
   | 334 | 28.01.2018 | Prodej | Prodejní dodávka | 102043 | TEST | MODRÝ | 1 | 10 | 1 | 1 | Ano |

## Základy vyrovnání zboží
Pro každou skladovou transakci se vytvoří položka vyrovnání zboží, která propojí příjemce nákladů se zdrojem nákladů, takže lze náklady předat podle metody ocenění. Pro více informací navštivte [Detaily návrhu: Vyrovnání zboží](design-details-item-application.md).

- U vstupní položka zboží se položka vyrovnání zboží vytvoří při vytvoření položky zboží.

- U výstupní položka zboží se položka vyrovnání zboží vytvoří při zaúčtování položky zboží, POKUD existuje otevřená vstupní položka zboží s dostupným množstvím, na které se může vztahovat. Pokud neexistuje žádná otevřená vstuoní položka zboží, na kterou se může vztahovat, pak výstupní položka zboží zůstane otevřená, dokud nebude zaúčtována vstuoní položka zboží, na kterou se může vztahovat.

Existují dva typy vyrovnání zboží:

- Vyrovnání množství

- Vyrovnání nákladů

### Vyrovnání množství
Vyrovnání množství se vytvářejí pro všechny skladové transakce a vytvářejí se automaticky nebo ručně ve speciálních procesech. Pokud jsou vyrovnání množství vyrobeny ručně, jsou označovány jako pevné vyrovnání.

Následující diagram ukazuje, jak jsou vytvářeny vyrovnání množství.

![Tok úpravy nákladů od nákupu k prodeji](media/helene/TechArticleInventoryZero2.png "Tok úpravy nákladů od nákupu k prodeji")

Všimněte si výše, že položka zboží 1 (Nákup) je dodavatelem zboží i zdrojem nákladů pro položku zboží 2 (prodej).

> [!NOTE]  
> Pokud je výstupní položka zboží oceněna průměrnými náklady, pak použitá vstupní položka zboží není jedinečným zdrojem nákladů. Hraje pouze roli při výpočtu průměrných nákladů za období.

### Vyrovnání nákladů
Vyrovnání nákladů je vytvořeno pouze pro příchozí transakce, kde je vyplněno pole **Vyrovnáno položkou zboží** aby bylo možné poskytnout pevné vyrovnání. K tomu obvykle dochází v souvislosti s prodejním dobropisem nebo scénářem vrácení dodávky. Vyrovnání nákladů zajišťuje, že zboží znovu vstupuje do zásob se stejnými náklady, jako když byla dodána.

Následující diagram ukazuje, jak se vytvářejí vyrovnání nákladů.

| Číslo položky | Zúčtovací datum | Typ položky | Typ dokladu | Číslo dokladu | Číslo zboží | Kód lokace | Množství | Částka nákladů (skutečná) | Fakturované množství | Zbývající množství | Otevřít |
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
| 333 | 28.01.2018 | Prodej | Prodejní dodávka | 102043 | TEST | MODRÝ | -1 | -10 | -1 | -1 | Ano |
| 334 | 28.01.2018 | Prodej | Prodejní dodávka | 102043 | TEST | MODRÝ | 1 | 10 | 1 | 1 | Ano |

Všimněte si výše, že vstuoní položka zboží 3 (Prodejní vratka) je příjemcem nákladů pro původní výstupní položku zboží 2 (Prodej).

## Ilustrace základního toku nákladů
Předpokládejme kompletní tok nákladů, kde je zboží přijato, odesláno a fakturováno, vráceno s přesnými náklady a znovu dodáno.

Následující diagram ilustruje tok nákladů.

![Tok úpravy nákladů od prodeje po prodejní vratku](media/helene/TechArticleInventoryZero4.png "Tok úpravy nákladů od prodeje po prodejní vratku")

Všimněte si výše, že náklady jsou předány do položky zboží 2 (Prodej), pak do položky zboží 3 (Prodejní vratka) a nakonec do položky zboží 4 (Prodej 2).

## Důvody problému
Problém, kdy je úroveň skladového minima nulová, přestože existují otevřené položky zboží, může být způsoben následujícími scénáři:

- Scénář 1: Dodávka a faktura jsou zaúčtovány, i když zboží není k dispozici. Zaúčtování je pak vráceno přesnými náklady pomocí prodejního dobropisu.

- Scénář 2: Zásilka je zaúčtována, i když zboží není k dispozici. Zaúčtování je poté vráceno pomocí funkce Vrátit dodávku.

Následující diagram ukazuje, jak jsou vyrovnání zboží vytvářeny v obou scénářích.

![ok úpravy nákladů probíhá oběma směry](media/helene/TechArticleInventoryZero6.png "ok úpravy nákladů probíhá oběma směry")

Výše uvedené upozornění, že je vytvořeno vyrovnání nákladů (reprezentovano modrými šipkami), aby se zajistilo, že položce zboží 2 (Prodejní vratka) budou přiřazeny stejné náklady jako položce zboží 1 (Prodej 1), která je stornována. Vyrovnání množství (reprezentované červenými šipkami) se však nevytváří.

Položka zboží 2 (Prodejní vratka) nemůže být příjemcem nákladů původní položky zboží a zároveň dodavatelem zboží a jeho zdrojem nákladů. Proto původní položka zboží 1 (prodej 1) zůstane otevřená, dokud se neobjeví platný zdroj.

## Identifikace problému
Chcete-li zjistit, zda jsou vytvořeny otevřené položky zboží, postupujte pro příslušný scénář takto:

U scénáře 1 identifikujte problém takto:

- Na stránce **Účtovaný prodejní dobropis** nebo **Účtovaná příjemka vratky** vyhledejte v poli **Vyrovnáno položkou zboží** zda je pole vyplněno, a v takovém případě, ke které položce zboží je příjemka vratky použita.

U scénáře 2 identifikujte problém jedním z následujících způsobů:

- Vyhledejte otevřenou výstupní položku zboží a vstupní položku zboží se stejným číslem v poli **Číslo dokladu** a Ano v poli **Oprava**. Podívejte se na následující příklad takové situace položky zboží.

| Číslo položky | Zúčtovací datum | Typ položky | Typ dokladu | Číslo dokladu | Číslo zboží | Kód lokace | Množství | Částka nákladů (skutečná) | Fakturované množství | Zbývající množství | Otevřít | Oprava |
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
| 333 | 28.01.2018 | Prodej | Prodejní dodávka | 102043 | TEST | MODRÝ | -1 | -10 | -1 | -1 | Ano | Ne |
| 334 | 28.01.2018 | Prodej | Prodejní dodávka | 102043 | TEST | MODRÝ | 1 | 10 | 1 | 1 | Ano | **Ano** |

- Na stránce **Účtovaná prodejní dodávka** vyhledejte v poli **Vyrovnáno položkou zboží**, zda je pole vyplněno, a v takovém případě, ke které položce zboží je účtována příjemka vratky.

> [!NOTE]  
> Na stránce **Vyrovnané položky zboží** nelze identifikovat vyrovnání nákladů, protože tato stránka zobrazuje pouze vyrovnání množství.

U obou scénářů identifikujte příslušné vyrovnání nákladů následovně:

1. Otevřete tabulku **Položka vyrovnání zboží**.

2. Filtrujte v poli **Číslo položky zboží** pomocí čísla položky zboží prodejní vratky.

3. Analyzujte položku vyrovnání zboží a vezměte na vědomí následující:

   Pokud je pole **Vyrovnáno položkou číslo** vyplněno pro vstupní položku zboží (kladné množství), znamená to, že vstupní položka zboží je příjemcem nákladů výstupní položky zboží.

   Podívejte se na následující příklad položky vyrovnání zboží.

   | Číslo položky | Číslo položky zboží | Vyrovnává položku číslo | Vyrovnáno položkou číslo | Množství | Zúčtovací datum | Vyrovnání nákladů |
   |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
   | 299 | 334 | 334 | 333 | 1 | 28.01.2018 | Ano |
<!--![Why is inventory zero 8](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

Všimněte si výše, že u vstupní položky zboží 334 jsou náklady použité na výstupní položku zboží 333.

## Řešení problému
Na stránce **Deník zboží** zaúčtujte následující řádky pro předmětné zboží:

- Kladná úprava pro uzavření otevřené výstupní položky zboží.

- Záporná úprava se stejným množstvím.

   Tato úprava vyrovná zvýšení zásob způsobené kladnou úpravou a uzavře otevřenou vstupní položku zboží.

Výsledkem je, že zásoby jsou nulové a všechny položky zboží jsou uzavřeny.

## Viz také
[Detaily návrhu: Vyrovnání zboží](design-details-item-application.md)     
[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]