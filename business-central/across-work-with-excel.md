---
title: Prohlížení a úpravy v Excelu z Business Central | Microsoft Docs
description: Zjistěte, jak můžete otevřít stránky v aplikaci Microsoft Excel z aplikace Business Central pro lepší analýzu dat.
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 01/14/2020
ms.reviewer: v-zdbice
ms.author: jswymer

---
# Prohlížení a úpravy v Excelu z Business Central

U stránek, které zobrazují seznam záznamů v řádcích a sloupcích, například seznam zákazníků, prodejních objednávek nebo faktur, můžete tyto záznamy zobrazit také pomocí aplikace Microsoft Excel. K tomu máte dvě možnosti. Na stránce můžete vybrat akci **Otevřít v Excelu** nebo **Upravit v Excelu**. Rozdíly mezi těmito dvěma akcemi jsou následující:

## Otevřít v Excelu

- Při této akci Excel respektuje všechny filtry na stránce, které omezují zobrazené záznamy. To znamená, že sešit aplikace Excel bude obsahovat stejné řádky a sloupce, které se zobrazují na stránce v [!INCLUDE[prodshort](includes/prodshort.md)].

- Můžete provádět změny záznamů v Excelu, ale nemůžete publikovat změny zpět do [!INCLUDE[prodshort](includes/prodshort.md)]. Změny můžete uložit pouze do souboru Excel v počítači.

- Tato akce funguje ve Windows i MacOS.

> [!NOTE]
> Pro [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, ve výchozím nastavení je k dispozici akce **Otevřít v Excelu**. Pokud však nastavíte [!INCLUDE[prodshort](includes/prodshort.md)] on-premises pro úpravy dat v Excelu, akce **Otevřít v Excelu** je nahrazena akcí **Upravit v Excelu**.

## Upravit v Excelu

- Při této akci aplikace Excel respektuje většinu filtrů na stránce, které omezují zobrazené záznamy. To znamená, že sešit aplikace Excel bude obsahovat téměř stejné záznamy a sloupce.

- Výhodou akce **Upravit v Excelu** je, že umožňuje provádět změny v záznamech v Excelu a poté je publikovat zpět do [!INCLUDE[prodshort](includes/prodshort.md)].

- Funguje to pouze ve Windows, ne v MacOS.

Toto bylo vylepšeno ve vydání 2019 wave 2. Další informace viz [Vylepšení integrace Excelu](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).

> [!NOTE]
> Pro [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, je akce **Upravit v Excelu** k dispozici pouze v případě, Váš správce že nakonfiguroval doplněk Excel (Excel AddIn). Pokud se chcete dozvědět, jak nainstalovat doplněk Excel, přečtěte si část [Nastavení doplňku Excel pro úpravy dat Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).

> [!NOTE]
> Pro [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, tato funkce je k dispozici pouze pro webového klienta.

### Podívejte se na rozdíly mezi oběma akcemi

<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## Viz také

[Práce s [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  