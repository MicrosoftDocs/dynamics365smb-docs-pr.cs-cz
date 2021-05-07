---
    title: Design Details - Accounts in the General Ledger | Microsoft Docs
    description: To reconcile inventory and capacity ledger entries with the general ledger, the related value entries are posted to different accounts in the general ledger.
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
# Detaily návrhu: Účty hlavní knihy
Chcete-li odsouhlasit položky zásob a kapacit s věcnými položkami, jsou související položky ocenění zaúčtovány na různé účty v hlavní finanční knize. Pro více informací navštivte [Detaily návrhu: Odsouhlasení hlavní účetní knihy](design-details-reconciliation-with-the-general-ledger.md).

## Z položek zásob
Následující tabulka ukazuje vztah mezi různými typy položek hodnot zásob a účty a protiúčty v hlavní knize.

| **Typ položky zboží** | **Typ položky ocenění** | **Typ odchylky** | **Očekáváné náklady** | **Účet** | **Protiúčet** |
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
| Nákup | Přímé náklady | Ano | Zásoby (dočasné) | Účet adjustace zboží (Dočasné) |
| Nákup | Přímé náklady | Ne | Zásoby | Použité přímé náklady |
| Nákup | Nepřímé náklady | Ne | Zásoby | Vyrvonaná režie |
| Nákup | Odchylka | Nákup | Ne | Zásoby | Odchylka nákupu |
| Nákup | Přecenění | Ne | Zásoby | Oprava zásob |
| Nákup | Zaokrouhlení | Ne | Zásoby | Oprava zásob |
| Prodej | Přímé náklady | Ano | Zásoby (dočasné) | COGS (Interim) |
| Prodej | Přímé náklady | Ne | Zásoby | COGS |
| Prodej | Přecenění | Ne | Zásoby | Oprava zásob |
| Prodej | Zaokrouhlení | Ne | Zásoby | Oprava zásob |
| Příjem, Výdej, Transfer | Přímé náklady | Ne | Zásoby | Oprava zásob |
| Příjem, Výdej, Transfer | Přecenění | Ne | Zásoby | Oprava zásob |
| Příjem, Výdej, Transfer | Zaokrouhlení | Ne | Zásoby | Oprava zásob |
| Spotřeba (Výroby) | Přímé náklady | Ne | Zásoby | Nedokončená výroba |
| Spotřeba (Výroby) | Přecenění | Ne | Zásoby | Oprava zásob |
| Spotřeba (Výroby) | Zaokrouhlení | Ne | Zásoby | Oprava zásob |
| Spotřeba montáže | Přímé náklady | Ne | Zásoby | Oprava zásob |
| Spotřeba montáže | Přímé náklady | Ne | Použité přímé náklady | Oprava zásob |
| Spotřeba montáže | Nepřímé náklady | Ne | Vyrvonaná režie | Oprava zásob |
| Výstup (Výroby) | Přímé náklady | Ano | Zásoby (dočasné) | Nedokončená výroba |
| Výstup (Výroby) | Přímé náklady | Ne | Zásoby | Nedokončená výroba |
| Výstup (Výroby) | Nepřímé náklady | Ne | Zásoby | Vyrvonaná režie |
| Výstup (Výroby) | Odchylka | Materiál | Ne | Zásoby | Material Variance |
| Výstup (Výroby) | Odchylka | Kapacita | Ne | Zásoby | Odchylka kapacit |
| Výstup (Výroby) | Odchylka | Subdodávky | Ne | Zásoby | Odchylka subdodávky |
| Výstup (Výroby) | Odchylka | Režie kapacit | Ne | Zásoby | Odchylka režie kapacity |
| Výstup (Výroby) | Odchylka | Režie výroby | Ne | Zásoby | Odchylka režie výroby |
| Výstup (Výroby) | Přecenění | Ne | Zásoby | Oprava zásob |
| Výstup (Výroby) | Zaokrouhlení | Ne | Zásoby | Oprava zásob |
| Výstup montáže | Přímé náklady | Ne | Zásoby | Oprava zásob |
| Výstup montáže | Přecenění | Ne | Zásoby | Oprava zásob |
| Výstup montáže | Nepřímé náklady | Ne | Zásoby | Vyrvonaná režie |
| Výstup montáže | Odchylka | Materiál | Ne | Zásoby | Material Variance |
| Výstup montáže | Odchylka | Kapacita | Ne | Zásoby | Odchylka kapacit |
| Výstup montáže | Odchylka | Režie kapacit | Ne | Zásoby | Odchylka režie kapacity |
| Výstup montáže | Odchylka | Režie výroby | Ne | Zásoby | Odchylka režie výroby |
| Výstup montáže | Zaokrouhlení | Ne | Zásoby | Oprava zásob |

## Z položek kapacity
Následující tabulka ukazuje vztah mezi různými typy položek ocenění kapacity, účtů a protiúčtů v hlavní knize. Položky kapacity představují pracovní dobu spotřebovou při montážních nebo výrobě.

| **Typ práce** | **Typ položky kapacity** | **Typ položky ocenení** | **Účet** | **Protiúčet** |
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
| Montáž | Zdroj | Přímé náklady | Použité přímé náklady | Oprava zásob |
| Montáž | Zdroj | Nepřímé náklady | Vyrvonaná režie | Oprava zásob |
| Výroba | Strojní centra/Pracovní centra | Přímé náklady | Účet nedokončené výroby | Použité přímé náklady |
| Výroba | Strojní centra/Pracovní centra | Nepřímé náklady | Účet nedokončené výroby | Vyrvonaná režie |

## Náklady na montáž jsou vždy skutečné
Jak je uvedeno ve výše uvedené tabulce, účtování montáže není v průběžných účtech reprezentováno. Důvodem je, že koncept nedokončené výroby (NV) se na účtování výstupu montáže nevztahuje, na rozdíl od účtování výstupu výroby. Náklady na motnáž jsou zaúčtovány pouze jako skutečné náklady, nikdy jako očekávané náklady.

Pro více informací navštivte [Detaily návrhu: Účtování montážní zakázky](design-details-assembly-order-posting.md).

## Výpočet částky zaúčtované do hlavní finanční knihy
Následující pole v tabulce **Položky ocenení** se používají k výpočtu částky očekávané ceny, která se zaúčtuje do hlavní knihy:

- Částka nákladů (skutečná)
- Náklady zaúčtované do Hlavní finančí knihy
- Částka nákladů (očekávaná)
- Očekávané náklady zaúčtované do hlavní knihy

Následující tabulka ukazuje, jak se částky, které mají být zaúčtované do hlavní knihy, počítají pro dva různé typy nákladů.

| Typ nákladů | Výpočet |
|---------------|-----------------|  
| Skutečné náklady | Částka nákladů (skutečná) – náklady zaúčtované do hlavní knihy |
| Očekávané náklady | Částka nákladů (očekávaná) - očekávané náklady účtované do hlavní knihy |

## Viz také
[Detaily návrhu: Zásoby a ocenění](design-details-inventory-costing.md)   
[Detaily návrhu: Účtování zásob](design-details-inventory-posting.md)   
[Detaily návrhu: Účtování očekávaných nákladů](design-details-expected-cost-posting.md)  
[Správa zásob a ocenění](finance-manage-inventory-costs.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]