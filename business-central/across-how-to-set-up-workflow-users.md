---
title: How to Set Up Workflow Users | Microsoft Docs
description: Before you can create workflows, you must set up the users who take part in workflows. This is necessary, for example, to specify who will receive a notification to act on a workflow step.
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 10/01/2019
ms.author: sgroespe

---
# Nastavení uživatelů workflow
Před vytvořením workflow je nutné nastavit uživatele, kteří se workflow účastní. To je nutné například k určení, kdo bude dostávat oznámení, aby mohl vykonávat činnosti v daném workflow.

Na stránce **Skupina uživatelů workflow** nastavíte uživatele ve skupinách uživatelů workflow a zadáte číslo uživatele v sekvenci procesů, například v řetězci schvalovatelů.

Na stránce **Nastavení uživatelů schvalování** musí být také nastaveni uživatelé workflow, kteří fungují jako uživatelé schválování, a to jak žadatelé o schválení, tak i schvalovatelé. Pro více informací navštivte [Nastavení uživatelů Workflow](across-how-to-set-up-approval-users.md).

> [!NOTE]
> Chcete-li definovat, že žádost o schválení nebude schválena, dokud ji neschválí více schvalovatelů v schvalovacím řetězci, nastavte schvalovatele v hierarchii. Pro typ **Schvalovatel**, nastavte schvalovatele na stránce **Nastavení uživatelů schvalování**. Pro typ **Skupina uživatelů workflow**, nastavte schvalovatele na stránce **Skupiny uživatelů workflow** a definujte hierarchii přiřazením dílčích čísel každému schvalovateli v poli **Pořadové číslo**. Pro více informací navštivte [Nastavení uživatelů schvalování](across-how-to-set-up-approval-users.md).
> Chcete-li definovat, že žádost o schválení není schválena, dokud ji neschválí více stejných schvalovatelů, bez ohledu na hirarchii, vytvořte plochou skupinu uživatelů workflow. Pro typ schvalovatele **Skupina uživatelů workflow**, nastavte schvalovatele na stránce **Skupiny uživatelů workflow** a přiřaďte každému schvalovateli stejné číslo v poli **Pořadové číslo**. Pro více informací navštivte toto téma.
> 
### Nastavení uživatelů workflow

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Skupiny uživatelů workflow** a poté vyberte související odkaz.
2. Vyberte tlačítko **Nový**. Otevře se stránka **Skupina uživatelů workflow**.
3. Do pole **Kód** zadejte maximálně 20 znaků pro identifikaci workflow.
4. V poli **Popis** popište daný workflow.
5. Na záložce **Členové skupiny uživatelů workflow** vyplňte pole v prvním řádku, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Uživatelské jméno** | Určete uživatele, který se bude účastnit workflow. <X1 /><x2 />Uživatel musí existovat na stránce **Nastavení uživatele**. Pro více informací navštivte [Správa uživatelů a práv](ui-how-users-permissions.md). |
   | **Pořadové číslo** | Zadejte pořadí, ve kterém uživatel workflow provede workflow vzhledem k ostatním uživatelům. Toto pole lze použít například k určení, kdy uživatel schvaluje související odezvu workflow ve vztahu k jiným schvalovatelům. Provádí se to tak, že použijete možnost **Skupina uživatelů workflow** v poli **Typ schvalovatele**. **TIP:**  Chcete-li definovat, že žádost o schválení není schválena, dokud ji neschválí více stejných schvalovatelů, bez ohledu na hierarchii, vytvořte skupinu uživatelů plochého workflow přiřazením stejného pořadového čísla příslušným schvalovatelům. |
6. Opakováním kroku 5 přidejte do skupiny uživatelů další uživatele workflow.
7. Opakováním kroků 2 až 6 přidejte další skupiny uživatelů workflow.

## Viz také
[Nastavení uživatelů schvalování](across-how-to-set-up-approval-users.md)  
[Nastavení workflow](across-set-up-workflows.md)  
[Použití workflow](across-use-workflows.md)  
[Návod: Nastavení a použití workflow schvalování nákupů](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)
