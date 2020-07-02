---
    title: How to Set Up Approval Users | Microsoft Docs
    description: Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes. In the Approval User Setup page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.
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
# Nastavení uživatelů schvalování
Před vytvořením workflow zahrnující kroky schválení je nutné nastavit uživatele workflow, kteří jsou zapojeni do procesů schvalování. Na stránce **Nastavení uživatele schválení** také nastavíte limity množství pro konkrétní typy požadavků a definujete náhradní schvalující osoby, kterým jsou žádosti o schválení delegovány, když původní schvalující osoba chybí.

> [!NOTE]
> Uživatelé schvalování, žadatelé o schválení i schvalovatelé, musí být nejprve nastaveny jako uživatelé workflow na stránce **Skupina uživatelů workflow**. Pro více informací navštivte [Nastavení uživatelů workflow](across-how-to-set-up-workflow-users.md).

Po nastavení uživatelů schvalování můžete pomoci nastavení vytvořit odezvy workflow pro schválení workflow. Pro více informací navštivte krok 9 ve [Vytvoření workflow](across-how-to-create-workflows.md).

> [!NOTE]
> Chcete-li definovat, že žádost o schválení nebude schválena, dokud ji neschválí více schvalovatelů v schvalovacím řetězci, nastavte schvalovatele v hierarchii. Pro typ **Schvalovatel**, nastavte schvalovatele na stránce **Nastavení uživatelů schvalování**. Pro typ **Skupina uživatelů workflow**, nastavte schvalovatele na stránce **Skupiny uživatelů workflow** a definujte hierarchii přiřazením dílčích čísel každému schvalovateli v poli **Pořadové číslo**. Pro více informací navštivte toto téma a [Nastavení uživatelů workflow](across-how-to-set-up-workflow-users.md).
> Chcete-li definovat, že žádost o schválení není schválena, dokud ji neschválí více stejných schvalovatelů, bez ohledu na hirarchii, vytvořte plochou skupinu uživatelů workflow. Pro typ schvalovatele **Skupina uživatelů workflow**, nastavte schvalovatele na stránce **Skupiny uživatelů workflow** a přiřaďte každému schvalovateli stejné číslo v poli **Pořadové číslo**. Pro více informací navštivte [Nastavení uživatelů workflow](across-how-to-set-up-workflow-users.md).
> 
## Nastavení uživatele schvalování
1. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Nastavení uživatelů schvalování** a poté vyberte související odkaz.
2. Na stránce **Nastavení uživatelů schvalování** vytvořte nový řádek a vyplňte pole podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **ID uživatele** | Vyberte ID uživatele, který je zapojen do schvalovacího procesu. |
   | **Kód prodejce/nákupčího** | Zadejte kód prodejce nebo nákupčího, který se vztahuje k uživateli v poli **Kód prodejce/ nákupčího**.<br /><br /> Obvykle vyplníte pole **Kód prodejce/ nákupčího**, je-li prodejcem nebo kupujícím, který je odpovědný za zákazníka nebo prodávajícího, rovněž osoba, která musí dotyčný požadavek na prodej nebo nákup schválit. |
   | **ID schvalovatele** | Vyberte ID uživatele, který musí schválit požadavky provedené uživatelem v poli **ID uživatele**. |
   | **Limit pro schvalování částky prodeje** | Zadejte maximální částku prodeje v LM, kterou může uživatel v poli **ID uživatele** schválit. |
   | **Neomezené schvalování prodeje** | Specifikujte, že uživatel v poli **ID uživatele** může schválit všechny prodejní požadavky bez ohledu na jejich částku.<br /><br /> Pokud zaškrtnete toto políčko, nebude možné vyplnit pole **Limit pro schvalování částky prodeje**. |
   | **Limit pro schvalování částky nákupu** | Zadejte maximální částku nákupu v LM, kterou může uživatel v poli **ID uživatele** schválit. |
   | **Neomezené schvalování nákupu** | Zadejte, že uživatel v poli **ID uživatele** může schvalovat všechny nákupní požadavky bez ohledu na jejich částku.<br /><br /> Pokud zaškrtnete toto políčko, nebude možné vyplnit pole **Limit pro schvalování částky prodeje**. |
   | **Limit pro schvalování částky požadavku** | Zadejte maximální částku v CZK, kterou může uživatel v poli **ID uživatele** schválit pro nákupní poptávky.<br /><br /> Chcete-li použít toto pole, musíte vybrat možnost **Řetězec schvalovatelů** v poli **Typ limitu schvalovatele** na stránce **Odezvy workflow**. |
   | **Neomezené schvalování požadavku** | Zadejte, že uživatel v poli **ID uživatele** může schválit všechny nákupní poptávky bez ohledu na jejich částku.<br /><br /> Pokud zaškrtnete toto políčko, nebude možné vyplnit pole **Limit pro schvalování částky požadavku**. |
   | **Náhradník** | V poli <x1 />ID uživatele<x2 /> vyberte ID uživatele, který musí schválit žádosti uživatele, pokud uživatel v poli <x3 />ID schvalovatele<x4 /> není k dispozici. **Poznámka:** Náhradníkem může být buď uživatel v poli **Náhradník**, přímý schvalovatel nebo správce schválení v tomto pořadí podle priority. Pro více informací navštivte [Použití schovalování workflow](across-how-use-approval-workflows.md). |
   | **Email** | Zadejte e-mailovou adresu uživatele do pole **ID uživatele**. |
   | **Správce schvalování** | Určete uživatele, který má práva k odblokování schvalování workflow, například delegováním žádostí o schválení na nové náhradníky schvalování a odstraněním žádostí o schválení po splatnosti. |

   > [!Note]
Správcem schválení může být pouze jedna osoba.

3. Chcete-li otestovat nastavení uživatelů schvalování, zvolte akci **Nastavení uživatelů schvalování - test**.
4. Opakujte kroky 2 a 3 pro každého uživatele, kterého chcete nastavit jako uživatele schvalování.

## Viz také
[Nastavení uživatelů Workflow](across-how-to-set-up-workflow-users.md)  
[Nastavení upozornění workflow](across-setting-up-workflow-notifications.md)  
[Vytvoření Workflow](across-how-to-create-workflows.md)  
[Nastavení workflow](across-set-up-workflows.md)  
[Návod: Nastavení a použití workflow schvalování nákupů](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Workflow](across-workflow.md)
