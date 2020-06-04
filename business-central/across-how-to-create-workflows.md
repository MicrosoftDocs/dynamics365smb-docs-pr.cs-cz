---
    title: How to Create Workflows | Microsoft Docs
    description: You can create workflows that connect business-process tasks performed by different users. System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks. Requesting and granting approval to create new records are typical workflow steps.
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
# Vytvoření Workflow
Můžete vytvářet workflow, které spojují úlohy podnikových procesů prováděné různými uživateli. Systémové úlohy, jako je například automatické účtování, lze zahrnout jako kroky do workflow, které předchází nebo následují úkoly uživatele. Vyžádání a udělení souhlasu k vytvoření nových záznamů jsou typické kroky workflow.

Na stránce **Workflow** vytvoříte workflow vypsáním příslušných kroků na řádcích. Každý krok sestává z události workflow, která je řízená podmínkami události, a odezvy workflow s možnostmi odezvy. Kroky workflow definujete vyplněním polí na řádcích workflow z pevných seznamů hodnot událostí a odezev představujících scénáře, které jsou podporovány kódem aplikace.

Při vytváření workflow můžete zkopírovat kroky z existujících workflow nebo ze šablon workflow. Šablony workflow jsou neupravitelné postupy, které existují v obecné verzi aplikace [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kód šablon workflow přidaných společností Microsoft je s předponou „MS-“, například „MS-PIW“. Pro více informací navštivte [Vytvoření workflow z šablony workflow](across-how-to-create-workflows-from-workflow-templates.md).

Pokud váš obchodní scénář vyžaduje události workflow nebo odezvy, které nejsou podporovány, musí je partner společnosti Microsoft implementovat přizpůsobením kódu aplikace.

> [!NOTE]
> Všechna oznámení o krocích workflow se odesílají prostřednictvím fronty úloh. Ujistěte se, že fronta úloh ve vaší instalaci je nastavena na zpracování oznámení workflow a zda je zaškrtnuto políčko **Spustit automaticky z NAS**. Pro více informací viz [Použití front úloh k plánování úkolů](admin-job-queues-schedule-tasks.md).

## Vytvoření Workflow
1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Workflow** a poté vyberte související odkaz.
2. Vyberte tlačítko **Nový**. Otevře se stránka **Workflow**.
3. Do pole **Kód** zadejte maximálně 20 znaků pro identifikaci workflow.
4. Chcete-li vytvořit workflow ze šablony workflow, na stránce **Workflow** zvolte akci **Nové workflow ze šablony**. Pro více informací navštivte [Vytvoření workflow z šablony workflow](across-how-to-create-workflows-from-workflow-templates.md).
5. V poli **Popis** popište dané workflow.
6. V poli **Kategorie** zadejte, do které kategorie workflow patří.
7. V poli **Když událost** zadejte událost, která musí nastat ke spuštění kroku workflow.

   Pokud vyberete pole, otevře se stránka **Události workflow** kde můžete vybrat ze všech událostí workflow, které existují.
8. V poli **Predpoklad** zadejte jednu nebo více podmínek, které musí být splněny, aby mohla nastat událost v poli **Když událost**.

   Když vyberete pole, otevře se stránka **Podmínky události**, kde si vyberete ze seznamu polí filtru, která jsou relevantní jako podmínky pro danou událost. Můžete přidat nová pole filtru, která chcete použít jako podmínky událostí. Filtry podmínek událostí se nastavují stejně jako filtry na stránkách požadavků na sestavu.

   Pokud je událostí workflow změna určitého pole záznamu, otevře se stránka **Podmínky události** s možnostmi pro výběr pole a typu změny.

   1. Chcete-li určit změnu pole pro událost, na stránce **Podmínky události** vyberte v poli **Pole** to pole, které se změní.
   2. V poli **Operátor** vyberte buď **Snížené**, **Zvýšené** nebo **Změněno**.
9. V poli **Potom odezva** zadejte odezvu, která bude následovat, když dojde k události workflow.

   Když vyberete pole, otevře se stránka **Odezvy workflow**, kde můžete vybrat ze všech existujících odezev workflow a nastavit možnosti odezvy pro vybranou odezvu.
10. Na záložce **Možnosti pro vybranou odezvu** můžete určit možnosti odezvy workflow výběrem hodnot v různých zobrazených polích, a to následovně:

   1. Chcete-li zadat možnosti pro workflow, které zahrnují odeslání oznámení, vyplňte pole podle popisu v následující tabulce.

      | Pole | Popis |
      |----------------------------------|---------------------------------------|  
      | **ID uživatele příjemce** | Určete uživatele, kterému musí být oznámení zasláno. Poznámka: Tato možnost je k dispozici pouze pro odezvy workflow se zástupným symbolem pro konkrétního uživatele. Pro odezvy workflow bez zástupných symbolů pro uživatele je příjemce oznámení obvykle definován nastavením uživatele pro schvalování. |
      | **Odkaz na cílovou stránku** | Zadejte jinou stránku v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)], aby se místo výchozí stránky otevřel odkaz v oznámení. |
      | **Vlastní odkaz** | Kromě odkazu na stránku v [!INCLUDE[d365fin](includes/d365fin_md.md)] zadejte URL odkazu, který se přidá k oznámení. |
   2. Chcete-li určit možnosti pro odezvu workflow, která zahrnuje vytvoření požadavku na schválení, vyplňte pole podle následující tabulky.

      | Pole | Popis |
      |----------------------------------|---------------------------------------|  
      | **Výpočet data platnosti** | Určete, kolik dní musí být žádost o schválení vyřešena od data, kdy byla odeslána. |
      | **Delegovat po** | Určete, zda a kdy bude žádost o schválení automaticky delegována na příslušného zástupce. Můžete zvolit automatické delegování jednoho, dvou nebo pěti dnů po datu požadavku na schválení. |
      | **Typ schvalovatele** | Určete, kdo je schvalovatel, podle nastavení uživatelů schvalování a uživatelů workflow.<br /><br /> Existují následující možnosti:<br /><br /> -   **Prodejce/nákupčí** určuje, že uživatel, který je nastaven v poli **Kód prodejce/ nákupčího** na stránce **Nastavení uživatelů schvalování** určuje schvalovatele. Položky požadavku ke schvalování jsou poté vytvořeny podle hodnoty v poli **Typ limitu schvalovatele**.<br /> Pro více informací navštivte [Nastavení uživatelů schvalování](across-how-to-set-up-workflow-users.md). |
      | **Zobrazení potvrzovací zprávu** | Zadejte, zda se uživateli zobrazí potvrzovací zpráva po vyžádání schválení. |
      | **Typ limitu schvalovatele** | Určete, jak mají být limity schválení schvalovatelů ovlivněny při vytváření položek požadavků na schválení. Kvalifikovaný schvalovatel je osoba, jehož schvalovací limit je nad hodnotou na zadané žádosti.<br /><br /> Existují následující možnosti:<br /><br /> 1.  **Řetěz schvalovatelů** určuje, že položky žádosti o schválení jsou vytvářeny pro všechny schvalovatele žadatele až do prvního kvalifikovaného schvalovatele včetně<br />2.  **Přímý schvalovatel** určuje, že položka požadavku na schválení je vytvořena pouze pro okamžitého schvalovatele žadatele, bez ohledu na limit schválení schvalovatele.<br />3.  **První kvalifikovaný schvalovatel** určuje, že položka požadavku na schválení je vytvořena pouze pro prvního kvalifikovaného schvalovatele žadatele.<br /> |
   3. Chcete-li určit možnosti pro odezvu workflow, která zahrnuje vytvoření řádků deníku, vyplňte pole tak, jak je popsáno v následující tabulce.

      | Pole | Popis |
      |----------------------------------|---------------------------------------|  
      | **Název šablony finančního deníku** | Zadejte název šablony finančního deníku, ve které jsou vytvořeny určené řádky deníku. |
      | **Název listu finančního deníku** | Zadejte název listu finančního deníku, ve kterém jsou vytvořeny zadané řádky deníku. |

