---
title: Introduction to Business Central and Power BI| Microsoft Docs
description: Getting insight, business intelligence, and KPIs from your Business Central data is easy with the Business Central apps for Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer

---
# [!INCLUDE[prod_short](includes/prod_short.md)] a Power BI

Získání přehledu o vašich datech [!INCLUDE[prod_short](includes/prod_short.md)] je snadné pomocí [Power BI](https://powerbi.microsoft.com) - systému vizualizace dat od společnosti Microsoft. Power BI načte data [!INCLUDE[prod_short](includes/prod_short.md)], která vám umožní vytvářet řídicí panely a sestavy na základě těchto dat. Power BI poskytuje flexibilní alternativu k sestavám zabudované v [!INCLUDE[prod_short](includes/prod_short.md)], což vám umožní přejít k podrobnostem a přizpůsobit vizualizaci a dokonce sloučit data z různých společností v [!INCLUDE[prod_short](includes/prod_short.md)]. Některé sestavy Power BI lze také vložit do Business Central a zobrazit bez opuštění systému. Složitější řídicí panely je lépe spouštět z webu Power BI.

![Power BI a Business Central](media/power-bi-intro.png)


## Co můžete dělat s Power BI a [!INCLUDE[prod_short](includes/prod_short.md)]

Existují různé funkce pro práci s [!INCLUDE[prod_short](includes/prod_short.md)] a Power BI. Některé věci můžete dělat z Power BI, zatímco jiné se dělají z [!INCLUDE[prod_short](includes/prod_short.md)]. Některé funkce jsou k dispozici pouze s [!INCLUDE[prod_short](includes/prod_short.md)] online, nikoli on-premises. V následující tabulce je uveden přehled.

| Funkce | Popis | Online | On-premises | Více informací |
|-------|-----------|--------------|-----------|----------------|
| Zobrazit data [!INCLUDE[prod_short](includes/prod_short.md)] v Power BI | Data si můžete prohlédnout z [!INCLUDE[prod_short](includes/prod_short.md)] v sestavách v Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online zahrnuje některé předdefinované sestavy Power BI. Nebo vám vaše organizace zpřístupní některé vlastní sestavy. | ![Funguje online](media/check.png) | ![Funguje v on-premises prostředí](media/check.png) | [Viz...](across-working-with-business-central-in-powerbi.md) |
| Zobrazit sestavy Power BI v klientovi [!INCLUDE[prod_short](includes/prod_short.md)]. | Sestavy Power BI, které zobrazují data [!INCLUDE[prod_short](includes/prod_short.md)], mohou být vloženy přímo do částí stránek [!INCLUDE[prod_short](includes/prod_short.md)]. Přepnutím součásti zobrazíte libovolnou sestavu, která je vám k dispozici. | ![Funguje online](media/check.png) | ![Funguje v on-premises prostředí](media/check.png)<sup>[*](#onprem)</sup> | [Viz...](across-working-with-powerbi.md). |
| Vytvářet sestavy a řídicí panely v Power BI, které zobrazují [!INCLUDE[prod_short](includes/prod_short.md)]. | Pomocí Power BI Desktop můžete vytvářet vlastní sestavy a řídicí panely. Sestavy můžete publikovat do své vlastní služby Power BI nebo je sdílet s ostatními ve vaší organizaci. | ![Funguje online](media/check.png) | ![Funguje v on-premises prostředí](media/check.png) | [Viz...](across-how-use-financials-data-source-powerbi.md) |
| [!INCLUDE[prod_short](includes/prod_short.md)] aplikace v Power BI | [!INCLUDE[prod_short](includes/prod_short.md)] publikuje tři aplikace pro Power BI na Microsoft AppSource. Tyto aplikace vytvářejí podrobné sestavy a řídicí panely ve službě Power BI pro prohlížení dat [!INCLUDE[prod_short](includes/prod_short.md)]. Mezi dostupné aplikace patří: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul> | ![Funguje online](media/check.png) | [Viz...](across-powerbi-business-central-apps.md) |

<a name="onprem"><sup>*</sup></a> Tato funkce vyžaduje registrovanou aplikaci pro Business Central v Microsoft Azure. Pro více informací navštivte [Registrace Business Central On-Premises ve službě Azure AD pro integraci s jinými službami](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

## Připravte se na používání Power BI

Než začnete používat Power BI s [!INCLUDE[prod_short](includes/prod_short.md)], je třeba provést několik úkolů. Některé úlohy obvykle provádí pouze správci nebo speciální uživatelé.

1. Pokud používáte [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, ujistěte se, že vaše nasazení splňuje požadavky uvedené v [Nastavení [!INCLUDE[prod_short](includes/prod_short.md)] on-premises pro integraci Power BI](admin-powerbi-setup.md#setup). Tento úkol je obvykle administrativní.

2. Publikujte data jako webové služby.

   Codeunits, stránky a dotazy, které chcete použít jako zdroj dat v sestavách Power BI, musí být publikovány jako webové služby. Ve výchozím nastavení je publikováno mnoho webových služeb. Snadný způsob, jak najít webové služby, je vyhledat *webové služby* v [!INCLUDE[prod_short](includes/prod_short.md)].

   Pro více informací o publikování webových služeb navštivte [Publikování webové služby](across-how-publish-web-service.md).

3. Získejte účet Power BI.

   Chcete-li s Power BI a [!INCLUDE[prod_short](includes/prod_short.md)] dělat cokoli, ať už jste administrátor nebo jen běžný uživatel, budete potřebovat účet služby Power BI. Účet získáte na [https://powerbi.microsoft.com](https://powerbi.microsoft.com). K přihlášení k účtu použijte svou pracovní e-mailovou adresu a heslo. Registrace vyžaduje, abyste měli licenci, ale ve většině případů byste již měli mít licenci zdarma. Pro více informací navštivte [Licencování Power BI](admin-powerbi-setup.md#license).

4. Pokud chcete vytvořit vlastní sestavy Power BI, získejte Power BI Desktop.

   Můžete si stáhnout [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Pro více informací navštivte [Získat Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

## Zobrazit související školení na webu [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Viz také

[Power BI pro uživatelé](/power-bi/consumer/end-user-consumer)    
[„Nový vzhled“ služby Power BI](/power-bi/service-new-look)    
[Rychlý start: Připojení k datům v Power BI Desktopu](/power-bi/desktop-quickstart-connect-to-data)    
[Dokumentace Power BI](/power-bi/)    
[Business Intelligence](bi.md)    
[Začínáme](product-get-started.md)    
[Import obchodních dat z jiných finančních systémů](across-import-data-configuration-packages.md)    
[Nastavení [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] jako zdroje dat Power BI](across-how-use-financials-data-source-powerbi.md)    
[Použití [! INCLUDE[prod_short](includes/prod_short.md)] jako zdroje dat Power Apps](napříč- jak- použít-finanční-data-zdroj-powerapps.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] v Power Automate](across-how-use-financials-data-source-flow.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]