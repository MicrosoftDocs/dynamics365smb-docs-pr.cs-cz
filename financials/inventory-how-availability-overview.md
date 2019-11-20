---
title: Získejte přehled dostupnosti | Microsoft Docs
description: 'Můžete získat informace o dostupnosti zboží nebo zásob napříč lokacemi, podle prodejních nebo nákupních akcí, podle časového období nebo podle polohy zboží na kusovníku sestavy nebo výroby.'
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 08/15/2017
ms.author: SorenGP
---
# <a name="view-the-availability-of-items"></a>Zobrazení dostupnosti zboží
Z kontextu obchodního úkolu můžete získat pokročilé informace o tom, kdy a kde je zboží k dispozici, například při rozhovoru se zákazníkem ohledně data dodání.

Můžete zobrazit dostupnost všeho zboží na lokacích a dostupnost každého zboží podle události, podle období nebo podle lokace. Událost je jakákoli transakce naplánovaného zboží, jako je prodejní zásilka nebo potvrzení o příchozím převodu.

> [!NOTE]  
>   Zobrazení dostupnosti podle lokace vyžaduje, abyste udržovali zásoby na více než jedné lokaci. Pro více informací navštivte [Nastavení lokací](inventory-how-setup-locations.md).

V [!INCLUDE [d365fin](includes/d365fin_md.md)] jsou zobrazeny údaje o dostupnosti ve dvou různých polích, každé s odlišnou definicí:

* Pole **Množství na skladě** zobrazuje skutečné aktuální množství podle účtovaných položek zboží.
* Pole **Předpokládané dost.množ.** je vypočteno a zobrazuje množství na skladě plus plánované příjmy mínus celkové požadavky. (V [!INCLUDE [d365fin](includes/d365fin_md.md)], naplánované příjmy zahrnují množství na nákupních objednávkách a vstupních objednávkách transferu. Hrubé požadavky zahrnují množství na prodejních objednávkách a odchozích objednávkách transferu.)

> [!TIP]  
>   Předpokládaný disponibilní zůstatek je zvláště důležitý pro zobrazení v okně **Zboží k dispozici dle období** a **Dostupnost zboží dle událostí**, protože obsahují dimenzi data.  

