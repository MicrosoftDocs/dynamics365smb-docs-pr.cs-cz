---
title: 'Výpočet, úprava a přeřazení zásob | Microsoft Docs'
description: 'Popisuje, jak provádět fyzické počítání, záporné nebo kladné úpravy a jak měnit informace, jako je lokace nebo číslo šarže, u položek zboží nebo položek skladu.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'adjustment, negative, positive, increase, decrease'
ms.date: 11/29/2017
ms.author: sgroespe
---
# <a name="count-adjust-and-reclassify-inventory"></a>Výpočet, úprava a přeřazení zásob
Alespoň jednou za fiskální rok musíte provést fyzickou inventuru, tj. spočítat všechno zboží ve skladu, abyste zjistili, zda je množství evidované v databázi stejné jako skutečné fyzické množství ve skladech. Je-li známo skutečné fyzické množství, musí být zaúčtováno do hlavní knihy jako součást ocenění zásob na konci období.

Ačkoli počítáte všechno zboží v inventáři alespoň jednou ročně, možná jste se rozhodli některé zboží počítat častěji, snad proto, že jsou cennější, nebo proto, že jsou velmi rychlými pohyby a velkou částí vašeho podnikání. Za tímto účelem můžete těmto zbožím přiřadit speciální období pro počítání. Pro více informací navštivte Provádění počítání cyklů.

Pokud potřebujete upravit zaznamenané množství zásob, v souvislosti s počítáním nebo pro jiné účely, můžete pomocí deníku zboží přímo měnit položky inventury bez účtování obchodních transakcí. Můžete také upravit samostatné zboží na kartě zboží.

Pokud potřebujete změnit atributy u položek zboží, můžete použít deník přeřazení zboží. Mezi typické atributy, které se mají přeřadit, patří dimenze a kódy prodejních kampaní, ale také třeba vykonat „systémové transfery“ přeřazením kódů bin a lokace. Pokud chcete přeřadit sériová čísla nebo čísla šarže a data jejich vypršení, platí zvláštní kroky. Pro více informací navštivte [Práce se sériovými čísly a čísly šarže](inventory-how-work-item-tracking.md).

> [!NOTE]
> V pokročilých konfiguracích skladů je zboží evidováno v přihrádkách jako položky skladu, nikoli jako položky zboží. Proto provádíte počítání, úpravy a přeřazení ve speciálních denících skladu, které podporují přihrádky. Poté pomocí speciálních funkcí synchronizujete nové nebo změněné položky skladu s jejich souvisejícími položkami zboží, aby odrážely změny v množstvích a hodnotách zásob. To je popsáno v konkrétních postupech níže.

## <a name="to-perform-a-physical-inventory"></a>Provádění fyzické inventury
Musíte provést fyzickou inventuru, tj. spočítat skutečné zboží na skladě, abyste zkontrolovali, zda evidované množství je stejné jako fyzické množství na skladě na konci fiskálního roku, ne-li častěji. Pokud existují rozdíly, musíte je před ohodnocením zásob zaúčtovat na účty zboží.

Kromě úlohy fyzického počítání zahrnuje celý proces následující tři úkoly:

- Výpočet očekávaného množství na skladě.
- Vytištění sestavy, která se použije při počítání.
- Zadání a zaúčtování skutečně spočítaných zásob.

Fyzickou inventuru můžete provést jedním z následujících způsobů v závislosti na nastavení vašeho skladu. Pro více informací navštivte [Nastavení správy skladu](warehouse-setup-warehouse.md).  

-   Pokud vaše lokace nepoužívá řízené zaskladnění/vyskladnění (základní konfigurace skladu), použijete stránku **Deník fyzické inventury** v nabídce **Zásoby** a postup je téměř stejný jako při provádění fyzické inventury bez cyklické inventury.  
-   Pokud vaše lokace používá řízené zaskladnění/vyskladnění (pokročilá konfigurace skladu), nejprve použijte okno **Deník fyz. inventury  skladu** a poté pomocí okna **Deník zboží** spusťte funkci **Vypočítat  adjustace skladu**.

### <a name="to-calculate-the-expected-inventory-in-basic-warehouse-configurations"></a>Výpočet očekávaného množství na skladě v základních konfiguracích skladu
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deníky  fyzické inventury** a poté vyberte související odkaz.
2. Vyberte akci **Vypočítat množství zásob**.
3. V okně **Vypočítat množství zásob** určete podmínky, které se mají použít k vytvoření řádků deníku, například zda zahrnout zboží, které má nulovou evidovanou zásobu.
4. Nastavte filtry, pokud chcete vypočítat inventury pouze pro určité zboží, přihrádky, lokace nebo dimenze.
5. Zvolte tlačítko **OK**.

