---
title: Couple and Synchronize Records Manually| Microsoft Docs
description: Synchronizing an integration table mapping enables data syncing in all records in a table in Business Central and Dynamics 365 Sales entity that are coupled.
services: project-madeira
documentationcenter: ''
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2020
ms.author: bholtorf

---

# Ruční párování a synchronizace záznamů
Toto téma popisuje, jak spojit jeden nebo více záznamů v [!INCLUDE[d365fin](includes/d365fin_md.md)]se záznamy ve službě Common Data Service nebo [!INCLUDE[crm_md](includes/crm_md.md)]. Záznamy párování umožňují zobrazit informace v Common Data Service z [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa. Spojení také umožňuje synchronizovat data mezi záznamy. Můžete spárovat existující záznamy nebo vytvářet a spárovat nové záznamy.

> [!Note]
> Spojování a synchronizace dat je k dispozici, pouze pokud správce systému vytvořil spojení mezi [!INCLUDE[d365fin](includes/d365fin_md.md)] a Common Data Service nebo [!INCLUDE[crm_md](includes/crm_md.md)]. Rychlý způsob, jak zkontrolovat, je otevřít kartu **Zákazník** a vyhledat akci **Nastavení párování**. Pokud je akce k dispozici, aplikace jsou připojené.

## Video příklad

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## Párování záznamů
1. In [!INCLUDE[d365fin](includes/d365fin_md.md)], otevřete kartu pro záznam, který chcete párovat. Například, karta zákazníka nebo kontaktu.

   Můžete také otevřít stránku se seznamem a vybrat záznam, který chcete spárovat.

2. Zvolte akci **Nastavení párování**.
3. Vyplňte pole a vyberte tlačítko **OK**.

## Synchronizace jednoho záznamu
1. In [!INCLUDE[d365fin](includes/d365fin_md.md)], otevřete kartu pro záznam, který chcete párovat. Například, karta zákazníka nebo kontaktu.
2. Vyberte akci **Synchronizovat nyní**.
3. Pokud lze záznam synchronizovat jedním směrem, vyberte možnost, která určuje směr aktualizace dat, a poté zvolte **OK**.

## Synchronizace jednoho záznamu z [!INCLUDE[crm_md](includes/crm_md.md)]
1. V [!INCLUDE[crm_md](includes/crm_md.md)], otevřete formulář pro záznam, který chcete sprárovat. Například, karta účtu nebo karta kontaktu.
2. Vyberte akci **[!INCLUDE[d365fin](includes/d365fin_md.md)]** v pásu karet k otevření a párovaného záznam automaticky.

> [!Note]
> Jeden záznam můžete synchronizovat z [!INCLUDE[crm_md](includes/crm_md.md)] automaticky pouze tehdy, když **Synchronizovat  pouze spárované záznamy** je vypnut a směr synchronizace je nastaven na obousměrnou nebo z tabulky integrace na  stránku **Mapování tabulky integrace**. Pro více informací navštivte [Úprava mapování tabulek pro synchronizaci](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).

## Synchronizace více záznamů
1. V [!INCLUDE[d365fin](includes/d365fin_md.md)], otevřete stránku se položkami záznamu, například stránky Zákazníci nebo Kontakty.
2. Vyberte záznamy, které chcete synchronizovat, a poté vyberte akci **Synchronizovat nyní**.
3. Pokud lze záznamy synchronizovat v jednom směru, vyberte možnost, která určuje směr, a pak zvolte **OK**.

## Viz také
[Používání Dynamics 365 Sales from Business Central](marketing-integrate-dynamicscrm.md)