> [!NOTE]  
>   Následující postupy popisují, jak zobrazit informace o rozšířené dostupnosti ze seznamu zboží a karty zboží. Můžete také získat přístup k informacím z řádků prodejních dokladů pro zboží na řádku. Pro více informací navštivte [Prodej produktů](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Zobrazení dostupnosti zboží podle toho, kdy bude přijato nebo odesláno
Dostupnost zboží podle naplánovaných transakcí zboží zobrazíte v okně **K dispozici dle události**.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Zboží** a pak vyberte související odkaz.
2. Otevřete kartu zboží, pro které chcete zobrazit dostupnost.
3. Vyberte akci **K dispozici dle** a poté vyberte **Událost**.

    Okno **Zboží k dispozici dle událostí** ukazuje, jak se bude množství zásob zboží vyvíjet v průběhu času podle naplánovaných zásilek a událostí přijetí. Okno poskytuje zhuštěné zobrazení, které ukazuje jeden řádek kumulovaných informací za časový interval, ve kterém se mění množství zásob. Časové intervaly, ve kterých nedošlo k žádným událostem, nejsou zobrazeny. Každý řádek můžete rozbalit a zobrazit podrobnosti o události nebo událostech, které způsobily nashromážděné množství na řádku.
4. Vyberte hodnotu v poli **Předpokládané dost.množ.** pro zobrazení položky zboží nebo otevřených dokladů, které tuto hodnotu tvoří.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Zobrazení dostupnosti zboží v různých obdobích
Dostupnost zboží v čase pro určitá časová období zobrazíte v okně **Zboží k dispozici dle období**.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Zboží** a pak vyberte související odkaz.
2. Otevřete kartu zboží, pro které chcete zobrazit dostupnost.
3. Vyberte akci **K dispozici dle** a poté vyberte **Období**.

    Okno **Zboží k dispozici dle období** zobrazuje, jak se bude množství zásob zboží vyvíjet v průběhu času, a to po dobu, kterou vyberete, například den, týden nebo čtvrtletí.
4. Vyberte hodnotu v poli **Předpokládané dost.množ.** pro zobrazení položky zboží nebo otevřených dokladů, které tuto hodnotu tvoří.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Zobrazení dostupnosti zboží v lokacích, kde je uloženo
Dostupnost zboží pro různé lokace, kde je uloženo zobrazíte v okně **Zboží k dispozici dle lokace**.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Zboží** a pak vyberte související odkaz.
2. Otevřete kartu zboží, pro které chcete zobrazit dostupnost.
3. Vyberte akci **K dispozici dle** a poté vyberte **Lokace**.

    Okno **Zboží k dispozici dle lokace** ukazuje, jak se bude v budoucnu vyvíjet množství zásob zboží, zobrazené pro každou lokaci, kde je uloženo.
4. Vyberte hodnotu v poli **Množství na skladě** pro zobrazení položky zboží, které tuto hodnotu tvoří.
5. Vyberte hodnotu v poli **Předpokládané dost.množ.** pro zobrazení položky zboží nebo otevřených dokladů, které tuto hodnotu tvoří.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Zobrazení dostupnosti všeho zboží dle lokace
V okně **Zboží dle lokací** můžete zobrazit dostupnost všeho zboží ve všech lokacích.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Zboží** a pak vyberte související odkaz.
2. Vyberte akci **Zboží dle lokací**.

    V okně **Zboží dle lokací** se u všeho zboží zobrazuje, kolik je v každé lokaci k dispozici.
3. Vyberte hodnotu v poli **Množství na skladě** pro zobrazení položky zboží, které tuto hodnotu tvoří.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms"></a>Zobrazení dostupnosti zboží pomocí jejího použití v montážních nebo výrobních kusovnících
Pokud zboží existuje v montáži nebo kusovnících výroby, buď jako nadřazené zboží nebo jako komponenta, můžete v okně **Dostupnost zásob za úroveň kusovníku** zobrazit, kolik jeho jednotek je vyžadováno. V tomto okně je uvedeno, kolik jednotek nadřazeného zboží můžete vytvořit na základě dostupnosti podřízeného zboží na základních řádcích. Každé zboží, které má kusovník sestavy nebo výroby, se v okně zobrazí jako skládací řádek. Tento řádek můžete rozšířit a zobrazit základní komponenty a podsestavy nižší úrovně s jejich vlastními kusovníky.

Pomocí tohoto okna můžete zjistit, zda můžete splnit prodejní objednávku pro zboží v určeném datu, a to tak, že se podíváte na její aktuální dostupnost a množství, které mohou její součásti dodat. Okno můžete také použít k identifikaci úzkých míst v souvisejících kusovnících.

Na každém řádku v okně pro nadřazené i podřízené zboží určují následující klíčová pole údaje o dostupnosti. Pomocí těchto čísel můžete slíbit, kolik jednotek nadřazeného zboží můžete dodat, pokud zahájíte související proces montáže.

|Pole|Popis|
|------|-----------|
|**Schopnost vyrobit nadřazené zboží**|Zobrazuje, kolik jednotek jakékoli podsestavy v zboží nejvyšší úrovně můžete vytvořit. Pole určuje, kolik okamžitých nadřazených jednotek můžete sestavit. Hodnota je založena na dostupnosti zboží na řádku.|
|**Schopnost vyrobit zboží nejvyšší úrovně**|Zobrazuje, kolik jednotek zboží nejvyšší úrovně můžete vytvořit. Pole specifikuje, kolik jednotek zboží nejvyšší úrovně kusovníku můžete sestavit. Hodnota je založena na dostupnosti zboží na řádku.|

### <a name="item-availability-by-bom-level-window"></a>Dostupnost zboží podle úrovně kusovníku
Okno **Dostupnost zásob za úroveň kusovníku** zobrazuje informace o zboží na kartě nebo řádku dokladu, pro kterou je okno otevřena. Zboží je vždy zobrazeno v horním řádku. Informace o jiným zboží nebo o všem zboží můžete zobrazit změnou hodnoty v poli **Filtr zboží**.

> [!NOTE]  
>   Ve výchozím nastavení čísla dostupnosti na řádcích ukazují celkovou dostupnost všeho zboží pod zbožím nejvyšší úrovně. Tyto údaje jsou zobrazeny v poli **Dostupné množství** a důraz je kladen na zboží nejvyšší úrovně. Informace o tom, kolik podsestav můžete vytvořit, však mohou být zkreslené. Chcete-li získat skutečný údaj o tom, kolik zobrazených podsestav můžete vytvořit, musíte zrušit zaškrtnutí políčka **Zobrazit celkovou dostupnost** a poté zobrazit hodnotu v poli **Schopnost vytvořit nadřazené**.

Pole **Úzký profil** určuje, které zboží ve struktuře kusovníku vám omezuje možnost vyrobit větší množství, než je množství, které je zobrazeno v poli **Schopnost vytvořit nejvyšší položku**. Například může být úzkým profilem zakoupená komponenta s očekávaným datem přijetí, které je příliš pozdní na to, aby se další jednotky nejvyššího zboží mohly do data v poli **Potřebné dle data** vytvořit.

## <a name="assembly-availability-window"></a>Okno dostupnost sestavy
Okno **Dostupnost sestavy** zobrazuje podrobné informace o dostupnosti zboží sestavy. Otevře se:

- Automaticky z řádku prodejní objednávky ve scénářích sestavení na objednávku, když zadáte množství, které způsobuje problém s dostupností komponent.
- Automaticky z hlavičky objednávky sestavy, když do pole Množství zadáte hodnotu, která způsobuje problém s dostupností komponent.
- Ručně, když ji otevřete z objednávky sestavy. Na záložce Akce ve skupině Funkce klikněte na Zobrazit dostupnost.

Záložka **Podrobnosti** zobrazuje podrobné informace o dostupnosti zboží sestavy, včetně toho, kolik z množství sestavy lze sestavit do data splatnosti na základě dostupnosti požadovaných komponent. To se zobrazí v poli Schopen montáže na záložce Podrobnosti.

Pokud je množství menší než množství v poli **Zůstatek (množství)**, je hodnota v poli **Schopen montáže** zobrazena červeně, což znamená, že není k dispozici dostatek komponent k sestavení celého množství.

Záložka **Řádky** zobrazuje podrobné informace o dostupnosti komponent sestavy.

Pokud není k dispozici jedna nebo více součástí sestavy, projeví se to v poli **Schopen montáže** na příslušném řádku jako množství menší než množství v poli **Zůstatek (množství)** na záložce **Podrobnosti**.

## <a name="see-also"></a>Viz také
[Spravovat zásoby](inventory-manage-inventory.md)  
[Řízení montáže](assembly-assemble-items.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)    
[Nastavení lokace](inventory-how-setup-locations.md)  
[Převod zásob mezi lokacemi](inventory-how-transfer-between-locations.md)  
[Prodávané produkty](sales-how-sell-products.md)      
[Práce s Business Central](ui-work-product.md)  
[Hlavní obchodní funkcionality](ui-across-business-areas.md)
