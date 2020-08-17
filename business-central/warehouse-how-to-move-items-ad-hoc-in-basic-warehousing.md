---
title: How to Move Items Ad Hoc in Basic Warehouse Configurations | Microsoft Docs
description: You may occasionally need to move items between internal bins, not receiving or shipping bins, without a specific demand from a source document. You may perform these ad hoc movements, for example, to reorganize the warehouse, to bring items to an inspection area, or to move additional items to and from a production area without a system relation to the production order source document.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 04/01/2020
ms.author: sgroespe

---
# Ad Hoc přesun zboží v základních konfiguracích skladu
Někdy může být nutné přesunout zboží mezi interními přihrádky, nikoli přijímacími nebo expedičními přihrádky, bez konkrétní poptávky z původního dokladu. Tyto ad hoc pohyby můžete provádět například za účelem reorganizace skladu, převážení zboží do kontrolní oblasti nebo přesunutí dalšího zboží do a z výrobní oblasti bez systémového vztahu k původnímu dokladu výrobní zakázky.

V základních konfiguracích skladu, tedy lokacích, která používají nastavení pole **Přihrádka nutná** a případně pole **Vyžadovat vyskladnění** a **Vyžadovat zaskladnění**, můžete zapsat ad hoc pohyby bez původních dokladů následujícími způsoby:

- Pomocí stránky **Interní přesun**.
- Pomocí stránky **Deník přeřazení zboží**.

> [!NOTE]
> V pokročilých konfiguracích skladu, tj. lokacích, která používají nastavení pole **Řízené zaskladnění/vyskladnění**, použijete stránku **Sešit přesunu**, **Interní  Vyskladnění** nebo **Interní  zaskladnění** pro ad hoc přesun zboží mezi přihrádky.

## Přesun zboží pomocí interního pohybu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Interní přesun** a poté vyberte související odkaz.
2. Na záložce **Obecné** vyplňte pole **Číslo**, a to buď opuštěním pole, nebo výběrem tlačítka **AssistEdit**, které vyberete z číselné řady.
3. Do pole **Kód lokace** zadejte místo, kde se přesun provádí.

   Pokud je lokace nastavena jako výchozí lokace pro zaměstnanece skladu, kód lokace se vloží automaticky.
4. Do pole **Do kódu přihrádky** zadejte kód přihrádky, do které chcete zboží přesunout. Pro výrobní účely se může jednat například o kód přihrádky dílny, jak je definováno na kartě lokace nebo pracovním centru.
5. Do pole **Datum vyřízení** zadejte datum, do kterého musí být přesun dokončen.
6. Na záložce **Řádky** vyberte pole **Číslo zboží** a otevřete stránku **Přehled obsahů přihrádek** a pak vyberte zboží, které se má přesunout, na základě jeho dostupnosti v přihrádkách. Alternativně vyberte akci **Načíst obsah přihrádky** abyste vyplnili řádky interního přesunu na základě filtrů. Pro více informací navštivte nápovědu k akci **Načíst obsah přihrádky**.

   Pokud jste zboží vybrali, pole **Z kódu přihrádky** se automaticky vyplní podle vybraného obsahu přihrádky, ale můžete jej změnit na jakoukoli jinou přihrádku, kde je zboží k dispozici.

   > [!NOTE]
   > Protože jsou propojeny pole **Číslo zboží** a **Z kódu přihrádky**, mohou se jejich hodnoty při úpravách některého z polí vzájemně měnit.

   Pole **Do kódu přihrádky** je vyplněno hodnotou, kterou jste zadali v záhlaví, ale můžete ji na řádku změnit na jakýkoli jiný kód přihrádky, který není blokován nebo vyhrazen pro zvláštní účely. Pro více informací o vyhrazených přihrádkách navštivte Vyhrazeno.
7. Pokud jste definovali, ze kterých přihrádek chcete zboží přesunout, zadejte množství, které se má přesunout, do pole **Množství**.

   > [!NOTE]
   > Množství musí být k dispozici v Z kódu přihrádky.

8. Až budete připraveni zpracovat interní přesun, zvolte akci **Vytvořit přesun zásob**.

   > [!NOTE]
   > Po vytvoření přesunu zásob budou řádky interního přesunu odstraněny.

   Zbytek ad hoc přesunu provedete na stránce **Přesun zásob** stejným způsobem jako u přesunu založeného na původních dokladech. Pro více informací navštivte například [Přesouvání komponent do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

## Přesunutí zboží pomocí deníku přeřazení zboží
Namísto použití dokladů přesunu ve skladu můžete zaznamenávat přesun zboží pomocí přeřazení jejich kódů přihrádek. Pro více informací navštivte [Počet, úprava a přeřazení zásob pomocí deníků](inventory-how-count-adjust-reclassify.md).
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník přeřazení  zboží** a poté vyberte související odkaz.
2. Na každém řádku deníku definujte přihrádky, ze kterých a do kterých chcete zboží přesunout, vyplněním polí **Kód přihrádky** a **Kód nové přihrádky**.

   1. Chcete-li přesunout celý obsah přihrádky do jiné přihrádky, zvolte akci **Načíst obsah přihrádky**.
   2. Vyplňte filtry a najděte přihrádku, jejíž obsah chcete přesunout, a pak zvolte tlačítko **OK**. Řádky deníku jsou vyplněny obsahem přihrádky.
3. Vyplňte zbývající pole na každém řádku deníku.
4. Zaúčtujte deník přeřazení.

   > [!NOTE]
   > Na rozdíl od dokladů přesunů nevytvoří zaúčtováný přesun deníkem přeřazení požadavek skladu k provedení fyzické úlohy.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
