---
    title: Transferring and Posting Cost Entries | Microsoft Docs
    description: Before you define cost allocations, you must understand where cost entries come from.
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
# Transfer a účtování položek nákladů
Před definováním rozdělení nákladů je nutné pochopit, jak položky nákladů přicházejí z následujících zdrojů:

- Automatický transfer věcných položek.
- Manuální zaúčtování nákladů čisté nákladové položky, vnitřní poplatky a ruční rozdělení.
- Automatické rozdělení účtů pro skutečné náklady.
- Transfer položek rozpočtu na skutečné.

## Kritéria pro transfer věcných položek do položek nákladů
Je důležité porozumět kritériím pro transfer věcných položek do položek nákladů. Během transferu používá dávková úloha **Přesun věc. položek do nákl. účetnictví** následující kritéria k určení, zda a jak budou přeneseny věcné položky.

Věcné položky se převádějí, pokud:

- Položky mají hodnoty dimenzí odpovídající buď nákladovému středisku nebo nositeli nákladů.
- Položky mají hodnoty dimenzí, které odpovídají nákladovému středisku a nositeli nákladů. U těchto položek má nákladové středisko přednost. To pomáhá vyhnout se situaci, kdy se typ nákladů objeví jak v nositeli níkladů, tak v nákladovém středisku, a proto se ve statistice započítává dvakrát.
- Číslo dokladu v položkách je prázdné, takže se v položkách nákladů zobrazí číslo dokladu 0000.
- Položky jsou převedeny na typ nákladů, který umožňuje kombinované položky a tyto položky jsou převedeny jako kombinovaná položka buď měsíčně nebo denně.

Věcné položky se nepřevádějí, pokud:

- Položky mají hodnoty dimenzí, které neodpovídají nákladovému středisku nebo nákladovému objektu.
- Položky mají nulovou částku.
- Položky mají účet hlavní knihy, který byl odstraněn.
- Položky mají účet hlavní knihy, který není typu **Výsledovka**.
- Položky mají účet hlavní knihy, kterému není přiřazen typ nákladů.
- Položky mají datum zaúčtování před **Počátečním datumem transferu z věcných položek**.
- Položky byly zaúčtovány s datem uzavření. Jedná se obvykle o položky, které vyrovnávají zůstatek výkazu zisku a ztráty na konci roku.

## Transfer věcných položek na položky nákladů
Věcné položky můžete převést na položky nákladů.

Před spuštěním procesu převodu věcných položek na položky nákladů musíte připravit transfer, abyste se vyhnuli ručním opravám účtování.

### Příprava transferu

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení nákladového účetnictví** a poté vyberte související odkaz.
2. Na stránce **Nastavení nákladového účetnictví** ověřte, zda je pole **Počáteční datum transferu z věcných položek** nastaveno na správnou hodnotu.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Osnova druhů nákladů** a poté vyberte související odkaz.
4. Na stránce **Karta druhu nákladů** ověřte, zda je pole **Rozmezí fin. účtu** správně propojeno pro každý typ nákladů, aby bylo možné pořizovat položky z hlavní knihy.
5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
6. U každého příslušného účtu hlavní knihy na stránce **Karta finančního účtu** ověřte, zda je pole **Číslo druhu nákladů** správně spojeno s typem nákladů. Pro více informací navštivte [Nastavení nákladového účetnictví](finance-set-up-cost-accounting.md).
7. Ověřte, zda všechny příslušné věcné položky mají hodnoty dimenzí, které odpovídají nákladovému středisku a nositeli nákladů.

### Transfer věcných položek na položky nákladů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Přesun věc. položek do nákl. účetnictví** a poté vyberte související odkaz.
2. Výběrem tlačítka **Ano** spusťte transfer. Proces převede všechny věcné položky, které ještě nebyly převedeny.

   Během transferu proces vytvoří připojení v položkách v tabulce **Záznam nákladů** a **Žurnál nákladů**. To umožňuje sledovat zdroj položek nákladů.

## Automatický transfer a kombinované položky
V nákladovém účetnictví můžete převádět věcné položky do typu nákladů pomocí kombinovaného účtování. Můžete určit, zda typ nákladů přijímá kombinované položky v poli **Kombinované položky** v definici typu nákladů. Následující tabulka popisuje různé možnosti.

| Kombinovat položky | Popis |
|---------------------|-----------------|  
| Žádný | Každá věcná položka je převedena jednotlivě do odpovídajícího typu nákladů. |
| Den | Věcné položky se stejným datem zaúčtování jsou převedeny jako jedna položka na odpovídající typ nákladů. |
| Měsíc | Všechny věcné položky ve stejném kalendářním měsíci jsou převedeny jako jedna položka na odpovídající typ nákladů. |

> [!IMPORTANT]
> Pokud jste na stránce **Nastavení nákladového účetnictví** vybrali políčko **Automatický transfer z věcných položek** [!INCLUDE[d365fin](includes/d365fin_md.md)] aktualizuje účtování nákladů po každém účtování ve věcných položkách. Kombinované položky nejsou možné.

## Výsledky transferu věcných položek do položek nákladů
Během převodu věcných položek na položky nákladů, [!INCLUDE[d365fin](includes/d365fin_md.md)] vytvoří přepojení v položkách v tabulce **Věcná položka**, **Záznam nákladů** a **Žurnál nákladů**, aby bylo možné sledovat přepojení mezi položkami nákladů a položkami zboží.

### Věcné položky
Pro každou věcnou položku, která je převedena do nákladového účetnictví, vyplní [!INCLUDE[d365fin](includes/d365fin_md.md)] pole **Číslo položky**.

### Položky nákladů
Pro každou položku nákladů, [!INCLUDE[d365fin](includes/d365fin_md.md)] uloží číslo položky odpovídající věcné položky do pole **Číslo věcné položky** v tabulce **Položka nákladů**.

Pro kombinované položky nákladů, [!INCLUDE[d365fin](includes/d365fin_md.md)] uloží číslo záznamu poslední věcné položly, což je položka s nejvyšším číslem.

Pole **Finanční účet** v tabulce **Položka nákladu** obsahuje číslo účtu hlavní knihy, ze kterého přišla položka nákladů.

Pro jednotlivé položky nákladů, [!INCLUDE[d365fin](includes/d365fin_md.md)] převede účtovací text z věcné položky do textového pole **Popis**. U kombinovaných položek je v textovém poli uvedeno, že se tyto položky přenášejí jako kombinované položky. Například pro kombinovanou položku za měsíc říjen 2013 může být text **Kombinované položky, říjen 2013**.

### Žurnál nákladů
V tabulce **Žurnál nákladů**, [!INCLUDE[d365fin](includes/d365fin_md.md)] vytvoří záznam s transferem zdroje z věcných položek. Záznam zaznamenává první a poslední číslo položky z věcných položek, které jsou přenášeny, kromě prvního a posledního čísla položky nákladových položek, které jsou vytvořeny.

## Viz také
[O nákladovém účetnictví](finance-about-cost-accounting.md)  
[Nastavení nákladového účetnictví](finance-set-up-cost-accounting.md)  
[Definování a rozdělení nákladů](finance-define-and-allocate-costs.md)  
[Účtování nákladů](finance-manage-cost-accounting.md)
