---
    title: Design Details - Transfers in Planning | Microsoft Docs
    description: This topic describes how to use transfer orders as a source of supply when planning inventory levels.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: design, transfer, sku, locations, warehouse
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Plánování transferů
Objednávky transferu jsou také zdrojem nabídky při práci na úrovni skladové položky. Při použití více lokací (skladů) lze systém doplňování skladové položky nastavit na Transfer, což znamená, že lokace je doplněna převodem zboží z jiné lokace. V situaci s více sklady mohou mít společnosti řetězec transferů, kdy je transfer do lokace ZELENÝ převeden ze ŽLUTÝ a dodávka do ŽLUTÝ je převedena z ČERVENÝ a tak dále. Na začátku řetězce je systém doplnění z Výr. Zakázky nebo Nákupu.

![Příklad toku transferu](media/nav_app_supply_planning_7_transfers1.png "Příklad toku transferu")

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Při porovnávání situace, kdy objednávka dodávky přímo čelí objednávce poptávky, se situací, kdy je prodejní objednávka dodávána prostřednictvím řetězce transferu SKJ, je zřejmé, že úkol plánování v posledně uvedené situaci se může stát velmi složitým. Pokud se poptávka změní, může to způsobit zvlnění v řetězci, protože všechny objednávky transferu plus nákupní/výrobní objednávka na opačném konci řetězce budou muset být zmanipulovány, aby se obnovila rovnováha mezi poptávkou a nabídkou.

![Příklad rovnováhy mezi nabídkou a poptávkou v transferech](media/nav_app_supply_planning_7_transfers2.png "Příklad rovnováhy mezi nabídkou a poptávkou v transferech")

## Proč je Transfer speciální případ?
Objednávka transferu vypadá podobně jako každá jiná objednávka v aplikaci. V zákulisí je to však velmi odlišné.

Jedním ze základních aspektů, díky nimž se převody v plánování liší od nákupních a výrobních objednávek, je to, že řádek transferu představuje současně poptávku i nabídku. Odchozí část, která je odeslána ze starého místa, je poptávka. Příchozí část, která má být přijata na novém místě, je na této lokaci dodávkou.

![Obsah stránky objednávka transferu](media/nav_app_supply_planning_7_transfers3.png "Obsah stránky objednávka transferu")

To znamená, že když systém manipuluje se stranou převodu na straně nabídky, musí provést podobnou změnu na straně poptávky.

## Převody jsou závislou poptávkou
Závislá poptávka a nabídka se do jisté doby podobají komponentám řádku výrobní zakázky, ale rozdíl je v tom, že komponenty budou na další plánovací úrovni a s jiným zbožím, zatímco obě části převodu se nacházejí na stejné úrovni pro stejné zboží.

Důležitou podobností je, že stejně jako komponenty jsou závislou poptávkou, tak je i transfer poptávek. Poptávka z řádku transferu je diktována na straně nabídky transferu v tom smyslu, že pokud dojde ke změně nabídky, je poptávka přímo ovlivněna.

Pokud je flexibilita plánování Žádná, řádek transferu by nikdy neměl být považován za nezávislou poptávku při plánování.

V plánovacím postupu by měla být poptávka po transferu zohledněna až poté, co plánovací systém zpracuje stranu nabídky. Předtím není známa skutečná poptávka. Pořadí provedených změn je proto při transferu objednávek velmi důležité.

## Sekvence plánování
Následující obrázek znázorňuje, jak by mohl vypadat řetězec transferů.

![Příklad jednoduchého toku transferu](media/nav_app_supply_planning_7_transfers4.png "Příklad jednoduchého toku transferu")

V tomto příkladu si zákazník objedná zboží na lokaci ZELENÝ. Umístění ZELENÝ se dodává transferem z centrálního skladu ČERVENÝ. Centrální sklad ČERVENÝ je zásobován transferem z výroby na lokaci MODRÝ.

V tomto příkladu bude plánovací systém začínat na přání zákazníka a bude se v řetězci propracovávat zpět. Poptávky a nabídky budou zpracovány postupně

![Plánování dodávek s transfery](media/nav_app_supply_planning_7_transfers5.png "Plánování dodávek s transfery")

## Kód úrovně transferu
Pořadí, ve kterém jsou lokace v plánovacím systému zpracovávány, je určeno kódem úrovně transferu skladové položky

Kód úrovně transferu je interní pole, které se automaticky vypočítá a uloží do skladové položky při vytvoření nebo změně skladové položky. Výpočet běží napříč všemi skladními položkami pro danou kombinaci zboží / varianty a používá kód lokace a kód transferu k určení trasy, kterou bude plánování muset použít při procházení skladových položek, aby bylo zajištěno zpracování všech poptávek.

