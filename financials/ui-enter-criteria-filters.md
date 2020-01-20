---
title: Hledání dat a zadávání kritérií filtru | Microsoft Docs
description: 'Popisuje, jak pracovat s filtry, například s Rychlým filtrem, k vylepšení výsledků, které získáte, když hledáte data.'
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'delimit, FlowFilter'
ms.date: 03/29/2017
ms.author: solsen
---
# <a name="searching-filtering-and-sorting-data"></a>Vyhledávání, Filtrování a Řazení dat
Existuje několik věcí, které můžete udělat, aby vám pomohly najít, určit a prozkoumat záznamy v seznamu. Patří sem t, vyhledávání a filtrování.

Pokud chcete vyhledávat data, jako jsou jména zákazníků, adresy nebo skupiny produktů, zadejte kritéria. Ve vyhledávacích kritériích můžete použít všechna čísla a písmena, která normálně používáte v konkrétním poli. Kromě toho můžete použít speciální symboly k dalšímu filtrování výsledků. Existují dva způsoby vyhledávání: pomocí Rychlého filtru nebo sloupcových filtrů.

## <a name="sorting"></a>Řazení
Řazení vám usnadňuje dostat rychlý přehled o vašich datech. Máte-li například mnoho zákazníků, můžete je řadit podle **Čísla zákazníka**, **Účto skupiny zákazníka**, **Kódu měny**, **Kódu zěmě/oblasti** nebo **Čísla registrace DPH**, abyste dostali přehled, který potřebujete.

Chcete-li seřadit seznam, můžete buď zvolit text záhlaví sloupce pro přepínání mezi vzestupným a sestupným pořadí, nebo zvolit malou šipku dolů v záhlaví sloupce a poté zvolit **Vzestupně** nebo **Sestupně**.  

> [!NOTE]  
>   Řazení není podporováno pro obrázky, pole typu BLOB, dynamický filtr a pole, která nepatří do tabulky.  

## <a name="searching-by-using-the-quick-filter"></a>Vyhledávání pomocí Rychlého filtru
Filtry můžete přidat na všechny stránky pomocí Rychlého filtru. Rychlý filtr je povolen výběrem ikony lupy v pravém horním rohu stránky. Tento typ filtrování se používá pro rychlé zadání kritérií.

> [!IMPORTANT]  
>   Rychlý filtr poskytuje snadný přístup k datům filtru zadáním prostého textu, ale také poskytuje mnoho možností vyhledávacích kritérií. V závislosti na tom, zda zadáváte prostý text nebo text včetně symbolů, se rychlý filtr chová odlišně.  

* Pokud do vyhledávacích kritérií zadáte prostý text, budou vyhledávací kritéria interpretována tak, že vyhledávání rozlišuje malá a velká písmena, která obsahují určitý text.  
* Pokud do vyhledávacích kritérií zadáte text obsahující symboly, vyhledávací kritéria se interpretují přesně tak, jak jste je zadali, a při vyhledávání se rozlišují velká a malá písmena.

### <a name="quick-filter-criteria"></a>Kritéria Rychlého filtru
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Kritéria vyhledávání</TH>
    <TH>Inerpretováno jako...</TH>
    <TH>Vrátí...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Všechny záznamy, které obsahují text <b>man</b> rozlišující malá a velká písmena.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Všechny záznamy, které obsahují text <b>se</b> rozlišující malá a velká písmena.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Začíná na <b>Man</b> a rozlišuje malá a velká písmena.</TD>
    <TD>Všechny záznamy, které začínají textem <b>Man</b>.</TD>
  </TR>
  <TR>
    <TD>&#39;man&#39;</TD>
    <TD>Přesný text rozlišující malá a velká písmena.</TD>
    <TD>Všechny záznamy, které přesně odpovídají <b>man</b>.</TD>
  </TR>
  <TR>
    <TD><xref href="man*" data-throw-if-not-resolved="False" data-raw-source="@man*"></xref> </TD>
    <TD>Začíná na a nerozližuje malá a velká písmena.</TD>
    <TD>Všechny záznamy, které začínají textem <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Končí na a nerozlišuje malá a velká písmena.</TD>
    <TD>Všechny záznamy, které končí textem <b>man</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   Zástupný znak nelze použít při filtrování v polích výčtu, například v poli **Stav** u prodejních objednávek. Chcete-li zadat filtr pro tento typ pole, můžete zadat číselnou hodnotu jako parametr filtrování. Například v poli **Stav** na prodejní objednávce, která má hodnoty **Otevřeno**, **Vydáno**, **Čeká na schválení** a **Čeká na zálohu** použijte hodnoty **0**, **1**, **2** a **3** k filtrování těchto možností. 

