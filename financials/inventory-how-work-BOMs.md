---
title: Práce s kusovníky pro správu komponent | Microsoft Docs
description: 'Vytvoříte kusovník montáže nebo výrobní kusovník a určete komponenty nebo zdroje potřebné k sestavení zboží, kterou kusovník představuje.'
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/04/2017
ms.author: sgroespe
---
# <a name="work-with-bills-of-material"></a>Práce s kusovníky
K rozdělování nadřazených položek, které musí být smontovány nebo vyrobeny zdroji nebo strojními centry z komponent, použijete kusovníky (BOM). Montážní kusovník lze také použít k prodeji nadřazeného zboží jako soupravy sestávající z jejích součástí.

## <a name="assembly-boms-or-production-boms"></a>Montážní nebo výrobní kusovníky
Montážní zakázku použijte pro výrobu koncových položek z komponent v jednoduchém procesu, který může být proveden jedním nebo více základními zdroji, které nejsou strojními nebo pracovními centry nebo bez jakýchkoli zdrojů. Proces montáže by například mohl vybrat dvě láhve vína a jeden kávový pytlík a pak je zabalit jako dárek.  

Kusovníky montáže jsou kmenová data, která definují, které komponenty zboží přecházejí do koncového zboží montáže a jaké zdroje se používají k sestavení zboží montáže. Když zadáte zboží montáže a množství do záhlaví nové montážní objednávky, pak se řádky objednávky automaticky vyplní podle montážního kusovníku jedním řádkem montážní zakázky na komponentu nebo zdroj. Pro více informací navštivte [Správa montáže](assembly-assemble-items.md).

V tomto tématu jsou popsány kusovníky montáže.

Výrobní zakázky používáte pro výrobu koncového zboží z komponent ve složitém procesu, který vyžaduje směrování výroby a pracoviště nebo strojní centra, která představují výrobní kapacity. Jak příklad výrobního procesu může být řezání ocelových plechů v jedné operaci, jejich svařování v další operaci a lakování konečného zboží v poslední operaci. Pro více informací navštivte [Výroba](production-manage-manufacturing.md).  

Výrobní kusovníky jsou kmenová data, která definují výrobní zboží a komponenty, které do něj vstupují. Pro zboží montáže musí být výrobní kusovník před použitím ve výrobní zakázce certifikován a přiřazen k výrobnímu zboží. Když zadáte výrobní zboží na řádku výrobní zakázky, buď ručně, nebo obnovením zakázky, stane se obsah kusovníku výroby součástmi výrobní zakázky. Pro více informací navštivte [Vytvoření výrobních kusovníků](production-how-to-create-production-boms.md).  

Koncept zdrojů ve výrobě je mnohem pokročilejší než ve správě montáže. Pracovní centra a strojní centra fungují jako prostředky a výrobní kroky jsou reprezentovány operacemi, které jsou přiřazeny k prostředkům ve výrobních postupech. Pro více informací navštivte [Vytvoření TNG postupů](production-how-to-create-routings.md).

Montážní zakázky i výrobní zakázky mohou být přímo spojeny s prodejními objednávkami. Můžete však použít pouze montážní zakázky k přizpůsobení konečného zboží přímo pro požadavek zákazníka s prodejní objednávkou.

## <a name="to-create-an-assembly-bom"></a>Vytvoření kusovníku montáže
Chcete-li definovat nadřazené zboží, které se skládá z jiných položek, a potenciálně ze zdrojů potřebných k sestavení nadřazené jednotky, musíte vytvořit kusovník montáže.  

Kusovníky montáže obvykle obsahují položky, ale mohou také obsahovat jeden nebo více zdrojů, které jsou potřebné pro sestavení zboží montáže dohromady.

Kusovníky montáže mohou mít více úrovní, což znamená, že komponentou v kusovníku montáže může být samotné zboží montáže. V takovém případě pole **Kusovník montáže** na řádku kusovníku montáže obsahuje **Ano**.

Zvláštní požadavky se vztahují na zboží na kusovnících montáže s ohledem na dostupnost. Pro více informací navštivte "Zjištění dostupnosti zboží pomocí jejího použití v kusovnících montáže", co je sekce v [Zobrazení dostupnosti zboží](inventory-how-availability-overview.md).

Vytvoření kusovníku montáže obsahuje dvě části:
- Založení nového zboží
- Definování struktury kusovníku zboží montáže.

1. Nastavení nového zboží Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).

    Pokračujte v zadávání součástí nebo zdrojů do kusovníku montáže.  