> [!NOTE]  
>   Položky zboží jsou zpracovávány podle zadaných informací a řádky jsou vytvářeny v deníku fyzické inventury. Všimněte si, že pole **Množství (Fyz.inventura)** je automaticky vyplněno stejným množstvím jako pole **Množství (vypočtené)**. S touto funkcí není nutné zadávat počítané zásoby na skladě pro zboží, které jsou stejné jako vypočtené množství. Pokud se však vypočítané množství liší od toho, co je zadáno do pole **Množství (vypočtené)**, musíte jej přepsat skutečným vypočítaným množstvím.

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Výpočet očekávaného množství na skladě v pokročilých konfiguracích skladu
1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deník zboží** a pak vyberte související odkaz.  
2.  Vyberte akci **Výpočet adjustace skladu**.  
3.  Vyplňte okno žádosti o dávkovou úlohu čísly zboží, které chcete spočítat, a svou lokaci.
4. Vyberte tlačítko **OK** a zaúčtujte změny, pokud existují.

    Pokud tak neučiníte před provedením fyzické inventury skladu, výsledky, které zaúčtujete do deníku fyzické inventury a položek zboží ve druhé části procesu, budou výsledky fyzické inventury kombinované s dalšími úpravami skladu pro zboží, které byly spočítané.  
5.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deník  fyzické  inventury skladu** a poté vyberte související odkaz.  
6. Vyberte akci **Vypočítat množství zásob**. Otevře se stránka dávkové úlohy **Výpočet zásob skladu**.  
7.  Nastavte filtry tak, aby omezovaly zboží, které bude započítávané do deníku, a poté zvolte tlačítko **OK**.

    Program vytvoří řádek pro každou přihrádku, která splňuje požadavky na filtr. V tomto okamžiku můžete některé řádky odstranit, ale pokud chcete výsledky zaúčtovat jako fyzickou inventuru, musíte zboží spočítat ve všech přihrádkách, které jej obsahují.  

     Pokud máte pouze čas spočítat zboží jenom v některých přihrádkách, ne ve všech, můžete odhalit nesrovnalosti, zaregistrovat je a později je zaúčtovat v deníku zboží pomocí funkce **Výpočet adjustace skladu**.  
8.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deník fyzické inventury skladu** a vyberte související odkaz.  
9.  Otevřete stránku dialog sestavy a vytiskněte seznamy, na kterých mají zaměstnanci zaznamenávat množství zboží, které počítají v každé přihrádce.  
10. Po dokončení počítání zadejte počet kusů do pole **Množství (fyz. Inventura)** v deníku fyzické inventury skladu.  

    > [!NOTE]  
    >  V deníku fyzické inventury skladu, se pole **Množství (vypočtené)** vyplní automaticky na základě záznamů ze skladu a tyto kopie se zkopírují do pole **Množství (fyzické)** na každém řádku. Pokud se množství počítané zaměstnancem skladu liší od toho, co program zadal do pole Množství. (Fyzické), musíte zadat skutečně spočítané množství.  

11. Po zadání všech počítaných množství vyberte akci **Zápis**.  

    Když zapíšete deník, program vytvoří dvě položky skladu v žurnály skladu pro každý řádek, který byl spočítán a zapsán:  

    -   Pokud se vypočtené a fyzické množství liší, zaregistruje se do přihrádky záporné nebo kladné množství a vyrovnávací množství se zaúčtuje do vyrovnávací přihrádky lokace.  
    -   Pokud se vypočítané množství rovná fyzickému množství, program zaregistruje položku 0 pro přihrádku i pro adjustační přihrádka. Položky jsou záznamy, které k datu zápisu byly provedeny fyzickou inventurou skladu a nedošlo k žádnému rozporu v zásobě zboží.  

Když zapíšete fyzickou inventuru skladu, nezaúčtuje se do knihy zboží, do knihy fyzické inventury nebo do knihy ocenění, ale záznamy jsou k dispozici pro okamžité odsouhlasení, kdykoli to bude nutné. Pokud však chcete vést přesné záznamy o tom, co se děje ve skladu, a započítali jste všechny přihrádky, ve kterých bylo zboží zapsáno, měli byste okamžitě zaúčtovat výsledky skladu jako fyzický inventář zásob. Pro více informací navštivte sekci „Zadání a zaúčtování aktuálně počítaného inventáře v pokročilých konfiguracích skladu“.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Tisk sestavy, která se použije při počítání
1. V okně **Deník  fyzické inventury** obsahující vypočítaný očekávaný inventář vyberte akci **Tisk**.
2. V okně **Deník fyzické inventury** určete, zda by se v sestavě mělo zobrazit vypočtené množství a zda by se v sestavě mělo zobrazovat zboží soupisu podle sériových čísel nebo čísel šarže.
3. Nastavte filtry, pokud chcete tisknout sestavu pouze pro určité zboží, přihrádky, lokace nebo dimenze.
4. Zvolte tlačítko **Tisk**.

