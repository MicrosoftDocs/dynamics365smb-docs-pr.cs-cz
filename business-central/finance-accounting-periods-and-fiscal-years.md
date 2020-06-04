---
    title: Working with Accounting Periods and Fiscal Years | Microsoft Docs
    description: Learn how to work with accounting periods to define when your company reports financial performance.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: bholtorf

---
# Fiskální období a fiskální roky
Účetní období, která jsou také známá jako vykazovaná období, jsou období, za která společnost nebo organizace vykazuje finanční výkonnost, například generováním výsledovky nebo rozvahy. Účetní období se obvykle vztahují na fiskální rok společnosti, který může obsahovat několik účetních období, například měsíce nebo čtvrtletí.

Pro mnoho společností fiskální rok není v souladu s kalendářním rokem. Například fiskální rok může skončit 30. června místo 31. prosince. U nově vytvořených společností může být fiskální doba ve skutečnosti delší než 12 měsíců.

[!INCLUDE[d365fin](includes/d365fin_md.md)] vyžaduje účetní období pouze v případě, že chcete zavřít výsledovku nebo spustit úlohy komprese dat.

Účetní období můžete použít v sestavách. Pokud například kontrolujete zaúčtované položky na stránce **Saldo/rozpočet** kde lze zadat interval vykazování. Je to jedna z možností, které můžete zadat pro vykazování podle účetního období. Můžete také vytvořit účetní plán, který porovnává výsledky pro různá účetní období.

## Vytvoření nového fiskálního roku
Účetní období můžete vytvořit hromadně pomocí dávkové úlohy **Vytvořit fiskální rok** nebo ručně.

### Vytváření účetního období hromadně
Pomocí dávkové úlohy **Vytvořit fiskální rok** rozdělte fiskální rok na období stejné délky.

1. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Účetní období** a poté zvolte související odkaz.
2. Vyberte akci **Vytvořit rok**.  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. Do pole **Počáteční datum** zadejte datum, kdy začíná fiskální rok.
4. Do pole **Počet  období** zadejte počet účetních období, do kterých se má fiskální rok rozdělit. Za rok může být až 365 období.
5. Do pole **Délka období** zadejte trvání pro každou periodu. Například 1M za jeden měsíc, 1Q pro jedno čtvrtletí a 1Y po dobu jednoho roku.
6. Zvolte **OK**.

### Vytvoření účetního období ručně
Pokud účetní období ve fiskálním roce mají různé doby trvání, například kalendář 4-4-5 používaný v maloobchodě, můžete jej nastavit ručně.

1. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Účetní období** a poté zvolte související odkaz.
2. Do pole **Počáteční datum** zadejte datum, kdy začíná fiskální rok. V poli **Název** se zobrazí název měsíce.
3. Zaškrtnutím políčka **Nový fiskální rok** označte, že se jedná o první období v roce. [!INCLUDE[d365fin](includes/d365fin_md.md)] použije toto období k určení, která období se mají na konci roku uzavřít.
4. Opakujte kroky 2 a 3 pro každé zbývající období.

## Ukončení fiskálního roku
Uzavření fiskálního roku je jedním z úkolů pro uzavření účetní knihy. Po uzavření fiskálního roku jsou pro všechna období v roce zaškrtnuta políčka **Uzavřeno** a **Datum uzavřeno**. Nelze znovu otevřít rok ani zrušit zaškrtnutí políček.

> [!NOTE]
> Musíte mít vždy alespoň jeden otevřený fiskální rok. Při uzavírání roku se ujistěte, že byl vytvořen nový rok. Všimněte si také, že po uzavření jednoho roku nelze změnit počáteční datum následujícího roku.

1. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Účetní období** a poté zvolte související odkaz.
2. Vyberte akci **Uzavřít rok**.

## Zaúčtování položek do uzavřeného fiskálního roku
Přestože je fiskální rok uzavřen, můžete do něj stále zaúčtovat věcné položky. Když tak učiníte, položky se označí jako zaúčtované do uzavřeného fiskálního roku a je zaškrtnuto políčko **Položka předchozího roku**. Ve výchozím nastavení není zaškrtávací políčko na stránce zobrazeno, ale můžete jej přidat. Dalším krokem je uzavření účtů výsledovky a převod ročních výsledků na účet v rozvaze. Tyto kroky opakujte při každém zaúčtování položek do uzavřeného fiskálního roku.

## Viz také
[Uzavírání knih](year-close-books.md)  
[Uzavírání roků a období](year-close-years-periods.md)  
[Práce s účetními schématy](bi-how-work-account-schedule.md)






