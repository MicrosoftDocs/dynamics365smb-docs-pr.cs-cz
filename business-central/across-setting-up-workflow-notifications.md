---
    title: Setting Up Workflow Notifications | Microsoft Docs
    description: Many workflow responses are about notifying a user that an event has occurred that they must act on. For example, on one workflow step, the event can be that User 1 requests approval of a new record, and the response is that a notification is sent to User 2, the approver. On the next workflow step, the event can be that User 2 approves the record, and the response is that a notification is sent to User 3 to start a related processing of the approved record. For workflow steps that are about approval, each notification is tied to an approval entry.
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
# Natavení upozornění workflow
Mnoho odezev workflow se týká upozornění uživatele, že došlo k události, na kterou musí reagovat. Například u jednoho kroku workflow může být událost taková, že uživatel 1 požaduje schválení nového záznamu a odpověď je, že oznámení je odesláno uživateli 2, který je schvalovatel. V dalším kroku workflow může být událost, kterou uživatel 2 schválí, a odpověď je, že uživateli 3 je odesláno oznámení o zahájení souvisejícího zpracování schváleného záznamu. U kroků workflow, které se týkají schvalování, je každé oznámení vázáno na položku schválení. Pro více informací navštivte [Workflow](across-workflow.md).

> [!NOTE]
> Obecná verze [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje oznámení jako e-mail a interní poznámky.

> [!IMPORTANT]
> Všechna oznámení o krocích workflow se odesílají prostřednictvím fronty úloh. Ujistěte se, že fronta úloh ve vaší instalaci je nastavena na zpracování oznámení workflow a zda je zaškrtnuto políčko **Spustit automaticky ze serveru**. Pro více informací viz [Použití front úloh k plánování úkolů](admin-job-queues-schedule-tasks.md).

Různé aspekty oznámení workflow se nastavují na následujících místech:

1. Pro workflow schválení nastavte příjemce oznámení workflow vyplněním řádku na stránce **Nastavení uživatelů schvalování** pro každého uživatele, který se účastní daného workflow. Pokud je například v řádku uživatele 1 zadána v poli **ID schvalovatele** uživatel 2, je oznámení požadavku na schválení odesláno uživateli 1. Pro více informací navštivte [Nastavení uživatelů schvalování](across-how-to-set-up-approval-users.md).
2. Můžete nastavit, kdy a jak budou uživatelé dostávat oznámení workflow vyplněním stránky **Plán upozornění** pro každého uživatele workflow. Pro více informací navštivte [Určení, kdy a jak přijímat upozornění](across-how-to-specify-when-and-how-to-receive-notifications.md).
3. Chcete-li, můžete upravit obsah oznámení e-mailem úpravou sestavy 1320, E-mail s oznámením. Pro více informací navštivte [Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md).
4. Při vytváření daného workflow se nastavuje specifický obsah a pravidla oznámení workflow. To lze provést výběrem možností na stránce **Možnosti odezvy workflow** pro odezvu workflow, která představuje oznámení. Pro více informací navštivte krok 9 ve [Vytvoření workflow](across-how-to-create-workflows.md).

## Viz také
[Nastavení uživatelů schvalování](across-how-to-set-up-approval-users.md)  
[Nastavení uživatelů workflow](across-how-to-set-up-workflow-users.md)  
[Určení, kdy a jak přijímat upozornění](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[Vytvoření workflow](across-how-to-create-workflows.md)  
[Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md)  
[Použití fronty úloh na plánování úloh](admin-job-queues-schedule-tasks.md)  
[Nastavení e-mailu](admin-how-setup-email.md)  
[Návod: Nastavení a použití workflow schvalování nákupů](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)
