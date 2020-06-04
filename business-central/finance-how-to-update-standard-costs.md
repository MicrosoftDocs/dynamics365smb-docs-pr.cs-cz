---
title: How to Update Standard Costs | Microsoft Docs
description: You must periodically update the standard costs of components and roll the new costs up to the parent item.
services: project-madeira
documentationcenter: ''
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
# Aktualizace standardních nákladů
Musíte pravidelně aktualizovat standardní náklady na součásti a nové náklady rozdělovat až k nadřazenému zboží. Proces se obvykle skládá z následujících čtyř kroků:

1. Aktualizace nákladů na úrovni komponenty a kapacity. Pro více informací navštivte dávkovou úlohu **Navrhnout pevnou cenu zboží**.
2. Konsolidace a rozbalení nákladů na komponenty a kapacitu a výpočet celkových výrobních nebo montážních nákladů na zboží.
3. Implementace standardních nákladů zadaných při spuštění předchozích dávkových úloh. Pevná pořizovací cena se projeví až po jejich zavedení. Pro více informací navštivte Implementace změn standardních nákladů.
4. Proveďte změny a aktualizujte pole **Pořizovací cena** na kartě zboží a proveďte přecenění skladu. Pro více informací navštivte [Přeceňování zásob](inventory-how-revalue-inventory.md).

Pro více informací navštivte [Výpočet pevné požizovací ceny](finance-about-calculating-standard-cost.md).
## Aktualizace standardních nákladů
1. Spusťte dávkovou úlohu **Adjustace nákladů položek zboží**.
2. Spusťte dávkovou úlohu **Účtování nákladů na zboží**.
3. Otevřete **Sešit pevné ceny** a použijte jednu nebo více z následujících funkcí:

   1. Spusťte dávkovou úlohu **Navrhnout pevnou cenu zboží**.
   2. Zkontrolujte výsledky a podle potřeby proveďte změny.
   3. Spusťte dávkovou úlohu **Navrhnout pevnou pořizovací cenu kapacity**.
   4. Zkontrolujte výsledky a podle potřeby proveďte změny.
   5. Spusťte dávkovou úlohu **Pevná cena více úrovní**.
   6. Zkontrolujte výsledky a podle potřeby proveďte změny.
   7. Spusťte dávkovou úlohu **Provést změny pevné ceny**.
4. Zkontrolujte a zaúčtujte stránku **Deník přecenění**, která byla naplněna položkami z předchozích kroků v tomto procesu.

## Viz také
[Výpočet standardních nákladů](finance-about-calculating-standard-cost.md)  
[Správa nákladů zásob](finance-manage-inventory-costs.md)  
[Detaily návrhu: Metody ocenění](design-details-costing-methods.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
