---
title: Design Details - Item Application | Microsoft Docs
description: This topic describes where inventory quantity and value are recorded when you post an inventory transaction.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, items, ledger entries, posting, inventory
ms.date: 06/08/2021
ms.author: edupont

---
# Detaily návrhu: Vyrovnání zboží

Když zaúčtujete skladovou transakci, zaúčtování množství se zaznamená do položek zboží, zaúčtování hodnoty do položek ocenění. Pro více informací navštivte [Detaily návrhu: Účtování zásob](design-details-inventory-posting.md).

Kromě toho je vytvořeno vyrovnání zboží, které propojí příjemce nákladů s jeho zdrojem nákladů a poskytuje přeposílání nákladů podle metody ocenění. Pro více informace navštivte [Detaily návrhu: Metody ocenění](design-details-costing-methods.md).

[!INCLUDE[prod_short](includes/prod_short.md)] vytváří dva typy vyrovnání zboží.

| Typ vyrovnání | Popis |
|----------------------|---------------------------------------|  
| Vyrovávání množství | Vytvořeno pro všechny inventarizační transakce |
| Vyrovávání nákladů | Vytvořeno pro příchozí položky spolu vyrovnáváním množství v důsledku interakce uživatele ve speciálních procesech. |

Vyrovávání položek lze provádět následujícími způsoby.

| Metoda | Popis | Typ vyrovnání |
|------------|---------------------------------------|----------------------|  
| Automatické | Vyskytuje se jako obecné přeposílání nákladů podle metody výpočtu nákladů. | Vyrovávání množství |
| Pevné | Vytvořeno uživatelem, když:<br /><br /> -   Zpracování se vrátí<br />-   Účtování oprav<br />-   Účtování vrácení množství<br />-   Vytváření přímých dodávek **Poznámka:**  Pevné vyrovnání může být vytvořeno mauálně a to vložením čísla položky v poli **Vyrovnáno položkou zboží** nebo pomocí funkce jako třeba **Získat účt. řádky pro stornování**. | Vyrovnání množství<br /><br /> Vyrovnání ceny **Poznámka:**  Vyrovnání ceny nastane pouze u příchozích transakcí, kde pole **Vyrovnáno položkou zboží** je vyplněno aby se vytvořilo pevné vyrování. Viz následující tabulka. |

To, zda jsou vyrovnání množství nebo vyrovnání nákladů, závisí na směru skladové transakce a na tom, zda je aplikace zboží podána automaticky nebo pevně v souvislosti se speciálními procesy.

Následující tabulka ukazuje, na základě centrálních polí vyrovnání na řádcích transakce zásob, jak náklady plynou v závislosti na směru transakce. Označuje také, kdy a proč je vyrovnání zboží typu množství nebo náklady.

|-|Vyrovnat položkou na nákupním řádku|Vyrovnat položkou na nákupním řádku|  
|-|--------------------------------|----------------------------------|  
|Vyrovnání pro for výstupní položku|Výstupní položka táhne cenu z otevřené příchozí položky vyrovnání zboží.<br /><br /> **Vyrovnání množství**|Nepodporováno|  
|Vyrovnání pro příchozí položky|Příchozí položky tlačí cenu do otevřené vyrovnané položky.<br /><br /> Příchozí položky jsou zdrojem nákladů.<br /><br /> **Vyrovnání množství**|Příchozí položky táhnou cenu z výstupní položky. **Poznámka**  Při vytváření tohoto pevného vyrovnání se příchozí transakce považuje za prodejní vratku. Proto odchozí položka zůstane otevřená. <br /><br /> Příchozí položka NENÍ zdrojem nákladů.<br /><br /> **Vyrovávání nákladů**|

> [!IMPORTANT]  
> Při pevném vyrovnání NENÍ prodejní vratka považována za zdroj nákladů.
>
> Položka prodeje zůstane otevřená, dokud nebude zaúčtován skutečný zdroj.

Záznam položky vyrovnání zboží zaznamenává následující informace.

