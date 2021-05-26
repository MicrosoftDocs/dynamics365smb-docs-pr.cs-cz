---
    title: Design Details - Inventory Valuation | Microsoft Docs
    description: Inventory valuation is the determination of the cost of an inventory item.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2021
    ms.author: edupont

---
# Detaily návrhu: Hodnota zásob
Hodnota zásob je stanovení nákladů, které jsou přiřazeny skladové položce, vyjádřené následující rovnicí.

Koncové zásoby = počáteční zásoby + čisté nákupy – náklady na prodané zboží

Výpočet hodnoty zásob používá pole **Částka nákladů (skutečná)** položek ocenění pro zboží. Položky jsou klasifikovány podle typu položky, který odpovídá komponentám nákladů, přímým nákladům, nepřímým nákladům, odchylkám, přecenění a zaokrouhlování. Pro více informací navštivte [Detaily návrhu: Náklady komponent](design-details-cost-components.md).

Položky se vyrovnávají proti sobě, buď pevným vyrovnáním, nebo podle obecného předpokladu toku nákladů definovaného metodou ocenění. Jeden záznam snížení zásob lze použít na více než jeden záznam zvýšení s různými daty zaúčtování a případně různými pořizovacími náklady. Pro více informací navštivte [Detaily návrhu: Vyrovnání zboží](design-details-item-application.md). Výpočet hodnoty zásob pro dané datum je proto založen na sečtení položek kladné a záporné hodnoty.

## Sestava hodnoty zásob
Pro výpočet hodnoty zásob v sestavě **Hodnota zásob** začíná sestava výpočtem hodnoty zásob zboží k danému počátečnímu datu. Poté přidá hodnotu zvýšení zásob a odečte hodnotu snížení zásob až do daného data ukončení. Konečným výsledkem je hodnota zásob k datu ukončení. Sestava vypočítá tyto hodnoty sečtením hodnot v poli **Částka nákladů (skutečná)** v položkách ocenění, přičemž jako filtry použije data zaúčtování.

Tištěná sestava vždy zobrazuje skutečné částky, tj. náklady na položky, které byly zaúčtovány jako fakturované. Sestava také vytiskne očekávané náklady na položky, které byly zaúčtovány jako přijaté nebo odeslané, pokud vyberete pole Včetně oček.nákladů na záložce Možnosti.

> [!IMPORTANT]  
> Hodnoty v sestavě **Hodnota zásob** jsou odsouhlaseny s účtem zásob v hlavní knize, což znamená, že příslušné položky ocenění byly zaúčtovány do hlavní knihy.

> [!IMPORTANT]  
> Částky ve sloupcích sestavy **Hodnota** vycházejí z data zaúčtování transakcí pro zboží.

## Sestava Hodnota zásob vlastní výroby
Výrobní společnost musí určit hodnotu tří typů zásob:

* Zásoby surovin
* Zásoby nedokončené výroby
* Zásoby hotových výrobků

Hodnota zásob nedokončené výroby je určena následující rovnicí:

* Konečné zásoby NV = počáteční zásoby NV + výrobní náklady – náklady na vyrobené zboží

Pokud jde o nakoupené zásoby, položky ocenění poskytují základ ocenění zásob. Výpočet se provádí pomocí hodnot v poli **Částka nákladů (skutečná)** zboží a položek ocenění kapacity přidružených k výrobní zakázce.

Účelem ocenění zásob NV je určit hodnotu zboží, kterého výroba ještě nebyla k danému datu dokončena. Hodnota zásob NV je proto založena na položkách ocenění souvisejících s položkami spotřeby a kapacity. Položky spotřeby musí být k datu ocenění zcela fakturovány. Proto sestava  **Hodnota zásob vlastní výroby** zobrazuje náklady představující hodnotu zásob NV ve dvou kategoriích: spotřeba a kapacita.

## Viz také
[Detaily návrhu: Odsouhlasení s hlavní knihou](design-details-reconciliation-with-the-general-ledger.md)     
[Detaily návrhu: Přecenění](design-details-revaluation.md)     
[Detaily návrhu: Účtování prodejní zakázky](design-details-production-order-posting.md)  
[Správa nákladů zásob](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]