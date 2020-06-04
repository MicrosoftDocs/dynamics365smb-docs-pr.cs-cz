---
title: Create Analysis Reports| Microsoft Docs
description: Describes how to create new analysis reports for sales, purchases, and inventory, and set up analysis templates.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2020
ms.author: sgroespe

---
# Vytvoření sestav analýzy
Manažeři prodeje musí pravidelně analyzovat obrat, hrubý zisk a další klíčové ukazatele výkonnosti prodeje. Kupující se více zajímají o dynamiku nákupních objemů, výkonnost dodavatelů a nákupní ceny. Zatímco vedoucí logistiky/zásob potřebují informace o obratu zásob, analýze pohybu zásob a statistice hodnoty zásob.

Analytické zprávy můžete použít k vytvoření přizpůsobených sestav založených na záznamech vašich zaúčtovaných transakcí, například prodeje, nákupy, převody a úpravy zásob. V přizpůsobitelné sestavě lze zdrojová data, která jsou odvozena z položek zboží (s přidruženými položkami hodnot), kombinovat, porovnávat a prezentovat smysluplnými způsoby definovanými uživatelem. V tomto smyslu je zpráva o analýze velmi podobná sestavě kontingenční tabulky v aplikaci Microsoft Excel.

Můžete si vytvořit svoji osobní sestavu, která se zaměřuje na vaše klíčové účty z hlediska celkového obratu v množství i množství prodaného, ​​hrubého zisku a procentuálního podílu hrubého zisku během aktuálního měsíce, a nechat porovnat tyto údaje s výsledky z předchozích měsíců nebo ve stejném měsíci loňského roku a vypočítat odchylky. To vše lze provést v jednom a stejném zobrazení, s možností přejít na příčinu identifikovaných problémových oblastí výběrem rozbalovacího tlačítka pro přístup k podrobnostem o úrovni jednotlivých transakcí.

Sestava analýzy se skládá z objektů, které chcete analyzovat, jako jsou zákazníci, skupiny zákazníků, prodejci a tak dále, reprezentované jako řádky a parametry analýzy, to znamená způsob, jakým chcete analyzovat objekt, reprezentovaný jako sloupce, jako jsou výpočty zisku, periodické porovnání prodejních částek a objemů nebo periodická porovnání skutečných údajů a údajů rozpočtů.

Kromě sestav analýzy můžete vytvářet a zobrazovat podobné informace v zobrazeních analýzy, které jsou založeny na dimenzích. Pro více informací navštivte [Analýza dat podle dimenzí](bi-how-analyze-data-dimension.md).

## Příklad
Můžete nastavit následující řádky:
- Počítače
- Zobrazí se
- Náhradní díly

Pak můžete nastavit sloupce, jako jsou tyto:

- Aktuální měsíc prodeje
- Prodej za minulý měsíc
- Prodej za minulý měsíc v procentech

## Nastavení rozvržení řádků a sloupců
Na stránce **Sestava analýzy** můžete zobrazit různá rozvržení řádků a sloupců podle toho, co jste nastavili. Řádky nebo šablony řádků nastavíte na stránce **Šablony řádků analýzy**. Na této stránce můžete definovat název sestavy a objekty, které chcete zobrazit v řádcích sestavy. Sloupce nastavíte na stránce **Šablony sloupců analýzy**. Na této stránce můžete definovat název šablony sloupce a parametry analýzy, které chcete v sestavě zobrazit jako sloupce. Na stránce **Šablony sloupců analýzy** představuje každý řádek sloupec v sestavě. Všimněte si, že řádky analýzy a sloupce analýzy jsou na sobě nezávislé.

Na základě řádků a sloupců, které jste nastavili, bude aplikace agregovat výsledek sestavy na stránce matice **Sestava analýzy**, například v tomto příkladu:

| |Aktuální měsíc prodeje|Prodej za poslední měsíc|Prodej za poslední měsíc %|
|-|-|-|-|
|Počítače| | | |
|Zobrazí se| | | |
|Náhradní díly| | | |
|Celkem| | | |

Můžete například nastavit jednu sadu řádků a několik sad rozvržení sloupců, aby se zobrazovaly měsíční a výroční zprávy.

## Nastavení šablon sloupců analýzy
Následující postup je založen na analytických pohledech na prodej. Kroky jsou podobné pro zobrazení nákupu a analýzy zásob.

V sestavě analýzy jsou parametry analýzy zobrazeny jako sloupce. Sloupce, které chcete zahrnout do sestavy analýzy, můžete definovat nastavením šablon sloupců analýzy.

