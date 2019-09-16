---
title: Nastavení speciálních prodejních cen a slev pro zákazníky | Microsoft Docs
description: 'Popisuje, jak definovat alternativní dohody o cenách a slevách, které chcete použít pro prodejní faktury při prodeji různým zákazníkům.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'special price, alternate price, pricing'
ms.date: 11/28/2018
ms.author: sgroespe
---
# <a name="record-special-sales-prices-and-discounts"></a>Záznam speciálních prodejních cen a slev
Různé dohody o cenách a slevách, které se uplatňují při prodeji různým zákazníkům, musí být definovány tak, aby se dohodnutá pravidla a hodnoty uplatňovaly na prodejní dokumenty, které pro zákazníky vytvoříte.

Pokud jste zaznamenali speciální ceny a řádkové slevy za prodej a nákupy, [!INCLUDE[d365fin](includes/d365fin_md.md)] zajistí, že váš zisk z obchodu se zbožím je vždy optimální automatickým výpočtem nejlepší ceny na prodejních a nákupních dokladech a na řádcích deníků zboží a projektů. Pro více informací navštivte [Výpočet nejlepší ceny](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Pokud jde o ceny, můžete na prodejních řádcích vložit speciální prodejní ceny, pokud existuje určitá kombinace zákazníka, zboží, minimálního množství, měrné jednotky nebo data zahájení / ukončení.

Pokud jde o slevy, můžete nastavit a použít dva typy prodejních slev:

| Typ slevy | Popis |
| --- | --- |
| **Prodejní řádkové slevy** |Pokud existuje určitá kombinace zákazníka, zboží, minimálního množství, měrné jednotky nebo data zahájení / ukončení, může být na prodejní řádek vložena speciální množstevní sleva. Toto funguje stejně jako u prodejních cen. |
| **Fakturační sleva** |Procentní sleva, která je odečtena od celkové částky faktury, pokud hodnota všech řádků v prodejním dokladu překročí určité minimum. |

Protože prodejní ceny a prodejní řádkové slevy jsou založeny na kombinaci zboží a zákazníka, můžete tuto konfiguraci provést také z karty zboží, kde platí pravidla a hodnoty.

> [!NOTE]  
> Pokud si nepřejete, aby se zboží někdy prodávalo za zvýhodněnou cenu, jednoduše ponechte na kartě položky pole slev prázdné a nezahrnujte zboží do žádného nastavení řádkové slevy.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Nastavení prodejní ceny pro zákazníka
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") ikona, zadejte **Zákazníci**, a poté vyberte související odkaz.
2. Otevřete příslušnou kartu zákazníka a pak zvolte akci **Ceny**.

    Pole**Typ nákupu** je předvyplněno **Zákazník** a pole **Kód nákupu** je vyplněno číslem zákazníka.
3. Vyplňte pole na řádku podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vyplňte řádek pro každou kombinaci, která zákazníkovi poskytne speciální prodejní cenu.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Nastavení prodejní řádkové slevy pro zákazníka
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") ikona, zadejte **Zákazní**, a poté vyberte související odkaz.
2. Otevřete příslušnou kartu zákazníka a pak zvolte akci **Řádková sleva**.

    Pole**Typ nákupu** je předvyplněno **Zákazník** a pole **Kód nákupu** je vyplněno číslem zákazníka.
3. Vyplňte pole na řádku podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vyplňte řádek pro každou kombinaci, která zákazníkovi poskytne prodejní řádkovou slevu.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Nastavení slevy na faktuře pro zákazníka
Pokud jste se rozhodli, kteří zákazníci mají nárok na slevy na faktuře, zadejte kód zákaznické faktury na zákaznické karty a pro každý kód nastavte podmínky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") ikona, zadejte **Zákazníci**, a poté vyberte související odkaz.
2. Otevřete zákaznickou kartu od zákazníka, který bude mít nárok na slevy na faktuře.
3. V poli **Kód fakturační  slevy** vyberte kód pro příslušné podmínky slev na faktuře, které chcete použít pro výpočet slev na faktuře pro zákazníka.

> [!NOTE]  
>   Kódy fakturační slevy jsou představovány stávajícími zákaznickými kartami. To Vám umožní rychle přiřadit smluvní podmínky slevy na faktuře výběrem jména jiného zákazníka, který bude mít stejné podmínky.

Pokračujte v nastavování nových podmínek slev z prodejní faktury.

1. Na stránce **Karta zákazníka**, vyberte akci **Fakturační slevy**. **Zák. fakturační slevy**.
2. Do pole **Kód měny** zadejte kód měny, na kterou se vztahují podmínky slevy z faktury na řádku. Chcete-li nastavit podmínky slevy z faktury v USD, ponechte pole prázdné.
3. Do pole **Minimální částka** zadejte minimální částku, kterou musí faktura obsahovat, aby vznikl nárok na slevu.
4. Do pole **Sleva %** zadejte slevu z faktury jako procento z částky faktury.
5. Opakujte kroky 5 až 7 pro každou měnu, za kterou zákazník obdrží jinou fakturační slevu.

Fakturační sleva je nyní nastavena a přiřazena dotyčnému zákazníkovi. Když vyberete zákaznický kód v **Kód fakturační  slevy**, na různých zákaznických kartách je  pak těmto zákazníkům přidělena stejná fakturační sleva.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Práce s fakturačními slevami prodejních faktur a servisními poplatky.
Když použijete fakturační slevy, velikost faktury určuje velikost poskytnuté slevy.  

Na stránce **Zák. fakturační slevy**, můžete také k fakturám za určitou částku přidat servisní poplatek.  

Než budete moci použít během prodeje fakturační slevy, musíte do programu zadat určité informace. Musíte se rozhodnout:  

- kterým zákazníkům bude tento typ slevy poskytnut.  
- jaká procenta slev použijete.  

Pokud fakturujete slevy, které chcete vypočítat automaticky, tak je můžete zadat na stránce **Nastavení prodeje a pohledávek**.  

U každého zákazníka můžete specifikovat, zda udělíte fakturační slevy, jestliže je splněn uvedený požadavek (tj. Je-li částka faktury dostatečně velká). Podmínky fakturační slevy můžete definovat v místní měně pro tuzemské zákazníky a v cizí měně pro zahraniční zákazníky.  

Propojíte procenta slev se specifickými částkami faktur na stránce **Zák. fakturační slevy**. Na každou stránku můžete zadat libovolný počet procent. Každý zákazník může mít svou vlastní stránku nebo můžete na stejnou stránku připojit několik zákazníků.  

Kromě (nebo namísto) procenta slevy můžete propojit částku servisního poplatku s konkrétní částkou faktury.  

> [!TIP]  
>  Než začnete zadávat tyto informace do programu, je vhodné připravit si osnovu struktur slev, kterou budete chtít použít. To nám usnadní zjistit, kteří zákazníci mohou být propojeni na stejnou stránku fakturační slevy. Čím méně stránek musíte nastavit, tím rychleji můžete zadat základní informace.  

## <a name="best-price-calculation"></a>Výpočet nejlepší ceny
Pokud jste zaznamenali speciální ceny a řádkové slevy za prodej a nákupy, [!INCLUDE[d365fin](includes/d365fin_md.md)] zajistí, že váš zisk z obchodu se zbožím je vždy optimální automatickým výpočtem nejlepší ceny na prodejních a nákupních dokladech a na řádcích deníků zboží a projektů.

Nejlepší cena je nejnižší přípustná cena s nejvyšší přípustnou řádkovou slevou k danému datu. [!INCLUDE[d365fin](includes/d365fin_md.md)] Automaticky je vypočteno, když vloží jednotkovou cenu a procento řádkové slevy pro zboží na nových řádcích dokladu a deníku.

> [!NOTE]  
>   Následující text popisuje, jak je pro prodej vypočítána nejlepší cena. Výpočet je stejný pro nákupy.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] zkontroluje kombinaci plátce a zboží a poté vypočítá použitelnou jednotkovou cenu a procentuální řádkovou slevu pomocí následujících kritérií:

    - Má zákazník dohodu o cenách/slevách, nebo patří do skupiny, která slevy má?
    - Je zboží nebo skupina slev zboží na řádku zahrnuta v některé z těchto dohod o cenách/slevách?
    - Je datum objednávky (nebo datum zaúčtování faktury a dobropisu) v rozmezí počátečního a koncového data dohody o ceně/slevě?
    - Je zadán kód měrné jednotky? Pokud ano, [!INCLUDE[d365fin](includes/d365fin_md.md)] zkontrolujte ceny/slevy se stejným kódem měrné jednotky a ceny/slevy bez kódu měrné jednotky.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] zkontroluje, zda se nějaké dohody o ceně/slevě nevztahují na informace v dokladu nebo v řádku deníku a poté vloží příslušné jednotkové ceny a procentuální řádkovou slevu, a to pomocí následujících kritérií:

    - Existuje v dohodě o ceně/slevě požadavek na minimální množství, který je splněn?
    - Existuje v dohodě o ceně/slevě požadavek na měnu, který je splněn? Pokud ano, bude vložena nejnižší cena a nejvyšší řádková sleva pro tuto měnu, a to i v případě, že by místní měna poskytovala lepší cenu. Pokud pro zadaný kód měny neexistuje dohoda o ceně/slevě, [!INCLUDE[d365fin](includes/d365fin_md.md)] vloží nejnižší cenu a nejvyšší řádkovou slevu ve Vaší lokální měně.

