---
title: Design Details - Costing Methods
description: This topic describes how the costing method affects how actual and budgeted values are capitalized and used in the cost calculation.
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 30, 42, 43
ms.date: 06/14/2021
ms.author: bholtorf

---
# Detaily návrhu: Metody ocenění

Metoda ocenění určuje, zda je skutečná nebo rozpočtovaná hodnota aktivována a použita při výpočtu nákladů. Metoda ocenění spolu s datem a posloupností účtování také ovlivňuje způsob zaznamenávání nákladového toku.

> [!NOTE]
> Metodu ocenění zboží nelze změnit, pokud pro dané zboží existují záznamy v položkách zboží. Pro více informace navštivte [Detaily návrhu: Změna metod ocenění pro zboží](design-details-changing-costing-methods.md).

Následující metody jsou podporovány v [!INCLUDE[prod_short](includes/prod_short.md)]:

| Metoda ocenění | Popis | Kdy použít |
|--|--|--|
| FIFO | Jednotková cena zboží je skutečná hodnota jakéhokoli příjmu zboží zvolená pravidlem FIFO.<br /><br /> Při oceňování zásob se předpokládá, že první zboží umístěné do zásob je prodáno jako první. | V podnikovém prostředí, kde jsou náklady na zboží stabilní.<br /><br /> (Když ceny rostou, rozvaha vykazuje větší hodnotu. To znamená, že se zvyšují daňové povinnosti, ale zlepšuje se kreditní skóre a schopnost půjčovat si hotovost.)<br /><br /> Pro zboží s omezenou dobou použitelnosti, protože nejstarší zboží je třeba prodat, než překročí datum prodeje. |
| LIFO | Jednotková cena zboží je skutečná hodnota jakéhokoli příjmu zboží zvolená pravidlem LIFO.<br /><br /> Při oceňování zásob se předpokládá, že poslední zboží umístěné v zásobách je prodáno jako první. | Zakázáno v mnoha zemích/oblastech, protože může být použito ke snížení zisku.<br /><br /> (Když ceny rostou, hodnota ve výsledovce klesá. To znamená, že daňové závazky se snižují, ale schopnost půjčovat si hotovost se zhoršuje.) |
| Průměr | Jednotková cena zboží se vypočítá jako průměrná jednotková cena v každém okamžiku po nákupu.<br /><br /> Pro ocenění zásob se předpokládá, že všechny zásoby jsou prodány současně. | V obchodním prostředí, kde jsou náklady na produkt nestabilní.<br /><br /> Když jsou zásoby nahromaděny nebo smíchány dohromady a nelze je rozlišit, jako jsou chemikálie. |
| Otevřená položka | Jednotková cena zboží je přesná cena, za kterou byla konkrétní jednotka přijata. | Při výrobě nebo obchodu snadno identifikovatelného zboží s poměrně vysokými jednotkovými náklady.<br /><br /> Pro zboží, které podléhá regulaci.<br /><br /> Pro zboží se sériovými čísly. |
| Pevná cena | Jednotková cena zboží je přednastavena na základě odhadované.<br /><br /> Když se později zjistí skutečné náklady, musí se standardní náklady upravit na skutečné náklady prostřednictvím hodnot odchylky. | Tam, kde je kontrola nákladů kritická.<br /><br /> Při opakované výrobě ocenit náklady na přímý materiál, přímou práci a výrobní režii.<br /><br /> Tam, kde je disciplína a personál k udržení standardů. |

Následující obrázek znázorňuje, jak náklady procházejí zásobami pro každou metodu ocenění.

![Metody ocenění.](media/design_details_inventory_costing_7_costing_methods.png "Metody ocenění")

Metody ocenění se liší způsobem, jakým oceňují snížení zásob a zda jako základ ocenění používají pevnou pořizovací cenu nebo skutečné náklady. Následující tabulka vysvětluje různé charakteristiky. (Metoda LIFO je vyloučena, protože je velmi podobná metodě FIFO.)

