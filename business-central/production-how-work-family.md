---
    title: How to Use Item Families in Manufacturing | Microsoft Docs
    description: The main task in customizing a base calendar for your company, or one of its business partners, is to enter any changes to working and nonworking day status.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2019
    ms.author: sgroespe

---
# Práce s výrobními skupinami zboží
Produkční skupina je skupina jednotlivého zboží, jejichž vztah je založen na podobnosti jejich výrobních procesů. Vytvářením výrobních skupin lze některé položky vyrábět dvakrát nebo více v jedné výrobě, což optimalizuje spotřebu materiálu.

V poli **Množství** na stránce **Skupina** zadejte množství, které bude vytvořeno, když bude celá skuúina jednou vyrobena.

## Příklad
Při procesu děrování mohou být čtyři kusy stejného zboží vyrobeny z jednoho listu a 10 kusů z jiného, odlišného a současně. Děrovací stroj děruje všech 14 kusů v jednom kroku.

Vytváření výrobních skupin snižuje množství šrotu, protože to, co by za normálních okolností zbylo, bude při výrobě velkých kusů použito k výrobě malých kusů.

## Nastavení skupiny výrobků
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny zboží** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Výroba na základě skupiny výrobků
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pevně plánované výr.   zak.** a poté vyberte související odkaz.
2. Vytvoření nové výrobní zakázky. Pro více informací navštivte [Vytvoření montážní zakázky](production-how-to-create-production-orders.md).
3. V poli **Typ zdroje** vyberte **Skupiny zboží**.
4. V poli **Číslo zdroje** vyberte příslušnou skupiny zboží.

## Viz také
[Vytvoření výrobního kusobníku](production-how-to-create-production-boms.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
