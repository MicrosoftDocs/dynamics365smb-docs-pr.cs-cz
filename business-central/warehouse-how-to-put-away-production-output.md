---
    title: How to Put Away Production Output | Microsoft Docs
    description: How you put away your output from production depends on how your warehouse is set up as a location.
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
# Zaskladnění výroby nebo výstupu montáže
Způsob zaskladnění výstupu z výroby závisí na tom, jak je sklad nastaven jako lokace. Pro více informací navštivte [Nastavení správy skladů](warehouse-setup-warehouse.md).

V základních konfiguracích skladu, kde lokace vyžaduje zpracování zaskladnění, ale ne zpracování příjmu, použijete doklad **Zaskladnění zásob** k uspořádání a zaznamenání zaskladněného výstupu.

V pokročilých konfiguracích skladu, kde lokace vyžaduje zpracování zaskladnění i příjmu, vytvoříte buď interní doklad zaskladnění, nebo doklad přesunu, který zaskladní výstup.

Prvním krokem při vytváření zaskladnění výstupu je vytvoření požadavku na vstupní sklad. Tento požadavek informuje sklad, že výstup výrobní nebo montážní zakázky je připraven k zaskladnění.

## Vytvoření požadavku na vstupní sklad
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vydaná výrobní zakázka** a poté vyberte související odkaz.
2. Ve výrobní zakázce, která je připravena k zaskladnění, zvolte akci **Vytvořit vstupní požadavek  skl.**.

> [!NOTE]
> Požadavek na vstupní sklad můžete také vytvořit zaškrtnutím políčka **Vytvořit vstupní požadavek** při aktualizaci výrobní zakázky. Pro více informací navštivte [Přeplánování nebo přímá aktualizace výrobních zakázek](production-how-to-replan-refresh-production-orders.md).

## Zaskladnění výstupu pomocí zaskladnění zásob
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaskladnění zásob** a poté vyberte související odkaz.
2. Vytvořte nové zaskladnění zásob. Pro více informací navštivte [Zaskladnění zboží pomocí zaskladnění zásob](warehouse-how-to-put-items-away-with-inventory-put-aways.md).
3. Chcete-li získat přístup k výstupu výrobní zakázky, zvolte akci **Kopie pův.dokladů** a pak vyberte vydanou výrobní zakázku.
4. Podle potřeby vyplňte řádky zaskladnění.
5. Až budou řádky připraveny k zaúčtování, zvolte akci **Účtovat**. Účtování vytvoří potřebné položky skladu a zaúčtuje výstup zboží.

Můžete také vytvořit **Zaskladnění zásob** přímo z vydané výrobní zakázky. Pro více informací navštivte [Zaskladnění zboží pomocí zaskladnění zásob](warehouse-how-to-put-items-away-with-inventory-put-aways.md).

Při zaúčtování zaskladnění zásob se předpokládá, že všechny operace jsou zaúčtovány podle standardního postupu, to znamená, že výstupní množství je zaúčtováno podle poslední operace. Deník výstupu můžete použít k zaúčtování odchylek ve výstupním množství a časech nastavení a spuštění. Pokud je nutné zaúčtovat množství částečně po vytvoření zaskladnění zásob, můžete tak učinit v době nastavení a množství pro všechny operace kromě poslední. V takovém případě je poslední operace řízena zaskladněním zásob.

Pokud potřebujete pouze zaúčtovat nastavení nebo dobu běhu při poslední operaci, nastavte výstupní množství v poslední operaci na hodnotu 0. Případně se můžete rozhodnout, že poslední řádek nezaúčtujete, a to jeho pouhým odstraněním.

## Zaskladnění výstupu pomocí interního zaskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník  zaskladnění** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vyplňte záhlaví nového interního zaskladnění alespoň s hodnotou v poli **Kód lokace**.
4. Vyplňte řádek pro každé zboží, které chcete přesunout do skladu. Musíte pouze vyplnit pole **Číslo zboží** a **Množství**.

   > [!NOTE]
   > Když vyberete pole **Číslo zboží**, otevře se místo seznamu **Přehled obsahů přihrádek** seznam **Přehled zboží**. Důvodem je, že chcete zaskladnit zboží, které je v určité přihrádce – obsah přihrádky – nejen zboží, a již víte, z jaké přihrádky by mělo být zboží odebráno.

4. Chcete-li vyplnit řádky listu celým obsahem přihrádky nebo filtrovaným obsahem přihrádek v lokaci, zvolte akci **Načíst obsah přihrádky**.
5. Vyberte akci **Vytvořit vyskladnění** a zboží, které chcete přesunout z výroby, je nyní v pokynech k zaskladnění čekajících na uložení ve skladu.

> [!NOTE]
> Když je vaše lokace skladu nastavena na použití řízeného zaskladnění a vyskladnění, je sklad propojen s výrobním zařízením prostřednictvím výrobních přihrádek: vstupní a výstupní přihrádky a přihrádka otevřeného obchodu, definujte na záložce **Přihrádky** na kartě lokace. Když účtujete výstup výrobní zakázky, výstup je umístěn do **Výstupní výrobní přihrádky**. Stejným postupem, jaký je popsán výše, zaskladněte produkční výstup, s tím rozdílem, že namísto použití výchozí přihrádky zboží přesunete nebo zaskladníte zboží z **Výstupní výrobní přihrádky** do výchozí přihrádky zboží.

## Ruční zadání přihrádky pro ukládání zboží z výrobního výstupu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit přesunu** a poté vyberte související odkaz.
2. Vyplňte záhlaví a vytvořte řádek pro každé zboží, které chcete přesunout do skladu.
3. Vyplňte pole **Z kódu přihrádky** a **Do kódu přihrádky** a zadejte množství do pole **Množství**.
4. Chcete-li vyplnit řádky listu celým obsahem přihrádky nebo filtrovaným obsahem přihrádek v lokaci, zvolte akci **Načíst obsah přihrádky**.
5. Vyberte akci **Vytvořit přesun**. Pokyny k přesunu skladu jsou vytvořeny pomocí řádků Vzít a Vložit, aby je zaměstnanci skladu provedli.

> [!NOTE]
> Nelze zadat číslo původního dokladu, například číslo výrobní zakázky, do dokladů o zaskladnění, interním zaskladnění nebo přesunu pro žádný z těchto postupů.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
