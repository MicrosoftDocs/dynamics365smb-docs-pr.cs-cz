---
title: Czech Local Functionality Check of Posting Group changing – Customer, Vendor, item, bank account
description: The following topics describe the local functionality Check of Posting Group changing – Customer, Vendor, item, bank account in the Czech version of Business Central.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Finance, Localization, CZ
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Kontrola změn účto skupin - zákazník, dodavatel, zboží, bankovní účet

Standardní funkcionalita byla doplněna o kontroly v případě požadavku na změnu účtoskupin u karet zákazníků, dodavatelů, zboží a bankovních účtů.

|Karta|Popis|
|-|-|
|Karta zákazníka|Na Kartě zákazníka změnit účto skupinu zákazníka. Pokud neexistují otevřené položky zákazníka, Účto skupinu zákazníka lze změnit. Pokud existují otevřené položky zákazníka, pak Účto skupinu zákazníka nelze  změnit.|
|Karta dodavatele| Na Kartě dodavatele změnit účto skupinu dodavatele. Pokud neexistují otevřené položky dodavatele, pak Účto skupinu dodavatele lze změnit. Pokud existují otevřené položky dodavatele, pak Účto skupinu dodavatele nelze změnit.|
|Karta zboží|Na Kartě zboží změnit účto skupinu zboží. Pokud existují otevřené položky zboží, pak Účto skupinu zboží nelze změnit. Pokud neexistují otevřené položky zboží a zároveň pokud existují nevyfakturované uzavřené položky, pak Účto skupinu zboží nelze změnit. Pokud neexistují otevřené položky zboží a zároveň neexistují nevyfakturované uzavřené položky zboží, pak lze účto skupinu změnit.|
|Karta bankovního účtu|Na Kartě bankovního účtu změnit účto skupinu bankovního účtu. Pokud je Saldo nebo Saldo (LM) nenulové, pak nelze změnit účto skupinu bankovního účtu.|
## Viz také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](../../finance.md)  
