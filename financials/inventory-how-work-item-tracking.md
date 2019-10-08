---
title: Přiřazení sériových čísel čísla a čísel šarží ke zboží pro sledování | Microsoft Docs
description: Sériová čísla a čísla šarží můžete přidat do jakéhokoli odchozího nebo příchozího dokladu a jeho účtované položky sledování zboží se zobrazí v souvisejících položkách zboží.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/22/2017
ms.author: sgroespe
---
# <a name="work-with-serial-and-lot-numbers"></a>Práce se sériovými čísly a čísly šarží
Sériová čísla a čísla šarží můžete přiřadit k jakémukoli odchozímu nebo příchozímu dokladu a jeho účtované položky sledování zboží se zobrazí v souvisejících položkách zboží. Úkon provedete v okně **Řádky sledování zboží**.

Pole matice množství v horní části okna **Řádky sledování zboží** zobrazuje množství a součty sledovacích čísel zboží definovaných na řádcích. Množství musí odpovídat množství v řádku dokladu, které je v polích **Nedefinováno** označeno 0.

Jako měřítko výkonu program shromažďuje informace o dostupnosti v okně **Řádky sledování zboží** pouze jednou, když stránku otevřete. To znamená, že program neaktualizuje informace o dostupnosti během doby, kdy máte otevřené okno, i když během této doby dojde ke změnám ve skladu nebo na jiných dokladech.

Zboží se sériovým číslem nebo číslem šarže lze v dodavatelském řetězci sledovat zpět i vpřed. To je užitečné pro obecné zajištění kvality a stahování produktů z trhu. Pro více informací navštivte [Sledování zboží - Sledované zboží](inventory-how-to-trace-item-tracked-items.md).

## <a name="about-picking-serial-or-lot-numbers-in-the-warehouse"></a>Vybírání sériových čísel nebo čísel šarží ve skladu
Odchozí zpracování sériových čísel nebo čísel šarží je častým úkolem v různých skladových procesech.  

V některých procesech skladové položky nenesou sériová čísla nebo čísla šarže a pracovník skladu musí při odchozí manipulaci přiřadit nové číslo, obvykle z předdefinované číselné řady.

V jednoduchých procesech již skladové položky nesou sériová čísla nebo čísla šarže, například přiřazená během odkládání, a tato čísla jsou automaticky přenášena prostřednictvím všech výstupních skladových činností bez interakce pracovníků skladu.

Ve zvláštních situacích u sériových nebo šaržových zásob jsou ve zdrojovém dokumentu definována konkrétní sériová nebo šaržová čísla, jako je prodejní objednávka, kterou musí pracovník skladu při manipulaci s výstupním skladem respektovat. Může to být způsobeno tím, že zákazník během procesu objednávky požadoval konkrétní dávku. Když je doklad vyskladnění zásob nebo vyskladnění ze skladu vybrán z výstupního zdrojového dokladu, kde jsou již definována sériová čísla nebo čísla šarže, všechna pole v okně **Řádky sledování zboží** pod vyskladněním zásob jsou zablokovány pro zápis, kromě pole **Množství ke zpracování**. V takovém případě řádky vyskladnění zásob určují sledovací čísla zboží na jednotlivých řádcích pro odběr a místo. Množství je již rozděleno do jedinečných kombinací sériových čísel nebo čísel šarží, protože prodejní objednávka specifikuje sledovací čísla zboží k odeslání.  

## <a name="item-tracking-availability"></a>Dostupnost sledování zboží
Když pracujete se sériovými čísly a čísly šarží, [!INCLUDE [d365fin](includes/d365fin_md.md)] vypočítá informace o dostupnosti pro čísla šarže a sériová čísla a zobrazí je na různých oknech pro sledování zboží. To vám umožní zjistit, kolik z čísla šarže nebo sériového čísla se aktuálně používá v jiných dokladech. To snižuje chyby a nejistotu způsobenou dvojím přidělením.

V okně **Řádky sledování zboží** se v poli **Dostupnost, číslo šarže** nebo **Dostupnost, sériové číslo** zobrazí varovná ikona, pokud se některé nebo celé množství, které jste vybrali, již používá v jiných dokladech nebo pokud číslo šarže nebo sériové číslo není k dispozici.

