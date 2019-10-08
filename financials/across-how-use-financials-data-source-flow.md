---
title: Propojte svá data pomocí Flow | Microsoft Docs
description: Můžete dát své finanční údaje k dispozici jako zdroj dat a zadat OData URL svých webových služeb a vytvořit tak automatizovaný pracovní postup.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'workflow, Odata, Power App, SOAP'
ms.date: 01/25/2018
ms.author: solsen
---
# <a name="using-include-d365finincludesd365fin_mdmd-in-an-automated-workflow"></a>Používání [!INCLUDE [d365fin](includes/d365fin_md.md)] v automatizovaném pracovním postupu.
Svá data [!INCLUDE [d365fin](includes/d365fin_md.md)] můžete použít jako součást pracovního postupu v aplikaci Microsoft Flow.  

> [!NOTE]
>   Musíte mít platný účet v [!INCLUDE [d365fin](includes/d365fin_md.md)] a ve službě Flow.  

## <a name="to-add-include-d365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Chcete-li přidat [!INCLUDE [d365fin](includes/d365fin_md.md)] jako zdroj dat ve Flow
1. V prohlížeči přejděte na web [flow.microsoft.com](https://flow.microsoft.com/en-us/) a přihlaste se.
2. Z pásu karet v horní části stránky vyberte položku **Moje toky**.
3. V okně **Moje toky** zvolte možnost **Vytvořit od začátku**.
4. Ze seznamu dostupných triggerů vyberte jeden z dostupných triggerů [!INCLUDE [d365fin](includes/d365fin_md.md)]:  
    *Když je požadováno schválení zákazníka*,  
    *Když je požadováno schválení List finančního deníku *,  
    *Když je požadováno schválení řádku finančního deníku*,  
    *Když je požadováno schvalování zboží *,  
    *Když je požadováno schválení nákupního dokladu*,  
    *Když je požadováno schválení prodejního dokladu *, nebo  
    *Když je požadováno schválení dodavatele*.
5. Flow vás vyzve k výběru společnosti ve vašem [!INCLUDE [d365fin](includes/d365fin_md.md)] klientovi, Protože každý krok v toku je nezávislý na dalším, budete pravděpodobně muset při použití šablony [!INCLUDE [d365fin](includes/d365fin_md.md)] definovat společnost vícekrát.

V tomto okamžiku jste se úspěšně připojili k datům Business Central a jste připraveni začít budovat svůj tok. Pro více informací navštivte sekci [Dokumentace Flow](https://flow.microsoft.com/documentation/getting-started/).

Pro poradce při potížích v Microsoft Flow navštivte sekci [Integrace poradce při potížích v Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Viz také
[Vítejte v [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Správa uživatelů a práv](ui-how-users-permissions.md)    
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finance](finance.md)  
