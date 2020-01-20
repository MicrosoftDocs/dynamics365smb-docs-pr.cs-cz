---
title: Jak nastavit Kalendáře dílny | Microsoft Docs
description: 'Kalendář pracovního centra určuje pracovní dny a hodiny, směny, svátky a nepřítomnosti, které určují hrubou dostupnou kapacitu pracovního centra (typicky měřenou v minutách). Vytvoření a povolení kalendáře pracovního centra zahrnuje několik přípravných úkolů.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/14/2017
ms.author: sgroespe
---
# <a name="set-up-shop-calendars"></a>Nastavení Kalendářů dílny
Kalendář pracovního nebo strojního centra určuje pracovní dny, hodiny, směny, svátky a nepřítomnosti, které určují hrubou dostupnou kapacitu pracovního centra, měřenou v čase, podle definovaných hodnot účinnosti a kapacity.

Jako základ pro výpočet konkrétního kalendáře pracovních nebo strojních center musíte nejprve nastavit jeden nebo více obecných kalendářů dílen. Kalendář dílny definuje standardní pracovní týden podle časů začátku a konce každého pracovního dne a vztahu pracovních směn. Kalendář dílny navíc definuje pevné svátky během roku.  

Následující článek popisuje jak nastavit kalendáře pracovního centra. Kroky jsou podobné nastavení strojního centra.  

## <a name="to-create-work-shifts"></a>Pro vytvoření pracovních směn  
1.  Zvolte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "Ikona Vyhledat Stránku nebo Sestavu"), zadejte **Pracovní směny ** a pak vyberte související odkaz.  
2.  Na prázdný řádek zadejte číslo do pole **Kód** pro identifikaci pracovní směny, jako například **1**.  
3.  Popište pracovní směnu v poli **Popis**, jako například, **první směna**  
4.  Popřípadě vyplňte řádky pro druhou nebo třetí pracovní směnu.  

I když vaše pracovní centra nepracují v různých pracovních směnách, zadejte alespoň jeden kód pracovní směny.  

## <a name="to-set-up-a-shop-calendar"></a>Nastavení kalendářů dílny  
1.  Zvolte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "Ikona Vyhledat Stránku nebo Sestavu"), zadejte **Kalendáře dílny** a pak vyberte související odkaz.  
2.  Na prázdný řádek zadejte číslo do pole **Kód** pro identifikaci kalendře dílny.  
3.  Popište kalendář dílny v poli **Popis**.  
4.  Vyberte akci **Pracovní dny**.
5.  V okně **Kalendář prac.dnů dílny** definujte celý pracovní týden s časy začátku a konce pro každý den.  

    V poli **Kód pracovní směny** vyberte jednu z dříve definovaných směn. Přidejte řádek pro každý pracovní den a každou směnu. Například:  

    Pondělí 07:00 15:00 1   
    Úterý 07:00 15:00 1  

    Potřebujete-li kalendář dílny se dvěma směnami, musíte ho vyplnit tímto způsobem:  

    Pondělí 07:00 15:00 1   
    Pondělí 15:00 23:00 2  
    Úterý 07:00 15:00 1  
    Úterý 15:00 23:00 2  

    Všechny dny v týdnu, které v kalendáři dílny nedefinujete, jako je sobota, nebo neděle, budou považovány za nepracovní dny a budou mít v kalendáři pracovního centra nulovou dostupnou kapacitu.  

    Pokud jsou definovány všechny pracovní dny v týdnu, můžete zavřít okno **Kalendář prac. dnů dílny** a pokračovat k zadávání svátků.  

6.  V okně **Kalendáře dílny** vyberte kalendář obchodu a poté vyberte akci **Svátky**.
7. V okně **Svátky kalendáře dílen** definujte svátky roku zadáním počátečního data a času, koncového času a popisu každého svátku na jednotlivých řádcích. Například:  

    04/07/14 0:00:00 23:59:00 Letní prázdniny  
    05/07/14 0:00:00 23:59:00 Letní prázdniny  
    06/07/14 0:00:00 23:59:00 Letní prázdniny  

