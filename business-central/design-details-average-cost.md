---
    title: Design Details - Average Cost | Microsoft Docs
    description: The average cost of an item is calculated with a periodic weighted average, based on the average cost period that is set up in Business Central.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2021
    ms.author: edupont

---
# Detaily návrhu: Průměrné náklady
Průměrné náklady na zboží se počítají s periodickým váženým průměrem založeným na období průměrných nákladů, které je nastaveno v [!INCLUDE[prod_short](includes/prod_short.md)].

Datum ocenění se nastavuje automaticky.

## Nastavení výpočtu průměrných nákladů
Následující tabulka popisuje dvě pole na stránce **Nastavení zásob**, která je nutné vyplnit, aby bylo možné vypočítat průměrné náklady.

| Pole | Popis |
|---------------------------------|---------------------------------------|  
| **Období průměrných nákladů** | Určuje, ve kterém období jsou vypočteny průměrné náklady. Existují následující možnosti:<br /><br /> -   **Den**<br />-   **Týden**<br />-   **Měsíc**<br />-   **Účetní období**<br /><br /> Všechny poklesy zásob, které jsou zaúčtovány v období průměrných nákladů, obdrží průměrné náklady vypočtené pro toto období. |
| **Typ výpočtu prům.poř. ceny** | Určuje způsob výpočtu průměrných nákladů. Existují následující možnosti:<br /><br /> -   **Zboží**<br />-   **Zboží, Varianta a Lokace**<br />     S touto možností se průměrné náklady počítají pro každé zboží, pro každou lokaci a pro každou variantu zboží. To znamená, že průměrné náklady na tuto položku závisí na tom, kde je uložena a jakou variantu zboží jste vybrali, například barvu. |

> [!NOTE]  
> Ve fiskálním roce můžete použít pouze jedno období průměrných nákladů a jeden typ výpočtu průměrných nákladů.
>
> Stránka **Účetní období** zobrazuje, které období průměrných nákladů a jaký typ výpočtu průměrných nákladů je v tomto období pro každé účetní období.

## Výpočet průměrných nákladů
Když zaúčtujete transakci pro zboží, které používá metodu průměrného výpočtu nákladů, vytvoří se položka v tabulce **Místo  zadání úpravy  průměrné ceny**. Tato položka obsahuje číslo transakce zboží, kód varianty a kód lokace. Položka také obsahuje pole **Datum ocenění**, které určuje poslední datum období průměrných nákladů, ve kterém byla transakce zaúčtována.

> [!NOTE]  
> Toto pole by nemělo být zaměňováno s polem **Datum ocenění** v tabulce **Položka ocenění**, které zobrazuje datum, kdy hodnota nabývá účinku, a slouží k určení období průměrných nákladů, do kterého hodnota patří.

Průměrné náklady transakce se vypočítají, když se upraví cena zboží. Pro více informací navštivte [Detaily návrhu: Úprava nákladů](design-details-cost-adjustment.md). Úprava nákladů používá položky v tabulce **Místo  zadání úpravy  průměrné ceny** pro určení zboží (nebo zboží, lokací a variant) pro výpočet průměrných nákladů. Pro každou položku s náklady, které nebyly upraveny, používá úprava nákladů k určení průměrných nákladů následující:

- Určuje náklady na zboží na začátku období průměrných nákladů.
- Přidá součet vstupních nákladů, které byly zaúčtovány během období průměrných nákladů. Patří mezi ně nákupy, prodejní vratky, pozitivní úpravy a výrobní a montážní výstupy.
- Odečte součet nákladů všech výstupních transakcí, které byly pevně použity na příjmy v období průměrných nákladů. Obvykle zahrnují nákupní vratky a záporné výstupy.
- Vydělí celkovým množstvím zásob na konci období průměrných nákladů, s výjimkou snížení zásob, která jsou oceňována.

Vypočtená průměrná cena se poté použije na snížení zásob pro zboží (nebo zboží, lokaci a variantu) s daty zaúčtování v období průměrných nákladů. Pokud existují nějaká zvýšení zásob, která byla pevně aplikována na poklesy zásob v období průměrných nákladů, pak je vypočítaná průměrná cena přeposlána ze zvýšení do snížení.

