---
    title: Design Details - Searching for Dimension Combinations | Microsoft Docs
    description: When you close a page after you edit a set of dimensions, Business Central evaluates whether the edited set of dimensions exists. If the set does not exist, a new set is created and the dimension combination ID is returned.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Vyhledávání kombinací dimenzí
Vyhledávání kombinací dimenzí, [!INCLUDE[prod_short](includes/prod_short.md)] vyhodnotí, zda upravená sada dimenzí existuje. Pokud sada neexistuje, vytvoří se nová sada a vrátí se ID kombinace dimenzí.

## Budování stromu vyhledávání
Tabulka **Uzel stromu sady dimenzí** je použita když [!INCLUDE[prod_short](includes/prod_short.md)] vyhodnotí, zda sada dimenzí již existuje v tabulce 480 **Položka sady dimenzí**. Vyhodnocení se provádí rekurzivně procházením vyhledávacího stromu počínaje nejvyšší úrovní s číslem 0. Nejvyšší úroveň 0 představuje sadu dimenzí bez položek sady dimenzí. Podřízené sady této sady dimenzí představují sady dimenzí pouze s jednou položkou. Podřízené sady těchto sad dimenzí představují sady dimenzí se dvěmi podřízenými a tak dále.

### Příklad 1
Následující diagram představuje vyhledávací strom se šesti sadami dimenzí. V diagramu je zobrazena pouze položka rozlišovací sady dimenzí.

![Příklad struktury stromu dimenzí](media/nav2013_dimension_tree.png "Příklad struktury stromu dimenzí")

Následující tabulka popisuje úplný seznam položek sady dimenzí, které tvoří každou sadu dimenzí.

| Sady dimenzí | Položky sady dimenzí |
|--------------------|---------------------------|  
| Sada 0 | Žádné |
| Sada 1 | AREA 30 |
| Sada 2 | AREA 30, DEPT ADM |
| Sada 3 | AREA 30, DEPT PROD |
| Sada 4 | AREA 30, DEPT ADM, PROJ VW |
| Sada 5 | AREA 40 |
| Sada 6 | AREA 40, PROJ VW |

### Příklad 2
Tento příklad ukazuje, jak  [!INCLUDE[prod_short](includes/prod_short.md)] vyhodnotí, zda existuje sada dimenzí, která se skládá z položek sady AREA 40, DEPT PROD.

Nejprve, [!INCLUDE[prod_short](includes/prod_short.md)] aktualizuje tabulku **Uzel stromu sady dimenzí** aby se ujistil, že vyhledávací strom vypadá jako následující diagram. Sada dimenzí 7 se tak stává podřízenou sadou dimenzí 5.

![Příklad struktury stromu dimenzí v NAV 2013](media/nav2013_dimension_tree_example2.png "Příklad struktury stromu dimenzí v NAV 2013")

### Hledání ID sady dimenzí
Na koncepční úrovni jsou **Nadřazené ID**, **Dimenze** a **Hodnoty dimenze**,  ve stromu hledání kombinovány a používány jako primární klíč, protože [!INCLUDE[prod_short](includes/prod_short.md)] tprochází strom ve stejném pořadí jako položky dimenze. Funkce GET (záznam) se používá k vyhledání ID sady dimenzí. Následující příklad kódu ukazuje, jak najít ID sady dimenzí, pokud existují tři hodnoty dimenze.

```
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```

Nicméně, aby se zachovala schopnost [!INCLUDE[prod_short](includes/prod_short.md)] pro přejmenování dimenze i hodnoty tabulky 349, **Hodnoty dimenze**, je rozšířena o celé pole **ID hodnoty dimenze**. Tato tabulka převede dvojici polí **Dimenze** a **Hodnoty dimenze** na celočíselnou hodnotu. Při přejmenování dimenze a hodnoty dimenze se celá hodnota nezmění.

```
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```

## Viz také
[Funkce GET (Záznam)](/dynamics-nav/GET-Function--Record-)    
[Detaily návrhu: Položky sady dimenzí](design-details-dimension-set-entries.md)   
[Přehled položek sad dimenzí](design-details-dimension-set-entries-overview.md)   
[Detaily návrhu: Struktura tabulky](design-details-table-structure.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]