Zaměstnanci nyní mohou začít počítat zásoby a zaznamenávat jakékoli nesrovnalosti ve vytištěné sestavě.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Zadání a zaúčtování aktuálně počítané inventury v základních konfiguracích skladu
1. Na každém řádku v okně **Deník  fyzické inventury**, kde se skutečné zásoby na skladě, stanovené fyzickým počtem, liší od vypočteného množství, zadejte skutečné množství zásob na skladě do pole **Množství (fyz. inventura)**.

    Související pole jsou odpovídajícím způsobem aktualizována.

    > [!NOTE]  
   >   Pokud fyzický počet odhalí rozdíly způsobené zbožím zaúčtovaným s nesprávnými kódy lokace, nezadávejte rozdíly v deníku fyzických zásob. Místo toho použijte k přeřazení zboží na správnou lokaci deník přeřazení nebo objednávku transferu. Pro více informací navštivte Deník přeřazení zboží nebo Vytváření objednávek transferu.

2. Chcete-li upravit vypočtená množství na skutečná počítaná množství, vyberte akci **Účtovat**.

    Vytvoří se položky zboží i položky fyzické inventury. Otevřete kartu zboží a zobrazte výsledné položky fyzické inventury.

3. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Zboží** a pak vyberte související odkaz.
4. Chcete-li ověřit počítání inventury, otevřete dotyčnou kartu zboží a poté vyberte akci **Položky fyzické inventury**.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Zadání a zaúčtování aktuálně počítané inventury v pokročilých konfiguracích skladu

1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deník zboží** a pak vyberte související odkaz.  
2.  Vyberte akci **Výpočet adjustace skladu**.  
3.  Vyberte stejné zboží, které jste započítali ve fyzické inventuře počítání cyklů, který jste právě provedli, a všechno další zboží, které vyžaduje úpravu, a poté stiskněte tlačítko **OK**.  

     Otevře se okno **Deník zásob** a pro toto zboží se vytvoří řádky. Pamatujte, že čistá množství, která jste právě spočítali a zapsali přihrádku po přihrádce, jsou nyní připravena ke konsolidaci a synchronizaci jako položky zboží.  

4.  Zaúčtujte deník beze změny množství.  

Množství v položkách zboží a množství ve skladu (položky skladu) jsou nyní opět stejné pro toto zboží a program aktualizoval poslední datum počítání zboží nebo skladové jednotky.  

## <a name="to-perform-cycle-counting"></a>Provádění počítání cyklů
Ačkoli počítáte všechno zboží v inventáři alespoň jednou ročně, možná jste se rozhodli některé zboží počítat častěji, snad proto, že jsou cennější, nebo proto, že jsou velmi rychlými pohyby a velkou částí vašeho podnikání. Za tímto účelem můžete těmto zbožím přiřadit speciální období pro počítání.

Počítání cyklů můžete provést jedním z následujících způsobů v závislosti na nastavení vašeho skladu. Pro více informací navštivte [Nastavení správy skladu](warehouse-setup-warehouse.md).  

-   Pokud vaše lokace nepoužívá řízené zaskladnění/vyskladnění (základní konfigurace skladu), použijete stránku **Deník fyzické inventury** v nabídce **Zásoby** a postup je téměř stejný jako při provádění fyzické inventury bez cyklické inventury.  
-   Pokud vaše lokace používá řízené zaskladnění/vyskladnění (pokročilá konfigurace skladu), nejprve použijte okno **Deník fyzické inventury skladu** a poté pomocí okna **Deník zboží** spusťte funkci **Vypočítat adjustace skladu**.  

### <a name="to-set-up-counting-periods"></a>Nastavení období počítání
Fyzická inventura se obvykle provádí v opakujících se intervalech, například měsíčně, čtvrtletně nebo ročně. Můžete nastavit libovolná nezbytná období počítání zásob.

