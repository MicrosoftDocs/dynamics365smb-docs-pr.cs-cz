---
title: Ruční úprava nákladů zboží | Microsoft Docs
description: 'Ocenění zboží můžete upravit pomocí metod FIFO nebo průměrné kalkulace, například když se náklady zboží změní z jiných důvodů, než jsou transakce.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 08/07/2017
ms.author: sgroespe
---
# <a name="adjust-item-costs"></a>Upravit cenu položky
Náklady na položku (hodnotu zásob), kterou si koupíte a později prodáváte, se mohou během své životnosti měnit, například proto, že náklady na dopravu jsou po prodeji položky přidány k nákupním nákladům. Úprava nákladů je zvláště důležitá v situacích, kdy zboží prodáváte před fakturací nákupu tohoto zboží. Aby byla vždy známá správná hodnota inventáře, je třeba pravidelně upravovat náklady na položky. To zajišťuje, že statistiky prodeje a zisku jsou aktuální a že finanční ukazatele KPI jsou správné. Pro více informací navštivte [Podrobnosti o designu: Úpravy nákladů](design-details-cost-adjustment.md).

Hodnota v poli **Pořizovací cena** na kartě zboží je zpravidla založena na pevné pořizovací ceně, která je pro zboží standardem metody ocenění. Kalkulace zboží se všemi ostatními metodami je založena na výpočtu dostupných zásob (fakturované náklady a očekávané náklady) děleno množstvím na skladě. Pro více informací navštivte sekci „Porozumění výpočtu pořizovací ceny“.

V [!INCLUDE [d365fin](includes/d365fin_md.md)], se náklady na zboží automaticky upravují pokaždé, když dojde k transakci se zásobami, například při účtování nákupní faktury za zboží.

Pomocí funkce můžete také manuálně upravit náklady na jedno nebo více zboží. To je užitečné například tehdy, když víte, že náklady na zboží se změnilo z jiných důvodů než standardní transakcí se zbožím.

Náklady na zboží se upravují metodou FIFO nebo metodou průměrné kalkulace, v závislosti na vašem výběru v asistovaném nastavení **Nastavení mé společnosti** nebo v poli **Metoda ocenění** na kartě zboží. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).  

Pokud používáte metodu ocenění FIFO, pak pořizovací cena zboží je skutečná hodnota jakéhokoli přijetí zboží. Zásoby se oceňují za předpokladu, že první zboží uložené v zásobách je prodáváno jako první.

Pokud použijete metodu průměrného ceny, pořizovací cena zboží se vypočte jako průměrná pořizovací cena v každém okamžiku po nákupu. Zásoby se oceňují s předpokladem, že všechny zásoby se prodávají současně. U zboží, které používá tuto metodu ocenění, můžete vybrat pole **Pořizovací cena** na kartě zboží a zobrazit historii transakcí, z nichž se vypočítá průměrná cena.

Funkce úpravy nákladů zpracovává pouze hodnoty, které ještě nebyly upraveny. Pokud se funkce setká s situací, kdy je třeba přenést změněné příchozí náklady do přidružených odchozích položek, vytvoří se nové upravené položky, které jsou založeny na informacích v položkách původní hodnoty, ale obsahují upravenou částku. Funkce úpravy nákladů používá datum zaúčtování položky původní hodnoty do upravené položky, pokud se tento datum nenachází v uzavřeném období zásob. V takovém případě program používá datum zahájení dalšího otevřeného období zásob. Pokud se nepoužije doba zásob, pak bude v poli **Povolit odesílání z** v okně **Nastavení hlavní knihy** definováno, kdy bude zaúčtována upravená položka.

## <a name="to-adjust-item-costs-manually"></a>Ruční úpravy položek položek
1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Adjustace nákladů - položky zboží** a pak vyberte související odkaz.
2. V okně **Adjustace nákladů - položky zboží** zadejte, pro které zboží chcete upravit náklady.
3. Zvolte tlačítko **OK**.

