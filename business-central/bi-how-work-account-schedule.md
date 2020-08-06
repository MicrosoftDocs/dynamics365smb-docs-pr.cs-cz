---
title: Build financial reports using account schedules
description: Describes how to use account schedules to create various views and report for analyzing financial performance data.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 02/12/2020
ms.author: edupont

---
# Příprava finančních výkazů s účetními schématy a kategoriemi účtů
Pomocí účetních schémat získáte přehled o finančních datech uložených v účetní osnově. Účetní schémata analyzují údaje v účetních závěrkách a porovnávají položky hlavní knihy s položkami rozpočtu hlavní knihy. Výsledky se zobrazují v grafech v Centru rolí, například v grafu cashflow a v sestavách, jako je rozvaha výsledovka.

K těmto dvěma sestavám získáte přístup například pomocí akce **Finanční výkazy** v Centrech rolí Obchodního manažera a Účetního.

[!INCLUDE[d365fin](includes/d365fin_md.md)] poskytuje několik ukázkových plánů účtů, které můžete okamžitě použít, nebo můžete nastavit vlastní řádky a sloupce pro určení čísel, které chcete porovnat. Můžete například vytvořit účetní schémata pro výpočet ziskových marží pro dimenze, jako jsou oddělení nebo skupiny zákazníků. Můžete vytvořit tolik vlastních finančních výkazů, kolik chcete.

Nastavení účetních schémat vyžaduje pochopení finančních dat v účetní osnově. Můžete například zobrazit položky hlavní knihy jako procenta položek rozpočtu. To vyžaduje vytvoření rozpočtů. Pro více informací navštivte [Vytvoření finančních rozpočtů](finance-how-create-budgets.md).

## Účetní schémata
Účetní schémata se používají k uspořádání účtů uvedených v účetní osnově způsobem, který je vhodný pro prezentaci informací o těchto účtech. Můžete nastavit různá rozvržení pro definování informací, které chcete získat z účetní osnovy. Jednou z hlavních funkcí účetních schémat je poskytnout místo pro výpočty, které nelze provést přímo v účetní osnově, jako je například vytváření mezisoučtů pro skupiny účtů, které mohou být zahrnuty do nových součtů a pak mohou být použity v jiných součtech. Uživatelé mohou například vytvářet účetní schémata pro výpočet ziskových marží pro takové dimenze, jako jsou oddělení nebo skupiny zákazníků. Kromě toho lze filtrovat položky hlavní knihy a položky rozpočtu hlavní knihy, například podle čisté změny nebo částky Má dáti.

Pomocí vzorců můžete také porovnat dvě nebo více účetních schémat a rozložení sloupců. Tento druh porovnání poskytuje možnost:

* Vytvářet vlastní finanční sestavy.
* Vytvářet tolik účetních schémat kolik bude potřeba, každý s jedinečným názvem.
* Nastavit různá rozvržení sestav a tisk sestavy s aktuálními čísly.

## Kategorie finančního účtu
Kategorie finančních účtů můžete použít ke změně rozvržení finančních výkazů. Po nastavení kategorií účtu na stránce **Kategorie finančního účtu** zvolením akce **Generovat účetní schémata** se vygenerují základní účty pro základní finanční sestavy, které jsou aktualizovány. Při příštím spuštění jedné z těchto sestav, například **Rozvaha**, budou přidány nové součty a podúčty na základě vašich změn.

> [!NOTE]
> Kategorie účtu nejvyšší úrovně, například uzel **Pasiva** jsou pevné a nelze přidat své vlastní. Můžete však odstranit a přidat kategorie účtů na nižších úrovních a změnit jejich strukturu a definovat, jak se související přehled účtů objeví v přehledech.<br /><br />
> Doporučuje se vytvořit a strukturovat své vlastní kategorie účtů nižší úrovně na začátku v hierarchii, pokud je to nutné, namísto pokusu o změnu uspořádání stávajících. Můžete například restrukturalizovat uzel **Závazků** tak, aby obsahoval nový uzel **Vlastní kapitál**  následovaný uzly **Krátkodobé závazky** a **Dlouhodobé  závazky**.

## Vytvoření nového účetního schématu
Účetní schémata slouží k analýze číselných údajů na účtech hlavní knihy nebo k porovnání položek hlavní knihy s položkami rozpočtu hlavní knihy. Můžete například zobrazit položky hlavní knihy jako procenta položek rozpočtu.

Účetní schémata ve standardní verzi [!INCLUDE[d365fin](includes/d365fin_md.md)] jsou základem standardních finančních výkazů, které nemusí vyhovovat potřebám vašeho podnikání. Chcete-li rychle vytvořit vlastní finanční sestavy, můžete začít kopírováním existujícího účetního schématu. Viz krok 3 níže.