V okně **Č. Šarže / Sériové č.-Seznam**,  **Č. Šarže / Sériové č.-Dostupnost** a **Sledování zboží - Vybrat položky** se zobrazí informace o tom, jak velké množství zboží se používá. To zahrnuje následující informace.

|Pole|Popis|
|-----|-----------|  
|**Celkové množství**|Celkový počet zboží aktuálně ve skladu|
|**Celkové požadované množství**|Celkový počet požadovaného zboží, které bude použito v tomto a dalších dokladech|
|**Aktuální množství ke zpracování**|Počet zboží, které je požadováno a které bude použito v aktuálním dokladu, ale které dosud není vázáno na databázi|
|**Aktuální požadované množství**|Počet požadovaného zboží, které bude použito v aktuálním dokladě|
|**Celkové množství k dispozici**|Celkové množství zboží v zásobách, snížené o množství zboží, které je požadováno v tomto a dalších dokladech (celkové požadované množství), a mínus množství, které je v tomto dokladě požadováno, ale ještě není vázáno (aktuální nevyřízené množství)|

Pokud v okně **Řádky sledování zboží** pracujete dlouhou dobu nebo pokud existuje velká aktivita se zbožím, s kterým pracujete, můžete zvolit akci **Aktualizovat dostupnost**. Kromě toho, když zavřete okno, je dostupnost zboží automaticky znovu zkontrolována abyste se ujistili, že neexistují žádné problémy s dostupností.

## <a name="to-set-up-item-tracking-codes"></a>Nastavení kódů sledování zboží
Kód sledování zboží odráží různé aspekty, které má společnost ohledně používání sériových čísel a čísel šarží pro zboží pohybujíce se v zásobách.  

1. Zvolte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "Ikona Vyhledat Stránku nebo Sestavu"), zadejte **Kód sledování zboží** a pak vyberte související odkaz.  
2. Zvolte akci **Nový**.
3. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Na záložkách **Sériové číslo** a **Číslo šarže** definujte zásady sledování zboží podle sériových čísel a čísel šarží.  

### <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Nastavení pravidla vypršení platnosti pro sériová čísla nebo čísla šarže  
U některých zboží můžete chtít v kódu sledování zboží nastavit konkrétní data a pravidla vypršení platnosti. Tato funkce umožňuje sledovat, kdy vyprší platnost specifických sériových čísel a čísel šarží.

1. Vyberte existující kód sledování zboží a poté vyberte akci **Upravit**.  
2.  Na záložce **Různé** , zaškrtněte následující políčka.  

    |Pole|Popis|  
    |---------------------------------|---------------------------------------|  
    |**Přísné účtování expirace**|Určuje, že datum expirace přidělené k číslu sledování zboží, když vstoupilo do zásob, musí být respektováno, když zásoby opouští.|  
    |**Pož. ruč. zadání data platnosti**|Určuje, že musíte ručně zadat datum vypršení platnosti na řádku sledování zboží.|  

### <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Nastavení záruk na sériová čísla nebo čísla šarže  
U některého zboží můžete chtít nastavit konkrétní záruky v kódu sledování zboží. Tato funkce umožňuje sledovat, kdy se vyčerpají záruky na konkrétní sériová čísla nebo čísla šarže v zásobách.        
1.  Zvolte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "Ikona Vyhledat Stránku nebo Sestavu"), zadejte **Kód sledování zboží** a pak vyberte související odkaz.  

1. Vyberte existující kód sledování zboží a poté vyberte akci **Upravit**.  
2.  Na záložce **Různé** , vyplňte pole **Vzorec data záruky** a poté zaškrtněte políčko.  

    |Pole|Popis|  
    |---------------------------------|---------------------------------------|  
    |**Vzorec data záruky**|Určuje poslední den záruky zboží.|  
    |**Pož. ručního zadání data záruky**|Určuje, že na řádku sledování zboží musíte ručně zadat datum záruky.|  

## <a name="to-record-serial-or-lot-number-information"></a>Zaznamenávaní informace o sériovém čísle nebo čísle šarži  
Potřebujete-li například spojit zvláštní informace s konkrétním číslem sledování zboží, například pro zajištění kvality, můžete tak učinit na informační kartě sériového čísla nebo čísla šarže.

