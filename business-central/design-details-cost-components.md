---
    title: Design Details - Cost Components | Microsoft Docs
    description: Cost components are different types of costs that make up the value of an inventory increase or decrease.
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
# Detaily Návrhu: Komponenty nákladů
Komponenty nákladů se skládájí z různých typy nákladů, které tvoří hodnotu zvýšení nebo snížení zásob.

V následující tabulce jsou uvedeny různé komponenty nákladů a všechny podřízené nákladové komponenty, z nichž se skládají.

| Komponenty nákladů | Podřízené komponenty nákladů | Popis |
|--------------------|--------------------------------|---------------------------------------|  
| Přímé náklady | Jednotková cena (přímá nákupní cena) | Náklady, které lze vysledovat k nákladovému objektu. |
| Přímé náklady | Náklady na dopravu (poplatky za zboží) | Náklady, které lze vysledovat k nákladovému objektu. |
| Přímé náklady | Náklady na pojištění (poplatky za zboží) | Náklady, které lze vysledovat k nákladovému objektu. |
| Nepřímé náklady | Náklady, které nelze vysledovat k nákladovému objektu. |
| Odchylka | Odchylka nákupu | Rozdíl mezi skutečnými a standardními náklady, který je zaúčtován pouze pro zboží pomocí metody **standardních** nákladů. |
| Odchylka | Odchylka materiálu | Rozdíl mezi skutečnými a standardními náklady, který je zaúčtován pouze pro zboží pomocí metody **standardních** nákladů. |
| Odchylka | Odchylka kapacity | Rozdíl mezi skutečnými a standardními náklady, který je zaúčtován pouze pro zboží pomocí metody **standardních** nákladů. |
| Odchylka | Subdodavatelská odchylka | Rozdíl mezi skutečnými a standardními náklady, který je zaúčtován pouze pro zboží pomocí metody **standardních** nákladů. |
| Odchylka | Odchylka režijních kapacit | Rozdíl mezi skutečnými a standardními náklady, který je zaúčtován pouze pro zboží pomocí metody **standardních** nákladů. |
| Odchylka | Odchylka režijních nákladů výroby | Rozdíl mezi skutečnými a standardními náklady, který je zaúčtován pouze pro zboží pomocí metody **standardních** nákladů. |
| Přecenění | Odpis nebo zhodnocení aktuální hodnoty zásob. |
| Zaokrouhlení | zbytky způsobené způsobem výpočtu snížení hodnoty zásob. |

> [!NOTE]  
> Náklady na dopravu a pojištění jsou poplatky za zboží, které lze kdykoli přidat k ceně zboží. Když spustíte dávkovou úlohu  **Adjustace nákladů položek zboží** hodnota všech souvisejících snížení zásob se odpovídajícím způsobem aktualizuje.

## Viz také
[Detaily návrhu: Detaily: Náklady zásob](design-details-inventory-costing.md)   
[Detaily návrhu: Odchylka](design-details-variance.md)
[Správa nákladů zásob](finance-manage-inventory-costs.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]