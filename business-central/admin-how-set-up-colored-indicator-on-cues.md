---
    title: Specify Colored Indicators to Customize Visual Signals About a Cue's Activity for the Company or Individual Users | Microsoft Docs
    description: As an administrator, you can set up Cues that appear on the users' Role Centers to include an indicator that changes color based on the data values in the Cues.
    author: jswymer

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: jswymer

---
# Nastavení barevného indikátoru na hromádkách pro společnost, nebo individuálního uživatele
Jako správce můžete nastavit hromádky, které se zobrazují v Centrech rolí uživatelů, aby zahrnovaly indikátor, který mění barvu na základě datových hodnot v hromádkách.

Indikátor se zobrazí jako barevný pruh podél horního okraje dlaždice hromádky. Poskytuje vizuální signál o stavu aktivity hromádky, což může naznačovat příznivé nebo nepříznivé podmínky, které vyzve uživatele k akci. Pokud například hromádka zobrazí průběžné prodejní faktury, můžete nastavit, aby se indikátor zobrazoval zeleně (příznivě), když je celkový počet probíhajících prodejních faktur nižší než 10, a zobrazí se červeně (nepříznivě), pokud je součet větší než 20.

Na stránce **Nastavení hromádky** nastavíte indikátory pro všechny hromádky, které jsou dostupné v databázi společnosti. Indikátory můžete nastavit tak, aby se vztahovaly na všechny uživatele ve společnosti nebo pouze na jednotlivé uživatele. Nastavení indikátoru na stránce **Nastavení hromádky** fungují jako výchozí nastavení. Pokud je stránka **Nastavení hromádky** uživatelům k dispozici, mohou přizpůsobit nastavení indikátorů, které definujete na stránce **Nastavení hromádky**.

Chcete-li nastavit označení, určete až dvě prahové hodnoty, které definují tři rozsahy datových hodnot (dolní, střední a vysoká), na které můžete použít jinou barvu (nebo styl).

### Nastavení barevných označení v Hromádkách
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení hromádky** a poté vyberte související odkaz.

   Zobrazí se stránka **Nastavení hromádky**. Na stránce jsou uvedené označení, které jsou aktuálně nastaveny v Hromádce. Indikátory, které se vztahují na všechny uživatele ve společnosti, mají pole **Uživatelské jméno** prázdné. Indikátory, které se vztahují na konkrétního uživatele, zahrnují jméno uživatele v poli **Uživatelské jméno**.

   > [!NOTE]
   > Pokud nastavíte celofiremní indikátor a uživatel jej později upraví, objeví se v seznamu pro tohoto uživatele samostatný záznam pro tento indikátor.

2. Zvolte akci **Upravit přehled**.
3. Chcete-li nastavit indikátor pro hromádku, která není uvedena na stránce, vyberte akci **Nový** a vyplňte pole podle následujícího popisu. Pokud chcete upravit existující indikátor, přejděte k dalšímu kroku.

   | Pole | Popis |
   |---------|---------------|  
   | **Název uživatele** | Chcete-li nastavit indikátor pro všechny uživatele, ponechte toto pole prázdné.<br /><br /> Pokud chcete nastavit indikátor pro konkrétního uživatele, nastavte toto pole na název uživatele. |
   | **Číslo tabulky** | Určuje ID objektu tabulky, který obsahuje hromádku. K nalezení tabulky použijte rozevírací seznam. Rozevírací seznam obsahuje všechny tabulky hromádky v databázi společnosti<br /><br /> Pole **Název tabulky** pole bude automaticky doplněno podle vašeho výběru. |
   | **Číslo pole** | Určuje ID hromádky, na které chcete nastavit indikátor. Pomocí rozevíracího seznamu najděte hromádku, kterou chcete. **Poznámka:**  ID hromádky odpovídá číslu pole, které je hromádce přiřazeno v tabulce. <br /><br /> Pole **Název pole** je automaticky vyplněno na základě vaší volby.  |

4. Chcete-li nastavit indikátor hromádky, nastavte pole podle popisu v následující tabulce.

   | Pole | Popis |
   |---------|---------------|  
   | **LowStyle** | Určuje barvu indikátoru, když je hodnota hromádky pod hodnotou pole  **Práh 1**. |
   | **LowThreshold** | Určuje hodnotu, při které indikátor změní barvu určenou v poli **Middle Range Style**. |
   | **MiddleStyle** | Určuje barvu indikátoru, když je hodnota hromádky větší nebo rovná hodnotě pole **Práh 1**, ale menší nebo rovna hodnotě pole **Práh 2**. |
   | **HighThreshold** | Určuje hodnotu, nad kterou se indikátor změní na barvu určenou v poli **High Range Style**. |
   | **HighStyle** | Určuje barvu, která se má použít, když je hodnota hromádky vyšší než hodnota pole **Práh 2**. |

   Následující tabulka uvádí barvy, které odpovídají možnostem polí **LowStyle**, **MiddleStyle**, a **HighStyle**.

   | Možnost | Barva |
   |----------|---------|  
   | **None** | Žádná barva (stejná barva jako dlaždice hromádky) |
   | **Favorable** | Zelená |
   | **Unfavorable** | Červená |
   | **Ambiguous** | Žlutá |
   | **Subordinate** | Šedá |

## Viz také
