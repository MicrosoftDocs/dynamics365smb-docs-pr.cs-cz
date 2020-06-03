---
title: Czech Local Functionality - Bank feature| Microsoft Docs
description: This section describes Czech local functionality - Bank feature
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Bank, Finance, CZ, Bank feature
ms.date: 12/30/2019
ms.reviewer: v-pejano
ms.author: v-makune
---

# Tuzemské bankovnictví  

Tato funkce zajišťuje vyšší efektivitu a zabraňuje uživateli dělat chyby při zadávání údajů o bankovním účtu zákazníků a dodavatelů tím, že ukládá bankovní informace a eliminuje potřebu údaje vždy znovu zadávat. Taková funkce je zapotřebí, zvláště když je více bankovních transakcí prováděno elektronicky.

## Nastavení bankovnictví  

Nová pole jsou doplněna na Bankovní účet:
- Obecné informace – přiřazení k č. bankovního účtu
- Číslování - Číslo platebního příkazu, číslo bankovního výpisu
- Import, export informací
- Informace pro účtování a párování
- Nastavení pro platební příkazy/bankovní výpisy

Nová pole jsou doplněna na Bankovní účet, Bankovní účet zákazníka a Bankovní účet dodavatele.

## Výchozí bankovní účet společnosti

Kód výchozího bankovního účtu je doplněn do Informací o společnosti.

## Prodejní doklady a bankovní účty

Je docela běžné, že společnosti mají několik bankovních účtů vedených v několika bankovních institucích za účelem snížení nákladů finančních transakcí. Proto [!INCLUDE[d365fin](../../includes/d365fin_md.md)] musí umožnit uživatelům vybrat preferovaný bankovní účet, který má být vytištěn na prodejních dokladech.
Výběr Kódu bankovního účtu byl přidán do prodejních dokladů a informace z vybraného bankovního účtu jsou přenášeny do hlavičky dokladu.

Byla přidána další pole pro identifikaci platby do hlavičky dokladu (specifický symbol, variabilní symbol, konstantní symbol, atd.). Tyto informace jsou během účtování přenášeny do zaúčtovaného dokladu a položky zákazníka. To umožňuje přesnější vyrovnání plateb faktur.  

## Nákupní doklady a bankovní účty

Dodavatelé mají běžně několik bankovních účtů vedených v několika bankovních institucích. Proto [!INCLUDE[d365fin](../../includes/d365fin_md.md)] musí umožnit uživatelům vybrat preferovaný dodavatelský bankovní účet, který má být použit pro platbu nákupních dokladů.

Výběr kódu bankovního účtu dodavatele byl přidán do nákupních dokladů a informace z vybraného bankovního účtu dodavatele jsou převedeny do nákupní hlavičky.

Byla přidána další pole pro identifikaci platby do nákupní hlavičky (specifický symbol, variabilní symbol, konstantní symbol, atd.).  Tyto informace jsou během účtování přenášeny do zaúčtovaného dokladu a položky dodavatele. To následně umožňuje použití těchto informací pro návrhy plateb a pozdější párování.

## Bankovní výpisy a platební příkazy  

Umožňuje vytvářet platební příkazy a bankovní výpisy. Lze evidovat neomezený počet bankovních účtů u různých bankovních ústavů a v různých měnách. Lze importovat a exportovat soubory (výpisy a příkazy) z bankovních softwarů.

### Hlavní funkčnosti  

- Vytvoření, vydání a exportování platebního příkazu
- Vytvoření, import a vydání bankovního výpisu
- Překlopení bankovního výpisu do deníku odsouhlasení plateb
- Párování položek v deníku odsouhlasení plateb a zaúčtování

### Další podporované funkčnosti  

- Na dokladech Platební příkaz a Bankovní výpis je možné využít vedle vlastních importních/exportních funkcí také standardních nástrojů pro definici formátů importu a exportu bankovních souborů.
- Pro zpracování položek výpisu je využíváno výhradně standardního Deníku odsouhlasení plateb Standardní párovací nástroj pro automatické vyrovnání položek je rozšířen o CZ specifika (pravidla vyrovnání plateb rozšířena např. o variabilní symbol).
- Další informace a pravidla pro výpočet plateb a mapování účtů na základě textu.
- Textové mapování účtů - pro automatické párování položek bankovního výpisu dle textu uvedeného v popisu, rozšířeno také o možnost mapování účtů dle variabilního symbolu, konstantního symbolu, specifického symbolu, čísla bankovního účtu, IBAN a kódu SWIFT.
- Deníky odsouhlasení plateb - možnost spustit vyrovnání automaticky.

## Viz také  

[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](finance.md)
