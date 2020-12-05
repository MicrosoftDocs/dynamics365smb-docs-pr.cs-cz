---
    title: Service Price Management | Microsoft Docs
    description: This topic describes how to apply the best price to service orders, set up personalized service price agreements for customers, improve service employees' efficiency, and accelerate the invoicing process.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: bholtorf

---
# Správa cen servisu
Funkce správy cen servisu vám umožňuje aplikovat nejlepší ceny na servisní zakázky, uzavřít dohody o personalizovaných cenách servisu pro zákazníky, zlepšit efektivitu zaměstnanců servisu a urychlit fakturační proces.

Správa cen servisu vám umožňuje nastavit různé cenové skupiny servisu, abyste mohli kromě typu závady, kterou servisní úloha zahrnuje, uvážit i předmět servisu nebo skupinu předmětů servisu. Tyto skupiny můžete nastavit na omezenou dobu nebo pro konkrétního zákazníka nebo měnu. Struktury výpočtu ceny můžete použít jako šablony k přiřazení určité ceny ke konkrétní servisní zakázce.

To například umožňuje, kromě druhu práce, přiřadit navíc i konkrétní zboží zahrnuté v ceně servisu. To také umožňuje použít různé částky DPH a slev pro různé cenové skupiny servisu. Abyste se ujistili, že jsou použity správné ceny, můžete přiřadit pevné, minimální nebo maximální ceny v závislosti na dohodách, které máte se svými zákazníky.

Před úpravou ceny předmětu servisu v servisní zákazce získáte přehled o tom, jaké budou výsledky úpravy ceny. Tyto výsledky můžete schválit nebo můžete provést další změny, pokud chcete dostat jiný výsledek. Celé nastavení se provádí řádek po řádku, což znamená, že nejsou vytvořeny žádné další řádky.

A konečně, statistiky cenových skupin servisu a standardní sestavy umožňují sledovat ziskovost každé cenové skupiny servisu.

## Skupiny úprav ceny servisu
Skupiny úprav ceny servisu můžete použít k nastavení různých typů úprav cen. Můžete například vytvořit skupinu úpravy ceny servisu, která upravuje ceny podle náhradních dílů, skupinu, která upravuje ceny podle práce, skupinu, která upravuje ceny podle nákladů atd. Můžete také určit, zda se má úprava ceny servisu použít pouze na konkrétní zboží nebo zdroj nebo na veškeré zboží nebo zdroje.

Každá skupina úprav ceny servisu obsahuje informace o úpravách, které chcete provést na řádcích servisu.

Funkce úpravy ceny servisu se nevztahuje na předměty servisu, které patří do servisních smluv. Můžete upravit pouze servisní ceny předmětů, které jsou součástí servisní zakázky. Nelze upravit cenu předmětu servisu, pokud má záruku. Nelze upravit cenu předmětu servisu v servisní zakázce, pokud s ním spojený řádek servisu byl zaúčtován jako faktura, zcela nebo částečně.

Při spuštění funkce úpravy ceny servisu budou všechny slevy v zakázce nahrazeny hodnotami úpravy ceny servisu.

## Cenové skupiny servisu
Můžete nastavit cenové skupiny servisu a vytvořit skupiny předmětů servisu, které obdrží stejné speciální ceny servisu. Pokud jste nastavili cenové skupiny servisu, můžete je přiřadit k předmětům servisu na řádcích předmětů servisu. Cenové skupiny servisu můžete také přiřadit ke skupinám předmětů servisu.

Před přiřazením cenové skupiny servisu k předmětu servisu musíte určit, na kterou oblast poruchy, měnu nebo skupinu úprav ceny servisu se tato cena vztahuje. Musíte určit, na jakou částku by se měla cena servisu upravit, a zda by tato částka měla zahrnovat DPH a slevy. Musíte také určit, zda se tato úprava týká pevné částky, nebo zda by měla být použita pouze za určitých podmínek.

Když k předmětu servisu přiřadíte cenovou skupinu servisu, pak se na tento předmět servisu budou vztahovat všechny speciální ceny servisu, které jste nastavili v této skupině.

## Cena servisu
Nastavíte skutečné typy cen servisu (typ úpravy ceny a cena) pro kombinaci cenových skupin servisu a cenových skupin zákazníka. Pro každý typ ceny servisu vyberete skupinu úpravy ceny servisu. Můžete také určit typ úpravy ceny servisu, pevný, maximální nebo minimální a skutečnou cenu.

Můžete například nastavit typy cen servisu pro cenovou skupinu rádio servis. Pro zákazníky bez cenové skupiny se můžete rozhodnout, že budete mít k dispozici ceny servisu s maximální cenou práce, což je skupina úpravy ceny práce. Pro zákazníky s konkrétní cenovou skupinou se můžete rozhodnout, že budete mít k dispozici ceny za servis s pevnou cenou za práci, tedy stejnou skupinu úprav ceny práce.

## Úpravy cen servisu
Úpravy cen servisu vám umožňují upravit cenu zboží, zdroje, účtu hlavní knihy nebo nákladů na servisní zakázku.

Po zadání zboží do řádku předmětu servisu zadáte všechny informace o nákladech tohoto zboží na servisní řádky. Když spustíte funkci Upravit servisní cenu, můžete si prohlédnout úpravy cen. Můžete provést úpravy, pokud musíte. Když potvrdíte úpravy, vypočítají se úpravy a poté se přenesou na řádky servisu. Poté odešlete servisní zakázku.

V závislosti na typu úpravy ceny servisu se vypočítá celková částka úpravy.

Následující tabulka popisuje výpočty.

| Možnost | Popis |
|----------------------------------|---------------------------------------|  
| **Pevná cena** | To znamená, že účtujete pevnou cenu za předmět servisu, zdroj, účet hlavní knihy nebo náklady, bez ohledu na skutečné náklady nebo běžné poplatky. Výběr této možnosti znamená, že úprava ceny servisu dosáhne přesné částky uvedené v cenové skupině servisu. |
| **Maximum** | To znamená, že zákazníkovi stanovíte horní limit poplatku bez ohledu na skutečné náklady nebo pravidelné poplatky. Výběr této možnosti znamená, že úprava ceny servisu bude provedena pouze v případě, že celková cena přesáhne částku uvedenou v cenové skupině servisu. |
| **Minimum** | To znamená, že zákazníkovi uložíte nižší limit poplatku bez ohledu na skutečné náklady nebo pravidelné poplatky. Výběr této možnosti znamená, že úprava ceny servisu bude provedena, pouze pokud je celková částka nižší než částka uvedená v cenové skupině servisu. |

## Viz také
[Nastavení cen a dodatečných nákladů servisu](service-how-setup-service-costs-pricing.md)  
[Nastavení správy servisu](service-setup-service.md)
