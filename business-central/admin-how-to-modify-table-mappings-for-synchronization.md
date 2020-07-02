---
title: Modify Table Mappings for Synchronization | Microsoft Docs
description: Learn how to change the table mappings that are used when synchronizing data between Business Central and Dynamics 365 Sales.
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 10/01/2019
ms.author: bholtorf

---
# Změna mapování tabulek pro synchronizaci
Mapování tabulky integrace propojí tabulku v [!INCLUDE[d365fin](includes/d365fin_md.md)] do integrační tabulky pro entinu [!ZAHRNOUT[crm_md](includes/crm_md.md)]. Pro každou entitu v [!ZAHRNOUT[crm_md](includes/crm_md.md)], kterou chcete synchronizovat s odpovídajícími daty v [!INCLUDE[d365fin](includes/d365fin_md.md)], musí existovat odpovídající mapování tabulky integrace. Mapování integrační tabulky zahrnuje několik nastavení, která vám umožní řídit, jak budou záznamy v tabulce [!INCLUDE[d365fin](includes/d365fin_md.md)] a entitě [!INCLUDE[crm_md](includes/crm_md.md)] synchronizovány pomocí odpovídající úlohy synchronizace integrace.

## Filtrování záznamů
Pokud nechcete synchronizovat všechny záznamy pro určitou entitu v [!ZAHRNOUT[crm_md](includes/crm_md.md)] nebo tabulku v [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete nastavit filtry omezující synchronizované záznamy. Filtry nastavíte na stránce **Mapování tabulky integrace**.

#### Filtrování záznamů pro synchronizaci
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Mapování tabulky integrace** a poté vyberte související odkaz.

2. Chcete-li filtrovat záznamy [!INCLUDE[d365fin](includes/d365fin_md.md)], nastavte pole **Filtr tabulky**.

3. Chcete-li filtrovat záznamy [!INCLUDE[crm_md](includes/crm_md.md)], nastavte pole **Filtr tabulky integrace**.

## Vytváření nových záznamů
Ve výchozím nastavení budou synchronizačními úlohami synchronizovány pouze záznamy v [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. Mapování tabulek můžete nastavit tak, aby se v každém cíli vytvořily nové záznamy (například [!INCLUDE[d365fin](includes/d365fin_md.md)]) pro každý záznam ve zdroji (například [!INCLUDE[crm_md](includes/crm_md.md)]), který ještě není spojen.

Například úloha synchronizace prodeje PRODEJCI - Dynamics 365 Sales používá mapování tabulky PRODEJCI. Synchronizační úloha kopíruje data z uživatelských záznamů v [!INCLUDE[crm_md](includes/crm_md.md)] do záznamů prodejců v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pokud nastavíte mapování tabulek tak, aby se vytvářely nové záznamy, pro každého uživatele v [!INCLUDE[crm_md](includes/crm_md.md)], který ještě není spojen s prodejcem v [!INCLUDE[d365fin](includes/d365fin_md.md)], vytvoří se nový záznam prodejce v [!INCLUDE[d365fin](includes/d365fin_md.md)].

#### Vytvoření nových záznamů během synchronizace
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Mapování tabulky integrace** a poté vyberte související odkaz.

2. V seznamu položek mapování tabulky, zrušte zaškrtnutí pole **Synchronizovat  pouze spárované záznamy**.

## Použití konfiguračních šablon při mapování tabulek
K mapování tabulek můžete přiřadit šablony konfigurace, které budou použity pro nové záznamy vytvořené v [!INCLUDE[d365fin](includes/d365fin_md.md)] nebo [!INCLUDE[crm_md](includes/crm_md.md)]. Pro každé mapování tabulek můžete určit konfigurační šablonu, která se použije pro nové záznamy [!INCLUDE[d365fin](includes/d365fin_md.md)] a jinou šablonu pro použití nových záznamů [!INCLUDE[crm_md](includes/crm_md.md)].

Pokud nainstalujete výchozí nastavení synchronizace, budou po většinu času automaticky vytvořeny a použity dvě konfigurační šablony pro mapování tabulek pro [!INCLUDE[d365fin](includes/d365fin_md.md)] zákazníky a [!INCLUDE[crm_md](includes/crm_md.md)] účty: **ZÁKCRM** and **ÚČETCRM**.

- **ZÁKCRM** se používá k vytváření a synchronizaci nových zákazníků v [!INCLUDE[d365fin](includes/d365fin_md.md)] na základě účtu v [!INCLUDE[crm_md](includes/crm_md.md)].

   Tato šablona je vytvořena zkopírováním existující šablony konfigurace pro zákazníky v aplikaci. **ZÁKCRM** je vytvořeno, pouze pokud existuje konfigurační šablona a pole  **Kód měny** v šabloně je prázdné. Pokud pole v konfigurační šabloně obsahuje hodnotu, bude tato hodnota použita místo hodnoty v mapovaném poli pro účet [!INCLUDE[crm_md](includes/crm_md.md)]. Pokud například pole **Země/oblast** na účtu v [!INCLUDE[crm_md](includes/crm_md.md)] obsahuje *U.S.* a pole **Země/oblast** v konfigurační šabloně je *GB*, pak je *GB* použito jako **Země/oblast** pro zákazníka v [!INCLUDE[d365fin](includes/d365fin_md.md)].

- **ÚČETCRM** vytváří a synchronizuje nové účty v [!INCLUDE[crm_md](includes/crm_md.md)] na základě účtu v [!INCLUDE[d365fin](includes/d365fin_md.md)].

#### Určení šablon konfigurace pro mapování tabulek
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Mapování tabulky integrace** a poté vyberte související odkaz.

2. V seznamu položek mapování tabulky, v poli **Kód šablony konfigurační tabulky**, zvolte šablonu konfigurace, kterou chcete použít pro nové záznamy v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Nastavte pole **Kód  šablony  interní tabulky konfigurace** do konfigurační šablóny, ktorá sa použije pre nové záznamy v [!INCLUDE[crm_md](includes/crm_md.md)].

## Viz také
[Integrace Dynamics 365 Business Central s Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Synchronizace Business Central a Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Plánování synchronizace](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)