|Kategorie|FIFO|Průměrná cena|Pevná cena|Otevřená položka|  
|-|----------|-------------|--------------|--------------|  
|Obecná charakteristika|Snadno pochopitelná|Na základě možností období: **Den**/**Týden**/**Měsíc**/**Čtvrtletí**/**Účetní období**.<br /><br /> Lze vypočítat na zboží nebo na zboží/lokaci/variantu.|Snadné použití, ale vyžaduje kvalifikovanou údržbu.|Vyžaduje sledování zboží u příchozích i odchozích transakcí.<br /><br /> Obvykle se používá pro serializované zboží.|  
|Aplikace/Úprava|Aplikace sleduje **zbývající množství**.<br /><br /> Úprava převádí náklady podle aplikace množství.|Aplikace sleduje **zbývající množství**.<br /><br /> Náklady se vypočítají a předají k **datumu ocenění**.|Aplikace sleduje **zbývající množství**.<br /><br /> Aplikace je založena na FIFO.|Všechny aplikace jsou opraveny.|  
|Přecenění|Přeceňuje pouze fakturované množství.<br /><br /> Lze provést pro zboží nebo pro každý záznam v položkách zboží.<br /><br /> Lze provést zpětně v čase.|Přeceňuje pouze fakturované množství.<br /><br /> Lze provést pouze pro zboží.<br /><br /> Lze provést zpětně v čase.|Přeceňuje fakturovaná a nevyfakturovaná množství.<br /><br /> Lze provést pro zboží nebo za zboží v položkách zboží.<br /><br /> Lze provést zpětně v čase.|Přeceňuje pouze fakturované množství.<br /><br /> Lze provést pro zboží nebo zboží v položkách zboží.<br /><br /> Lze provést zpětně v čase.|  
|Různé|Pokud provedete zpětné datum snížení zásob, pak stávající zboží NENÍ znovu použito k zajištění správného toku nákladů FIFO.|Pokud provedete zpětné datování zvýšení nebo snížení zásob, pak se průměrné náklady přepočítají a všechny dotčené položky budou upraveny.<br /><br /> Pokud změníte období nebo typ výpočtu, musí být upraveny všechny dotčené položky.|K pravidelné aktualizaci a načítání standardních nákladů použijte stránku **Standardní sešit**.<br /><br /> NENÍ podporováno pro SKJ.<br /><br /> Pro pevnou cenu neexistují žádné historické záznamy.|Sledování konkrétního zboží můžete použít bez použití metody otevřené položky. Pak se cena NEBUDE řídit číslem šarže, ale předpokladem nákladů zvolené metody ocenění.|

## Příklad

V této části jsou uvedeny příklady toho, jak různé metody ocenění ovlivňují hodnotu zásob.

V následující tabulce jsou uvedeny nárůsty a snížení zásob, na kterých jsou příklady založeny.

| Zúčtovací datum | Množství | Číslo položky |
|------------------|--------------|---------------|  
| 01.01.20 | 1 | 1 |
| 01.01.20 | 1 | 2 |
| 01.01.20 | 1 | 3 |
| 01.02.20 | -1 | 4 |
| 01.03.20 | -1 | 5 |
| 01.04.20 | -1 | 6 |

> [!NOTE]  
> Výsledné množství na skladě je nulové. V důsledku toho musí být hodnota zásob také nulová, bez ohledu na metodu ocenění.

### Vliv metody kalkulace na zvýšení ocenění zásob

