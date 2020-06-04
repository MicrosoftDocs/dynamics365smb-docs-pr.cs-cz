---
    title: How to Specify When and How to Receive Notifications | Microsoft Docs
    description: When you set up users in approval workflows, you must specify in the Notification Setup and Notification Schedule pages how and when each user receives notifications about approval workflow steps. Individual users can also change their notification setup by choosing the Change Notification Settings button on any notification.
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
# Určení, kdy a jak přijímat upozornění
Pokud nastavíte uživatele ve workflow schvalování, musíte na stránkách **Nastavení upozornení** a **Plán upozornění** určit, jak a kdy jednotliví uživatelé obdrží upozornění na kroky workflow schvalování. Jednotliví uživatelé mohou také změnit své nastavení upozornění výběrem tlačítka **Změnit nastavení upozornění** u jakéhokoli upozornění.

Než budete moci nastavit předvolby upozornění uživatele schvalování, musíte jej nastavit jako uživatele schvalování. Pro více informací navštivte [Nastavení uživatelů schvalování](across-how-to-set-up-approval-users.md).

Rozložení e-mailových upozornení můžete definovat přizpůsobením sestavy 1320, e-mailové upozornění. Pro více informací navštivte [Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md).

Mnoho kroků workflow schvalování je o upozorňování uživatelů na to, že došlo k události, na kterou musí reagovat. Například v jednom kroku workflow může být událostí, že uživatel 1 požaduje schválení nového záznamu. Související odpověď je, že oznámení je zasláno uživateli 2, schvalovateli. V dalším kroku workflow může být událostí, že uživatel 2 záznam schválí. Související odpovědí je, že uživateli 3 je odesláno upozornění o zahájení procesu se schváleným záznamem. U kroků workflow, které se týkají schvalování, je každé oznámení vázáno na položku schválení. Pro více informací navštivte [Workflow](across-workflow.md).

## Určení, kdy a jak budou uživatelé dostávat upozornění

1. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Nastavení uživatelů schvalování** a poté vyberte související odkaz.
2. Vyberte řádek pro uživatele, pro kterého chcete nastavit předvolby upozornění, a poté vyberte akci **Nastavení upozornění**.
3. Na stránce **Nastavení upozornení** vyplňte pole podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Typ upozornění** | Zadejte typ události, které se upozornění týká. <br /><br />Vyberte jednu z následujících možností:<br /><br /> - **Nový záznam** Určuje, že se upozornení týká nového záznamu, například dokladu, na který musí uživatel reagovat.<br /> - **Schválení** Určuje, že oznámení se týká nejméně jedné žádosti o schválení.<br /> - **Vypr. platnost** Určuje, že upozornění upozorní uživatele, že se zpozdí v reakci na událost. |
   | **Metoda upozornění** | Určete, zda je upozornění e-mailem nebo interní poznámkou. |

   Rozložení e-mailových upozornení můžete definovat přizpůsobením sestavy 1320, e-mailové upozornění. Pro více informací navštivte [Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md).

   Nyní jste určili, jak uživatel obdrží upozornění. Pokračujte a určete, kdy uživatel obdrží upozornění.

4. Vyberte akci **Plán upozornění**.
5. Na stránce **Plán upozornění** vyplňte pole podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Opakování** | Zadejte způsob opakování, ve kterém uživatel obdrží upozornění. |
   | **Čas** | Určete, kdy počas dne obdrží uživatel upozornění, pokud se ohdnota v poli **Opakování** liší od **Okamžitě**. |
   | **Denní frekvence** | Určete, ve které části dne obdrží uživatel upozornění, když je hodnota v poli **Opakování** nastavena na **Denně**. <br /><br />Vyberte **Pracovní den** a uživatel bude přijímat upozornění každý pracovní den v týdnu. Vyberte **Denně**, chcete-li dostávat oznámení každý den v týdnu, včetně víkendů. |
   | **Pondělí** až **neděle** | Můžete určit dny, kdy uživatel obdrží upozornění, pokud je hodnota v poli **Opakování** nastavena na **Týdně**. |
   | **Den v měsíci** | Určete, zda uživatel obdrží upozornění první, poslední nebo konkrétní den v měsíci. |
   | **Datum měsíčního upozornění** | Zadejte datum v měsíci, ve kterém uživatel obdrží upozornění, pokud je hodnota v poli **Den upozornění** nastavena na **Vlastní** . |

## Změnit, kdy a jak dostávat upozornění
1. V jednom z přijatých upozornění, buď jako e-mail nebo poznámka, vyberte tlačítko **Změnit nastavení oznámení**.
2. Na stránce **Nastavení upozornění** změňte předvolby upozornění, jak je popsáno v předchozím postupu.

## Viz také
[Nastavení uživatelů schvalování](across-how-to-set-up-approval-users.md)  
[Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md)  
[Nastavení upozornění workflow](across-setting-up-workflow-notifications.md)  
[Nastavení workflow](across-set-up-workflows.md)  
[Použití workflow](across-use-workflows.md)
