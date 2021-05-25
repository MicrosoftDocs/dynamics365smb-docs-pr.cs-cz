---
    title: Design Details - Expected Cost Posting | Microsoft Docs
    description: Expected costs represent the estimation of, for example, a purchased item’s cost that you record before you receive the invoice for the item.
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
# Detaily návrhu: Účtování očekávaných nákladů
Očekávané náklady představují odhad například nákladů na zakoupené zboží, které zaznamenáte před přijetím faktury za zboží.

Očekávané náklady můžete zaúčtovat do zásob a do financí. Když zaúčtujete množství, které je pouze přijato nebo odesláno, ale není fakturováno, vytvoří se položka ocenění s očekávanými náklady. Tyto očekávané náklady ovlivňují hodnotu zásob, ale nejsou zaúčtovány do financí, pokud k tomu nenastavíte systém.

> [!NOTE]  
> Očekávané náklady jsou spravovány pouze u transakcí za zboží. Očekávané náklady neplatí pro nehmotné typy transakcí, jako jsou poplatky za kapacitu a zboži.

Pokud byla zaúčtována pouze část množství, která zvyšuje zásoby, hodnota zásob ve financích se nezmění, pokud jste na stránce **Nastavení zásob** nezaškrtli políčko **Účtování oček.nákladů do fin.**. V takovém případě se očekávané náklady zaúčtují na mezitímní účty v okamžiku přijetí. Poté, co byla příjemka plně fakturována, jsou prozatímní účty vyrovnány a skutečné náklady jsou zaúčtovány na účet zásob.

Pro podporu odsouhlasení a sledovatelnosti práce zobrazuje zaúčtovaná položka ocenění očekávanou částku nákladů, která byla zaúčtována k vyrovnání mezitímních účtů.

## Příklad
Následující příklad ukazuje očekávané náklady, pokud jsou na stránce **Nastavení zásob** zaškrtnuta políčka **Automatické účtování nákladů** a **Účtování oček.nákladů do fin.**.

Zaúčtujete nákupní objednávku tak, jak byla přijata. Očekávaná cena je 95,00 CZK.

**Položky ocenění**

| Zúčtovací datum | Typ položky | Částka nákladů (očekávaná) | Zaúčtované očekávané náklady | Očekávané náklady | Číslo položky zboží | Číslo položky |
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
| 1.1.2020 | Přímé náklady | 95,00 | 95,00 | Ano | 1 | 1 |

**Vazba položek v tabulce Vazba věcná pol. - pol. zboží**

| Číslo věcné položky | Č. položky ocenění | Číslo finančního žurnálu |
|--------------------|---------------------|-----------------------|  
| 1 | 1 | 1 |
| 2 | 1 | 1 |

**Věcné položky**

| Zúčtovací datum | Finanční účet | Číslo účtu (En-US Demo) | Částka | Číslo položky |
|------------------|------------------|---------------------------------|------------|---------------|  
| 1.1.2020 | Účet časového rozlišení zásob (dočasné) | 5530 | -95,00 | 2 |
| 1.1.2020 | Účet zásob (dočasné) | 2131 | 95,00 | 1 |

Později zaúčtujete nákupní objednávku jako fakturovanou. Fakturované náklady jsou 100,00 CZK.

**Položky ocenění**

| Zúčtovací datum | Částka nákladů (skutečná) | Částka nákladů (očekávaná) | Zaúčtované náklady | Očekávané náklady | Číslo položky zboží | Číslo položky |
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
| 15.1.2020 | 100,00 | -95,00 | 100,00 | Ne | 1 | 2 |

**Vazba položek v tabulce Vazba věcná pol. - pol. zboží**

| Číslo věcné položky | Č. položky ocenění | Číslo finančního žurnálu |
|--------------------|---------------------|-----------------------|  
| 3 | 2 | 2 |
| 4 | 2 | 2 |
| 5 | 2 | 2 |
| 6 | 2 | 2 |

**Věcné položky**

| Zúčtovací datum | Finanční účet | Číslo účtu (En-US Demo) | Částka | Číslo položky |
|------------------|------------------|---------------------------------|------------|---------------|  
| 15.1.2020 | Účet časového rozlišení zásob (dočasné) | 5530 | 95,00 | 4 |
| 15.1.2020 | Účet zásob (dočasné) | 2131 | -95,00 | 3 |
| 15.1.2020 | Účet použitých přímých nákl. | 7291 | -100 | 6 |
| 15.1.2020 | Účet zásob | 2130 | 100 | 5 |

## Viz také
[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)     
[Detaily návrhu: Úprava nákladů](design-details-cost-adjustment.md)     
[Detaily návrhu: Odsouhlasení s hlavní knihou](design-details-reconciliation-with-the-general-ledger.md)     
[Detaily návrhu: Účtování zásob](design-details-inventory-posting.md)     
[Detaily návrhu: Odchylka](design-details-variance.md)    
[Správa nákladů zásob](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]