## <a name="to-make-general-changes-in-the-direct-unit-cost"></a>Provádění změn v přímé pořizovací ceně
Pokud potřebujete změnit přímou pořizovací cenu pro zboží, můžete použít dávkovou úlohu **Upravit náklady/ceny zboží**.  

 Dávková úloha mění obsah v poli **Jednotková cena** na kartě zboží. Dávková úloha mění obsah pole stejným způsobem pro všechno zboží nebo jen pro vybrané zboží. Dávková úloha násobí hodnotu v poli pomocí faktoru úpravy, který zadáte.  

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Upravit náklady/ceny zboží** a pak vyberte související odkaz.  
2. V poli **Upravit pole** zadejte, které zboží nebo pole karty SKJ chcete upravit.  
3. V poli **Faktor úpravy** zadejte faktor, podle kterého bude hodnota upravena. Například zadejte **1,5** pro zvýšení hodnoty o 50%.  
4. V záložce **Zboží** nastavte filtry, aby určily například, které zboží se má zpracovávat dávkovou úlohou.  
5. Zvolte tlačítko **OK**.  

## <a name="understanding-unit-cost-calculation"></a>Porozumění výpočtu pořizovací ceny
Hodnota v poli **Pořizovací cena** na kartě zboží je zpravidla založena na pevné pořizovací ceně, která je pro zboží standardem metody ocenění. Kalkulace zboží se všemi ostatními metodami je založena na výpočtu dostupných zásob (fakturované náklady a očekávané náklady) děleno množstvím na skladě.  

 V následujících částech je podrobněji popsáno, jak obsah pole **Metoda ocenění** ovlivňuje výpočet pořizovací ceny na nákupy a prodeje.  

## <a name="unit-cost-calculation-for-purchases"></a>Výpočet pořizovací ceny nákupu  
 Při nákupu zboží se hodnota v poli **Poslední pořizovací cena** na kartě zboží zkopíruje do pole **Nákupní cena** na nákupním řádku nebo na řádku jednotkové ceny na řádku deníku zboží.  

 To, co vyberete v poli **Metoda ocenění**, ovlivňuje jak [!INCLUDE [d365fin](includes/d365fin_md.md)] vypočítá obsah pole **Pořizovací cena** na řádcích.  

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Metoda ocenění FIFO, LIFO, specifická nebo průměrná  
 [!INCLUDE [d365fin](includes/d365fin_md.md)] vypočítá obsah pole **Pořizovací cena (LM)** na nákupním řádku nebo obsah pole **Pořizovací cena** na řádku deníku zboží podle následujícího vzorce:  

 Pořizovací cena (LM) = (Nákupní cena – (Částka slevy / Množství)) x (1 + Nepřímé náklady % / 100) + Režijní náklady  

### <a name="costing-method-standard"></a>Standardní metoda ocenění  
 Pole **Pořizovací cena (LM)** na nákupním řádku nebo pole **Pořizovací ceny** je vyplněno na řádku deníku zboží zkopírováním hodnoty do pole **Pořizovací ceny** na kartě zboží. Při použití metody ocenění nastavené jako standardní je vždy založena na pevné pořizovací ceně.  

 Když zaúčtujete nákup, pořizovací cena z řádku nákupu nebo řádku deníku zboží se zkopíruje do položky nákupní faktury za zboží a lze ji zobrazit v seznamu položek pro zboží.  

### <a name="all-costing-methods"></a>Všechny metody ocenění  
 Pořizovací cena z řádku zdrojového dokladu se používá k výpočtu obsahu pole **Částka nákladů (skutečná)** nebo případně pole **Částka nákladů (očekávaná)**, která se vztahuje k této položce zboží, bez ohledu na způsob ocenění zboží.  

## <a name="unit-cost-calculation-for-sales"></a>Výpočet pořizovací ceny pro prodej  
 Když prodáváte zboží, pořizovací cena se zkopíruje z pole Pořizovací cena na kartě zboží na prodejní řádek nebo na řádek deníku zboží.  

 Když zaúčtujete, pořizovací cena z řádku nákupu nebo řádku deníku zboží se zkopírují do položky nákupní faktury za zboží a lze ji zobrazit v seznamu položek zboží. [!INCLUDE [d365fin](includes/d365fin_md.md)] používá Pořizovací cenu z řádku zdrojového dokladu k výpočtu obsahu pole **Částka nákladů (skutečná)** nebo případně pole **Částka nákladů (očekávaná)** v položce ocenění vztahující se k této položce zboží.  

## <a name="see-also"></a>Viz také
[Správa nákladů zásob](finance-manage-inventory-costs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Prodej](sales-manage-sales.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
