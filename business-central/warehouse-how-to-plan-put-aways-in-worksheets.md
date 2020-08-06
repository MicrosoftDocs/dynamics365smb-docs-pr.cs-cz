---
    title: How to Plan Put-aways in Worksheets | Microsoft Docs
    description: If your location requires both put-away and receive processing, and you want to plan put-away instructions for a number of receipts, rather than have employees follow the instructions that application creates for separate posted receipts, you can use the put-away worksheet.
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
# Plánování v sešitech zaskladění
Pokud vaše lokace vyžaduje zpracování zaskladění i příjmu a chcete naplánovat pokyny k zaskladění pro několik příjmů, místo aby zaměstnanci postupovali podle pokynů, které aplikace vytvoří pro samostatné zaúčtované příjmy, můžete použít sešit zaskladění.

Chcete-li nastavit sklad tak, aby řádky příjmu byly k dispozici v sešitě zaskladnění ihned po zaúčtování, vyberte pole **Použít sešit zaskladnění** na záložce **Sklad** na kartě lokace. Pro více informací navštivte [Nastavení správy skladu](warehouse-setup-warehouse.md).

Pokud toto pole nevyberete, aplikace automaticky vytvoří pokyny k zaskladnění pro příjemky při jejich zaúčtování.

> [!NOTE]
> Bez ohledu na stav pole **Použít sešit zaskladnění** na kartě lokace, můžete vždy dostat řádky pokynů zaskladnění, tj.  řádky zaúčtovaných příjemek, do sešitu zaskladnění pomocí následujícího postupu:
> 1. Na stránce **Zaskladnění** odstraňte celý pokyn zaskladnění stisknutím kombinace kláves Ctrl+D nebo vyberte řádky, které chcete zpracovat v sešitu, a odstraňte je.
> 2. Pokračujte v procesu tolikrát, kolikrát budete chtít, dokud neodstraníte řádky, na kterých chcete pracovat v sešitu. Nyní vyberte **Sešity zaskladnění** a pokračujte v plánování.


## Plánování pokynů v sešitu zaskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit zaskladnění** a poté vyberte související odkaz.
2. Vyberte akci **Kopie dokladů skladu**. Otevře se stránka **Výběr zaskladnění**.

   Zobrazí se všechny zaúčtované příjemky a zapsané interní zaskladnění, které byly předány do funkce zaskladnění, včetně těch, pro které již byly vytvořeny pokyny k zaskladnění. Doklady s řádky zaskladnění, které byly zcela zaskladněny a zapsány, nejsou v tomto seznamu zobrazeny.

3. Vyberte doklady, na kterých chcete pracovat v sešitu. Můžete pracovat na řádcích z několika dokumentů současně.

   > [!NOTE]
Pokud se pokusíte vybrat příjemku nebo interní doklad zaskladnění, pro který jste již vytvořili pokyny pro všechny jeho řádky, aplikace vás informuje, že není co zpracovat.

4. Vyplňte pole **Způsob třídění**  a seřaďte řádky podle vašich preferencí.

   > [!NOTE]
Způsob řazení řádků v sešitu se neprovádí automaticky do pokynů zaskladnění, ale existují stejné možnosti řazení spolu s pořadím přihrádek. Pořadí řádků, které plánujete v sešitu, je tak snadno znovu vytvořeno při vytváření pokynů k zaskladnění nebo při řazení v pokynech k zaskladnění.

5. Vyplňte pole **Množ. ke zpracování**. Vyberte akci **Automat.vyplnit množ.ke zprac.** nebo vyplňte pole ručně.
6. V případě potřeby upravte řádky ručně. Řádky můžete odstranit například v případě, že některé zboží musí být zaskladněné do přihrádky daleko od přihrádek pro ostatní zboží.

   > [!NOTE]
Odstraněné řádky jsou odstraněny pouze z tohoto sešitu, nikoli ze seznamu výběrů zaskladnění.

7. Vyberte akci **Vytvořit vyskladnění**. Otevře se stránka **Vytvořit dokument**, kde můžete přidat další informace k zaskladnění, které vytváříte, následujícím způsobem:

   - Zaskladnění můžete přiřadit konkrétnímu zaměstnanci.
   - Řádky pokynu zaskladnění můžete seřadit stejně jako v sešitu nebo podle pořadí přihrádek. Při řazení podle pořadí přihrádky se nejprve zobrazí řádky Vzít, protože většina příjmových přihrádek má pořadí přihrádek 0 a řádky Vložit se zobrazí jako poslední, počínaje přihrádkami s nejnižším pořadím přihrádky. Pokud jste strukturovali svůj sklad tak, aby přihrádky s podobným pořadím byly vedle sebe, řádky řazené tímto způsobem nakonec uloží kroky pro zaměstnance skladu.
   - Můžete se rozhodnout, že zprostředkující řádky vytvořené při přerušení větší měrné jednotky na menší měrné jednotky neuvidíte, a to výběrem pole **Nastavit filtr rozbalení**. Pro více informací navštivte [Povolení automatického rozdělení zboží s řízeným zaskladněním a vyskladněním](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).
   - Můžete si vybrat, že nebudete mít pole **Množ. ke zpracování** automaticky vyplněné podle pokynů pro zaskladnění.
   - Dokument můžete vytisknout okamžitě.

8. Vyberte tlačítko **OK** a aplikace vytvoří zaskladnění podle vašich požadavků.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
