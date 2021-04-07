---
title: Define a WIP Method and Monitor Job Progress| Microsoft Docs
description: Describes how you can create a work in process (WIP) method and calculate WIP to estimate the financial value of jobs while they are ongoing.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 10/01/2020
ms.author: edupont

---
# Sledování průběhu a výkonu Projektů
V průběhu projektu se spotřebovávají materiály, zdroje a další výdaje, které je třeba zaúčtovat. Nedokončená výroba (WIP) je funkce, která umožňuje odhadnout finanční hodnotu projektů v hlavní knize v době, kdy projekty stále probíhají. V mnoha případech můžete zaúčtovat výdaje za práci před fakturací projektu. Pokud byly zaúčtovány pouze výdaje, bude finanční výkaz nepřesný. Pro více informací navštivte  [Principy nedokončené výroby](projects-understanding-wip.md).

Chcete-li sledovat hodnotu v hlavní knize, můžete vypočítat cenu nedokončené výroby a zaúčtovat ji do hlavní knihy.

Nedokončenou výrobu lze vypočítat na základě následujících informací:

* Hodnota nákladů
* Hodnota prodeje
* Uznatelné náklady
* Procento dokončení
* Dokončené smlouvy

Chcete-li zobrazit výsledek jinou metodou, můžete metodu změnit a znovu vypočítat nedokončenou výrobu. Počet výpočtů nedokončené výroby není omezen. Nedokončená výroba se pouze vypočítá, ale nezaúčtuje se. Po výpočtu nedokončené výroby můžete zaúčtovat.

## Vytvoření projektu s nedokončenou výrobou
Můžete vytvořit projekt s nedokončenou výrobou, který bude odrážet potřeby Vaší společnosti. Po vytvoření můžete nastavit nedokončenou výrobu jako výchozí metodu kalkulace projektu, která bude použita ve Vaší společnosti.

> [!NOTE]
> Jakmile použijete novou metodu nedokončené výroby na položky, není možné tuto metodu smazat nebo měnit.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Metody NV projektu** a poté vyberte související odkaz.
2. Zvolte tlačítko **Nový** a vyplňte pole dle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Zavřete stránku.
4. Chcete-li tuto novou metodu nastavit jako výchozí, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení projektů** a poté vyberte související odkaz..
5. V poli **Výchozí metoda NV** vyberte metodu ze seznamu.

## Definování Nedokončené výroby pro projekt
Při vytváření nového projektu musíte určit, která metoda nedokončené výroby projektu se použije. V některých případech byla pro Vás jako výchozí nastavena metoda nedokončené výroby projektu, kterou můžete použít.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Projekty** související odkaz.
2. Zvolte tlačítko **Nový**. Pro více informací navštivte [Vytváření projektů](projects-how-create-jobs.md).
3. Na stránce **Karta projektu** v poli **Metoda NV** vyberte metodu nedokončené výroby ze seznamu. Pokud byla definována výchozí metoda, můžete v případě potřeby vybrat jinou možnost.

## Výpočet Nedokončené výroby
Můžete určit částku nedokončené výroby, která má být zaúčtována na rozvahové účty pro vykazování na konci období. Můžete k tomu použít úlohu **Vypočítat NV projektu**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vypočítat NV projektu** a poté vyberte související odkaz.
2. Vyberte akci **Kalkulovat NV**.
3. Na stránce **Vypočítat NV projektu**, vyplňte pole podle potřeby.
4. Vyberte tlačítko **OK**.

> [!NOTE]  
> Úloha počítá pouze nedokončenou výrobu. Nejedná se o účtování. Pro účtování musíte použít úlohu **Zaúčtovat NV projektu** poté, co jste ji vypočítali. Další informace naleznete v následujícím postupu.

## Účtování Nedokončené výroby
Když jste vypočítali nedokončenou výrobu, můžete jí zaúčtovat na rozvahové účty pro vykazování konce období. Můžete k tomu použít úlohu **Zaúčtovat NV projektu**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaúčtovat NV projektu** a poté vyberte související odkaz.
2. Na stránce **Zaúčtovat NV projektu**, vyplňte pole podle potřeby.
3. Vyberte tlačítko **OK**.

## Náhled odhadů využití projektů a průběžné účtování
V jednom kroku můžete zobrazit využití prjektů až do dokončení projektu. Chcete-li tak učinit použijte úlohu **Výpočet zbývajícího použití projektu** pro všechny úkoly až do konce projektu.

To vám umožní sledovat a porovnávat původní odhady se skutečnými výsledky a podle potřeby provádět úpravy nebo přidávat nové položky. Můžete například odhadnout, že úloha vyžaduje 10 hodin a k dnešnímu dni to trvalo 15 hodin. Můžete přidat dalších pět hodin do existujícího řádku deníku nebo vytvořit nový řádek deníku pro vykazování těchto pěti hodin jako přesčas, jako jiný typ práce. Jsou vypočteny příslušné náklady a cena, kdy následně můžete účtovat v deníku.

> [!NOTE]  
> Řádky se zbožím vytvoří položky zboží a sníží množství v zásobách. Úloha **Účtování nákladů na zboží** přenáší náklady zásob do hlavní knihy. Zdroje vytvářejí položky zdrojů.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky projektů** a poté vyberte související odkaz.
2. Vyberte příslušný deník projektů a pak zvolte akci **Výpočet zbývajícího použití**.
3. Na stránce **Výpočet zbývajícho použití** zadejte číslo dokladu a datum zaúčtování, které má být vloženo do deníku, a zvolte tlačítko **OK**.
4. Aktualizujte deník s případnými potřebnými úpravami.
5. Vyberte **Účtovat**

## Zobrazení Položek projektu
Všechny položky související s projektem jsou zaznamenány v žurnálech a jsou číslovány postupně, počínaje 1. Z žurnálu projektu můžete získat přehled o všech položkách projektu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Žurnály projektů** a poté vyberte související odkaz.
2. Vyberte příslšný žurnál a vyberte akci **Žurnály projektů**.

Na stránce **Položky projektu** můžete zkontrolovat položky, které jsou přidruženy k libovolnému projektu.

## Viz také
[Správa projektů](projects-manage-projects.md)
[Správa nákladů zásob](finance-manage-inventory-costs.md)   
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)         
[Prodej](sales-manage-sales.md)      
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]