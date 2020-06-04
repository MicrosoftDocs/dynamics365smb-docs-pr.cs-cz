---
title: Set Up and Report Intrastat| Microsoft Docs
description: Learn how to set up Intrastat reporting features, and how to report trade with companies in other EU countries.
services: project-madeira
documentationcenter: ''
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.date: 01/13/2020
ms.author: bholtorf

---
# Nastavení a hlášení Intrastatu
Všechny společnosti v Evropské unii musí hlásit svůj obchod s ostatními zeměmi nebo oblastmi EU. Pohyb zboží musíte nahlásit statistickým úřadům ve vaší zemi / regionu každý měsíc a zpráva musí být doručena daňovým úřadům. Toto se nazývá hlášení Intrastatu. Pomocí stránky **Deníky Intrastat** můžete dokončit pravidelné hlášení Intrastat.

## Povinné a volitelné nastavení
Před použitím deníku Intrastat k vykazování informací o intrastatu je třeba nastavit několik věcí:

* **Nastavení Intrastat**: Stránka Nastavení Intrastatu se používá k povolení hlášení intrastatu a nastavení výchozích hodnot pro něj. Můžete určit, zda chcete nahlásit Intrastat ze dodávek (odchozí), příjemek (příchozí) nebo obojí v závislosti na prahových hodnotách stanovených místními předpisy. Můžete také nastavit výchozí typy transakcí pro běžné doklady a doklady vratky, které se používají podle povahy vykazování transakcí.
* **Šablony deníků Intrastat**: Je nutné nastavit šablony deníku Intrastat, které budete používat. Protože je Intrastat hlášen měsíčně, musíte vytvořit 12 deníků založených na stejné šabloně.
* **Kódy komodity**: Celní a daňové orgány zavedly číselné kódy, které klasifikují položky a služby. Tyto kódy zadáte u zboží.
* **Typy transkací**: Země a oblasti mají různé kódy pro typy transakcí Intrastat, jako je běžný nákup a prodej, výměna vráceného zboží a výměna nevráceného zboží. Nastavte všechny kódy, které platí pro vaši zemi nebo oblast. Tyto kódy se používají v prodejních a nákupních dokladech a při zpracování vratek.
* **Typy přepravy**: Existuje sedm jednomístných kódů pro metody přepravy Intrastatu. **1** po moři, **2** po železnici, **3** po silnici, **4** letecky, **5** poštou, **7** pevné instalace, a **9** vlastní doprava (například, doprava vlasním vozem). [!INCLUDE[d365fin](includes/d365fin_md.md)] tyto kódy nevyžaduje, doporučujeme však, aby popisy poskytovaly podobný význam.

Volitelně můžete také nastavit:

* **Specifikace transakcí**: Pomocí nich můžete doplnit popisy typů transakcí.
* **Oblasti**: Slouží k doplnění informací o zemích a regionech.
* **Místa přechodu**: Pomocí nich můžete určit místa, kam odesíláte nebo přijímáte zboží do nebo z jiných zemí. Letiště Heathrow je příkladem vstupního nebo výstupního bodu. Vstupní nebo výstupní body zadáte na prodejní a nákupní doklady na záložce s náhledem **Zahraniční obchod**. Tyto informace budou také zkopírovány z položek zboží při vytváření deníku Intrastatu.

### Nastavení šablon a listů Intrastat
Dávkové úlohy Intrastat obsahují pouze položky zboží, nikoli finanční položky. Pokud máte položky hlavní knihy, které splňují podmínky pro hlášení Intrastat, musíte je zadat ručně. Pokud například kupujete počítač z jiné země nebo oblasti EU, počítač není uskladněn, ale je zaúčtován přímo na účet hlavní knihy. Tento typ záznamu musíte ručně zadat do deníku Intrastatu.

Položky můžete exportovat do souboru, který můžete odeslat orgánům Intrastatu. Můžete také vytisknout zprávu, ručně zadat informace do formulářů od svých úřadů a poté tyto informace odeslat.

> [!Note]
> Doporučujeme nastavit dávkovou úlohu instrastatu každý měsíc..

1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Šablony deníků Intrastat** a vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Vytvořte šablonu pro každý formulář Intrastat.
3. Chcete-li vytvořit Listy, vyberte akci **Listy**.
4. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]. Vytvořte šablonu pro každý formulář Intrastat, který používáte.

> [!Note]
> Do pole **Statistické období** zadejte období jako čtyř místné číslo, kde první dvě čísla reprezentují rok a ostatní dvě měsíc. Zadejte například hodnotu 1706 pro červen 2017.

### Nastavení čísel sazebníku
Všechny zboží, které nakupujete nebo prodáváte, musí mít kód komodity.

1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Čísla sazebníku** a vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Pro přiřazení komodity ke zboží, bežte na **kartu zboží**, zobrazte celou záložku **Cena a Účtování**, a vyberte kód v poli **Číslo sazebníku**.

### Nastavení typů transkací
1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Typy transkací** a vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!Tip]
> Pokud často používáte určitý kód povahy transakce, můžete jej nastavit jako výchozí. Chcete-li to provést, přejděte na stránku **Nastavení Intrastatu** a vyberte kód.