Pokud pro zboží na řádku nelze vypočítat žádnou speciální cenu, je vložen buď poslední přímý náklad, nebo jednotková cena z karty zboží.

## <a name="to-copy-sales-prices"></a>Kopírování prodejních cen  
Pokud chcete kopírovat prodejní ceny, jako například prodejní ceny jednotlivého zákazníka, které chcete použít pro cenovou skupinu zákazníka, musíte spustit **Navrhnout cenu z ceny**  dávkovou úlohu. Na stránce **Sešit prodejní ceny** můžete pro dávkovou úlohu spustit akci.    

1.  Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Sešit prodejní ceny** a poté vyberte související odkaz.  
2.  Vyberte **Navrhnout cenu z ceny**  tlačítko.  
3.  Na záložce s náhledem **Prodejní ceny** vyplňte pole **Typ prodeje** a **Kód prodeje** původními prodejními cenami, které chcete kopírovat.  
4.  V horní části stránky s požadavkem vyplňte pole **Typ prodeje** a **Kód prodeje** typem a názvem, do kterých chcete prodejní ceny kopírovat.  
5.  Pokud chcete, aby dávková úloha vytvořila nové ceny, zaškrtněte políčko **Vytvořit nové ceny**.  
6.  Vyberte tlačítko **OK** pro vyplnění řádků na stránce **Sešitu prodejní ceny** navrhovanými cenami, které označují, že jsou platné pro vybraný typ prodeje.  

