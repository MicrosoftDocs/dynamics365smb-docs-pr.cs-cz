---
    title: Setting Up Cost Accounting | Microsoft Docs
    description: Before you start working with cost accounting, you must perform setup tasks.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Nastavení nákladového účetnictví
Než začnete pracovat s nákladovým účetnictvím, musíte provést úkoly nastavení.

## Rovnováha medzi typem nákladů, nákladovým střediskem a nositelem nákladů
Při nastavování nákladového účetnictví se musíte ujistit, že všechny položky jsou přiřazeny k typu nákladů a nákladovému středisku nebo nositeli nákladů. To znamená, že každé položce nákladů musí být přiřazen typ nákladů a kód nákladového střediska nebo nositel nákladů. Toto pravidlo zajišťuje, že každá položka nákladů se zobrazí v nákladových střediscích nebo nositelech nákladů, ale nikdy na obou naraz.

Tímto způsobem vytvoříte následující účetní rovnici:

*Saldo druhu nákladů* = *Saldo nákladového strědiska* + *Saldo nositele nákladů*

Při tisku osnovy typu nákladů, osnovy nákladových středisek a osnovy sestav nositelů nákladů můžete tento vztah analyzovat.

## Nastavení druhů nákladů
Tabulka druhů nákladů je podobná účetní osnově v hlavní knize. Tabulku druhů nákladů můžete nastavit následujícími způsoby:

- Vytvořte osnovy druhů nákladů podobných účtům výkazu zisku a ztráty v účetní osnově. Poté můžete převést účetní osnovu hlavní knihy do osnovy druhů nákladů. Po převodu můžete provést potřebné úpravy.
- Vytvořte novou osnovu druhů nákladů nebo přidejte nové druhy nákladů do stávající osnovy druhů nákladů. Každý nový druh nákladů musíte vytvořit samostatně.

### Převod účetní osnovy hlavní knihy do osnovy druhů nákladů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Osnova druhů nákladů** a poté vyberte související odkaz.
2. Vyberte akci **Získat druhy nákladů z účetní osnovy**. V dialogovém okně zvolte tlačítko **Ano** pro potvrzení přenosu. Funkce používá účetní osnovu k vytvoření osnovy druhů nákladů.

   Osnova druhů nákladů nyní obsahuje všechny účty výsledovky v hlavní knize a obsahuje nadpisy a mezisoučty. Podle potřeby můžete změnit osnovu druhů nákladů. Můžete například odstranit existující duplicity druhů nákladů.

   > [!IMPORTANT]
   > Funkce **Zapsat druhy nákladů do účetní osnovy** aktualizuje vztah mezi účetní osnovou a osnovou druhů nákladů. Pole **Číslo** je vyplněno a ověřeno, aby bylo zajištěno, že každý účet hlavní knihy souvisí pouze s jedním druhem nákladů. Funkce se spustí automaticky před převodem věcných položek do nákladového účetnictví.

### Nastavení nových druhů nákladů na stránce Osnova druhů nákladů
1. Otevřete stránku **Osnova druhů nákladů** v režimu úprav.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Druhy nákladů můžete nastavit a udržovat na stránce **Karta druhu nákladů** nebo na stránce **Osnova druhů nákladů**. V tomto postupu nastavíte druhy nákladů na stránce **Osnova druhů nákladů**.

3. Po vytvoření všech typů nákladů vyberte akci **Odsadit druhy nákladů**. V dialogovém okně vyberte tlačítko **Ano**.
4. Propojte nový druh nákladů s odpovídajícím účtem hlavní knihy.

   > [!IMPORTANT]
   > Pokud jste do pole **Součet** zadali definice pro typ řádku **Do-součet** před spuštěním funkce **Odsadit druhy nákladů**, pak musíte znovu zadat definice, protože funkce přepíše hodnoty ve všech polích **Do-součet**.