| Pole | Popis |
|---------------------------------|---------------------------------------|  
| **Číslo položky zboží** | Číslo položky zboží pro transakci, pro kterou je toto vyrovnání zboží vytvořeno. |
| **Číslo vstupní položky zboží** | Číslo položky zboží zvýšení zásob, ke kterému má být transakce navázána, je-li to relevantní. |
| **Číslo výstupní položky zboží** | Číslo položky zboží snížení zásob, se kterým by měla být transakce propojena, pokud je to možné. |
| **Množství** | Použité množství. |
| **Datum zaúčtování** | Datum zaúčtování transakce. |

## Zvýšení zásob
Když zaúčtujete zvýšení zásob, pak se jednoduchá položka vyrovnání zboží zaznamená bez vyrovnání do výstupní položky.

### Příklad
Následující tabulka ukazuje položku vyrovnání zboží, která se vytvoří, když zaúčtujete potvrzení o nákupu 10 jednotek.

| Zúčtovací datum | Číslo vstupní položky zboží | Číslo výstupní položky zboží | Množství | Číslo položky zboží |
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
| 01.01.20 | 1 | 0 | 10 | 1 |

## Snížení zásob
Když zaúčtujete snížení zásob, vytvoří se položka vyrovnání zboží, která propojí snížení zásob s nárůstem zásob. Tento odkaz je vytvořen pomocí metody metody ocenění zboží jako směrnice. U zboží používajících metody ocenění FIFO, Standardní a průměrnú metodu ocenění je propojení založeno na principu „první dovnitř, první ven“. Snížení zásob se aplikuje na přírůstek zásob s nejbližším datem zaúčtování. U položek používajících metodu ocenění LIFO je propojení založeno na principu "poslední dovnitř, první ven". Snížení zásob se použije na zvýšení zásob s posledním datem zaúčtování.

V tabulce **Položka zboží** zobrazuje pole **Zbývající množství** množství, které ještě nebylo použito. Pokud je zbývající množství větší než 0, je zaškrtnuto políčko **Otevřít**.

### Příklad
Následující příklad ukazuje položku vyrovnání zboží, která se vytvoří, když zaúčtujete 5 jednotek zboží prodejní dodávku, které byly přijaty v předchozím příkladu. První položka vyrovnání zboží je nákupní doklad. Druhou položkou vyrovnání zboží je prodejní dodávka.

V následující tabulce jsou uvedeny dvě položky vyrovnání zboží, které jsou výsledkem zvýšení a snížení zásob.

| Zúčtovací datum | Číslo vstupní položky zboží | Číslo výstupní položky zboží | Množství | Číslo položky zboží |
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
| 01.01.20 | 1 | 0 | 10 | 1 |
| 3.1.2020 | 1 | 2 | -5 | 2 |

## Pevné vyrovnání
Pevné vyrovnání vytvoříte, když určíte, že náklady na zvýšení zásob by se měly vztahovat na konkrétní snížení zásob nebo naopak. Pevné vyrovnání ovlivňuje zbývající množství položek, ale také obrátí přesné náklady na původní položku, na kterou nebo z které aplikujete.

Chcete-li vytvořit pevné vyrovnání, použijte pole **Vyrovnat položkou zboží** nebo pole **Vyrovnáno položkou zboží** v řádcích dokladu k určení položky zboží, na kterou nebo z které se má řádek transakce vztahovat. Můžete například vytvořit pevné vyrovnání, když chcete vytvořit vyrovnání nákladů, která určuje, že prodejní vratka by se měla vztahovat na konkrétní prodejní dodávku, aby se obrátily náklady na prodejní dodávku. V tomto případě [!INCLUDE[prod_short](includes/prod_short.md)] ignoruje metodu ocenění a použije snížení nebo zvýšení zásob pro prodejní vratku na položku zboží, kterou určíte. Výhodou vytvoření pevného vyrovnání je, že náklady na původní transakci jsou přeneseny na novou transakci.

### Příklad – Pevné vyrovnání v prodejní vratce
Následující příklad, který ilustruje účinek pevného vyrovnání nákupní vratky položky pomocí metody FIFO, je založen na následujícím scénáři:

1. V položce 1 uživatel zaúčtuje nákup za cenu 10,00 LM.
2. V položce 2 uživatel zaúčtuje nákup za cenu 20,00 LM.
3. V položce 3 uživatel zaúčtuje nákupní vratku. Uživatel provede pevné vyrovnání na druhý nákup zadáním čísla položky zboží do pole **Vyrovnat položkou zboží** na řádku objednávky nákupní vratky.