## <a name="searching-by-using-column-filters"></a>Vyhledávání pomocí filtrů sloupců
Filtr můžete přidat do jednoho nebo více sloupců v seznamu. Filtrování na sloupcích je flexibilnější a vylepšené oproti Rychlému filtru. 

### <a name="to-add-a-filter-on-a-column"></a>Pro přidání fultru do sloupce
1. Před přidáním filtru zvolte ikonu ![Zobrazit jako seznam](media/ui_show_as_list_icon.png "Zobrazit jako seznam šipka vlevo") a přejděte do zobrazení seznamu.
2. V záhlaví sloupce vyberte šipku dolů a pak zvolte **Filtr**.
3. Proveďte jeden z následujících: 
   -  Zvolte *...* Vedle pole a vyberte hodnotu ze seznamu.
   -  Do pole zadejte kritéria filtru. Podrobnosti najdete v další sekci.
4. Zvolte tlačítko **OK**.

## <a name="filter-criteria-and-symbols"></a>Filtrujte kritéria a symboly
Při zadávání kritérií můžete použít všechna čísla a písmena, která můžete v poli normálně použít. Kromě toho můžete použít speciální symboly k dalšímu filtrování výsledků. Následující tabulky ukazují symboly, které lze použít ve filtrech.  
  
> [!IMPORTANT]
>  Mohou se vyskytnout případy, kdy hodnoty polí obsahují tyto symboly a vy je chcete filtrovat. Chcete-li toto provést, musíte do uvozovek ('') zahrnout výraz filtru, který obsahuje symbol. Pokud například chcete filtrovat záznamy, které začínají textem *S&R*, je výraz filtru <strong>'S&R*'</strong>.  
  
### <a name="-interval"></a>(..) Interval  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|1100..2100|Čísla 1100 až 2100|  
|..2500|Až do 2500 včetně|  
|..12 31 00|Data do 12 31 00 včetně|  
|P8.|Informace za účetní období 8 a následující|  
|..23|Od počátečního data do 23-aktuální měsíc-aktuální rok 23:59:59|  
|23..|Od 23-aktuální měsíc-aktuální rok 0:00:00 do konce času|  
|22..23|Od 22-aktuální měsíc-aktuální rok 0:00:00 do 23-aktuální měsíc-aktuální rok 23:59:59|  
  
### <a name="124-eitheror"></a>(&#124;) Buď/nebo  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|1200&#124;1300|Čísla s 1200 nebo 1300|  
  
### <a name="-not-equal-to"></a>(<>) Není rovno  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|<>0|Všechny čísla kromě 0<br /><br /> Možnost SQL Server umožňuje kombinovat tento symbol s výrazem zástupných znaků. Například <>A* znamená nerovnost žádnému textu, který začíná na A.|  
  
### <a name="-greater-than"></a>(>) Větší než  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|>1200|Čísla větší než 1200|  
  
### <a name="-greater-than-or-equal-to"></a>(>=) Větší než nebo rovno  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|>=1200|Čísla větší než nebo rovno 1200|  
  
### <a name="-less-than"></a>(<) Menší než  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|<1200|Čísla menší než 1200|  
  
### <a name="-less-than-or-equal-to"></a>(?=) Menší než nebo rovno  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|<=1200|Čísla menší než nebo rovno 1200|  
  
### <a name="-and"></a>(&) A  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|>200&<1200|Čísla větší než 200 a zároveň menší než 1200|  
  
### <a name="-an-exact-character-match"></a>('') Přesná shoda znaků  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|man|Text, který přesně odpovídá výrazu man a rozlišuje velká a malá písmena.|  
  
### <a name="-case-insensitive"></a>(@) Nerozlišující malá a velká písmena  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|@man*|Text, který začíná man a nerozlišuje velká a malá písmena.|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Neomezený počet neznámých znaků  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|*Co*|Text, který obsahuje “Co“ a rozlišuje malá a velká písmena.|  
|*Co|Text, který končí na “Co“ a rozlišuje malá a velká písmena.|  
|Co*|Text, který začíná na “Co“ a rozlišuje malá a velká písmena.|  
  
### <a name="-one-unknown-character"></a>(?) Jeden neznámý znak  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|Hans?n|Text jako Hansen nebo Hanson|  
  
### <a name="combined-format-expressions"></a>Výrazy v kombinovaném formátu  
  
|Ukázkový výraz|Záznamy zobrazeny|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Obsahuje všechny záznamy s číslem 5999 nebo číslem z intervalu 8100 až 8490.|  
|..1299&#124;1400..|Obsahuje záznamy s číslem menším nebo rovnajícím se 1299 nebo číslem rovnajícím se 1400 nebo větším (všechna čísla kromě 1300 až 1399).|  
|>50&<100|Obsahuje záznamy s čísly, které jsou větší než 50 a menší než 100 (čísla 51 až 99).|  
 
## <a name="see-also"></a>Viz také
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
