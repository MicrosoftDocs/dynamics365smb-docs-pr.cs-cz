---
    title: Put Items Away | Microsoft Docs
    description: The warehouse activity of putting items away after they are received or output is performed in different ways depending on how warehouse management features are configured.
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
# Zaskladnění zboží
Činnost skladu zaskladnění zboží po jeho přijetí nebo vyskladnění se provádí různými způsoby v závislosti na tom, jak jsou nakonfigurovány funkce správy skladu. Složitost se může řadit od žádných funkcí skladu, přes základní konfigurace skladu pro zpracování objednávek pouze v jedné nebo více aktivitách, až po pokročilé konfigurace, kde všechny aktivity skladu musí být prováděny v směrovaném workflow. Pro více informací navštivte [Nastavení správy skladu](warehouse-setup-warehouse.md).

Pokud se rozhodnete, že chcete uspořádat a zaznamenat údaje o zaskladnění pomocí dokumentů skladu, zaškrtněte políčko **Vyžadovat zaskladnění** na kartě lokace. To znamená, že když máte zboží přicházející do skladu prostřednictvím vstupního původního dokladu, chcete, aby bylo zaskladnění tohoto zboží řízeno systémem. Vstupní původní dokument může být nákupní objednávka, objednávka prodejní vratky, vstupní objednávka transferu nebo výrobní zakázka, jejíž výstup je připraven k zaskladnění.

Pokud je vaše lokace nastavena na použití procesu zaskladnění, ale nepoužíva proces k příjmu můžete pomocí stránky **Zaskladnění zásob** uspořádat informace o zaskladnění, vytisknout jej a zadat výsledek skutečného zaskladnění a zaúčtovat informace o zaskladnění, které zase zaúčtují informace o příjmu pro původní doklad. V případě výrobní zakázky zaúčtuje proces zaúčtování výstup objednávky a dokončí výrobní zakázku.

Pokud je vaše lokace nastavena tak, aby vyžadovala zpracování příjmu i zaskladnění, takže jste zašktrli pole **Vyžadovat příjem** a **Vyžadovat zaskladnění** na karte lokace, existuje jiný postup pro zaskladnění zboží. V takovém případě použijete stránku **Zaskladnění**. Zaskladnění funguje podobně jako zaskladnění zásob s tím rozdílem, že místo zaúčtování informací zaregistrujete zaskladnění. Všimněte si, že registrace zaskladněné položky skladu nezaúčtuje příjem zboží. Pouze aktualizuje obsah přihrádky. Jako správce skladu můžete pomocí listů zaskladnění uspořádat informace o zaskladnění před vytvořením jednotlivých pokynů pro zaskladnění skladem.

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| **Viz** | **také** |
|------------|-------------|  
| Zaúčtování příjmu zboží přímo z dokladu vstupní objednávky a tím zaznamenání zaskladněného dokladu, protože neexistuje žádná konfigurace skladu. | [Příjem zboží](warehouse-how-receive-items.md) |
| Zaskladnění objednávky zboží podle objednávky a zaúčtování příjemky ve stejné aktivitě v základní konfiguraci skladu. | [Zaskladnění zboží pomocí zaskladnění zásob](warehouse-how-to-put-items-away-with-inventory-put-aways.md) |
| Zaskladnění zboží pro více objednávek v rozšířené konfiguraci skladu. | [Zaskladnění zboží pomocí zaskladnění](warehouse-how-to-put-items-away-with-warehouse-put-aways.md) |
| Zaskladnění vyrobeného nebo sestaveného zboží do základní nebo pokročilé konfigurace skladu. | [Zaskladnění výroby nebo montáže](warehouse-how-to-put-away-production-output.md) |
| Naplánování optimalizovaných pokynů pro zaskladnění pro řadu zaúčtované příjemky ze skladu, nikoli aby pracovníci skladu jednali přímo na příjemkách. | [Plánování zaskladnění v sešitech](warehouse-how-to-plan-put-aways-in-worksheets.md) |
| Vrácení zboží, které bylo technicky vyskladněno pomocí interního vyskladnění, například pro výrobní zakázku, která nespotřebovávala očekávané množství. | [Vyskladnění a zaskladnění bez původního dokladu](warehouse-how-to-create-put-aways-from-internal-put-aways.md) |
| Rozdělení řádku zaskladnění, umístění části zaskladněného množství do dostupných přihrádek, protože určená přihrádka je již plná. | [Rozdělení řádků aktivit skladu](warehouse-how-to-split-warehouse-activity-lines.md) |
| Získání okamžitého přístupu k zaskladněným položkám, které jsou vám přiřazeny jako skladníkovi. | [Najděte svá přiřazení skladu](warehouse-how-to-find-your-warehouse-assignments.md) |

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)    
[Zásoby](inventory-manage-inventory.md)    
[Nastavení správy skladu](warehouse-setup-warehouse.md)       
[Správa montáže](assembly-assemble-items.md)      
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]