---
title: Přizpůsobení Vizuálních Signálů O Aktivitě Hromádek | Microsoft Docs
description: 'Nastavte barevné označení v Hromádce, aby poskytovalo přizpůsobený vizuální signál aktivitě hromádky.'
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'personalize, customize'
ms.date: 10/01/2018
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
---
# <a name="set-up-a-colored-indicator-on-cues"></a>Nastavení barevného indikátoru hromádek
Hromádky, které se zobrazují ve Centre rolí, můžete nastavit tak, aby obsahovaly označení, které mění barvu na základě datových hodnot v Hromádce.

Označení se objeví jako barevný pruh podél horního okraje Hromádky. Poskytuje vizuální signál o stavu aktivitě Hromádky, což může naznačovat příznivé nebo nepříznivé podmínky, které uživatele vyzývají k akci. Pokud například Hromádka zobrazuje probíhající prodejní faktury, můžete nastavit označení tak, aby bylo zelené (příznivý), když je celkový počet probíhajících prodejních faktur pod 10, a červené (nepříznivý) se zobrazí, když je součet větší než 20.

Na stránce **Nastavení hromádky** nastavíte označení pro všechny Hromádky, které jsou dostupné v databázi společnosti.

Chcete-li nastavit označení, určete až dvě prahové hodnoty, které definují tři rozsahy datových hodnot (dolní, střední a vysoká), na které můžete použít jinou barvu (nebo styl).

## <a name="to-set-up-colored-indicators-on-cues"></a>Nastavení barevných označení v Hromádkách
1. V části **Aktivity** v Centru rolí zvolte **Nastavit hromádky**.  
   Zobrazí se stránka **Nastavení hromádky**. Na stránce jsou uvedené označení, které jsou aktuálně nastaveny v Hromádce.
2. Chcete-li upravit označení, upravte pole a upravte například hodnoty pro různé prahové hodnoty.  

V následující tabulce jsou uvedeny barvy, které odpovídají možnostem polí **Styl pro nízké hodnoty**, **Styl pro střední hodnoty** a **Styl pro vysoké hodnoty**.

| Možnost | Barva |
| --- | --- |
| **Žádný** |Žádná barva (stejná barva jako Hromádka)|
| **Příznivý** |Zelená |
| **Nepříznivý** |Červená |
| **Neutrální** |Žlutá |
| **Nevýznamný** |Šedá |

## <a name="see-also"></a>Viz také
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
