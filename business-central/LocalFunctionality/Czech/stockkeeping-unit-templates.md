---
title: Czech Local Functionality Templates for inventory Operations – Stockkeeping Unit Templates
description: The following topics describe the local functionality Stockkeeping Unit Templates in the Czech version of Business Central.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Inventory, Localization, CZ
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Šablony skladových jednotek

Nastavte šablony skladových jednotek, které bude možné využít v procesu vytváření nových skladových jednotek zboží.

Šablony se definují pro kombinaci Kategorie zboží a Lokace a lze zde nastavit základní parametry skladové jednotky, jako je Systém doplnění, Způsob přiobjednání a další.

Šablony skladových jednotek je možné využít ve funkci, která vytváří nové skladové jednotky zboží. Při vytváření skladové jednotky funkcí jsou nastavení parametrů v šablonách automaticky kopírována do karet skladových jednotek.

## Vytvoření a nastavení šablon skladových jednotek
### Vytvoření šablony konfigurace pro šablonu skladové jednotky

Pro správné nastavení detailů karty skladové jednotky, například pro vybranou lokaci, je možné nutné nastavit obecné informace jako je Způsob přionjednání, Systém přiobjednání a další. 

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační šablony** a poté vyberte související odkaz.
2. V panelu funkcí vyberte **Nový**.
3. Do pole **Kód** zadejte kód pro skladovou jednotku.
4. Do pole **Popis** vyplňte název pro šabolu.
5. V poli **ID tabulky** vyberte tabulku 5700.
6. V řádích vyberte typ **Pole** dále ve sloupečku **Název pole** vyberte pole z tabulky skladové jednotky, které chcete nastavovat. Do pole **Výchozí hodnota** zadejte, co má pole obsahovat.
7. Po nastavená vybraných polí, bude systém dopňovat předdefinované hodnoty do karty skladové jednotky během využití šablony při vytváření skladové jednotky z šablony.

### Vytvoření šablony skladové jednotky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony skladových jednotek** a poté vyberte související odkaz.
2. V panelu funkcí vyberte **Nový**.
3. V novém řádku vyplňte pole **Kód kategorie zboží** a do pole **Kód lokace** vyberte lokaci. Dále je možné vyplnit **Kód šablony konfigurace**, kde vyberte vytvořenou konfigurační šablonu skladové jednotky a poté se pole **Popis šablony konfigurace** automaticky doplní.
5. Po vyplnění hodnot můžete přehled šablon můžete zavřít.
  
### Vytvoření skladové jednotky pomocí šablony

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte kartu zboží, pro které je vytvořena šablona.
3. Otevřete kartu zboží.
4. Na kartě zboží použijte funkci **Sklad** - **Skladové jednotky**.
5. Otevře se vám přehled **Skladových jednotek** pro danou kartu zboží.
6. Na přehledu zvolte funkci **Nový**.
7. Na kartě skladové jednotky vyberte pole **Kód lokace**. Po vybrání pole se do karty skladové jednotky přenese nastavení z šablony.
8. Po kontrole můžete kartu zavřít. 

## Použití šablon skladových jednotek na vybraném zboží
### Vytvoření šablony konfugirace pro šablonu skladové jednotky pro vybrané zboží

Pro správné nastavení detailů karty skladové jednotky, například pro vybranou lokaci, je možné nutné nastavit obecné informace jako je Způsob přionjednání, Systém přiobjednání a další. 

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Konfigurační šablony** a poté vyberte související odkaz.
2. V panelu funkcí vyberte **Nový**.
3. Do pole **Kód** zadejte kód pro skladovou jednotku, například **SKJ0000003**.
4. Do pole **Popis** vyplňte název pro šabolu, například "**Skladová jednotka KŘESLO MODRÝ**".
5. V poli **ID tabulky** vyberte tabulku, nad kterou bude šablona fungovat. V tom to případě to je tabulka **5700** - **Stockkeeping Unit**
6. V řádích vyberte typ **Pole** dále ve sloupečku **Název pole** vyberte pole z tabulky skladové jednotky, které chcete nastavovat. Do pole **Výchozí hodnota** zadejte, co má pole obsahovat. V tomto příkladu vyberte například pole **Systém doplnění** a hodnotu **Transfer**.
7. Po nastavená vybraných polí, bude systém dopňovat předdefinované hodnoty do karty skladové jednotky během využití šablony při vytváření skladové jednotky z šablony.

### Vytvoření šablony skladové jednotky pro vybrané zboží

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony skladových jednotek** a poté vyberte související odkaz.
2. V panelu funkcí vyberte **Nový**.
3. V novém řádku vyplňte pole **Kód kategorie zboží** například hodnotou **KŘESLO**, do pole **Kód lokace** vyberte lokaci **MODRÝ**, následně se vyplní pole **Popis** automaticky textem "**Kancelářské křeslo z Modrý sklad**". Dále je možné vyplnit **Kód šablony konfgurace**, kde vyberte hodnotu **SKJ0000003** a pole **Popis šablony konfigurace** se automaticky doplní.
5. Po vyplnění hodnot můžete přehled šablon zavřít.
  

### Vytvoření skladové jednotky vybraného zboží pomocí šablony

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Použijte funkci hledání a najděte zboží **1900-S Křeslo PAŘÍŽ, černé**
3. Otevřete kartu zboží.
4. Na kartě zboží použijte funkci **Sklad** - **Skladové jednotky**.
5. Otevře se vám přehled **Skladových jednotek** pro danou kartu zboží.
6. Na přehledu zvolte funkci **Nový**.
7. Na kartě skladové jednotky vyberte pole **Kód lokace**. Po vybrání pole se do karty skladové jednotky přenese nastavení z šablony.
8. Po kontrole můžete kartu zavřít. 

## Viz také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