1. Otevřete dokument, který má přiřazeno sériové číslo nebo číslo šarže.
2. Otevřete okno **Řádky sledování zboží** pro doklad.
3. Vyberte například akci **Karta informace sériového čísla**.  

    Pole **Sériové číslo** a **Číslo šarže** jsou vyplněna z řádku pro sledování zboží.  
4. Do pole **Popis** zadejte krátkou informaci, například o stavu zboží.  
5. Zvolte akci **Komentář** k vytvoření samostatného záznamu komentářů.  
6. Chcete-li vyloučit sériové číslo nebo číslo šarže z transakcí, zaškrtněte políčko **Blokované**.  

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Úprava stávající informace o sériovém čísle nebo čísle šarže  
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Položky** a pak vyberte související odkaz.  
2. Vyberte zboží, které má kód sledování zboží a obsahuje sériové číslo nebo číslo šarže.
3. V okně **Karty zboží** vyberte akci **Položky** a poté zvolte **Položky hlavní knihy**.
4. Vyberte pole **Číslo šarže** nebo **Sériové číslo**. Pokud pro sledovací číslo zboží existují informace, otevře se okno **Seznam informací o čísle šarže** nebo **Seznam informací o sériovém čísle**.  
5. Vyberte kartu a poté vyberte akci **Karta informace sériového čísla/čísla šarže**.  
6. Upravte text s krátkým popisem, záznam komentáře nebo pole **Blokované**.  

Sériová čísla ani čísla šarží nelze upravovat. Chcete-li tak učinit, musíte překlasifikovat dotyčný účet zboží. Pro více informací navštivte „Přeřadění čísel šarže nebo sériových čísel“.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Přiřazení sériových čísel nebo čísel šarží během příchozí transakce  
Společnosti mohou chtít sledovat zboží od okamžiku, kdy vstoupí do společnosti. V této situaci je objednávka často ústředním dokladem, ačkoli sledování zásilek může být zpracováno z jakéhokoli příchozího dokladu a jeho zaúčtovaného zboží zobrazeného v souvisejících položkách zboží.  

Přesná pravidla pro manipulaci s čísly sledování zboží ve vaší společnosti se řídí nastavením v okně **Karta kódu sledování zboží**.  

> [!NOTE]  
>  Chcete-li v činnostech ve skladu používat čísla sledování zboží, musí být vybrána pole **Sledování šarže ve skladu** a **Sledování s.čísel ve skladu**, protože definují zvláštní principy při zpracování sériových čísel a čísel šarží v činnostech skladu.  

1.  Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "Hledat ikonu stránky nebo sestavy"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.  
2.  Vyberte příslušný řádek dokumentu a na záložce **Řádky** vyberte akci **Řádek** a poté vyberte akci **Řádky sledování zboží.**  

    Sériová čísla nebo čísla šarže můžete přiřadit následujícími způsoby:  

    -   Automaticky výběrem **Přiřadit sér.číslo** nebo **Přiřadit č.šarže** pro přiřazení sériových čísel / čísel šarží z předdefinovaných číselných řad.  
    -   Automaticky výběrem **Vytvořit vlastní s.č.** přiřadíte sériová čísla / čísla šarže na základě číselných sérií, které definujete konkrétně pro přijaté zboží.  
    -   Ručně, přímým zadáním sériových čísel nebo čísel šarží, například čísel prodejců.  
    -   Ručně přiřazením konkrétního čísla každé jednotce zboží.  

3. Chcete-li automaticky přiřadit, vyberte akci **Vytvořit vlastní s.č.**.  
4. Do pole **Vlastní s.č.** zadejte počáteční číslo popisné řady sériových čísel, například **S/N-Vend0001**.  
5. Do pole **Přírůstek** zadejte 1, abyste definovali, že každé pořadové číslo se zvýší o jedno.  

    Pole **Množství k vytvoření** obsahuje ve výchozím nastavení množství řádků, ale můžete je upravit.  

6. Zaškrtněte políčko **Vytvořit nové č.šarže**, chcete-li uspořádat nová sériová čísla v samostatné šarži.  
7. Zvolte tlačítko **OK**.  

Číslo šarže s jednotlivými sériovými čísly se vytvoří podle množství zboží v řádku dokladu, počínaje **S/N-Vend0001**.  

