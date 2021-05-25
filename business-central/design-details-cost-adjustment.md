---
title: Design Details - Cost Adjustment | Microsoft Docs
description: The main purpose of cost adjustment is to forward cost changes from cost sources to cost recipients, according to an item’s costing method, to provide correct inventory valuation.
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
# Detaily návrhu: Úprava nákladů

Hlavním účelem úpravy nákladů je předat změny nákladů ze zdrojů nákladů příjemcům nákladů podle metody ocenění zboží, aby byla zajištěna správná hodnota zásob.

Zboží může být fakturováno z prodeje před tím, než bylo fakturována za nákup, takže zaznamenaná hodnota zásob prodeje neodpovídá skutečným nákupním nákladům. Úprava nákladů aktualizuje náklady na prodané zboží (NNPZ) pro historické položky prodeje, aby bylo zajištěno, že odpovídají nákladům na vstupní transakce, na které jsou použity. Pro více informací navštivte [Detaily návrhu: Vyrovnání zboží](design-details-item-application.md).

Následují sekundární účely nebo funkce úpravy nákladů:

* Faktura dokončené výrobní zakázky:

   * Změňte stav položek ocenění z **Očekávané** na **Skutečnou**.
   * Vymažte účty nedokončené výroby. Pro více informací navštivte [Detaily návrhu: Účtování prodejní zakázky](design-details-production-order-posting.md).
   * Odchylka účtování. Pro více informací navštivte [Detaily návrhu: Odchylka](design-details-variance.md).
   * Aktualizujte jednotkovou cenu na kartě zboží.

Náklady na zásoby musí být upraveny před odsouhlasením souvisejících položek ocenění s hlavní knihou. Pro více informací navštivte [Detaily návrhu: Odsouhlasení s hlavní knihou](design-details-reconciliation-with-the-general-ledger.md).

## Detekce úpravy

Úkol zjištění, zda má dojít k úpravě nákladů, je primárně prováděn rutinou Deník zboží - Zaúčtovat řádek, zatímco úkol výpočtu a generování položek úpravy nákladů je prováděn dávkovou úlohou **Adjustace nákladů položek zboží**.

Aby bylo možné předávat náklady, detekční mechanismus určuje, které zdroje se změnily v nákladech a do jaké destinace by tyto náklady měly být předány. Následující tři detekční funkce existují v [!INCLUDE[prod_short](includes/prod_short.md)]:

* Položka vyrovnání zboží
* Vstupní bod úpravy Průměrných nákladů
* Úroveň objednávky

### Položka vyrovnání zboží

Tato detekční funkce se používá pro zboží, které používá metody FIFO, LIFO, Standardní a Specifické metody ocenění a pro scénáře pevného vyrovnání. Funkce funguje následovně:

* Úprava nákladů je zjištěna tak, že zdrojové položky zboží označíte jako *Vyrovnaná položka k adjustaci*, aby se náklady upravili kdykoli je zaúčtována položka zboží nebo položka ocenění.
* Náklady jsou předány podle nákladových řetězců, které jsou zaznamenány v tabulce **Položka vyrovnání zboží**.

### Vstupní bod úpravy Průměrných nákladů

Tato detekční funkce se používá pro zboží, které používá průměrnú metodu ocenění. Funkce funguje následovně:

* Úprava nákladů je zjištěna označením záznamu v tabulce **Místo  zadání úpravy  průměrné ceny** tvždy, když je zaúčtována položka ocenění.
* Náklady jsou předány použitím nákladů na položkách ocenění s pozdějším datem ocenění.

### Úroveň objednávky

Tato detekční funkce se používá ve scénářích převodu, výroby a montáže. Funkce funguje následovně:

* Úprava nákladů je zjištěna označením objednávky při každém zaúčtování materiálu/zdroje jako spotřebovaného/použitého.
* Náklady se přeposílají uplatněním nákladů z materiálu/zdroje na výstupní položky spojené se stejnou objednávkou.

Funkce Úroveň objednávky se používá k detekci úprav při zaúčtování montáže. Následující obrázek ukazuje strukturu vstupu úpravy:

![Tok položek v úpravě nákladů](media/design_details_assembly_posting_3.png "Tok položek v úpravě nákladů")

Pro více informací navštivte [Podrobnosti návrhu: Účtování montážní zakázky](design-details-assembly-order-posting.md).

## Ruční versus automatická úprava nákladů

Úpravu nákladů lze provést dvěma způsoby:

