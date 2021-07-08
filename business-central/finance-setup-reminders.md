---
title: Set Up Reminder Terms and Levels
description: Learn how to set up Business Central so that you can send a reminder to a customer about a payment that is due and add charges, or fees to the payment because of the delay.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/01/2021
ms.author: edupont

---
# Nastavení podmínek a úrovní upomínek

Pomocí připomenutí můžete zákazníkům připomenout částky po splatnosti. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## Podmínky upomínky

Pokud mají zákazníci platby po splatnosti, musíte se rozhodnout, kdy a jak jim zaslat upomínku. Kromě toho můžete z jejich účtů odepsat úroky nebo poplatky. Můžete nastavit libovolný počet podmínek upomínky.

> [!NOTE]
> Chcete-li vypočítat úrok z prodlení s platbami po splatnosti, můžete tak učinit při vytváření upomínek. Pokud však chcete pouze vypočítat úroky a informovat o tom své zákazníky bez zasílání upomínky, měli byste použít [Penále](finance-setup-finance-charges.md). Další informace naleznete v tématu [Upomínky](receivables-collect-outstanding-balances.md#reminders) nebo [Finanční poplatky](receivables-collect-outstanding-balances.md#finance-charges).

### Nastavení podmínek upomínky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Podmínky upomínky** a vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Chcete-li použít více než jednu kombinaci podmínky upomínky, nastavte pro každou z nich vlastní kód.

## Úrovně upomínky

Pro každý kód podmínek upomínky můžete definovat neomezený počet úrovní upomínky. Při prvním vytvoření upomínky pro zákazníka se používá nastavení z úrovně 1. Při vystavení upomínky je číslo úrovně zaznamenáno v položkách upomínky, které jsou vytvořeny a propojeny s jednotlivými položkami zákazníka. Pokud je nutné zákazníkovi znovu připomenout, jsou všechny položky upomínky spojené s otevřenými položkami zákazníka zkontrolovány, aby bylo vyhledání nejvyššího čísla úrovně. Pro nové upomínky budou poté použity podmínky z čísla další úrovně.

Pokud vytvoříte více upomínek, než jste definovali úrovně, budou použity podmínky pro nejvyšší úroveň. Můžete vytvořit tolik upomínek, kolik povoluje pole **Maximální počet upomínek** v podmínkách upomínek.

### Nastavení úrovní upomínek

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Podmínky upomínky** a vyberte související odkaz.
2. Na stránce **Podmínky upomínky** vyberte řádek s podmínkami, pro které chcete nastavit úrovně, a poté vyberte akci **Úrovně**.
3. Podle potřeby vyplňte pole. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

   > [!TIP]
   > Nastavením polí **Vypočítat penále** určuje, zda se úrok zobrazí na upomínce při vystavení upomínky. Pole **Účtovat úrok** na stránce **Podmínky upomínky** určuje, zda musí být vypočtený úrok zaúčtován na zápočty a účty odběratelů.
   >
   > Chcete-li označit, že úroky mají být vypočteny, zvolte pole **Výpočet penále**.

   Volitelně pro každou úroveň upomínky zadejte další poplatky v CZK i v cizí měně. Pro každý kód můžete na stránce **Úrovně upomínky** definovat mnoho dalších poplatků v cizích měnách.

   Dodatečné poplatky lze vypočítat třemi různými způsoby, které jsou definovány hodnotou v poli **Typ výpočtu poplatku**.

   - **Pevný**

      Poplatky se počítají na základě hodnoty pole **Poplatek** na řádku pro samotnou úroveň upomínky.
   - **Jednoduchý dynamický**

      Poplatky se počítají na základě hodnot polí na příslušném řádku na stránce **Nastavení poplatku** pro tuto úroveň připomenutí.
   - **Kumulovaný dynamický**

      Poplatky se počítají na základě hodnot polí na kombinovaných řádcích na stránce **Nastavení poplatku** pro tuto úroveň připomenutí.

4. Vyberte akci **Měny**.
5. Na stránce **Měna pro úroveň upomínky**, definujte pro každý kód úrovně upomínky a odpovídající číslo upomínky kód měny a další poplatek.

   > [!NOTE]  
   > Když vytváříte upomínky v cizí měně, pak budou vytvoření připomenutí použity podmínky v cizí měně, které zde nastavíte. Pokud nejsou nastaveny žádné podmínky upomínky v cizí měně, budou použity podmínky upomínky v CZK, které jsou nastaveny na stránce **Úrovně upomínky** a poté převedeny na příslušnou měnu.

   Pro každou úroveň upomínky můžete zadat text, který bude vytištěn před (**Text na začátku**) nebo (**Text na konci**) u položek na upomínce.

6. Zvolte akce **Text na začátku** nebo **Text na konci** a vyplňte stránku **Text upomínky**
7. Chcete-li automaticky vložit související hodnoty do výsledného textu upomínky, zadejte do pole **Text** následující symboly .

   | Zástupný symbol | Hodnota |
   |-----------------|-----------|  
   | %1 | Obsah pole **Datum dokladu** v záhlaví upomínky |
   | %2 | Obsah pole **Datum splatnosti** v záhlaví upomínku |
   | %3 | Obsah pole **Úroková sazba** v souvisejících podmínkách penále |
   | %4 | Obsah pole **Zbývající částka** v záhlaví upomínky |
   | %5 | Obsah pole **Částka úroku** v záhlaví upomínek |
   | %6 | Obsah pole **Poplatek** hlavičce upomínky |
   | %7 | Celková částka upomínky |
   | %8 | Obsah pole **Úroveň připomenutí** v záhlaví upomínky |
   | %9 | Obsah pole **Kód měny** v záhlaví upomínky |
   | %10 | Obsah pole **Zúčtovací datum** v hlavičce upomínky |
   | %11 | Název společnosti |
   | %12 | Obsah pole **Poplatek řádku** v hlavičce upomínky |

   Například pokud napíšete **Dlužíte % 9 %7 z důvodu %2.**, výsledná upomínka bude obsahovat následující text: **Dlužíte 1 200,50 USD splatného 02-02- 2014**.

   > [!NOTE]
   > Datum splatnosti se počítá podle zadaného vzorce data. Pro více informací navštivte [Použití vzorců dat](ui-enter-date-ranges.md#using-date-formulas).

Po nastavení podmínek upomínky s dalšími úrovněmi a textem zadejte jeden z kódů na každé kartě zákazníka. Pro více informací navštivte <x3/>Evidence nového zákazníka<x4/>.

## Viz také

[Inkaso nevyrovnaných zůstatků](receivables-collect-outstanding-balances.md)  
[Nastavení podmínek penále](finance-setup-finance-charges.md)  
[Nastavení financí](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]