Pole matice množství v záhlaví dynamicky zobrazuje množství a součty čísel sledovaného zboží, které v okně definujete. Množství musí odpovídat množství v řádku dokladu, které je v polích **Nedefinováno** označeno 0.  

Když je doklad zaúčtován, položky sledování zboží jsou přeneseny do přidružených položek zboží.

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Přiřazení sériového čísla nebo čísla šarže během výstupní transakce  
Existují dva způsoby, jak přiřadit odchozí transakci sériová čísla a čísla šarže:  

-   Výběr ze stávajících sériových čísel nebo čísel šarží. To platí, pokud již byla během příchozí transakce přiřazena čísla pro sledování zboží. Pro více informací navštivte „Výběr ze stávajících sériových čísel a čísel šarží“.
-   Přiřazení nových sériových čísel nebo čísel šarží během odchozích transakcí. To platí, pokud sledovací čísla zboží nejsou přiřazena ke zboží, dokud nejsou prodány a připraveny k odeslání.  

Různá pravidla pro čísla sledovaného zboží jsou nastavena v okně **Karta kódu sledování zboží**.  

> [!NOTE]  
>  Chcete-li při činnostech skladu přiřadit čísla sledování zboží, musí být na kartě kódu sledování položky zaškrtnuta políčka **Sledování s.čísel ve skladu** a **Sledování šarže ve skladu**.    

1. Vyberte příslušný doklad a na záložce **Řádky** vyberte akci **Objednávka** a poté vyberte akci **Řádky sledování zboží**.  

    Čísla pro sledování zboží můžete přiřadit následujícími způsoby:  
    -   Automaticky z předdefinovaných číselných řad: Vyberte akci **Přiřadit sér.číslo** nebo **Přiřadit č.šarže**.  
    -   Automaticky na základě parametrů, které definujete konkrétně pro odchozí zboží: Vyberte tlačítko **vytvořit ID zákazníka **.  
    -   Ručně zadáním sériových čísel nebo čísel šarží, bez použití číselné řady.  

2.  Při tomto postupu přiřaďte sériové číslo automaticky výběrem **Přiřadit sér.číslo**.  

    Pole **Množství k vytvoření** obsahuje ve výchozím nastavení množství řádků, ale můžete je upravit.  
3.  Chcete-li uspořádat nová sériová čísla v samostatné části, vyberte pole **Vytvořit nové č.šarže**.  
4.  Stisknutím tlačítka **OK** vytvoříte číslo šarže a nová jednotlivá sériová čísla podle množství, které je třeba zpracovat na příslušné řádce dokladu.  

Pole matice množství v horní části dynamicky zobrazuje množství a součty čísel sledovaného zboží, které definujete v okně. Množství musí odpovídat množství v řádku dokladu, které je v polích **Nedefinováno** označeno **0**.  

Když je doklad zaúčtován, položky sledování zboží jsou přeneseny do přidružených položek zboží.  

## <a name="to-select-from-existing-serial-or-lot-numbers"></a>Výběr ze stávajících sériových čísel nebo čísel šarží  
Když pracujete se zbožím, které vyžaduje sledování zboží a vytváříte odchozí transakce, kde zboží vychází ze zásob, obvykle musíte vybrat šarže nebo sériová čísla z těch, která již v zásobách existují.  

 Přesná pravidla pro zpracování čísel sledování zboží ve vaší společnosti se řídí nastavením tabulky **Kód sledování zboží**.  

> [!NOTE]  
>  Chcete-li zpracovat čísla sledování zboží v činnostech skladu, musí být zboží nastaveno pomocí Sledování šarže ve skladu/Sledování s.čísel ve skladu, protože to určuje zvláštní zásady upravující sériová čísla a čísla šarže ve skladu.

1.  Z libovolného odchozího dokladu vyberte řádek, pro který chcete vybrat sériové číslo nebo číslo šarže.  
2.  Na záložce **Řádky** vyberte akci **Akce**, vyberte akci **Řádek** nebo **Zboží** a poté vyberte akci **Řádky sledování zboží**.  
3.  V okně **Řádky sledování zboží** máte tři možnosti pro zadání čísla šarže nebo sériového čísla:  

    -   Vyberte pole **Číslo šarže** nebo **Sériové číslo** a potom vyberte číslo v okně **Souhrn sledování zboží**.  
    -   Vyberte akci **Vybrat položky**. V okně **Vybrat položky** jsou uvedena všechna čísla šarže nebo sériová čísla spolu s informacemi o dostupnosti.