* Ručně spuštěním dávkové úlohy **Adjustace nákladů položek zboží**. Tuto dávkovou úlohu můžete spustit buď pro všechno zboží, nebo pouze pro určité zboží nebo kategorii zboží. Tato dávková úloha spustí úpravu nákladů pro zboží v zásobách, pro které byla provedena příchozí transakce, například nákup. U zboží, které používá metodu průměrného ocenění, dávková úloha také provede úpravu, pokud jsou vytvořeny nějaké odchozí transakce.
* Automaticky, úpravou nákladů pokaždé, když zaúčtujete transakci zásob a po dokončení výrobní zakázky. Úprava nákladů se provádí pouze u konkrétního zboží nebo u zboží ovlivněného účtováním. Tato možnost se nastaví, když zaškrtnete políčko **Automatická adjustace nákladů** na stránce **Nastavení zásob**.

Je vhodné spustit úpravu nákladů automaticky při zaúčtování, protože jednotkové náklady jsou častěji aktualizovány, a proto jsou přesnější. Nevýhodou je, že výkon databáze tak může být ovlivněn častým spuštěním úpravy nákladů.

Vzhledem k tomu, že je důležité udržovat pořizovací cenu zboží aktuální, doporučujeme spustit dávkovou úlohu **Adjustace nákladů položek zboží** co nejčastěji během nepracovní doby. Případně použijte automatickou úpravu nákladů. Tím je zajištěno, že pořizovací cena je pro zboží denně aktualizována.

Bez ohledu na to, zda úpravu nákladů provádíte ručně nebo automaticky, je proces úpravy a její důsledky stejný. [!INCLUDE[prod_short](includes/prod_short.md)] vypočítá hodnotu vstupní transakce a předá náklady na všechny odchozí transakce, jako jsou prodeje nebo spotřeby, které byly použity pro vstupní transakci. Úprava nákladů vytvoří položky ocenění, které obsahují částky úprav a částky, které kompenzují zaokrouhlení.

Nové úpravy a zaokrouhlování hodnot mají datum zaúčtování související faktury. Výjimkou jsou případy, kdy položky ocenění spadají do uzavřeného účetního období nebo období zásob nebo pokud je zúčtovací datum dřívější než datum v poli **Povolit účto od** na stránce **Nastavení financí**. Pokud k tomu dojde, přiřadí dávková úloha datum zaúčtování jako první datum následujícího otevřeného období.

## Dávková úloha Úprava nákladů - položky zboží

Když spustíte dávkovou úlohu **Adjustace nákladů položek zboží** máte možnost spustit dávkovou úlohu pro všechno zboží nebo pouze pro určité zboží nebo kategorie.

> [!NOTE]  
> Doporučujeme vždy spustit dávkovou úlohu pro všechno zboží a použít možnost filtrování pouze ke snížení doby běhu dávkové úlohy nebo k opravě nákladů na určitém zboží.

### Příklad

Následující příklad ukazuje, zda zaúčtujete nakoupené zboží jako přijaté a fakturované dne 1.1.2020. Později zaúčtujete prodané zboží jako dodané a fakturované dne 15.1.2020. Potom spusťte dávkové úlohy **Adjustace nákladů položek zboží** a **Účtování nákladů na zboží**. Budou vytvořeny následující položky.

#### Položky ocenění (1)

| Zúčtovací datum | Typ položky zboží | Částka nákladů (skutečná) | Zaúčtované náklady | Fakturované množství | Číslo položky |
|------------|----------------------|--------------------|------------------|-----------------|---------|  
| 1.1.2020 | Nákup | 10,00 | 10,00 | 1 | 1 |
| 15.1.2020 | Prodej | -10,00 | -10,00 | -1 | 2 |

#### Vazba položek v tabulce Vazba věcná pol. - pol. zboží (1)

| Číslo věcné položky | Č. položky ocenění | Číslo finančního žurnálu |
|-------------|---------------|----------------|  
| 1 | 1 | 1 |
| 2 | 1 | 1 |
| 3 | 2 | 1 |
| 4 | 2 | 1 |

#### Věcné položky (1)

| Zúčtovací datum | Finanční účet | Číslo účtu (En-US Demo) | Částka | Číslo položky |
|------------------|------------------|---------------------------------|------------|---------------|  
| 1.1.2020 | [Účet zásob] | 2130 | 10,00 | 1 |
| 1.1.2020 | [Účet použitých přímých nákl.] | 7291 | -10,00 | 2 |
| 15.1.2020 | [Účet zásob] | 2130 | -10,00 | 3 |
| 15.1.2020 | [Účet nákladů na prod.zboží] | 7290 | 10,00 | 4 |

Později účtujete související poplatek za nákupené zboží za 2,00 CZK fakturovaný dne 10.2.2020. Spusťte dávkovou úlohu **Adjustace nákladů položek zboží** a potom spusťte dávkovou úlohu **Účtování nákladů na zboží**. Dávková úloha Adjustace nákladů odpovídajícím způsobem upraví náklady prodeje o -2,00 CZK a dávková úloha **Účtování nákladů na zboží** zaúčtuje nové položky ocenění do hlavní knihy. Výsledek je následující.

#### Položky ocenění (2)

