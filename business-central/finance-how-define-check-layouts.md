---
title: Specify the Layout of a Check| Microsoft Docs
description: You can design and print your checks in different formats to conform with standards.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 02/20/2020
ms.author: edupont

---
# Výběr rozvržení šeku
Šeky můžete navrhnout tak, aby odpovídaly normám stanoveným místními úřady. Šeky lze vytisknout v angličtině, francouzštině nebo španělštině.

Šeky jsou určeny k tisku ve formátu pro Spojené státy i Kanadu ve formátu check-stub-check nebo ve formátu stub-stub-check.

## Výběr rozvržení šeku
1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Výběry sestav bankovního účtu** a vyberte související odkaz.
2. Na stránce **Výběr sestav - bankovní účet** v poli **Použití** vyberte **Šek**.
3. Vyberte jedno z následujících ID sestavy.

| ID Sestavy | Titulek Sestavy | Popis |
| --- | --- | --- |
| 1401 | Šek | Toto je výchozí sestava. |
| 10411 | Šek (Stub/Stub/Check) | Tato sestava je ve formátu stub/stub/check. |
| 10412 | Šek (Stub/Check/Stub) | Tato sestava je ve formátu stub/check/stub. |
| 10413 | Tři šeky na stránku | Tato sestava je určena k tisku tří šeků na každé stránce. |

Po nastavení rozvržení šeků můžete šeky vytisknout na stránce **Deník plateb**. Pro více informací navštivte [Práce s šeky](payables-how-work-checks.md)

Chcete-li změnit jedno z těchto výchozích rozvržení šeků, použijte k tomu integraci Word nebo RDLC. Pro více informací navštivte [Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md).

## Použití MICR a bezpečtnostního písma
Online verze [!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje předinstalované fonty na serverech, které mohou být použity při sestavování šeku. Následující přehled popisuje, které fonty jsou k dispozici, a obsahuje odkazy na podrobné informace od dodavatelů fontů třetích stran.

> [!Important]
> MICR a bezpečnostní fonty v Microsoft Dynamics[!INCLUDE[d365fin](includes/d365fin_md.md)] jsou licencovány v balíčku písem od IDAutomation.com, Inc. Tyto produkty mohou být používány pouze jako součást a v souvislosti s aplikací Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].

V aktualizaci 15.3 a novější jsou nainstalovány a dostupné fonty Magnetic Ink Character Recognition (MICR).. Jsou podporovány jak standardy E-13B, tak CMC-7. Kromě písem MICR jsou k dispozici speciální bezpečnostní fotny pro generování textu, jmen, částek a měnových symbolů dolaru, eura, libry a jenu, s nimiž lze po vytištění šeku těžko manipulovat.

> [!NOTE]
> Z bezpečnostních a právních důvodů nemůžete nahrát vlastní fonty do prostředí [!INCLUDE[d365fin](includes/d365fin_md.md)].

### Specifikace MICR E-13B
Následující souhrny specifikací pro fonty MICR E-13B, které mohou být užitečné při kalibraci fontů a také rozložení šeku s konkrétními tiskárnami MICR.

![MICR E-13B Specifikace](media/font_MICR_E-13B_Specifications.png "MICR E-13B Specifikace")

Úplnou specifikaci fontů MICR E-13B naleznete v dokumentaci dodavatele zde: (https://www.idautomation.com/micr-fonts/e13b/).

### Specifikace MICR CMC-7
Následující fotny CMC-7 jsou k dispozici v [!INCLUDE[d365fin](includes/d365fin_md.md)] online:

- IDAutomationCMC7
- IDAutomationCMC7n10
- IDAutomationCMC7n25
- IDAutomationCMC7n40

Následující souhrny specifikací pro fonty MICR CMC-7, které mohou být užitečné při kalibraci fontů a na  rozložení šeků s konkrétními tiskárnami MICR.

![MICR CMC-7 Specifikace](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 Specifikace")

Úplnou specifikaci fontů MICR CMC-7 naleznete v dokumentaci dodavatele zde: (http://www.idautomation.com/micr-fonts/cmc7/).

### Specifikace bezpečnostního fontu
Následující souhrny shrnují specifikace pro bezpečnostní fonty šeků, které mohou být užitečné při kalibraci fontů a na rozložení šeku s konkrétními tiskárnami MICR.

![Check Security Font Specifikace](media/font_check-security-font_Specifications.png "Check Security Font Specifikace")

Úplnou specifikaci bezpečnostních fontů naleznete v dokumentaci dodavatele zde: (https://www.idautomation.com/security-fonts/).

Fonty pro jiné účely jsou také k dispozici v [!INCLUDE[prodshort](includes/prodshort.md)]. Pro více informací navštivte [Dostupné Fonty](ui-fonts.md).

## Viz také
[Vytvoření a editace vlastních rozvržení sestav](ui-how-create-custom-report-layout.md)  
[Fonty v Business Central](ui-fonts.md)  
[Správa pohledávek](payables-manage-payables.md)  
[Odsouhlasení bankovních účtů](bank-manage-bank-accounts.md)   
[Dokončení procesů na konci období](year-how-complete-period-end-processes.md)  
[Práce s [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)  
[Obecné obchodní Funkcionality](ui-across-business-areas.md)