- **FIFO**/**LIFO**/**Průměrná cena**/**Otevřená položka**

   U zboží s metodami ocenění, které používají skutečné náklady jako základ ocenění (**FIFO**, **LIFO**, **Průměrná cena**, nebo **Otevřená položka**), se zvýšení zásob oceňuje náklady na pořízení zboží.

   Následující tabulka ukazuje, jak se zvyšují zásoby pro všechny metody ocenění s výjimkou **Pevné ceny**.

   | Zúčtovací datum | Množství | Částka nákladů (skutečná) | Číslo položky |
   |------------------|--------------|----------------------------|---------------|  
   | 01.01.20 | 1 | 10,00 | 1 |
   | 01.01.20 | 1 | 20,00 | 2 |
   | 01.01.20 | 1 | 30,00 | 3 |

- **Pevná cena**

   U zboží používající metodu ocenění **Pevná cena** se zvýšení zásob oceňuje aktuální standardní cenou zboží.

   Následující tabulka ukazuje, jak jsou zvýšení zásob oceňována pro metodu ocenění **Pevná cena**.

   | Zúčtovací datum | Množství | Částka nákladů (skutečná) | Číslo položky |
   |------------------|--------------|----------------------------|---------------|  
   | 01.01.20 | 1 | 15,00 | 1 |
   | 01.01.20 | 1 | 15,00 | 2 |
   | 01.01.20 | 1 | 15,00 | 3 |

### Vliv metod ocenění na snížení cen zásob

- **FIFO**

   U zboží používající metodu icenění **FIFO** je zboží, které bylo zakoupeno jako první, vždy prodáno jako první (v tomto příkladu jsou uvedena čísla položek 3, 2 a 1). V souladu s tím se snížení zásob oceňuje tím, že se vezme hodnota prvního zvýšení zásob.

   NNPZ se vypočítá pomocí hodnoty prvních pořízení zásob.

   Následující tabulka ukazuje, jak se oceňují snížení zásob pro metodu ocenění **FIFO**.

   | Zúčtovací datum | Množství | Částka nákladů (skutečná) | Číslo položky |
   |------------------|--------------|----------------------------|---------------|  
   | 01.02.20 | -1 | -10,00 | 4 |
   | 01.03.20 | -1 | -20,00 | 5 |
   | 01.04.20 | -1 | -30,00 | 6 |

- **LIFO**

   U zboží používající metodu ocenění **LIFO** je zboží, které bylo zakoupeno naposledy, vždy prodáno jako první (v tomto příkladu čísla položek 3, 2 a 1). V souladu s tím se snížení zásob oceňuje tak, že se vezme hodnota posledního zvýšení zásob.

   NNPZ se vypočítá pomocí hodnoty posledních pořízení zásob.

   Následující tabulka ukazuje, jak se oceňují snížení zásob pro metodu ocenění **LIFO**.

   | Zúčtovací datum | Množství | Částka nákladů (skutečná) | Číslo položky |
   |------------------|--------------|----------------------------|---------------|  
   | 01.02.20 | -1 | -30,00 | 4 |
   | 01.03.20 | -1 | -20,00 | 5 |
   | 01.04.20 | -1 | -10,00 | 6 |

- **Průměrná cena**

   U zboží používající metodu ocenění **Průměrná cena** se snížení zásob oceňuje výpočtem váženého průměru zbývajících zásob k poslednímu dni průměrného nákladového období, ve kterém bylo zaúčtováno snížení zásob. Pro více informací navštivte [Detaily návrhu: Průměrné náklady](design-details-average-cost.md).

   Následující tabulka ukazuje, jak se oceňuje snížení zásob pro metodu ocenění **Průměrná cena**.

   | Zúčtovací datum | Množství | Částka nákladů (skutečná) | Číslo položky |
   |------------------|--------------|----------------------------|---------------|  
   | 01.02.20 | -1 | -20,00 | 4 |
   | 01.03.20 | -1 | -20,00 | 5 |
   | 01.04.20 | -1 | -20,00 | 6 |

- **Pevná cena**

   U zboží používající metodu ocenění **Pevná cena** se úbytky zásob oceňují podobně jako pro metodu ocenění **FIFO**, s tím rozdílem, že ocenění je založeno na pevné pořizovací ceně, nikoli na skutečných nákladech.

   Následující tabulka ukazuje, jak se oceňuje snížení zásob pro metodu ocenění **Pevná cena**.

   | Zúčtovací datum | Množství | Částka nákladů (skutečná) | Číslo položky |
   |------------------|--------------|----------------------------|---------------|  
   | 01.02.20 | -1 | -15,00 | 4 |
   | 01.03.20 | -1 | -15,00 | 5 |
   | 01.04.20 | -1 | -15,00 | 6 |

- **Otevřená položka**

   Metody ocenění vycházejí z předpokladu, jakým způsobem probíhá tok nákladů od zvýšení zásob ke snížení. Pokud však existují přesnější informace o toku nákladů, můžete tento předpoklad přepsat vytvořením pevného vyrovnání mezi položkami. Pevné vyrovnání vytváří vazbu mezi snížením zásob a konkrétním zvýšením zásob a podle toho řídí tok nákladů.

   U zboží, které používá metodu ocenění **Otevřená položka**, jsou snížení zásob oceněna podle zvýšení zásob, se kterým je propojeno pevným vyrovnáním.

   Následující tabulka ukazuje, jak se oceňuje snížení zásob pro metodu ocenění **Otevřená položka**.

   | Zúčtovací datum | Množství | Částka nákladů (skutečná) | Vyrovnává položku | Číslo položky |
   |------------|--------|--------------------|----------------|---------|  
   | 01.02.20 | -1 | -20,00 | **2** | 4 |
   | 01.03.20 | -1 | -10,00 | **1** | 5 |
   | 01.04.20 | -1 | -30,00 | **3** | 6 |

## Viz také

[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)     
[Detaily návrhu: Odchylka](design-details-variance.md)     
[Detaily návrhu: Průměrné náklady](design-details-average-cost.md)     
[Detaily návrhu: Vyrovnání zboží](design-details-item-application.md)    
[Přehled nákladů na zásoby](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]