### Příklad: Období průměrných nákladů = Den
Následující příklad ukazuje účinek výpočtu průměrných nákladů na základě průměrných nákladů jednoho dne. Pole **Typ výpočtu prům.poř. ceny** na stránce **Nastavení zásob** je nastaveno na  **Zboží**.

V následující tabulce jsou uvedeny položky zboží pro vzorovou položku s průměrnými náklady ZBOŽÍ1 před spuštěním dávkové úlohy **Adjustace nákladů položek zboží**.

| **Datum zaúčtování** | **Typ položky zboží** | **Množství** | **Částka nákladů (skutečná)** | **Číslo položky** |
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
| 01.01.20 | Nákup | 1 | 20,00 | 1 |
| 01.01.20 | Nákup | 1 | 40,00 | 2 |
| 01.01.20 | Prodej | -1 | -20,00 | 3 |
| 1.2.2020 | Prodej | -1 | -40,00 | 4 |
| 2.2.2020 | Nákup | 1 | 100,00 | 5 |
| 3.2.2020 | Prodej | -1 | -100,00 | 6 |

> [!NOTE]  
> Protože k úpravě nákladů dosud nedošlo, hodnoty v poli **Částka nákladů (skutečná)** se snižují, což odpovídá nárůstu zásob, na který se vztahují.

Následující tabulka uvádí položky v tabulce **Místo  zadání úpravy  průměrné ceny**, které se vztahují na položky ocenění vyplývající z položek zboží v předchozí tabulce.

| **Číslo zboží** | **Kód varianty** | **Kód lokace** | **Datum ocenění** | **Náklady jsou adjustovány** |
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
| ZBOŽÍ1 | | MODRÝ | 01.01.20 | Ne |
| ZBOŽÍ1 | | MODRÝ | 1.2.2020 | Ne |
| ZBOŽÍ1 | | MODRÝ | 2.2.2020 | Ne |
| ZBOŽÍ1 | | MODRÝ | 3.2.2020 | Ne |

V následující tabulce jsou stejné položky zboží po spuštění dávkové úlohy **Adjustace nákladů položek zboží**. Průměrné náklady za den se počítají a aplikují na snížení zásob.

| **Datum zaúčtování** | **Typ položky zboží** | **Množství** | **Částka nákladů (skutečná)** | **Číslo položky** |
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
| 01.01.20 | Nákup | 1 | 20,00 | 1 |
| 01.01.20 | Nákup | 1 | 40,00 | 2 |
| 01.01.20 | Prodej | -1 | -30,00 | 3 |
| 1.2.2020 | Prodej | -1 | -30,00 | 4 |
| 2.2.2020 | Nákup | 1 | 100,00 | 5 |
| 3.2.2020 | Prodej | -1 | -100,00 | 6 |

### Příklad: Období průměrných nákladů = Měsíc
Následující příklad ukazuje účinek výpočtu průměrných nákladů na základě průměrných nákladů jednoho měsíce. Pole **Typ výpočtu prům.poř. ceny** na stránce **Nastavení zásob** je nastaveno na **Zboží**.

Pokud je období průměrných nákladů jeden měsíc, vytvoří se pro každou kombinaci čísla zboží, kódu varianty, kódu lokace a data ocenění pouze jedna položka.

V následující tabulce jsou uvedeny položky zboží pro vzorovou položku s průměrnými náklady ZBOŽÍ1 před spuštěním dávkové úlohy **Adjustace nákladů položek zboží**.

| **Datum zaúčtování** | **Typ položky zboží** | **Množství** | **Částka nákladů (skutečná)** | **Číslo položky** |
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
| 01.01.20 | Nákup | 1 | 20,00 | 1 |
| 01.01.20 | Nákup | 1 | 40,00 | 2 |
| 01.01.20 | Prodej | -1 | -20,00 | 3 |
| 01.02.20 | Prodej | -1 | -40,00 | 4 |
| 02.02.20 | Nákup | 1 | 100,00 | 5 |
| 03.02.20 | Prodej | -1 | -100,00 | 6 |

> [!NOTE]  
> Protože k úpravě nákladů ještě nedošlo, hodnoty v poli **Částka nákladů (skutečná)** se snižují, což odpovídá zvýšení zásob, na které se vztahují.

Následující tabulka uvádí položky v tabulce **Místo  zadání úpravy  průměrné ceny**, které se vztahují na položky ocenění vyplývající z položek zboží v předchozí tabulce.

