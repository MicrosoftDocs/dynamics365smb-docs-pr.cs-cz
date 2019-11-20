---
title: Jak nastavit Pracovní a Strojní centra | Microsoft Docs
description: 'Karta **Pracovního Centra** organizuje pevné hodnoty a požadavky zdroje výroby, tím řídí výstup výroby z tohoto pracovního centra.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/19/2017
ms.author: sgroespe
---
# <a name="set-up-work-centers-and-machine-centers"></a>Nastavení Pracovních a Strojních center
Program rozlišuje mezi třemi typy kapacit. Ty jsou seřazeny hierarchálně. Každá úroveň obsahuje úrovně podřízené.  

Nejvyšší úrovní je skupina pracovních center. Pracovní centra jsou přiřazena ke skupinám pracovních center. Každé pracovní centrum může patřit pouze do jedné skupiny pracovních center.

Ke každému pracovnímu centru můžete přiřadit různé strojní centra. Strojní centrum může patřit pouze do jednoho pracovního centra.  

Plánovaná kapacita pracovního centra se skládá z dostupnosti odpovídajících strojních center a dodatečné plánované dostupnosti pracovního centra. Plánovaná dostupnost skupiny pracovních center je tedy součtem všech odpovídajících dostupností strojních center a pracovních center.  

Dostupnost je uložena v Položkách kalendáře. Před nastavením pracovních, nebo strojních center musíte nastavit Kalendáře dílny. Další informace naleznete v části [Vytvoření Kalendářů dílny](production-how-to-create-work-center-calendars.md).  

## <a name="to-set-up-a-work-center"></a>Nastavení pracovního centra
Následující popis vysvětluje, jak nastavit pracovní centrum. Kroky pro nastavení Kalendáře strojního centra jsou podobné, kromě záložky Nastavení TNG  

1. Zvolte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "Ikona Vyhledat Stránku nebo Sestavu"), zadejte **Pracovní centrum** a pak vyberte související odkaz.  
2. Zvolte akci **Nový**.  
3. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. V poli **Skupina pracovních center** vyberte, pokud je to relevantní, seskupení prostředků vyšší úrovně, pod kterým je pracovní centrum organizováno. Vyberte z rozevíracího seznamu akci **Nový**.  
5. Vyberte pole **Uzavřeno** Pokud chcete zabránit použití pracovního centra při jakémkoliv zpracování. To znamená, že výstup nemůže být zaúčtován pro zboží vyrobené v pracovním centru. Pro více informací navštivte [Účtování výrobního výstupu](production-how-to-post-output-quantity.md).
6. Do pole **Nákupní cena** zadejte náklady na výrobu jedné měrné jednotky v tomto pracovním centru, s vyloučením jakýchkoliv dalších nákladů. Tyto náklady se často označují jako *přímá sazba za práci*.  
7. Do pole **Nepřímé náklady %** zadejte obecné provozní náklady používání pracovního centra jako procentuální hodnotu přímých jednotkových nákladů. Tato procentní částka se připočte k přímým nákladům při výpočtu nákupní ceny.  
8. V poli **Režijní náklady** doplňte jakékoliv jiné náklady než provozní, například náklady na údržbu, pracovního centra jako absolutní částka.  

   Pole **Pořizovací cena** obsahuje vypočítanou pořizovací cenu vyrobení jedné měrné jednotky v tomto pracovním centru, obsahující všechny následující náklady:  

   Pořizovací cena = Nákupní cena + (Nákupní cena x Nepřímé náklady %) + Režijní náklady.  

9. V poli **Výpočet pořizovací ceny** definujte, zda by měl být výše uvedený výpočet založen na množství použitého času:  **Čas**, nebo číslo vyprodukovaných jednotek:  **Jednotky**  
10. Vyberte pole **Zadaná pořizovací cena** pokud chcete definovat jednotkové náklady pracovního centra na řádku TNG postupu, kde jsou používány. Toto může být relevantní pro operace s výrazně odlišnými kapacitními náklady, než jaké by se běžně zpracovávaly v tomto pracovním centru.  
11. V poli **Metoda spotřeby** vyberte, zda-li se má účtování výstupu v tomto pracovním centru vypočítat a zaúčtovat ručně nebo automaticky, pomocí jedné z následujících metod.  

    |Možnost|Popis|  
    |----------------------------------|---------------------------------------|  
    |**Ručně**|Spotřeba je zaúčtována ručně ve Deníku výstupu nebo Deníku výroby.|
    |**Předem**|Spotřeba je vypočítána a zaúčtována automaticky, když je zadána produkční zakázka.|  
    |**Zpětně**|Spotřeba je vypočítána a zaúčtována automaticky, když je dokončena produkční zakázka.|  

    > [!NOTE]  
    >  V případě potřeby lze metodu spotřeby zvolenou zde a na kartě **Zboží**změnit pro jednotlivé operace změnou nastavení na řádcích TNG postupu.

12. Do pole **Kód měrné jednotky** zadejte časovou jednotku, ve které se provádí výpočet nákladů a plánování kapacity tohoto pracovního centra.
    Abyste mohli neustále sledovat spotřebu, musíte nejprve nastavit metodu měření. Jednotky, které zadáte, jsou základní jednotky. Například doba zpracování se měří v hodinách a minutách.

    > [!NOTE]  
    > Pokud se rozhodnete použít Dny, nezapomeňte, že 1 den = 24 hodin - a ne 8 hodin (pracovní doba).

