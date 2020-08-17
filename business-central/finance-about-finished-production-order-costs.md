---
title: About Finished Production Order Costs | Microsoft Docs
description: Finishing the production order is an important task in completing the costing lifecycle of the item that is being produced. Final costs, including variances in a standard cost environment, actuals in a FIFO, Average, or LIFO cost environment, are calculated using the Adjust Cost - Item Entries batch job.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords:
ms.date: 04/01/2020
ms.author: sgroespe

---
# Náklady na dokončenou výrobní zakázku
Dokončení výrobní zakázky je důležitým úkolem při dokončení životního cyklu nákladů vyráběného zboží. Konečné náklady, včetně odchylek v prostředí standardních nákladů, skutečné hodnoty v nákladovém prostředí FIFO, Průměr nebo LIFO, se vypočítají pomocí dávkové úlohy **Úprava nákladů - položky zboží**, která umožňuje finanční odsouhlasení nákladů na výrobu zboží. Aby se výrobní zakázka považovala za úpravu nákladů, musí být stav nastaven na **Dokončeno**. Je proto důležité, aby se po dokončení stav výrobní zakázky změnil na **Dokončeno**.

## Příklad
V prostředí standardních nákladů, když spotřebováváte materiál k výrobě zboží, jednoduše řečeno, náklady na zboží plus práce a režie, jdou do nedokončené výroby. Při výrobě zboží se NV sníží o částku standardních nákladů na zboží. Obvykle tyto náklady nejsou nulové. Aby tyto náklady mohly být nulové, musíte spustit dávkovou úlohu **Úprava nákladů - položky zboží** s tím, že pro úpravu budou považovány pouze výrobní zakázky se stavem **Dokončeno**.

## Viz také
[Správa nákladů zásob](finance-manage-inventory-costs.md)  
[Výroba](production-manage-manufacturing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
