---
title: Work with Dimensions| Microsoft Docs
description: You use dimensions to categorize entries, for example, by department or project, so you can easily track and analyze data.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 01/13/2020
ms.author: sgroespe

---
# Práce s dimenzemi
Chcete-li zjednodušit provádění analýzy dokladů, jako jsou prodejní objednávky, můžete použít dimenze. Dimenze jsou atributy a hodnoty, které kategorizují položky, takže je můžete sledovat a analyzovat. Například dimenze mohou označovat projekt nebo středisko, ze kterého pochází položka.

Například namísto zřízení samostatných finančních účtů pro každé oddělení a projekt můžete použít dimenze. To dává zajímavou příležitost k analýze, aniž by bylo nutné vytvořit složitou účetní osnovu. Pro více informací navštivte [Business Intelligence](bi.md).

Dalším příkladem je nastavení dimenze nazvané *Středisko* a její použití při účtování prodejních dokladů. To vám umožní použít nástroje business intelligence, abyste zjistili, které středisko prodalo které položky.
Čím více dimenzí používáte, tím podrobnější sestavy můžete vytvořit a pak na nich založit svá obchodní rozhodnutí. Jedna prodejní položka může například obsahovat více informací o dimenzích, například:

* Účet, do kterého byl prodej zboží zaúčtován
* Kde bylo zboží prodáno
* Kdo to prodal
* Typ zákazníka, který ho koupil

## Analýza pomocí dimenzí
Funkce Dimenze hraje důležitou roli v business inteligence, například při definování analytických pohledů. Pro více informací navštivte [Analýza dat podle dimenzí](bi-how-analyze-data-dimension.md).

> [!TIP]
> Rychlý způsob, jak analyzovat transakční data podle dimenzí je, že můžete filtrovat součty v tabulce účtů a záznamů na všech stránkách **položek** podle dimenzí. Vyhledejte akci **Nastavit filtr dimenze**.

## Sady dimenzí
Sada dimenzí je jedinečnou kombinací hodnot dimenzí. Je uložena jako položky sady dimenzí v databázi. Každá položka sady dimenzí představuje jednu hodnotu dimenze. Sada dimenze je označena společným ID, které je přiřazeno ke každé položce sady dimenze, která patří do dané sady.

Při vytváření řádku deníku, záhlaví dokladu nebo řádku dokladu můžete určit kombinaci hodnot dimenze. Namísto explicitního ukládání každé hodnoty dimenze v databázi je řádku deníku, záhlaví dokladu nebo řádku dokladu přiřazeno ID sady dimenzí, které určuje sadu dimenzí.

## Nastavení dimenzí
Můžete definovat dimenze a hodnoty dimenzí pro kategorizaci deníků a dokladů, například prodejních a nákupních objednávek. Dimenze nastavíte na stránce **Dimenze**, kde pro každou dimenzi můžete vytvořit jeden řádek, například *Projekt*, *Středisko*, *Oblast* nebo *Prodejce*.

Nastavte také hodnoty dimenzí. Hodnoty mohou být například oddělení ve vaší společnosti. Hodnoty dimenzí lze nastavit v hierarchické struktuře podobné účetní osnově, takže lze data rozdělit na různé úrovně a podskupiny hodnot dimenzí lze sčítat. Můžete definovat libovolný počet dimenzí a hodnot dimenzí a všichni ve vaší společnosti je mohou používat.

