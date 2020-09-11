---
    title: How to Plan Order by Order | Microsoft Docs
    description: This planning task can be performed on the **Order Planning** page, which displays all new demand along with availability information and suggestions for supply. It provides the visibility and tools needed to effectively plan demand from sales lines and component lines and then create different types of supply orders directly.
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
# Plán nové poptávky podle objednávky
Tuto plánovací úlohu lze provést na stránce **Plánování objednávek**, která zobrazuje veškerou novou poptávku spolu s informacemi o dostupnosti a návrhy na dodávku. Poskytuje přehled a nástroje potřebné k efektivnímu plánování poptávky z prodejních řádků a řádků komponent a následnému přímému vytvoření různých typů objednávek dodávek.

Můžete otevřít stránku **Plánování objednávek** dvěma způsoby v závislosti na vašem zaměření: Z objednávky, kterou chcete naplánovat specificky, nebo v dávkovém režimu, protože chcete naplánovat pro všechny a jakékoliv nové poptávky.


## Plánování nové poptávky výrobní zakázky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz. (Tyto kroky můžete provést pro plánovanou, pevně plánovanou objednávku, nebo vydané výrobní zakázky.)
2. Otevřete výrobní zakázku, pro kterou chcete naplánovat, a poté vyberte akci **Plánování**.
3. Na stránce **Plánování objednávek**, vyberte akci **Vypočítat plán**.

Stránka zobrazuje plánovací řádky podle filtru zobrazení **Výrobní poptávka**, což znamená nesplněné řádky komponent všech existujících výrobních zakázek. Poptávka pouze po jedné výrobní zakázce není zobrazena, protože je nutné naplánovat jednu výrobní zakázku s přehledem poptávky po potenciálně dřívějších řádcích komponent. Řádky plánování pro výrobní zakázku jsou v kontextu rozbalené.

## Plánování nové poptávky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Plánování objednávek**, a poté vyberte související odkaz.
2. Na stránce **Plánování objednávek**, vyberte akci **Vypočítat plán**.
3. Zvolte tlačítko **Rozbalit (+)** před datem v poli **Datum poptávky** chcete-li zobrazit základní řádky plánování, které představují řádky poptávky s nedostatečnou dostupností.
4. Pro každý rozšířený plánovací řádek, tj. řádek poptávky, můžete vidět hodnoty v informačních polích v dolní části stránky.

   | Možnost | Popis |
   |----------------------------------|---------------------------------------|  
   | **Množství na jiných lokacích** | Zobrazuje, zda položka existuje na jiné lokaci. Poté ji můžete vyhledat a vybrat ji. |
   | **Náhrada existuje** | Zobrazuje, zda je pro položku vytvořena náhradní zboží. Poté ji můžete vyhledat a vybrat ji. Všimněte si, že tato funkce se vztahuje pouze na součásti, to znamená z řádků poptávky typu **Produkce**. |
   | **Dostupné množství** | Zobrazuje celkovou dostupnost položky, tj. Předpokládané dostupné množství. |
   | **Nejbližší dostupné datum** | Zobrazuje datum příjezdu příchozí nabídky, která může pokrýt potřebné množství k datu pozdějšímu, než je datum poptávky. |

5. Na poli **Systém doplnění**, vyberte, který typ objednávky dodávky chcete vytvořit.

   Výchozí hodnota je hodnota karty zboží nebo karty skladové položky, ale můžete ji změnit na jednu ze tří možností:

   | Možnost | Popis |
   |----------------------------------|---------------------------------------|  
   | **Nákup** | Vytvoření nákupní objednávky |
   | **Převést** | Vytvoření příkazu k převodu. |
   | **Výrobní zakázka** | Vytvoří výrobní zakázku. |

   V poli **Dodávka od** musíte vybrat hodnotu podle vybraného systému doplnění.

   > [!NOTE]
   > Pokud pole není vyplněno, systém zobrazí chybovou zprávu při použití funkce **Vytvořit objednávky dodávek**, pro daný plánovací řádek nebude vytvořena žádná objednávka. To však neplatí, pokud je doplňovací systém **Výrobní zakázka**.

