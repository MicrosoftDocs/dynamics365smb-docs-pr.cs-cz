---
title: About Setting Up Value-Added Tax | Microsoft Docs
description: Make sure that you correctly calculate, post, and report on VAT for sales and purchases.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 01/13/2020
ms.author: bholtorf

---

# Nastavení daně z přidané hodnoty
Spotřebitelé a podniky platí daň z přidané hodnoty (DPH) při nákupu zboží nebo služeb. Výše DPH se může lišit v závislosti na několika faktorech. V [! INCLUDE [d365fin](includes/d365fin_md.md)] nastavíte DPH, k určení sazeb, které se použijí pro výpočet daně, na základě následujících kritérií:

* Komu prodáváte
* Od koho nakupujete
* Co prodáváte
* Co kupujete

Výpočty DPH můžete nastavit ručně, ale to může být složité a časově náročné. Abychom vám to usnadnili, poskytujeme asistovaného průvodce nastavením s názvem **Nastavit DPH**, který vám pomůže udělat patřičné kroky. K nastavení DPH doporučujeme použít průvodce nastavením.

> [!NOTE]  
> Průvodce můžete použít pouze v případě, že jste vytvořili společnost a neúčtovali jste transakce, které zahrnují DPH. V opačném případě by bylo velmi snadné omylem použít různé sazby DPH a učinit sestavy související s DPH nepřesnými.

Pokud si chcete sami stanovit výpočty DPH nebo se chcete o každém kroku dozvědět, toto téma obsahuje popisy jednotlivých kroků.

## Použití asistovaného průvodce Nastavit DPH pro nastavení DPH
Doporučujeme použít asistované nastavení Nastavit DPH pro nastavení DPH v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Chcete-li spustit průvodce asistovaným nastavením, postupujte takto:
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Asistované nastavení** a vyberte související odkaz.
2. Vyberte **Nastavit DPH** a dokončete kroky.
3. Po dokončení asistovaného nastavení navštivte stránku <x1 />Nastavení účtování DPH<x2 /> a zkontrolujte, zda je třeba vyplnit další pole podle Vaší země. Pro víc informací navštivte [Lokální funkcionality v Business Central](about-localization.md) .

## Nastavení DIČ pro vaší zemi nebo oblast
Chcete-li zajistit, aby lidé zadávali platná DIČ, můžete definovat formáty pro DIČ, která se používají v zemích nebo regionech, ve kterých podnikáte. [!INCLUDE[d365fin](includes/d365fin_md.md)] zobrazí chybovou zprávu, když někdo udělá chybu nebo použije formát, který je pro danou zemi nebo oblast nesprávný.

Pro nastavení DIČ postupujte takto:
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Země/oblasti** a vyberte související odkaz.
2. Vyberte zemi nebo oblast a péte vyberte tlačítko **Formáty  DIČ**.
3. V poli **Formáty**, definujte formát zadáním jednoho nebo více z následujících znaků:

* **#** vyžaduje jednociferné číslo.
* **@** vyžaduje písmeno. Na velikosti písmen nezáleží.
* **?** umožňuje libovolný znak.

   > [!Tip]
   > Můžete použít i jiné znaky, pokud jsou ve formátu vybrané země nebo oblasti.. Pokud například potřebujete zahrnout tečku nebo pomlčku mezi sadami čísel, můžete formát definovat jako ##.######## nebo @@@-###-####.

## Nastavení DPH obchodních účto skupin
Obchodní DPH účto skupiny by měly představovat trhy, na kterých obchodujete se zákazníky a prodejci, dále skupiny určijí, jak vypočítat a účtovat DPH na každém trhu. Příklad obchodních DPH účto skupin jsou **Domácí** and **Evropská unie (EU)**.

Používejte kódy, které jsou snadno zapamatovatelné a popisují obchodní účto skupinu, například **EU**, **EXPORT**, nebo **DOMÁCÍ**. Kód musí být jedinečný. Můžete nastavit libovolný počet kódů, ale nemůžete mít stejný kód více než jednou v tabulce.

