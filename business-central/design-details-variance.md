---
    title: Design Details - Variance | Microsoft Docs
    description: Variance is defined as the difference between the actual cost and the standard cost, as described in the following formula.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Odchylka
Odchylka je definována jako rozdíl mezi skutečnými náklady a standardními náklady, tak jak je popsáno v následujícím vzorci.

skutečné náklady – standardní náklady = odchylka

Pokud se skutečné náklady změní například proto, že účtujete poplatek za zboží k pozdějšímu datu, bude odchylka odpovídajícím způsobem aktualizována.

> [!NOTE]  
> Přecenění neovlivní výpočet odchylky, protože přeceněním se změní pouze hodnota zásob.

## Příklad
Následující příklad ilustruje, jak se vypočítává odchylka u koupeného zboží. Je založen na následujícím scénáři:

1. Uživatel zakoupí zboží za 90.00 LM, ale standardní cena je 100.00 LM. Odchylka nákupu je tedy –10.00 LM.
2. 10.00 LM je připsáno na účet odchylky nákupu.
3. Uživatel zaúčtuje poplatek za zboží ve výši 20.00 LM. V souladu s tím se skutečné náklady zvýší na 110.00 LM a hodnota odchylky nákupu se změní na 10,00 LM.
4. 20.00 LM je připsáno na účet odchylky nákupu. V souladu s tím se čistá odchylka nákupu změní na 10.00 LM.
5. Uživatel přecení položku ze 100,00 LM na 70,00 LM. To nemá vliv na výpočet odchylky, pouze na hodnotu zásob.

Následující tabulka ukazuje výsledné hodnoty.

![Výpočet odchylky nákupu](media/design_details_inventory_costing_11_purchase_variance.png "Výpočet odchylky nákupu")

## Stanovení standardních nákladů
Standardní cena se používá při výpočtu odchylky a částky, která se má kapitalizovat. Vzhledem k tomu, že standardní náklady lze v průběhu času měnit z důvodu ruční aktualizace výpočtu, potřebujete bod v čase, kdy jsou standardní náklady fixovány pro výpočet odchylky. Tímto bod je, když je zvýšení zásob fakturováno. U vyrobených nebo smontovaných položek je okamžikem, kdy jsou stanoveny standardní náklady a to je okamžik, kdy jsou náklady adjustovány.

Následující tabulka ukazuje, jak se při použití funkce Vypočítat standardní náklady počítají různé podíly nákladů pro vyrobené a smontované zboží.

| Podíl nákladů | Zakoupené zboží | Vyrobené/smontované zboží |
|----------------|--------------------|------------------------------|  
| **Standardní náklady** | Jedna úroveň nákl. na materiál + Jedna úroveň nákl. na kapacitu + Jedna úroveň nákl. subdod. + Jed.ú. režijních nákl.kapacity + J.úroveň režijních nákl.výroby |
| **Jedna úroveň nákl. na materiál** | Pořizovací cena | ![Rovnice 1](media/design_details_inventory_costing_11_equation_1.png "Rovnice 1") |
| **Jedna úroveň nákl. na kapacitu** | Nelze použít | ![Rovnice 2](media/design_details_inventory_costing_11_equation_2.png "Rovnice 2") |
| **Jedna úroveň nákl. na kapacitu** | Nelze použít | ![Rovnice 3](media/design_details_inventory_costing_11_equation_3.png "Rovnice 3") |
| **Jed.ú.režijních nákl.výroby** | Nelze použít | ![Rovnice 4](media/design_details_inventory_costing_11_equation_4.png "Rovnice 4") |
| **J.úroveň rež. nákl.výroby** | Nelze použít | (Jedna úroveň nákl. na materiál + Jedna úroveň nákl. na kapacitu + Jedna úroveň nákl. subdod.) * Nepřímé náklady % / 100 + Režijní náklady |
| **Více úrovní nákl. na materiál** | Pořizovací cena | ![Rovnice 5](media/design_details_inventory_costing_11_equation_5.png "Rovnice 5") |
| **Více úrovní nákl. na kapacitu** | Nelze použít | ![Rovnice 6](media/design_details_inventory_costing_11_equation_6.png "Rovnice 6") |
| **Více úrovní nákl.subdodavatele** | Nelze použít | ![Rovnice 7](media/design_details_inventory_costing_11_equation_7.png "Rovnice 7") |
| **Více úrovní nákl. na kapacitu** | Nelze použít | ![Rovnice 8](media/design_details_inventory_costing_11_equation_8.png "Rovnice 8") |
| **Rolled-up Mfg. režijních nákl. na kapacitu** | Nelze použít | ![Rovnice 9](media/design_details_inventory_costing_11_equation_9.png "Rovnice 9") |

## Viz také
[Detaily návrhu: Zásoby a ocenění](design-details-inventory-costing.md)   
[Detaily návrhu: Metody kalkulace nákladů](design-details-costing-methods.md)
[Správa zásob a ocenění](finance-manage-inventory-costs.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]