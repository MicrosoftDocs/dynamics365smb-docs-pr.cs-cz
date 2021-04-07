---
    title: Design Details - Item Tracking Lines Page | Microsoft Docs
    description: Read about how to managethe flow of serial and lot numbers in your inventory.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: design, inventory, item, tracking, serial number, lot number
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Stránka Řádky sledování zboží
Záznamy sledování zboží a záznamy rezervací jsou vytvářeny v rezervačním systému a jejich dostupnost se vypočítává dynamicky. Data zadaná na stránce **Řádky sledování zboží** je řízena pomocí dočasné tabulky **Specifikace sledování**. Po zavření stránky jsou aktivní data zapsána do tabulky **Položky rezervace** a stará data jsou zapsána do tabulky **Specifikace sledování**. Pro více informací navštivte [Detaily návrhu: Aktivní versus Historické položky sledování zboží](design-details-active-versus-historic-item-tracking-entries.md).

Náhled z polí **Sériové číslo** a **Číslo šarže** zobrazují dostnunost na základě tabulky **Položky zboží** a tabulky **Položky rezervace** bez filtru na datum. Matice polí množství v záhlaví stránky **Řádky sledování zboží** dynamicky rozbrazuje množství a součty čísel sledování položek, které jsou zadávány na řádcích stránky. Množství musí odpovídat množství řádku dokladu, který je označen hodnotou **0** v poli **Nedefinováno** v hlavičce stránky.

Chcete-li koordinovat tok sériových čísel a čísel šarží prostřednictvím zásob, existují následující pravidla pro zadávání dat na stránce **Řádky sledování zboží**:

* U vstupních i výstupních řádků sledování zboží nelze zadat sériové číslo s číslem šarže nebo bez více než jednou ve stejné instanci stránky **Řádky sledování zboží**. Pokud se pokusíte zadat libovolnou kombinaci sériových čísel nebo čísel šarží, která jsou již na stránce, chybová hláška zablokuje zadávání dat.
* Pro vstupní řádky sledování zboží, nelze zaúčtovat související doklad, pokud je zboží stejné varianty a se stejným sériovým číslem již na skladě. Pokud se pokusíte zaúčtovat kladný řádek pro skladové zboží se stejnou variantou a sériovým číslem, chybová hláška zablokuje účtování. Pokud máte u vstupních i výstupních řádků sledování zboží na otevřených dokladech stejné kombinace sériových čísel a čísel šarže, které se vztahují k různým řádkům zdrojového dokladu, tj, existují v různých případech na stránce **Řádky sledování zboží** dokud nebude zaúčtován související dokument.
* Pokud je zboží nastaveno pro sledování specifického sériového čísla nebo sledování specifického číslo šarže, nelze zaúčtovat řádek výstupního dokladu, pokud ve skladu neexistuje zboží s definovaným sériovým číslem nebo číslem šarže. Pokud se pokusíte zaúčtovat řádek výstupního dokladu se zbožím se sériovým číslem nebo číslem šarže, které není ve skladu, chybová zpráva zablokuje účtování.

Pravidla pro zadávání dat na stránce **Řádky sledování zboží** také podporují zásady spojování, které upravují sledování, plánování a rezervaci objednávek. Pro více informací navštivte [Detaily návrhu: Sledování zboží a plánování](design-details-item-tracking-and-planning.md).

## Viz také
[Detaily návrhu: Sledování zboží](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]