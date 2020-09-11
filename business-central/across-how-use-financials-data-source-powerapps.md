---
title: Use Your Data to Create an App| Microsoft Docs
description: You can make your Business Central data available as a data source and specify an OData URL of your web services to build a business app using Power Apps.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 06/22/2020
ms.author: edupont

---
# Připojení k centrálním obchodním datům pro vytvoření obchodní aplikace pomocí PowerApps

Svá data z [!INCLUDE[prodshort](includes/prodshort.md)] můžete zpřístupnit jako zdroj dat v aplikacích Power Apps.

> [!NOTE]  
> Musíte mít platný účet pro [!INCLUDE[prodshort](includes/prodshort.md)] a Power Apps.

## Přidání [!INCLUDE[prodshort](includes/prodshort.md)] jako zdroj dat pro Power Apps

1. Běžte v prohlížeči na stránku [powerapps.microsoft.com](https://powerapps.microsoft.com/) a přihlašte se.
2. Na domovské stránce v sekci **Vycházet z dat** vyberte dlaždici **Jiné datové zdroje** tile.

   Tím se otevře Power Apps Studio. Při prvním přihlášení musíte zadat zemi nebo oblast
3. V seznamu dostupných připojení zvolte **Business Central** a pak zvolte tlačítko **Vytvořit**.

   Power Apps se připojí k vašemu [!INCLUDE[prodshort](includes/prodshort.md)] pomocí přihlašovacích údajů, s kterými jste přihlášeni. Pokud nejste správcem vašeho [!INCLUDE[prodshort](includes/prodshort.md)], budete se muset přihlásit pomocí jiného účtu.

4. Power Apps zobrazí seznam *Prostředí a společností*, které jsou dostupné z [!INCLUDE[prodshort](includes/prodshort.md)]. Vyberte prostředí a společnost, která obsahuje data, ke kterým se chcete připojit, například *VÝROBA - Moje společnost*.

5. Dále se zobrazí seznam tabulek, které jsou vystaveny jako součást rozhraní API pro vaše prostředí. Vyberte tabulku, ke které se chcete připojit, a poté zvolte **Připojit** .

Tyto takzvané tabulky jsou vystaveny jako koncové body [!INCLUDE[prodshort](includes/prodshort.md)] - konektor pro Power Apps.

> [!NOTE]
> Pokud chcete zahrnout i data z jiných tabulek z [!INCLUDE[prodshort](includes/prodshort.md)] do Vaší aplikace, musíte s vývojářem definovat vlastní API v [!INCLUDE[prodshort](includes/prodshort.md)] a poté toto vlastní API použijte jako vlastní konektor v aplikacích Power Apps. Pro více informací navštivte [Vytváření vlastního konektoru od nuly](/connectors/custom-connectors/define-blank).

V tomto okamžiku jste se úspěšně připojili k vašemu [!INCLUDE[prodshort](includes/prodshort.md)] a jste připraveni začít vytvářet PowerApp. Můžete přidat další obrazovky a připojit se k dalším datům z vašeho [!INCLUDE[prodshort](includes/prodshort.md)]. Pro více informací navštivte [Vytvoření aplikace z příkladu Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).

Pokud jste aplikaci navrhli a vytvořili, můžete ji sdílet se svými kolegy. Pro více informací navštivte [Uložení a publikování vzorové aplikace in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).

> [!NOTE]
> Pokud se chcete připojit k on-premises [ [!INCLUDE[prodshort](includes/prodshort.md)] tak musíte vybrat **Business Central (on-premises)** konektor v kroku 3.

## Viz také

[Vytvoření vzorové aplikace z šablony v Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importování dat z jiných finančích systémů](across-import-data-configuration-packages.md)  
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Vývoj Connect Apps pro Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)
