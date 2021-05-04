---
    title: Design Details - Item Tracking Availability | Microsoft Docs
    description: The Item Tracking Lines and Item Tracking Summary pages provide dynamic availability information for serial or lot numbers. The purpose of this is to increase transparency for users on outbound documents, such as sales orders, by showing them which serial numbers or how many units of a lot number are currently assigned on other open documents.
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
# Detaily návrhu: Dostupnost sledování zboží
Stránky **Řádky sledování zboží** a **Souhrn sledování zboží** poskytují dynamické informace o dostupnosti sériových čísel nebo čísel šarží. Účelem je zvýšit transparentnost pro uživatele na odchozích dokladech, jako jsou prodejní objednávky, tím, že jim ukážete, která sériová čísla nebo kolik jednotek čísel šarže je aktuálně přiřazeno na jiných otevřených dokladech. To snižuje nejistotu způsobenou dvojitým přidělením a dává zpracovatelům objednávek důvěru, že sledování zboží a data, která slibují na nezaúčtovaných prodejních objednávkách, mohou být splněny. Pro více informací navštivte [Detaily návrhu: Stránka Řádky sledování zboží](design-details-item-tracking-lines-window.md).

Když otevřete stránku **Řádky sledování zboží**, data dostupnosti se načtou z tabulky **Položky zboží** a tabulky **Položky rezervace** bez filtru data. Pokud zbolíte pole **Séeriové číslo** nebo **Číslo šarže**, otevře se stránka **Souhrn sledování zboží** a zobrazí souhrn informace o sledování položky v tabulce **Položka rezervace**. Souhrn obsahuje následující informace o každém sériovém čísle nebo čísle šarže na řádku sledování zboží:

| Pole | Popis |
|---------------------------------|---------------------------------------|  
| **Celkové množství** | Celkové množství sériových čísel nebo čísla šarže, které jsou aktuálně na skladě. |
| **Celkové požadované množství** | Celkové množství sériových čísel nebo čísla šarže, které jsou aktuálně požadovány ve všech dokladech. |
| **Aktuální množství ke zpracování** | Množství, které je zadáno v aktuální instanci stránky **Řádky sledování zboží**, ale ještě nejsou zapsány do databáze |
| **Celkové množství k dispozici** | Množství sériových čísel nebo čísel šarží, které má uživatel k dispozici.<br /><br /> Toto množství se počítá z ostatních polí na stránce následujícím způsobem:<br /><br /> Celkové množství – (Celkové požadované množství + Aktuální množství ke zpracování). |

> [!NOTE]  
> Informace také můžete zobrazit v předchozí tabulce pomocí funkce **Vybrat položky** na stránce **Řádky sledování zboží**.

Pro zachování výkonu databáze, jsou data dostupnosti načtena z databáze pouze jednou, když otevřete stránku **Řádky sledování zboží** a když použijte funkci **Aktualizovat dostupnost**.

## Vzorec výpočtu
Jak je popsáno v předchozí tabulce, dostupnost daného sériového čísla nebo čísla šarže se počítá následujícím způsobem.

Celkové množství k dispozici = Množství ve skladu  – (všechny požadavky + množství dosud nezapsáno v databázi)

> [!IMPORTANT]  
> Tento vzorec znamená, že výpočet dostupnosti sériového čísla nebo čísla šarže zohledňuje pouze zásoby a ignoruje předpokládané příjmy.. Proto dodávka, která ještě není zaúčtována do zásob, nemá vliv na dostupnost sledování zboží, na rozdíl od běžné dostupnosti zboží, kde jsou zahrnuty předpokládané příjmy.

## Viz také
[Detaily návrhu: Sledování zboží](design-details-item-tracking.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]