| Zúčtovací datum | Typ položky zboží | Částka nákladů (skutečná) | Zaúčtované náklady | Fakturované množství | Adjustace | Číslo položky |
|------------|----------------------|--------------------|------------------|-----------------|----------|---------|  
| 10.2.2020 | Nákup | 2,00 | 2,00 | 0 | Ne | 3 |
| 15.1.2020 | Prodej | -2,00 | -2,00 | 0 | Ano | 4 |

#### Vazba položek v tabulce Vazba věcná pol. - pol. zboží (2)

| Číslo věcné položky | Č. položky ocenění | Číslo finančního žurnálu |
|-------------|---------------|----------------|  
| 5 | 3 | 2 |
| 6 | 3 | 2 |
| 7 | 4 | 2 |
| 8 | 4 | 2 |

#### Věcné položky (2)

| Zúčtovací datum | Finanční účet | Číslo účtu (En-US Demo) | Částka | Číslo položky |
|------------|-----------|------------------------|------|---------|  
| 10.2.2020 | [Účet zásob] | 2130 | 2,00 | 5 |
| 10.2.2020 | [Účet použitých přímých nákl.] | 7291 | -2,00 | 6 |
| 15.1.2020 | [Účet zásob] | 2130 | -2,00 | 7 |
| 15.1.2020 | [Účet nákladů na prod.zboží] | 7290 | 2,00 | 8 |

## Automatická adjustace nákladů

Chcete-li nastavit automatickou úpravu nákladů při zaúčtování skladové transakce, použijte pole **Automatická adjustace nákladů** fna stránce **Nastavení zásob**. Toto pole umožňuje vybrat, jak daleko v čase od aktuálního pracovního data chcete provést automatickou úpravu nákladů. Existují následující možnosti.

| Možnost | Popis |
|------|-----------|
| Nikdy | Náklady se při zaúčtování neupravily. |
| Den | Náklady jsou upraveny, pokud dojde k zaúčování v rozmezí jednoho dne od pracovního data. |
| Týden | Náklady jsou upraveny, pokud dojde k zaúčtování v rozmezí jednoho týdne od pracovního data. |
| Měsíc | Náklady jsou upraveny, pokud dojde k zaúčtování v rozmezí jednoho měsíce od pracovního data. |
| Čtvrtletí | Náklady jsou upraveny, pokud dojde k zaúčtování v rozmezí jednoho čtvrtletí od pracovního data. |
| Rok | Náklady jsou upraveny, pokud dojde k zaúčtování v rozmezí jednoho roku od pracovního data. |
| Vždy | Náklady jsou vždy upraveny při zaúčtování bez ohledu na zúčtovací datum. |

Výběr provedený v poli **Automatická adjustace nákladů**, je důležitý pro výkon a přesnost vašich nákladů. Kratší časová období, například **Den** nebo **Týden**, ovlivňují výkon systému méně, protože poskytují přísnější požadavek, aby bylo možné automaticky upravit pouze náklady zaúčtované v posledním dni nebo týdnu. To znamená, že automatická úprava nákladů neprobíhá tak často, a proto méně ovlivňuje výkon systému. Znamená to však také, že pořizovací ceny mohou být méně přesné.

### Příklad

Následující příklad ukazuje scénář automatické úpravy nákladů:

* Dne 10. ledna zaúčtujete zakoupenou položku jako přijatou a fakturovanou.
* Dne 15. ledna zaúčtujete prodejní objednávku pro zboží jako dodanou a fakturovanou.
* Dne 5. února obdržíte fakturu za poplatek za dopravu při původním nákupu. Zaúčtujete tento poplatek za dopravu a použijete jej na původní nákupní fakturu, což zvyšuje náklady na původní nákup.

Pokud jste nastavili automatickou úpravu nákladů tak, aby se vztahovala na zaúčtování, která proběhnou do měsíce nebo čtvrtletí od aktuálního data práce, pak automatická úprava nákladů proběhne a předá cenu nákupu do prodeje.

Pokud jste nastavili automatickou úpravu nákladů tak, aby se vztahovala na účtování, ke kterému dojde během jednoho dne nebo týdne od aktuálního pracovního data, automatická úprava nákladů se nespustí a náklady na nákup nebudou předány do prodeje, dokud nespustíte dávkovou úlohu **Adjustace nákladů položek zboží**.

## Viz také

[Úprava nákladu zboží](inventory-how-adjust-item-costs.md)    
[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)    
[Detaily návrhu: Odsouhlasení s hlavní knihou](design-details-reconciliation-with-the-general-ledger.md)    
[Detaily návrhu: Účtování zásob](design-details-inventory-posting.md)    
[Detaily návrhu: Odchylka](design-details-variance.md)    
[Podrobnosti návrhu: Účtování montážní zakázky](design-details-assembly-order-posting.md)    
[Detaily návrhu: Účtování prodejní zakázky](design-details-production-order-posting.md)    
[Správa nákladů zásob](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]