Šablona obsahuje sadu řádků, z nichž každý představuje sloupec analýzy, který se zobrazí v sestavě analýzy. Chcete-li definovat sloupec, musíte řádku přiřadit typ kódu analýzy. Tento typ kódu analýzy určuje typ zdrojových dat v položkách zboží, na nichž bude analýza založena. Zdrojová data zahrnují cenu, částku prodeje nebo množství a související položky ocenění. Můžete nastavit libovolný počet šablon sloupců a pak je použít k vytvoření nových sestav analýzy.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony sloupců prodeje** a poté vyberte související odkaz.
2. Vyberte první prázdný řádek a podle potřeby vyplňte pole.
3. Vyberte akci **Sloupce**.
4. Na stránce **Sloupce analýzy** vyplňte pole a určete sloupce, které chcete zahrnout do sestavy analýzy.

   > [!NOTE]
   > Chcete-li definovat sloupec, musíte vyplnit pole **Kódy typu analýzy** pro všechny typy sloupců kromě **Vzorce**. Na stránce **Typy analýz** nastavte kódy typu analýzy.
Také v poli **Typ souvis.položky** vyberete-li **Položky zboží**, budou zkopírovány skutečné údaje z položky zboží. Pokud vyberete **Položky rozpočtu zboží**, zkopírují se částky rozpočtu z daného rozpočtu.
5. Stisknutím tlačítka **OK** uložte změny.

## Nastavení šablon řádků analýzy
Následující postup je založen na analytických sestavách pro prodej. Kroky jsou podobné pro sestavy analýzy nákupu a zásob.

V sestavě analýzy jsou objekty analýzy zobrazeny na řádcích. Řádky, které chcete zahrnout do sestavy analýzy, můžete definovat nastavením šablon řádků analýzy.

Šablona obsahuje sadu řádků představujících analytické řádky, které vidíte v analytické sestavě. Řádek může určit jedno nebo více zboží, odběratelů, dodavatelů nebo skupin. Rovněž můžete vytvořit vzorec v řádku a sčítat ostatní řádky. Můžete nastavit libovolný počet šablon řádků a poté je použít k vytvoření nových analytických sestav.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony řádků prodeje** a poté vyberte související odkaz.
2. Vyberte první prázdný řádek a podle potřeby vyplňte pole.
3. Vyberte akci **Řádky**.
4. Na stránce **Řádky analýzy** vytvořte řádky pro položky, zákazníky, dodavatele nebo prodejce, pro které chcete zobrazit čísla ve své analýze. Musíte vyplnit pole **Typ**, **Rozsah** a **Popis**.

> [!NOTE]
> Alternativně, pokud chcete pro každou položku, zákazníka atd. vytvořit mnoho samostatných řádků, můžete vybrat příslušnou možnost vložení a vyplnit všechna příslušná pole na řádku. V případě potřeby můžete řádky upravit ručně. Chcete-li vložit řádky, vyberte akci **Vložit zboží** nebo **Vložit skupiny zboží**.

## Vytvoření nové sestavy analýzy prodeje
Následující postup je založen na analytických sestavách pro prodej. Kroky jsou podobné pro sestavy analýzy nákupu a zásob.

Sestavy analýzy slouží k analýze dynamiky prodeje podle klíčových ukazatelů výkonnosti prodeje, které vyberete, například obrat u obratu prodeje v částkách a množstvích, příspěvkové marže nebo průběh skutečného prodeje vůči rozpočtu. Sestavu můžete také použít k analýze průměrných prodejních cen a k vyhodnocení prodejní výkonnosti.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sestavy analýzy prodeje** a poté vyberte související odkaz.
2. Na stránce **Sestava analýzy – prodej** vyberte akci **Nový**.
3. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vyberte akci **Upravit sestavu analýzy**.
5. Na stránce **Sestava analýzy prodeje** vyberte akci **Zobrazit matici**.

> [!NOTE]
> Vytváření kombinací šablon řádků a sloupců pro vytváření sestav a přiřazování jedinečných jmen je volitelné. Pokud tak učiníte, výběr názvu sestavy znamená, že nebudete muset vybrat šablony řádků a sloupců na stránce **Sestava analýzy prodeje**. Jakmile vyberete název sestavy, můžete samostatně změnit šablony řádků a sloupců a později znovu vybrat název sestavy a obnovit původní kombinaci.

## Viz také
[Business Intelligence](bi.md)  
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Položky zboží a účetní osnova](finance-general-ledger.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
