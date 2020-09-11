---
    title: How to Track Relations Between Demand and Supply | Microsoft Docs
    description: From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Sledování vztahů mezi poptávkou a nabídkou
Z jakéhokoli dokladu o nabídce nebo poptávce v takzvané síti objednávek můžete sledovat poptávku po objednávce (sledované množství), předpověď, plošná prodejní objednávka nebo plánovací parametr (nevysledované množství), který vedl ke vzniku plánovací linie.

Plánovací pracovní listy také nabízejí podpůrné plánovací informace o netradičních entitách, které pomáhají plánovači získat optimální plán zásobování. Pro více informací navštivte [Nesledované prvky plánování](production-how-track-demand-supply.md#untracked-planning-elements).

## Sledování propojených položek
Sledování objednávek ukazuje, jak prodejní objednávky, výrobní zakázky a nákupní objednávky souvisejí s výrobní objednávkou prostřednictvím systémů plánování a rezervace.

Následující text popisuje, jak sledovat propojené položky na pevně plánované výrobní zakázce. Kroky jsou podobné pro všechny ostatní typy objednávek a řádků sešitu plánování. 

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pevně plánovaná výr. zakázka** a poté vyberte související odkaz.
2. Otevřete ze seznamu příslušnou pevně plánovanou výrobní zakázku.
3. Na záložce s náhledem **Řádky**, zvolte akci **Řádky**, a potom vyberte akci **Sledování zakázky**.

Řádky na **Sledování zakázky** zobrazují dokumenty, které se vztahují k aktuálnímu řádku výrobní zakázky.

## Nesledované prvky plánování
Stránka **Nesledované prvky plánování** se otevře, když zvolíme pole **Nesledované množství**, na stránce **Plánování objednávek**. Slouží dvěma účelům:

1. K držení informací o nesledovaných množstvích zobrazených, když uživatel vyhledá stránky Sledování zakázky.
2. K přidržení varovných zpráv zobrazených, když uživatel zvolí ikonu **Varování**  na stránce **Plánovací sešit**.

Tato stránka obsahuje položky, které představují nepozorované nadbytečné množství v síti pro sledování objednávek. Tyto položky jsou generovány během běhu plánování a vysvětlují, odkud pocházejí nadbytečné množství v řádcích pro položku sledování objednávky. Tento nesledovaný přebytek může pocházet z:

- Výrobní prognóza
- Hromadné objednávky
- Minimální zásoby
- Bod přiobjednání
- Maximální zásoby
- Přiobjednané množství
- Maximální množství objednávky
- Minimální množství objednávky
- Násobek objednávky
- Prodleva (% velikosti dávky)

## Viz také
[Plánování](production-planning.md)  
[Doporučené](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Podrobnosti návrhu: Rezervace, sledování zásilky a zasílání zpráv](design-details-reservation-order-tracking-and-action-messaging.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)  
[Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