Nastavíte období počítání zásob, které chcete použít, a pak každému zboží přiřadíte jedno. Když provedete fyzickou inventuru a použijete **Vypočítat období inventury** v deníku fyzické inventury, automaticky se vytvoří řádky pro zboží.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deníky fyzické  inventury** a pak vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Přiřadění období inventury ke zboží  
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Zboží** a pak vyberte související odkaz.  
2. Vyberte zboží, kterému chcete přiřadit období inventury.  
3. V poli **Kód období fyzické inventury** vyberte příslušné období inventury.  
4. Stisknutím tlačítka **Ano** změníte kód a vypočítáte první období inventury pro zboží. Při příštím výběru výpočtu období inventury v deníku fyzického inventáře se zboží zobrazí jako řádek v okně **Výběr  fyzické inventury**. Poté můžete začít pravidelně počítat zboží.

### <a name="to-initiate-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Inicializace počtu na základě období inventury v základních konfiguracích skladu
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deníky inventury** a pak vyberte související odkaz.
2. Vyberte akci **Vypočítat období inventury**.

    Otevře se stránka **Výběr fyzické zboží**, kde kde je zobrazené zboží, které má přiřazené období inventury a musí být dopočítáno podle jejich období inventury.
3. Provádění fyzické inventury. Pro více informací navštivte Provádění počítání cyklů.

### <a name="to-initiate-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Inicializace počtu na základě období inventury v pokročilých konfiguracích skladu
1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deník fyzické fyzické skladu** a poté vyberte související odkaz.  
2. Vyberte akci **Vypočítat období inventury**.

    Otevře se stránka **Výběr fyzické zboží**, kde kde je zobrazené zboží, které má přiřazené období inventury a musí být dopočítáno podle jejich období inventury.
3. Provádění fyzické inventury. Pro více informací navštivte sekci „Provádění fyzické inventury“.  

    > [!NOTE]  
    >  Musíte spočítat zboží ve všech přihrádkách, které obsahují konkrétní zboží. Pokud odstraníte některé řádky přihrádky, které program načítal pro počítání v okně **Fyzické  fyzické skladu**, nebudete počítat všechno zboží ve skladu. Pokud později zaúčtujete takové neúplné výsledky v Deníku fyzické inventury, budou zveřejněné částky nesprávné.  

## <a name="to-adjust-the-inventory-of-one-item"></a>Úprava zásob jednoho zboží
Po provedení sčítaní fyzického počtu zboží ve skladě můžete pomocí funkce **Upravit zásoby** zaznamenat skutečné množství zásob.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Zboží** a pak vyberte související odkaz.
2. Vyberte zboží, pro které chcete upravit zásoby, a poté vyberte akci **Upravit zásoby**.
3. Do pole **Nové zásoby** zadejte množství zásob, které chcete pro zboží zaznamenat.
4. Zvolte tlačítko **OK**.

Zásoby zboží jsou nyní upraveny. Nové množství se zobrazí v poli **Aktuální zásoby**, v okně **Upravit zásoby** a v poli **Zásoby** v okně **Karty zboží**.