Když jsou nastaveny dimenze a jejich hodnoty, můžete definovat globální dimenze a zkratky dimenze na stránce **Nastavení financí**, které budou vždy k dispozici pro výběr polí na řádcích deníku a dokladu, aniž byste museli nejprve otevírat stránku **Dimenze**. Pro více informací navštivte [Nastavení globálních dimenzí a zkratek dimenzí](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globální dimenze** se používají jako filtry, například pro sestavy, dávkové úlohy a porty XML. Můžete použít pouze dvě globální dimenze, proto zvolte dimenze, které budete často používat.
* **Zkratky dimenzí** jsou k dispozici jako pole na řádcích deníku a dokladu. Můžete si jich vytvořit až šest.

### Nastavení výchozích dimenzí pro zákazníky, dodavatele a další účty
Můžete přiřadit výchozí dimenzi pro konkrétní účet. Dimenze bude zkopírována do deníku nebo dokladu, když zadáte číslo účtu na řádku, ale v případě potřeby můžete kód na řádku odstranit nebo změnit. Můžete také vytvořit dimenzi potřebnou pro zaúčtování položky s konkrétním typem účtu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dimenze** a poté vyberte související odkaz.
2. Na stránce **Dimenze** vyberte příslušnou dimenzi a pak zvolte akci **Výchozí dimenze typu účtu**.
4. Vyplňte řádek pro každou novou výchozí dimenzi, kterou chcete nastavit. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Pokud chcete vytvořit požadovanou domenzi, ale nechcete jí přiřadit výchozí hodnotu dimenze, nechte pole **Kód hodnoty dimenze** prázdné a poté vyberte **Nutný kód** v poli **Účtování hodnoty**.

> [!WARNING]
> Pokud je účet používán v dávkové úloze **Úprava směnných kurzů** nebo **Účtování nákladů na zboží**, nevybírejte **Nutný kód** nebo **Stejný kód**. Tyto dávkové úlohy nemohou používat kódy dimenze.

> [!NOTE]
> Pokud k účtu musí být přiřazena jiná dimenze než výchozí dimenze již nastavená pro typ účtu, musíte pro tento účet nastavit výchozí dimenzi. Výchozí dimenze pro jednotlivé účty pak nahradí výchozí dimenzi pro typ účtu.

### Nastavení výchozích priorit dimenzí
Různé typy účtů, například zákaznický účet a účet zboží, mohou mít nastaveny různé výchozí dimenze. V důsledku toho může mít položka pro dimenzi více než jednu výchozí dimenzi. Chcete-li se těmto konfliktům vyhnout, můžete použít pravidla priorit pro různé zdroje.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výchozí priority dimenzí** a poté vyberte související odkaz.
2. Na stránce **Výchozí priority dimenzí** zadejte do pole **Kód původu** kód pro tabulku vstupů, na kterou se budou vztahovat výchozí priority dimenze.
3. Vyplňte řádek pro každou výchozí prioritu dimenze, kterou chcete pro vybraný kód původu.
4. Opakujte postup pro každý kód původu, pro který chcete nastavit výchozí priority dimenze.

> [!IMPORTANT]
> Pokud nastavíte dvě tabulky se stejnou prioritou pro stejný kód původu, [!INCLUDE[d365fin](includes/d365fin_md.md)] vždy vybere tabulku s nejnižší hodnotou ID tabulky.

### Nastavení kombinací dimenzí
Chcete-li se vyhnout účtování položek s protichůdnými nebo irelevantními dimenzemi, můžete blokovat nebo omezit konkrétní kombinace dvou dimenzí. Kombinace blokovaných dimenzí znamená, že nemůžete účtovat obě dimenze na stejné položce bez ohledu na to, jaké jsou hodnoty dimenze. Omezená kombinace dimenzí umožňuje účtovat obě dimenze na stejné položce, ale pouze pro určité kombinace hodnot dimenze.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kombinace dimenzí** a poté vyberte související odkaz.
2. Na stránce **Kombinace dimenzí** vyberte pole kombinace dimenze a vyberte jednu z následujících možností.

   | Pole | Popis |
   |----------------------------------|---------------------------------------|  
   | **Bez omezení** | Tato kombinace dimenzí nemá žádná omezení. Všechny hodnoty dimenzí jsou povoleny. |
   | **Omezeno** | Tato kombinace dimenzí má omezení v závislosti na tom, které hodnoty dimenze zadáte. Omezení musíte definovat na stránce **Kombinace hodnoty dimenze**. |
   | **Uzavženo** | Tato kombinace dimenzí není povolena. |

3. Pokud jste vybrali možnost **Omezeno** musíte definovat, které kombinace hodnot dimenzí jsou blokovány. Chcete-li to provést, vyberte pole pro definování kombinace dimenzí.
4. Nyní vyberte kombinaci hodnoty dimenzí, která je blokována, a do pole zadejte **Uzavženo**. Prázdné pole znamená, že je kombinace hodnot dimenzí povolena. Opakujte, pokud je blokováno více kombinací.

> [!NOTE]
> Stejné dimenze jsou zobrazeny v řádcích i sloupcích, a proto se všechny kombinace dimenzí objevují dvakrát. [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky zobrazí nastavení v obou polích. V polích z levého horního rohu směrem k pravému dolnímu rohu nemůžete vybrat nic, protože tato pole mají v řádcích i sloupcích stejnou dimenzi.
> Vybraná možnost není před ukončením pole viditelná.
> Chcete-li místo dimenze zobrazit název dimenze, vyberte pole **Zobrazit název sloupce**.

### Nastavení globálních dimenzí a zkratek dimenzí
Globální a zkratkové dimenze lze použít jako filtr kdekoli v [!INCLUDE[d365fin](includes/d365fin_md.md)], včetně zpráv, dávkových úloh a zobrazení analýzy. Globální dimenze a zkratky dimenze jsou vždy k dispozici pro přímé vložení bez prvního otevření stránky **Dimenze**. Na řádcích deníku a dokladu můžete v poli na řádku vybrat globální dimenzi a zkratku dimenze. Můžete nastavit dvě globální dimenze a osm zkratek. Zvolte dimenze, které používáte nejčastěji.

> [!Important]
Změna globální dimenze nebo zkratky dimenze vyžaduje, aby byly aktualizovány všechny položky účtovány s touto dimenzí. Tuto úlohu můžete provést pomocí funkce **Změna globálních dimenzí**, ale pozor, může to být časově náročné a může to ovlivnit výkon. Proto pečlivě zvolte globální dimenze a zkratky dimenze, abyste je později nemuseli měnit.

> [!Note]
Když přidáte nebo změníte globální dimenzi nebo zkratku dimenze, budete automaticky odhlášeni a znovu přihlášenï na to aby byla nová hodnota připravena k použití v celé aplikaci.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení financí** a poté vyberte související odkaz.
2. Na záložce **Dimenze** vyplňte pole. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Změna globálních dimenzí
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Změna globálních dimenzí** a poté vyberte související odkaz.
2. Umístěním kurzoru na akce a pole na stránce se dozvíte, jak změnit globální dimenze a zkratky dimenze.

### Příklad nastavení dimenze
Řekněme, že vaše společnost chce sledovat transakce na základě organizační struktury a zeměpisných lokací. Chcete-li to provést, můžete na stránce **Dimenze** nastavit dvě dimenze:

* **OBLAST**
* **STŘEDISKO**

| Kód | Název | Titulek kódu | Titulek filtru |
| --- | --- | --- | --- |
| OBLAST | Oblast | Kód oblasti | Filtr oblasti |
| STŘEDISKO | Středisko | Kód střediska | Filtr střediska |

Pro **OBLAST** přidejte následující hodnoty dimenze:

| Kód | Název | Typ hodnoty dimenze |
| --- | --- | --- |
| 10 | Amerika | Od-součet |
| 20 | Severní Amerika | Standard |
| 30 | Pacifik | Standard |
| 40 | Jižní Amerika | Standard |
| 50 | Amerika, Celkem | Do-součet |
| 60 | Evropa | Od-součet |
| 70 | EU | Standard |
| 80 | mimo EU | Standard |
| 90 | Evropa, celkem | Do-součet |

Pro dvě hlavní geografické oblasti, Ameriku a Evropu přidáte podkategorie pro regiony odsazením hodnot dimenzí. Umožní vám to podat zprávu o prodeji nebo výdajích v regionech a získat součty za větší geografické oblasti. V závislosti na vaší firmě můžete také použít země nebo oblasti jako hodnoty dimenze nebo okresy nebo města.

> [!NOTE]
K nastavení hierarchie musí být kódy v abecedním pořadí. To zahrnuje kódy hodnot dimenzí, které jsou uvedeny v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Pro **STŘEDISKO** přidáte následující hodnoty dimenze:

| Kód | Název | Typ hodnoty dimenze |
| --- | --- | --- |
| ADM | Administrativa | Standard |
| VÝROBA | Výroba | Standard |
| PRODEJ | Prodej | Standard |

S tímto nastavením můžete přidat své dvě dimenze jako dvě globální dimenze na stránce **Nastavení financí**. To znamená, že můžete použít OBLAST a STŘEDISKO jako filtry pro věcné položky, stejně jako na všechny sestavy a účetní schémata. Obě globální dimenze jsou také automaticky k dispozici pro použití na vstupních řádcích a záhlavích dokladů jako zkratky dimenze.

## Získání přehledu o dimenzích použitých vícekrát
Stránka **Výchozí dimenze-více** určuje, jak skupina účtů používá dimenze a hodnoty dimenzí. Můžete to provést zvýrazněním více účtů a zadáním výchozích dimenzí a hodnot dimenzí pro všechny účty, které jste zvýraznili v seznamu účtů. Pokud zadáte výchozí dimenze pro zvýrazněné účty, aplikace navrhne tyto dimenze a hodnoty dimenzí při každém použití jednoho z těchto účtů, například na řádku deníku. To uživateli usnadňuje účtování položek, protože pole pro dimenze jsou vyplňována automaticky. Navrhované hodnoty dimenze však lze změnit a to například na řádku deníku.

Stránka **Výchozí dimenze-více** obsahuje následující pole:

| Pole | Popis |
|-----|-----------|  
| **Kód dimenze** | Zobrazuje všechny dimenze, které byly definovány jako výchozí dimenze na jednom nebo více zvýrazněných účtech. Výběrem pole zobrazíte seznam všech dostupných dimenzí. Pokud vyberete dimenzi, vybraná dimenze bude definována jako výchozí dimenze pro všechny zvýrazněné účty. |
| **Kód hodnoty dimenze** | Zobrazuje buď hodnotu jedné dimenze, nebo termín (Konflikt). Pokud je v poli zobrazena hodnota dimenze, mají všechny zvýrazněné účty stejnou výchozí hodnotu dimenze. Pokud je v poli zobrazen termín (Konflikt), ne všechny zvýrazněné účty mají pro dimenzi stejnou výchozí hodnotu dimenze. Výběrem pole zobrazíte seznam všech dostupných hodnot dimenzí. Pokud vyberete hodnotu dimenze, bude vybraná hodnota definována jako výchozí hodnota dimenze pro všechny zvýrazněné účty. |
| **Účtování hodnoty** | Zobrazuje buď pravidlo účtování s jednou hodnotou nebo termín (konflikt). Pokud je v poli zobrazeno pravidlo účtování hodnoty, mají všechny zvýrazněné účty stejné pravidlo účtování hodnoty pro hodnotu dimenze. Pokud je termín (Konflikt) zobrazen v poli, pak ne všechny zvýrazněné účty mají stejné pravidlo účtování hodnoty pro hodnotu dimenze. Výběrem pole Účtování hodnoty se zobrazí seznam pravidel účtování hodnoty. Pokud vyberete pravidlo účtování hodnoty, bude použito pro všechny zvýrazněné účty. |

## Použití dimenzí
V dokladu, jako je například prodejní objednávka, můžete přidat informace o dimenzi pro jednotlivý řádek dokladu i pro samotný doklad. Například na stránce **Prodejní objednávky** můžete zadat hodnoty dimenze pro první dvě zkratky dimenze na jednotlivých prodejních řádcích a můžete přidat další informace o dimenzích, pokud zvolíte tlačítko **Dimenze**.

Pokud místo toho pracujete v deníku, můžete do položky přidat informace o dimenzi stejným způsobem, pokud jste nastavili zkratku dimenze jako pole přímo na řádcích deníku.

Můžete nastavit výchozí dimenze pro účty nebo typy účtů, aby se dimenze a hodnoty dimenzí vyplňovaly automaticky.

### Zobrazení globálních dimenzí na stránce položek hlavní knihy
Globální dimenze jsou vždy definovány společností a pojmenovány společností. Chcete-li zobrazit globální dimenze vaší společnosti, otevřete stránku **Nastavení financí**.

Na stránce položky hlavní knihy můžete vidět, zda existují globální dimenze pro položky. Dvě globální dimenze se liší od ostatních vašich dimenzí, protože je můžete použít jako filtry kdekoli v [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
2. Na stránce **Účetní osnova** vyberte akci **Položky**.
3. Chcete-li zobrazit pouze položky, které jsou relevantní, nastavte na stránce jeden nebo více filtrů.
4. Chcete-li zobrazit všechny dimenze pro položku, vyberte položku a poté vyberte akci  **Dimenze**.

> [!NOTE]
Na stránce **Dimenze položek** jsou pak zobrazeny dimenze pro jednu položku. Při procházení položek účetní knihy se odpovídajícím způsobem mění obsah na stránce **Dimenze položek**.

## Odstraňování chyb v dimenzích
Při účtování dokladů nebo řádků deníku, které obsahují dimenze, mohou nastat různé chyby, které obvykle souvisejí s nesprávným nastavením nebo přiřazením dimenzí.

> [!NOTE]
V následujícím seznamu potenciálních chybových zpráv jsou kódy *%X* zástupnými symboly pro datové proměnné, které bude skutečná zpráva obsahovat v uživatelském rozhraní v závislosti na kontextu. Například, *%1 %2 je uzavřena.* se může objevit v uživatelském rozhraní jako „Kód dimenze OBLAST je uzavřen.“.

| Problém | Chybové hlášení | Možné řešení |
|-----|-------------|-----------------|
| Blokovaná dimenze | %1 %2 je uzavřena. | - Vyhledejte nezaúčtované doklady obsahující sadu dimenzí s uzavřenou dimenzí a otevřete ji.<br />- Odstraňte nastavené řádky dimenze pro uzavřenou dimenzi. |
| Odstranění dimenze | %1 %2 nelze najít. | - Obnovte chybějící dimenzi.<br /> - Najděte nezaúčtované doklady obsahující sadu dimenzí s chybějící dimenzí a přidejte ji.<br />- Odstraňte nastavené řádky dimenze pro chybějící dimenzi. |
| Hodnota blokované dimenze | %1 %2 - %3 je uzavřena. | - Vyhledejte nezaúčtované doklady obsahující sadu dimenzí s uzavřenou hodnotou dimenze a otevřete ji.<br />- Odstraňte řádek sady dimenze pro uzavřenou hodnotu dimenze. |
| Hodnota smazané dimenze | %1 pro %2 chybí. | - Obnovte chybějící hodnotu dimenze.<br />-Najděte nezaúčtované doklady obsahující sadu dimenzí s chybějící hodnotou dimenze a přidejte ji. <br />- Odeberte řádek sady dimenze pro chybějící hodnotu dimenze. |
| Hodnota zakázané dimenze | Typ hodnoty dimenze pro %1 %2 - %3 nesmí být %4. | - Změňte pole **Typ hodnoty dimenze** na stránke **Hodnoty dimenze** na **Standardní** nebo **Od-součet**.<br /> - Odeberte řádek sady dimenzí pro uzavřenou hodnotu dimenze. |
| Kombinace uzavřených dimenzí | Dimenze %1 a %2 nelze použít současně. | -Najděte nezaúčtované doklady obsahující sadu dimenzí s kombinací uzavžených dimenzí a otevřete ji.<br />- Upravte jeden z konfliktních řádků sady oprávnění pro kombinaci dimenze. |
| Kombinace hodnoty uzavřené dimenze | Kombinace dimenze %1 - %2 a %3 - %4 nelze použít současně. | -Vyhledejte nezaúčtované doklady obsahující sadu dimenze pomocí kombinace uzavřených hodnot dimenze a otevřete je.<br />- Upravte jeden z konfliktních řádků sady oprávnění pro kombinaci hodnoty dimenze. |
| Prázdný kód hodnoty dimenze pro výchozí dimenzi, kde pole **Účtování hodnoty** obsahuje **Nutný kódy** | -Vyberte %1 pro %2 %3.<br />-Vyberte %1 pro %2 %3 pro %4 %5. | - Změňte pole **Účtování hodnoty** na stránce **Výchozí dimenze**.<br />- Zadejte neprázdnou hodnotu dimenze pro konfliktní dimenzi v sadě dimenze. |
| Chybný kód hodnoty dimenze pro výchozí dimenzi, kde pole **Účtování hodnoty** obsahuje **Stejný kód** | -Vyberte %1 %2 pro %3 %4.<br />-Vyberte %1 %2 pro %3 %4 pro %5 %6 | -Změnte pole **Účtování hodnoty** na stránce **Výchozí dimenze**.<br />- Zadejte požadovanou hodnotu dimenze pro konfliktní dimenzi v sadě dimenze. |
| Neprázdný kód hodnoty dimenze pro prázdnou výchozí dimnezi, kde pole **Účtování hodnoty** obsahuje **Stejný kód** | -%1 %2 musí být prázdné.<br />-%1 %2 musí být prázdné pro %3 %4. | -Změňte pole **Účtování hodnoty** na stránce **Výchozí dimenze**.<br />- Zadejte prázdný kód hodnoty dimenze pro konfliktní dimenzi v sadě dimenze. |
| Neočekávaná hodnota dimneze pro výchozí dimenzi, kde pole **Účtování hodnoty** neobsahuje **Žádný kód** | -%1 %2 nesmí být uvedeno.<br />-%1 %2 nesmí být uvedeno pro %3 %4 | -Změňte pole **Účtování hodnoty** na stránce **Výchozí dimenze**.<br />-Odeberte konfliktní řádek ze sady dimenze. |

## Viz související školení na webu [Microsoft Learn](/learn/modules/dimensions-dynamics-365-business-central/index)

## Viz také
[Business Intelligence](bi.md)  
[Finance](finance.md)  
[Analýze dat dle dimenzí](bi-how-analyze-data-dimension.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
