---
title: Viewing and Editing in Excel From Business Central | Microsoft Docs
description: Learn about how you can open the pages in Microsoft Excel from Business Central for better data analysis.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2019
ms.author: jswymer

---
# Zobrazení a úpravy v aplikaci Excel

U stránek, které zobrazují seznam záznamů v řádcích a sloupcích, například seznam zákazníků, prodejních objednávek nebo faktur, můžete tyto záznamy zobrazit také pomocí aplikace Microsoft Excel. Máte k tomu dvě možnosti. Na stránce můžete vybrat akci **Otevřít v Excelu** nebo **Upravit v Excelu**. Rozdíly mezi těmito dvěma akcemi jsou následující:

## Otevřít v aplikaci Excel

- Pomocí této akce aplikace Excel respektuje všechny filtry na stránce, které omezují zobrazené záznamy. To znamená, že sešit aplikace Excel bude obsahovat stejné řádky a sloupcy, které se zobrazují na stránce v [!INCLUDE[prodshort](includes/prodshort.md)].

- Můžete provádět změny záznamů v aplikaci Excel, ale nemůžete publikovat změny zpět do aplikace [!INCLUDE[prodshort](includes/prodshort.md)]. Změny lze uložit pouze do souboru aplikace Excel v počítači.

- Tato akce funguje na Windows i MacOS.

> [!NOTE]
> Pro [!INCLUDE[prodshort](includes/prodshort.md)] on-premis, akce **Otevřit v aplikace Excel** není dostupná, pokud akce **Upravit v aplikaci Excel** dostupná.

## Úprava v aplikaci Excel

- Pomocí této akce nebude sešit aplikace Excel respektovat filtry na stránce, které omezují zobrazené záznamy. To znamená, že sešit aplikace Excel bude obsahovat všechny dostupné záznamy a sloupce bez ohledu na to, co je na stránce zobrazeno.

- Výhodou akce **Upravit v aplikaci Excel** je, že umožňuje provádět změny záznamů v aplikaci Excel a poté tyto změny publikovat zpět do aplikace [!INCLUDE[prodshort](includes/prodshort.md)].

- Funguje to pouze na Windows, ne na MacOS.

> [!NOTE]
> Pro [!INCLUDE[prodshort](includes/prodshort.md)] on-premis, akce **upravit v aplikaci Excel** je dostupná, pokud add-in Excel byl nainstalován vaším správcem. Chcete-li získat informace o instalaci doplňku aplikace Excel, přečtěte si informace v tématu [Nastavení doplňku aplikace Excel](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) .

### Podívejte se na rozdíly mezi možnostmi
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## Viz také
[Práce s Business Central](ui-work-product.md)