> [!NOTE]  
>  Tato dávková úloha vytvoří pouze návrhy a neimplementuje navržené změny. Pokud jste s návrhy spokojeni a chcete je implementovat, to znamená vložit je na stránku **Prodejní ceny**, zvolte akci **Provést změnu ceny** na stránce **Sešit prodejní ceny**.

## <a name="to-bulk-update-item-prices"></a>Hromadná aktualizace cen zboží   
Pokud chcete hromadně aktualizovat ceny položek, jako například zvýšit všechny ceny zboží o určité procento, musíte spustit **Navrhnout cenu ze zboží** dávkovou úlohu. Na stránce **Sešit prodejní ceny** můžete najít odkaz na dávkovou úlohu.     

1.  Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Sešit prodejní ceny** a poté vyberte související odkaz.   
2.  Vyberte **Navrhnout cenu ze zboží** tlačítko.   
3.  Na záložce s náhledem **Zboží**, vyplňte **Ne** nebo **Účto skupina zboží** anebo jiná pole s původními cenami zboží, které chcete aktualizovat.   
4.  V horní části stránky s požadavkem vyplňte **Typ prodeje** a **Kód prodeje** typem a názvem, do kterých chcete prodejní ceny kopírovat.
5.  Pokud chcete, aby dávková úloha automaticky upravila navržené ceny zboží, zadejte úpravu do pole **Faktor úpravy**. Například pro 15% zvýšení ceny zboží zadáte 1,15 v **Faktoru úpravy** .  
6.  Pokud chcete, aby dávková úloha vytvořila nové ceny, vyberte pole **Vytvořit nové ceny**.   
7.  Vyberte tlačítko **OK** pro vyplnění řádků na stránce **Sešitu prodejní ceny** navrhovanými cenami, které označují, že jsou platné pro vybrané **Zboží**.   

> [!NOTE]   
>  Tato dávková úloha vytvoří pouze návrhy a neimplementuje navržené změny. Pokud jste s návrhy spokojeni a chcete je implementovat, to znamená vložit je do tabulky **Prodejní ceny**, můžete použít dávkovou úlohu **Provést změnu ceny**, která se nachází na záložce **Akce** ve skupině **Funkce** na stránce **Sešit prodejní ceny**.

## <a name="see-also"></a>Viz také
[Nastavení Prodeje](sales-setup-sales.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
