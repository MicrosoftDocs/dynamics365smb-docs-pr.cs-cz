---
title: VAT - Czech Local Functionality | Microsoft Docs
description: This section describes Czech local functionality for VAT.
author: ACMartinKunes

ms-service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: CZ, Czech, Finance, VAT
ms.date: 12/30/2019
ms.reviewer: v-pejano
ms.author: v-makune
---

# Finance - DPH

## Datum DPH

Datum DPH je důležité pro daňové doklady podle § 28 zákona o DPH 235/2004 Sb. Datum DPH se může lišit od data zaúčtování nebo data dokladu. Datum DPH je důležité pole pro vykazování DPH.

Tato funkce se zaměřuje na zlepšení následujících oblastí:

### Nastavení použití Data DPH

- Obecné povolení používání Data DPH v systému.
- Výběr způsobů, jakým systém bude zobrazovat výchozí hodnotu Data DPH v různých oblastech (Zúčtovací datum nebo Datum dokladu).
- Období pro vykazování DPH a účetní období společnosti se mohou často lišit. Abychom umožnili uživatelům bezproblémově vykazovat a účtovat DPH podle období pro vykazování DPH a také vydávat interní a další statutární vykazování na základě účetních období, zavádí tato funkce nově Období DPH.
- Povolit účtování DPH od/do – zadání časové období v polích od/do, aby se zabránilo chybám účtování do uzavřených účetních a DPH období.

### Účtování transakcí s datem DPH  

Aby uživatel zaúčtoval transakce s použitím Data DPH, musí být schopen zadat datum DPH v aplikaci do hlaviček dokladů a řádků deníku.
Po zaúčtování je Datum DPH součástí zaúčtovaných dokladů, věcných položek a položek DPH.

### Výpočet a účtování vyrovnání DPH

Systém filtruje položky DPH na základě data DPH (místo Zúčtovacího data) výběrem DPH období a připraví sestavu ukazující, které položky budou převedeny na účet vyrovnání DPH. Výtisk obsahuje také informace o datu DPH.

### Odsouhlasení položek DPH a věcných položek  

Uživatelé často porovnávají částky v položkách DPH a částky DPH zaúčtované ve věcných položkách.
Částky zobrazované v novém poli Pohyb (Datum DPH) v následujících formulářích jsou vždy filtrované dle data DPH:

- Účetní osnova
- Saldo
- Saldo účtu

## Výkaz DPH

Výkaz DPH obsahuje řadu vylepšení a možností:

- Doplněno Nastaven stat. vykazování s obecným nastavením pro vykazování DPH.
- Doplněny dvě nové řádkové operace v poli typ (Dělení řad a Násobení řad).
- Doplněno nastavení pro DPH ze záloh.
- Filtrovat položky DPH pro výkaz DPH dle režimu třístranného obchodu v EU. Tento krok je nutný, protože třístranný obchod (prostředník - 1 dlužník) v EU musí být veden na samostatných řádcích. 
- Vytisknout výkaz DPH s novou možností zaokrouhlit vypočtené částky ve výkazu DPH na celé hodnoty.
- Filtrovat data na základě Data DPH s použitím Období DPH.
- Filtrovat data pro starší zaúčtovaná hlášení DPH.
- Další typy výkazu DPH – Řádný, Následný, Dodatečný – podle § 43 část 1 Zákona o DPH 235/2004) plátce může předložit dodatečné hlášení o DPH (viz dále).
- Exportovat výkaz DPH do souboru .xml.
- Přidat komentáře a přílohy k exportu pro finanční úřad.

## Dodatečná hlášení DPH  

Podle § 43 část 1 zákona o DPH 235/2004 může plátce předložit dodatečné hlášení DPH. V případě, že chce uživatel provést dodatečné hlášení DPH, vybere si Typ hlášení – Dodatečné v rámci exportu výkazu.  
Ve funkcionalitě Vypočítat a účtovat vyrovnání DPH je číslo dokladu uloženo do uzavíraných položek DPH jako Číslo daňového přiznání  pro další vyhledávání ve výkazu DPH a sestavách. Tato funkce umožňuje výpočet a tisk pro různé výkazy DPH zaúčtované a podané v jednom období DPH.

## Souhrnné hlášení  

Souhrnné hlášení je používáno k hlášením o prodejích daňovým orgánům v zemích EU (Evropské unie). Podle § 102 zákona o DPH 235/2004 je plátce povinen podat Souhrnné hlášení. Souhrnné hlášení musí být podáno elektronicky na finanční úřad.  

Funkcionalita Souhrnného hlášení umožňuje:

- Nastavit stat. vykazování s obecným nastavením pro hlášení
- Vybrat kombinace DPH obchodní účto skupiny a DPH účto skupiny zboží (nastavení účtování DPH) pro zahrnutí do souhrnného hlášení
- Uchovat historii souhrnných hlášení
- Zadat všechny informace potřebné pro elektronické podání souboru
- Navrhnout řádky pro souhrnné hlášení
- Podporovat opravná hlášení
- Exportovat data do souboru pro elektronické podání

## Institut nespolehlivého plátce  

Novela zákona o DPH 235/2004 (§ 106a) zavedla institut nespolehlivého plátce. Ministerstvo financí zveřejňuje elektronicky seznam nespolehlivých plátců.  
Tato funkce využívá tuto službu k získání zveřejněných informací a ukazuje stav plátce na kartách dodavatelů a nákupních dokladech.  
Ministerstvo financí také zveřejňuje informace o registrovaných bankovních účtech plátců (pouze tyto účty jsou povoleny pro platby). Informace o registrovaných bankovních účtech plátců jsou uloženy v Bankovních účtech dodavatele a používány v rámci platebního styku.

## Směnný kurz pro DPH  

Směnný kurz se již v dokladech nachází, ale v České republice musí existovat možnost nastavit v prodejních a nákupních dokladech jiný směnný kurz pro účtování a jiný pro výpočet DPH. Tato funkce přidává pole Kód měny DPH a Směnný kurz DPH na dokladech.  Uživatelé mohou změnit směnný kurz pro DPH před zaúčtováním dokladů.  

## [Kontrolní hlášení DPH](vat-control-report.md)

Funkcionalita [!INCLUDE[d365fin](../../includes/d365fin_md.md)] byla rozšířena o Kontrolní hlášení DPH. Položky DPH jsou pro zvolené datum DPH a datum zaúčtování (podle nastavení hlavní knihy) načítány do formuláře podle zvoleného období.  Ke zpracování kontrolního hlášení je nutné nastavit sekce kontrolního hlášení DPH, čísla sazebníku, výkaz DPH, nastavení  stat. vykazování a rozšířené nastavení účtování DPH.

## Sestavy DPH

Pro splnění nároků na tiskové výstupy odpovídající legislativním požadavkům a místním zvyklostem poskytuje tato funkce následující sestavy:  

- Výpočet a účtování vyrovnání DPH - standartní sestava byla přizpůsobena
- Podklady pro DPH
- Seznam daňových dokladů,
- Přehled DPH na prodejních  zálohách
- Přehled DPH na  nákupních  zálohách

## Viz také

[Česká lokální funkcionalita](czech-local-functionality.md)