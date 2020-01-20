---
    title: Setting Up Workflows | Microsoft Docs
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
# Nastavení workflow
Můžete nastavovat a používat workflow, které spojují úlohy podnikových procesů prováděné různými uživateli. Systémové úlohy, jako je například automatické účtování, lze zahrnout jako kroky do workflow, které předchází nebo následují úkoly uživatele. Vyžádání a udělení souhlasu k vytvoření nových záznamů jsou typické kroky workflow. Pro více informací navštivte [Použití workflow](across-use-workflows.md).

Dříve než začnete používat workflow, musíte nastavit uživatele a uživatele schvalování workflow, určit způsob, jakým budou uživatelé dostávat oznámení o krocích workflow, a potom vytvořit workflow, které mohou předcházet přizpůsobení kódu.

Na stránce **Workflow** vytvoříte workflow vypsáním příslušných kroků na řádcích. Každý krok sestává z události workflow, která je řízená podmínkami událostí, a odezvy workflow, která je řízená možnostmi odezvy. Kroky workflow definujete vyplněním polí na řádcích workflow z pevných seznamů hodnot událostí a odezev představujících scénáře, které jsou podporovány kódem aplikace.

Pokud váš obchodní scénář vyžaduje události workflow nebo odezvy, které nejsou podporovány, musí je partner společnosti Microsoft implementovat přizpůsobením kódu aplikace. Pro více informací navštivte v nápovědě pro vývojáře a IT-pro [Návod: Implementace nových událostí a odezev workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| **Viz** | **také** |
|------------|-------------|  
| Nastavení uživatelů workflow a skupin živatelů. | [Nastavení uživatelů workflow](across-how-to-set-up-workflow-users.md) |
| Nastavení uživatelů workflow, kteří se účastní workflow schvalování. | [Nastavení uživatelů schvalování](across-how-to-set-up-approval-users.md) |
| Určete, jak budou uživatelé workflow upozorňováni na kroky workflow, včetně žádostí o schválení. | [Nastavení upozornění workflow](across-setting-up-workflow-notifications.md) |
| Určete, zda jsou uživatelé upozorněni e-mailem nebo poznámkou a jak často jsou oznámení posílané. | [Určení, kdy a jak přijímat upozornění](across-how-to-specify-when-and-how-to-receive-notifications.md) |
| Přizpůsobte obsah oznámení e-mailem úpravou sestavy 1320, e-mailové oznámení. | [Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md) |
| Nastavení serveru SMTP pro povolení e-mailové komunikace v aplikaci [! INCLUDE [ d365fin ](includes/d365fin_md.md) ] | [Nastavení e-mailu](admin-how-setup-email.md) |
| Zadejte různé kroky workflow podle událostí workflow připojením odezvy workflow. | [Vytvoření workflow](across-how-to-create-workflows.md) |
| Použijte šablony workflow k vytváření nového workflow. | [Vytvoření workflow z šablony workflow](across-how-to-create-workflows-from-workflow-templates.md) |
| Sdílejte workflow s jinými [!INCLUDE[d365fin](includes/d365fin_md.md)] databázemi. | [Export a import workflow](across-how-to-export-and-import-workflows.md) |
| Naučte se nastavit workflow pro schvalování prodejních dokladů provedením koncové procedury. | [Návod: Nastavení a použití workflow schvalování nákupů](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) |
| Přidejte podporu pro obchodní scénář, který vyžaduje nové události nebo odezvy workflow přizpůsobením kódu aplikace. | [Návod: Implementace nových událostí a odezev workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) |

## Viz také
[Použití workflow](across-use-workflows.md)  
[Workflow](across-workflow.md)  
[Návod: Nastavení a použití workflow schvalování nákupů](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Práce s Business Central](ui-work-product.md)
