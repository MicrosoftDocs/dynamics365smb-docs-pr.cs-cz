---
title: Process Sales Opportunities in Sales Cycles| Microsoft Docs
description: You can view, close, or delete sales opportunities, and you can also create quotes and sales orders for opportunities, and move an opportunity through the stages of a sales cycle.
services: project-madeira
documentationcenter: ''
author: jswymer

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2020
ms.author: jswymer

---
# Zpracování prodejních příležitostí
Po vytvoření příležitosti existuje několik funkcí pro správu příležitosti a její přesunutí k dokončení.

## Zobrazení příležitostí
Existující prodejní příležitosti jsou k dispozici na stránce **Přehled příležitostí**. Existují různé způsoby přístupu na tuto stránku pro zpracování prodejních příležitostí:

| Zobrazení příležitosti pro | Pak |
| --- | --- |
| Všichni prodejci a kontakty | Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Přehled příležitostí** a poté vyberte související odkaz. |
| Konkrétní prodejce | Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejci** a poté vyberte související odkaz. Vyberte prodejce, zvolte akci **Příležitosti** a poté vyberte akci **Přehled**. |
| Konkrétní kontakt | Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kontakty** a poté vyberte související odkaz. Vyberte kontakt ze seznamu a poté vyberte akci **Příležitosti**. |

Každá z těchto úloh otevře stránku **Přehled příležitostí**.

## Uzavření příležitostí
Příležitosti můžete uzavřít, až jednání skončí. Při zavírání příležitosti můžete určit, zda byla vyhrána nebo ztracena, a také můžete určit důvody pro její uzavření. Chcete-li určit důvod, musíte nastavit kódy uzavřených příležitostí.

1. Na stránce **Přehled příležitostí** vyberte příležitost a vyberte akci **Zavřít**. Otevře se stránka **Uzavřít příležitost**.
2. Vyplňte příslušná pole a vyberte tlačítko **OK**.

   Pole **Kód uzavření příležitosti** a **Datum uzavření** jsou povinná pole a před výběrem tlačítka **OK** musí být vyplněna.

   V poli **Kód uzavření příležitosti** můžete vybrat jeden z existujících kódů blízkých příležitostí nebo přidat nový kód. Chcete-li přidat nový kód, z rozevíracího seznamu vyberte **Výběr z úplného seznamu** a poté vyberte **Nový**. Na nový prázdný řádek vyplňte pole **Kód**, **Typ** a **Popis** a poté vyberte tlačítko **OK**.

## Vytvoření nabídek pro příležitosti
Můžete vytvořit prodejní nabídky pro kontakty, které nejsou zaznamenány jako zákazníci.

1. Na stránce **Přehled příležitostí** vyberte příležitost a poté vyberte akci **Přiřadit prod.nabídku**. Otevře se stránka **Prodejní nabídka**.
2. Vyplňte příslušná pole.

## Vytvoření prodejních objednávek pro příležitosti
Prodejní objednávky můžete provádět z prodejních nabídek, které jste vytvořili pro své příležitosti. Před vytvořením prodejních objednávek pro kontakty je nutné vytvořit kontakt jako zákazníka. Pro více informací navštivte [Vytvoření kontaktů](marketing-create-contact-companies.md).

1. Na stránce **Přehled příležitostí** vyhledejte příležitost, pro kterou jste vytvořili prodejní nabídku.
2. Vyberte akci **Přiřadit prod.nabídku**. Otevře se stránka **Prodejní nabídka**, která zobrazuje prodejní nabídku, kterou jste příležitosti přiřadili.
3. Vyplňte další pole a poté vyberte akci **Vytvořit objednávku**.

Při zpracování prodejních příležitostí může být nutné vytvořit nabídku pro kontakt, se kterým je příležitost propojena.

## Odstranění příležitostí
Příležitosti můžete odstranit například po uzavření dohody. Můžete však odstranit pouze uzavřené příležitosti. Uzavřené příležitosti lze odstranit dvěma způsoby. Jednotlivé uzavřené příležitosti můžete odstranit ze stránky **Přehled příležitostí** nebo můžete spustit dávkovou úlohu **Odstranit uzavřené příležitosti** a odstranit více příležitostí na základě zadaných kritérií.

Chcete-li odstranit uzavřené příležitosti ze stránky **Přehled příležitostí**, vyberte příležitost a zvolte akci **Odstranit**.

Chcete-li odstranit uzavřené příležitosti pomocí dávkové úlohy **Odstranit uzavřené příležitosti**, postupujte takto:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Odstranit příležitosti** a poté vyberte související odkaz.
2. V sekci **Příležitost** nastavte filtry, které určují uzavřené příležitosti k odstranění.
3. Vyberte tlačítko **OK**.

Po odstranění příležitosti je příležitost odebrána ze stránky **Přehled příležitostí**.

## Přesunutí příležitosti ve fázích prodejního cyklu
Pokud příležitost následuje po prodejním cyklu, můžete ji přesunout dopředu nebo dozadu v různých fázích, například přesunout další nebo předchozí fázi a dokonce fázi přeskočit.

1. Na stránce **Přehled příležitostí** vyberte akci **Aktualizace**.  Otevře se stránka **Aktualizovat příležitost**.
2. Pomocí pole **Typ akce** přesuňte příležitost ve fázích prodejního cyklu:
   * **Další** přesune příležitost o jednu fázi dopředu.
   * **Přeskočit** přesune příležitost dopředu o jednu nebo více fází prodejního cyklu, které zadáte v poli **Prezentace**. Přeskočit lze pouze fáze, které byly nastaveny tak, aby umožňovaly přeskočení.
   * **Předchozí** přesune příležitost zpět o jednu fázi.
   * **Skočit** přesune příležitost zpět o jednu nebo několik fází prodejního cyklu, které zadáte v poli **Prezentace**.
   * **Aktualizovat** umožňuje měnit informace (například upravit hodnocení jejich šance na úspěch a odhadované hodnoty) bez přechodu do jiné fáze.
3. Podle potřeby vyplňte ostatní pole a pak zvolte tlačítko **OK**.

## Viz také
[Prodej](sales-manage-sales.md)  
[Vytváření a správa kontaktů](marketing-contacts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
