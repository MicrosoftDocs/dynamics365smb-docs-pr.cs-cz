---
    title: Cash Flow Forecasts by Using Account Schedules
    description: This walkthrough describes how you can use account schedules to make cash flow forecasts in Business Central.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 06/24/2021
    ms.author: edupont

---
# Návod: Tvorba prognóz cashflow pomocí účetních schémat

Tento návod popisuje, jak můžete pomocí účetních schémat provádět prognózy cashflow. Účetní schémata provádějí výpočty, které nelze provést přímo v grafu účtů cashflow. V účetních schématech můžete nastavit mezisoučty pro příjemky a výdaje cashflow. Tyto mezisoučty mohou být zahrnuty do nových součtů, které pak lze použít při vytváření prognóz cashflow.

## O tomto návodu

Tento návod popisuje následující úkoly:

- Nastavení nového názvu účetního schématu cashflow.
- Nastavení řádků účetního schématu.
- Nastavení nového rozvržení sloupce.
- Přiřazení rozvržení sloupce k účetnímu schématu.
- Zobrazení a tisk prognózy cashflow.

### Předpoklady

K dokončení tohoto návodu budete potřebovat:

- [!INCLUDE[prod_short](includes/prod_short.md)]
- Řádky listu cashflow jsou registrovány.

## Role

Tento návod ukazuje úkoly, které jsou prováděny následujícími uživatelskými rolemi:

- Řadič

## Příběh

Ken je řadič ve společnosti CRONUS, který provádí měsíční prognózy cashflow. Do prognózy zahrne finance, prodej, nákup a dlouhodobý majetek a poté je předá finanční ředitelce Sarah, aby získala přehled bchodu.

## Nastavení nového názvu účetního schématu

Účetní schéma se skládá z názvu účetního schématu cashflow s řadou řádků a rozložením sloupců.

### Nastavení nového názvu účetního schématu

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní schémata** a poté vyberte související odkaz.
2. Na stránce **Názvy účetních schémat** vyberte **Nový** a vytvořte nový název účetního schématu cashflow.
3. Do pole **Název** zadejte **Prognóza**.
4. Do pole **Popis** zadejte **Prognóza cashflow**.
5. Pole **Výchozí rozložení sloupce** a **Název pohledu analýzy** nechte prázdná.

## Nastavení řádků účetního schématu

Po nastavení názvu účetního schématu Ken definuje každý řádek, který se objeví v účetním schématu cashflow. Ken definuje řádky, které lze zobrazit v sestavách kromě řádků, které jsou pouze pro účely výpočtu.

### Nastavení řádků účetního schématu

1. Na stránce **Názvy účetních schémat** vyberte nový název **Prognózy** účetního schématu, který jste vytvořili, a poté vyberte akci **Upravit účetní schéma**.
2. Na stránce **Účetní schéma** zadejte jednotlivé řádky, jak je znázorněno v následující tabulce.

   > [!TIP]  
   > Pomocí funkce **Vložit účty CF** můžete rychle označit účty cashflow z tabulky účtů peněžních toků a zkopírovat je do řádků účetního schématu.

   | Číslo řady | Popis | Typ součtu | Součet | Typ řady | Typ částky | Zobrazení |
   |---------|--------------------------|--------------------------|----------|------------|-------------|------|
   | R10 | Otevřené prodejní objednávky | Položka účtů cashflow | 20 | Pohyb | Netto částka | Ano |
   | R10 | Vypůjčení | Položka účtů cashflow | 30 | Pohyb | Netto částka | Ano |
   | R10 | Finanční majetek | Položka účtů cashflow | 40 | Pohyb | Netto částka | Ano |
   | R10 | Vyřazení dlouhodobého majetku | Položka účtů cashflow | 50 | Pohyb | Netto částka | Ano |
   | R10 | Soukromé investice | Položka účtů cashflow | 60 | Pohyb | Netto částka | Ano |
   | R10 | Příjmy různé | Položka účtů cashflow | 70 | Pohyb | Netto částka | Ano |
   | R10 | Otevřené servisní zakázky | Položka účtů cashflow | 80 | Pohyb | Netto částka | Ano |
   | R20 | Celkové příjemky hotovosti | Vzorec | R10 | Pohyb | Netto částka | Ano |
   | R20 | Celkové příjemky hotovosti | Vzorec | R10 | Pohyb | Netto částka | Ano |
   | R30 | Závazky | Položka účtů cashflow | 1010 | Pohyb | Netto částka | Ano |
   | R30 | Otevřené nákupní objednávky | Položka účtů cashflow | 1020 | Pohyb | Netto částka | Ano |
   | R30 | Osobní náklady | Položka účtů cashflow | 1030 | Pohyb | Netto částka | Ano |
   | R30 | Provozní náklady | Položka účtů cashflow | 1040 | Pohyb | Netto částka | Ano |
   | R30 | Finanční náklady | Položka účtů cashflow | 1050 | Pohyb | Netto částka | Ano |
   | R30 | Investice | Položka účtů cashflow | 1070 | Pohyb | Netto částka | Ano |
   | R30 | Osobní spotřeba | Položka účtů cashflow | 1090 | Pohyb | Netto částka | Ano |
   | R30 | Splatné DPH | Položka účtů cashflow | 1100 | Pohyb | Netto částka | Ano |
   | R30 | Jiné výdaje | Položka účtů cashflow | 1110 | Pohyb | Netto částka | Ano |
   | R40 | Celkové výdaje hotovosti | Vzorec | R30 | Pohyb | Netto částka | Ano |
   | R50 | Přebytek | Vzorec | R20+R40 | Pohyb | Netto částka | Ano |
   | R60 | Fondy cashflow | Položka účtů cashflow | 2100 | Pohyb | Netto částka | Ano |
   | R70 | Celkové cashflow | Vzorec | R50+R60 | Pohyb | Netto částka | Ano |

   > [!NOTE]
   > Číslo řádku R10 se používá k zachycení součtu pohledávek na účtu. Číslo řádku R20 se používá k výpočtu součtu všech peněžních příjmů. Řádek číslo R30 se používá k zachycení součtu účtů za závazky. Číslo řádku R40 se používá k výpočtu součtu všech výdajů hotovosti. Číslo řádku R50 se používá k zachycení součtu přebytku hotovosti. Číslo řádku R60 se používá k zachycení penězných fondů. Číslo řádku R70 se používá k výpočtu předpokládaného cashflow.