Kód úrovně transferu bude 0 pro skladové položky se systémem doplnění Nákup nebo Výrobní zakázka a bude -1 pro první úroveň transferu, -2 pro druhou a tak dále. Ve výše popsaném řetězci transferu by proto byly úrovně -1 pro ČERVENÝ a -2 pro ZELENÝ, jak je znázorněno na následujícím obrázku.

![Obsah stránky karty skladové položky](media/nav_app_supply_planning_7_transfers6.gif "Obsah stránky karty skladové položky")

Při aktualizaci skladové položky plánovací systém zjistí, zda jsou skladové položky se systémem transferu doplnění nastaveny s cyklickými odkazy.

## Plánování transferů bez skladové položky

I když se funkce skladové položky nepoužívá, je možné použít lokaci a provést ruční transfer mezi lokacemi. Pro společnosti s méně pokročilým nastavením skladu podporuje plánovací systém scénáře, kdy jsou existující zásoby přeneseny ručně do jiné lokace například k pokrytí prodejní objednávky na tomto místě. Současně by měl plánovací systém reagovat na změny v poptávce.

Aby bylo možné podpořit ruční transfery, bude plánování analyzovat stávající objednávky transferu a poté naplánovat pořadí, ve kterém mají být lokace zpracovány. Interně bude plánovací systém pracovat s dočasnými skladovými jednotkami nesoucími kódy úrovní transferu.

![Kód úrovně transferu](media/nav_app_supply_planning_7_transfers7.png "Kód úrovně transferu")

Pokud existuje více transferů do dané lokace, první převodní příkaz definuje směr plánování. Transfery běžící opačným směrem budou zrušeny.

## Změna množství s rezervacemi
Při změně množství stávající dodávky bere plánovací systém v úvahu rezervace v tom smyslu, že rezervované množství představuje dolní hranici pro to, o kolik lze dodávku snížit.

Při změně množství na existujícím řádku převodního příkazu mějte na paměti, že dolní limit bude definován jako nejvyšší rezervované množství odchozího a příchozího řádku transferu.

Pokud je například, řádek převodního příkazu s 117 kusy rezervován proti prodejnímu řádku 46 a nákupnímu řádku 24, není možné snížit řádek převodu pod 46 kusů, i když to může představovat nadměrné dodávky na vstupní straně.

![Rezervace v plánování transferů](media/nav_app_supply_planning_7_transfers8.png "Rezervace v plánování transferů")

## Změna množství v řetězci transferu
V následujícím příkladu je výchozím bodem vyvážená situace s řetězcem transferu dodávajícím prodejní objednávku 27 na lokaci ČERVENÝ s odpovídající nákupní objednávkou na umístění MODRÝ, transferovaná prostřednictvím umístění RŮŽOVÝ. Kromě prodeje a nákupu proto existují dvě objednávky převodu: MODRÝ-RŮŽOVY a RŮŽOVÝ-ČERVENÝ.

![Změna množství v plánování transferu 1](media/nav_app_supply_planning_7_transfers9.png "Změna množství v plánování transferu 1")

Nyní se plánovač v lokalitě RŮŽOVÝ rozhodne rezervovat proti nákupu.

![Změna množství v plánování transferu 2](media/nav_app_supply_planning_7_transfers10.png "Změna množství v plánování transferu 2")

To obvykle znamená, že plánovací systém bude ignorovat nákupní objednávku a poptávku po transferu. Dokud existuje rovnováha, není problém. Ale co se stane, když zákazník v lokalitě ČERVENÝ částečně lituje objednávky a změní ji na 22?

![Změna množství v plánování transferu 3](media/nav_app_supply_planning_7_transfers11.png "Změna množství v plánování transferu 3")

Když se plánovací systém znovu spustí, měl by se zbavit přebytečné nabídky. Rezervace však uzamkne nákup a převod na množství 27.

![Změna množství v plánování transferu 4](media/nav_app_supply_planning_7_transfers12.png "Změna množství v plánování transferu 4")

Transfer RŮŽOVÝ-ČERVENY byl snížen na 22. Příchozí část převodu MODRÝ-RŮŽOVÝ není vyhrazena, ale protože je vyhrazena odchozí část, není možné snížit množství pod 27.

## Výpočet průběžné doby
Při výpočtu data splatnosti objednávky transferu budou brány v úvahu různé druhy průběžné lhůty.

Průběžné doby, které jsou aktivní při plánování převodu, jsou:

* Výstupní doba zpracování ve skladu
* Doba dodávky
* Výstupní doba zpracování ve skladu
* Na řádku plánování se k poskytnutí informací o výpočtu používají následující pole.
* Datum dodávky transferu
* Počáteční datum
* Datum ukončení
* Datum splatnosti

