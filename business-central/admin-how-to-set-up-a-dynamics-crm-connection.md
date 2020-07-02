---
    title: Connect to Dynamics 365 Sales | Microsoft Docs
    description: You can integrate with Dynamics 365 Sales.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: bholtorf


---
# Nastavení připojení k Dynamics 365 for Sales
Toto téma popisuje, jak nastavit spojení mezi [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)].
<br><br>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## Než začnete
Před vytvořením připojení je třeba připravit několik informací:

* Adresa URL pro vaši aplikaci [!INCLUDE[crm_md](includes/crm_md.md)]. Rychlý způsob, jak získat adresu URL, je otevřít [!INCLUDE[crm_md](includes/crm_md.md)], kopírovat adresu URL a vložit ji do pole **Dynamics 365 for Sales URL** v [!INCLUDE[d365fin](includes/d365fin_md.md)]. [!INCLUDE[d365fin](includes/d365fin_md.md)] opraví formátování za vás.
* Uživatelské jméno a heslo uživatelského účtu, které se používá pouze pro integraci.
* Uživatelské jméno a heslo uživatelského účtu, které má oprávnění správce.

> [!Note]
> Tyto kroky popisují postup online verze [!INCLUDE[d365fin](includes/d365fin_md.md)].

## Nastavení, testování a povolení připojení k [!INCLUDE[crm_md](includes/crm_md.md)]
Pro všechny typy ověřování jiné než ověřování Office 365 nastavíte připojení k Dynamics 365 for Sales na stránce **Nastavení připojení k Microsoft Dynamics 365 for Sales**. K ověření sady Office 365 můžete také použít průvodce asistovaným nastavením **Nastavení připojení Dynamics 365 for Sales**, který vám pomůže poskytnout požadované informace.

### Použití průvodce asistovaným nastavením
Průvodce asistenčním nastavením **Nastavení připojení Dynamics 365 for Sales** vám může pomoci nastavit připojení a určit, zda povolit pokročilé funkce, například propojení mezi záznamy.

1. Vyberte **Nastavení a rozšíření** a poté zvolte **Asistované nastavení**.
2. Vyberte **Nastavení připojení k Dynamics 365 for Sales** a spusťte průvodce asistovaným nastavením.
3. Vyplňte pole podle potřeby.
4. Volitelně existují pokročilá nastavení, která mohou zvýšit zabezpečení a umožnit [!INCLUDE[crm_md](includes/crm_md.md)] další funkce, jako je zpracování prodejních objednávek a zobrazení úrovní zásob. Následující tabulka popisuje pokročilá nastavení.

