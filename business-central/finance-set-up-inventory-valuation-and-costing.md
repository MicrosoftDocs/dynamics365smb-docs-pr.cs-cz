---
    title: Set Up Inventory Valuation and Costing | Microsoft Docs
    description: The following table describes a sequence of tasks, with links to the topics that describe them.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Nastavení oceňování zásob a nákladů
Abyste se ujistili, že jsou náklady zásob zaznamenány správně, musíte před zahájením transakcí se zbožím nastavit různá pole a stránky.

Následující tabulka popisuje posloupnost úkolů s odkazy na témata, která je popisují.

| **K** | **Videní** |
|------------|-------------|  
| Pro každou položku nastavte metodu ocenění, abyste určili, jak budou použity její vstupní náklady k vyhodnocení hodnoty zásob a nákladů na prodané zboží. | [Registrace nového zboží](inventory-how-register-new-items.md) |
| Ujistěte se, že náklady jsou automaticky zaúčtovány do hlavní knihy při každém zaúčtování skladové transakce. | Pole **Automatické účtování nákladů** na stránce **Nastavení zásob** |
| Ujistěte se, že očekávané náklady jsou zaúčtovány do hlavní knihy, abyste z dočasných účtů zásob viděli odhad dlužných částek a nákladů na obchodované položky před jejich skutečným zaúčtováním. | Pole **Účtování oček.nákladů do fin.** na stránce **Nastavení zásob** |
| Nastavte systém tak, aby automaticky upravil všechny změny nákladů při každém zaúčtování skladových transakcí. | [Úprava nákladů zboží](inventory-how-adjust-item-costs.md) |
| Definujte, zda se průměrné náklady mají vypočítat pouze pro zboží nebo pro zboží u každé sledované jednotky a pro každou variantu zboží. | Pole **Typ výpočtu prům. poř.ceny** na stránce **Nastavení zásob** |
| Vyberte časové období, které má aplikace použít pro výpočet vážených průměrných nákladů na zboží, které používá metodu průměrného ocenění. | Pole **Období průměrných nákladů** na stránce **Nastavení zásob** |
| Definujte skladová období pro řízení hodnoty zásob v čase tím, že povolíte zaúčtování transakce v uzavřených skladových obdobích. | [Práce se skladovými obdobími](finance-how-to-work-with-inventory-periods.md) |
| Zajistěte, aby byly vrácené tržby použity na původní odchozí transakci, aby se zachovala hodnota zásob. | Pole **Nutné vrác.přesn.nákladů** na stránce **Prodeje a pohledávky** |
| Ujistěte se, že nákupní vratky jsou použity na původní příchozí transakci aby byla zachována hodnota zásob. | Pole **Nutné vrác.přesn.nákladů** na stránce **Nákupy a závazky** |
| Nastavte pravidla zaokrouhlení, která se použijí při úpravě nebo navrhování cen zboží a při úpravě nebo navrhování standardních nákladů. | Stránka **Způsob zaokrouhlení** |

## Viz také
[Správa nákladů zásob](finance-manage-inventory-costs.md)  
[Práce s Business Central](ui-work-product.md)  
[Finance](finance.md)
