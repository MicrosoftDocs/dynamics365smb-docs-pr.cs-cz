---
title: Nastavení speciálních a alternativních cen a slev pro dodavatele | Microsoft Docs'
description: 'Můžete definovat zvláštní nebo alternativní ceny a dohody o slevách, a aplikovat je na nákupní doklady pro dodavatele.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'special price, alternate price, pricing'
ms.date: 07/03/2017
ms.author: sgroespe
---
# <a name="record-special-purchase-prices-and-discounts"></a>Zaznamenávání speciálních nákupních cen a slev
Různé smlouvy o cenách a slevách, které platí při nákupu od různých dodavatelů, musí být definovány tak, aby se dohodnutá pravidla a hodnoty vztahovaly na nákupní doklady, které pro dodavatele vytvoříte.

Pokud jste zaznamenali speciální ceny a řádkové slevy za prodej a nákupy, [!INCLUDE [d365fin](includes/d365fin_md.md)] zajistí, že váš zisk z obchodu se zbožím je vždy optimální automatickým výpočtem nejlepší ceny na prodejních a nákupních dokladech, a na řádcích deníků zboží a projektů. Pro více informací navštivte sekci "Výpočet nejlepší ceny".

Pokud jde o ceny, můžete do nákupních řádků vložit speciální nákupní cenu, pokud existuje určitá kombinace dodavatele, zboží, minimálního množství, měrné jednotky nebo počátečního/koncového data.

Pokud jde o slevy, můžete nastavit a použít dva typy nákupních slev:

| Typ slevy | Popis |
| --- | --- |
| **Sleva nákupního řádku** |Množstevní sleva, která je vložena na nákupní řádky, pokud existuje určitá kombinace dodavatele, zboží, minimálního množství, měrné jednotky nebo počátečního/koncového data. Toto funguje stejně jako u nákupních cen. |
| **Fakturační sleva** |Procentní sleva, která se odečte od celkové částky dokladu, pokud hodnota všech řádků na nákupním dokladu přesáhne určité minimum. |

Protože slevy na nákupních řádcích a nákupní ceny jsou založeny na kombinaci zboží a dodavatele, můžete tuto konfiguraci zadat také z karty zboží, kde jsou definována pravidla a hodnoty. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Nastavení speciálních nákupních cen pro dodavatele
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Dodavatelé** a pak vyberte související odkaz.
2. Vyberte příslušnou kartu dodavatele a pak zvolte akci **Ceny**.

    Pole **Typ nákupu** je předvyplněno **Dodavatelem** a pole **Kód nákupu** je vyplněno číslem dodavatele.
3. Vyplňte pole na řádku podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vyplňte řádek pro každou kombinaci, pro kterou vám dodavatel poskytne nákupní řádkovou slevu.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Chcete-li nastavit řádkovou slevu pro dodavatele
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Dodavatelé** a pak vyberte související odkaz.
2. Vyberte příslušnou kartu dodavatele a pak zvolte akci **Řádkové slevy**.

    Pole **Typ nákupu** je předvyplněno **Dodavatelem** a pole **Kód nákupu** je vyplněno číslem dodavatele.
3. Vyplňte pole na řádku podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vyplňte řádek pro každou kombinaci, pro kterou vám dodavatel poskytne nákupní řádkovou slevu.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Nastavení fakturační slevy pro dodavatele
Jakmile vás vaši dodavatelé informují o tom, které slevy z faktury poskytují, zadejte na kartách dodavatele kód slevy z faktury a nastavte podmínky pro každý kód.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Dodavatelé** a pak vyberte související odkaz.
2. Otevřete kartu dodavatele pro dodavatele, který bude mít nárok na slevy z faktury.
3. V části **Kód fakturační  slevy** vyberte kód pro příslušné podmínky slev z faktury, které chcete použít pro výpočet slev z faktury pro dodavatele.

    > [!NOTE]  
   >   Kódy slev z faktury jsou představovány existujícími kartami dodavatelů. To vám umožní rychle přiřadit dodavatelům podmínky slevy z faktury výběrem jmen dalších dodavatelů, kteří budou mít stejné podmínky.

    Pokračujte v nastavování nových podmínek slevy z nákupní faktury.
4. V okně **Karta dodavatele** vyberte akci **Fakturační slevy**. Otevře se okno **Dod.  fakturační slevy**.
5. Do pole **Kód měny** zadejte kód měny, na kterou se vztahují podmínky slevy z faktury na řádku. Chcete-li nastavit podmínky slevy z faktury v USD, ponechte pole prázdné.
6. Do pole **Minimální částka** zadejte minimální částku, kterou musí faktura obsahovat, aby vznikl nárok na slevu.
7. Do pole **Sleva %** zadejte slevu z faktury jako procento z částky faktury.
8. Opakujte kroky 5 až 7 pro každou měnu, pro kterou dodavatel obdrží jinou slevu z faktury.

Sleva z faktury je nyní nastavena a přiřazena dotyčnému dodavateli. Při výběru kódu dodavatele v části **Kód fakturační  slevy** na kartách dalších dodavatelů je těmto prodejcům přidělena stejná sleva z faktury.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Pro výběr principu účtování nákupních slev  
Když zaúčtujete nákupní fakturu, která obsahuje jednu nebo více slev, můžete si vybrat mezi dvěma principy pro účtování částek slev. Slevy můžete účtovat samostatně nebo je můžete odečíst z fakturačních slev.  