| **Číslo zboží** | **Kód varianty** | **Kód lokace** | **Datum ocenění** | **Náklady jsou adjustovány** |
|-------------------------------------|-----------------------------------------|------------------------------------------|-------------------------------------------|---------------------------------------------|  
| ZBOŽÍ1 | | MODRÝ | 31.01.20 | Ne |
| ZBOŽÍ1 | | MODRÝ | 28.02.20 | Ne |

> [!NOTE]  
> Datum ocenění je nastaveno na poslední den v období průměrných nákladů, což je v tomto případě poslední den měsíce.

V následující tabulce jsou stejné položky zboží po spuštění dávkové úlohy **Adjustace nákladů položek zboží**. Průměrné náklady za měsíc se počítají a aplikují na snížení zásob.

| **Datum zaúčtování** | **Typ položky zboží** | **Množství** | **Částka nákladů (skutečná)** | **Číslo položky** |
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
| 01.01.20 | Nákup | 1 | 20,00 | 1 |
| 01.01.20 | Nákup | 1 | 40,00 | 2 |
| 01.01.20 | Prodej | -1 | -30,00 | 3 |
| 1.2.2020 | Prodej | -1 | -65,00 | 4 |
| 2.2.2020 | Nákup | 1 | 100,00 | 5 |
| 3.2.2020 | Prodej | -1 | -65,00 | 6 |

Průměrné náklady položky číslo 3 se počítají v období průměrných nákladů za leden a průměrné náklady pro položky 4 a 6 se počítají v období průměrných nákladů za únor.

Chcete-li získat průměrné náklady za únor, k průměrné ceně na začátku období (30,00) se přidají průměrné náklady na kus obdržený v zásobách (100,00). Součet těchto dvou (130,00) se poté vydělí celkovým množstvím v zásobách (2). Získají se tak výsledné průměrné náklady na zboží za únorové období (65,00). Průměrné náklady jsou přiřazeny ke snížení zásob v období (položky 4 a 6).

## Nastavení data ocenění
Pole **Datum ocenění** v tabulce **Položka ocenění** se používá k určení, do kterého období průměrných nákladů patří položka snížení zásob. To platí také pro zásoby nedokončené výroby (NV).

V následující tabulce jsou uvedena kritéria, která se používají k nastavení data ocenění.

| Scénář | Zúčtovací datum | Oceněné množství | Přecenění | Datum ocenění |
|--------------|-------------------------------------|-----------------------------------------|-----------------|-----------------------------------------|  
| 1 | | Pozitivní | Ne | Datum zaúčtování položky zboží |
| 2 | Pozdější než poslední datum ocenění použitých položek ocenění | Negativní | Ne | Datum zaúčtování položky zboží |
| 3 | Dříve než poslední datum ocenění použitých položek ocenění | Pozitivní | Ne | Poslední datum ocenění použitých položek ocenění |
| 4 | | Negativní | Ano | Zúčtovací datum položky přecenění |

### Příklad
Následující tabulka položek ocenění ilustruje různé scénáře.

| Scénář | Zúčtovací datum | Typ položky zboží | Datum ocenění | Oceněné množství | Částka nákladů (skutečná) | Číslo položky zboží | Číslo položky |
|--------------|-------------------------------------|-----------------------------------------------|-----------------------------------------|-----------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
| 1 | 01.01.20 | Nákup | 01.01.20 | 2 | 20,00 | 1 | 1 |
| 2 | 15.01.20 | (Poplatek za zboží) | 01.01.20 | 2 | 8,00 | 1 | 2 |
| 3 | 01.02.20 | Prodej | 01.02.20 | -1 | -14,00 | 2 | 3 |
| 4 | 01.03.20 | (Přecenění) | 01.03.20 | 1 | -.4,00 | 1 | 4 |
| 5 | 01.02.20 | Prodej | 01.03.20 | -1 | -10,00 | 3 | 5 |

> [!NOTE]  
> V položce číslo 5 v předchozí tabulce uživatel zadal prodejní objednávku s datem zaúčtování (1.2.2020), které nastane před posledním datem ocenění použitých položek ocenění (1.3.2020). Pokud byla pro tuto položku použita odpovídající hodnota v poli **Částka nákladů (skutečná)** pro toto datum (1.2.2020), bude to 14,00. To by znamenalo situaci, kdy je množství na skladě nulové, ale hodnota zásob je –4,00.
>
> Aby se předešlo takovému nesouladu mezi hodnotou a množstvím, je datum ocenění nastaveno tak, aby se rovnalo poslednímu dni ocenění použitých položek ocenění (1.3.2020). Hodnota v poli **Částka nákladů (skutečná)** se změní na 10,00 (po přecenění), což znamená, že množství na skladě je nulové a hodnota zásob je také nulová.

