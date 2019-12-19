---
title: How to Create Workflows from Workflow Templates | Microsoft Docs
description: To save time when creating new workflows, you can create workflows from workflow templates.
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
# Vytvoření workflow z šablony workflow
Chcete-li ušetřit čas při vytváření nového workflow, můžete jej vytvořit ze šablon workflow.

Šablony workflow jsou neupravitelné postupy, které existují v obecné verzi aplikace [! INCLUDE[d365fin](includes/d365fin_md.md)]. Kódy pro šablony workflow přidané společností Microsoft jsou s předponou "MS-".

Dalším způsobem rychlého vytvoření workflow je import existujícího workflow, který je mimo [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro více informací navštivte [Export a import workflow](across-how-to-export-and-import-workflows.md).

Na stránce **Workflow** vytvoříte workflow vypsáním příslušných kroků na řádcích. Každý krok sestává z události workflow, která je řízená podmínkami událostí, a odezvy workflow, která je řízená možnostmi odezvy. Kroky workflow definujete vyplněním polí na řádcích workflow z pevných seznamů hodnot událostí a odezev představujících scénáře, které jsou podporovány kódem aplikace. Pro více informací navštivte [Vytvoření workflow](across-how-to-create-workflows.md).

## Vytvoření workflow z šablony workflow
1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Workflow** a poté vyberte související odkaz.
2. Vyberte akci **Nové workflow ze šablony workflow**. Otevře se stránka **Šablony workflow**.
3. Vyberte šablonu workflow a poté zvolte tlačítko **OK**.

   Otevře se stránka **Workflow** pro nový workflow obsahující všechny informace z vybrané šablony. Hodnota v poli **Kód** je rozšířena, například o "-01", což označuje, že se jedná o první workflow, který je vytvořen ze šablony daného workflow.
4. Pokračujte ve vytváření workflow úpravou kroků nebo přidáním nových kroků. Pro více informací navštivte [Vytvoření workflow](across-how-to-create-workflows.md).

## Viz také
[Vytvoření Workflow](across-how-to-create-workflows.md)  
[Export a import workflow](across-how-to-export-and-import-workflows.md)  
[Zobrazení archivovaných instancí kroku workflow](across-how-to-view-archived-workflow-step-instances.md)  
[Odstranění workflow](across-how-to-delete-workflows.md)  
[Návod: Nastavení a použití workflow schvalování nákupů](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Nastavení workflow](across-set-up-workflows.md)  
[Použití workflow](across-use-workflows.md)  
[Workflow](across-workflow.md)
