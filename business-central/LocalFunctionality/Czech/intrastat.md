---
title: Czech Local Functionality - Intrastat | Microsoft Docs
description: This section describes local functionality - Intrastat
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Intrastat, Payables, Finance, CZ, Cash
ms.date: 12/30/2019
ms.reviewer: v-pejano
ms.author: v-makune
---

# Intrastat

Standardní funkce systému Intrastat nepřenese všechny platné transakce do deníku Intrastat. Výsledkem je množství manuální práce, která je nutná k vyloučení nebo zahrnutí nadbytečných nebo chybějících transakcí, což často způsobuje velké množství chyb. Podle požadavků České republiky jsou pro funkci Intrastat nutná následující vylepšení:
- Jednotlivé možnosti v modulu Intrastat je třeba parametrizovat
- Potřeba lepšího zpracování doplňkových měrných jednotek
- Potřeba vylepšit výpočet statistické částky a částky Intrastat
- Potřeba zdokonalit dávku pro získání položek Intrastat
- Export sestav Intrastat do souborů CSV podle místních požadavků

Tato funkce přidává vylepšení dat převedených do deníku Intrastat a připravuje prostředí pro správné vykazování v systému Intrastat.

## Nastavení modulu Intrastat

Další nastavení obecných parametrů modulu Intrastat umožňuje:
- Stanovit povinná pole Intrastat transakcí v oblasti prodeje, nákupu a transferů
- Nastavit odkud mají být získávána některá data týkající se zboží (zboží nebo zaúčtované položky) a jaké atributy zboží jsou povinné v transakcích prodeje, nákupu a transferů
- Nastavit zda některé Poplatky za zboží spojené s transakcemi prodeje, nákupu a transferů bude systém ignorovat (nezahrnovat je do částky nebo statistiky)
- Definovat, zda se vypočte statistická částka a způsob jejího výpočtu
- Vybrat Typ zaokrouhlování, jak budou částky a statistické částky zaokrouhlovány
- Nastavit směnný kurz cizí měny pro hlášení Intrastat
- Nastavit objekt pro export výkazu Intrastat

### Nové tabulky nastavení byly přidány pro:

- Statistické údaje
- Specifické pohyby
- Dodací skupiny Intrastat

### Dodatečné nastavení pro Intrastat umožňuje:

- Nastavení kódu Země/oblasti pro Místa přechodu
- Stanovit pro číslo sazebníku doplňkové měrné jednotky, pokud musí být číslo sazebníku vykazováno v doplňkových měrných jednotkách. 
- Nastavit zda konkrétní poplatky za zboží musí být zahrnuty v částce nebo statistické částce či v obou
- Nastavit chování Intrastatu pro způsoby dodávky – zda poplatky za zboží musí být zahrnuty/vyloučeny pro konkrétní způsoby dodávky a dodací skupiny Intrastat
- Nastavit hodnotu Oblasti na kartě lokace
- Nastavit výchozí hodnoty pro dalších doplňkové údaje Intrastat na zákaznických a dodavatelských kartách
- Definovat na kartě zboží další údaje pro Intrastat – Statistický údaj a Specifický pohyb
- Vytvořit speciální nastavení pro zahraniční směnný kurz a nastavení objektu pro export pro každou registraci země 

## Účtování transakcí pro Intrastat 

Pro identifikaci a zadání parametrů transakce, které budou použity v systému Intrastat, postupujte podle následujících kroků:
- Uživatel ověřuje Intrastat údaje (typ transakce, specifikace transakce a typ přepravy, atd.) na kartě Zahraniční obchod. Tyto údaje byly převedeny do hlavičky dokladu z příslušné karty zákazníka nebo dodavatele a mohou být ručně přepsány. 
- Pole Intrastat transakce (needitovatelné) informuje uživatele o tom, zda konkrétní transakce je kvalifikována jako transakce vykazovaná v Intrastat.
- Identifikace fyzického pohybu v korekčních dokladech (dobropisech) pomocí pole Fyzický pohyb. 
- Uživatel může ručně vyloučit Intrastat transakce z vykazování Intrastat pomocí pole Nezahrnuto do Intrastatu.
- Uživatel ověřuje data pro Intrastat (Číslo sazebníku, Statistický údaj, země/oblast původu a hmotnost) v řádcích dokladu. Tyto údaje byly převedeny do řádku z příslušné karty zboží a mohou být ručně přepsány.
- Uživatel přiřadí poplatky za zboží k řádku a zahrne/vyloučí jejich hodnotu z částky a statistické částky pro Intrastat.
- Během účtování systém přenese všechny relevantní informace pro Intrastat do položky zboží.
- Během účtování systém ohlásí chybu, pokud některá Intrastat pole nastavená jako povinná ve formuláři Nastavení stat. vykazování nejsou vyplněna.  Toto nedovolí uživateli transakci zaúčtovat.

## Příprava deníku Intrastat

Deník Intrastat obsahuje následující nová pole a funkce: 
- Kód způsobu dodávky
- Statistický údaj
- Specifický pohyb
- Kalkulace doplňkových měrných jednotek
- Číslování hlášení
- Typy hlášení pro klasifikaci výkazů – Nové, Prázdné, Opravné, Storno
- Filtrování položek dle Registrace země

Nejrychlejší způsob jak uživatel může připravit Intrastat deník a ujistit se, že všechna pravidla stanovená v předchozích krocích jsou dodržována, je pomocí dávkové úlohy Najít položky zboží. Při provádění dávkové úlohy Najít položky zboží se systém postará o následující:
- Zpracovává položky zboží a položky projektu vytvořené v transakcích identifikovaných jako Intrastat transakce. 
- Ignoruje prodejní a nákupní Intrastat transakce, které mají příznak EU obchod třetích stran
- Zahrnuje Intrastat transakce, které mají místa přechodu v EU zemích
- Systém zahrnuje prodejní a nákupní doklady zaúčtované s příznakem Oprava (tj. dobropisy) do deníku Intrastat se stejným typem pohybu jako opravovaný doklad, ale s opačným znaménkem pro doklady neoznačené jako Fyzický pohyb a s opačným typem pohybu pro doklady označené jako Fyzický pohyb. 
- Zajišťuje, že zrušené Intrastat transakce (pomocí funkcí Vrátit příjemku/Vrátit dodávku) jsou vyloučeny z vykazování.
- Zajišťuje, že Poplatky za zboží jsou (nejsou) započteny a upraveny v částce a statistické částce podle nastavení v Nastavení stat. vykazování, na poplatcích za zboží, způsoby dodávky a přiřazení poplatku za zboží. 
- Zajišťuje, že při přípravě řádků Intrastat deníku se používají Doplňkové měrné jednotky. 
- Zajišťuje, že je užíván správný zdroj dat pro číslo sazebníku, hmotnost a zemi/oblast původu podle Nastavení stat. vykazování.

## Podání hlášení Intrastat do formátu CSV

Do deníku Intrastat bylo přidána možnost exportu sestav do souborů .csv odpovídající lokálním požadavkům (pro aplikace INSTATDESK a INSTATONLINE)
Export používá objekt na export podle Nastavení. stat. vykazování, nebo Země/oblasti registrace.

## Viz také
[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](finance.md)