Funkci **Upravit zásoby** můžete také použít jako jednoduchý způsob umisťování zakoupeného zboží do skladu, pokud k zaznamenávání svých nákupů nepoužíváte nákupní faktury nebo objednávky. Pro více informací navštivte [Evidence nákupu](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Po úpravě zásob musíte aktualizovat aktuální vypočtenou hodnotu. Pro více informací navštivte [Přeceňovaní zásob](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-inventory-quantity-of-multiple-items-in-basic-warehouse-configurations"></a>Úprava množství zásob více zboží v základních konfiguracích skladu
V okně **Deníku zboží** můžete zaúčtovat transakci přímo a upravit zásoby v souvislosti s nákupy, prodejem a kladnými nebo zápornými úpravami bez použití dokladů.

Pokud často používáte deník zboží k zaúčtování stejných nebo podobných řádků deníku, například v souvislosti se spotřebou materiálu, můžete tuto opakující se práci usnadnit pomocí okna **Standardní deník zboží**. Pro více informací navštivte sekci „Standardní deníky“ v [Práce s Finančními deníky](ui-work-general-journals.md).

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deník zboží** a pak vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Chcete-li provést úpravy zásob, vyberte akci **Účtovat**.

> [!NOTE]  
>   Po úpravě zásob musíte aktualizovat aktuální vypočítanou hodnotu. Pro více informací navštivte [Přeceňovaní zásob](inventory-how-revalue-inventory.md).

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Nastavení množství přihrádek v pokročilých konfiguracích skladu  
Pokud vaše lokace používá řízené zaskladnění a vyskladnění, použijte **Deník zboží skladu** k účtování, mimo kontextu fyzické inventury, všechny pozitivní a negativní úpravy v počtu zboží, o kterých víte, že jsou skutečné zisky, jako například zboží dříve zaúčtováno jako chybějící, které se projeví neočekávaně nebo jako skutečné ztráty, například rozbití.  

Na rozdíl od účtování adjustace zásob deníkem zboží, pomocí deníku zboží skladu získáte další úroveň úprav, díky níž jsou záznamy o množství ještě přesnější. Sklad má tedy vždy kompletní záznam o tom, kolik zboží je na skladě a kde je uloženo, ale žádná registrace úpravy se neúčtuje okamžitě do položek zboží. V procesu registrace jsou strany Má dáti nebo Dal provedeny do skutečné přihrádky s úpravou množství a do vyrovnávací přihrádky, virtuální přihrádky bez skutečných položek, je provedeno vyrovnávací zboží. Tato přihrádka je definována v **kódu adjustační přihrádky** na kartě lokace.

1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deník Zboží** a pak vyberte související odkaz.  
2.  Vyplňte informace v záhlaví.  
3.  Vyplňte pole **Číslo zboží** na řádku.  
4.  Zadejte přihrádku, do které vkládáte další zboží nebo kde jste našli zboží, které chybí.  
5.  Do pole **Množství** zadejte množství, které považujete za nesrovnalost. Pokud jste našli zboží navíc, zadejte kladné množství. Pokud zboží chybí, zadejte záporné množství.  
6.  Zvolte akci **Zápis**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Synchronizace upraveného zboží skladu s příslušnými položkami zboží
Ve vhodných intervalech, jak je definováno v zásadách společnosti, musíte zaúčtovat záznamy adjustační přihrádky skladu do položek zboží. Některé společnosti považují za vhodné zaúčtovat úpravy do položek zboží každý den, zatímco jiné mohou považovat za vhodné účtovat méně často.

1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deník zboží** a pak vyberte související odkaz.  
2.  Vyplňte pole na každém řádku deníku.  
3.  Vyberte akci **Výpočet adjustace skladu** a vyplňte filtry podle potřeby v okně požadavku dávkové úlohy. Úpravy se počítají pouze pro zboží v adjustační přihrádce, které splňuje požadavky na filtr.  
4.  Na záložce **Možnosti** vyplňte pole **Číslo dokladu** číslem, které zadáte ručně. Protože pro tuto dávkovou úlohu nebyla nastavena žádná číselná řada, použijte číselné schéma nastavené ve skladu nebo zadejte datum, za kterým následují vaše iniciály.  
5.  Zvolte tlačítko **OK**. Kladné a záporné úpravy se sčítají pro každé zboží a v deníku zboží se vytvoří řádky pro všechno zboží, u kterého je součet kladné nebo záporné množství.  
6.  Zaúčtováním řádků deníku zadejte rozdíly v množství v položkách zboží. Inventura v přihrádkách skladu nyní přesně odpovídá inventáři v položkách zboží.  

## <a name="to-reclassify-an-items-lot-number"></a>Přeřazení čísla šarže zboží
Pokud potřebujete změnit atributy u položek zboží, můžete použít deník přeřazení zboží. Mezi typické atributy, které se mají přeřadit, patří dimenze a kódy prodejních kampaní, ale také třeba vykonat „systémové transfery“ přeřazením kódů bin a lokace.

Pokud chcete přeřadit sériová čísla nebo čísla šarže a data jejich vypršení, platí zvláštní kroky. Pro více informací navštivte [Práce se sériovými čísly a čísly šarže](inventory-how-work-item-tracking.md).

Následující příklad je založen na kódu lokace. Kroky jsou podobné pro další typy atributů zboží.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Deníky  přeřazení zboží** a poté vyberte související odkaz.
2. V okně **Deníku  přeřazení zboží** vyplňte pole podle potřeby.
3. Do pole **Kód lokace** zadejte aktuální kód lokace zboží.
4. Do pole **Kód nové lokace** zadejte nový kód lokace zboží.
5. Zvolte akci **Zaúčtovat**.

Informace o převodu zboží s plnou kontrolou odeslaného a přijatého množství naleznete v části [Převod zásob mezi lokacemi](inventory-how-transfer-between-locations.md).

## <a name="see-also"></a>Viz také
[Zásoby](inventory-manage-inventory.md)
[Správa skladu](warehouse-manage-warehouse.md)    
[Prodej](sales-manage-sales.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
