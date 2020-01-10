---
title: Často kladené otázky týkající se zobrazení seznamů
description: Podrobné informace o ukládání filtrů jako zobrazení seznamu.
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 01/09/2020
ms.reviewer: v-zdbice
ms.author: mikebc

---
# Často kladené otázky týkající se zobrazení seznamů

Toto téma odpovídá na otázky, na které se naši pokročilí uživatelé často ptají při práci se zobrazeními seznamu a ukládáním filtrů.  

## Odpovědi na otázky

### Jak pohledy zpracovávají vzorce?

Při ukládání pohledu, který obsahuje filtry se vzorci, jako jsou časové období, operátory, klíčová slova nebo tokeny filtru, se uloží výraz a nikoli výsledné hodnoty. Například uložením pohledu, který se filtruje v poli **Datum vytvoření** s výrazem **- 1T..today**, budou vždy nalezeny záznamy relativně k aktuálnímu datu, a to i v případě, že je pohled použit příští měsíc.

### Kde jsou uložena zobrazení seznamu?

Podobně jako skrytí pole nebo změna pořadí vaší navigační nabídky jsou zobrazení seznamu součástí přizpůsobení uživatele a jsou uložena v databázi. Vymazáním veškerého přizpůsobení ze seznamu také trvale odstraníte vaše osobní pohledy a vymažete další přizpůsobení, jako je změna pořadí pohledů. Další informace viz [Přizpůsobení pracovního prostoru](ui-personalization-user.md).

### Proč nemám ikonu Uložit?

Ikona uložení a nabídka možností se nezobrazí vedle pohledů v podokně filtru, pokud je přizpůsobení zakázáno pro roli uživatele. Uživatelé, kteří nemají povoleno přizpůsobení, mají stále přístup k systémovým pohledům, která jsou standardní součástí stránky, a mohou upravovat nebo vytvářet další filtry.

### Na kterých typech stránek mohu použít zobrazení seznamu?

Zobrazení jsou k dispozici pouze na stránkách seznamů a pracovních listů.

### Jsou pohledy k dispozici také na jiné formy seznamů?

Ano. Všechny pohledy, které uložíte do svého stolního prohlížeče nebo stolní aplikace, budou k dispozici také na tabletu nebo smartphonu. Pohledy na mobilních zařízeních nelze upravovat ani přizpůsobovat.

### Jsou moje osobní pohledy vždy přístupné?

Stejné pohledy jsou k dispozici na stránce seznamu, pokud k ní přistupujete z navigační nabídky, prostřednictvím okna **Řekněte mi** nebo prostřednictvím URL odkazu na stránku seznamu. Pohledy nejsou k dispozici v podoknech seznamu, při vyhledávání ani při zobrazení stránky seznamu jako dialogu.

### Jak vrátím pohled na původní filtry po jejich úpravě?

V dolní části podokna filtru vyberte akci **Obnovit filtry**, abyste vyčistili změny filtru provedené v pohledu a vrátili se k původním filtrovaným polím a kritériím filtru.

### Jaký je rozdíl mezi skrytím a odebráním pohledů?

Odebráním pohledu se toto zobrazení trvale odstraní. Skrytí pohledu vám umožňuje dočasně ho skrýt z podokna filtru, ale později ho můžete znovu skrýt výběrem akce **Zobrazit**.

### Jak mohu sdílet své pohledy s ostatními?

[!INCLUDE[d365fin](includes/d365fin_md.md)] neposkytuje způsob sdílení přesného zobrazení seznamu, ale můžete sdílet své současné filtry, aby ostatní uživatelé mohli vidět podobný seznam záznamů. V prohlížeči na počítači jednoduše zkopírujte URL adresu a sdílejte ji se svými kolegy. Sdílení filtrů nezaručuje příjemci identickou sadu filtrů, které vidíte v prohlížeči.

### Mohu hledat pohledy v okně Řekněte mi?

Ne. Okno **Řekněte mi** zobrazuje pouze výsledky vyhledávání pro stránku, ale po navigaci na stránku jste jen krok od dosažení svého oblíbeného zobrazení.

### Co je sdílené rozložení?

Všechna zobrazení na stránce seznamu sdílejí společné rozvržení sloupců, které zahrnuje, jaké sloupce jsou zobrazeny, jejich pořadí, šířku, nastavené podokno a nastavení rychlého vstupu. Přizpůsobení rozložení sloupců ovlivní také další pohledy, které sdílejí stejné rozložení na stránce seznamu.

Některá systémová zobrazení mohou mít jedinečná rozvržení sloupců v seznamu. Mohli například změnit uspořádání sloupců tak, aby zobrazovaly pouze sloupce nejrelevantnější pro toto zobrazení. Můžete určit, která zobrazení mají jedinečná rozvržení výběrem ikony ![Show more options](media/show-more-options-icon.png "Zobrazit více možností") a pozorování, že není zaškrtnuto políčko **Použít sdílené rozvržení**. Jako uživatel si můžete přizpůsobit rozvržení sloupců pro pohled s jedinečným rozvržením, aniž by to ovlivnilo kterékoli z ostatních pohledů na stránce seznamu. Pouze vývojáři mohou definovat jedinečné rozvržení sloupců pro pohled, který má původní sdílené rozvržení.