| Pole | Popis |
|-----|-----|
| **Importování řešení Dynamics 365 for Sales** | Povolte instalaci a konfiguraci integračního řešení v aplikaci [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací, navštivte [Integrace řešení Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md). |
| **Publikace webové služby dostupnosti zboží** | Umožněte lidem, kteří používají [!INCLUDE[crm_md](includes/crm_md.md)], zobrazit dostupnost zboží (produktů) v inventáři v [!INCLUDE[d365fin](includes/d365fin_md.md)]. To vyžaduje uživatelský účet [!INCLUDE[d365fin](includes/d365fin_md.md)] s přístupovým klíčem webových služeb. Přiřazení klíče je proces sestávající ze dvou kroků. Na uživatelském účtu v [!INCLUDE[d365fin](includes/d365fin_md.md)] musíte zvolit akci **Změna klíče webové služby**. V průvodci asistovaného nastavení připojení Dynamics 365 for Sales musíte zadat adresu URL webové služby Dynamics 365 Business Central OData a poskytnout [!INCLUDE[d365fin](includes/d365fin_md.md)] uživatelské údaje pro přístup ke službě. Pro více informací navštivte [Webové služby OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **Webová služba URL Dynamics 365 Business Central OData** | Pokud povolíte webovou službu dostupnosti zboží, bude adresa URL pro webovou službu OData poskytována za vás. |
| **Název uživatele webové služby aplikace Dynamics 365 Business Central OData** | Název [!INCLUDE[d365fin](includes/d365fin_md.md)] uživatelský účet [!INCLUDE[crm_md](includes/crm_md.md)] používá k načtení informací o dostupnosti zboží v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)] prostřednictvím webové služby OData. |
| **Accesskey webové služby aplikace Dynamics 365 Business Central OData** | Přístupová klávesa pro uživatelský účet, který [!INCLUDE[crm_md](includes/crm_md.md)] používá k získání informací o dostupnosti zboží z [!INCLUDE[d365fin](includes/d365fin_md.md)] prostřednictvím webové služby OData. Klíč je přiřazen uživateli zvoleným v poli **Nazev uživatele webové služby aplikace Dynamics 365 Business Central OData**. Chcete-li klíč získat, klepněte na tlačítko **Vyhledat hodnotu** vedle uživatelského jména, zvolte uživatele, zvolte možnost **Spravovat** a pak **Upravit**. Na kartě uživatele zvolte **Akce**, **Ověření** a pak klepněte na **Změna klíče webových služeb**. |
| **Povolit integraci s prodejní objednávkou** | Když uživatelé vytvářejí prodejní objednávky v aplikaci [!INCLUDE[crm_md](includes/crm_md.md)] a cílově objednávky v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)], integruje proces v aplikaci [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací navštivte [Možnost integrovat zpracování prodejních objednávek](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). To vyžaduje zadání pověření pro uživatelský účet správce v aplikaci [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací navštivte [Zpracování údajů o prodejní objednávce](marketing-integrate-dynamicscrm.md). |
| **Povolení připojení Dynamics 365 for Sales** | Povolit připojení k [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Verze Dynamics 365 SDK** | Tento význam je relevantní pouze v případě, že provádíte integraci s verzí aplikace [!INCLUDE[crm_md](includes/crm_md.md)]. Toto je sada pro vývoj softwaru Dynamics 365 (označované také jako XRM), kterou používáte pro připojení [!INCLUDE[d365fin](includes/d365fin_md.md)] do [!INCLUDE[crm_md](includes/crm_md.md)]. Verze musí být kompatibilní s verzí sady SDK používanou aplikací [!INCLUDE[crm_md](includes/crm_md.md)] a je rovno nebo novější než verze používaná službou [!INCLUDE[crm_md](includes/crm_md.md)]. |

> [!Note]
> Sprievodca nastavením asistovaného nastavenia **Nastavení připojení k Dynamics 365 for Sales** automaticky priradí bezpečnostné role **Správce integrace** a **Uživatel integrace** k užívateľskému účtu použitému na integráciu.

### Postup vytvoření nebo udržování připojení ručně
Následující postup popisuje ruční vyplnění polí na stránce **Nastavení připojení Microsoft Dynamics 365 for Sales**. Jedná se také o stránku, na které spravujete nastavení integrace.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení připojení k Microsoft Dynamics 365** a poté vyberte související odkaz.
2. Zadejte následující informace pro připojení z [!INCLUDE[d365fin](includes/d365fin_md.md)] do [!INCLUDE[crm_md](includes/crm_md.md)].

| Pole | Popis |
|-----|-----|
| **URL Dynamics 365 for Sales** | Adresa URL pro instanci aplikace [!INCLUDE[crm_md](includes/crm_md.md)]. Chcete-li získat adresu URL, otevřete okno [!INCLUDE[crm_md](includes/crm_md.md)], zkopírujte adresu URL z adresního řádku v prohlížeči a potom vložte adresu URL do pole. [!INCLUDE[d365fin](includes/d365fin_md.md)] ujistěte se, že je formát správný. |
| **Uživatelské jméno** a **Heslo** | Přihlašovací údaje uživatelského účtu, který je vyhrazen pro integraci. Pro více informací navštivte [Nastavení užívatelských účtů pro integraci s Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md). |
| **Povoleno** | Začněte s integrací. Pokud připojení nyní nepovolíte, bude nastavení připojení uloženo, ale uživatelé nebudou mít přístup k [!INCLUDE[crm_md](includes/crm_md.md)] datům z [!INCLUDE[d365fin](includes/d365fin_md.md)]. Můžete se vrátit na tuto stránku a povolit připojení později. |
| **Verze Dynamics 365 SDK** | Pokud provádíte integraci s verzí [!INCLUDE[crm_md](includes/crm_md.md)], jedná se o soupravu pro vývoj softwaru Dynamics 365 (označovanou také jako Xrm), kterou používáte pro připojení [!INCLUDE[d365fin](includes/d365fin_md.md)] do [!INCLUDE[crm_md](includes/crm_md.md)]. Verze, kterou vyberete, musí být kompatibilní s verzí SDK, kterou používá [!INCLUDE[crm_md](includes/crm_md.md)]. Tato verze je stejná nebo novější než verze použitá v [!INCLUDE[crm_md](includes/crm_md.md)]. |

> [!Note]
> Pokud připojujete místní verzi [!INCLUDE[d365fin](includes/d365fin_md.md)] na [!INCLUDE[crm_md](includes/crm_md.md)] a chcete nakonfigurovat připojení k [!INCLUDE[crm_md](includes/crm_md.md)] s konkrétním typem autentizace, vyplňte pole na záložce **Detaily typu ověření**. Pro více informací navštivte [Použití připojovacích řetězců v nástrojích XRM pro připojení k Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Tento krok není vyžadován při připojování online verze [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Zadejte následující informace pro připojení z [!INCLUDE[crm_md](includes/crm_md.md)] do [!INCLUDE[d365fin](includes/d365fin_md.md)].

| Pole | Popis |
|-----|-----|
| **Dynamics 365 Business Central Web Client URL** | Adresa URL vaší instance [!INCLUDE[d365fin](includes/d365fin_md.md)]. To umožňuje uživatelům v [!INCLUDE[crm_md](includes/crm_md.md)] otevírat odpovídající záznamy v [!INCLUDE[d365fin](includes/d365fin_md.md)] ze záznamů v [!INCLUDE[crm_md](includes/crm_md.md)], například účet nebo produkt. Záznamy [!INCLUDE[d365fin](includes/d365fin_md.md)] se otevírají v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Toto pole nastavte na adresu URL instance [!INCLUDE[d365fin](includes/d365fin_md.md)].<br /><br /> Chcete-li obnovit pole na výchozí adresu URL pro [!INCLUDE[d365fin](includes/d365fin_md.md)], vyberte akci **Resetovat Web Client URL**.<br /><br /> Toto pole je relevantní pouze v případě, že [!INCLUDE[d365fin](includes/d365fin_md.md)] integrační řešení je nainstalováno v [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Povolení webové služky dostupnosti zboží** | Umožněte lidem, kteří používají [!INCLUDE[crm_md](includes/crm_md.md)], zobrazit dostupnost zboží (produktů) v inventáři v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pokud to povolíte, musíte také zadat uživatelské jméno a přístupový klíč pro [!INCLUDE[crm_md](includes/crm_md.md)] , který se použije k dotazování na webovou službu OData o dostupnosti zboží (produktů). Pro více informací navštivte [Webová služba OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md). |
| **Webová služba URL Dynamics 365 Business Central OData** | Pokud povolíte webovou službu dostupnosti zboží, bude adresa URL pro webovou službu OData poskytována za vás. |
| **Název uživatele webové služby aplikace Dynamics 365 Business Central OData** | Název uživatelského účtu, který používá [!INCLUDE[crm_md](includes/crm_md.md)] k získání informací o dostupnosti zboží z [!INCLUDE[d365fin](includes/d365fin_md.md)] prostřednictvím webové služby OData. |
| **Accesskey webové služby aplikace Dynamics 365 Business Central OData** | Přístupový klíč pro uživatelský účet, který používá [!INCLUDE[crm_md](includes/crm_md.md)] k získání informací o dostupnosti zboží z [!INCLUDE[d365fin](includes/d365fin_md.md)] prostřednictvím webové služby OData. Klíč je přiřazen uživateli zvoleným v poli **Nazev uživatele webové služby aplikace Dynamics 365 Business Central OData**. Chcete-li klíč získat, klepněte na tlačítko **Vyhledat hodnotu** vedle uživatelského jména, zvolte uživatele, zvolte možnost **Spravovat** a pak **Upravit**. Na kartě uživatele zvolte **Akce**, **Ověření** a pak klepněte na **Změna klíče webových služeb**. |

4. Zadejte následující nastavení pro [!INCLUDE[crm_md](includes/crm_md.md)].

| Pole | Popis |
|-----|-----|
| **Povolení integrace prodejních objednávek** | Umožněte uživatelům zadávat prodejní objednávky a aktivované nabídky v [!INCLUDE[crm_md](includes/crm_md.md)] a poté je zobrazit a zpracovat v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tím se proces integruje do [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací navštivte [Možnost integrovat zpracování prodejních objednávek](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Automatické vytváření prodejní objednávky** | Když uživatel vytvoří a odešle objednávku v [!INCLUDE[d365fin](includes/d365fin_md.md)], vytvořte prodejní objednávku v [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Automatické zpracování prodejní nabídky** | Když uživatel vytvoří a aktivuje nabídku v [!INCLUDE[d365fin](includes/d365fin_md.md)], zpracujte prodejní nabídku v [!INCLUDE[crm_md](includes/crm_md.md)]. |

5. Zadejte následující pokročilá nastavení.

| Pole | Popis |
|-----|-----|
| **[!INCLUDE[d365fin](includes/d365fin_md.md)] Uživatelé musí mapovat prodejní uživatele Dynamics 365 for Sales** | Určete, zda uživatelské účty [!INCLUDE[d365fin](includes/d365fin_md.md)] musí mít odpovídající uživatelské účty v [!INCLUDE[crm_md](includes/crm_md.md)]. **Ověřovací e-mail Office 365** uživatele [!INCLUDE[d365fin](includes/d365fin_md.md)] musí být stejný jako **Primární e-mail** uživatele [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Pokud nastavíte hodnotu na **Ano**, uživatelé [!INCLUDE[d365fin](includes/d365fin_md.md)], kteří nemají odpovídající uživatelský účet [!INCLUDE[crm_md](includes/crm_md.md)], nebudou mít v uživatelském rozhraní integrační schopnosti [!INCLUDE[d365fin](includes/d365fin_md.md)]. Přístup k [!INCLUDE[crm_md](includes/crm_md.md)] datům přímo z [!INCLUDE[d365fin](includes/d365fin_md.md)] se provádí jménem uživatelského účtu [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Pokud nastavíte hodnotu **Ne**, všichni uživatelé [!INCLUDE[d365fin](includes/d365fin_md.md)] budou mít [!INCLUDE[crm_md](includes/crm_md.md)] integrační schopnosti v uživatelském rozhraní. Přístup k datům [!INCLUDE[crm_md](includes/crm_md.md)] se provádí jménem uživatele [!INCLUDE[crm_md](includes/crm_md.md)] připojení (integrace). |
| **Aktuální uživatel Business Central je namapován k uživateli Dynamics 365 for Sales** | Označuje, zda je váš uživatelský účet namapován na účet v [!INCLUDE[crm_md](includes/crm_md.md)] |

6. Chcete-li otestovat nastavení připojení, vyberte **Testovat připojení**.

   > [!NOTE]
   > Pokud není povoleno šifrování v [!INCLUDE[d365fin](includes/d365fin_md.md)], zobrazí se dotaz, zda jej chcete povolit. Chcete-li aktivovat šifrování dat, vyberte **Ano** a zadejte požadované informace. Jinak zvolte **Ne**. Šifrování dat můžete povolit později. Pro více informací navštivte [Šifrování dat v Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) v nápovědě pro vývojáře a IT-Pro.

7. Pokud synchronizace [!INCLUDE[crm_md](includes/crm_md.md)] ještě není nastavena, zobrazí se dotaz, zda chcete použít výchozí nastavení synchronizace. V závislosti na tom, zda chcete udržovat záznamy zarovnány v [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], vyberte **Ano** nebo **Ne**.

> [!Note]
> Připojení k Dynamics 365 Sales pomocí stránky **Nastavení připojení Microsoft Dynamics 365 Sales** může vyžadovat přiřazení role Správce integrace a Užívatel integrace k účtu použitému pro integraci. Pro více informací navštivte [Přiřazení role zabezpečení uživateli](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user).


> [!Note]
> Připojení k Dynamics 365 for Sales pomocí stránky **Nastavení připojení Microsoft Dynamics 365 for Sales** může vyžadovat, abyste [přiřadili bezpečnostní role **Správce integrace** a **Uživatel integrace**](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user) k uživatelskému účtu použitému pro integraci.


### Odpojení od [!INCLUDE[crm_md](includes/crm_md.md)]
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení připojení k Microsoft Dynamics 365 for Sales** a poté vyberte související odkaz.
2. Na stránce **Nastavení připojení k Microsoft Dynamics 365 for Sales** zrušte zaškrtnutí políčka **Povoleno**.

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension?


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [https://go.microsoft.com/fwlink/?LinkID=616519](https://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](https://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.-->

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [Set Up a Microsoft Dynamics 365 Sales Connection]() -->

<!--
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## Viz také
[Zobrazení stavu synchronizace](admin-how-to-view-synchronization-status.md)
