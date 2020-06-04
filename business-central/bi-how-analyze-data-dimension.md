---
title: Analyze Data by Dimensions| Microsoft Docs
description: Describes how to analyze various business data by dimensions.
services: project-madeira
documentationcenter: ''
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
# Analýza dat podle dimenzí
Ve finanční analýze jsou dimenze data, která můžete přidat do položky jako druh značky. Tato data se používají k seskupení položek s podobnými charakteristikami, jako jsou zákazníci, oblasti, produkty a prodejce, a k snadnému načtení těchto skupin pro analýzu. Dimenze lze použít pro položky v denících, dokladech a rozpočtech. Termín dimenze popisuje, jak probíhá analýza. Například dvourozměrnou analýzou by byl prodej na oblast. Pokud však při vytváření záznamu použijete více než dvě dimenze, můžete provést složitější analýzu, jako je prodej za prodejní kampaň na skupinu zákazníků podle oblasti. Pro více informací navštivte [Práce s dimenzemi](finance-dimensions.md).

Analýzou dat podle dimenzí získáte lepší přehled o své firmě, takže můžete vyhodnotit informace, například o tom, jak dobře vaše firma funguje, kde prosperuje a kde ne, a kde by mělo být přiděleno více zdrojů.

> [!TIP]
> Rychlý způsob, jak analyzovat transakční data podle dimenzí, je filtrovat součty v tabulce účtů a záznamů na všech stránkách **Položek** podle dimenzí. Vyhledejte akci **Nastavit filtr dimenze**.

## Nastavení zobrazení analýzy
Analýza podle dimenzí zobrazuje vybranou kombinaci dimenzí. Můžete uložit a načíst každou analýzu, kterou jste nastavili. Informace pro nastavení analýzy jsou uloženy na kartě **Zobrazení analýzy** pro zjednodušení budoucí analýzy.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zobrazení analýzy** a poté vyberte související odkaz.
2. Na stránce **Přehled zobrazení analýzy** vyberte akci **Nový**.
3. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Chcete-li přidat další kódy dimenzí kromě čtyř na záložce **Dimenze**, vyberte akci **Filtr**, vyplňte pole a poté vyberte tlačítko **OK**.
5. Chcete-li zobrazení aktualizovat, vyberte akci **Upravit**.

## Analýza podle dimenzí
Matici **Analýza dle dimenzí** můžete použít k zobrazení částek v hlavní knize pomocí pohledů na analýzu, které jste již nastavili. Vyplníte stránku **Analýza dle dimenzí**, abyste definovali, co se zobrazí v matici, a pak zvolíte **Zobrazit matici**, abyste matici zobrazili.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zobrazení analýzy** a poté vyberte související odkaz.
2. Vyberte příslušné zobrazení analýzy a poté vyberte akci **Analýza dle dimenzí**.
3. Na stránce **Analýza dle dimenzí** vyplňte pole a definujte, která data jsou zobrazena a jak.
4. Vyberte akci **Zobrazit matici** a otevřete příslušnou stránku matice pro definované zobrazení analýzy.
5. Chcete-li zobrazit specifikaci částky zobrazené na stránce matice, zvolte částku, kterou chcete přejít k podrobnostem.

- Sloupce vlevo obsahují informace založené na tom, co jste vybrali v poli **Zobrazit jako řádky** v záhlaví.
- Sloupce vpravo obsahují informace na základě toho, co jste vybrali v poli **Zobrazit jako sloupce** v záhlaví.

> [!IMPORTANT]
> Nelze vybrat kratší období, než je období určené pro kompresi na kartě **Zobrazení analýzy**. Příkazy **Další sada** a **Předchozí sada** jsou neaktivní, pokud jste vybrali **Období** v poli **Zobrazit jako řádky** nebo **Zobrazit jako sloupce**.

> [!NOTE]
> Sestava **Dimenze – detaily** můžete použít k zobrazení podrobné klasifikace toho, jak byly použity dimenze u položek za vybrané období. Pomocí sestavy **Dimenze – celkem** můžete zobrazit pouze celkové částky.

> [!TIP]
> Zobrazení můžete také změnit změnou obsahu pole **Zobrazit jako řádky** a **Zobrazit jako sloupce**. Chcete-li změnit nastavení zobrazení, vyberte akci **Výměna řádků a sloupců**.

## Aktualizace zobrazení analýzy
Částky, které se zobrazují na stránce **Analýza dle dimenzí**, vám poskytnou představu o stavu společnosti v době poslední aktualizace. Chcete-li získat obrázek o aktuálním stavu, musíte aktualizovat zobrazení analýzy spuštěním funkce aktualizace.

Následující postup slouží k aktualizaci zobrazení analýzy ze stránky **Analýza dle dimenzí**. Kroky jsou podobné na stránkách **Karta pohledu analýzy** a **Přehled zobrazení analýzy**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zobrazení analýzy** a poté vyberte související odkaz.
2. Vyberte příslušné zobrazení analýzy a poté vyberte akci **Analýza dle dimenzí**.
2. Na stránce **Analýza dle dimenzí** vyberte pole **Kód zobrazení analýzy**.
3. Vyberte řádek s příslušným zobrazením analýzy.
4. Na stránce **Zobrazení analýz** vyberte zobrazení analýzy a poté vyberte akci **Upravit**.

> [!TIP]
> Pokud zaškrtnete políčko **Aktualizace při účtování** na kartě s analýzou zobrazení, pohled se automaticky aktualizuje, jakmile je zaúčtována příslušná transakce.

> [!NOTE]
> Chcete-li aktualizovat některá nebo všechna zobrazení analýzy současně, musíte použít dávkovou úlohu **Aktualizace zobrazení analýzy**.

## Viz Související školení na [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index)

## Viz také
[Business Intelligence](bi.md)  
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Věcné položky a účetní osnova](finance-general-ledger.md)  
[Práce s dimenzemi](finance-dimensions.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
