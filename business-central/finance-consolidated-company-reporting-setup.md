---
title: Set up company consolidation
description: Learn how you can configure how data from different companies in Business Central is reported into a consolidation company.
author: brentholtorf


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.search.form: 1826, 1827
ms.date: 03/20/2023
ms.author: bholtorf

---

# Nastavení konsolidace společnosti

Před konsolidací věcných položek dvou nebo více samostatných společností (dceřiných společností) do konsolidované společnosti je nutné připravit účtovou osnovu a konsolidační společnost.

V závislosti na složitosti vašeho podnikání existují dva způsoby, jak nastavit konsolidaci:

* Pokud nepotřebujete upřesňující nastavení, například zahrnutí společnosti, jejíž součást vlastníte pouze část, můžete pomocí průvodce asistovaným nastavením **Konsolidace společnosti** rychle nastavit konsolidaci. Průvodce vám pomůže projít základními kroky.
* Pokud potřebujete pokročilejší nastavení, můžete konsolidovanou společnost a účetní jednotky nastavit sami.
   * V každé účetní jednotce určete, které účty hlavní knihy mají být zahrnuty do konsolidace, a určete metodu převodu konsolidace pro každý účet.
   * V konsolidační společnosti nastavte pro každou společnost, která má být zahrnuta do konsolidace, kartu účetní jednotky. Karta účetní jednotky obsahuje informace, například data fiskálního roku účetní jednotky a procento každého účtu, který musí být zahrnut do konsolidace.

## Jednoduché nastavení konsolidace

[!INCLUDE [2021_releasewave1](includes/2021_releasewave1.md)]
Pokud je vaše konsolidace přímočará, například proto, že jste úplným vlastníkem účetních jednotek určených ke konsolidaci, průvodce nastavením s asistencí **Konsolidace společnosti** vám pomůže projít následujícími kroky:

* Zvolte, zda chcete vytvořit novou konsolidovanou společnost nebo zda chcete konsolidovat data ve společnosti, kterou jste již vytvořili pro konsolidaci. Společnost by neměla obsahovat transakce.
* Zobrazte náhled výsledků. [!INCLUDE[prod_short](includes/prod_short.md)] ověřuje, že kmenová data a transakce mohou být úspěšně převedeny do konsolidované společnosti.

Chcete-li použít průvodce asistovaným nastavením, postupujte takto:

1. V Centru rolí **Účetní** vyberte akci **Asistované nastavení**.
2. Zvolte **Nastavit vykazování konsolidace** a pak dokončete každý krok v průvodci asistovaným nastavením.

## Pokročilé nastavení konsolidace

Pokud potřebujete pokročilejší nastavení pro konsolidaci, můžete konsolidaci nastavit ručně. Například pokud máte společnosti, které vlastníte pouze částečně, nebo máte společnosti, které nechcete zahrnout do konsolidace.

### Založení konsolidované společnosti

Nejprve musíte založit konsolidovanou společnost. Konsolidovanou společnost nastavíte stejným způsobem jako jiné společnosti. Pro více infomací běžte na [Příprava na podnikání](ui-get-ready-business.md).

Následující seznam znázorňuje klíčové aspekty konsolidované společnosti.

