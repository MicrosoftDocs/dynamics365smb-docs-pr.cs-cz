---
title: Propojte svá data pomocí Flow | Microsoft Docs
description: Můžete dát své Business Central údaje k dispozici jako zdroj dat a zadat OData URL svých webových služeb a vytvořit tak automatizovaný pracovní postup.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'workflow, Odata, Power App, SOAP'
ms.date: 10/16/2018
ms.author: solsen
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>Používání [!INCLUDE[d365fin](includes/d365fin_md.md)] v automatizovaném pracovním postupu.
Svá data [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete použít jako součást pracovního postupu v aplikaci Microsoft Flow.

> [!NOTE]
> Kromě Microsoft Flow můžete funkcionalitu pracovního postupu použít i uvnitř [!INCLUDE[d365fin](includes/d365fin_md.md)]. Všimněte si, že ačkoli se jedná o dva samostatné systémy workflow, jakákoli šablona toku, kterou vytvoříte pomocí aplikace Microsoft Flow, bude přidána do seznamu šablon pracovního postupu v rámci [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro více informací navštivte sekci [Workflow](across-workflow.md).  

> [!NOTE]  
>   Musíte mít platný účet v [!INCLUDE[d365fin](includes/d365fin_md.md)] a ve službě Flow.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Chcete-li přidat [!INCLUDE[d365fin](includes/d365fin_md.md)] jako zdroj dat ve Flow
1. V prohlížeči přejděte na web [flow.microsoft.com](https://flow.microsoft.com/en-us/) a přihlaste se.
2. Z pásu karet v horní části stránky vyberte položku **Moje toky**.
3. Existují 2 způsoby, jak vytvořit Flow; **Vytvořit ze šablony** a **Vytvořit od začátku**. Šablona je předdefinovaný tok, který pro vás byl vytvořen.  Chcete-li použít šablonu, jednoduše ji vyberte a vytvořte připojení pro každou službu, kterou šablona používá. Prázdná šablona vám umožňuje vytvořit nový tok zcela od začátku.
4. Chcete-li vytvořit tok z prázdné šablony, vyberte na stránce **Moje toky** možnost **Vytvořit od začátku**.
5. Vyhledejte **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** konektor.
6. Ze seznamu dostupných triggerů vyberte jeden z dostupných triggerů [!INCLUDE[d365fin](includes/d365fin_md.md)]:  
    *Když je požadováno schválení zákazníka*,  
    *Když je požadováno schválení List finančního deníku *,  
    *Když je požadováno schválení řádku finančního deníku*,  
    *Když je požadováno schvalování zboží *,  
    *Když je požadováno schválení nákupního dokladu*,  
    *Když je požadováno schválení prodejního dokladu *, nebo  
    *Když je požadováno schválení dodavatele*.
7. Flow vás vyzve k výběru společnosti ve vašem [!INCLUDE[d365fin](includes/d365fin_md.md)] klientovi, stejně tak k výběru stavu ve vašich datech, která chcete poslouchat.


V tomto okamžiku jste se úspěšně připojili k datům Business Central a jste připraveni začít budovat svůj tok.

8. Chcete-li vytvořit tok ze šablony, zvolte možnost **Vytvořit ze šablony**.
9. Vyhledejte **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]** šablony.
10. Ze seznamu dostupných šablon vyberte jednu z dostupných šablon.  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] prodejní objednávky*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] prodejní nabídky*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] prodejní faktury*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] prodejního dobropisu*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] zákazníka*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] nákupní objednávky*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] nákupní faktury*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] nákupního dobropisu*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] Zboží *,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] dodavatele*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] dávky finančního deníku*,  
    *Požadavek na schválení Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] listu finančního deníku*,  
11. Flow vás vyzve k výběru společnosti ve vašem [!INCLUDE[d365fin_md](includes/d365fin_md.md)] klientovi, Protože každý krok v toku je nezávislý na dalším, budete pravděpodobně muset při použití Flow šablony [!INCLUDE[d365fin_md](includes/d365fin_md.md)] definovat společnost vícekrát.

Pro více informací navštivte sekci [Dokumentace Flow](https://docs.microsoft.com/en-us/flow/getting-started).

Pro poradce při potížích v Microsoft Flow navštivte sekci [Integrace poradce při potížích v Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Viz také
[Začínáme](product-get-started.md)  
[Workflow](across-workflow.md)  
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Správa uživatelů a práv](ui-how-users-permissions.md)   
[Správa workflow[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].](across-use-workflows.md)  
[Nastavení uživatelů schvalování](across-how-to-set-up-approval-users.md)  
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finance](finance.md)  