11. Vyberte tlačítka **Zvýšit odsazení** a **Snížit odsazení**, chcete-li odsadit název události v poli **Když** a definovat pozici kroku ve workflow.
   1. Označte, že krok je další v sledu workflow odsazením názvu události pod názvem události předchozího kroku.
   2. Označte, že krok je jedním z více alternativních kroků, které mohou začít v závislosti na jeho stavu umístěním názvu události na stejné odsazení jako ostatní alternativní kroky. Tyto nepovinné kroky navolte podle priority tím, že umístíte nejdůležitější krok jako první.
   > [!NOTE]
   > Můžete změnit pouze odsazení kroku, který neobsahuje další krok.

12. Opakováním kroků 7 až 11 přidejte další kroky workflow, buď před, nebo po kroku, který jste právě vytvořili.
13. Zaškrtnutím políčka **Povoleno** určíte, že workflow bude zahájen, jakmile dojde k události v prvním kroku typu **Vstupní bod**. Pro více informací navštivte [Použití workflow](across-use-workflows.md).

> [!NOTE]
> Nepovolujte workflow, dokud si nejste jisti, že je workflow dokončen a že lze jeho příslušné kroky zahájit.

> [!TIP]
> Chcete-li zobrazit vztahy mezi tabulkami, které se používají ve workflow, vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), a poté zadejte **Workflow - vazby tabulky**.

## Viz také
[Vytvoření workflow z šablony workflow](across-how-to-create-workflows-from-workflow-templates.md)  
[Nastavení uživatelů schvalování](across-how-to-set-up-approval-users.md)  
[Nastavení upozornění workflow](across-setting-up-workflow-notifications.md)  
[Zobrazení archivovaných instancí kroku workflow](across-how-to-view-archived-workflow-step-instances.md)  
[Odstranění workflow](across-how-to-delete-workflows.md)  
[Návod: Nastavení a použití workflow schvalování nákupů](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Nastavení workflow](across-set-up-workflows.md)  
[Použití workflow](across-use-workflows.md)  
[Workflow](across-workflow.md)

