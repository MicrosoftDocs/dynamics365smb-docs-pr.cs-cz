---
title: Working with RDLC Layouts
description: Get an introduction to RDLC report layouts.
author: jswymer

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
---
# Práce s RDLC rozvrženími

Rozvržení RDLC jsou založeny na souborech rozvržení definice sestav klienta (typy souborů .rdl nebo .rdlc). Koncepty designu pro rozvržení RDLC jsou podobné ostatním typům rozložení. Rozvržení určuje, která pole se mají zobrazit a jak jsou uspořádána. Navrhování rozvržení RDLC je však pokročilejší než rozvržení Word a Excel.

[![Zobrazuje různé prvky rozložení RDLC.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## Požadované nástroje

Chcete-li upravit rozložení RDL, můžete použít Microsoft SQL Server Report Builder nebo Microsoft RDLC Report Designer.

- Report Builder je samostatná aplikace nainstalovaná na vášpočítač vámi nebo správcem. Společně s Business Central on-premises je Report Builder nainstalován současně s instalací Business Central Server installation. Další informace o instalaci Report Builder navštivte [Instalace Report Builder](/sql/reporting-services/install-windows/install-report-builder) v SQL Server dokumentaci.

- RDLC Report Designer je rozšíření pro Visual Studio 2017 a novější. RDLC Report Designer si můžete stáhnout a nainstalovat z [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## Vytváření a úpravy RDLC rozložení

Vytváření a úpravy RDLC rozvržení je pokročilá úloha, kterou obvykle provádějí zkušení uživatelé nebo vývojáři. Základní koncepty nejsou specifické pro rozvržení sestav Business Central. Z tohoto důvodu vás odkazujeme na následující dokumentaci:

- [Vytvoření RDL rozložení sestavy](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

   Tento článek vysvětluje, jak vytvořit rozvržení sestavy RDLC pomocí AL kódu.

- [Sestavy, části sestav a definice sestav](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

Odkazy na dokumentaci ke službě SQL Server Reporting Services pro RDL/RDLC. Tato dokumentace vysvětluje pojmy  
RDL/RDLC a jak používat nástroj Report Builder.

> [!NOTE]
> Nástroj Report Builder rozpozná pouze typ souboru .rdl file type;, not .rdlc. Soubory rozvržení exportované z Business Central jsou soubory typu .rdlc. Chcete-li upravit toto rozložení v Report Builder, přejmenujte typ souboru na .rdl

## Viz související školení na webu [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## Viz také

[Správa rozvržení sestav](ui-manage-report-layouts.md)  
[Nastavení rozvržení používaného sestavou](ui-set-report-layout.md)  
[Začínáme s vytvářením rozvržení sestav](ui-get-started-layouts.md)  
[Práace s sestavy, dávkovými úlohami, a XMLporty](ui-work-report.md)  
[Business Intelligence](bi.md)  
[Príce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Analýza dat sestavy pomcí Excelu](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]