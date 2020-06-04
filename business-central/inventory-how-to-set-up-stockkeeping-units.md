---
title: Jak založit skladové jednotky | Microsoft Docs
description: Pomocí skladových jednotek můžete zaznamenávat informace o svým zboží pro konkrétní lokaci nebo kód konkrétní varianty.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/15/2018
ms.author: sgroespe
---
# <a name="set-up-stockkeeping-units"></a>Nastavení skladové jednotky
Pomocí skladových jednotek můžete zaznamenávat informace o svém zboží pro konkrétní lokaci nebo kód konkrétní varianty.  

 Skladové jednotky jsou doplňkem ke kartám zboží. Nenahrazují je, i když s nimi souvisí. Skladové jednotky umožňují rozlišovat informace o zboží pro konkrétní lokaci, jako je sklad nebo distribuční centrum, nebo konkrétní varianta, jako jsou různá čísla polic a různé informace o doplňování, pro stejné zboží.  

## <a name="to-set-up-a-stockkeeping-unit"></a>Nastavení skladové jednotky  

1.  Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skladové jednotky** a poté vyberte související odkaz.  
2.  Zvolte akci **Nový**.  
3.  Vyplňte pole na kartě. Vyžadují se následující pole: **Číslo zboží**, **Kód lokace**, a/nebo **Kód varianty**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Pokud jste pro zboží nastavili první skladovou jednotku, je zaškrtnuto políčko **Skladová jednotka existuje** na kartě **Zboží**.  

Chcete-li pro zboží vytvořit několik skladových jednotek, použijte dávkovou úlohu **Vytvořit skladovou jednotku**.  

> [!NOTE]  
>  Informace na kartě **Skladové jednotky** mají přednost před kartou **Zboží**.

> [!Warning]
> Pokud je SKU dodávána prostřednictvím výroby, pole **Pevná pořizovací cena** se nepoužívá při fakturaci a úpravě skutečných nákladů na vyrobené zboží. Místo toho se použije pole **Pevná pořizovací cena** na kartě podkladového zboží a veškeré odchylky se vypočítají na základě podílů na nákladech daného zboží.<br /><br />
> Protože výrobní kusovníky a zaokrouhlování nemohou být přiřazeny k jednotkám SKU, pak souhrn jednotkových nákladů a související výpočet podílů na nákladech také nejsou k dispozici na jednotkách SKU. Pro více informací navštivte [O výpočtu pevné pořizovací ceny](finance-about-calculating-standard-cost.md).

## <a name="see-also"></a>Viz také  
[Evidence nového zboží](inventory-how-register-new-items.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa skladů](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Správa montáže](assembly-assemble-items.md)    
[Podrobnosti návrhu: Správa skladů](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
