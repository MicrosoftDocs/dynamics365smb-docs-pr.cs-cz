---
title: Nastavení pracovních a strojních center| Microsoft Docs
description: 'Karta **Pracovní centrum** organizuje pevné hodnoty a požadavky výrobního zdroje, a tak řídí výstup výroby prováděné v tomto pracovním centru.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 03/08/2019
ms.author: sgroespe
---
# <a name="set-up-work-centers-and-machine-centers"></a>Nastavení pracovních a strojových center
Program rozlišuje tři typy kapacit. Ty jsou uspořádány hierarchicky. Každá úroveň obsahuje podřízené úrovně.  

Nejvyšší úrovní je skupina pracovních center. Pracovní centra jsou přiřazena ke skupinám pracovních center. Každé pracovní centrum může patřit pouze do jedné skupiny pracovních center.

Každému pracovnímu centru můžete přiřadit různá strojní centra. Strojní centrum může patřit pouze do jednoho pracovního centra.  

Plánovaná kapacita pracovního centra spočívá v dostupnosti odpovídajících strojních center a další budoucí plánované dostupnosti pracovního centra. Plánovaná dostupnost skupiny pracovních center je tedy součtem všech odpovídajících dostupnosti strojních center a pracovních center.  

Dostupnost je uložena v položkách kalendáře. Před nastavením pracovních nebo strojních center musíte nastavit kalendáře dílny. Pro další informace se podívejte na [Vytvoření kalendáře dílny](production-how-to-create-work-center-calendars.md).  

## <a name="to-set-up-a-work-center"></a>Nastavení pracovního střediska
Následujicí článek popisuje jak nastavit pracovního centrum. Kroky pro nastavení kalendář strojního centra jsou podobné, kromě záložky s náhledem **Nastavení TNG postupu**.  