### Co dělá odkaz Zobrazit systémové filtry?

Na některých stránkách seznamu podokno filtrů zobrazuje **Zobrazit filtry systému** v dolní části podokna filtrů, pokud stránka obsahuje filtry definované systémem. Tyto speciální filtry se obvykle používají k zobrazení záznamů na základě aktuálního kontextu, například když je třeba seznam objednávek filtrovat pro konkrétního zákazníka.

Systémové filtry nastavují vývojáři pomocí skupiny filtrů 0. Technické podrobnosti o systémových filtrech viz [Metoda skupin filtrů](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method)

### Na své stránce vidím více pohledů, ale nevytvořil jsem je. Odkud přišli?

Pohledy, které vidíte v kterémkoli seznamu, jsou kombinací vašich osobních pohledů a systémových pohledů. Systémové pohledy mohou pocházet z podnikové aplikace, z rozšíření nebo mohou být specifické pro roli, pokud byl seznam přizpůsoben vaší roli.

### Proč některá pohledy poskytují méně možností?

Některé pohledy poskytují pouze možnost uložit kopii pohledu, zatímco jiná neumožňují vůbec uložit změny v pohledu. Způsob vytvoření pohledu určuje možnosti dostupné pro toto zobrazení. Pohledy lze vytvářet několika způsoby:

- Osobní pohledy, které jste uložili
- Systémové pohledy, které jsou standardní součástí podnikové aplikace nebo jsou přidána pomocí rozšíření nebo zobrazení specifických pro roli. Na rozdíl od osobních pohledů nemůžete uložit změny filtrů zpět do tohoto systémového zobrazení.
- Starší systémové pohledy, které jsou standardní součástí podnikové aplikace, ale byly vytvořeny pomocí starších verzí systému [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tato zobrazení nabízejí výrazně méně možností. Můžete je uložit pouze jako nové zobrazení a nelze je skrýt ani změnit jejich pořadí. Uvědomte si, že starší systémová zobrazení budou v budoucích aktualizacích [!INCLUDE[d365fin](includes/d365fin_md.md)] zrušena.

### Jak převést starší systémové pohledy?

Starší systémové pohledy jsou zobrazení seznamu, která byla vytvořena vývojáři ve starších verzích systému  [!INCLUDE[d365fin](includes/d365fin_md.md)] umístěním na stránku Centrum rolí. Tyto pohledy se nyní zobrazují přímo na stránce seznamu, ale nabízejí zhoršenou obsluhu a výrazně méně možností. Starší systémové pohledy můžete převést na osobní pohled, který je plně přizpůsobitelný, jednoduše tak, že toto starý pohled uložíte jako nový. Podobně se správci mohou rozhodnout převést starší pohledy specifické pro uživatelskou roli přizpůsobením uživatelské role a uložením zastaralého pohledu jako nového pohledu specifického pro roli.

Uvědomte si, že starší systémová zobrazení budou v budoucích aktualizacích [!INCLUDE[d365fin](includes/d365fin_md.md)] zrušena.

### ostatní v mé organizaci potřebují podobné zobrazení seznamu jako standardní. Co můžu dělat?

Práce s osobními pohledy je rychlá a efektivní, ale [!INCLUDE[d365fin](includes/d365fin_md.md)] poskytuje další nástroje pro definování zobrazení seznamu potřebných pro konkrétní uživatelské role nebo pro všechny uživatele v organizaci.

- Vývojáři mohou přizpůsobit prostředí a vytvářet zobrazení seznamu v rozšířeních pro všechny uživatele v organizaci.
- Ne-vývojáři, jako jsou administrátoři nebo vedoucí oddělení, mohou při přizpůsobování role na stránce **Profily (Role)** vytvářet zobrazení seznamu podle rolí.

### Pracuji s více jazyky: jak překládám název pohledu?

Při ukládání nového pohledu nebo přejmenování existujícího pohledu musíte pro toto zobrazení zadat rozpoznatelný a smysluplný název. Název se uloží pro váš aktuální jazyk a zobrazí se také, když s ním Vy nebo jiný uživatel pracujete [!INCLUDE[d365fin](includes/d365fin_md.md)] v různých jazycích. Chcete-li poskytnout přeložený název pohledu, musíte přepnout jazyk pomocí stránky **Moje nastavení** a poté přejmenovat zobrazení, které uloží přeložený název do nového jazyka.

### Fungují zobrazení se vzorci ve všech jazycích?

Vzorce, které používají pouze symboly, například '**|**' nebo **..**, jsou považovány za bezpečné pro přístup uživatelů v jakémkoli jazyce. Všechna zobrazení s výrazy, které obsahují písmena, klíčová slova nebo tokeny filtru, budou fungovat pouze pro jazyk, ve kterém byly vytvořeny.

### Viz také

[Ukládaní a přizpůsobení zobrazení seznamů](ui-views.md)  
[Hledání funkcí a informací](ui-search.md)  
[Řazení, vyhledávání a filtrování](ui-enter-criteria-filters.md)  