2. V okně **Karty zboží** pro zboží montáže vyberte akci **Montáž** a poté vyberte akci **Kusovník montáže**.
3. V okně **Kusovník montáže** vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Zobrazení součástí zboží montáže odsazené podle struktury kusovníku
V okně **Kusovníku montáže** můžete otevřít samostatné okno, které zobrazuje komponenty a všechny prostředky odsazené podle jejich pozice kusovníku pod zbožím montáže.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Položky** a pak vyberte související odkaz.
2. Otevřete kartu pro zboží montáže. (Pole **Kusovník montáže** v okně **Položky** obsahuje **Ano**.)
3. V okně **Karty zboží**  vyberte akci **Montáž** a poté vyberte akci **Kusovník montáže**.
4. V okně **Kusovníku montáže** zvolte akci **Ukázat kusovník**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Nahrazení zboží montáže za komponenty na řádcích dokladu
Z jakéhokoli dokladu o prodeji a nákupu, který obsahuje zboží montáže, můžete speciální funkci nahradit řádek zboží montáže novými řádky pro její součásti. Tato funkce je užitečná například v případě, že chcete komponenty prodat jako soupravu představující zboží montáže.

**Pozor**: Pokud jste použili funkci **Rozbalit kusovník**, nemůžete ji snadno vrátit zpět. Musíte odstranit řádky prodejní objednávky představující komponenty a poté znovu zadat řádek prodejní objednávky pro zboží montáže.

Následující postup je založen na prodejní faktuře. Stejné kroky platí i pro ostatní prodejní doklady a všechny nákupní doklady.

1. V pravém horním rohu vyberte ikonu **Hledat stránku nebo sestavu**, zadejte **Prodejní faktura**, a pak vyberte související odkaz.
2. Otevřete prodejní fakturu, která obsahuje řádek pro zboží montáže.
3. Vyberte řádek pro zboží montáže a poté řádkovou akci **Rozbalit kusovník**.

Všechna pole na řádku prodejní faktury pro zboží montáže jsou vymazána, kromě polí **Zboží** a **Popis**. Pro komponenty a možné zdroje, které tvoří součást zboží montáže, se vkládají úplné řádky prodejní faktury.

**Poznámka**: Funkce Rozbalení kusovníku je k dispozici také v okně **Kusovník montáže**.

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Výpočet standardních nákladů na zboží montáže
Jednotkové náklady na zboží montáže vypočítáte sloučením jednotkových nákladů na každou součást a zdroj v kusovníku montáže zboží.

V okně **Sešit pevné ceny** můžete také spočítat a aktualizovat standardní náklady na jedno nebo více zboží. Pro více informací navštivte [Aktualizace pevná pořizovací ceny](finance-how-to-update-standard-costs.md).  

Jednotkové náklady na kusovník montáže se vždy rovnají součtu jednotkových nákladů na jeho součásti, včetně ostatních kusovníků montáže a jakýchkoli zdrojů.

1. V pravém horním rohu zvolte ikonu **Hledat stránku nebo sestavu**, zadejte **Zboží** a zvolte související odkaz.
2. Otevřete kartu pro zboží montáže. (Pole **Kusovník montáže** v okně **Položky** obsahuje **Ano**.)
3. V okně **Karty zboží**  vyberte akci **Montáž** a poté vyberte akci **Kusovník montáže**.
4. V okně **Kusovníku montáže** zvolte akci **Výpočet  pevné poř.ceny**.
5. Vyberte jednu z následujících možností a poté stiskněte tlačítko **OK**.

|Možnost |Popis |
|-------|------------|
|**Nejvyšší úroveň**|Vypočítá standardní náklady zboží montáže jako celkové náklady na všechny zakoupené nebo smontované zboží na tomto kusovníku montáže bez ohledu na jakékoli základní kusovníky montáže.|
|**Všechny úrovně**|Vypočítá standardní náklady montáže jako součet: 1) Vypočítané náklady na všechny základní kusovníky montáže na kusovníku montáže. 2) Náklady na všechny základní kusovníky montáže na kusovníku montáže.|



Náklady na zboží, které tvoří kusovník montáže, se zkopírují z karet komponentů. Cena každého zboží se vynásobí množstvím a celkové náklady se zobrazí v poli **Pořizovací cena** na kartě zboží.

## <a name="see-also"></a>Viz také
[Zaevidujte nové zboží](inventory-how-register-new-items.md)  
[Zobrazit dostupnost zboží](inventory-how-availability-overview.md)     
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