V následující tabulce jsou uvedeny věcné položky vyplývající ze scénáře.

| **Datum zaúčtování** | **Typ položky zboží** | **Množství** | **Částka nákladů (skutečná)** | **Číslo položky zboží** |
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
| 01-04-20 | Nákup | 10 | 10,00 | 1 |
| 01-05-20 | Nákup | 10 | 20,00 | 2 |
| 01-06-20 | Nákup (vratka) | -10 | -20,00 | 3 |

Vzhledem k tomu, že od nákupní vratky do druhé nákupní položky je provedené pevné vyrovnání, jsou položky vráceny se správnou cenou. Pokud by uživatel neprovedl pevné vyrovnání, pak by vrácené zboží bylo nesprávně oceněné na 10,00 LM, protože vratka by byla použita na první nákupní položku podle principu FIFO.

V následující tabulce je uvedena položka vyrovnání zboží, která je výsledkem pevného vyrovnání.

| Zúčtovací datum | Číslo vstupní položky zboží | Číslo výstupní položky zboží | Množství | Číslo položky zboží |
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
| 01-06-20 | 2 | 3 | 10 | 3 |

Náklady na druhý nákup, 20,00 LM, jsou správně předány do nákupní vratky.

### Příklad – pevné vyrovnání s průměrnými náklady
Následující příklad, který ilustruje účinek pevného vyrovnání, je založen na následujícím scénáři pro zboží, které používá průměrnú metodu ocenění:

1. V číslech položky 1 a 2 uživatel zaúčtuje dvě nákupní faktury. Druhá faktura obsahuje nesprávné přímé jednotkové náklady 1 000,00 LM.
2. V položce číslo 3 uživatel zaúčtuje nákupní dobropis s pevným vyrovnáním aplikovanýn na položku nákupu s nesprávnými přímými jednotkovými náklady. Součet pole **Částka nákladů (skutečná)** pro dvě pevně vyrovnané položky se změní na 0,00
3. V položce číslo 4 uživatel zaúčtuje další nákupní fakturu se správnou přímou jednotkovou cenou 100,00 LM
4. V položce číslo 5 uživatel zaúčtuje prodejní fakturu.
5. Množství zásob je 0 a hodnota zásob je také 0,00

V následující tabulce je uveden výsledek scénáře u položek ocenění zboží.

Následující tabulka ukazuje výsledek scénáře u položek ocenění zboží po dokončení zaúčtování a spuštění úpravy nákladů.

| Zúčtovací datum | Typ položky zboží | Oceněné množství | Částka nákladů (skutečná) | Vyrovnat položkou zboží | Oceněno prům.náklady | Číslo položky zboží | Číslo položky |
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
| 01.01.20 | Nákup | 1 | 200,00 | Ne | 1 | 1 |
| 01.01.20 | Nákup | 1 | 1000,00 | Ne | 2 | 2 |
| 01.01.20 | Nákup | -1 | -1000 | 2 | Ne | 3 | 3 |
| 01.01.20 | Nákup | 1 | 100,00 | Ne | 4 | 4 |
| 01.01.20 | Prodej | -2 | -300,00 | Ano | 5 | 5 |

Pokud by uživatel neprovedl pevné vyrovnání mezi nákupním dobropisem a nákupem s nesprávnými přímými jednotkovými náklady (krok 2 v předchozím scénáři), pak by byly náklady upraveny odlišně.

Následující tabulka ukazuje výsledek u položek ocenění zboží, pokud je krok 2 v předchozím scénáři proveden bez pevného vyrovnání.

| Zúčtovací datum | Typ položky zboží | Oceněné množství | Částka nákladů (skutečná) | Vyrovnat položkou zboží | Oceněno prům.náklady | Číslo položky zboží | Číslo položky |
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
| 01.01.20 | Nákup | 1 | 200,00 | Ne | 1 | 1 |
| 01.01.20 | Nákup | 1 | 1000,00 | Ne | 2 | 2 |
| 01.01.20 | Nákup | -1 | 433,33 | Ano | 3 | 3 |
| 01.01.20 | Nákup | 1 | 100,00 | Ne | 4 | 4 |
| 01.01.20 | Prodej | -2 | 866,67 | Ano | 5 | 5 |