4. Do pole **Vybrané množství** zadejte množství každé šarže nebo sériového čísla, které chcete použít.   
5. Klikněte na tlačítko **OK** a vybrané informace o sledovaném zboží se přenesou do okna **Řádky sledování zboží**.  
6. Zadejte nebo naskenujte číslo sledování zboží.

Pole matice množství v záhlaví dynamicky zobrazuje množství a součty čísel sledovaných zboží, které v okně definujete. Množství musí odpovídat množství v řádku dokladu, které je v polích **Nedefinováno** označeno **0**.  

 Když zaúčtujete řádek dokladu, informace o sledování zboží se přenesou do přidružených položek zboží.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Zpracování sériových čísel a čísel šarží při převodních objednávkách  
Postupy pro zpracování sériových čísel a čísel šarží, které se přenášejí mezi různými lokacemi, jsou podobné postupům používaným při prodeji a nákupu zboží.  

Objednávka transferu je však jedinečná v tom, že zásilka i příjem jsou prováděny ze stejného řádku transferu, a proto používají stejnou instanci na okně **Řádky sledování zboží**. To znamená, že sledovací čísla zboží dodávaná z jedné lokace musí být přijata beze změny na druhé lokaci.  

 Přesná pravidla pro zpracování čísel sledování zboží ve vaší společnosti se řídí nastavením tabulky **Kód sledování zboží**.    
1.  Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "Hledat ikonu stránky nebo sestavy"), zadejte **Objednávky transferu** a poté vyberte související odkaz.  
2.  Otevřete objednávku transferu, kterou chcete zpracovat. Na záložce **Řádky** vyberte akci **Řádek**, vyberte akci **Řádky sledování zboží** a pak vyberte akci **Dodávka**.  
3.  V okně **Řádky sledování zboží** přiřaďte nebo vyberte sériová čísla nebo čísla šarže jako u jakékoli jiné odchozí transakce zboží.  

    Při manipulaci se sériovými čísly a čísly šarží pro zboží transferu má zboží obvykle již přiřazená čísla. Proto proces obvykle sestává z výběru ze stávajících sériových čísel nebo čísel šarží.  

4.  Zašlete příkaz k převodu, nejprve zasílejte a poté přijměte, abyste zaznamenali, že je zboží převedeno s položkami sledování zboží.  

Během přenosu zůstane okno **Řádky sledování zboží** zamčena pro zápis.  

## <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Zpracování sériových čísel a čísel šarží z řádků nákupní faktury  
Pokud pomocí funkce získáte řádky zaúčtovaného dokladu nebo dodávky ze souvisejících faktur nebo dobropisů, pak se všechny řádky pro sledování zboží v dokladech skladu přenášejí automaticky, jsou však zpracovávány zvláštním způsobem.

Funkce podporuje následující příchozí procesy:  
-   **Kopie řádků příjemky** - z kupní faktury.  
-   **Kopie řádků dodávky vratky** - z dobropisu na nákup.  

Funkce podporuje následující výstupní procesy:  
-   **Kopie řádků dodávky** - z prodejní faktury nebo kombinovaných dodávek.  
-   **Kopie řádků příjemky vratky** - z dobropisu na prodej.  

V těchto situacích se stávající řádky pro sledování zboží zkopírují automaticky do faktury nebo dobropisu, ale okno **Řádky sledování zboží** neumožňuje změny sériových čísel nebo čísel šarží. Změnit lze pouze množství.  