**Náhled účetního schématu** je místo, kde zobrazíte náhled finanční sestavy, kterou definuje účetní schéma. V následujícím textu je důležité si uvědomit to, co nastavíte jako řádky a sloupce účetního schématu, lze zobrazit a ověřit pouze na stránce **Náhledu účetního schématu**, kterou otevřete z účetího schématu pomocí tlačítka **Náhled**. Stránka **Účetního schématu** je pouze oblast nastavení.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní schémata** a poté vyberte související odkaz.
2. Na stránce **Účetní schémata** zvolte tlačítko **Nový** a vytvořte nový název účetního schématu.
3. Případně zvolte tlačítko **Kopírovat účetní schéma**, vypňte dvě políčka, a poté stiskněte tlačítko **OK**.
4. Podle potřeby vyplňte pole. V poli **Výchozí rozložení sloupce** vyberte existující rozložení. Pokud chcete, můžete jej upravit později.

   Rozložení sloupců slouží k definování sloupců pro různé parametry, podle kterých jsou zobrazena finanční data na řádcích. Můžete například navrhnout rozložení sloupce pro porovnání čisté změny a zůstatku za stejné období letošního a minulého roku ve čtyřech sloupcích. Pro více informací navštivte [Úprava rozložení sloupců](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Zvolte tlačítko **Upravit účetní schéma**.
6. Vytvořte řádek pro každý finanční prvek, který chcete v přehledu zobrazit, například jeden řádek pro aktuální aktiva a druhý řádek pro dlouhodobá aktiva. Inspiraci najdete v existujících účetních schématech v demonstrační společnosti CRONUS.
7. Zvolte tlačítko **Náhled**, chcete-li zobrazit výslednou finanční sestavu.
8. Na stránce **Přehledu účetních schémat**, v poli **Název rozložení sloupce**, vyberte jiné rozložení sloupců a zobrazte finanční údaje podle jiných parametrů.
9. Vyberte tlačítko **OK**.

Nyní jste definovali základ účetního schématu, řádky finančních dat, která mají být zobrazena a existující rozložení sloupců, které zobrazí data na řádcích podle různých parametrů. Pokud výchozí rozložení sloupců, které jste vybrali v kroku 4, nevyhovuje vašemu účelu, postupujte podle následujícího postupu.

### Úprava rozložení sloupců
Rozložení sloupců slouží k definování sloupců, které mají být zahrnuty do výsledné sestavy. Můžete například navrhnout rozložení pro porovnání čisté změny a zůstatku za stejné období tohoto roku a loňského roku.

> [!NOTE]
> Tištěná/náhledová/uložená verze účetního schématu může zobrazit maximálně pět sloupců. Pokud je účetní schéma určeno pouze pro analýzu na stránce **Přehledu účetních schémat**, můžete vytvořit tolik sloupců, kolik chcete.

1. Na stránce **Účetní schémata**, vyberte příslušné účetní schéma a pak zvolte talčítko **Upravit rozložení sloupců.**
2. Na stránce **Rozložení sloupců**, vytvořte řádek pro každý sloupec, podle kterého jsou finanční data zobrazena ve finanční sestavě. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vyberte tlačítko **OK**.
4. Otevřete  **Přehled účetních schémat** abyste ověřili, že nové rozvržení sloupců funguje jak má.

> [!NOTE]
> Sloupce, které definujete v každém řádku, představují sloupce 3 a vyšší na stránce **Přehled účetních schémat**. První dva sloupce, **Číslo řádku** a **Popis** jsou pevné.

### Vytvoření sloupce, který vypočítává procenta
Někdy můžete chtít zahrnout sloupec do účetního schématu pro výpočet procent z celkového počtu. Například, pokud máte několik řádků, které rozdělují tržby podle dimenzí, můžete chtít, aby sloupec označil procento z celkových prodejů, které každý řádek představuje.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní schémata** a poté vyberte související odkaz.
2. Na stránce **Názvy účetních schémat** vyberte účetní schéma.
3. Zvolte akci **Upravit účetní schéma** a nastavte řádek účetního schématu pro výpočet součtu, na kterém budou procenta založena.
4. Vložte řádek bezprostředně nad první řádek, pro který chcete zobrazit procento.
5. Vyplňte pole na řádku takto: Do pole **Typ součtu** vložte **Nastavit základ pro procenta**. V poli **Součet** zadejte vzorec pro celkový součet, na kterém bude procentuální hodnota založena. Pokud například řádek 11 obsahuje celkový prodej, zadejte **11**.
6. Zvolte akci **Nastavení rozložení sloupců** k nastavení sloupce.
7. Vyplňte pole na řádku takto: V poli **Typ sloupce** vyberte **Vzorec** . Do pole **Vzorec** zadejte vzorec pro částku, pro kterou chcete vypočítat procento, následovanou hodnotou %. Pokud například sloupec číslo N obsahuje pohyb, zadejte **N%** .
8. Opakujte kroky 4 až 7 pro každou skupinu řádků, které chcete rozdělit podle procent.

## Nastavení účetních schémat s náhledy
Účetní schémata můžete použít k vytvoření výkazu porovnávajícího čísla hlavní knihy a obecné údaje o rozpočtu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní schémata** a poté vyberte související odkaz.
2. Na stránce **Názvy účetních schémat** vyberte účetní schéma.
3. Zvolte akci **Upravit účetní schéma**.
4. Na stránce **Účetnícho schématu** v poli **Název** vyberte výchozí název pro schéma.
5. Vyberte akci **Vložit účty**.
6. Vyberte účty, které chcete zahrnout do výkazu, a pak zvolte tlačítko **OK**.

   Účty jsou nyní vloženy do vašeho účetního schématu. Pokud chcete, můžete také změnit rozložení sloupce.
7. Zvolte talčítko **Náhled**.
8. Na stránce **Přehledu finančních schémat**, v záložce **Filtry dimenzí** nastavte filtr rozpočtu na požadovaný název filtru..
9. Vyberte tlačítko **OK**.

Nyní můžete zkopírovat a vložit výkaz rozpočtu do tabulky.

## Porovnání účetních období pomocí vzorců za období
Účetní schéma může porovnat výsledky různých účetních období, například tento měsíc oproti stejnému měsíci loňského roku. Chcete-li to provést, přidejte sloupec s polem **Vzorec srovnávacího úč.období** a potom nastavte toto pole na vzorec období.

Účetní období nemusí odpovídat kalendáři, ale každý fiskální rok musí mít stejný počet účetních období, i když každé období se může lišit délkou.

[!INCLUDE[d365fin](includes/d365fin_md.md)] používá vzorec období k výpočtu částky z období porovnání ve vztahu k období reprezentovanému filtrem data v okně před tiskem sestavy. Období srovnání je založeno na období počátečního data filtru data. Zkratky pro specifikace období jsou:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Zkratka</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>P</p></td>
<td><p>Období</p></td>
</tr>
<tr class="even">
<td><p>LP</p></td>
<td><p>Poslední období fiskálního roku, půl roku nebo čtvrtletí.</p></td>
</tr>
<tr class="odd">
<td><p>CP</p></td>
<td><p>Běžné období fiskálního roku, pololetí nebo čtvrtletí.</p></td>
</tr>
<tr class="even">
<td><p>FY</p></td>
<td><p>Fiskální rok. Například FY[1..3] označuje první čtvrtletí aktuálního fiskálního roku</p></td>
</tr>
</tbody>
</table>

Příklady vzorců:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vzorec</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Prázdný></p></td>
<td><p>Aktuální období</p></td>
</tr>
<tr class="even">
<td><p>-1P</p></td>
<td><p>Předchozí období</p></td>
</tr>
<tr class="odd">
<td><p>-1FY[1..LP]</p></td>
<td><p>Celý předchozí fiskální rok</p></td>
</tr>
<tr class="even">
<td><p>-1FY</p></td>
<td><p>Aktuální období v předchozím fiskálním roce</p></td>
</tr>
<tr class="odd">
<td><p>-1FY[1..3]</p></td>
<td><p>První čtvrtletí předchozího fiskálního roku</p></td>
</tr>
<tr class="even">
<td><p>-1FY[1..CP]</p></td>
<td><p>Od začátku předchozího fiskálního roku do aktuálního období v předchozím fiskálním roce, včetně</p></td>
</tr>
<tr class="odd">
<td><p>-1FY[CP..LP]</p></td>
<td><p>Od aktuálního období v předchozím fiskálním roce do posledního období předchozího fiskálního roku, včetně</p></td>
</tr>
</tbody>
</table>

Chcete-li vypočítat podle pravidelných časových období, musíte místo toho zadat vzorec do pole **Vzorec srovnávacího úč.období**.

> [!NOTE]
> Není vždy transparentní, která období porovnáváte, protože můžete nastavit filtr data v sestavě, která zahrnuje jiná data než účetní období, která se odráží v datech v účtové osnově. Můžete například vytvořit účetní schéma, ve kterém chcete porovnat toto období se stejným obdobím minulého roku, takže nastavíte pole **Vzorec srovnávacího úč.období**  na  *-1FY* . Poté spustíte sestavu 28. února a nastavíte filtr data na leden a únor. V důsledku toho účetní schéma porovnává leden a únor letošního roku s lednem loňského roku, což je jediné dokončené účetní období dvou za loňský rok.

## Viz souvisejnící školení [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## Viz také
[Business Intelligence](bi.md)  
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Hlavní kniha a účetní osnova](finance-general-ledger.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
