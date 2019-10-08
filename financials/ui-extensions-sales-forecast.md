---
title: Použití rozšíření Sales and Inventory Forecast ke správě zásob | Microsoft Docs
description: 'Toto rozšíření vám pomůže předpovědět prodej, získat jasný přehled o očekávaném nedostatku zásob a dokonce vám pomůže vytvořit požadavky na doplnění prodejcům.'
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'app, add-in, manifest, customize, budget'
ms.date: 03/29/2017
ms.author: edupont
---
# <a name="sales-and-inventory-forecast-for-business-central"></a>Prognóza prodejů a zásob pro Business Central 
Řízení zásob je kompromisem mezi službami zákazníkům a správou vašich nákladů. Na jedné straně malé zásoby vyžadují méně pracovního kapitálu, na druhé straně však nedostatek zásob může vést ke ztrátě prodejů. Rozšíření Sales and Inventory Forecast předpovídá potenciální prodeje použitím historických dat a poskytuje jasný přehled o očekávaném nedostatku zásob. Na základě prognózy rozšíření pomáhá vytvářet žádosti o doplnění vašim dodavatelům a šetří váš čas.  

## <a name="setting-up-forecasting"></a>Nastavení prognózy
V [!INCLUDE [d365fin](includes/d365fin_md.md)], je připojení ke [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) již nastaveno. Prognózu však můžete nakonfigurovat tak, aby používala jiný typ období, ve kterém se bude vykazovat, jako je například změna z prognózy podle měsíce na prognózu podle čtvrtletí. Můžete také zvolit počet období, ve kterých chcete počítat prognózu, v závislosti na tom, jak podrobnou prognózu chcete. Doporučujeme, abyste předpovídali po měsíci s 12 měsíčním horizontem pro prognózu.  

## <a name="using-the-forecasts"></a>Používání prognóz
Rozšíření používá Cortana Intelligence k předpovídání budoucích prodejů na základě vaší prodejní historie, což vám pomůže vyhnout se nedostatku zásob. Pokud například vyberete zboží na okně **Zboží**, graf v podokně **Prognóza zboží** zobrazuje odhadované prodeje tohoto zboží v nadcházejícím období. Tímto způsobem můžete zjistit, zda je pravděpodobně, že brzy dojdou zásoby daného zboží.  

Pomocí rozšíření můžete také navrhnout, kdy se mají doplnit zásoby na skladě. Pokud například vytvoříte nákupní objednávku pro Fabrikam, protože si chcete koupit jejich novou stolní židli, rozšíření Sales and Inventory Forecast navrhne, abyste také doplnili zásoby otočné židle LONDON, kterou obvykle kupujete u tohoto prodejce. Důvodem je, že rozšíření předpovídá, že v nadcházejících dvou měsících vám dojdou zásoby otočného křesla LONDON, takže je možné, že budete chtít objednat více židlí už teď najednou.  

## <a name="see-also"></a>Viz také
[Prodej](sales-manage-sales.md)  
[Zásoby](inventory-manage-inventory.md)  
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] pomocí rozšíření](ui-extensions.md)  