### Aktualizace druhů nákladů
1. Na stránce **Nastavení nákladového účetnictví** vyberte, zda chcete, aby se osnova druhů nákladů automaticky aktualizovala při změně účetní osnovy.
2. V poli **Připojit fin.účet** si můžete vybrat z následujících možností.

- **Ne** - Při změně účetní osnovy nedochází k žádné odpovídající změně v osnově druhů nákladů.
- **Automaticky** - Při změně účetní osnovy se v osnově druhů nákladů provádí odpovídající změna.
- **Po dotazu** - Zobrazí se zpráva s dotazem, zda chcete provést odpovídající změnu v osnově druhů nákladů při změně účetní osnovy.

## Definování vztahu mezi druhy nákladů a účty hlavní knihy
Vztah mezi druhem nákladů a účtem hlavní knihy je vytvořen v druhu nákladů a v účtu hlavní knihy.

* Pole **Rozmezí fin. účtu** v tabulce **Druh nákladů** stanoví, které účty hlavní knihy patří k druhu nákladů.
* Pole **Číslo druhu nákladů** v účtové osnově určuje, ke kterému typu nákladů patří účet hlavní knihy.

Tato dvě pole jsou vyplněna automaticky při použití funkce **Získat druhy nákladů z účetní osnovy**.

### Vztah mezi účty hlavní knihy a druhy nákladů
Existuje vztah n:1 mezi účty hlavní knihy a druhy nákladů. K jednomu druhu nákladů může patřit několik účtů hlavní knihy, ale každý účet hlavní knihy patří pouze k jednomu druhu nákladů. Následující tabulka popisuje podrobnosti ve vztahu.

| Vztah | **Rozmezí fin. účtu** | **Číslo druhu nákladů** |
|------------------|------------------------------------------------|-------------------------------------------|  
| Jeden účet hlavní knihy pro každý druh nákladů | Jeden účet hlavní knihy | Jeden druh nákladů |
| Několik účtů hlavní knihy pro jeden druh nákladů | Rozsah účtu hlavní knihy, například 7110..7193 pro každý účet hlavní knihy | Pro každý účet hlavní knihy v rozsahu existuje pouze jeden druh nákladů |
| Druhy nákladů bez odpovídajících účtů hlavní knihy | <Empty> |
| Finanční účty, jejichž položky nebudou převedeny | <Empty> |

### Druhy nákladů bez vztahu k hlavní knize
Druh nákladů nemusí mít vztah k účtům hlavní knihy, pokud je splněna jedna z následujících podmínek:

