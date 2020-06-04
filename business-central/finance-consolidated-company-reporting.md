---
title: Consolidate Data from Multiple Companies | Microsoft Docs
description: Get an summary view of the financial health accross your businesses.
documentationcenter: ''
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 10/01/2019
ms.author: bholtorf

---

# Konsolidování finančních dat z několika společností
Pokud máte více než jednu společnost v [!INCLUDE[d365fin](includes/d365fin_md.md)], může vám zpráva o konsolidovaném zkušebním zůstatku v centru rolí Účetní poskytnout přehled o finančním zdraví celého vašeho podnikání.

Sestava kombinuje položky hlavní knihy z každé z vašich společností v nové společnosti, kterou vytvoříte, aby obsahovala konsolidovaná data. Tato společnost se obvykle označuje jako "konsolidovaná společnost". Konsolidovaná společnost je pouze kontejner pro konsolidovaná data a nemá žádná živá obchodní data. Společnosti, které zahrnete do konsolidované společnosti, se stanou **Účetními jednotkami** v sestavě.

Konsolidace finančních údajů může být důležitá zejména v souvislosti s vnitropodnikovými procesy. Pro více informací navštivte [Správa vnitropodnikových transakcí](intercompany-manage.md).

Můžete konsolidovat:

* Napříč společnostmi, které mají různé účetní osnovy.
* Společnosti, které používají různé fiskální roky a různé měny.
* Celú částku nebo procento finančních informací společnosti.
* Použití různých směnných kurzů na jednotlivých finančních účtech.

V závislosti na složitosti vašich podniků existují dva způsoby nastavení sestavy:

* Pokud nepotřebujete pokročilá nastavení, jako je například zahrnutí společnosti, ve které vlastníte pouze část, můžete pomocí průvodce **Konsolidace společnosti** rychle nastavit konsolidaci. Průvodce vám pomůže projít základní kroky.
* Pokud potřebujete pokročilejší nastavení, můžete si sami nastavit konsolidovanou společnost a účetní jednotky.

## Jednoduché nastavení konsolidace
Pokud je vaše konsolidace přímá, například proto, že zcela vlastníte účetní jednotky, které chcete konsolidovat, pomůže vám průvodce nastavením **Konsolidace společnosti** pomocí následujících kroků:

* Zvolte, zda chcete vytvořit novou konsolidovanou společnost nebo zda chcete konsolidovat data ve společnosti, kterou jste již pro konsolidaci vytvořili. Společnost by neměla obsahovat transakce.
* Prohlédněte si náhled výsledků. [!INCLUDE[d365fin](includes/d365fin_md.md)] ověřuje, že hlavní data a transakce lze úspěšně převést do konsolidované společnosti.

Chcete-li použít průvodce asistovaným nastavením, postupujte takto:

1. V Centre rolí **Účetní** vyberte akci **Asistované nastavení**.
2. Zvolte **Nastavit vykazování konsolidace** a pak dokončete každý krok v průvodci asistovaným nastavením.

## Postup nastavení rozšířené konsolidace
Pokud pro svou konsolidaci potřebujete pokročilejší nastavení, můžete konsolidaci nastavit ručně. Máte-li například společnosti, které vlastníte pouze částečně, nebo máte společnosti, které nechcete zahrnout do konsolidace. Konsolidovanou společnost založíte stejným způsobem jako ostatní společnosti. Pro více informací navštivte [Příprava obchodování](ui-get-ready-business.md).

[!INCLUDE[d365fin](includes/d365fin_md.md)] umožňuje nastavit seznam společností pro konsolidaci, ověření účetních dat před jejich konsolidací, import souborů a generování konsolidačních sestav.

1. Přihlaste se do konsolidované společnosti.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní jednotky** a poté vyberte související odkaz.
3. Vyberte **Nový** a vyplňte povinná pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!IMPORTANT]
> Když vyplníte pole **Počáteční datum** a **Koncové datum**, ujistěte se, že dodržujete pravidla GAAP týkající se fiskálních období účetní jednotky proti mateřské společnost.

Pokud vaše účetní jednotka používá cizí měnu, musíte určit směnný kurz, který se použije při konsolidaci. Musíte také zadat informace o konsolidaci finančních účtů účetní jednotky. Tyto procesy jsou popsány v následujících částech.

### Příprava účtů hlavní knihy pro konsolidaci
Pokud se účetní osnova v účetní jednotce liší od konsolidované společnosti, musíte pro konsolidaci připravit účty hlavní knihy. Můžete pro strany MD a Dal určit účty, na které se má účtovat a metodu, která se použije k převodu měn v konsolidované společnosti. To je užitečné například v případě, že sestavu často spouštíte.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
2. Otevřete kartu pro účet a poté vyplňte pole na záložce **Konsolidace**.

