---
title: How to Set Up Stockkeeping Units
description: You can use stockkeeping units to record information about your items for a specific location or a specific variant code.
author: SorenGP

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.search.forms: 5704, 5700, 5702, 5701
ms.date: 04/01/2021
ms.author: edupont

---
# Nastavení skladové jednotky
Skladové jednotky můžete použít k záznamu informací o zboží pro konkrétní lokace nebo kód varianty.

Skladové jednotky jsou doplňkem ke kartám zboží. Nenahrazují je, i když s nimi souvisí. Skladovací jednotky umožňují rozlišovat informace o zboží pro konkrétní lokaci, jako je sklad nebo distribuční centrum, nebo konkrétní varianta, jako jsou různá čísla polic a různé informace o doplňování, pro stejné zboží.

## Nastavení skladové jednotky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skladové jednotky** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vyplňte pole na kartě. Následující pole jsou povinná: **Číslo zboží**, **Kód lokace** a/nebo **Kód varianty**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Pokud jste pro zboží nastavili první skladovou jednotku, je zaškrtnuto políčko **Skladová jednotka existuje** na kartě **Zboží**.

Chcete-li pro položku vytvořit několik skladových jednotek, použijte dávkovou úlohu **Vytvořit skladovou jednotku**.

> [!NOTE]  
> Informace na kartě **Skladová jednotka** mají přednost před kartou **Zboží**.

> [!Warning]
> Pokud je SKJ dodáváno prostřednictvím výroby, pak se pole **Standardní náklady** při fakturaci a úpravě skutečných nákladů na vyrobenou položku nepoužívá. Místo toho se použije pole **Standardní cena** na kartě zboží na nižších úrovních a případné odchylky se počítají proti podílům na nákladech této položky.<br /><br />
> Protože výrobní kusovníky a TNG postup nemohou být přiřazeny k SKJ, pak souhrn jednotkových nákladů a související výpočet podílů na nákladech také nejsou k dispozici na SKJ. Pro více informací navštivte [O výpočtu pevné pořizovací ceny](finance-about-calculating-standard-cost.md)

## Viz také
[Evidence nového zboží](inventory-how-register-new-items.md)    
[Nastavení řízení skladu](warehouse-setup-warehouse.md)    
[Řízení skladu](warehouse-manage-warehouse.md)    
[Zásoby](inventory-manage-inventory.md)    
[Řízení montáže](assembly-assemble-items.md)      
[Podrobnosti o designu: Řízení skladu](design-details-warehouse-management.md)    
[Pracovat s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]