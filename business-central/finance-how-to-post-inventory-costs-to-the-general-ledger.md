---
title: How to Post Inventory Costs to the General Ledger| Microsoft Docs
description: Describes how to manage the physical products that you trade in, for example, handling the stock in your warehouse.
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 04/01/2020
ms.author: sgroespe

---
# Odsouhlasení nákladů na zboží s financemi
Při zaúčtování skladových transakcí, jako jsou prodejní dodávky, nákupní faktury nebo úpravy zásob, jsou změněné náklady na zboží zaznamenány do položek ocenění zboží. Aby se tato změna hodnoty zásob projevila ve vašich finančních knihách, jsou náklady automaticky zaúčtovány na související účty zásob v hlavní knize. Pro každou skladovou transakci, kterou účtujete, jsou příslušné hodnoty zaúčtovány na účet zásob, účet úprav a účet nákladů na prod.zboží v hlavní knize.

Automatické účtování nákladů je definováno polem **Automatické účtování nákladů** na stránce **Nastavení zásob**.

I když jsou náklady automaticky zaúčtovány do hlavní knihy, je stále nutné zajistit, aby náklady na zboží byly předány na související transakci odchozího prodeje, zejména v situacích, kdy zboží prodáváte před fakturací nákupu tohoto zboží. Toto se nazývá úprava nákladů. Náklady zboží se automaticky upravují, když účtujete transakce za zboží, ale také můžete zboží upravovat ručně. Pro více informací navštivte [Úprava nákladů](inventory-how-adjust-item-costs.md).

## Ruční zaúčtování nákladů zásob
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtování nákladů na zboží** a poté vyberte související odkaz.
2. Ručně zaúčtujte náklady do hlavní knihy spuštěním dávkové úlohy. Při spuštění této dávkové úlohy jsou vytvořeny věcné položky na základě položek ocenění. Položky můžete zaúčtovat tak, aby byly shrnuty podle účto skupiny.

> [!NOTE]
> Při spuštění této dávkové úlohy se mohou vyskytnout chyby související s chybějícím nastavením nebo nekompatibilním nastavením dimenze. Pokud dávková úloha narazí na chyby v nastavení dimenze, přepíše tyto chyby a použije dimenze položky ocenění. V případě jakýchkoli dalších chyb přeskočí dávková úloha zaúčtování položek ocenění a uvádí je na konci zprávy v části nazvané „Přeskočené položky“. Chcete-li zaúčtovat tyto položky, musíte opravit chyby.

Chcete-li zobrazit seznam chyb před spuštěním dávkové úlohy účtování, můžete spustit sestavu **Účtování nákladů  na zboží - test**. Protokol o testu uvádí všechny chyby, které se vyskytly během testovacího účtování. Potom můžete chyby opravit a spustit dávkovou úlohu účtování nákladů zásob bez přeskočení jakýchkoli položek.

Pokud byste chtěli jednoduše získat přehled o tom, jaké hodnoty by mohly být zaúčtovány do hlavní knihy bez skutečného provedení účtování, můžete spustit dávkovou úlohu **Účtování nákladů na zboží** bez skutečného účtování hodnoty do hlavní knihy. To provedete zrušením zaškrtnutí pole **Účtovat** na stránce požadavku. Tímto způsobem je při spuštění dávkové úlohy vytvořena sestava zobrazující hodnoty, které jsou připraveny k zaúčtování do hlavní knihy, ale nejsou zaúčtovány.

## Kontrola sladění mezi položkami inventury a věcnými položkami
Stránka **Odsouhlasení zásoby – finance** obsahuje následující:

- Zpřístupní rozdíly odsouhlasení porovnáním toho, co je zaznamenáno ve věcných položkách a co je zaznamenáno v položkách inventury (položky ocenění).
- Zobrazí neodsouhlasené částky nákladů v položkách ocenění a v položkách inventury, jako by byly mapovány na odpovídající účty související se zásobami ve věcných položkách, a porovná je s součty skutečně zaznamenanými ve stejných účtech ve financích.
- Odráží strukturu podvojného účetnictví financí, a to vizuálním zobrazením dat jako takových. Například položka Náklady na prod. zboží má odpovídající položku inventury.
- Umožňuje uživatelům rozbalit a zobrazit položky, které tvoří částky nákladů.
- Zahrnuje filtry pro zúžení analýzy podle data, zboží a umístění.
- Vysvětluje důvody nesouladu v informativních zprávách.


Sloupec **Název** zobrazen vlevo v mřížce uvádí různé typy finančních účtů, které jsou spojeny se zásobami.

Sloupce **Zásoby**, **Zásoby (dočasné)** a **Nedokončená výroba** zobrazují fakturované, nefakturované a nedokončené součty každého typu finančního účtu. Vypočítávají se z položek ocenění, to znamená, že se promítají do typů finančních účtů, kde skončí, až budou nakonec zaúčtovány do financí.

Sloupec **Celkem** zobrazuje součet (tučným písmem) vstupních hodnot ve třech sloupcích zásob.

Sloupec **Finance celkem** zobrazuje částky (tučným písmem) pro každý typ finančního účtu, který existuje ve financích. Vypočítávají se z věcných položek, tj. představují náklady na zásoby již zaúčtované ve financích.

Sloupec **Rozdíl** představuje rozdíl mezi hodnotou v polích **Finance celkem** a **Celkem**.

V horní části stránky **Odsouhlasení zásoby – finance** můžete zadat filtry, které omezí například dobu, za kterou chcete získat informace.

Pokud zaškrtnete políčko **Zobrazit varování** a pokud existují nějaké nesrovnalosti mezi celkovými hodnotami zásob a věcnými položkami, aplikace zobrazí zprávy v poli **Varování** které vysvětlují tento rozpor. Pokud vyberete pole Varování, aplikace vám poskytne více informací o významu varování.

Po zadání všech příslušných filtrů vyberte akci **Zobrazit matici**. Data se vypočítají a objeví se stránka matice.

V levém sloupci v matici vidíte různé typy finančních účtů, které jsou spojeny se zásobami. V matici se pak zobrazí součty pro fakturované, nefakturované (dočasné) a nedokončené výrobky pro každý z těchto typů účtů. Tyto součty se počítají z položek ocenění.

Následující sloupce ukazují součty pro stejné typy účtů vypočtené z věcných položek.

Vyberte částku v kterémkoli z polí Celkem a zobrazte položky sestavy zásob, které byly použity k výpočtu součtů. U součtů zásob jsou položky sestavy zásob součtem položek ocenění pro zboží. Pro součty financí jsou položky sestavy zásob součty věcných položek.

## Viz také
[Správa nákladů zásob](finance-manage-inventory-costs.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)