V položce číslo 3 je hodnota v poli **Částka nákladů (skutečná)** oceněna průměrem, a proto zahrnuje chybné zaúčtování 1000,00. V souladu s tím se stává -433,33, což je nadhodnocená částka nákladů. Výpočet je 1300 / 3 = .-433,33.

V položce číslo 5 je hodnota pole **Částka nákladů (skutečná)** pro tuto položku také nepřesná ze stejného důvodu.

> [!NOTE]  
> Pokud vytvoříte pevné vyrovnání pro snížení zásob u položky, která používá metodu Průměrného ocenění nákladů, pak snížení neobdrží průměrné náklady na položku jako obvykle, ale místo toho obdrží náklady na zvýšení zásob, které jste zadali. Toto snížení zásob pak již není součástí kalkulace průměrných nákladů.

### Příklad – Pevné vyrovnání v prodejní vratce
Pevné vyrovnání je také velmi dobrým prostředkem k přesnému vrácení nákladů, například pomocí prodejní vratky.

Následující příklad, který ilustruje, jak pevné vyrovnání zajišťuje přesné zvrácení nákladů, je založen na následujícím scénáři:

1. Uživatel zaúčtuje nákupní fakturu.
2. Uživatel zaúčtuje prodejní fakturu.
3. Uživatel zaúčtuje prodejní dobropis pro vrácené zboží, které se vztahuje na položku prodeje, aby správně vrátil náklady.
4. Přijde náklad na přepravu související s dříve zaúčtovanou nákupní objednávkou. Uživatel ji zaúčtuje jako poplatek za zboží.

V následující tabulce je uveden výsledek kroků scénáře 1 až 3 u položek ocenění zboží.

| Zúčtovací datum | Typ položky zboží | Oceněné množství | Částka nákladů (skutečná) | Vyrovnáno položkou zboží | Číslo položky zboží | Číslo položky |
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
| 01.01.20 | Nákup | 1 | 1000,00 | 1 | 1 |
| 01.02.20 | Prodej | -1 | 1000,00 | 2 | 2 |
| 01.03.20 | Prodej (Dobropis) | 1 | 1000 | 2 | 3 | 3 |

V následující tabulce je uvedena položka ocenění vyplývající ze scénáře krok 4, zaúčtování poplatku za zboží.

| Zúčtovací datum | Typ položky zboží | Oceněné množství | Částka nákladů (skutečná) | Vyrovnáno položkou zboží | Číslo položky zboží | Číslo položky |
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
| 01.04.20 | (Poplatek za zboží) | 1 | 100,00 | 1 | 4 |

Následující tabulka ukazuje vliv přesného storna nákladů na položky ocenění zboží.

| Zúčtovací datum | Typ položky zboží | Oceněné množství | Částka nákladů (skutečná) | Vyrovnáno položkou zboží | Číslo položky zboží | Číslo položky |
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
| 01.01.20 | Nákup | 1 | 1000,00 | 1 | 1 |
| 01.02.20 | Prodej | -1 | 1100,00 | 2 | 2 |
| 01.03.20 | Prodej (Dobropis) | 1 | 1100,00 | 2 | 3 | 3 |
| 01.04.20 | (Poplatek za zboží) | 1 | 100,00 | 1 | 4 |

Když spustíte dávkovou úlohu **Adjustace nákladů položek zboží**, zvýšené náklady na položku nákupu, v důsledku poplatku za položku, jsou předány do položky prodeje (položka číslo 2). Položka prodeje pak předá tyto zvýšené náklady do položky prodejního kreditu (položka číslo 3). Konečným výsledkem je, že náklady jsou správně stornovány.

> [!NOTE]  
> Pokud pracujete s vratkami nebo dobropisy a máte nastaveno pole **Nutné vrác.přesn.nákladů** buď na stránce **Nastavení nákupu a závazků**, nebo na stránce **Nastavení prodeje a pohledávek**, podle situace, pak [!INCLUDE[prod_short](includes/prod_short.md)] automaticky vyplní různá pole pro zadání žádosti při použití funkce **Kopie z dokladu**. Pokud použijete funkci **Získat účt. řádky pro stornování**, pole se vždy vyplní automaticky.

