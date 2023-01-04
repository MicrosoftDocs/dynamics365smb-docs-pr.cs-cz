---
title: Power BI Integration Component and Architecture Overview for Business Central| Microsoft Docs
description: Learn about the different aspects of Power BI integration with Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer

---
# Integrace komponent Power BI a přehledu architertur pro [!INCLUDE[prod_short](includes/prod_short.md)]

V tomto článku se dozvíte o různých aspektech integrace Power BI s [!INCLUDE[prod_short](includes/prod_short.md)], čo vám pomůže pochopit jeho implementaci a použití.

## Komponenty

Následující tabulka popisuje hlavní komponenty, které jsou součástí integrace Power BI.

| Komponenta | Popis |
|---------|-----------|
| Power BI | Cloudová služba pro hostování a správu sestav. |
| Power BI Desktop | Vývojový nástroj pro vytváření sestav a řídicích panelů, který umožňuje spouštět sestavy. Je k dispozici ke stažení zdarma v Microsoft Store a je nainstalován lokálně. |
| [!INCLUDE[prod_short](includes/prod_short.md)] | Online nebo lokální řešení s konektory vystavenými Power BI a možností vložit část Power BI. |

## Co je k dispozici od začátku

Následující tabulka popisuje dostupné funkce.

| Funkce | Podpora [!INCLUDE[prod_short](includes/prod_short.md)] online nebo on-premises |
|-------|---------------------|
| Konektory Power BI | Oba Různé konektory pro online a on-premises. Stejný konektor používaný pro Power BI Desktop a Power BI Service |
| Vložené prostředí pro zobrazení dané sestavy uvnitř okna s faktami v [!INCLUDE[prod_short](includes/prod_short.md)] | Oba Vyžaduje konfiguraci pro zobrazení sestav pro prostředí on-premises. |
| Správa sestav Power BI od [!INCLUDE[prod_short](includes/prod_short.md)] | Online |
| Výchozí sestavy Power BI o centrech rolí nasazených do Power BI | Online |
| Aplikace Power BI na Microsoft AppSource | Online |

## Architektura

[!INCLUDE[prod_short](includes/prod_short.md)] se integruje s Power BI prostřednictvím konektoru pomocí OData. Zdroj dat pro sestavy Power BI je vystaven jako stránky API a webové služby OData.

![Architektura Power BI pro integraci s Business Central.](./media/power-bi-architecture.png)

## Obecný tok

Následující diagram znázorňuje základní workflow pro uživatele při připojování [!INCLUDE[prod_short](includes/prod_short.md)] do Power BI.

![Workflow Power BI pro integraci s Business Central.](./media/power-bi-flow.png)

1. Uživatel se zaregistruje k účtu Power BI.
2. Uživatel se připojuje k Power BI z [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] ověřuje licenci.
4. [!INCLUDE[prod_short](includes/prod_short.md)] nasadí výchozí sestavy do služby Power BI. Tento krok se děje pouze pro [!INCLUDE[prod_short](includes/prod_short.md)] online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] zpřístupní sestavy v Power BI pro výběr v [!INCLUDE[prod_short](includes/prod_short.md)]. Výchozí sestavy se automaticky zobrazují v částech Power BI.
6. Uživatel vytvoří sestavu v Power BI Desktop.
7. Uživatel publikuje sestavu do služby Power BI. Sestavy jsou pak k dispozici pro výběr v [!INCLUDE[prod_short](includes/prod_short.md)].

## Zobrazit související školení na webu [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Viz také

[Business Central a Power BI](admin-powerbi.md)    
[Power BI pro uživatelé](/power-bi/consumer/end-user-consumer)    
[„Nový vzhled“ služby Power BI](/power-bi/service-new-look)    
[Rychlý start: Připojení k datům v Power BI Desktopu](/power-bi/desktop-quickstart-connect-to-data)    
[Dokumentace Power BI](/power-bi/)    
[Business Intelligence](bi.md)    
[Připravte se na podnikání](ui-get-ready-business.md)    
[Import obchodních dat z jiných finančních systémů](across-import-data-configuration-packages.md)    
[Nastavení [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] jako zdroje dat Power BI](across-how-use-financials-data-source-powerbi.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] jako zdroje dat Power Apps](across-how-use-financials-data-source-powerapps.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] v Power Automate](across-how-use-financials-data-source-flow.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]