> [!CAUTION]  
> Protože sestava **Hodnota zásob** je založena na datu zaúčtování, bude tato sestava odrážet případné neshody mezi hodnotou a množstvím ve scénářích jako ve výše uvedeném příkladu. Pro více informací navštivte [Detaily návrhu: Hodnota zásob](design-details-inventory-valuation.md).

Pokud je množství na skladě po zaúčtování snížení zásob menší než nula, je datum ocenění nejprve nastaveno na zúčtovací datum snížení zásob. Toto datum může být později změněno podle pravidel popsaných v poznámce dříve v této části, když se použije zvýšení zásob.

## Přepočet průměrných nákladů
Oceňování poklesu zásob jako váženého průměru by bylo jednoduché, pokud by nákupy byly vždy fakturovány před fakturou prodeje, účtování nebylo nikdy zastaralé a nikdy jste neudělali chyby. Realita se však od tohoto ideálu poněkud liší.

Jak je znázorněno v příkladech v tomto tématu, datum ocenění je definováno jako datum, od kterého je položka ocenění zahrnuta do výpočtu průměrných nákladů. To vám dává flexibilitu provádět u položek pomocí metody průměrných nákladů následující:

- Fakturovat prodej zboží před fakturou nákupu zboží.
- Zpětně datovat účtování.
- Obnovit nesprávné zaúčtování.

> [!NOTE]  
> Dalším důvodem této flexibility je pevné vyrovnání. Další informace o pevném vyrovnání naleznete v tématu [Detaily návrhu: Vyrovnání zboží](design-details-item-application.md).

Z důvodu této flexibility může být možné, že budete muset přepočítat průměrné náklady po souvisejícím zaúčtování. Pokud například zaúčtujete zvýšení nebo snížení zásob s datem ocenění, které předchází snížení jednoho nebo více zásob. K přepočtu průměrných nákladů dojde automaticky při spuštění dávkové úlohy **Adjustace nákladů položek zboží**.

Základ ocenění zásob je možné změnit v účetním období změnou pole **Období průměrných nákladů** a **Typ výpočtu prům.poř. ceny**. To by však mělo být prováděno opatrně a po dohodě s auditorem.

### Příklad
Následující příklad znázorňuje, jak jsou průměrné náklady přepočítaly, když je k datu, které předchází snížení jednoho nebo více zásob, zavedeno opožděné zaúčtování. Příklad je založen na období průměrných nákladů **Den**.

V následující tabulce jsou uvedeny položky ocenění, které existují pro zboží před zavedením účtování.

| Datum ocenění | Množství | Částka nákladů (skutečná) | Číslo položky |
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
| 01.01.20 | 1 | 10,00 | 1 |
| 2.1.2020 | 1 | 20,00 | 2 |
| 15.2.2020 | -1 | -15,00 | 3 |
| 16.2.2020 | -1 | -15,00 | 4 |

Uživatel zaúčtuje zvýšení zásob (číslo položky 5) s datem ocenění (3.1.2020), které předchází snížení jednoho nebo více zásob. Pro vyvážení zásob je nutné přepočítat průměrné náklady a upravit je na 17,00.

Následující tabulka ukazuje položky ocenění, které existují pro položku po zavedení položky číslo 5.

| Datum ocenění | Množství | Částka nákladů (skutečná) | Číslo položky |
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
| 01.01.20 | 1 | 10,00 | 1 |
| 2.1.2020 | 1 | 20,00 | 2 |
| 3.1.2020 | 1 | 21,00 | 5 |
| 15.2.2020 | -1 | -17,00 | 3 |
| 16.2.2020 | -1 | -17,00 | 4 |

## Viz také
[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)     
[Detaily návrhu: Metody ocenění](design-details-costing-methods.md)     
[Detaily návrhu: Úprava nákladů](design-details-cost-adjustment.md)     
[Detaily návrhu: Vyrovnání zboží](design-details-item-application.md)    
[Správa nákladů zásob](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]