### Nastavení typů přepravy
1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Typy transakcí** a vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Nastavení povinných polí v sestavě Intrastatu
V některých zemích, například ve Španělsku a Velké Británii, úřady požadují, aby zprávy Intrastatu zahrnovaly například způsob přepravy nákupů nebo nějaké jiné hodnoty, pokud prodej přesáhne určitou hranici. Na stránce **Nastavení Intrastatu**, můžete vybrat nastavení **Nastavení Intrastat Checkist** a nastavit povinná pole na stránce **Deníku Intrastatu**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení Intrastat** a vybrat související odkaz.
2. Vybere tlačítko **Nastavení Intrastat checklist**.
3. Na stránce **Nastavení Intrastat Checklist** klikněte na pole **Název pole** a vyberte pole sestavy Intrastat, které chcete nastavit jako povinné.

## Hlášení Intrastat
Po vyplnění deníku Intrastat můžete spustit  **Kontrolní seznam** a ujistit se, že jsou všechny informace v deníku správné. Povinná pole, která jste nastavili v nastavení **Intrastat kontrolní seznamu**, která nevykazují hodnoty, se zobrazí v poli Chyby a upozornění na stránce **Deník Intrastat**. Poté můžete vytisknout výkaz Intrastat jako formulář nebo vytvořit soubor, který odešlete finančnímu úřadu ve vaší zemi / regionu.

### Vyplnění deníků Intrastat
1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Deníky Intrastat** a vyberte související odkaz.
2. Na stránce **Deníky Intrastat**, v poli **Název listu**, vyberte příslušný list a stiskněte **OK**.
3. Klidněte na tlačítko **navrhnout řádky**. Pole **Počáteční** a **Koncové** datum již budou obsahovat data zadaná pro statistické období v listu deníku.
4. V poli **Nepřímé náklady %**, můžete zadat procento pro pokrytí dopravy a pojištění. Pokud zadáte procento, je obsah pole **Statistická hodnota** v deníku úměrně vyšší.
5. Zvolte **OK** pro spuštění dávkové úlohy.

Dávková úloha načte všechny položky zboží v období statistiky a vloží je jako řádky do deníku Intrastat. V případě potřeby můžete řádky upravit.

> [!IMPORTANT]  
> Dávková úloha načte pouze položky, které obsahují kód země/oblasti, pro který byl zadán kód Intrastat na stránce **Země/Oblasti**. Proto je nutné zadat kódy Intrastat pro kódy zemí nebo oblastí, pro které budete dávkovou úlohu spouštět.

### Hlášení Intrastatu ve formuláři nebo souboru
Chcete-li získat informace, které jsou požadovány ve formuláři Intrastat od statistických úřadů, musíte vytisknout sestavu **Intrastat - Form**. Než to budete moci provést, musíte připravit deník Intrastat a vyplnit jej. Pokud máte jak prodejní, tak nákupní transakce, musíte pro každý typ vyplnit samostatný formulář, takže musíte sestavu vytisknout dvakrát.

1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Deníky Intrastat** a vyberte související odkaz.
2. Na stránce **Deníky Intrastat** vyberte příslušnou list deníku v poli **Název listu**.
3. Pokud jste tak ještě neučinili, vyplňte deník ručně nebo zvolte **Navrhnout řádky**.
4. Zvolte **Tisk deníku Intrastat**
5. V záložce **Řádek deníku Intrastat**, přijdete filtr **Typ** a potom určete, zda se jedná o **Příjemku** nebo **Dodávku**.
6. Zvolte **Tisk...** k tisku sestavy.

### Vykazování Intrastat do souboru
Hlášení Intrastatu můžete také odeslat jako datový soubor. Před vytvořením souboru si můžete vytisknout kontrolní seznam, který obsahuje stejné informace, jaké budou v souboru.

1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Deníky Intrastat** a vyberte související odkaz.
2. Na stránce **Deníky Intrastat** vyberte příslušný list deníku v poli **Název listu**.
3. Pokud jste tak ještě neučinili, vyplňte deník ručně nebo zvolte **Navrhnout řádky**.
4. Klidněte na tlačítko **Vytvořit soubor...**.
5. Na stránce úlohy, zvolte **OK**.
6. Vyberte **Uložit**.
7. Vyhledejte umístění, kam chcete soubor uložit, zadejte název souboru a vyberte **Uložit**.

## Reorganizace deníků Intrastatu
Vzhledem k tomu, že musíte odeslat sestavu Intrastat každý měsíc a vytvořit nový list deníku pro každou sestavu, budete mít nakonec mnoho listů deníku. Řádky deníku nejsou automaticky odstraněny. Možná budete chtít periodicky reorganizovat názvy dávek deníku. To provést odstraněním listů deníků, které již nepotřebujete. Řádky deníku v těchto dávkách jsou také odstraněny.

1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Deníky Intrastat** a vyberte související odkaz.
2. Chcete-li zobrazit možnosti, vyberte pole **Název listu**.
3. Vyberte listy deníku, které chcete odstranit, a poté zvolte tlačítko **Odstranit**.

## Viz související školení v programu [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index)

## Viz také
[Správa financí](finance.md)