1.  Vyberte ![Žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") ikonu, zadejte **Pracovní centra ** a poté vyberte související odkaz.  
2.  Zvolte akci **Nový**.  
3. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  V poli **Skupina pracovních center** vyberte, pokud je to relevantní, seskupení prostředků vyšší úrovně, pod kterým je pracovní centrum organizováno. V rozevíracím seznamu vyberte akci **Nové**.  
5.  Pokud chcete zabránit použití pracovního centra při jakémkoli zpracování, vyberte pole **Blokování**. To znamená, že výstup nemůže být zaúčtován pro položku vyrobenou v pracovním centru. Pro další informace se podívejte na [Účtování produkčního výstupu](production-how-to-post-output-quantity.md).
6.  V poli **Přímé jednotkové náklady** zadejte náklady na výrobu jedné měrné jednotky v tomto pracovním centru, s vyloučením jakýchkoli dalších nákladových prvků. Tyto náklady se často označují jako *přímé mzdové náklady*.  
7.  V poli **Nepřímé náklady %** zadejte obecné provozní náklady pro používání pracovního centra jako procento přímých jednotkových nákladů. Tato procentní částka je připočtena k přímým nákladům při výpočtu jednotkových nákladů.  
8.  Do pole **Režijní náklady** zadejte veškeré nepracovní náklady, jako například náklady na údržbu, v pracovním centru jako absolutní částku.  

    Pole **Jednicové náklady** obsahuje vypočtené jednotkové náklady na výrobu jedné měrné jednotky v tomto pracovním centru, včetně všech nákladových prvků, takto:  

    Jednicové náklady = přímé Jednicové náklady + (přímé Jednicové náklady x nepřímé náklady %) + režijní náklady.  

9.  V poli **Výpočet jednicových nákladů** definujte, zda by výše uvedený výpočet měl být založen na množství použitého času:  **Čas**, nebo na počtu vyrobených jednotek:  **Jednotky**.  
10.  Vyberte pole **Zadaná pořizovací cena**, pokud chcete definovat pořizovací cenu pracovního centra na řádku TNG postupu, kde je používána. To může být relevantní pro operace s výrazně odlišnými kapacitními náklady, než jaké by se běžně zpracovávaly v tomto pracovním středisku.  
11.  V poli **Metoda spotřeby** vyberte, zda se má účtování výstupu v tomto pracovním centru vypočítat a zaúčtovat ručně nebo automaticky, pomocí jedné z následujících metod.

|Volba|Popis|
|------|-----------|
|**Ručně**|Spotřeba je zaúčtována manuálně v deníku výstupu nebo deníku výroby.|
|**Předem**|Spotřeba se vypočítá a zaúčtuje automaticky když je vydána výrobní zakázka. |
|**Zpětně**|Spotřeba se vypočítá a zaúčtuje automaticky když je výrobní zakázka dokončena.|

> [!NOTE]
> V případě potřeby lze metodu spotřeby zvolenou zde a na kartě **zboží** přepsat pro jednotlivé operace změnou nastavení na směrovacích řádcích

12.  V poli **Kód měrné jednotky** zadejte časovou jednotku, ve které se provádí výpočet nákladů a plánování kapacity tohoto pracovního centra.
    Abyste mohli neustále sledovat spotřebu, musíte nejprve nastavit metodu měření. Jednotky, které zadáte jsou základní jednotky. Například, doba zpracování se měří v hodinách a minutách.

> [!NOTE]  
> Jestli zadáváte dny, tak pamatujte, že 1 den = 24 hodin - a ne 8 (pracovních hodin)

13.  V poli **Kapacita** určete, zda má pracovní centrum více než jeden stroj nebo osobu pracující současně. Pokud instalace vašeho [!INCLUDE[d365fin](includes/d365fin_md.md)] nezahrnuje funkci Strojní centrum, pak hodnota v tomto poli musí být **1**.  
14.  Do pole **Efektivita** zadejte procento očekávaného standardního výstupu, který toto pracovní centrum skutečně vydává. Pokud zadáte **100**, znamená to, že pracovní centrum má skutečný výstup stejný jako standardní výstup.  
15. Pokud používáte také strojní centrum, zaškrtněte políčko **Konsolidovaný kalendář**. Tím je zajištěno, že položky kalendáře jsou nahrány z strojního centra.  
16.  V poli **Kód kalendáře dílny**, vyberte kalendář dílny. Pro další informace se podívejte na [Vytvoření kalendáře dílny](production-how-to-create-work-center-calendars.md).  
17.  V poli **Doba ve frontě** specifikujte pevné časové rozpětí, které musí uplynout před tím, než bude možné zahájit přiřazenou práci v tomto pracovním centru. Všimněte si, že doba ve frontě se přidává k jiným neproduktivním časovým prvkům, jako je doba čekání a doba přesunu, kterou můžete definovat na řádcích TNG postupu pomocí tohoto pracovního centra.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Příklad - Různá strojní centra přiřazená k pracovním centrům
Při nastavování strojních center a pracovních center je důležité naplánovat, jaké kapacity mají tvořit celkovou kapacitu.

Jsou-li pracovnímu centru přiřazena různá strojní centra (např. 210 Balící stůl 1, 310 Lakovací kabina ...), je zohlednění jednotlivých kapacit obráběcích center významné, protože selhání jednoho strojního centra může přerušit celý proces. Skupiny strojů lze zadávat podle jejich kapacity, ale nemusí být zahrnuty do plánování. Při deaktivaci pole **Konsolidovaný kalendář ** je přiřazena pouze kapacita pracovního centra, ale nikoliv strojního centra.

Pokud jsou však strojní centra identická (jako například 210 Balicí stůl 1 a 220 Balící stůl 2) jsou zkombinována v pracovním centru, je zajímavé uvážení pracovního centra jako součet přiřazených strojních center. Pracovní středisko by proto mělo být uvedeno s nulovou kapacitou. Aktivací pole **Konsolidovaného kalendáře** je společná kapacita přiřazena pracovnímu centru.

Pokud kapacity pracovních center nepřispívají k celkové kapacitě, můžete toho dosáhnout s účinností = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Nastavení omezené kapacity strojního nebo pracovního centra
Musíte nastavit výrobní zdroje, které považujete za kritické, a označit je, aby akceptovaly konečné zatížení namísto výchozího nekonečného zatížení, které přijímají ostatní výrobní prostředky. Kapacitně omezený zdroj může být pracovní nebo strojové centrum, které jste označili jako úzký profil a pro které byste chtěli zavést omezené konečné zatížení.

[!INCLUDE[d365fin](includes/d365fin_md.md)] nepodporuje podrobné dílenské řízení. Plánuje možné využití zdrojů poskytnutím hrubého plánu, ale automaticky nevytváří a neudržuje podrobné plány na základě priorit nebo pravidel optimalizace.

Na stránce **Zdroje s limitovanou kapacitou** můžete provést nastavení, které brání přetížení konkrétních zdrojů a zajistí, aby žádná kapacita nebyla ponechána nepřidělená, pokud by to mohlo prodloužit dobu obratu výrobní zakázky. V poli **Prodleva (% celk.kapacity)** můžete ke zdrojům přidat čas prodlevy, aby se minimalizovalo dělení operací. To umožňuje systému naplánovat zatížení na poslední možný den mírným překročením procenta kritického zatížení, pokud to může snížit počet rozdělených operací.

Při plánování se zdroji s omezenou kapacitou systém zajišťuje, aby žádný zdroj nebyl zatížen nad jeho definovanou kapacitu (kritické zatížení). To se provádí přiřazením každé operace k nejbližšímu dostupnému časovému slotu. Pokud časový úsek není dostatečně dlouhý na dokončení celé operace, bude rozdělen na dvě nebo více částí umístěných v nejbližších dostupných časových slotech.

1. Vyberte ![Žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") ikonu, zadejte **Kapacitně omezené zdroje** a poté vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Vyplňte pole podle potřeby.

> [!NOTE]
> Operace na pracovních střediscích nebo strojních centrech, které jsou nastaveny jako omezené zdroje, budou vždy plánovány sériově. To znamená, že pokud omezený zdroj má více kapacit, pak mohou být tyto kapacity plánovány pouze postupně, nikoli paralelně, jako by tomu bylo v případě, že by pracovní nebo strojní centrum nebylo nastaveno jako omezený zdroj. V omezeném zdroji je pole Kapacita v pracovním centru nebo ve strojním centru větší než 1.

> V případě rozdělení operací je čas nastavení přiřazen pouze jednou, protože se předpokládá, že k optimalizaci plánu je provedeno nějaké ruční nastavení.

## <a name="see-also"></a>Viz také  
[Vytvoření kalendáře dílny](production-how-to-create-work-center-calendars.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)    
[Plánování](production-planning.md)   
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
