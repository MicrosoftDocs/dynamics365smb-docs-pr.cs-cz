---
title: Set Up Intercompany Transaction Posting| Microsoft Docs
description: Create your intercompany vendors and customers as so-called intercompany partners, and set up an intercompany chart of accounts.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 10/01/2019
ms.author: sgroespe

---
# Nastavení vnitropodniku
Chcete-li odeslat transakci (například řádek deníku prodeje) z jedné společnosti a mít odpovídající transakci (například řádek deníku nákupu) automaticky vytvořenou v partnerské společnosti, zúčastněné společnosti se musí dohodnout na společné účetní osnově a sadě dimenzí pro použití na vnitropodnikových transakcích. Vnitropodniková účetní osnova může být například zjednodušená verze účetní osnovy mateřské společnosti. Každá společnost mapuje svou úplnou účetní osnovu do sdílené vnitropodnikové účetní osnovy a každá společnost mapuje své dimenze na vnitropodnikové dimenze.

Pro každou partnerskou společnost musíte také nastavit kód vnitropodnikového partnera, na kterém se shodnou všechny společnosti, a poté je přiřadit do karet zákazníků a dodavatelů vyplněním pole **Kód vnitropodnikového partnera**.

Pokud vytváříte nebo přijímáte vnitropodnikové řádky se zbožím, můžete použít buď vlastní čísla zboží, nebo můžete nastavit čísla zboží partnera pro každé relevantní zboží, buď v poli **Číslo zboží dodavatele** nebo v poli **Obecné číslo zboží** na kartě zboží. Můžete také použít funkci **Křížový odkaz zboží**: Chcete-li namapovat čísla svého zboží na popisy zboží vnitropodnikových partnerů, otevřete kartu každého zboží a poté vyberte akci **Křížové odkazy** k nastavení křížových odkazů mezi popisy vašeho zboží a popisy zboží vnitropodnikového partnera.

Pokud provedete vnitropodnikové prodejní transakce, které zahrnují zdroje, musíte vyplnit pole **Číslo účtu  nákupu vnitrop. partn.** na kartě zdrojů pro každý relevantní zdroj. Toto je číslo vnitropodnikového účtu hlavní knihy, na který bude částka pro tento zdroj zaúčtována ve společnosti vašeho partnera. Pro více informací navštivte [Nastavení zdrojů](projects-how-setup-resources.md).

## Nastavení společností pro vnitropodnikové transakce
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Informace o společnosti** a poté vyberte související odkaz.
2. Na stránce **Informace o společnosti** vyplňte pole **Kód vnitropod. partnera**, **Typ vnitropodnik. doručené pošty**. a **Detaily vnitropod.doručené pošty**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Nastavení vnitropodnikových partnerů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodnikoví partneři** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Na stránce **Vnitropodnikového partnera** vyplňte pole podle potřeby.

## Nastavení vnitropodnikových dodavatelů a vnitropodnikových zákazníků
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dodavatelé** a poté vyberte související odkaz.
2. Případně přistupte k dodavateli z pole **Číslo dodavatele** na stránce **Vnitropodnikový partner**.
3. Otevřete kartu pro dodavatele, který je vnitropodnikovým partnerem. Pro více informací navštivte [Registrace nových dodavatelů](purchasing-how-register-new-vendors.md).
4. V polie **Kód vnitropodnikového partnera** vyberte příslušný kód partnera v rámci společnosti.
5. Opakujte kroky 1 až 4 pro zákazníky.

## Nastavení vnitropodnikových účetních osnov
Aby skupina společností mohla provádět vnitropodnikové transakce, musí se dohodnout na účetní osnově, kterou použijí jako společný odkaz. Musíte souhlasit se svými partnerskými společnostmi na číslech účtů, které budete všichni používat při vytváření vnitropodnikových transakcí. Například mateřská společnost skupiny vytvoří zjednodušenou verzi své vlastní účetní osnovy, exportuje tuto vnitropodnikovou tabulku účtů ze své databáze do souboru XML a distribuuje ji každé ze společností ve skupině.

Pokud je vaše společnost mateřskou společností a má definující vnitropodnikovou tabulku účtů, kterou bude vaše skupina používat jako běžný odkaz, postupujte podle postupu [Nastavení definující vnitropodnikové účetní osnovy](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts).

Pokud je vaše společnost dceřinou společností a obdržíte soubor XML obsahující společnou vnitropodnikovou tabulku účtů, postupujte podle postupu [Import vnitropodnikové účetní osnovy](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).

