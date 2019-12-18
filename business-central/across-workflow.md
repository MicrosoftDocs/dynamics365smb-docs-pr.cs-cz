---
    title: Workflow | Microsoft Docs
    description: You can set up and use workflows that connect business-process tasks performed by different users. System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks. Requesting and granting approval to create new records are typical workflow steps.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Workflow
Můžete nastavovat a používat workflow, které spojují úlohy podnikových procesů prováděné různými uživateli. Systémové úlohy, jako je například automatické účtování, lze zahrnout jako kroky do workflow, které předchází nebo následují úkoly uživatele. Vyžádání a udělení souhlasu k vytvoření nových záznamů jsou typické kroky workflow.

Na stránce **Workflow** vytvoříte workflow vypsáním příslušných kroků na řádcích. Každý krok sestává z události workflow, která je řízená podmínkami událostí, a odezvy workflow, která je řízená možnostmi odezvy. Kroky workflow definujete vyplněním polí na řádcích workflow z pevných seznamů hodnot událostí a odezev představujících scénáře, které jsou podporovány kódem aplikace.

Obecná verze programu [! INCLUDE [ d365fin ](includes/d365fin_md.md) ] obsahuje řadu předem nakonfigurovaných workflow reprezentovaných šablonami workflow, které můžete zkopírovat a tím workflow vytvořit. Kódy pro šablony workflow přidané společností Microsoft jsou s předponou "MS-". Pro více informací navštivte seznam šablon workflow na stránce šablony workflow.

Pokud váš obchodní scénář vyžaduje události workflow nebo odezvy, které nejsou podporovány, musí je partner společnosti Microsoft implementovat přizpůsobením kódu aplikace. Pro více informací navštivte v nápovědě pro vývojáře a IT-pro [Návod: Implementace nových událostí a odezev workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses).

> [!NOTE]
> Kromě funkce Workflow v [!INCLUDE[d365fin](includes/d365fin_md.md)] jej můžete integrovat do Microsoft Flow a definovat workflow pro události v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Všimněte si, že ačkoli se jedná o dva samostatné systémy workflow, jakákoli šablona toku, kterou vytvoříte pomocí aplikace Microsoft Flow, bude přidána do seznamu šablon workflow v rámci [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro více informací, navštivte [Použití Business Central v automatizovaných workflow](across-how-use-financials-data-source-flow.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| **Viz** | **také** |
|------------|-------------|  
| Nastavte uživatele workflow, určete způsob, jakým budou uživatelé upozorněni, a vytvořte nové workflow. U nových workflow pro nepodporované scénáře implementujte požadované prvky workflow přizpůsobením kódu aplikace. | [Nastavení workflow](across-set-up-workflows.md) |
| Povolení workflow, zpracování oznámení workflow včetně schválení žádostí a schválení žádostí o provedení kroku workflow. Archivovaní a odstranění workflow. | [Použití workflow](across-use-workflows.md) |

## Viz také
[Prodej](sales-manage-sales.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Řízení projektů](projects-manage-projects.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