Definované svátky budou mít v kalendáři pracovního centra nulovou dostupnou kapacitu  

Kalendář dílny může být nyní přiřazen k pracovnímu centru pro výpočet pracovního kalendáře dílny, který bude řídit veškeré plánování operací v tomto pracovním centru.  

## <a name="to-calculate-a-work-center-calendar"></a>Výpočet kalendáře pracovního centra  

1.  Zvolte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "Ikona Vyhledat Stránku nebo Sestavu"), zadejte **Pracovní centrum** a pak vyberte související odkaz.
2. Otevřete pracovní centrum, které chcete aktualizovat.  
3. V poli **Kód kalendáře dílny** vyberte, který kalendář dílny se má použít jako základ pro kalendář pracovního střediska.  
4. Zvolte akci **Kalendář**.  
5. V okně **Kalendář pracovního centra** zvolte akci **Ukázat Matice**.  

    Na levé straně maticového okna jsou uvedena nastavená pracovní centra. Na pravé straně je kalendář zobrazující dostupné hodnoty kapacity pro každý pracovní den v definované měrné jednotce, například **480** minut. Každý řádek představuje kalendář jednoho pracovního centra.  

    > [!NOTE]  
    >  Můžete také zvolit zobrazení hodnot kapacity pro každý týden nebo měsíc změnou výběru v poli **Zobrazit podle** v okně **Kalendář pracovního střediska**.  

    Aby se nový kalendář dílny promítl jako čára ve vybraném pracovním centru, musí být nejprve vypočítán.  

6.  Vyberte akci **Vypočítat**  
7.  Na záložce s náhledem **Pracovní centrum** můžete nastavit filtr tak, aby počítal pouze pro jedno pracovní centrum. Pokud nenastavíte filtr, budou vypočítány všechny existující kalendáře pracovního centra.  
8.  Definujte počáteční a koncové datum kalendářního období, které by se mělo vypočítat, například, jeden rok od 01/01/14 do 31/12/14.
9. Zvolte tlačítko **OK** a vypočítejte kapacitu.  

Položky kalendáře jsou nyní vytvářeny nebo aktualizovány a zobrazují dostupnou kapacitu pro každé období podle následujících tří sad hlavních dat:  

- Pracovní dny a směny definované v přiřazeném obchodním kalendáři.  
- Hodnota v poli **Kapacita** na kartě pracovního centra.  
- Hodnota v poli **Účinnost** na kartě pracovního centra.  

Vypočítaný kalendář pracovního centra bude nyní definovat, kdy a kolik kapacity je v tomto pracovním centru k dispozici. Tím se řídí podrobné plánování operací prováděných v pracovním centru.  

## <a name="to-record-work-center-absence"></a>Chcete-li zaznamenat nepřítomnost pracovního centra  
1.  V okně **Kalendář pracovního centra** zvolte akci **Ukázat Matice**.
2. V okně **Matice kalendáře pracovního centra** vyberte pracovní středisko a kalendářní den, kdy má být zaznamenána doba nepřítomnosti, a poté vyberte akci **Nepřítomnost**.  
3.  V okně **Nepřítomnost** definujte počáteční čas, konečný čas a popis nepřítomnosti daného dne. Například:  

    25/01/01 08:00 10:00 Údržba  

4.  Vyberte akci **Aktualizace** a zavřete okno **Nepřítomnost**.  

Kapacita vybraného dne se nyní snížila o zaznamenanou dobu nepřítomnosti.  

## <a name="see-also"></a>Viz také  
[Nastavení Kalendáře zdrojů](across-how-to-assign-base-calendars.md)  
[Nastavení Pracovních a Strojních center](production-how-to-set-up-work-and-machine-centers.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
