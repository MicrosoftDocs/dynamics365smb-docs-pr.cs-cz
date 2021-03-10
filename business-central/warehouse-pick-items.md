---
    title: Pick Items | Microsoft Docs
    description: The warehouse activity of picking items before they are shipped or consumed is performed in different ways, depending on how warehouse management features are configured. The setup complexity can rank from no warehouse features, through basic warehouse configurations for order-by-order handling in one or more activities only, to advanced configurations where all warehouse activities must be performed in a directed workflow.
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
# Vyskladnění zboží

Aktivita skladu vyskladnění zboží před jeho dodáním nebo spotřebou se provádí různými způsoby v závislosti na konfiguraci funkcí správy skladu. Složitost se může řadit od žádných funkcí skladu, přes základní konfigurace skladu pro zpracování podle objednávek pouze v jedné nebo více aktivitách, až po pokročilé konfigurace, kde musí být všechny aktivity skladu prováděny v řízeném workflow. Pro více informací navštivte [Nastavení správy skladu](warehouse-setup-warehouse.md).

Pokud se rozhodnete uspořádat a zaznamenat svou aktivitu vyskladnění pomocí dokladů skladu, zaškrtnete políčko **Vyžadovat vyskladnění** na kartě lokace. To naznačuje, že když máte zboží, které je třeba vyskladnit pro odchozí zdrojový doklad, chcete, aby vyskladnění tohoto zboží bylo řízené systémem. Výstupním původním dokladem může být prodejní objednávka, objednávka nákupní vratky, výstupní objednávka transferu, servisní zakázka nebo výrobní zakázka, jejíž komponenty by měly být vyskladněny.

> [!NOTE]
> I když se toto nastavení nazývá **Vyžadovat vyskladnění**, stále můžete odesílat zásilky přímo z původního obchodního dokladu na místo, kde toto políčko zaškrtnete.

Pokud je vaša lokace nastavena tak, aby vyžadovala zpracování vyskladnění, ale nikoli zpracování zásilky, můžete pomocí stránky **Vyskladnění zásob** uspořádat informace o vyskladnění, vytisknout informace o vyskladnění, zadat výsledek vyskladnění a odeslat informace o vyskladnění, pomocí kterých následně zaúčtujete zásilku zboží. V případě vyskladnění komponent pro výrobní zakázku zaúčtování vyskladnění také zaúčtuje spotřebu.

Pokud je vaše lokace nastavena tak, aby vyžadovala zpracování vyskladnění i dodávky, takže jste na kartě lokace zaškrtli pole **Vyžadovat vyskladnění** a **Vyžadovat dodání**, ke zpracování vyskladnění použijete stránku **Vyskladnění**. Vyskladnění funguje podobně jako vyskladnění zásob, kromě toho, že místo zaúčtování informací o vyskladnění vyskladnění i zaregistrujete. Tento proces registrace nezaúčtuje dodávku, ale pouze zpřístupní zboží k dodávce. Jako správce skladu můžete pomocí pracovních listů pro výběr uspořádat informace o vyskladnění před vytvořením jednotlivých pokynů pro vyskladnění skladu.

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| **Viz** | **také** |
|------------|-------------|  
| Zaúčtovat dodávku zboží přímo do výstupního dokladu objednávky, protože neexistují žádné prvky skladu. (Totéž platí pro prodejní objednávky, výstupní objednávky transferu a dodávky vratky.) | [Dodání zboží](warehouse-how-ship-items.md) |
| Vyberte zboží po objednávkách a zaúčtujte zásilku ve stejné aktivitě, v základní konfiguraci skladu. | [Vyskladnění zboží pomocí Vyskladnění zásob](warehouse-how-to-pick-items-with-inventory-picks.md) |
| Vyberte zboží pro více objednávek v pokročilé konfiguraci skladu. | [Vyskladnění zboží pomocí Vyskladnění](warehouse-how-to-pick-items-for-warehouse-shipment.md) |
| Vyberte komponenty pro výrobu nebo montáž v základní konfiguraci skladu. | [Vyskladnění pro výrobu nebo montáž v základních konfiguracích skladu](warehouse-how-to-pick-for-production.md) |
| Vyskladnění komponent pro výrobu nebo montáž v pokročilé konfiguraci skladu. | [Vyskladnění pro výrobu nebo montáž v pokročilých konfiguracích skladu](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md) |
| Naplánujte optimalizované pokyny pro vyskladnění pro řadu dodávek, nikoli aby pracovníci skladu jednali přímo na zaúčtovaných dodávkach. | [Plánujte vyskladnění v sešitech](warehouse-how-to-plan-picks-in-worksheets.md) |
| Vyskladnění zboží technicky pro zvláštní účel, jako je výrobní jednotka, která potřebuje další komponenty, tak, aby zboží technicky neopustilo sklad. | [Vyskladnění a zaskladnění bez původního dokladu](warehouse-how-to-create-put-aways-from-internal-put-aways.md) |
| Pochopte, jak automaticky vyskladnit zboží podle data vypršení platnosti, například zboží podléhající rychlé zkáze. | [Vyskladnění podle FEFO](warehouse-picking-by-fefo.md) |
| Rozdělte řádek vyskladnění na více řádků, například proto, že v určené přihrádce není dostatek zboží, ze kterých je možné požadované množství vyskladnit. | [Rozdělení řádků aktivit skladu](warehouse-how-to-split-warehouse-activity-lines.md) |
| Získejte okamžitý přístup k vyskladnění, která jsou vám přiřazena jako pracovníkovi skladu. | [Najděte svá přiřazení skladu](warehouse-how-to-find-your-warehouse-assignments.md) |

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)    
[Zásoby](inventory-manage-inventory.md)    
[Nastavení správy skladu](warehouse-setup-warehouse.md)       
[Správa montáže](assembly-assemble-items.md)      
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]