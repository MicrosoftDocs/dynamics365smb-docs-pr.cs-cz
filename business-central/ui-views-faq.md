---
title: Frequently Asked Questions about List Views
description: Detailed information about saving filters as list views.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 04/01/2020
ms.author: mikebc

---
# Nejčastějších dotazy - Seznamy
Toto téma odpovídá na otázky, na které se naši pokročilí uživatelé často ptají při práci se zobrazeními seznamu a ukládáním filtrů.

### Jak seznamy zpracovávají výrazy?
Při ukládání pohledu, který obsahuje filtry s výrazy, jako jsou časové období, operátory, klíčová slova nebo tokeny filtru, se uloží výraz a nikoli výsledné hodnoty. Například uložení zobrazení, které filtruje pole **Datum vytvoření** s výrazem **-1P..dnes** vždy najde záznamy vzhledem k aktuálnímu datu, i když je zobrazení přístupné až příští měsíc.

### Kde jsou uloženy seznamy?
Podobně jako skrytí políčka, nebo přeskládání vašeho navigačníhé menu se jedná o perzonalizaci, který je uložena v databázi. Vymazání veškeré personalizace bude mít za efekt také odstranění vaších seznamů a vymaže i další personalizaci, jako je například změna pořadí přehledů. Pro více informací navštivte [Přizpůsobení Vašeho pracovního prostoru](ui-personalization-user.md).

### Proč nemám ikonu Uložit?
Ikona uložení a nabídka možností se nezobrazují společně se zobrazeními v podokně filtrů, pokud je pro uživatele zakázáno přizpůsobení. Uživatelé, kteří nemají povolenou personalizaci, mají stále přístup k systémovým zobrazením, která jsou standardní součástí stránky pro úpravu nebo vytváření dalších filtrů.

### Na kterých typech stránek lze použít zobrazení seznamu?
Zobrazení jsou k dispozici pouze na seznamech a stránkách sešitů.

### Jsou k dispozici také pohledy na jiné formy?
Ano. Všechna zobrazení, která uložíte v prohlížeči pro stolní počítače nebo v aplikaci pro stolní počítače, budou k dispozici také na tabletu nebo smartphonu. Zobrazení na mobilních zařízeních nelze upravovat ani přizpůsobovat.

### Jsou moje pohledy vždy přístupné?
Stejné pohledy jsou k dispozici na stránce seznamu, pokud z ní přistupujete z navigačního podokna pomocí funkce **Řekněte mi** nebo pomocí okdazu URL na stránku seznamu. Pohledy nejsou k dispozici v částech seznamu, vyhledávání ani při zobrazení stránky seznamu jako dialogu.

### Jak mohu po úpravě vrátit seznam na původní filtry?
V dolní části podokna filtrů zvolte akci **Vymazat filtr** chcete-li vymazat změny filtrů, které jste provedli v zobrazení a vrátit se k původním filtrovaným polím a kritériím filtru.

### Jaký je rozdíl mezi skrytím a odebráním pohledů?
Odebráním pohledu se toto zobrazení trvale odstraní. Skrytí pohledů umožňuje dočasně skrýt zobrazení v podokně filtru, ale později jej můžete znovu zobrazit výběrem tlačítka **Zobrazit**.

### Jak mohu sdílet své pohledy s ostatními?
[!INCLUDE[d365fin](includes/d365fin_md.md)] neposkytuje způsob sdílení přesného zobrazení pohledu, ale můžete sdílet své aktuální filtry, aby ostatní uživatelé mohli vidět podobný pohled na záznamy. V prohlížeči pro stolní počítače jednoduše zkopírujte adresu URL a sdílejte ji se svými kolegy. Sdílení filtrů nezaručuje příjemci identickou sadu filtrů, které vidíte v prohlížeči.

### Mohu vyhledávat přehledy v okně Řekněte mi?
Ne. V okně **Řekněte mi** se zobrazují pouze výsledky vyhledávání pro stránku, ale po přechodu na stránku jste jen krůček od přechodu k oblíbenému zobrazení.

### Co je sdílené rozvržení?
Všechna pohledy na stránce seznamu sdílejí společné rozvržení sloupců, které zahrnuje souplce a jejich pořadí, šířku, podokno ukotvení a nastavení rychlého zadávání. Přizpůsobení libovolného rozložení sloupců ovlivní také další zobrazení sdílející stejné rozložení na stránce seznamu.

Některá systémová zobrazení mohou mít jedinečná rozložení sloupců v seznamu. Mohli například změnit uspořádání sloupců tak, aby zobrazovaly pouze sloupce nejrelevantnější pro toto zobrazení. Můžete určit, která zobrazení mají jedinečná rozložení, výběrem ikony ![Zobrazit více](media/show-more-options-icon.png "Zborazit více") se sjištěním, že políčko **Sdílené rozvržení** není zaškrtnuto. Jako uživatel si můžete přizpůsobit rozvržení sloupců pro pohled s jedinečným rozvržením, aniž by to ovlivnilo kterékoli z ostatních pohledů na stránce seznamu. Pouze vývojáři mohou definovat jedinečné rozložení sloupců pro zobrazení, které má sdílené rozložení.

