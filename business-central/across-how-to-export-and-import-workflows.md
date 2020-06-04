---
    title: How to Export and Import Workflows | Microsoft Docs
    description: To transfer workflows to other Business Central databases, for example to save time when creating new workflows, you can export and import workflows.
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
# Export a import workflow
Pro přenesení workflow do jiných [!INCLUDE[d365fin](includes/d365fin_md.md)] databází, například kvůli ušetření času při vytváření nových workflow, můžete daný workflow exportovat a importovat.

Dalším způsobem rychlého vytvoření workflow je vytvoření ze šablon workflow. Pro více informací navštivte [Vytvoření workflow z šablony workflow](across-how-to-create-workflows-from-workflow-templates.md).

Na stránce **Workflow** vytvoříte workflow vypsáním příslušných kroků na řádcích. Každý krok sestává z události workflow, která je řízená podmínkami událostí, a odezvy workflow, která je řízená možnostmi odezvy. Kroky workflow definujete vyplněním polí na řádcích workflow z pevných seznamů hodnot událostí a odezev představujících scénáře, které jsou podporovány kódem aplikace. Pro více informací navštivte [Vytvoření workfloworkflow](across-how-to-create-workflows.md).

## Exportování workflow
1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Workflow** a poté vyberte související odkaz.
2. Vyberte workflow a pak zvolte akci **Export do souboru**.
3. Na stránce **Export souboru** zvolte tlačítko **Uložit**.
4. Na stránce **Export** vyberte umístění souboru a pak klepněte na tlačítko **Uložit**.

## Importování workflow
1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Workflow** a poté vyberte související odkaz.
2. Zvolte akci **Importovat ze souboru**.
3. Na stránce **Importu** zvolte soubor XML, který obsahuje workflow, a pak zvolte tlačítko **Otevřít**.

> [!CAUTION]
> Pokud kód workflow již v databázi existuje, kroky workflow budou přepsány kroky v importovaném workflow.

## Viz také
[Vytvoření Workflow](across-how-to-create-workflows.md)  
[Vytvoření workflow z šablony workflow](across-how-to-create-workflows-from-workflow-templates.md)  
[Zobrazení archivovaných instancí kroku workflow](across-how-to-view-archived-workflow-step-instances.md)  
[Odstranění workflow](across-how-to-delete-workflows.md)  
[Návod: Nastavení a použití workflow schvalování nákupů](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Nastavení workflow](across-set-up-workflows.md)  
[Použití workflow](across-use-workflows.md)  
[Workflow](across-workflow.md)
