---
title: Porozumění typům zboží | Microsoft Docs
description: 'Ocenění zboží můžete upravit pomocí metod FIFO nebo průměrné kalkulace, například když se náklady zboží změní z jiných důvodů, než jsou transakce.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/18/2018
ms.author: sgroespe
---
# <a name="about-item-types"></a>O typech zboží
V poli **Typ** na stránce **Karta zboží** můžete vybrat, pro co je zboží ve vaší firmě použito a jak je v systému spravováno.  Existují tři možnosti:

|Možnost|Typický účel|
|------|-----------|
|Zásoby|Fyzická jednotka, například kolo, pro plnou podporu podnikání.|
|Neskladované|Fyzická jednotka, například šroub, pro omezenou podporu podnikání, například proto, že se položka používá pouze interně a má nízké náklady.|
|Služba|Jednotka pracovní doby, například poradenská hodina, pro omezenou podporu podnikání.|

Typ **Zboží** zahrnuje úplné sledování množství a hodnoty zásob. Proto jsou podporovány všechny typy transakcí zboží a zboží typu Zásoby lze použít se všemi funkcemi zpracování zboží.

Typy **Služba** a **Neskladované** nezahrnují sledování množství a hodnoty zásob. Proto jsou podporovány pouze vybrané typy a funkce transakcí zboží.

Tři typy zboží podporují následující funkce.

|Typ zboží|Prodej|Nakupování|Spotřeba práce|Spotřeba servisu|Spotřeba montáže|Spotřeba výroby|Výstup montáže|Výstup výroby|Lokace transferu|Fyzické počítání|Přecenění zásob|Zásoby a ocenění|Sledování zboží|Rezervace|Skladování|Plánování|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Zásoby|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|
|Neskladované|Ano|Ano|Ano|Ano|Ano|Ano|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|
|Služba|Ano|Ano|Ano|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|

> [!NOTE]
> Zboží, které nabízíte svým zákazníkům, ale nechcete ve svém systému spravovat, dokud je nezačnete prodávat, lze nastavit jako zboží v katalogu. Zboží v katalogu se nesmí zaměňovat s běžným zbožím typu Neskladované. Pro více informací navštivte [Práce s katalogovým zbožím](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Zboží zákazníků, na kterých provádíte servis, například tiskárna, se nazývá předmět servisu. Předmět servisu nemá nic společné s běžným zbožím nebo zbožím v katalogu. Komponenty služeb však mohou být běžným zbožím. Pro více informací navštivte [Nastavení Předmětů servisu a Komponent předmětu servisu](service-how-setup-service-items.md).

## <a name="see-also"></a>Viz také
[Zaevidujte nové zboží](inventory-how-register-new-items.md)  
[Nastavení zásob](inventory-setup-inventory.md)  
[Správa nákladů zásob](finance-manage-inventory-costs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