### Nastavení definující vnitropodnikové účetní osnovy
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodniková účtová osnova** a poté vyberte související odkaz.
2. Na stránce **Vnitropodniková účtová osnova** zadejte každý účet na řádek na stránce.
3. Pokud bude vaše vnitropodniková účetní osnova stejná nebo podobná běžné účetní osnově, můžete stránku vyplnit automaticky výběrem akce **Kopírovat z účetní osnovy**. Nové řádky můžete podle potřeby upravit.

### Export vnitropodnikové účetní osnovy
Chcete-li umožnit svým vnitropodnikovým partnerům importovat definující účetní osnovu, musíte ji exportovat do souboru.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodniková účtová osnova** a poté vyberte související odkaz.
2. Na stránce **Vnitropodniková účtová osnova** vyberte akci **Export** a poté vyberte tlačítko **Uložit**.
3. Zadejte název souboru a umístění, do kterého chcete soubor XML uložit, a poté vyberte tlačítko **Uložit**.

### Import vnitropodnikové účetní osnovy
Pokud existuje soubor pro definování vnitropodnikové účtové osnovy, mohou ho vnitropodnikoví partneři importovat a ujistit se, že mají stejné účty.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodniková účtová osnova** a poté vyberte související odkaz.
2. Na stránce **Vnitropodniková účtová osnova** vyberte akci **Importovat**.
3. Vyberte název souboru a umístění souboru XML a poté zvolte tlačítko **Otevřít**.

Stránka **Vnitropodniková účetní osnova** je vyplněna novými nebo upravenými řádky finančního účtu podle vnitropodnikové účetní osnovy v souboru. Všechny existující nesouvisející řádky na stránce zůstanou nezměněny.

### Mapování vnitropodnikové účetní osnovy na účetní osnovu vaší společnosti
Pokud jste definovali nebo importovali vnitropodnikovou účetní osnovu, s kterou jste vy a vaši vnitropodnikoví partneři souhlasili, musíte každý z vnitropodnikových účtů spojovat k jednomu z účtů vaší společnosti. Na stránce **Vnitropodniková účetní osnova** určete, jak budou vnitropodnikové účty hlavní knihy při příchozích transakcích převáděny na účty hlavní knihy z účetní osnovy vaší společnosti.

Pokud mají účty ve vnitropodnikové účetní osnově stejná čísla jako odpovídající účty v účetní osnově, můžete účty automaticky mapovat.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodniková účtová osnova** a poté vyberte související odkaz.
2. Vyberte řádky, které chcete automaticky mapovat, a poté vyberte akci **Propojit s účtem se  stejným číslem**.
3. Pro každý účet hlavní knihy v rámci společnosti, který nebyl mapován automaticky, vyplňte pole **Propojeno s číslem  fin. účtu**.

## Nastavení výchozích účtů hlavní knihy vnitropodnikového partnera
Když vytvoříte vnitropodnikový prodejní nebo nákupní řádek, který bude odeslán jako odchozí transakce, zadáte účet z vnitropodnikové účetní osnovy jako výchozí, pro který účet ve společnosti vašeho partnera je částka zaúčtována. Na stránce **Účetní osnova** u účtů, které často používáte na odchozích vnitropodnikových prodejních nebo nákupních řádcích, můžete určit výchozí účet hlavní knihy vnitropodnikových partnerů. Například pro vaše účty pohledávek můžete zadat odpovídající závazkové účty z vnitropodnikové účetní osnovy.

Poté, když zadáte účet hlavní knihy v poli **Číslo  protiúčtu** na vnitropodnikovém řádku **Vnitropodnikový partner** v poli **Typ účtu** pole **Finanční účet vnitropodnikového partnera** je automaticky vyplněno.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
2. V řádku pro účet hlavní knihy, který se používá pro vnitropodnikové transakce, zadejte do pole **Výchozí finanční účet vnitropodnikového partnera** účet hlavní knihy vnitropodnikové společnosti, na který bude váš partner účtovat při účtování na účet hlavní knihy na řádku.
3. Opakujte krok 2 pro každý účet, který často zadáváte v poli **Číslo  protiúčtu** na řádku ve vnitropodnikovém deníku nebo dokumentu.