Pro nastavení DPH obchodních účto skupin postupujte takto:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **DPH obchodní účto skupiny** a vyberte související odkaz.
2. Podle potřeby vyplňte pole.

Výchozí DPH obchodní účto skupiny nastavíte jejich propojením s obecnými obchodními účto skupinami. [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky přiřadí DPH obchodní účto skupinu při přiřazení obchodní účto skupiny k zákazníkovi, dodavateli nebo účtu.

## Nastavení DPH účto skupin zboží
DPH účto skupiny zboží reprezentují zboží a zdrojde, které kupujete nebo prádáváte a určují jak se bude počítat DPH podle typu zboží nebo zdroje a zda se nakupuje nebo prodává.  
Je vhodné používat kódy, které jsou snadno zapamatovatelné a popisují sazbu, například **BEZ DPH** nebo **NULOVE**, **DPH10** nebo **REDUKOVANA** pro 10% DPH a **DPH25** nebo **STANDARD** pro 25%.

Pro nastavení DPH obchodních účto skupin postupujte takto:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **DPH účto skupiny zboží** a vyberte související odkaz.
2. Podle potřeby vyplňte pole.

## Kombinace DPH účto skupin v nastavení účtování DPH
[!INCLUDE[d365fin](includes/d365fin_md.md)] vypočítá částky DPH za prodeje a nákup na základě nastavení účtování DPH, což jsou kombinace DPH obchodních účto skupin a DPH účto skupin zboží. Pro každou kombinaci můžete zadat procento DPH, typ výpočtu DPH a účty pro účtování DPH za prodej, nákup a vratky. Můžete také určit, zda se má přepočítat DPH při uplatnění nebo obdržení skonta.

Nastavte tolik kombinací, kolik potřebujete. Pokud chcete seskupit kombinace nastavení účtování DPH s podobnými atributy, můžete definovat **Identifikátor DPH** pro každou skupinu a přiřadit identifikátor členům skupiny.

Chcete-li kombinovat nastavení účtování DPH, postupujte takto:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení účtování DPH** a vyberte související odkaz.
2. Podle potřeby vyplňte pole.

## Přiřazení Účto skupin DPH ve výchozím nastavení k více entitám
Pokud chcete použít stejné účto skupiny DPH pro více entit, můžete nastavit [!INCLUDE[d365fin](includes/d365fin_md.md) ] tak učinit ve výchozím nastavení. Existuje několik způsobů, jak to udělat:

* Obchodní účto skupiny DPH můžete přiřadit k obecným obchodním účto skupinám nebo k šablonám zákazníků nebo dodavatelů.
* Můžete přiřadit DPH účto skupiny zboží k obecným účto skupinám zboží.

Dph obchodní nebo účto skupina zboží je přiřazena při výběru obchodní nebo zbožové účto skupině pro zákazníky, dodavatele, zboží nebo zdroj.

## Přiřazení DPH účto skupin k účtům, zákazníkům, dodavatelům, zboží a zdrojům
Následující části popisují, jak přiřadit DPH účto skupiny k jednotlivým subjektům.

### Přiřazení DPH účto skupin k jednotlivým účtům hlavní knihy
1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Účetní osnova** a vyberte související odkaz.
2. Otevřete kartu **Účtu účetní osnovy** pro vybraný účet.
3. Na záložce **Účtování** v poli **Typ obecného účtování**, vybertě buď **Prodej** nebo **Nákup**.
5. Zvolte DPH účto skupiny, které chcete použít pro prodejní nebo nákupní účet.

### Přiřazení DPH obchodních účto skupin zákazníkům a dodavatelům
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zákazníci** nebo **Dodavatelé** a vyberte související odkaz.
2. Na kartě **Zákazníka** nebo **Dodavatele**, rozbalte záložku **Fakturace**.
3. Vyberte DPH obchodní účto skupinu.

### Přiřazení DPH účto skupin zboží k jednotlivému zboží a zdrojům
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zboží** nebo **Zdroje** a vyberte související odkaz.
2. Proveďte jeden z následujících úkonů:

* Na kartě **Zboží** rozbalte záložku **Cena a Účtování** a použijte tlačítko **Zobrazit více polí** k zobrazení políčka **DPH účto skupina zboží**.
* Na kartě **Zdroje**, rozbalte záložku **Fakturace**.
3. Vyberte DPH účto skupinu zboží.

## Nastavení doložek k vysvětlení osvobození od DPH nebo nestandardních DPH sazeb
Nastavte klauzuli DPH popisující informace o typu DPH, která je použita. Informace mohou být vyžadovány nařízením vlády. Po nastavení klauzule DPH a přidružení k nastavení účtování DPH, se klauzule DPH zobrazí na vytištěných prodejních dokladech, které používají účto skupiny nastavení DPH.

V případě potřeby můžete také určit, jak převést klauzule DPH do jiných jazyků. Potom při vytváření a tisku prodejního dokladu, který obsahuje identifikátor DPH, bude dokument obsahovat přeloženou klauzuli DPH. Kód jazyka uvedený na kartě zákazníka určuje jazyk.

Pokud jsou nestandardní sazby DPH používány v různých typech dokumentů, jako jsou faktury nebo dobropisy, musí společnosti obvykle uvést text osvobození (klauzuli o DPH), v níž je uvedeno, proč byla vypočtena snížená nebo nulová sazba DPH. Můžete definovat různé klauzule DPH, které mají být zahrnuty do obchodních dokladů podle typu dokladu, například faktury nebo dobropisu. Můžete nastavení udělat na stránce **Klauzule DPH**.

Můžete upravit nebo odstranit klauzuli DPH a změny se následně projeví ve vygenerované sestavě. Nicméně, [!INCLUDE[d365fin](includes/d365fin_md.md)] neuchovává historii změny. V sestavě jsou popisy klauzule DPH vytištěny a zobrazeny pro všechny řádky v sestavě vedle částky DPH a základní částky DPH. Pokud nebyla klauzule DPH definována pro žádné řádky v prodejním dokladu, je při tisku sestavy vynechán celý oddíl.

### Nastavení klauzule DPH
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Klauzule DPH** a vyberte související odkaz.
2. Na stránce **Klauzule DPH** vytvořte nový řádek.
3. V poli **Kód** zadejte identifikátor klauzule. Pomocí tohoto kódu přiřadíte klauzuli skupinám účtování DPH.
4. V poli **Popis** zadejte text osvobození DPH, který chcete zobrazit v dokumentech, které mohou zahrnovat DPH. V poli **Popis 2** zadejte v případě potřeby další text. Text se zobrazí na nových řádcích dokumentu.
5. Vyberte tlačítko **Popis dle typu dokladu**.
6. Na stránce **Popis dle typu dokladu**, vyplňte pole, abyste nastavili, jaký text osvobození DPH se zobrazí pro který typ dokumentu.
7. Volitelné: Chcete-li klauzuli DPH přiřadit k nastavení účtování DPH ihned, zvolte **Nastavení** a následně vyberte klauzuli. Pokud chcete počkat, můžete klauzuli přiřadit později na stránce **Nastavení účtování DPH**.
8. Volitelné: Chcete-li určit, jak se má překládat doložka o DPH, vyberte akci **Překlady**.

### Přiřazení klauzule DPH k nastavení účtování DPH
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení účtování DPH** a vyberte související odkaz.
2. Ve sloupci **Klauzule DPH** zvolte klauzuli, která se má použít pro každé nastavení účtování DPH, na které se vztahuje.

### Nastavení překladů pro klauzule DPH
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Klauzule DPH** a vyberte související odkaz.
2. Vyberte tlačítko **Překlady**.
3. V poli **Kód jazyka** vyberte požadovaný jazyk.
4. V polích **Popis** a **Popis 2**, vložte překlady popisů. Tento text se zobrazí v přeložených dokladech DPH.

## Nastavení účtování DPH pro zpracování importní DPH
Funkce Importní DPH se používá v případě, že potřebujete zaúčtovat doklad, kde je celá částka DPH. Tuto možnost použijete, pokud obdržíte od finančního úřadu fakturu na DPH za dovážené zboží.

Pro nastavení kódů pro importní DPH postupujte takto:
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **DPH účto skupiny zboží** a vyberte související odkaz.
2. Na stránce DPH účto skupiny zboží nastavte novou DPH účto skupinu zboží pro importní DPH.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení účtování DPH** a vyberte související odkaz.
4. Na stránce Nastavení účtování DPH vytvořte nový řádek nebo použijte existující DPH obchodní účto skupiny v kombinaci s novou DPH účto skupinou zboží pro importní DPH.
5. V poli **Typ výpočtu DPH**, vyberte **Plná DPH**.
6. V poli  **Účet nákupní DPH** zadejte účet, na který chcete použít k zaúčtování dovozní DPH. Všechny ostatní účty jsou volitelné.


## Použití vratné DPH pro obchod mezi zeměmi nebo oblastmi EU
Některé společnosti musí při obchodování s jinými společnostmi používat vratnou DPH. Toto pravidlo se například vztahuje na nákupy ze zemí nebo oblastí EU a prodej do zemí nebo oblastí EU.

> [!NOTE]  
> Toto pravidlo platí při obchodování se společnostmi, které jsou registrovány jako plátce DPH v jiné zemi EU. Pokud obchodujete přímo se spotřebiteli v jiných zemích nebo oblastech EU, měli byste se obrátit na svůj daňový úřad s žádostí o příslušná pravidla DPH.

> [!TIP]  
> Ověřením, že společnost je registrována jako plátce DPH v jiné zemi EU, použijte službu ověřování DIČ v EU. Služba je k dispozici zdarma v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro více informace navštivte sekci _Ověření DIČ_.

### Prodej do zemí EU
DPH se nepočítá z prodeje společnostem povinným k DPH v jiných zemích nebo oblastech EU. Hodnotu těchto prodejů musíte nahlásit do zemí EU samostatně ve svém daňovém přiznání.

Chcete-li správně vypočítat DPH z prodeje do zemí nebo oblastí EU, měli byste udělat:

* Založte řádek pro prodej se stejnými informacemi pro nákupy. Pokud jste již nastavili řádky na stránce Nastavení účtování DPH pro nákupy ze zemí nebo oblastí EU, můžete tyto řádky použít také pro prodej.
* Přiřaďte DPH obchodní účto skupiny v  poli **DPH obchodní účto skupina** na záložce **Fakturace** na kartě každého zákazníka EU. DIČ zákazníka byste měli také zadat do pole**DIČ** v záložce **Zahraniční obchod**.

Když účtujete prodej zákazníkovi v jiné zemi nebo oblasti EU, vypočítá se částka DPH a položka DPH se vytvoří pomocí informací o přenesené daňové povinnosti DPH a základu DPH, což je částka, která se používá k výpočtu částky DPH. Na účtech DPH nejsou v hlavní knize zaúčtovány žádné položky.

## Principy zaokrouhlení DPH v dokladech
Částky v dokladech, které ještě nejsou zaúčtovány, jsou zaokrouhleny a zobrazeny tak, aby odpovídaly konečnému zaokrouhlení částek, které jsou skutečně zaúčtovány. DPH se vypočítá pro celý doklad, což znamená, že DPH je vypočtena na základě součtu všech řádků se stejnou sazbou DPH v dokladu.




## Viz také
[Nastavení šablony výkazu DPH a názvů výkazů DPH](finance-how-setup-vat-statement.md)   
[Nastavení nerealizované DPH](finance-setup-unrealized-vat.md)      
[Hlášení DPH finančním úřadům](finance-how-report-vat.md)      
[Práce s DPH v nákupu a prodeji](finance-work-with-vat.md)    
[Práce s změnou sazby DPH](finance-how-use-vat-rate-change-tool.md)    
[Ověření DIČ](finance-how-validate-vat-registration-number.md)  
[Lokální funkcionality v Business Central](about-localization.md)

## Viz související školení v programu [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)
