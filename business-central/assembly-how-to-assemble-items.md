---
    title: How to Assemble Items | Microsoft Docs
    description: If the **Replenishment System** field on the item card contains **Assembly**, then the default method of supplying the item is to assemble it from defined components and potentially by a defined resource.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: kit, kitting
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Montáž zboží
Pokud pole **Systém doplnění** na kartě zboží obsahuje **Montáž**, pak výchozí metodou dodání tohoto zboží je montáž z definovaných komponent a případně pomocí definovaného zdroje.

Komponenty a zdroje, které jdou do tohoto druhu zboží montáže, musí být definovány v kusovníku sestavy. Pro více informací navštivte [Práce s kusovníky](inventory-how-work-BOMs.md).

Zboží montáže lze nastavit pro dva různé procesy montáže:

- Montáž na sklad.
- Montáž na zakázku.

Obvykle používáte **Montáž na sklad** pro zboží, které chcete sestavit před prodejem, například pro přípravu na kampaň a udržení jich na skladě, dokud nejsou objednány. Toto zboží je obvykle standardní, jako jsou zabalené sady, které nenabízíte k přizpůsobení požadavkům zákazníků.

Obvykle používáte **Montáž na zakázku** pro zboží, které nechcete skladovat, protože očekáváte, že je přizpůsobíte požadavkům zákazníků nebo protože chcete minimalizovat účetní náklady zásob tím, že je dodáte včas. Pro více informací navštivte [Prodej zboží montáže na zakázku](assembly-how-to-sell-items-assembled-to-order.md).

Pro další informace o nastavení zboží montáže navštivte [Princip montáže na zakázku a montáže na sklad](assembly-assemble-to-order-or-assemble-to-stock.md).

Tyto možnosti nastavení jsou výchozí nastavení, které řídí, jak se prvotně zpracovávají řádky prodejních a montážních objednávek. Při zpracování prodeje se můžete odchýlit od těchto výchozích hodnot a dodávat zboží montáže nejoptimálnějším způsobem. Pro více informací navštivte [Prodej skladového zboží podle montáže na zakázku](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) a [Prodej zboží montáže na zakázku a skladového zboží dohromady](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]
> S komponenty montáže se manipuluje speciálním způsobem v základních konfiguracích skladu. Pro více informací navštivte sekci “Zpracování zboží montáže na zakázku pomocí vyskladnění zásob” v [Vyskladnění zboží pomocí vyskladnění zásob](warehouse-how-to-pick-items-with-inventory-picks.md).

V tomto postupu vytvoříte a zpracujete montážní zakázku pro zboží, které je smontováno do zásoby, což znamená bez propojené prodejní objednávky. Kroky zahrnují zahájení montážní zakázky, řešení potenciálních problémů s dostupností komponent a částečné zaúčtování výstupu zboží montáže.

## Smontování zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Montážní zakázky** a poté vyberte související odkaz.
2. Vyberte akci **Nový**. Otevře se stránka **Nové montážní zakázky**.
3. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. V poli **Číslo zboží** vyberte zboží montáže, které chcete zpracovat. Toto pole je filtrováno tak, aby zobrazovalo pouze zboží, které je nastaveno pro montáž, což znamená, že mají přiřazené kusovníky montáže.
5. Do pole **Množství** zadejte, kolik jednotek zboží chcete sestavit.

   > [!NOTE]
   > Pokud jedna nebo více komponent není k dispozici ke splnění zadaného množství zboží montáže k definovanému datu splnění, otevře se automaticky stránka **Dostupnost montáže**, která poskytne podrobné informace o počtu sestaveného zboží, které lze sestavit na základě dostupnosti komponent. Pro více informací navštivte [Zobrazení dostupnosti zboží](inventory-how-availability-overview.md). Po zavření stránky se vytvoří montážní zakázka s upozorněním na dostupnost při daných řádcích komponent.

   Řádky montážní zakázky jsou automaticky vyplněny obsahem kusovníku montáže a s množstvím řádků podle záhlaví montážní zakázky.

   > [!NOTE]
   > Pokud se po vyplnění záhlaví montážní zakázky otevře stránka **Dostupnost montáže**, pak každý ovlivněný řádek zakázky obsahuje hodnotu **Ano** v poli **Varování  dostupnosti** s odkazem na podrobné informace o dostupnosti. Pro více informací navštivte Kontrola dostupnosti. Problém s dostupností komponent můžete vyřešit odložením počátečního data, nahrazením komponenty jiným zbožím nebo výběrem dostupné náhrady, pokud je definována.

6. Do pole **Množství k montáži** zadejte, kolik jednotek zboží montáže chcete zaúčtovat jako výstup při příštím odeslání montážní zakázky. Toto množství může být nižší než hodnota v poli **Množství**, aby odráželo částečné zaúčtování výstupu.

   > [!NOTE]
   > Aby se zajistilo, že účtování spotřeby komponenty odpovídá účtování výstupu montáže, pole množství v řádcích montážní objednávky se automaticky přizpůsobí hodnotě, kterou zadáte do pole **Množství k montáži**.
7. Na řádcích montážní zakázky typu **Zboží** nebo **Zdroj** zadejte v poli **Množství ke spotřebě**, kolik jednotek chcete zaúčtovat jako spotřebované při příštím odeslání montážní zakázky.
8. Pokud jste připraveni částečně nebo úplně účtovat, vyberte akci **Účtovat**.

   > [!NOTE]
   > Pokud jsou výstrahy stále přítomny v kterékoli z řádků montážní zakázky, účtování se zablokuje. Zobrazí se zpráva o tom, která komponenta nebo komponenty nejsou v zásobách.

Po úspěšném zaúčtování je zboží montáže zaúčtováno jako výstup do kódu lokace a potenciálního kódu přihrádky, které jsou definovány v montážní zakázce. U ručně vytvořených montážních zakázek může být lokace zkopírována z pole **Vých. kód lokace pro obj**. Pro toky montáže na zakázku lze kód lokace zkopírovat z řádku prodejní objednávky.

## Viz také
[Správa montáže](assembly-assemble-items.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
