---
title: "Using Common Data Service"
description: Introduction to Common Data Service and its components.
author: bholtorf

ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 06/30/2020
---

# Integrace s Common Data Service

Obchodní aplikace často používají data z více než jednoho zdroje. [!INCLUDE[d365fin](includes/cds_long_md.md)] kombinuje data do jediné sady logiky, která usnadňuje připojení dalších aplikací Dynamics 365, jako je [!INCLUDE[crm_md](includes/crm_md.md)] nebo vlastní aplikaci postavenou na [!INCLUDE[d365fin](includes/cds_long_md.md)], k [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Pro více informací navštivte [!INCLUDE[d365fin](includes/cds_long_md.md)], see [Co je Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

Následující kroky poskytují přehled kroků pro integraci [!INCLUDE[d365fin](includes/cds_long_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Tyto úkoly vyžadují roli **Správce systému** v [!INCLUDE[d365fin](includes/cds_long_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Přiřazením licence [!INCLUDE[d365fin](includes/cds_long_md.md)] do [!INCLUDE[d365fin](includes/d365fin_md.md)] uživatelům, kteří budou používat integrované aplikace.

2. Nastavení připojení do [!INCLUDE[d365fin](includes/cds_long_md.md)]. Pro více informací navštivte [¨Připojení do Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).

3. Synchronizace dat mezi aplikacemi. Pro více informací, navštivte [Synchronizace Business Central a Common Data Service](admin-synchronizing-business-central-and-sales.md).

## Začínáme s [!INCLUDE[d365fin](includes/cds_long_md.md)]
Chcete-li začít s [!INCLUDE[d365fin](includes/cds_long_md.md)] musítě mít účet Microsoft Power Apps. Pokud ještě nemáte účet aplikace Power Apps, můžete si jej zdarma získat na stránce [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) a zvolit odkaz **Začít zdarma**. Chcete-li se dozvědět více o tom, jak začít s [!INCLUDE[d365fin](includes/cds_long_md.md)], bežte na [začínáme s Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) v Microsft Learn.

## Obousměrná nebo jednosměrná synchronizace dat
V závislosti na vašich obchodních potřebách můžete nastavit integraci pro synchronizaci dat buď do nebo z jedné obchodní aplikace Dynamics 365 do druhé, nebo v obou směrech v téměř reálném čase prostřednictvím [!INCLUDE[d365fin](includes/cds_long_md.md)]. Například, pokud integrujete [!INCLUDE[d365fin](includes/d365fin_md.md)] s [!INCLUDE[crm_md](includes/crm_md.md)] přes [!INCLUDE[d365fin](includes/cds_long_md.md)], prodejce může vytvořit prodejní objednávku v [!INCLUDE[crm_md](includes/crm_md.md)] a objednávka bude synchronizována s [!INCLUDE[d365fin](includes/d365fin_md.md)]. Naopak, z  [!INCLUDE[crm_md](includes/crm_md.md)], může prodejce zobrazit informace z [!INCLUDE[d365fin](includes/d365fin_md.md)]  o dostupnosti zboží na objednávce.

## Standardní a vlastní entity
[!INCLUDE[d365fin](includes/cds_long_md.md)] bezpečně ukládá data v sadě entit, což jsou sady záznamů podobné tomu, jak tabulka ukládá data v databázi. [!INCLUDE[d365fin](includes/cds_long_md.md)] zahrnuje základní sadu standardních entit, které pokrývají typické scénáře, ale můžete také vytvořit vlastní entity specifické pro vaši organizaci. V [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete zobrazit standardní a vlastní entity, které jsou synchronizovány na stránce Mapování tabulky integrace.

## O základním integračním řešení CDS

Základní řešení integrace CDS je klíčovou součástí integrace. Řešení přidá požadované role a úrovně přístupu k uživatelským účtům pro integraci a vytvoří entity potřebné k mapování [!INCLUDE[d365fin](includes/d365fin_md.md)] společnosti k obchodní jednotce v [!INCLUDE[d365fin](includes/cds_long_md.md)].

Ve výchozím nastavení **Nastavení připojení [!INCLUDE[d365fin](includes/cds_long_md.md)]**, asistované nastavení průvodce importuje řešení. K tomu používá průvodce nastavením uživatelský účet správce, který zadáte. Tento účet musí být platným uživatelem v [!INCLUDE[d365fin](includes/cds_long_md.md)] s následující rolí zabezpečení:

* Správce systému

Pro více informací navštivte [Nastavení uživateských účtu pro integraci s [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) a [Vytvoření uživatelů v Microsoft Dynamics 365 (online) a přiřazení bezpečnostních rolí](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Účet správce se používá pouze jednou během instalace z důvodu změn konfigurace pro konfiguraci změn v Základu CDS a provádí se v  [!INCLUDE[d365fin](includes/cds_long_md.md)]. Po importu řešení již účet není potřeba. Integrace bude nadále používat uživatelský účet, který je automaticky vytvořen speciálně pro integraci.

Kromě přizpůsobení [!INCLUDE[d365fin](includes/cds_long_md.md)], řešení také vytváří následující role pro integraci v [!INCLUDE[d365fin](includes/cds_long_md.md)]:

* **Správce integrace** - Umožňuje uživatelům spravovat spojení mezi [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)]. Obvykle je toto přiřazeno pouze k automaticky vytvořenému uživatelskému účtu pro synchronizaci.
* **Uživatel integrace** - Umožňuje uživatelům přístup k synchronizovaným datům. Obvykle je to přiřazeno automaticky vytvořenému uživatelskému účtu pro synchronizaci a dalším uživatelům, kteří potřebují prohlížet nebo přistupovat k synchronizovaným datům.

Podrobnosti o každé roli, například oprávnění a úrovně přístupu, naleznete v části [Nastavení uživatelských účtů pro integraci s [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Během instalace připojení jsou vytvořena mapování integračních tabulek, která jsou potřebná k synchronizaci dat. Entity ve službě Common Data Service jsou mapovány na tabulky a pole tabulek v Business Central prostřednictvím integračních tabulek. Pro více informací navštivte [ Standardní mapování entit pro synchronizaci](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## Viz také
[Modely vlastnictví dat](admin-cds-company-concept.md)
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