1.  Zvolte pravém horním rohu zvolte ikonu ![Vyhledat stránku nebo sestavu] (media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Nákupní faktury** a vybete související odkaz.  
2.  Otevřete nákupní fakturu pro zboží, které je zakoupeno se sériovým číslem nebo číslem šarže.  
3.  Na řádku prodejní faktury na záložce **Řádky** vyberte akci **Kopie řádků příjemky**.  
4.  V okně **Kopie řádků příjemky** vyberte řádky příjemky, které mají řádky pro sledování zboží, a poté klepněte na tlačítko **OK**.  

    Zdrojový dokument je zkopírován do nákupní faktury jako nový řádek a jeho řádky pro sledování zboží jsou zkopírovány na podkladové okno **Řádky sledování zboží**.  

5.  Na nákupní faktuře vyberte převedený řádek příjemky.  
6.  Na záložce **Řádky** vyberte akci **Řádek** a poté vyberte akci **Řádky sledování zboží**, abyste viděli převedené řádky sledování zboží.  

Obsah polí **Sériové číslo** a **Číslo šarže** nelze upravovat. Můžete však odstranit celé řádky nebo změnit množství tak, aby odpovídaly změnám na zdrojovém řádku.  

## <a name="to-reclassify-serial-or-lot-numbers"></a>Přeřazení sériových čísel nebo čísel šarží  
Přeřazení sledování zboží u zboží znamená změnu šarže nebo sériového čísla na novou šarži nebo sériové číslo nebo změnu data vypršení platnosti na nové datum vypršení platnosti. Pokud pracujete se šaržemi, můžete také sloučit více šarží do jedné. Tyto úkoly provádíte pomocí deníku přeřazení zboží.

1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deníky zboží** a poté vyberte související odkaz.  
2.  Vyplňte řádek s příslušnými informacemi. Pro více informací navštivte [Vypočítat, upravovat a přeřazovat zásoby](inventory-how-count-adjust-reclassify.md).
3.  Vyberte akci **Řádky sledování zboží**.  
4.  V poli **Sériové číslo** nebo **Číslo šarže** vyberte aktuální sériové číslo nebo číslo šarže.  
5.  Pokud chcete zadat nové číslo sledování zboží, zadejte jej do pole **Nové sériové číslo** nebo **Nové číslo šarže**. Pokud chcete, můžete sloučit jednu nebo více šarží do jedné nové nebo existující šarže.  

    > [!NOTE]  
    >  Uvědomte si, že když přeřadíte data expirace, budou nejprve navrženo zboží s nejčasnějšími daty expirace pro odchozí transakce. Pro více informací navštivte [Vyskladnění pomocí FEFO](warehouse-picking-by-fefo.md).  

5.  Pokud chcete zadat nové datum expirace sériového čísla nebo čísla šarže, zadejte je do pole **Nové datum expirace**.  

    > [!IMPORTANT]  
    >  Pokud přeřadíte šarži na stejné číslo šarže, ale s jiným datem expirace, musíte přeřadit celou šarži pomocí jednoho řádku deníku přeřazení zboží. Pokud přeřadíte více než jednu šarži na jedno nové číslo šarže, což znamená, že slučujete více šarží do jedné nové šarže, musíte pro všechny šarže zadat stejné nové datum expirace. Pokud přeřadíte jednu existující šarži na druhou existující šarži, která má jiné datum exspirace, musíte použít datum exspirace z druhé šarže. Pokud necháte pole **Nové datum expirace** prázdné, bude šarže nebo sériové číslo přeřazeno s prázdným datem expirace.  

6.  Pokud již máte informace o starém sériovém čísle nebo čísle šarže, můžete je zkopírovat na nové sériové číslo nebo číslo šarže.  

    1.  V okně **Řádky sledování zboží** vyberte akci **Informace o novém sériovém čísle** nebo **Informace o novém čísle šarže**.  
    2.  Chcete-li zkopírovat informace ze staré šarže nebo sériového čísla, vyberte akci **Kopírovat informace**.  
    3.  V okně se seznamem informací vyberte číslo šarže nebo sériové číslo, ze kterého chcete kopírovat, a stiskněte tlačítko **OK**.  

7.  Pokud chcete upravit existující informace o šarži nebo sériovém čísle, můžete zaznamenat informace šarže nebo sériové informace.  
8.  Zaúčtujte deník, abyste propojili obnovená sledovací čísla zboží nebo data expirace s položkou zboží.

## <a name="see-also"></a>Viz také
[Sledování zboží](inventory-how-to-trace-item-tracked-items.md)   
[Zásoby](inventory-manage-inventory.md)  
[Podrobnosti návrhu: Sledování zboží](design-details-item-tracking.md)
[Podrobnosti o návrhu- sledování a rezervace zboží](design-details-item-tracking-and-reservations.md)  
[Rezervace zboží](inventory-how-to-reserve-items.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