* Účty pro provozní účetnictví, například Kalk.  úroků a odpisů, berou pouze náklady z provozního účetnictví.
* Pomocné druhy nákladů, jako jsou typy nákladů 9901, 9902 a 9903 v databázi [!INCLUDE[d365fin](includes/d365fin_md.md)], se používají jako kreditní a debetní účty pro rozdělení.
* Pomocný účet 9920 v databázi [!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje skutečné účetní rezervy, které ukazují rozdíl mezi náklady a výdaji z hlavní knihy.

## Nastavení nákladových středisek
Nákladová střediska jsou oddělení, která odpovídají za náklady a příjmy. Osnova nákladových středisek je podobná informacím o dimenzi pro hlavní knihu. Osnova nákladových středisek můžete nastavit následujícími způsoby:

- Přeneste hodnoty dimenzí v hlavní knize do osnovy nákladových středisek. Po převodu můžete provést potřebné úpravy.
- Vytvořte novou osnovu nákladového střediska, která je nezávislá na hlavní knize, nebo přidejte nové nákladové středisko do existující osnovy nákladového strědiska. Každé nákladové středisko musíte vytvořit samostatně.

### Převod hodnot dimenzí v hlavní knize do osnovy nákladových středisek
1. Nastavte dimenzi jako dimenzi nákladového střediska na stránce **Aktualizovat dimenze nákladového  účetnictví**. Přenášejí se pouze hodnoty z této dimenze.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Osnova nákladových středisek** a poté vyberte související odkaz.
3. V záložce **Akce** ve skupině **Funkce** vyberte **Získat nákladová střediska z dimenze**, chcete-li přenést hodnoty dimenzí do osnovy nákladových středisek. Funkce přenese hodnoty dimenze definované v kroku 1.

   > [!NOTE]
   > Můžete nastavit pole **Připojit dimenzi nákladového střediska** tak, aby definovalo jednosměrnou synchronizaci hodnot dimenzí z hlavní knihy do osnovy nákladových středisek. Nelze definovat synchronizaci osnovy nákladových středisek s hodnotami dimenzí z hlavní knihy.

Osnova nákladových středisek nyní obsahuje všechny zadané hodnoty dimenze z hlavní knihy a zahrnuje názvy a mezisoučty.

### Vytvoření nových nákladových středisek na stránce Osnova nákladových středisek
Nákladová střediska můžete nastavit a udržovat buď na kartě **Karta nákladového střediska** nebo na stránce **Osnova nákladových středisek**. V tomto postupu nastavíte nákladová střediska na stránce **Osnova nákladových středisek**.

1. Otevřete stránku **Osnova nákladových středisek** v režimu úprav.
2. V poli **Kód** zadejte kód nákladového střediska. Všechna nákladová střediska musí mít kód.
3. V poli **Název** zadejte název nákladového střediska.
4. Zvolte pole rozevíracího seznamu v poli **Typ řádku** a určete účel nákladového střediska.

   - Pro nákladová střediska typu **Součet** musíte vyplnit pole **Součet**. K nastavení rozsahu nákladových středisek použijte operátor **nebo**, což je svislá čára (**&#124;**).
   - Pro nákladová střediska typu **Do-součet** se toto pole vyplní automaticky, když použijete funkci odsazení.
5. Vyplňte pole **Pořadí řazení** a **Podtyp nákladů**.
6. Vyberte další prázdný řádek a vytvořte nové nákladové středisko a opakujte kroky 2 až 5.
7. Po nastavení všech nákladových středisek vyberte akci **Odsadit nákladová střediska**. Zvolte tlačítko **Ano**.

> [!IMPORTANT]
> Pokud jste zadali definice do polí **Součet** pro nákladová střediska **Do-součet** před spuštěním funkce odsazení, musíte je zadat znovu. Funkce přepíše hodnoty ve všech polích **Do-součet**.

## Nastavení nositelů nákladů
Nositele nákladů jsou projekty, produkty nebo služby společnosti. Osnova nositelů nákladů je podobná informacím o dimenzích pro hlavní knihu. Osnovu nositelů nákladů můžete nastavit následujícími způsoby:

* Přeneste hodnoty dimenzí v hlavní knize do osnovy nositelů nákladů. Po převodu můžete provést potřebné úpravy.
* Vytvořte novou osnovu nositele nákladú, která je nezávislá na hlavní knize, nebo přidejte nového nositele nákladů do existující osnovy nositelů nákladů. Každého nositele nákladů musíte vytvořit samostatně.

### Převod hodnot dimenzí z hlavní knihy do osnovy nositelů nákladů
1. Nastavte dimenzi jako dimenzi nositele nákladů na stránce **Aktualizace CA dimenzí**. Přenášejí se pouze hodnoty z této dimenze.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Osnova nositelů nákladů** a poté vyberte související odkaz.
3. Vyberte akci **Získat nositele nákladů z dimenze** a přeneste hodnoty dimenzí do osnovy nositelů nákladů. Funkce přenese hodnoty dimenze definované v kroku 1.

   > [!NOTE]
   > Můžete nastavit pole **Připojit dimenzi nositele nákladů** tak, aby definovalo jednosměrnou synchronizaci hodnot dimenzí z hlavní knihy do osnovy nositelů nákladů. Nelze definovat synchronizaci osnovy nositelů nákladů s hodnotami dimenze z hlavní knihy.

Osnova nositelů nákladů nyní obsahuje všechny zadané hodnoty dimenze z hlavní knihy a zahrnuje názvy a mezisoučty.

### Vytvoření nových nositelů nákladů na stránce Osnova nositelů nákladů
Nositele nákladů můžete nastavit a udržovat na kartě **Karta nositele nákladů** na stránce **Osnova nositelů nákladů**. V tomto postupu nastavíte nositele nákladů na stránce **Osnova nositelů nákladů**.

1. Otevřete stránku **Osnova nositelů nákladů** v režimu úprav.
2. Do pole **Kód** zadejte kód nositele nákladů. Všechny nositele nákladů musí mít kód.
3. Do pole **Název** zadejte název nositele nákladů.
4. Vyberte rozevírací šipku v poli **Typ řádku** a určete účel nositele nákladů.

   * U nositele nákladů s typem řádku **Součet** vyplňte pole **Součet**. K nastavení rozsahu nositele nákladů použijte operátor **nebo**, což je svislá čára (**&#124;**).
   * U nositelů nákladů s typem řádku **Do-součet** je toto pole vyplněno automaticky, když použijete funkci odsazení.
5. Vyplňte pole **Pořadí řazení**.
6. Vyberte další prázdný řádek a vytvořte nového nositele nákladů a opakujte kroky 2 až 5.
7. Po nastavení všech nositelů nákladů vyberte akci **Odsadit nositele nákladů**. Zvolte tlačítko **Ano**.

> [!IMPORTANT]
> Pokud jste zadali definice do polí **Součet** pro nositele nákladů **Do-součet** před spuštěním funkce odsazení, musíte je zadat znovu. Funkce přepíše hodnoty ve všech polích **Do-součet**.

## Definování nákladových středisek a nositelů nákladů pro účetní osnovu
Můžete automaticky převádět položky výdajů a přijmů z hlavní knihy do nákladového účetnictví buď pro každé účtování hlavní knihy, nebo pomocí dávkové úlohy. Když provedete převod, [!INCLUDE[d365fin](includes/d365fin_md.md)] převede pouze položky, které jsou již propojeny s nákladovým střediskem nebo nositelem nákladů. Chcete-li vytvořit smysluplný převod, musíte zajistit, aby byla správně definována nákladová střediska a nositele nákladů.

### Definování výchozích hodnot dimenzí pro účty hlavní knihy
Pro každý účet hlavní knihy můžete definovat výchozí hodnoty dimenze v tabulce **Výchozí dimenze**. Následující příklad ukazuje, jak definovat při účtování na účet hlavní knihy, aby bylo nákladové středisko vždy ODDĚLENÍ, ale nositelem nákladů nesmí být nikdy PROJEKT.

| **Kód dimenze** | **Účtování hodnoty** |
|------------------------------------------|-----------------------------------------|  
| Oddělení | Nutný kód |
| Projekt | Žádný kód |

### Definování hodnot dimenze pro režijní náklady a přímé náklady
Můžete převést režijní náklady do nákladového střediska a přímé náklady na nositele nákladů. V následující tabulce je uvedena optimální kombinace hodnot nastavení dimenze.

| Převést do | Účtování nákladového střediska | Účtování nositelů nákladů |
|-----------------|-------------------------|-------------------------|  
| Nákladové středisko | Nutný kód | Žádný kód |
| Nositel nákladů | Žádný kód | Nutný kód |

> [!NOTE]
> Chcete-li zajistit, aby předdefinované nákladové středisko a nositel nákladů, které jste nastavili v hlavní knize, byly automaticky přeneseny do nákladového účetnictví, zaškrtněte políčko **Kontrola fin. účtování** na stránce Nastavení nákladového účetnictví.

## Viz také
[Účtování nákladů](finance-manage-cost-accounting.md)  
[Transfer a účtování položek nákladů](finance-transfer-and-post-cost-entries.md)  
[Definování a rozdělení nákladů](finance-define-and-allocate-costs.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