13. V poli **Kapacita** určete, zda má pracovní centrum více než jeden stroj nebo osobu pracující současně. Pokud vaše [!INCLUDE [d365fin](includes/d365fin_md.md)] instalace nezahrnuje funkci Strojní centrum, tak pak hodnota v tomto poli musí být **1**.  
14. V poli **Účinnost**, zadejte očekávanou standardní procentuální hodnotu  výstupu, kterou toto pracovní centrum vydává. Pokud zadáte **100**, znamená to, že aktuální výstup pracovního centra je stejný jako standardní výstup.  
15. Zaškrtněte pole **Konsolidovaný Kalendář**, pokud také používáte strojní centra. Tím je zajištěno, že položky kalendáře jsou zahrnuté z kalendářů strojních center.  
16. V poli **Kód kalendáře dílny** vyberte kalendář obchodu. Další informace naleznete v části [Vytvoření Kalendářů dílny](production-how-to-create-work-center-calendars.md).  
17. V poli **Doba ve frontě** specifikujte určitý časový, který musí uplynout, než se může proces v pracovním centru začít. Všimněte si, že Doba ve frontě se přidává k jiným neproduktivním časovým prvkům, jako je doba čekání a doba přesunu, kterou můžete definovat na řádcích TNG postupu pomocí tohoto pracovního centra.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Příklad - Přiřazení odlišných strojních center k pracovnímu centru
Při zřizování strojních a pracovních center je důležité naplánovat, které kapacity mají dohromady tvořit celkovou kapacitu.

Jsou-li pracovnímu centru přiřazena různá strojní centra (např. 210 Balicí stůl 1, 310 Lakovací kabina ...), pak je důležité zohlednit jejich jednotlivé kapacity, protože selhání jednoho strojního centra může přerušit celý proces. Skupiny strojních center mohou být zadávány podle jejich kapacity, ale nemusí být zahrnuty do plánování. Při deaktivaci pole **Konsolidovaný kalendář**  je přiřazena k plánování pouze kapacita pracovního centra, bez zohlednění strojního centra.

Pokud jsou však stejná strojní centra (jako je 210 Balicí stůl 1 a 220 Balící stůl 2) kombinována v pracovním centru, je důležité zohlednit pracovní centrum jako součet přidělených strojních center. Pracovní středisko by proto bylo uvedeno s nulovou kapacitou. Aktivací pole **Konsolidovaný kalendář** je společná kapacita přiřazena pracovnímu centru.

Jestli kapacity pracovních center nepřispívají k celkové kapacitě, tak to dosáhnout tím, že přiřadíte účinnost = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Nastavení stroje nebo pracovního centra s omezenou kapacitou
Musíte nastavit výrobní zdroje, které považujete za kritické, a označit je, aby akceptovaly konečné zatížení namísto výchozího nekonečného zatížení, které přijímají ostatní výrobní zdroje. Zdrojem s omezenou kapacitou může být pracovní nebo strojové centrum, které jste označili jako vaše kritické body a pro které byste chtěli zavést omezenou konečnou zátěž.

[!INCLUDE [d365fin](includes/d365fin_md.md)] nepodporuje podrobné dílenské řízení. Plánuje možné využití zdrojů poskytnutím podrobného plánu, ale automaticky nevytváří ani neudržuje podrobné plány na základě priorit nebo pravidel optimalizace.

V okně **Zdroje s limitovanou kapacitou**, můžete provést nastavení, které zabrání přetížení konkrétních zdrojů a zajistí, aby žádná kapacita nebyla ponechána nepřidělená, pokud by to mohlo prodloužit dobu obratu výrobní zakázky. Na poli **Prodleva ( % celk. kapacity**) můžete ke zdrojům přiřadit čas prodlevy k minimalizování rozdělení operací. To umožňuje systému naplánovat zatížení na poslední možný den, pokud to může snížit počet rozdělených operací, mírným překročením procenta kritického zatížení.

Při plánování s prostředky s omezenou kapacitou systém zajišťuje, aby žádný zdroj nebyl zatížen nad jeho definovanou kapacitu (kritické zatížení). To se provádí přiřazením každé operace k nejbližšímu dostupnému časovému úseku. Pokud časový úsek není dostatečně velký na dokončení celé operace, operace bude rozdělena na dvě nebo více částí naplánovaných v nejbližších dostupných časových úsecích.

1. Zvolte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "Ikona Vyhledat Stránku nebo Sestavu"), zadejte **Zdroje s limitovanou kapacitou** a pak vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Vyplňte pole podle potřeby.

> [!NOTE]
> Operace v pracovních, nebo strojních centrech, které jsou nastaveny jako zdroje s limitovanou kapacitou, budou vždy plánovány sériově. To znamená, že pokud zdroj s limitovanou kapacitou má více kapacit, pak mohou být tyto kapacity plánovány pouze postupně, a nikoliv paralelně, jako by tomu bylo v případě, kdy by pracovní nebo strojní centrum nebylo nastaveno jako zdroj s limitovanou kapacitou. U zdroje s limitovanou kapacitou je pole Kapacita v pracovním centru nebo ve strojním centru větší než 1.
> 
> V případě rozdělení operací je čas nastavení přiřazen pouze jednou, protože se předpokládá, že k optimalizaci plánu je provedeno nějaké ruční nastavení.

## <a name="see-also"></a>Viz také  
[Vytvoření Kalendářů dílen](production-how-to-create-work-center-calendars.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)    
[Plánování](production-planning.md)   
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
