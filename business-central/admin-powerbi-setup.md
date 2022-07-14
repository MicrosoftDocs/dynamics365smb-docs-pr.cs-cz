---
title: Enabling Power BI Integration With Business Central
description: Learn how to set up the connection to Power BI. With Power BI reports, you can get insights, business intelligence, and KPIs from your Business Central data.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, setup, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
---
# Povolení integrace Power BI s [!INCLUDE[prod_short](includes/prod_short.md)]

Tento článek popisuje, jak získat [!INCLUDE[prod_short](includes/prod_short.md)] připraven k integraci s Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online je již povolen pro integraci, i když existují některé informace o licencování, které byste si mohli chtít přečíst. Pro [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, budete mít nastavené prostředí pro připojení k Power BI, než s ním budou uživatelé moci pracovat.

## <a name="license"></a>Licencování Power BI

S [!INCLUDE[prod_short](includes/prod_short.md)], uživatelé získají bezplatnou licenci Power BI, která poskytuje přístup k nejběžnějším funkcím v [!INCLUDE[prod_short](includes/prod_short.md)] a Power BI. Můžete si také zakoupit licenci Power BI Pro, která poskytuje přístup k dalším funkcím. Následující tabulka obsahuje přehled funkcí dostupných s každou licencí.

|Licence pro spuštění|Zobrazení sestav|Vytváření sestav|Sdílení sestav|Aktualizace sestav| Aplikace [!INCLUDE[prod_short](includes/prod_short.md)]|
|-------------|--------||
|Power BI zdarma|![zaškrtnutí.](media/check.png)|![další zaškrtnutí](media/check.png)|(limitované)|(limitované)||
|Power BI Pro|![ještě další zaškrtnutí.](media/check.png)|![je to zaškrtnuté](media/check.png)|![opět zaškrtnutí](media/check.png)|(rozsáhlý)|![poslední zaškrtnutí](media/check.png)|

Pro více informací navštivte [Licencování služby Power BI pro uživatele ve vaší organizaci](/power-bi/admin/service-admin-licensing-organization) nebo [Registrace ke službě Power BI jako jednotlivci](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="exposedata"></a>Vystavení dat prostřednictvím stránek rozhraní API nebo webových služeb OData

Business Central nabízí dva způsoby přístupu k datům, která lze zpracovávat sestavami Power BI: stránky API a webové služby Open Data Protocol (OData).

### Stránky rozhraní API

> **PLATÍ PRO:** pouze Business Central online

Stránka API je specifický typ stránky vytvořený v kódu AL, který poskytuje přístup k databázovým tabulkám prostřednictvím služby REST, podporou webhooku a s podporou OData v4. Tento typ stránky nelze zobrazit v uživatelském rozhraní, ale je určen pro vytváření spolehlivých integračních služeb.

Business Central online je k dispozici se sadou vestavěných rozhraní API, která můžete použít k získání dat pro nejběžnější obchodní subjekty, jako jsou zákazníci, zboží, prodejní objednávky a další. K použití těchto rozhraní API jako zdroje dat pro sestavy Power BI není potřeba žádná další práce ani nastavení. Pro více informací o těchto rozhraních API navštivte [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online také podporuje vlastní rozhraní API. Vývojáři aplikací řešení Business Central mohou vytvářet vlastní stránky API a balit je do rozšíření. Rozšíření můžete nainstalovat do svého tenanta. Po instalaci můžete pro sestavy Power BI použít stránky rozhraní API, jako byste to udělali s integrovanými rozhraními API (v2.0). Pro více informací o tom, jak vytvořit stránky rozhraní API navštivte [Vývoj vlastního rozhraní API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

### Webové služby OData

Objekty aplikace Business Central, jako jsou codeunits, stránky a dotazy, můžete publikovat jako [Webové služby OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). S Business Central online existuje ve výchozím nastavení mnoho webových služeb. Snadný způsob, jak najít webové služby, je vyhledat *webové služby* v [!INCLUDE[prod_short](includes/prod_short.md)]. Na stránce **Webové služby** se ujistěte, že je pro výše uvedené webové služby vybráno pole **Publikovat**. Pro více informací o publikování webových služeb navštivte [Publikování webové služby](across-how-publish-web-service.md).

Chcete-li se dozvědět, co můžete udělat pro zajištění nejlepšího výkonu webových služeb, jak je vidět ze serveru Business Central (koncový bod) a od spotřebitele (klienta), přečtěte si [Webové služby s efektivním zápisem](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### Výběr, zda použít stránky API nebo webové služby OData

Kdykoli je to možné, doporučujeme používat stránky rozhraní API místo webové služby OData. Stránky rozhraní API jsou obecně rychlejší při načítání dat v sestavách Power BI než webové služby OData. Navíc jsou flexibilnější, protože umožňují získat data z polí tabulky, která nejsou definována v objektu stránky.

## <a name="setup"></a>Nastavení [!INCLUDE[prod_short](includes/prod_short.md)] on-premises pro integraci Power BI

Tato část vysvětluje požadavky na nasazení [!INCLUDE[prod_short](includes/prod_short.md)] on-premises pro integraci s Power BI.

1. Nakonfigurujte pro nasazení ověřování NavUserPassword nebo Azure Active Directory.

   Integrace Power BI nepodporuje ověřování windows.

2. Povolte webové služby OData a koncový bod ODataV4.

   Webová služba OData musí být povolena na [!INCLUDE[server](includes/server.md)], a port OData se otevřel v bráně firewall. Pro více informací, navštivte [Konfigurace webové služby Business Central Server - OData](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

   Místní server musí být přístupný z Internetu.

3. Dejte uživatelským účtům [!INCLUDE[prod_short](includes/prod_short.md)] přístupový klíč webové služby.

   Přístupový klíč webové služby je potřeba pouze k zobrazení dat [!INCLUDE[prod_short](includes/prod_short.md)] v Power BI. Každému uživatelskému účtu můžete přiřadit přístupový klíč webové služby. Nebo místo toho vytvořte konkrétní účet s přístupovým klíčem webové služby pro použití všemi uživateli. Pro více informací navštivte [Ověřování webových služeb](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

   <!--
       > [!IMPORTANT]
       > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Using OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

4. Vytvořte registraci přihlášky pro [!INCLUDE[prod_short](includes/prod_short.md)] v Microsoft Azure.

   Pro zobrazení sestav Power BI vložených na stránky [!INCLUDE[prod_short](includes/prod_short.md)], musí být přihláška zaregistrována pro [!INCLUDE[prod_short](includes/prod_short.md)] v Microsoft Azure. Registrovaná aplikace potřebuje oprávnění ke službám Power BI. Pro více informací navštivte [Registrace [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises v Azure AD pro integraci s jinými službami](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

   > [!NOTE]
   > Pokud vaše nasazení používá ověřování NavUserPassword, [!INCLUDE[prod_short](includes/prod_short.md)] se připojuje ke stejné službě Power BI pro všechny uživatele. Tento účet služby zadáte jako součást registrace aplikace. S ověřováním Azure AD, se [!INCLUDE[prod_short](includes/prod_short.md)] připojuje ke službě Power BI přidružené k jednotlivým uživatelským účtům.

   <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Propojte počáteční připojení z Business Central do Power BI.

   Než budou koncoví uživatelé moci používat Power BI v [!INCLUDE[prod_short](includes/prod_short.md)], správce aplikace Azure bude muset udělit souhlas se službou Power BI.

   Chcete-li vytvořit počáteční připojení, otevřete [!INCLUDE[prod_short](includes/prod_short.md)] a z centra rolí spusťte funkci **Začínáme s Power BI**. Tato akce vás povede procesem souhlasu a zkontroluje vaši licenci Power BI. Když se zobrazí výzva k přihlášení pomocí účtu správce Azure. Pro více informací navštivte [Připojení k Power BI - pouze jednou](across-working-with-powerbi.md#connect).

## Zobrazit související školení na webu [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## Viz také

[Business Central a Power BI](admin-powerbi.md)    
[Integrace komponent Power BI a přehledu architektur pro [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)    
[Power BI pro uživatelé](/power-bi/consumer/end-user-consumer)    
[„Nový vzhled“ služby Power BI](/power-bi/service-new-look)    
[Rychlý start: Připojení k datům v Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)    
[Dokumentace Power BI](/power-bi/)    
[Business Intelligence](bi.md)    
[Připravte se na podnikání](ui-get-ready-business.md)    
[Import obchodních dat z jiných finančních systémů](across-import-data-configuration-packages.md)    
[Nastavení [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] jako zdroje dat Power BI](across-how-use-financials-data-source-powerbi.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] jako zdroje dat Power Apps](across-how-use-financials-data-source-powerapps.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] v Power Automate](across-how-use-financials-data-source-flow.md)




[!INCLUDE[footer-include](includes/footer-banner.md)]