### Upřesnění směnných kurzů pro konsolidaci
Pokud účetní jednotka používá jinou měnu než konsolidovaná společnost, musíte před konsolidací zadat metody směnného kurzu pro každý účet. U každého účtu obsah pole **Způsob  převodu konsolidace** určuje směnný kurz. Na každé kartě účetní jednotky v poli **Tabulka směnných kurzů** určete, zda konsolidace použije směnné kurzy z obchodní jednotky nebo konsolidované společnosti. Pokud používáte směnné kurzy od konsolidované společnosti, můžete změnit směnné kurzy pro účetní jednotku. Pokud pro účetní jednotky obsahuje pole **Tabulka směnných kurzů** na kartě účetní jednotky hodnotu **Místní** můžete změnit směnný kurz z karty účetních jednotek. Směnné kurzy jsou zkopírovány z tabulky **Směnný kurz**, ale před konsolidací je můžete změnit.

Následující tabulka popisuje metody směnného kurzu, které můžete použít pro účty.

| Směnné kurzy | Typické použití |
|---|---|
| Průměrný kurz (ručně) | Ručně vypočítáte průměrný kurz za období, které má být konsolidováno. Vypočítejte průměr buď jako aritmetický průměr nebo jako nejlepší odhad a zadejte výsledek pro každou účetní jednotku. Používá se pro účty výsledovky. |
| Uzavírací kurz | Používá se pro rozvahové účty. |
| Poslední uzavírací kurz | Kurz platný na devizovém trhu k datu, ke kterému se sestavuje rozvaha nebo výsledovka. Tenhle kurz zadáváte pro každou účetní jednotku. Používá se pro rozvahové účty. |
| Historický kurz | Směnný kurz platný v době, kdy došlo k transakci. |
| Složený kurz | Částky za běžné období jsou přepočteny průměrným kurzem a připočteny k dříve zaznamenanému zůstatku v konsolidované společnosti. Tato metoda se obvykle používá pro účty nerozděleného zisku, protože zahrnují částky z různých období, a jsou tedy složením částek převedených s různými směnnými kurzy. |
| Kurz cenných papíru | Je to podobné jako **Složený kurz**. Rozdíl je, že se účtuje na samostatné účty hlavní knihy. |

Chcete-li určit směnné kurzy pro účetní jednotky, postupujte takto:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní jednotky** a poté vyberte související odkaz.
2. Na stránce **Přehled účetní jednotky** vyberte účetní jednotku a poté vyberte akci **Průměrný kurz (ručně)**.
3. Na stránce **Změna směnného kurzu** byl obsah pole **Částka vztažného  sm.kurzu** zkopírován z tabulky **Směnný kurz**, ale můžete ho upravit. Zavřete stránku.
4. Vyberte akci **Uzavírací kurz**.
5. Do pole **Částka vztažného  sm.kurzu** zadejte směnný kurz.

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### Vyloučení společnosti z konsolidace
Pokud nechcete zahrnout účetní jednotku do konsolidace, můžete ji vyloučit. Chcete-li to provést, přejděte na kartu účetní jednotky a zrušte zaškrtnutí políčka **Konsolidovat**.

### Zahrnutí částečně vlastněné společnosti do konsolidace
Pokud vlastníte pouze část společnosti, můžete zahrnout procento každé transakce, které odpovídá procentu společnosti, kterou vlastníte. Pokud například vlastníte 70 % společnosti, bude konsolidace zahrnovat 70 USD faktury za 100 USD. Chcete-li určit procento společnosti, kterou vlastníte, přejděte na kartu účetní jednotky a zadejte procento do pole **Konsolidace %**.

### Testování dat před konsolidací
Data můžete před přenosem do konsolidované společnosti otestovat. [!INCLUDE[d365fin](includes/d365fin_md.md)] hledá rozdíly v informacích v účetních jednotkách a konsolidované společnosti. Například zda se čísla účtů nebo kódy dimenzí liší. Před spuštěním sestavy je nutné opravit chyby. Databázi můžete otestovat nebo, pokud importujete data ze souboru XML, můžete otestovat soubor.

1. Otevřete konsolidovanou společnost.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní jednotky** a poté vyberte související odkaz.
3. Proveďte jeden z následujících úkonů:

   * Chcete-li testovat soubor, vyberte akci **Test souboru**,  zadejte název souboru, který chcete testovat, a poté vyberte **Tisk**.
   * Chcete-li testovat databázi, vyberte **Test databáze**.

## Spuštění konsolidace
Po otestování dat je můžete přenést do konsolidované společnosti.