Datum dodávky řádku transferu bude zobrazeno v poli Datum dodávky transferu a datum příjmu řádku transferu bude zobrazeno v poli Datum splatnosti.

Počáteční a koncové datum bude použito k popisu skutečného období přepravy.

Následující obrázek znázorňuje interpretaci počátečního data a koncového data a času plánování na řádcích plánování souvisejících s objednávkami transferu

![Centrální časy dat v plánování transferů](media/nav_app_supply_planning_7_transfers13.png "Centrální časy dat v plánování transferů")

V tomto příkladu to znamená, že:

* Datum dodávky + Odchozí zpracování = Počáteční datum
* Počáteční datum + Doba dodávky = Datum ukončení
* Datum ukončení + Příchozí zpracování = Datum příjmu

## Bezpečná průběžná doba
Pole Výchozí bezpečná průběžná doba na stránce Nastavení výroby a související pole Bezpečná průběžná doba na kartě zboží nebudou při výpočtu objednávky transferu zohledněny Bezpečná průběžná doba, však stále ovlivní celkový plán, stejně jako ovlivní zakázku na doplnění stavu zásob (nákup nebo výrobu) na začátku řetězce transferu, když je zboží umístěno na lokaci, ze kterého budou převedeny.

![Prvky termínu splnění transferu](media/nav_app_supply_planning_7_transfers14.png "Prvky termínu splnění transferu")

Na řádku výrobní zakázky je koncové datum + Bezpečná průběžná doba + Výstupní doba zpracování ve skladu = Datum splatnosti.

Na řádku nákupní objednávky je plánované datum příjmu + Bezpečná průběžná doba + Výstupní doba zpracování ve skladu = Očekávané datum příjmu.

## Přeplánovat
Při přeplánování existujícího řádku transferu musí plánovací systém prohledat odchozí část a změnit datum a čas. Je důležité si uvědomit, že pokud byla definována dodací doba, bude mezi dodávkou a příjmem mezera. Jak již bylo zmíněno, dodací doba se může skládat z více prvků, jako je doba přepravy a doba zpracování ve skladu. Na časové ose se plánovací systém posune zpět v čase, zatímco vyvažuje prvky.

![Změna data splatnosti v plánování transferu](media/nav_app_supply_planning_7_transfers15.png "Změna data splatnosti v plánování transferu")

Proto při změně data splatnosti na řádku transferu je nutné vypočítat dobu realizace, aby se aktualizovala odchozí strana přenosu.

## Sériová čísla a čísla šarží v řetězcích transferu
Pokud poptávka nese sériová čísla nebo čísla šarží a je spuštěn plánovací modul, povede to k několika přímo vytvořeným příkazům transferu. Více informací o tomto konceptu naleznete v tématu Atributy zboží. Pokud jsou však jsou z poptávky odstraněna sériová čísla nebo čísla šarží, vytvořené příkazy transferu v řetězci budou stále obsahovat sériová čísla nebo čísla šarží, a proto budou plánováním ignorovány (nebudou odstraněny).

## Propojení dávky-pro-dávku
V této ukázce, skladová položka MODRÝ je nastavena se způsobem přiobjednán, zatímco RŮŽOVÝ a ČERVENÝ používají Dávku-pro-dávku. Když je prodejní objednávka 27 vytvořena na umístění ČERVENÝ, povede to k řetězci transferu s tím, že bude poslední spoj na místě MODRÝ rezervován s vazbou. V tomto příkladu nejsou rezervace tvrdými rezervacemi vytvořenými pomocí plánovače na lokaci RŮŽOVÝ, ale jsou vazbami vytvořenými systémem plánování. Důležitým rozdílem je, že systém plánování může změnit ten druhý.

![Spojení zakázky-na-zakázku v plánování transferu](media/nav_app_supply_planning_7_transfers16.png "Spojení zakázky-na-zakázku v plánování transferu")

Pokud se poptávka změněna z 27 na 22, systém sníží množství dolů v řetězci, přičemž se sníží také závazná rezervace.

## Viz také
[Detaily návrhu: Parametry plánování](design-details-planning-parameters.md)   
[Detaily návrhu: Tabulka přiřazení plánování](design-details-planning-assignment-table.md)   
[Detaily návrhu: Zpracování způsobu přiobjednání](design-details-handling-reordering-policies.md)   
[Detaily návrhu: Poptávka v prázdném skladu](design-details-demand-at-blank-location.md)   
[Detaily návrhu: Centrální koncepce plánovacího systému](design-details-central-concepts-of-the-planning-system.md)   
[Detaily návrhu: Vyvažování poptávky a nabídky](design-details-balancing-demand-and-supply.md)   
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]