> [!NOTE]  
> Pokud zaúčtujete transakci s pevným vyronáním a položka zboží, o kterou žádáte, je uzavřena, což znamená, že zbývající množství je nulové, staré vyrovnání se automaticky vrátí zpět a znovu použije položku zboží pomocí pevného vyrovnání, které jste specifikovali.

## Transferové vyrovnání
Když je zboží převedené z jedné lokace do druhé, uvnitř zásob společnosti, pak je vytvořené vyrovnání mezi dvěma položkami převodu. Ocenění položky převodu závisí na metodě ocenění. U zboží používající průměrnú metodu ocenění se ocenění provádí pomocí průměrných nákladů v období průměrných nákladů, ve kterém nastane datum ocenění převodu. U zboží používající jiné metody ocenění se ocenění provádí zpětným sledováním nákladů na původní zvýšení zásob.

### Příklad – Průměrná metoda ocenění
Následující příklad, který ilustruje, jak se aplikují položky převodu, je založen na následujícím scénáři pro položku používající průměrnú metodu ocenění a období průměrných nákladů - Den.

1. Uživatel zakoupí zboží za cenu 10,00 LM.
2. Uživatel zakoupí zboží znovu za cenu 20,00 LM.
3. Uživatel přenese zboží z lokace VÝCHOD na lokaci ZÁPAD.

Následující tabulka ukazuje vliv převodu na položky ocenění zboží.

| Zúčtovací datum | Typ položky zboží | Kód lokace | Oceněné množství | Částka nákladů (skutečná) | Číslo položky |
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
| 01.01.20 | Nákup | EAST | 1 | 10,00 | 1 |
| 01.01.20 | Nákup | EAST | 1 | 20,00 | 2 |
| 01.02.20 | Transfer | EAST | -1 | 15,00 | 3 |
| 01.02.20 | Transfer | ZÁPAD | 1 | 15,00 | 4 |

### Příklad – standardní metoda ocenění
Následující příklad, který ukazuje, jak jsou použity položky převodu, je založen na následujícím scénáři pro zboží používající standardní metodu kocenění a období průměrných nákladů - Den.

1. Uživatel zakoupí zboží za standardní cenu 10,00 LM.
2. Uživatel přenese zboží z lokace VÝCHOD na lokaci ZÁPAD za standardní cenu 12,00 LM.

Následující tabulka ukazuje vliv převodu na položky ocenění zboží.

| Zúčtovací datum | Typ položky zboží | Kód lokace | Oceněné množství | Částka nákladů (skutečná) | Číslo položky |
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
| 01.01.20 | Nákup | EAST | 1 | 10,00 | 1 |
| 01.02.20 | Transfer | EAST | -1 | 10,00 | 2 |
| 01.02.20 | Transfer | ZÁPAD | 1 | 10,00 | 3 |

Vzhledem k tomu, že hodnota původního navýšení zásob je 10,00 LCY, převod se oceňuje při těchto nákladech, nikoli 12,00 LM.

## Opakované vyrovnání
Vzhledem ke způsobu výpočtu jednotkových nákladů zboží může nesprávné vyrovnání zboží vést ke zkresleným průměrným a jednotkovým nákladům. Následující scénáře mohou způsobit nesprávné vyrovnání zboží, které vyžadují vrácení vyrovnání zboží a opětovné použití položek zboží:

* Zapomněli jste vytvořit pevné vyrovnání.
* Udělali jste nesprávné pevné vyrovnání.
* Chcete zrušit vyrovnání vytvořené automaticky při zaúčtování podle metody ocenění zboží.
* Musíte vrátit zboží, na které již byl ručně uplatněn prodej, bez použití funkce **Získat účt. řádky pro stornování**, a proto musíte vyrovnání vrátit.

[!INCLUDE[prod_short](includes/prod_short.md)] nabízí funkci pro analýzu a opravu vyrovnání zboží. Tato práce se provádí na stránce **Sešit vyrovnání**.

## Viz také
[Detaily návrhu: Známé problémy vyrovnávání zboží](design-details-inventory-zero-level-open-item-ledger-entries.md)    
[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)    
[Detaily návrhu: Metody ocenění](design-details-costing-methods.md)    
[Detaily návrhu: Průměrné náklady](design-details-average-cost.md)     
[Detaily návrhu: Úprava nákladů](design-details-cost-adjustment.md)    
[Správa nákladů na zásoby](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]