1. Nastavení účetní osnovy

   Pro více informací navštivte [Nastavení nebo změna účetní osnovy](finance-setup-chart-accounts.md).

   Účetní osnovy můžou být stejné v rámci účetní jednotky a konsolidované společnosti nebo konsolidovaná společnost může mít jinou účetní osnovu. Pokud se účetní osnova organizační jednotky liší od účtové osnovy konsolidované společnosti, je nutné zadat mapování mezi účty na účtech v účetní jednotce. Další informace naleznete v části [Příprava účtů hlavní knihy na konsolidaci](#glacc).

2. Přidání účetních jednotek

   Chcete-li konsolidovat finanční data několika společností do konsolidované společnosti, musíte zadat informace o dceřiné společnosti jako účetní jednotky, které mají být zahrnuty, a o tom, do jaké míry budou zahrnuty jejich údaje.

   Další informace naleznete v části [Přidání účetních jednotek](#busunit).
3. Při konsolidaci účetní závěrky účetních jednotek můžete určit směnné kurzy, pokud je účetní závěrka v cizí měně.

   Používají se tři směnné kurzy **Průměrný kurz (ručně)**, **Uzavírací kurz** a **Poslední uzavírací kurz**. Další informace naleznete v části [Určení směnných kurzů pro konsolidace](#exchrates).
4. Můžete konsolidovat informace o dimenzích a finanční účty.

   Další informace naleznete v části [Zahrnutí nebo vyloučení dimenzí](#dim).

### <a name="busunit"></a> Přidání účetních jednotek

[!INCLUDE[prod_short](includes/prod_short.md)] umožňuje nastavit seznam účetních jednotek ke konsolidaci, ověřit účetní data před jejich konsolidací, importovat soubory a generovat konsolidační sestavy.

1. Přihlaste se ke konsolidované společnosti.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Účetní jednotky** a poté vyberte související odkaz.
3. Zvolte **Nový** a vyplňte požadovaná pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!DŮLEŽITÉ]
   > Když vyplníte pole **Počáteční datum** a **Koncové datum**, ujistěte se, že dodržujete pravidla GAAP týkající se fiskálních období účetní jednotky oproti mateřské společnosti.
4. Opakujte krok 3 pro každou další účetní jednotku

Pokud vaše účetní jednotka používá cizí měnu, musíte určit směnný kurz, který se má použít při konsolidaci. Musíte také zadat konsolidační informace o finančních účtech účetní jednotky. Tyto procesy jsou popsány v následujících částech.

### <a name="glacc"></a> Příprava finančních účtů pro konsolidaci

Účetní osnova společnosti, která bude konsolidována, musí specifikovat účty pro konsolidaci. Pro každý zaúčtovaný finanční účet v každé společnosti musíte zadat finanční účet v konsolidované společnosti, na který bude zůstatek převeden při konsolidaci. Jedná se o mapování, které umožní konsolidaci společností s různou účetní osnovou.

Pokud se účtová osnova v účetní jednotce liší od konsolidované společnosti, musíte připravit finanční účty pro konsolidaci. Můžete určit účty, na které se mají účtovat částky MD a částky Dal, a metodu, která se použije k převodu měn v konsolidované společnosti. To je užitečné například v případě, že sestavu často spouštíte.

1. V každé obchodní jednotce [!INCLUDE [prod_short](includes/prod_short.md)] vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Účetní osnova**a poté vyberte související odkaz.
2. Otevřete kartu pro účet a vyplňte pole na pevné záložce **Konsolidace**. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="exchrates"></a> Určení směnných kurzů pro konsolidace

Pokud účetní jednotka používá jinou měnu než konsolidovaná společnost, je nutné před konsolidací zadat metody směnných kurzů pro každý účet. Pro každý účet obsah pole **Způsob převodu konsolidace** určuje směnný kurz. V konsolidované společnosti na každé kartě účetní jednotky v poli **Tabulka směnných kurzů** určíte, zda bude konsolidace používat směnné kurzy z účetní jednotky nebo konsolidované společnosti. Pokud používáte směnné kurzy konsolidované společnosti, můžete změnit směnné kurzy pro účetní jednotku. Pokud u účetních jednotek pole **Tabulka směnných kurzů** na kartě účetní jednotky obsahuje **Místní**, můžete změnit směnný kurz z karty účetní jednotky. Směnné kurzy jsou zkopírovány z tabulky **Směnný kurz**, ale před konsolidací je můžete změnit.

Následující tabulka popisuje metody směnných kurzů, které lze použít pro účty.

| Směnný kurz | Typické použití |
|---|---|
| Průměrný kurz (ručně) | Ručně vypočítáte průměrnou sazbu pro období konsolidace. Vypočítejte průměr buď jako aritmetický průměr, nebo jako nejlepší odhad, a zadejte výsledek pro každou účetní jednotku. Používá se pro účty výsledovky. |
| Uzavírací kurz | Používá se pro rozvahové účty. |
| Poslední uzavírací kurz | Kurz, který byl platný na devizovém trhu k datu, pro který se sestavuje rozvaha nebo výsledovka. Tuto sazbu zadáte pro každou účetní jednotku. Používá se pro rozvahové účty. |
| Historický kurz | Směnný kurz, který byl platný v době uskutečnění transakce. |
| Složený kurz | Částky za běžné období jsou přepočteny průměrným kurzem a přičteny k dříve zaznamenanému zůstatku v konsolidované společnosti. Tato metoda se obvykle používá pro účty nerozděleného zisku, protože zahrnují částky z různých období, a jsou tedy složeny z částek převedených různými směnnými kurzy. |
| Kurz cenných papírů | To je podobné jako **Kompozitní**. Rozdíly jsou zaúčtovány do samostatných finančních účtů. |

Chcete-li zadat směnné kurzy pro účetní jednotky, postupujte takto:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Účetní jednotky** a poté vyberte související odkaz.
2. Na stránce **Seznam účetních jednotek** vyberte účetní jednotku a poté zvolte akci **Průměrný kurz (ručně)**.
3. Na stránce **Změnit směnný kurz**, je obsah pole **Změna směnného kurzu** zkopírován z tabulky **Směnný kurz**, ale můžete je upravit. Zavřete stránku.
4. Vyberte akci **Uzavírací kurz**.
5. V poli**Částka vztažného sm.kurzu ** zadejte směnný kurz.

### <a name="dim"></a> Zahrnutí nebo vyloučení dimenzí

Můžete konsolidovat informace o dimenzích a finanční účty.

* U příslušných dimenzí zadejte pole **Kód konsolidace** nebo jej ponechte prázdné
   * Chcete-li z konsolidace vyloučit dimenzi, ponechte pole **Kód konsolidace** na dimenzi prázdné a nevybírejte dimenze v polích **Kopie dimenzí** v žádných konsolidačních funkcích nebo sestavách.
   * Chcete-li do konsolidace zahrnout informace o dimenzích, ponechte pole **Kód konsolidace** prázdné. Konsolidace však bude fungovat pouze v případě, že hodnoty dimenzí v účetní jednotce jsou stejné jako v konsolidované společnosti.
   * Chcete-li konsolidovat kód hodnoty dimenze v účetní jednotce s jiným kódem hodnoty dimenze v konsolidované společnosti, vyplňte pole **Kód konsolidace** u příslušných dimenzích.
* Přidání příslušných dimenzí do příslušných finančních účtů

### <a name="exclude"></a>Vyloučení společnosti z konsolidace

Pokud nechcete zahrnout účetní jednotku do konsolidace, můžete ji vyloučit. Chcete-li to provést, přejděte na kartu účetní jednotky a zrušte zaškrtnutí políčka **Konsolidovat**.

### <a name="include"></a>Zahrnout do konsolidace částečně vlastněnou společnost

Pokud vlastníte pouze část společnosti, můžete zahrnout procento každé transakce, které odpovídá procentu společnosti, kterou vlastníte. Pokud například vlastníte 70 % společnosti, konsolidace bude zahrnovat fakturu ve výši 70 USD za 100 USD. Chcete-li zadat procento společnosti, kterou vlastníte, přejděte na kartu účetní jednotky a zadejte procento do pole **Konsolidace %.**

## Viz také

[Konsolidování finančních dat z několika společností](finance-consolidated-company-reporting.md)    
[Správa mezipodnikových transakcí](intercompany-manage.md)    
[Pracovat s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Export vašich obchodních dat do Excelu](about-export-data.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]