6. Z pole **Dodávka od**, můžete vyhledat v příslušném seznamu a vybrat, odkud má dodávka pocházet:

   - Pokud je doplňovací systém **Nákup**, vyhledávací tlačítko v tomto poli vyhledá stránku **Katalog zboží dodavatele**.
   - Pokud je systém doplnění **Převod**, vyhledávací tlačítko v tomto poli vyhledá stránku **Přehled lokací**.
   V případě, že položka existuje na jiném místě, pole **Množství na dalších lokacích** zobrazuje v dolní části hodnotu a poté můžete vyhledat a vybrat místo, ze kterého by mělo být zboží dodáno, když provedete příkaz k převodu.

   Pokud pro poptávanou položku existuje náhrada, pole **Existuje náhrada** je nastaveno na **Ano**, a můžete jej vyhledat na stránce **Náhrada zboží zákazníka** a vybrat náhradu.

7. Zvolte zaškrtávací políčko **Reservovat** pokud chcete provést rezervaci mezi objednávkou dodávky, kterou vytváříte, a řádkem poptávky, pro který je vytvořena. Ve výchozím nastavení je prázdný.

   > [!NOTE]
   > Toto políčko můžete zaškrtnout pouze v případě, že je na kartě zboží **Volitelné** nebo **Vždy** na poli **Rezervace**.

8. Na poli **Množství na objednávce**, můžete zadat množství, které půjde na objednávku, kterou vytváříte.
Výchozí hodnota je stejné množství jako v poli **Potřebné množství**. Ale můžete se rozhodnout objednat více nebo méně než toto množství na základě vašich znalostí o situaci poptávky. Pokud například na stránce **Plánování objednávek** uvidíte, že několik nesouvisejících poptávkových řádků je pro stejnou zakoupenou položku a jsou splatné kolem stejného data, můžete je konsolidovat zadáním celkového potřebného množství v poli **Množství na objednávce** na jednom řádku, a poté vymazat ostatní zastaralé řádky pro tuto položku.

9. V polích **Datum vyřízení** a **Datum objednávky**, můžete zadat data, která by se měla vztahovat na vytvořené objednávky dodávek.

   Tato dvě pole jsou vzájemně propojena podle pole **Výchozí bezp.průběžná doba**, které najdete na stránce **Nastavení výroby**. Podle výchozího nastavení je datum splatnosti stejné jako datum poptávky, můžete ho ale změnit podle svých představ.

> [!NOTE]
> Pokud zadáte datum později než datum poptávky, obdržíte varovnou zprávu..

## Vytvoření objednávek dodávek
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz. Tyto kroky můžete provést pro plánovanou, pevně plánovanou objednávku, nebo vydanou výrobní zakázku.
2. Otevřete výrobní zakázku, pro kterou chcete naplánovat, a poté vyberte akci **Plánování**.
3. Umístěte kurzor na příslušný řádek plánování a poté zvolte akci **Vytvořit objednávky**.
4. Na stránce **Vytvoření objednávky dodávek**, na záložce s náhledem **Plánování objednávek**, v poli **Vytvořit objednávky pro**, vyberte jednu z následujících možností.

   | Možnost | Popis |
   |----------------------------------|---------------------------------------|  
   | **Aktivní řádek** | Provede objednávku dodávek pouze pro řádek, na kterém je umístěn kurzor. |
   | **Aktivní objednávka** | Provede objednávku dodávek pro všechny řádky v objednávce, na kterém je kurzor umístěn. |
   | **Všechny řádky** | Vytvoří objednávky dodávek pro všechny řádky stránky **Plánování objednávek**. |

5. Na záložce s náhledem **Možnosti**, definujte, jaký druh objednávek dodávky nebo požadavků řádků sešitu má být provedeno.

   > [!NOTE]
   > Nastavení, které jste naposledy provedli na stránce **Vytvořit objednávky dodávek** budou uložena pod vaším ID uživatele, aby byla při příštím použití stránky stejná.

6. Zvolte tlačítko **OK** chcete-li vytvořit navrhované objednávky dodávek nebo požadavky řádku sešitu.

Nyní jste naplánovali nesplněnou poptávku provedením příslušných objednávek dodávek. Podrobnosti o konkrétních pracovních postupech při používání stránky **Plánování objednávek** by záviselo na interních zásadách společnosti.

Když jste dokončili své plánovací práce na stránce **Plánování objednávek**, například definovali alternativní způsob dodávky množství, můžete pokračovat v tvorbě objednávek dodávky pro jednu nebo více řádků plánování.

> [!NOTE]
> Objednávky dodávek, které vytvoříte, mohou představovat novou závislou poptávku, například pro základní výrobní zakázky, a proto byste měli znovu vybrat **Vypočítat plán**, abyste toto našli a vyřešili před přesunutím se níže v seznamu.

## Viz také
[Plánování](production-planning.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)  
[Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