Než to budete moci udělat, budete muset mít již zřízené účty potřebné pro účtování částek slev do účetní osnovy. Musíte také zkontrolovat, zda jste zadali správná čísla účtů v nastavení obecného účtování v polích **Účet nákupní řádkové slevy** a **Účet  nákupní fakturační  slevy**.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Nastavení nákupů a závazků** a pak vyberte související odkaz.
2. V poli **Účtování slevy** vyberte jeden z následujících principů účtování slev.

|**Princip účtování slevy**|**Fakturační sleva**|**Řádková sleva**|  
|------------------------------------|--------------------------|-----------------------|  
|**Všechny slevy**|Účtováno samostatně|Účtováno samostatně|  
|**Fakturační slevy**|Účtováno samostatně|Odečteno|  
|**Řádkové slevy**|Odečteno|Účtováno samostatně|  
|**Žádné slevy**|Odečteno|Odečteno|  

# <a name="purchase-invoice-discounts-and-service-charges"></a>Slevy z nákupních faktur a poplatky za služby
Pokud máte u jakýchkoli dodavatelů pevně stanovené podmínky pro slevy z faktury, můžete je pro tyto dodavatele zadat. Sleva se poté vypočítá při vyplnění nákupní faktury.  

 Než budete moci u nákupů použít fakturační slevy, musíte určit dodavatele, kteří vám slevy nabízejí.  

 Procenta slev s konkrétními částkami faktury propojíte v sekci **Dodav.  fakturační slevy**. Do každého okna můžete zadat libovolný počet procent. Každý dodavatel může mít své vlastní okno, nebo můžete ke stejnému oknu připojit několik dodavatelů.  

 Kromě procenta slevy můžete také spojit částku poplatku za služby s konkrétní částkou faktury.  

 Podmínky slevy z faktury můžete definovat v lokální měně pro domácí dodavatele a v cizí měně pro zahraniční dodavatele.  

 Můžete si vybrat, zda chcete, aby [!INCLUDE [d365fin](includes/d365fin_md.md)] automaticky vypočítal slevy na fakturách pro nabídky, hromadné objednávky, objednávky, faktury nebo dobropisy.  

> [!TIP]  
>  Před zadáním těchto informací je vhodné připravit osnovu struktury slev, kterou chcete použít. Díky tomu je snazší zjistit, kteří dodavatelé mohou být spojeni se stejným oknem slevy z faktury. Čím méně oken musíte nastavit, tím rychleji můžete zadat základní informace.

## <a name="best-price-calculation"></a>Výpočet nejlepší ceny
Pokud jste zaznamenali speciální ceny a řádkové slevy za prodej a nákupy, [!INCLUDE [d365fin](includes/d365fin_md.md)] zajistí, že váš zisk z obchodu se zbožím je vždy optimální automatickým výpočtem nejlepší ceny na prodejních a nákupních dokladech, a na řádcích deníků zboží a projektů.

Nejlepší cena je nejnižší přípustná cena s nejvyšší přípustnou řádkovou slevou k danému datu. [!INCLUDE [d365fin](includes/d365fin_md.md)] ji automaticky vypočte při vložení jednotkové ceny a procenta řádkové slevy pro zboží na nových řádcích dokladu a deníku.

> [!NOTE]  
>   Následující text popisuje, jak je pro prodej vypočítána nejlepší cena. Výpočet je stejný pro nákupy.

1. [!INCLUDE [d365fin](includes/d365fin_md.md)] zkontroluje kombinaci plátce a zboží a poté vypočítá použitelnou jednotkovou cenu a procentuální řádkovou slevu pomocí následujících kritérií:

   - Má zákazník dohodu o cenách/slevách, nebo patří do skupiny, která dohodu má?
   - Je zboží nebo skupina slev zboží na řádku zahrnuta v některé z těchto dohod o cenách/slevách?
   - Je datum objednávky (nebo datum zaúčtování faktury a dobropisu) v rozmezí počátečního a koncového data dohody o ceně/slevě?
   - Je zadán kód měrné jednotky? Pokud ano, [!INCLUDE [d365fin](includes/d365fin_md.md)] zkontrolujte ceny/slevy se stejným kódem měrné jednotky a ceny/slevy bez kódu měrné jednotky.

2. [!INCLUDE [d365fin](includes/d365fin_md.md)] zkontroluje, zda se nějaké dohody o ceně/slevě nevztahují na informace v dokladu nebo v řádku deníku a poté vloží příslušné jednotkové ceny a procentuální řádkovou slevu, a to pomocí následujících kritérií:

   - Existuje v dohodě o ceně/slevě požadavek na minimální množství, který je splněn?
   - Existuje v dohodě o ceně/slevě požadavek na měnu, který je splněn? Pokud ano, vloží se nejnižší cena a nejvyšší řádková sleva pro tuto měnu, i když by lokální měna poskytla lepší cenu. Pokud pro zadaný kód měny neexistuje dohoda o ceně/slevě, [!INCLUDE [d365fin](includes/d365fin_md.md)] vloží nejnižší cenu a nejvyšší řádkovou slevu v lokální měně.

Pokud pro zboží na řádku nelze vypočítat žádnou speciální cenu, je vložen buď poslední přímý náklad, nebo jednotková cena z karty zboží.

## <a name="see-also"></a>Viz také
[Nastavení nákupu](purchasing-setup-purchasing.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
