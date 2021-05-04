---
    title: Design Details - Table Structure | Microsoft Docs
    description: To understand how the dimension entry storing and posting is redesigned, it is important to understand the table structure.
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
# Detaily návrhu:  Struktura tabulky
Chcete-li pochopit, jak jsou položky dimenzí uloženy a zaúčtovány, je důležité porozumět struktuře tabulky.

## Tabulka 480, Položka sady dimenzí
Tuto tabulku nelze změnit. Po zapsání dat do tabulky není možné data odstranit ani upravit.

| Číslo pole. | Název pole | Datový typ | Komentář |
|---------------|----------------|---------------|-------------|  
| 1 | **ID** | Integer | >0,0 je rezervováno pro prázdnou sadu dimenzí. Odkazuje na pole 3 v tabulce 481. |
| 2 | **Kód Dimenze** | Code 20 | Vztah tabulky k tabulce 348. |
| 3 | **Kód hodnoty dimenze** | Code 20 | Vztah tabulky k tabulce 349. |
| 4 | **ID Hodnoty dimenze** | Integer | Odkazuje na pole 12 v tabulce 349. Jedná se o sekundární klíč, který se používá při procházení tabulky 481. |
| 5 | **Název Dimenze** | Text 30 | CalcField. Lookup do tabulky 348. |
| 6 | **Název Hodnoty dimenze** | Text 30 | CalcField. Lookup do tabulky 349. |

## Tabulka, Uzel stromu sady dimenzí
Tuto tabulku nelze změnit. Používá se k vyhledání sady dimenzí. Pokud sada dimenzí není nalezena, vytvoří se nová sada.

| Číslo pole. | Název pole | Datový typ | Komentář |
|---------------|----------------|---------------|-------------|  
| 1 | **ID sady nadřazených dimenzí** | Integer | 0 pro uzel nejvyšší úrovně. |
| 2 | **ID Hodnoty dimenze** | Integer | Vztah tabulky k poli 12 v tabulce 349. |
| 3 | **ID sady dimenzí** | Integer | AutoIncrement. Používá se v poli 1 v tabulce 480. |
| 4 | **V použití** | Boolean | False, pokud se nepoužívá. |

## Tabulka 482 Zásobník přeřazení sady dimenzí
Tato tabulka se používá, když měníte kód hodnoty dimenze, například na položce zboží pomocí využití **Deníků přeřazení zboží**.

| Číslo pole. | Název pole | Datový typ | Komentář |
|---------------|----------------|---------------|-------------|  
| 1 | **Kód Dimenze** | Code 20 | Vztah tabulky k tabulce 348. |
| 2 | **Kód hodnoty dimenze** | Code 20 | Vztah tabulky k tabulce 349. |
| 3 | **ID Hodnoty dimenze** | Integer | Odkazuje na pole 12 v tabulce 349. |
| 4 | **Nový kód hodnoty dimenze** | Code 20 | Vztah tabulky k tabulce 349. |
| 5 | **Nové ID hodnoty dimenze** | Integer | Odkazuje na pole 12 v tabulce 349. |
| 6 | **Název Dimenze** | Text 30 | CalcField. Lookup do tabulky 348. |
| 7 | **Název Hodnoty dimenze** | Text 30 | CalcField. Lookup do tabulky 349. |
| 8 | **Nový název hodnoty dimenze** | Text 30 | CalcField. Lookup do tabulky 349. |

## Tabulky transakcí a rozpočtu
Kromě dalších polí dimenzí v tabulce je toto pole důležité:

| Číslo pole. | Název pole | Datový typ | Komentář |
|---------------|----------------|---------------|-------------|  
| 480 | **ID sady dimenzí** | Integer | Odkazuje na pole 1 v tabulce 480. |

### Tabulka 83, Řádky deníku zboží
Kromě dalších polí dimenzí v tabulce jsou tato pole důležitá.

| Číslo pole. | Název pole | Datový typ | Komentář |
|---------------|----------------|---------------|-------------|  
| 480 | **ID sady dimenzí** | Integer | Odkazuje na pole 1 v tabulce 480. |
| 481 | **Nové ID Sady dimenze** | Integer | Odkazuje na pole 1 v tabulce 480. |

### Table 349, Dimension Value
Kromě dalších polí dimenzí v tabulce jsou tato pole důležitá.

| Číslo pole. | Název pole | Datový typ | Komentář |
|---------------|----------------|---------------|-------------|  
| 12 | **ID Hodnoty dimenze** | Integer | AutoIncrement. Používá se pro odkaz v tabulce 480 a 481. |

### Tabulky, které obsahují pole ID sady dimenzí
**ID Sady Dimenzí** pole (480) existuje v následujících tabulkách. U tabulek, které ukládají zaúčtovaná data, pole poskytuje pouze neupravitelné zobrazení dimenzí, které je označeno jako přechod k podrobnostem. U tabulek, které ukládají pracovní doklady, je pole upravitelné. Tabulky vyrovnávací paměti, které se používají interně, nepotřebují upravitelné nebo needitovatelné možnosti.