## Nastavení nového rozvržení sloupce

Než bude moci Ken vytisknout prognózu cashflow, musí vytvořit rozložení sloupce pro číselné informace. Ve sloupcích definuje informace, které chce použít z řádků.

- První sloupec má číslo *C10* s názvem **Částka** a obsahuje pohyb.
- Druhý sloupec má číslo *C20* s názvem **Saldo do data** a obsahuje transakce za dané období.
- Třetí sloupec má číslo *C30* s názvem **Celý rok** a obsahuje pohyb zůstatků za celý fiskální rok.
- Nakonec přiřadí rozvržení sloupce jako výchozí rozvržení sloupce pro účetní schému **Prognóza**.

## Nastavení nového rozvržení sloupce

1. V okně **Názvy účetních schémat** vyberte nový název účetního schématu **Prognóza**, který jste vytvořili. Na kartě **Domů** ve skupině **Proces** zvolte **Nastavit rozložení sloupců**.

   > [!TIP]
   > Stejnou akci najdete na stránce **Účetní schéma**, pokud tam stále upravujete plán účtu **Prognóza**.

2. Vytvořte nové rozložení sloupce s názvem **Cashflow**.

3. Zvolte tlačítko OK.

4. Zadejte každý řádek přesně tak, jak je znázorněno v následující tabulce.

   | Číslo sloupce | Hlavička sloupce | Typ sloupce | Typ souvis.položky | Typ částky | Zobrazení |
   |----------|-------------|-----------|-----------------|-----------|----|
   | C10 | Částka | Pohyb | Položky | Netto částka | Vždy |
   | C20 | Částka do data | Saldo do data | Položky | Netto částka | Vždy |
   | C30 | Celý fiskální rok | Celý fiskální rok | Položky | Netto částka | Vždy |

## Přiřazení rozložení sloupce k názvu účetního schématu

Ken je nyní připraven přiřadit rozložení sloupce k názvu účetního schématu.

### Přiřazení rozložení sloupce k názvu účetního schématu

1. Na stránce **Účetní schéma** kde pracujete s účetním schématem **Prognóza** zvolte akci **Nastavit rozložení sloupců**.
2. V poli **Název rozložení sloupce** vyberte rozložení sloupce **Cashflow**, které chcete přiřadit jako výchozí rozložení sloupce.

### Zobrazení a tisk prognózy cashflow

1. Na stránce **Názvy účetních schémat** vyberte akci **Náhled** a zobrazte prognózu cashflow.
2. Na stránce **Náhled  účetního schéma** můžete vybrat částku a poté zobrazit položky prognózy cashflow, které tvoří částku. Kromě toho můžete zobrazit vzorec, který se používá k výpočtu částky. Můžete také filtrovat částky podle data a dimenze.
3. Zvolte akci **Tisk** chcete-li prognózu cashflow vytisknout.

## Viz také

[Práce s účetními schématy](bi-how-work-account-schedule.md)    
[Analýza peněžních toků ve vaší společnosti](finance-analyze-cash-flow.md)    
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]