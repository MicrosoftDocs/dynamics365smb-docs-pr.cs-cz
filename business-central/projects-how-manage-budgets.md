---
title: Set Up and Manage a Budget for a Job| Microsoft Docs
description: Describes how to plan resources and forecast and control the costs of a project by setting up a budget for each job.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 10/01/2019
ms.author: sgroespe

---
# Správa rozpočtů projektu
Pro každý projekt můžete nastavit rozpočet. Rozpočet se používá k plánování zdrojů, které k projektu přidělujete. Rozpočet může být buď obecný s několika položkami, nebo může obsahovat více položek, které jsou rozděleny do úrovní aktivity. Poté můžete porovnat rozpočtové částky se skutečnou spotřebou zaznamenanou v deníku projektů. Sledováním rozdílů mezi skutečným využitím a rozpočtovaným využitím můžete řídit probíhající projekt a zlepšit kvalitu budoucích projektů snížením rizika podceňování nákladů.

Následující postup popisuje, jak odhadnout rozpočtované náklady během plánování. Pro více informací o zaznamenávání rozpočtovaných cen oproti skutečným cenám práce a nákladům navštivte [Evidence spotřeby na projektu](projects-how-record-job-usage.md).

## <a name="JobBudgetCosts"></a> Odhad rozpočtových nákladů na projekt
Pokud chce zákazník znát cenu projektu, který bude fakturován na základě spotřeby, musíte určit rozpočtové náklady projektu. K tomu použijte stránku **Řádky úlohy projektu**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Otevřete příslušný projekt.
3. Vyberte řádek úkolu typu Účtování a poté vyberte akci **Řádky plánování projektu**.
4. Na novém řádku vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Označení pole **Typ řádku**, naleznete v následujících informacích.

| Typ řádku | Popis |
| --- | --- |
| **Plán i Fakturovatelné** | Částky nákladů a cen zadané do řádku plánování jsou rozpočtové náklady pro konkrétní řádek plánování. Částka ceny bude fakturována. |
| **Plán** | Zákazník není za používání účtován. Použití není převedeno na fakturu, ale bude stále použito při výpočtu Nedokončené výroby. |
| **Fakturovatelné** | Za použití je zákazník účtován. Použití je převedeno na fakturu na základě množství určeného v poli Množství k transf. k fakturaci. |

> [!NOTE]
> Pole **Plánované datum dodávky** plánovacího řádku obsahuje datum, kdy se očekává dokončení použití související s řádkem plánování. Je to také datum, kdy může být řádek plánování převeden na prodejní fakturu a zaúčtován. <br /><br /> Na podkladové úloze projektu na stránce **Karta projektu**, obsahují jednotlivé pole **Počáteční datum** a **Koncové datum** určitou hodnotu z pole **Plánované datum dodávky** na nejstarších a nejnovějších řádcích plánování projektu související stránky - **Řádky plánování projektu**.

> [!NOTE]
> Když vyplníte pole **Množství**, budou všechny informace o celkové ceně a celkových nákladech vypočteny a vyplněny pro tento plánovací řádek. Můžete je kdykoli upravit.

Na stránce **Karta projektu**, můžete nyní zobrazit souhrn celkových rozpočtových nákladů, rozpočtovaných cen, fakturovatelných nákladů a fakturovatelných cen pro každý projekt.

Pro více informací o zaznamenávání rozpočtovaných cen oproti skutečným cenám práce a nákladům navštivte [Evidence spotřeby na projektu](projects-how-record-job-usage.md).

## Viz také
[Správa projektů](projects-manage-projects.md)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
