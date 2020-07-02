---
title: Integrating with Dynamics 365 Sales| Microsoft Docs
description: Learn how to get Dynamics 365 Business Central ready to integrate with Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf

---
# Integrace s Dynamics 365 for Sales
Role prodejce je často považována za jedno z nejvýraznějších úkolů v podnikání. Může však být užitečné, aby se prodejci mohli podívat dovnitř a zjistit, co se děje na zadním konci. Integrací [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] můžete dát svým prodejcům informace, které jim umožní prohlížet informace v [!INCLUDE[d365fin](includes/d365fin_md.md)], zatímco pracují v [!INCLUDE[crm_md](includes/crm_md.md)]. Například při přípravě prodejní nabídky by mohlo být užitečné vědět, zda máte dostatek zásob pro splnění objednávky. Pro více informací navštivte [Použití Dynamics 365 for Sales z Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Tyto kroky popisují proces integrace online verzí [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Informace o konfiguraci v místě instalace naleznete v části [Příprava Dynamics 365 for Sales pro integraci na místě](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

<!--## Software Requirements
You must have an Office 365 subscription, and both [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)] must be part of the same organization.  -->

## Přehled procesu integrace
Následující kroky poskytují přehled kroků k integraci [!INCLUDE[crm_md](includes/crm_md.md)] s [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]
> Tyto úkoly vyžadují bezpečnostní roli **Správce systému** v [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. V centru pro správu Microsoft 365 vytvořte uživatelský účet pro připojení a synchronizaci dat pomocí [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací navštivte [Nastavení užívatelských účtů pro integraci s Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

2. Přiřaďte licence pro [!INCLUDE[crm_md](includes/crm_md.md)] k uživatelům [!INCLUDE[d365fin](includes/d365fin_md.md)], kteří budou používat integrované aplikace.

3. Nastavte připojení na [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací navštivte [Nastavení připojení k Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md).

4. Volitelné: Pár [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] záznamy. Pro více informací navštivte [Ruční párování a synchronizace záznamů](admin-how-to-couple-and-synchronize-records-manually.md).

5. Synchronizace dat mezi aplikacemi. Pro více informací, navštivte [Synchronizace Business Central a Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md).

## Řešení pro integraci Business Central
Řešení umožňuje uživatelům zobrazit informace v [!INCLUDE[d365fin](includes/d365fin_md.md)] při práci v [!INCLUDE[crm_md](includes/crm_md.md)]. Například poskytuje informace o statistikách zákazníků, umožňuje uživatelům spárovat a prohlížet záznamy v [!INCLUDE[d365fin](includes/d365fin_md.md)] z [!INCLUDE[crm_md](includes/crm_md.md)] a umožňuje lidem zjistit, zda jsou produkty dostupné v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ve výchozím nastavení asistenční instalační příručky **Nastavení připojení Dynamics 365 for Sales** importuje integrační řešení [!INCLUDE[d365fin](includes/d365fin_md.md)]. Instalační příručka k tomu používá uživatelský účet správce. Tento účet musí být také platným uživatelem v [!INCLUDE[crm_md](includes/crm_md.md)] s následujícími bezpečnostními rolemi:

* Správce systému
* Modifikátor řešení

Pro více informací navštivte [Nastavení uživatelských účtů pro integraci s Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md), [Vytvoření uživatelů v Microsoft Dynamics 365 (online) a přiřazení zabezpečených rolí](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) a [Přiřazení oprávnění uživatelům a skupinám](ui-define-granular-permissions.md).

Tento účet se během instalace používá pouze jednou. Po importu řešení do [!INCLUDE[d365fin](includes/d365fin_md.md)] účet již není potřeba. Integrace bude nadále používat uživatelský účet, který byl vytvořen speciálně pro integraci.

Kromě přizpůsobení [!INCLUDE[crm_md](includes/crm_md.md)] vytváří integrační řešení [!INCLUDE[d365fin](includes/d365fin_md.md)] následující role v [!INCLUDE[crm_md](includes/crm_md.md)] pro integraci:

* **Správce integrace** - Umožňuje uživatelům spravovat připojení mezi [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. Obvykle je přiřazen k uživatelskému účtu pro synchronizaci.
* **Uživatel integrace** - Umožňuje uživatelům přístup ke synchronizovaným datům. Obvykle je přiřazen k uživatelskému účtu pro synchronizaci a všem ostatním uživatelům, kteří potřebují zobrazit nebo přistupovat k synchronizovaným datům.
* **Uživatel dostupnosti produktu** - Umožňuje uživatelům dotazovat se na dostupnost produktu v [!INCLUDE[d365fin](includes/d365fin_md.md)] z [!INCLUDE[crm_md](includes/crm_md.md)].

Podrobnosti o každé roli, například oprávnění a úrovně přístupu, naleznete v části [Nastavení uživatelských účtů pro integraci s Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

Na konci průvodce nastavením vás [!INCLUDE[d365fin](includes/d365fin_md.md)] vyzve, abyste spojili prodejní uživatele s uživateli v [!INCLUDE[crm_md](includes/crm_md.md)]. K záznamům v [!INCLUDE[crm_md](includes/crm_md.md)] je obvykle přiřazen vlastník (uživatel), a pokud neexistuje propojení mezi uživatelem v [!INCLUDE[crm_md](includes/crm_md.md)] a prodejní osobou v [!INCLUDE[d365fin](includes/d365fin_md.md)], synchronizace selže. Můžete to také provést později pomocí akce **Spárovat prodejce** na stránce **Nastavení připojení Microsoft Dynamics 365**.

## Viz také
[Nastavení uživatelských účtů pro integraci s Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Nastavení připojení k Dynamics 365 for Sales](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Synchronizace Business Central a Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Příprava Dynamics 365 for Sales pro integraci na místě](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