1. Přihlaste se do konsolidované společnosti.
2. V **Centru rolí Účetní** vyberte akci **Spustit konsolidaci**.
3. Vyplňte povinná pole.
4. V poli **Kde** vyberte **Název společnosti** a poté vyberte konsolidovanou společnost v poli **je**.

## Odstranění opakovaných transakcí
Po konsolidaci všech společností musíte najít všechny transakce, které jsou zaznamenány více než jednou mezi společnostmi, a potom zaúčtovat položky eliminace, abyste je odstranili.

Zpracování eliminace konsolidace je manuální proces. Můžete postupovat takto:
1. Najděte transakce, které je potenciálně nutné upravit, a zadejte řádky finančního deníku, abyste je odstranili.
2. Spusťte sestavu **Eliminace fin. konsolidace**, která vám pomůže posoudit účinek řádků finančního deníku před účtováním.
3. Zaúčtujte vyrovnávací transakce.

Sestava **Eliminace fin. konsolidace** zobrazuje předběžnou zkušební bilanci, ve které můžete simulovat důsledky eliminace položek porovnáním položek v konsolidované společnosti s vyloučením, která byla zapsána do finančního deníku.

Předtím, než může být účetní jednotka zahrnuta do sestavy, musí být nastavena na stránce **Účetní jednotky** a musí být vybráno pole **Konsolidovat**.

Každý účet se objeví na řádku samostatně podle struktury účetní osnovy. Účet se nezobrazí, pokud jsou všechny částky na řádku 0. Pro každý účet jsou zobrazeny následující informace:

* Číslo účtu.
* Název účtu.
* Pokud jste vybrali jeden nebo více kódů účetních jednotek v poli **Kód účetní jednotky** na stránce požadavku, zobrazí se součet za konsolidovanou společnost bez vybraných účetních jednotek a vyloučení. Pokud jste nevyplnili pole **Kód účetní jednotky**, zobrazí se součet za konsolidovanou společnost bez vyloučení.
* Pokud jste na stránce požadavku vybrali kód účetní jednotky v poli **Kód účetní jednotky**, zobrazí se součet importovaných položek z účetní jednotky. Pokud jste nevyplnili pole **Kód účetní jednotky**, zobrazí se celkový počet zaúčtovaných eliminací v konsolidované společnosti.
* Součet pro konsolidovanou společnost se všemi účetními jednotkami a všemi zaúčtovanými eliminacemi.
* Eliminace, které mají být provedeny v konsolidované společnosti, to znamená položky ve finančním deníku, které jsou vybrány na stránce požadavku.
* Zaúčtování textu zkopírovaného z finančního deníku.
* Konsolidovaná společnost po eliminaci, pokud je zaúčtována.


## Export a import konsolidovaných dat mezi databázemi
Pokud jsou data pro účetní jednotku v jiné databázi, musíte je exportovat do souboru, než je můžete zahrnout do konsolidace. Každá společnost musí být exportována samostatně. Za tímto účelem použijte dávkovou úlohu **Export konsolidace**.

Po spuštění dávkové úlohy jsou zpracovány všechny položky v účtech hlavní knihy. Pro každou kombinaci vybraných dimenzí a dat se obsah polí **Částka** sčítá a exportuje. Zpracovává se další kombinace vybraných dimenzí a dat se stejným číslem účtu, poté se zpracují kombinace v dalším čísle účtu atd.

Exportované položky obsahují následující pole: **Číslo účtu**, **Zúčtovací datum** a **Částka**. Pokud byly exportovány také informace o dimenzích, jsou zahrnuty také kódy dimenzí a hodnoty dimenzí.

1. Pokud je pro každý exportovaný řádek součet polí **Částka** MD, číslo účtu, které je nastaveno v poli účetní jednotky **Kons.  účet MD** je exportováno na řádek. Pokud je součet na straně Dal, odpovídající číslo v poli **Kons.  účet Dal** je exportováno na řádek.
2. Datum použitý pro každý exportovaný řádek je buď datum ukončení období, nebo, pokud dojde k převodu každý den, přesné datum výpočtu.
3. Hodnota dimenze exportovaná pro položku bude konsolidovaná hodnota dimenze společnosti, která je nastavena v poli **Kód konsolidace** pro tuto hodnotu dimenze. Pokud nebyla do pole **Kód konsolidace** pro tuto hodnotu dimenze zadána žádná konsolidovaná hodnota dimenze společnosti, bude hodnota dimenze exportována do řádku.
4. Soubory XML také obsahují směnné kurzy měn v konsolidačním období. Tyto sazby jsou zahrnuty v samostatné části na začátku souboru.

## Viz také
[Správa vnitropodnikových transakcí](intercompany-manage.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Export vašich obchodních dat do Excelu](about-export-data.md)
