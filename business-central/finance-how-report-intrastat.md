---
title: Work with Intrastat reporting
description: Learn how to report trade with companies in other EU countries/regions using the Intrastat system.
author: fcoufal
ms.reviewer: v-pejano
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: electronic document, Intrastat, trade, EU, European Union
ms.search.form: 308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077
ms.date: 01/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---
# Práce s vykazováním Intrastat

Všechny společnosti v Evropské unii (EU) musí ohlašovat svůj obchod s ostatními zeměmi/regiony EU. Pohyb zboží se musí každý měsíc hlásit statistickým úřadům a hlášení se musí doručit finančním úřadům. Intrastat je systém pro sběr statistických údajů o obchodu se zbožím v rámci těchto zemí/regionů. K vyplňování pravidelných výkazů pro Intrastat (obvykle měsíčně), shromažďování, evidenci a vykazování obchodu se zbožím podle právních předpisů místní vlády se používá **Hlášení Intrastat**.

Vykazování Intrastatu vychází ze základních předpisů EU, které platí pro všechny země/regiony, v praxi však existují určité rozdíly v rámci jednotlivých zemí/regionů. Každá země/region má svá pravidla, co přesně a jak se má vykazovat.

> [!IMPORTANT]  
> Tento článek popisuje novou funckionalitu  Intrastatu, která jsou k dispozici v [!INCLUDEprod_short] od druhé vlny vydání 2022, který obsahuje rozšířené funkce a  [musí být zapnuta pro stávající společnosti](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Pro zapnutí a nastavení nové možnosti kontaktujte svého správce.
>
> Přečtěte si článek o nastavení a používání Intrastatu v předchozí verzi na adrese [Nastavení a Vykazování Intrastat](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]  
> Informace Intrastatu se nevztahují na pohyb služeb mezi zeměmi/regiony, ale pouze na pohyb zboží (položek a dlouhodobého majetku). Pokud místní samospráva vyžaduje registraci pohybu služeb mezi zeměmi/regiony, lze ji provést pomocí funkce **Hlášení služeb**.
>
> V současné době očekáváme, že tato funkce bude k dispozici od listopadu 2022 jako aplikace na [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). V té době si ji pro její použití musíte nejprve nainstalovat na stránce **Správa rozšíření**.

## Vyplnění Hlášení Intrastat

1. Zvolte ikonu ![Žárovky která otevře funkci Řekni mi](media/ui-search/search_small.png "Řekněte mi co chcete dělat"), zadejte **Hlášení Intrastat**, a zvolte související odkaz.
2. Zvolte akci **Nový** pro vytvoření nového **Hlášení Intrastat**.
3. Pokud potřebujete zadat podrobnější informace o **Hlášení Intrastat**, vyplňte tyto informace v poli **Popis**.
4. V poli **Statistické období**, zadejte měsíc, za který se mají údaje vykazovat. Období zadejte jako čtyřmístné číslo bez mezer a symbolů. V závislosti na zemi/oblasti zadejte nejprve měsíc a poté rok, nebo naopak. Například pro červen 2022 zadejte buď *2206*, nebo *0622*.
5. Vyberte akci **Návrh řádků**. Pole **Počáteční datum** a **Koncové datum** již budou obsahovat data zadaná pro statistické období v záhlaví výkazu Intrastat.
6. Do pole **Nepřímé náklady %** se může zadat procentní podíl na úhradu dopravy a pojištění. Pokud zadáte procento, obsah pole **Statistická hodnota** v deníku se úměrně zvýší. Pokud však chcete tuto funkci využít, musíte přepnout pole **Částka včetně poplatků za zboží** na hodnotu **Ano**.
7. V části **Další** můžete případně nastavit další konfigurace:
   1. **Přeskočit přepočet pro nulové částky** udává, že řádky bez částek nebudou během dávkové úlohy přepočítány.
   2. **Přeskočit nulové částky** udává , že záznamy v položkách zboží bez částek nebudou zahrnuty do dávkové úlohy..
   3. **Přeskočit nefakturované položky** udává, zda mají být z procesu vyloučeny záznamy z položek zboží, které byly odeslány nebo přijaty, ale ještě nebyly fakturovány.
8. Zvolte **OK** pro spuštění dávkové úlohy.

Dávková úloha načte všechny položky ve statistickém období a vloží je jako řádky do řádků **Hlášení Intrastat**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Úprava výkazu Intrastat

V případě potřeby můžete řádky upravit, ale kdykoli změníte hodnotu v řádku výkazu Intrastat, pole **Oprava** bude automaticky označeno jako **Ano**. Případně můžete přidat nový řádek ručně, pokud k tomu máte důvod. Ruční přidání nového řádku:

1. Na stránce **Hlášení Intrastat**, zvolte akci **Nový řádek**.
2. Zvolte možnost **Příjem** nebo **Dodávku** v poli **Typ**.
3. v poli **Typ původu**, zvolte jednu z následujících možnosti: **Položka zboží**, **Položka DM**, nebo **Položka projektu**.
4. Na základě **Typu původu** v poli **Číslo zboží**, zvolte **Zboží** (v obou případech, **položka zboží** or **položka projektu**) nebo **Dlouhodobý majetek**.
5. Vyplňte ostatní pole dle Vaší potřeby.

> [!NOTE]  
> Při ručním přidání nového řádku do výkazu Intrastat musí být pole **Datum** v řádku uvnitř rozsahu **Statistického období**, který jste přidali v záhlaví.

## Ověření řádků Intrastatu

Po vyplnění hlášení **Intrastat** můžete spustit akci **Kontrolní sestava**, abyste se ujistili, že jsou všechny informace v hlášení **Intrastat** správné. Povinná pole, která jste nastavili na stránce **Kontrolní seznam hlášení Intrastat** a v nichž chybí hodnoty, se zobrazí v poli **Chyby a varování** na stránce **Hlášení Intrastat**.

Spusťte sestavu **Kontrolní sestava** a zkontrolujte řádky Intrastatu před jejich exportem do požadovaného formátu. Kontrola se provádí uvnitř **Hlášení Intrastatu**.

## Přepočet hmotnosti nebo doplňkové měrné jednotky

Pokud se zobrazí chybová zpráva *"Celková hmotnost" v řádku hlášení Intrastat nesmí být prázdná*, je to pravděpodobně proto, že jste u použitého zdroje, položky nebo dlouhodobého majetku nenastavili pole **hmotnost netto**. V takovém případě vyhledejte kartu položky nebo dlouhodobého majetku a doplňte požadovanou hodnotu. Poté stačí znovu otevřít **Hlášení Intrastat** a postupovat podle následujících kroků:

1. Vyberte možnost **Přepočítat hmotnost/doplň. MJ** pro přepočítání **celkové hmotnosti** a/nebo **doplňkových měrných jednotek**.
2. Zvolte jednu z následujících možností:

    1. **Hmotnost** – přepočítat pouze **Celkovou hmotnost** na základě aktuálních informací o **netto hmotnosti** na kartách zboží a dlouhodobého majetku.
    2. **Množství v doplňkové MJ** - přepočet pouze **doplňkových měrných jednotek** na řádku **Hlášení Intrastat**, pokud existuje, na základě aktuálních informací o **Množství v doplňkové MJ** na kartách položky a dlouhodobého majetku.
    3. **Obojí** - přepočet **Celkové hmotnosti** i **Množství v doplňkové MJ** na základě aktuálních údajů na kartách zboží a dlouhodobého majetku.
3. Zvolte **OK** pro spuštění dávkové úlohy.

## Export výkazu Intrastat

Výkaz pro Intrastat můžete předložit jako soubor na základě požadavků úřadů. Před vytvořením souboru byste měli spustit **Kontrolní sestava** a zkontrolovat, zda všechny řádky obsahují všechny potřebné a platné informace. Vytvoření souboru:

1. Zvolte ikonu![Žárovky, která otevře funkci Řekni mi.](media/ui-search/search_small.png "Řekněte mi co chcete dělat"), zadejte **Seznam Hlášení Intrastat**, a poté zvolte související odkaz.
2. Zvolte **Hlášení Intrastat** pokud chcete výkaz exportovat do souboru.
3. Pokud jste tak ještě neučinili, vyplňte **Hlášení Intrastat** ručně nebo zvolte akci **Návrh řádků**.
4. Zvolte akci **Vytvořit soubor**.
5. Soubor s výkazem Intrastat bude uložen v požadovaném formátu.

Jakmile vytvoříte soubor, [!INCLUDE[prod_short](includes/prod_short.md)] budou automaticky vyplněny následující pole.

* **Datum Exportu** stanovuje, kdy byl výkaz exportován.
* **Čas exportu** stanovuje čas, kdy byl výkaz exportován.

> [!NOTE]  
> Při příštím vytvoření souboru budou pole **Datum exportu** a **Čas exportu** uchovávat pouze informace o naposledy vytvořeném souboru.

## Pravidla Intrastatu

### Seskupování řádků

V řádcích **Hlášení Intrastat** není žádné seskupení podle polí. Všechny záznamy jsou zkopírovány z původního zdroje, lze je tedy rychle vyhledat na základě kombinace **Typu původu** a **Čísla položky původu**.

V exportovaném souboru bude uvedeno seskupení požadované úřady. To je třeba nakonfigurovat v **Definice výměny dat**, která je plně konfigurovatelná. Více informací naleznete na stránce [Nastavení definice výměny dat](across-how-to-set-up-data-exchange-definitions.md).

### Výkaz dlouhodobého majetku

Dlouhodobý majetek se v řádcích Intrastatu zobrazí pouze v případě, že:

* Typ zaúčtování **DM** v poli **Záznam v účetní knize DPH** je **Pořizovací náklady** a pokud je **Typ dokladu** v případě nákupu **Faktura** a
* Typ zaúčtování **DM** v poli **položka DPH** je **Výnos z prodeje** a pokud je **Typ dokladu** v případě prodeje **Faktura**.

### Stavy hlášení Intrastatu

Při práci s výkazem **Intrastat** se v záhlaví dokumentu zobrazí pole **Stav**. Najdete zde následující stavy spolu se souvisejícími pravidly:

* **Otevřený**: Tento stav se vytvoří automaticky při vytváření nového hlášení Intrastat a můžete v něm provádět všechny operace.
* **Vydané**: [!INCLUDE[prod_short](includes/prod_short.md)] při vytváření souboru automaticky změní stav na *Vydané*. Od tohoto okamžiku se nemůže **Hlášení Intrastat** upravovat. Pokud potřebujete něco změnit a hlášení znovu otevřít, můžete použít akci **Otevřít** a hlášení Intrastat znovu otevřít. Po opětovném otevření dokumentu můžete použít akci **Vydat** a dokument opět vydat.
* **Vyázáno**: Určuje, zda byl záznam již nahlášen finančnímu úřadu. Nejedná se o běžný stav, ale o samostatné pole, a i kdybyste výkaz pro Intrastat znovu otevřeli, stále by se zobrazovalo, že soubor je pro tento výkaz již vytvořen.

### Lokace ve výkazu Intrastat

[!INCLUDE[prod_short](includes/prod_short.md)] ajako zemi pro **odeslání z** nebo **přijetí do** zboží se vždy použijí údaje v poli **Kód země/oblasti** na stránce **Lokace**. Pokud tyto informace neexistují nebo umístění nebylo použito, systém použije informace ze stránky **Informace o společnosti**.

> [!NOTE]  
> Pokud společnost působí ve více než jedné zemi, nefunguje hlášení Intrastatu pro všechny země, kde jsou konfigurovány lokace. Vykazování je založeno pouze pro hlavní zemi, protože v současné době není možné používat vykazování pro více zemí. 

### Trojstranný obchod v Intrastatu

Trojstranný obchod zahrnuje obchod mezi třemi zeměmi nebo regiony, kde zboží obchází zemi vykazující společnosti. V aplikaci Business Central lze usnadnit pomocí funkce [Přímá dodáva](sales-how-drop-shipment.md). Chcete-li tuto možnost povolit, aktivujte pole **Zahrnout přímou dodávku** v **Nastavení hlášení Intrastat**.

Pokud tuto možnost povolíte, systém použije následující pravidla, ale pouze v případě, že máte v **Prodejní objednávce** označenou možnost **Přímá dodávka**:

| Příjem z | Dodávka do | Očekávaný výsledek Intrastatu |
|----------|------------|----------------------|
| Země, která je v **Informace o společnosti** | Země, která je v **Informace o společnosti** | Žádné řádky Intrastatu |  
| Země, která je v **Informace o společnosti** | Země EU, která je jiná od země v **Informace o společnosti** | řádky dodávky Intrastatu | 
| Země, která je v **Informace o společnosti** | Země mimo EU |Žádné řádky Intrastatu |   
| Země EU, která je jiná od země v **Informace o společnosti** | Země, která je v **Informace o společnosti** | Řádky příjmu Intrastatu | 
| Země EU, která je jiná od země v **Informace o společnosti** | Země EU, která je jiná od země v **Informace o společnosti** | Žádné řádky Intrastatu |
| Země EU, která je jiná od země v **Informace o společnosti** | Země mimo EU | Žádné řádky Intrastatu |
| Země mimo EU | Země, která je v **Informace o společnosti** | Žádné řádky Intrastatu |  
| Země mimo EU | Země EU, která je jiná od země v **Informace o společnosti** | Žádné řádky Intrastatu |
| Země mimo EU | Země mimo EU | Žádné řádky Intrastatu |

## Viz také

[Nastavení Intrastat](finance-how-setup-report-intrastat.md)  
[Finanční management](finance.md)  
[Přímá dodávka](sales-how-drop-shipment.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
