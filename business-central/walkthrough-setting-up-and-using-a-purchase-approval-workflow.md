---
    title: Setting Up and Using a Purchase Approval Workflow | Microsoft Docs
    description: You can automate the process of approving new or changed records, such as documents, journal lines, and customer cards, by creating workflows with steps for the approvals in question. Before you create approval workflows, you must set up an approver and substitute approver for each approval user. You can also set approvers’ amount limits to define which sales and purchase records they are qualified to approve. Approval requests and other notifications can be sent as email or internal note. For each approval user setup, you can also set up when they receive notifications.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Návod: Nastavení a použití workflow schvalování nákupu
Můžete automatizovat proces schvalování nových nebo změněných záznamů, jako jsou doklady, řádky deníku a karty zákazníků, vytvořením workflow s kroky pro příslušné schvalování. Před vytvořením schvalovacího workflow je nutné nastavit schvalovatele a nahradit schvalovatele pro každého uživatele schvalování. Můžete také nastavit limity částky schvalovatelů a definovat, které záznamy prodeje a nákupu jsou kvalifikovány ke schvalování. Žádosti o schválení a další oznámení lze odeslat jako e-mail nebo interní oznámení. Pro každé nastavení uživatele schvalování můžete také nastavit, když obdrží oznámení.

> [!NOTE]
> Kromě funkce Workflow v [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete integrovat Microsoft Flow a definovat workflow pro události v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Všimněte si, že ikdyž se jedná o dva samostatné systémy workflow, jakákoli šablona Flow, kterou vytvoříte pomocí aplikace Microsoft Flow, bude přidána do seznamu workflow v [! INCLUDE <x7 /> d365fin <x8 />]. Pro více informací, navštivte [Použití Business Central v automatizovaných workflow](across-how-use-financials-data-source-flow.md).

Můžete nastavovat a používat workflow, které spojují úlohy podnikových procesů prováděné různými uživateli. Systémové úlohy, jako je například automatické účtování, lze zahrnout jako kroky do workflow, které předchází nebo následují úkoly uživatele. Vyžádání a udělení souhlasu k vytvoření nových záznamů jsou typické kroky workflow. Pro více informací navštivte [Workflow](across-workflow.md).

## O tomto návodu
Tento návod ilustruje následující úkoly:

- Nastavení uživatelů schvalování
- Nastavení oznámení pro uživatele schvalování.
- Úprava a povolení schvalovacího workflow.
- Jako Alicia budeme žádet o schválení objednávky.
- Jako Sean obdržíme oznámení a žádost o schválení.

## Příběh
Sean je super uživatel ve společnosti CRONUS. Vytvořil dva uživatele schvalování. Jedním z nich je Alicia, která zastupuje nákupčího. Ten druhý sám zastupuje Aliciina schvalovatele. Sean si poté udělí neomezená práva ke schválení nákupu a stanoví, že obdrží interní notifikaci, jakmile nastane příslušná událost. Nakonec Sean vytvoří požadované workflow schvalování jako kopii existující šablony workflow schvalování objednávky, ponechá všechny stávající podmínky události a možnosti odpovědí nezměněné a poté povolí workflow.

K otestování schvalovacího workflow, se Sean nejdříve připojí do [!INCLUDE[d365fin](includes/d365fin_md.md)] jako Alicia a poté požádá o schválení objednávky. Sean se poté přihlásí sám za sebe, uvidí oznámení ve svém Centru rolí, poté rozkline odkaz na žádost o schválení objednávky a žádost schválí.

## Nastavení vzorových dat
Předím, než nastavíte uživatele schvalování a metodu oznámení, musíe se ujistit, že existují dva uživatelé v [!INCLUDE[d365fin](includes/d365fin_md.md)]: Jeden uživatel reprezentuje Alicii. Druhý uživatel, vy, reporezentujete Seana. Pro více informací navštivte [Vytvoření uživatelů dle licencí](ui-how-users-permissions.md).

### Nastavení uživatelů schvalování
Pokud jste přihlášeni jako vy, nastavte Alicii jako uživatele schválení, jehož schvalovatelem jste sami. Nastavte oprávnění ke schválení a určete, jak a kdy budete o žádostech o schválení informováni.

#### Nastavení Vašeho účtu a Alicie jako uživatelů schvalování
1. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Nastavení uživatelů schvalování** a poté vyberte související odkaz.
2. Na stránce **Nastavení uživatelů schvalování** vyberte akci **Nový**.

   > [!NOTE]  
   > Nejdříve musíte nastavit schvalovatele, než nastavíte uživatele schvalování, který potřebuje svého schvalovatele. Proto musíte nejdříve nastavut sebe před nastavením Alicie.

3. Nastavte dva uživatele schvalování tak, že vyplníte pole podle popisu v následující tabulce.

   | ID uživatele | ID schvalovatele | Neomezené schvalování nákupu |
   |-------------|-----------------|---------------------------------|  
   | VY | Vybraný |
   | ALICIA | VY |

### Nastavení oznámení
V tomto návodu je uživatel upozorněn interním oznámením o požadavcích na schvalování. Oznámení o schválení může být také odsláno e-mailem. Pro více informací navštivte [Nastavení, kdy a jak přijímat upozornění](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### Nastavení způsobu jak a kdy budete upozorněni
1. Na stránce **Nastavení uživatelů schvalování**, vyberte řádek s Vími a zvolte akci **Nastavení upozornění**.
2. Na stránce **Nastavení upozornění** v poli **Typ upozornění** vyberte **Schvalování**.
3. V poli **Metoda upozornení** zvolte **Oznámení**.
6. Na stránce **Nastavení upozornění**zvolte akci **Plán upozornění**.
7. Na stránce **Plán upozornění** v poli **Opakování** vyberte **Okamžitě**.

## Vytvoření Workflow
Vytvořte workflow schvalování nákupní objednávky zkopírováním kroků ze šablony workflow Schvalování nákupní objednávky. Ponechejte existující kroky workflow beze změny a povolte ho.

### Vytvoření a povolení workflow schvalování nákupní objednávky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Workflow** a poté vyberte související odkaz.
2. Na stránce **Workflow** zvolte akci **Nové workflow ze šablony**.
3. Na stránce **Šablony workflow** vyberte workflow jménem Workflow schvalování nákupní objednávky, a potom vyberte tlačítko **OK**.

   Otevře se stránka **Workflow** pro nové workflow obsahující všechny informace o vybrané šabloně. Hodnota v poli **Kód** je rozšířena o “-01” což znamená, že se jedná o první workflow vytvořené ze šablony Workflow schvalování nákupní objednávky.
5. V hlaviččce stránky **Workflow** vyberte **Povoleno**.

## Použití schovalování workflow
Použijte nové workflow Schvalování nákupní objednávky tak, že se nejprve přihlásíte do [[!INCLUDE[d365fin](includes/d365fin_md.md)] jako Alicia a podejte požádat o schvalování nákupní objednávky. Potom se přihlaste sami, zobrazte upozornění v Centru rolí, kliknetě na odkaz žádosti o schválení a pak žádost schvalte.

### Žádost o schválení objednávky jako Alicia.
1. Přihlaste se jako Alicia.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.
3. Vyberte řádek pro otevřenou nákupní objednávku 106001 a pak zvolte akci **Upravit**.
4. Na stránce **Nákupní objednávka** zvolte **Odeslat žádost o schávlení**.

Všimněte si, že hodnota v poli **Stav** se změnila na **Čeká na schválení**.

### Schválení objednávky jako Sean
1. Přihlaste se jako Sean.
2. V centru rolí v sekci **Samoobslužné** vyberte dlaždici **Požadavky na schválení**.
3. Na stránce **Požadavky na schválení** vyberte řádek od Aliciea poté zmáčkněte tlačítko **Schválit**

Hodnota v poli **Stav** na Aliciini nákupní objednávce se změní na **Vydáno**.

Nyní jste nastavili a testovali jednoduché workflow na základě prvních dvou kroků Workflow schvalování nákupní objednávky. Můžete snadno rozšířit toto workflow tak, aby se automaticky odesílaly nákupní objednávky Alicii, když je Sean schválí. Chcete-li to provést, musíte povolit Worklflow nákupní faktury ve Workflow, ve kterém je odpověď na vydanou nákupní fakturu k zaúčtování. Nejprve je nutné změnit podmínku události při prvním kroku workflow z (nákupní) **Faktura** na **Objednávka**.

Obecná verze [!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje řadu šablon workflow pro scénáře, které jsou podporovány kódem aplikace. Většina z nich je určena pro schvalování.

Varianty workflow definujete vyplněním polí na řádcích workflow z pevných seznamů hodnot událostí a odpovědí představujících scénáře podporované kódem aplikace. Pro více informací navštivte [Vytvoření workflow](across-how-to-create-workflows.md).

Pokud obchodní scénář vyžaduje událost nebo odpověď workflow, která není podporována, musí je partner společnosti Microsoft implementovat. Pro více informací navštivte v nápovědě pro vývojáře a IT-pro [Návod: Implementace nových událostí a odezev workflow](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses).

## Viz také
[Nastavení uživatů schvalování](across-how-to-set-up-approval-users.md)   
[Nastavení upozonění Workflow](across-setting-up-workflow-notifications.md)   
[Vytváření workflow](across-how-to-create-workflows.md)   
[Použití schvalování Workflows](across-how-use-approval-workflows.md)   
[Workflow](across-workflow.md)  
[Použivání Business Central v automatických Workflow](across-how-use-financials-data-source-flow.md)