## Nastavení vnitropodnikových dimenzí
Pokud vy a vaši vnitropodnikoví partneři chcete mít možnost vyměňovat si transakce s dimenzemi s nimi spojenými, musíte se dohodnout na dimenzích, které všichni budete používat. Například mateřská společnost skupiny vytvoří zjednodušenou verzi své vlastní sady dimenzí, exportuje tyto vnitropodnikové dimenze do souboru XML a distribuuje je každé ze společností ve skupině. Každá z dceřiných společností pak importuje soubor XML na stránku **Vnitropodnikové dimenze** a mapuje vnitropodnikové dimenze na stránce **Dimenze**.

Pokud je vaše společnost mateřskou společností a má definující sadu vnitropodnikových dimenzí, které bude vaše skupina používat jako společný odkaz, postupujte podle postupu [Definování vnitropodnikových dimenzí](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Pokud je vaše společnost dceřinou společností a obdržíte soubor XML obsahující vnitropodnikové dimenze, které bude vaše skupina používat jako běžný odkaz, postupujte podle postupu [Import vnitropodnikových dimenzí](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### Definování vnitropodnikových dimenzí
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodnikové dimenze** a poté vyberte související odkaz.
2. Na stránce **Vnitropodnikové dimenze** zadejte každou dimenzi do řádku na stránce.

   Pokud budou vaše vnitropodnikové dimenze podobné nebo stejné jako vaše firemní dimenze, můžete stránku vyplnit automaticky pomocí funkce **Kopírovat z dimenzí** a pak můžete upravit výsledné řádky.
3. Chcete-li exportovat vnitropodnikové dimenze do souboru XML pro distribuci partnerským společnostem, vyberte akci **Exportovat**.
4. Zadejte název souboru a umístění, do kterého chcete soubor XML uložit, a poté vyberte tlačítko **Uložit**.

### Import vnitropodnikových dimenzí
Pokud soubor existuje pro definování vnitropodnikových dimenzí, mohou jej vnitropodnikoví partneři importovat, aby se ujistili, že mají stejné dimenze.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodnikové dimenze** a poté vyberte související odkaz.
2. Na stránce **Vnitropodnikové dimenze** vyberte akci **Importovat**.
3. Zadejte název souboru a umístění souboru XML a poté vyberte tlačítko **Otevřít**.

Řádky na stránce **Vnitropodnikové dimenze** a **Hodnoty vnitropodnikových dimenzí** se importují.

### Mapování vnitropodnikových dimenzí na dimenze vaší společnosti
Pokud jste definovali nebo importovali dimenze, které jste se dohodli používat se svými partnery v rámci vnitropodniku, musíte přiřadit každou z vnitropodnikových dimenzí k jedné z dimenzí vaší společnosti a naopak. Na stránce **Vnitropodnikové dimenze** určete, jak budou vnitropodnikové dimenze při příchozích transakcích převedeny do dimenzí ze seznamu dimenzí vaší společnosti. Na strínce **Dimenze** určete, jak budou vaše dimenze převedeny na vnitropodnikové dimenze u odchozích transakcí.

Pokud má některá z vnitropodnikových dimenzí stejný kód jako odpovídající dimenze v seznamu dimenzí vaší společnosti, můžete nechat aplikaci mapovat dimenze automaticky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodnikové dimenze** a poté vyberte související odkaz.
2. Na stránce **Vnitropodnikové dimenze** vyberte řádky, které chcete automaticky mapovat, a poté vyberte akci **Propojit s dimenzí  se stejným kódem**.
3. Pro každou vnitropodnikovou dimenzi, která není automaticky mapována, vyplňte pole **Propojeno s kódem dimenze**.
4. Vyberte akci **Hodnoty vnitropodnikové dimenze**.
5. Na stránce **Hodnoty vnitropodnikové dimenze** vyplňte pole **Propojeno s kódem hodn.dimenze**.

   Pokračujte v mapování dimenzí na vnitropodnikové dimenze provedením podobných kroků.
6. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dimenze** poté vyberte související odkaz.
7. Na stránce **Dimenze** vyberte řádky, které chcete automaticky mapovat, a poté vyberte akci **Propojit s vnitropodnikovou dimenzí  se stejným kódem**.
8. Pro každou vnitropodnikovou dimenzi, která není automaticky mapována, vyplňte pole **Propojeno s kód.hod.vnitrop.dim.**
9. Vyberte akci **Hodnoty dimenzí**.
10. Na stránce **Hodnoty dimenzí** vyplňte pole **Propojeno s kód.hod.vnitrop.dim.**

## Viz také
[Správa vnitropodnikových transakcí](intercompany-manage.md)  
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Práce s finančními deníky](ui-work-general-journals.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