### Co dělá odkaz Zobrazit systémové filtry?
Na některých stránkách seznamu se v podokně filtrů zobrazí **Zobrazit systémové filtry** v dolní části podokna filtrů, pokud stránka obsahuje filtry určené systémem. Tyto speciální filtry se obvykle používají k zobrazení záznamů na základě aktuálního kontextu, například když musí být seznam objednávek filtrován pro konkrétního zákazníka.

Systémové filtry jsou nastaveny vývojáři pomocí skupiny filtrů 0. Technické podrobnosti o systémových filtrech naleznete v části [Metody filtračních skupin](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method)

### Na své stránce vidím více pohledů, ale nevytvořil jsem je. Kde se tu vzali?
Pohledy, které vidíte v kterémkoli seznamu, jsou kombinací vašich osobních pohledů a systémových pohledů. Systémové pohledy mohou pocházet z obchodní aplikace, z rozšíření nebo mohou být specifická pro roli, pokud byl seznam přizpůsoben pro vaši roli.

### Proč některá zobrazení poskytují méně možností?
Některá pohledy poskytují pouze možnost uložení kopie zobrazení, zatímco jiná neumožňují uložení změn do pohledů. Způsob vytvoření pohledů určuje možnosti, které jsou pro toto zobrazení k dispozici. Pohledy lze vytvořit několika způsoby:
- Osobní, které jste uložili
- Systémové pohledy, která jsou standardní součástí obchodní aplikace nebo jsou přidány rozšířeními nebo zobrazeními specifických pro roli. Na rozdíl od osobních pohledů nelze uložit změny filtrů zpět do systémového zobrazení.
- Starší systémové pohledy, která jsou standardní součástí aplikace, ale byly vytvořeny pomocí starších verzí [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tyto pohledy nabízejí podstatně méně možností. Můžete je uložit pouze jako nové pohledy a nelze je skrýt ani přeřadit. Všimněte si, že starší pohledy systému budou ukončeny v budoucí aktualizaci [!INCLUDE[d365fin](includes/d365fin_md.md)].

### Jak převést starší systémové pohledy?
Starší systémové pohledy jsou zobrazení seznamu, která byly vytvořeny vývojáři ve starších verzích [!INCLUDE[d365fin](includes/d365fin_md.md)] umístěním na stránku Centrum rolí. Tyto pohledy jsou nyní zobrazena přímo na stránce seznamu, ale nabízejí zhoršené prostředí a výrazně méně možností. Starší systémové pohledy můžete převést na osobní pohledy, které jsou plně přizpůsobitelné, jednoduše uložením tohoto staršího pohledu jako nového. Podobně se správci mohou rozhodnout převést starší systémové pohledy specifické pro roli přizpůsobením uživatelem a uložením staršího pohledu jako nového pro specifickou roli.

Všimněte si, že starší pohledy systému budou ukončeny v budoucí aktualizaci [!INCLUDE[d365fin](includes/d365fin_md.md)].

### Ostatní v mé organizaci potřebují podobné pohledy jako standard. Co můžu dělat?
Práce s osobními pohledy je rychlá a efektivní, ale [!INCLUDE[d365fin](includes/d365fin_md.md)] poskytuje další nástroje pro definování pohledů seznamu potřebných konkrétními uživatelskými rolemi nebo všemi uživateli v organizaci.
- Vývojáři mohou přizpůsobit prostředí a vytvořit zobrazení seznamu rozšíření pro všechny uživatele v organizaci.
- Ne-programátoři jako jsou administrátoří nebo vedoucí oddělení mohou vytvářet seznamy specifické pro vybranou roli ze stránky **Profily**.

### Pracuji s několika jazyky: jak přeložím název seznamu?
Při ukládání nového seznamu nebo přejmenování existujícího je nutné zadat rozpoznatelný a smysluplný název tohoto seznamu. Název je uložen pro váš aktuální jazyk a zobrazí se také, když Vy nebo ostatní uživatelé pracujete s [!INCLUDE[d365fin](includes/d365fin_md.md)] v jiném jazyce. Chcete-li přejmenovat název seznamu, musíte přepnout jazyk pomocí stránky **Má nastavení** a poté přejmenovat seznam, ktery se uloží pod přeloženým názvem v novém jazyce.

### Fungují seznamy se výrazy ve všech jazycích?
Výrazy, které používají pouze symboly, například '**|**' nebo '**..**' , jsou považovány za bezpečné pro přístup uživatelů v jakémkoli jazyce Jakékoli seznamy s výrazy, které obsahují písmena, klíčová slova nebo tokeny filtru, budou fungovat pouze pro jazyk, ve kterém byly vytvořeny.


### Viz také
[Uložení a přizpůsobení zobrazení seznamu](ui-views.md)  
[Vyhledání funkcí a informací](ui-search.md)    
[Řazení, Vyhledávání a Filtrování](ui-enter-criteria-filters.md)
