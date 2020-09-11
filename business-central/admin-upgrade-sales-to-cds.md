---
title: Upgrading an Integration with Dynamics 365 Sales| Microsoft Docs
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
# Aktualizace integrace s Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] integruje s [!INCLUDE[d365fin](includes/cds_long_md.md)],který usnadňuje připojení a synchronizaci dat s jinými aplikacemi Dynamics 365, například [!INCLUDE[crm_md](includes/crm_md.md)], nebo dokonce aplikace, které si sami vytvoříte. Pokud se integrujete poprvé, doporučujeme, abyste tak učinili prostřednictvím [!INCLUDE[d365fin](includes/cds_long_md.md)]. Pro více informací navštivte [Integrace s Common Data Service](admin-common-data-service.md).

Pokud jste již integrovali [!INCLUDE[crm_md](includes/crm_md.md)] s [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete pokračovat v synchronizaci dat pomocí nastavení. Nicméně, pokud upgradujete [!INCLUDE[d365fin](includes/d365fin_md.md)], nebo vypínáte vaší integraci [!INCLUDE[crm_md](includes/crm_md.md)] musíte se znovu připojit pomocí [!INCLUDE[d365fin](includes/cds_long_md.md)].

> [!NOTE]
> Při opětovném připojení pomocí [!INCLUDE[d365fin](includes/cds_long_md.md)] se použijí výchozí nastavení synchronizace a přepíší všechny konfigurace, které máte. Například, bude aplikována tabulka výchozího mappování.

## Aktualizace vašeho připojení do Common Data Service
1. Otevřete stránku **Nastavení připojení k Microsoft Dynamics 365**, vyberte **Povoleno** k vypnutí stávajícího připojení do [!INCLUDE[crm_md](includes/crm_md.md)].
2. Otebřete stránku  **Nastavení připojení Common Data Service**, a vyberte **Povoleno** k vypnutí připojení.

   Po tom co povolíte připojení CDS, the Business Central CDS Základní řešení integrace bude nasazeno do Common Data Service.
3. Odinstalace řešení Microsoft Dynamics 365 Business Central Integration z aplikace Dynamics 365 Sales následujte [téma Odinstalování nebo odebrání řešení](/powerapps/developer/common-data-service/uninstall-delete-solution)

4. Na stránce Nastavení připojení k Microsoft Dynamics 365, zvolte přepínač Povolit a zapněte připojení [!INCLUDE[crm_md](includes/crm_md.md)].

   Po tom co povolíte připojení do Sales, the Business Central Integration Solution je nasazeno do Sales. To umožňuje integraci s entitami, které jsou specifické pro [!INCLUDE[crm_md](includes/crm_md.md)], například prodejní objednávky, nabídky a faktury.
5. Vyberte **Řešení opěovné integrace** pro instalaci a konfiguraci upgradovaného řešení integrace Business Central Integration Solution.
6. Na stránce **Nastavení připojení Sales** zvolte **Použít výchozí nastavení synchronizace** k inicializaci mapování tabulky integrace v [!INCLUDE[crm_md](includes/crm_md.md)].

## Viz také
[Integrace s Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integrace s Common Data Service](admin-common-data-service.md)