Pole 480 nelze upravovat v následujících tabulkách.

| Číslo tabulky | Název tabulky |
|---------------|----------------|  
| 17 | **Věcná položka** |
| 21 | **Položka Zákazníka** |
| 25 | **Položky dodavatele** |
| 32 | **Položky zboží** |
| 110 | **Hlavička prodejní dodávky** |
| 111 | **Řádky prodejní dodávky** |
| 112 | **Hlavička prodejní faktury** |
| 113 | **Řádek prodejní faktury** |
| 114 | **Hlavička prodejního dobropisu** |
| 115 | **Řádek prodejního dobropisu** |
| 120 | **Hlavička nákupní příjemky** |
| 121 | **Řádek nákupní příjemky** |
| 122 | **Hlavička nákupní faktury** |
| 123 | **Řádek nákupní faktury** |
| 124 | **Hlavička nákupního dobropisu** |
| 125 | **Řádek nákupního dobropisu** |
| 169 | **Položky projektu** |
| 203 | **Položka zdroje** |
| 271 | **Položky bankovního účtu** |
| 281 | **Položka fyzické inventury** |
| 297 | **Hlavička vydané upomínky** |
| 304 | **Hlavička vydaného penále** |
| 5107 | **Archivovaná prodejní hlavička** |
| 5108 | **Archivovaný prodejní řádek** |
| 5109 | **Archivovaná nákupní hlavička** |
| 5110 | **Archivovaný nákupní řádek** |
| 5601 | **Položky DM** |
| 5625 | **Položky údržby** |
| 5629 | **Položka pojistného krytí** |
| 5744 | **Hlavička dodávky transferu** |
| 5745 | **Řádek dodávky transferu** |
| 5746 | **Hlavička příjemky transferu** |
| 5747 | **Řádek příjemky transferu** |
| 5802 | **Položky ocenění** |
| 5832 | **Položky kapacity** |
| 5907 | **Položky servisu** |
| 5908 | **Hlavička servisu** |
| 5933 | **Zásobník účtování serv.zakázky** |
| 5970 | **Archivovaná servisní smlouva** |
| 5990 | **Hlavička dodávky servisu** |
| 5991 | **Řádek dodávky servisu** |
| 5992 | **Hlavička faktury servisu** |
| 5993 | **Řádek fakturace servisu** |
| 5994 | **Hlavička dobropisu servisu** |
| 5995 | **Řádek dobropisu servisu** |
| 6650 | **Hlavička dodávky vratky** |
| 6651 | **Řádky dodávky vratky** |
| 6660 | **Hlavička příjmu vratky** |
| 6661 | **Řádky příjemky vratky** |

Pole 480 je editovatelné v následujících tabulkách.

| Číslo tabulky | Název tabulky |
|---------------|----------------|  
| 36 | **Prodejní hlavička** |
| 37 | **Prodejní řádky** |
| 38 | **Nákupní hlavička** |
| 39 | **Nákupní řádky** |
| 81 | **Řádek finančního deníku** |
| 83 | **Řádky deníku zboží** |
| 89 | **Řádek deníku kusovníku** |
| 96 | **Položky finančního rozpočtu** |
| 207 | **Řádek deníku zdrojů** |
| 210 | **Řádek deníku projektů** |
| 221 | **Deník rozdělení** |
| 246 | **Řádky požadavků** |
| 295 | **Hlavička upomínky** |
| 302 | **Hlavička penále** |
| 5405 | **Výrobní zakázka** |
| 5406 | **Řádek výrobní zakázky** |
| 5407 | **Komponenta výrobní zakázky** |
| 5615 | **Rozdělení DM** |
| 5621 | **Řádek deníku DM** |
| 5635 | **Řádek deníku pojištění** |
| 5740 | **Hlavička transferu** |
| 5741 | **Řádky transferu** |
| 5900 | **Hlavička servisu** |
| 5901 | **Řádky předmětu servisu** |
| 5902 | **Řádky servisu** |
| 5965 | **Servisní smlouva** |
| 5997 | **Řádek standardního servisu** |
| 7134 | **Položky rozpočtu zboží** |
| 99000829 | **Plánované komponenty** |

Pole 480 existuje v následujících tabulkách vyrovnávací paměti.

| Číslo tabulky | Název tabulky |
|---------------|----------------|  
| 49 | **Zásobník pro fakturaci** |
| 212 | **Zásobník pro účtování projektu** |
| 372 | **Zásobník plateb** |
| 382 | **Zásobník položek zákazníka/dodavatele** |
| 461 | **Prepayment Inv. Line Buffer** |
| 5637 | **Zásobník účtování DM** |
| 7136 | **Zásobník rozpočtu zboží** |

## Viz také
[Detaily návrhu: Položky sady dimenzí](design-details-dimension-set-entries.md)   
[Přehled položek sad dimenzí](design-details-dimension-set-entries-overview.md)   
[Detaily návrhu: Vyhledávání kombinace dimenzí](design-details-searching-for-dimension-combinations.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]