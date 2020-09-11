---
    title: How to Put Items Away with Inventory Put-aways | Microsoft Docs
    description: When your location is setup to require put-away processing but not receive processing, you use the **Inventory Put-away** document to record and post put-away and receipt information for your source documents. The inbound source document can be a purchase order, a sales return order, an inbound transfer order, or a production order whose output is ready for put-away.
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
# Zaskladnění zboží pomocí zaskladnění zásob
Pokud je lokace nastavena tak, aby vyžadovala zpracování zaskladnění, ale ne zpracování příjmu, použijete doklad **Zaskladnění zásob** k zaznamenání a zaúčtování informací o zaskladnění a příjmu pro vaše původní doklady. Vstupním původním dokladem může být nákupní objednávka, objednávka prodejní vratky, vstupní objednávka transferu nebo sestava nebo výrobní zakázka, jejíž výstup je připraven k zaskladnění.

Zaskladněné zásoby můžete vytvořit třemi způsoby:

- Nejprve vytvořte zaskladnění ve dvou krocích vytvořením požadavku skladu z původního dokladu, který funguje jako signál pro sklad, že původní doklad je připraven k zaskladnění. Zaskladnění zásob lze pak vytvořit ze stránky **Zaskladnění zásob** na základě původního dokladu.
- Vytvořte zaskladnění zásob přímo ze samotného původního dokladu.
- Pomocí dávkové úlohy vytvořte zaskladnění zásob pro několik původních dokladů najednou.

## Žádost o zaskladnění zásob vydáním původního dokladu
U nákupních objednávek, objednávek prodejní vratky, příchozích objednávek transferu a montážních zakázek vytvoříte požadavek na sklad vydáním objednávky. Následující text popisuje, jak to provést z nákupní objednávky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.
2. Vyberte nákupní objednávku, kterou chcete vydat, a pak zvolte akci **Vydat**.

   U výrobních zakázek vytvoříte požadavek skladu vytvořením vstupního požadavku z vydané výrobní zakázky.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vydané výrobní zakázky** a poté vyberte související odkaz.
4. Vyberte akci **Vytvořit vstupní požadavek  skl.**.

> [!NOTE]
> Požadavek na vstupní sklad můžete také vytvořit zaškrtnutím políčka **Vytvořit vstupní požadavek** při aktualizaci výrobní zakázky. Pro více informací navštivte [Přeplánování nebo přímá aktualizace výrobních zakázek](production-how-to-replan-refresh-production-orders.md).

Po vytvoření požadavku na sklad může zaměstnanec skladu přiřazený k zaskladnění zboží vidět, že je původní doklad připraven, a může vytvořit doklad zaskladnění zásob.

## Vytvoření zaskladnění na základě původního dokladu
Po vytvoření požadavku může zaměstnanec skladu vytvořit nové zaskladnění zásob na základě vydaného původního dokladu.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaskladnění zásob** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. V poli **Původní doklad** vyberte typ původního dokladu, pro který chcete vytvořit zaskladnění.
4. V poli **Číslo původu** vyberte původní doklad.
5. Případně zvolte akci **Kopie původ.dokladu**, chcete-li vybrat doklad ze seznamu příchozích původních dokladů, které jsou připraveny k zaskladnění v lokaci.
6. Stisknutím tlačítka **OK** vyplňte řádky zaskladnění podle vybraného původního dokladu.

## Vytvoření zaskladnění zásob z původního dokladu
1. V původním dokladu, kterým může být nákupní objednávka, objednávka prodejní vratky, objednávka vstupního transferu nebo výrobní zakázka, zvolte akci **Vytvořit zaskl./vyskl.zásob**.
2. Zaškrtněte políčko **Vytvořit zaskladnění  zásob**.
3. Vyberte tlačítko **OK**. Nyní je vytvořeno nové zaskladnění zásob.

## Vytvoření více zaskladnění zásob pomocí dávkové úlohy
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vytvořit zaskl. /vyskl.zásob** a poté vyberte související odkaz.
2. Na záložce **Požadavek skladu** na stránce požadavku použijte pole **Původní doklad** a **Číslo původu** pro filtrování určitých typů dokladů nebo rozsahů čísel dokladů.
3. Na záložce **Možnosti** zašktněte políčko **Vytvořit zaskladnění  zásob**.
4. Vyberte tlačítko **OK**. Nyní je vytvořeno zadané zaskladnění zásob.

## Zaznamenání zaskladnění zásob
1. Otevřete dříve vytvořený doklad zaskladnění výběrem dokladu ze stránky **Zaskladnění zásob**.
2. V poli **Kód přihrádky** na řádcích zaskladnění je přihrádka, kde musí být zboží zaskladněné, navržena podle výchozí přihrádky zboží. V případě potřeby můžete přihrádku na této stránce změnit.
3. Proveďte zaskladnění a zadejte informace o skutečném zaskladněném množství do pole **Množ. ke zpracování**.

   Pokud je nutné umístit zboží pro jeden řádek do více než jedné přihrádky, například proto, že je určená přihrádka plná, použijte funkci **Rozdělit řádek** na záložce **Řádky**. Pro více informací o rozdělení řádků navštivte [Rozdělení řádků aktivit skladu](warehouse-how-to-split-warehouse-activity-lines.md).
4. Po provedení zaskladnění zvolte akci **Účtovat**.

Proces účtování zaúčtuje příjem nebo pro výrobní zakázky výstup řádků původního dokladu, které byly zaskladněny, a pokud lokace používá přihrádky, účtování také vytvoří položky skladu k zaúčtování změn množství přihrádky.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
