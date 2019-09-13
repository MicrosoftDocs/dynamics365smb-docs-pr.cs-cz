---
title: Nastavení generování sestav v Business Central v Power BI | Microsoft Docs
description: 'Zpřístupněte svá data jakožto zdroj dat v Power BI a vytvářejte silné sestavy, vypovídající o stavu vašeho podnikání.'
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 10/01/2018
ms.author: edupont
---
# <a name="using-included365fin_long_mdincludesd365fin_long_mdmd-as-power-bi-data-source-for-building-reports"></a>Používání [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] jako zdroje dat Power BI pro vytváření sestav.
Můžete zpřístupnit svá [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data jakožto zdroj dat v Power BI a vytvářet silné sestavy o stavu vašeho podnikání.  

Musíte mít platný účet v [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] a ve službě Power BI. Také si musíte stáhnout [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365fin_long_mdincludesd365fin_long_mdmd-as-a-data-source-in-power-bi-desktop"></a>Chcete-li přidat [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] jako zdroj dat v Power BI Desktop
1. V Power BI Desktop, v levém navigačním podokně zvolte **Získat data**.
2. Na stránce **Získat data** zvolte **Online služby**, zvolte ** Microsoft Dynamics 365 Business Central**, a poté zvolte tlačítko **Připojit**.
3. Power BI zobrazí průvodce, který vás provede skrz [proces připojení](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). Budete vyzváni k přihlášení do služby. Vyberte možnost **Přihlásit se** a vyberte účet, kterým se chcete přihlásit. To by měl být stejný účet, se kterým se přihlašujete do [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
4. Zvolte tlačítko **Připojit** a pokračujte. Průvodce Power BI zobrazuje seznam Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] společností a zdrojů dat. Tyto zdroje dat představují všechny webové služby, které jste publikovali z každé společnosti v Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. Případně vytvořte novou adresu URL webové služby v [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] pomocí akce **Vytvořit sadu dat** na stránce **Webové služby**, pomocí Průvodce asistovanou instalací **Nastavení vykazování** nebo výběrem akce **Upravit v Excelu** v libovolném seznamu.
6. Určete data, která chcete přidat do svého datového modelu, a poté zvolte tlačítko **Načíst**.
7. Chcete-li do datového modelu Power BI přidat další Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data, opakujte předchozí kroky.

> [!NOTE]  
> Jakmile se úspěšně připojíte k Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], nebudete již vyzýváni k přihlášení.

Jakmile jsou data načtena, objeví se v navigaci vpravo na stránce. V tomto okamžiku jste se úspěšně připojili k datům Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] a jste připraveni začít budovat své sestavy Power BI. 

Před vytvořením sestavy doporučujeme importovat soubor motivu Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Soubor motivu vytvoří paletu barev, takže můžete vytvářet sestavy se stejným stylem barev jako mají obsahové balíčky Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], aniž byste museli definovat vlastní barvy pro každý vizuál.

Pro více informací navštivte[Dokumentace Power BI ](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Viz také
[Business Intelligence](bi.md)  
[Začínáme](product-get-started.md)  
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finance](finance.md)  
[Připojení Power BI k [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  
