---
title: Getting the Business Central Add-in for Excel
description: Learn about how to get users the Business Central add-in for Excel. 
author: jswymer

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource
ms.date: 01/03/2023
ms.author: jswymer

---
# Získejte doplněk Business Central pro Excel

[!INCLUDE[prod_short](includes/prod_short.md)] obsahuje doplněk pro excel, který umožňuje uživatelům vybrat akci **Upravit v excelu** na určitých stránkách a otevřít tak data v excelovém listu. Tato akce se liší od akce **Otevřít v aplikaci Excel**, protože umožňuje uživatelům provádět změny v aplikaci Excel a poté publikovat změny zpět do [!INCLUDE[prod_short](includes/prod_short.md)]

## Přehled

### O doplňku

Doplněk se nazývá **Doplněk Microsoft Dynamics Office** a je k dispozici pro instalaci z [Office Store (AppSource).](https://appsource.microsoft.com/) S nainstalovaným doplňkem je akce **Upravit v Excelu** dostupná na většině stránek seznamu a částí seznamu pomocí ikony **Sdílet** ![Sdílet stránku v jiné aplikaci.](media/share-icon.png). Další informace o použití doplňku naleznete v tématu [Zobrazení a úpravy v aplikaci Excel z Business Central](across-work-with-excel.md).

> [!NOTE]
> Doplněk funguje pouze v systému Windows; ne na MacOS.

### O nasazení jako správce

S [!INCLUDE[prod_short](includes/prod_short.md)] online existuje několik možností nasazení, jak dostat doplněk k uživatelům. Jednou z možností je *individuální pořízení*, kdy necháte uživatele instalovat doplněk sami. Při použití této možnosti musí mít uživatelé přístup ke stahování souborů z Office Store. Další možností je nastavit *centralizované nasazení* v Admin Centru pro správu Microsoft 365 tak, aby se doplněk automaticky nasadil do celé organizace, skupin nebo konkrétních uživatelů. Centralizované nasazení poskytuje způsob, jak získat doplněk pro uživatele, pokud vaše organizace neposkytuje uživatelům přístup k Office Store.

Pro koncového uživatele se prostředí instalace liší pro dva scénáře nasazení:

- Při individuální akvizici se při prvním výběru akce **Upravit v aplikaci Excel** otevře podokno **Nový doplněk Office** v aplikaci Excel. K instalaci doplňku uživatel zvolí **Důvěřovat tomuto doplňku**, čímž se doplněk nainstaluje přímo z Office Store. Uživatelé se pak přihlásí do [!INCLUDE[prod_short](includes/prod_short.md)] pomocí svého uživatelského jména a hesla.

- Při centralizovaném nasazení se doplněk při prvním výběru akce **Upravit v aplikaci Excel** automaticky nainstaluje do aplikace Excel z centralizovaného nasazení; ne z Office Store. Jediné, co uživatelé musí udělat, je přihlásit se k [!INCLUDE[prod_short](includes/prod_short.md)]

S oběma těmito možnostmi nasazení je doplněk automaticky nakonfigurován pro připojení k [!INCLUDE[prod_short](includes/prod_short.md)]. Třetí možností nasazení je ruční instalace doplňku přímo z aplikace Excel. Pomocí této možnosti budou uživatelé muset nakonfigurovat doplněk pro připojení k [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="switch"></a>Přechod z individuální akvizice na centralizované nasazení nebo naopak

Když přejdete z individuálního pořízení doplňku na centralizované nasazení nebo naopak, budou ovlivněny soubory aplikace Excel, které uživatelé vytvořili před přechodem. Po přechodu mohou uživatelé stále otevírat všechny listy aplikace Excel, které byly dříve vytvořeny pomocí akce **Upravit v aplikaci Excel** nebo vytvořeny ručně konfigurací doplňku aplikace Excel. Nemohou však aktualizovat data v souboru z Business Central nebo odesílat aktualizace do Business Central

Tento stav je způsoben skutečností, že každému souboru aplikace Excel je přiřazen identifikátor "doplňku". Při přechodu do centralizovaného nasazení nebo z centralizovaného nasazení je přiřazeno jiné ID, takže dřívější ID se zablokuje.

## Příprava (pouze on-premise)

[!INCLUDE[prod_short](includes/prod_short.md)] v místním prostředí vyžaduje, aby vaše prostředí bylo nakonfigurované pro doplněk. Pokud ne, akce **Upravit v Excelu** nebude uživatelům k dispozici. Další informace naleznete v části [Nastavení doplňku aplikace Excel pro úpravu dat Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) v nápovědě pro vývojáře a IT profesionály.

## Nasazení doplňku pomocí centralizovaného nasazení

Centralizované nasazení je funkce v Centru pro správu Microsoft 365, kterou používáte k automatické instalaci doplňků do aplikací Office, jako je Excel. Abychom vám pomohli s centralizovaným nasazením, [!INCLUDE[prod_short](includes/prod_short.md)] zahrnuje asistovanou instalaci **centralizovaného nasazení doplňku aplikace Excel**.

### Než začnete

- Informace o tom, jak uživatelům zabránit ve stahování z obchodu Office, najdete v části [Správa doplňků v centru pro správu](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Ověřte, že centralizované nasazení bude pro vaši organizaci fungovat. Další informace naleznete v tématu [Určení, zda centralizované nasazení doplňků funguje pro vaši organizaci](/microsoft-365/admin/manage/centralized-deployment-of-add-ins)
- Pokud přecházíte z individuální akvizice, přečtěte si téma [Přechod z individuální akvizice na centralizované nasazení.](#switch)

> [!NOTE]
> Povolení centralizovaného nasazení ovlivní funkce, které používají doplněk aplikace Excel, jako je například akce **Upravit v aplikaci Excel**. Nemá žádný vliv na jiné funkce související s aplikací Excel a nebo oprávnění přiřazená uživatelům v [!INCLUDE[prod_short](includes/prod_short.md)]

### Nastavení centralizovaného nasazení doplňku

Budete pracovat v [!INCLUDE[prod_short](includes/prod_short.md)] i v centru pro správu Microsoft 365.

1. V [!INCLUDE[prod_short](includes/prod_short.md)], vyberte ![žárovku, která otevře funkci Řekněte mi.](media/ui-search/search_small.png " Řekněte mi, co chcete udělat"), zadejte **Centralizované nasazení doplňku Excelu** a pak vyberte související odkaz.
2. Přečtěte si informace na stránce **Nastavení doplňku Business Central Excel** a zvolte **Další**.
3. Přihlaste se k [Centru pro správu Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2163967) a přejděte na **Integrované aplikace**<!--**Add-ins**-->.

   Provedením následujících kroků nakonfigurujte doplněk pro nasazení z Office Store:
   1. Zvolte **Získat aplikace** a otevřete Office Store (AppSource). <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
   2. Vyhledejte **Doplněk Microsoft Dynamics Office** a pak vyberte **Získat nyní**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
   3. Na stránce **Přidat uživatele** zadejte uživatele, pro které chcete doplněk nasadit, a pak zvolte **Další**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
   4. Zkontrolujte **Přijmout žádosti o oprávnění** a poté zvolte **Další** > **Dokončit implementaci**.
   5. Počkejte, až se u doplňku zobrazí zelená značka zaškrtnutí vedle položky **Nasazeno**, a poté vyberte možnost **Hotovo**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

      Doplněk se zobrazí na stránce **Doplňky**. Další informace o nasazení doplňků v Centru pro správu Microsoft 365 najdete v tématu [Nasazení doplňků v centru pro správu](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).
4. Vraťte se k asistovanému nastavení **centralizovaného nasazení doplňku aplikace Excel** v [!INCLUDE[prod_short](includes/prod_short.md)] a zvolte **Další**.
5. Zapněte **Použít centralizované nasazení** a zvolte **Dokončit**.

   Pokud tento přepínač nezapnete, [!INCLUDE[prod_short](includes/prod_short.md)] získá doplněk přímo z Office Store.

Po dokončení můžete kdykoli změnit nasazení v Centru pro správu Microsoft 365, například přiřazení dalších uživatelů. Další informace o nasazení doplňků v centru pro správu najdete v části [Nasazení doplňků v centru pro správu](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).

> [!IMPORTANT]
> Máte-li více než jedno prostředí, musíte spustit asistované nastavení **Centralizovaného nasazení doplňku Excel** v každém prostředí, ve kterém chcete centralizované nasazení použít. Centralizované nasazení v Microsoftu 365 ale nemusíte znovu konfigurovat. Jediné, co musíte udělat, je zapnout přepínač **Použít centralizované nasazení** v asistovaném nastavení.

> [!NOTE]
> Uživatelům může trvat až 24 hodin, než se doplněk automaticky nasadí do aplikace Excel.

## <a name="install"></a> Individuální pořízení: Nainstalujte doplněk ručně pro vlastní potřebu

Ve většině případů, když otevřete aplikaci Excel z Business Central, doplněk bude buď nainstalován automaticky pro vás, nebo budete vyzváni k jeho instalaci. Mohou však nastat případy, kdy budete muset doplněk nainstalovat ručně.

1. Otevřete Excel a otevřete libovolný excelový sešit.
2. V nabídce **Vložit** zvolte **Doplňky** > **Získat doplňky**
3. Přejděte na **Spravováno správcem** a vyhledejte **Doplněk Microsoft Dynamics Office**. Pokud tam vidíte, vyberte ji a pak zvolte **Přidat**. Pokud ji nevidíte, přejděte do **Obchodu**, vyhledejte *doplněk Microsoft Dynamics Office* a podle pokynů na obrazovce jej přidejte.

Když je doplněk nainstalován, zobrazí se jako panel v aplikaci Excel. Dále nakonfigurujte připojení.

### Konfigurace připojení Business Central

Pokud se uživatel nemůže připojit automaticky, můžete ho odblokovat tak, že ho požádáte, aby postupoval takto:

1. V podokně doplňku **Microsoft Dynamics** v aplikaci Excel zvolte **možnost Přidat informace o serveru**. Pokud jej nevidíte, vyberte ![v aplikaci Excel tlačítko volby další.](media/cogwheel.png) nahoře a otevřete dialogové okno možností.
2. Pro [!INCLUDE[prod_short](includes/prod_short.md)] online, **nastavte adresu URL serveru** na `https://exceladdinprovider.smb.dynamics.com`. Pro [!INCLUDE[prod_short](includes/prod_short.md)] v místním prostředí, nastavte adresu URL webového klienta, například `https://myBCserver/190`.
3. Zvolte **OK** a potvrďte, že se aplikace znovu načte.
4. Po zobrazení výzvy se přihlaste pomocí svého uživatelského jména a hesla pro Business Central.
5. Volitelně můžete zvolit prostředí a společnost, ke které se chcete připojit.

Doplněk je nyní připojen k [!INCLUDE [prod_short](includes/prod_short.md)] a můžete upravovat data a publikovat změny na [!INCLUDE [prod_short](includes/prod_short.md)].

## Příprava zařízení a sítě pro doplněk aplikace Excel

Síťové služby, jako jsou proxy servery nebo brány firewall, musí umožňovat směrování mezi každým klientským zařízením, na kterém je doplněk nainstalovaný, a mnoha koncovými body služby. Seznam koncových bodů najdete v tématu [Příprava sítě na doplněk Excelu](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## Řešení potíží

Někdy uživatelé narazí na problémy s doplňkem aplikace Excel. Tato část obsahuje několik tipů, jak za určitých okolností uživatele odblokovat.

| Problém | Řešení nebo alternativní řešení | Komentáře |
|---------|---------|---------|
| Doplněk se nespustí | Zkontrolujte, zda je doplněk nasazen centrálně. Nebo zkontrolujte, zda je uživateli blokována místní instalace. | Správce může Office nakonfigurovat tak, aby uživatelé nemohli získat doplňky. V těchto případech musí správce nasadit doplněk centrálně. Další informace najdete v tématu [Nasazení doplňků v Centru pro správu](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true). |
| Data se nenačítají do Excelu | Otestujte připojení otevřením dalšího seznamu v aplikaci Excel z [!INCLUDE [prod_short](includes/prod_short.md)]. Nebo otevřete sešit v aplikaci Excel v prohlížeči. | Pokud uživatel zadal název společnosti, který obsahuje speciální znaky, doplněk se nemůže připojit. |
| Data nelze publikovat zpět do [!INCLUDE [prod_short](includes/prod_short.md)]. | Otestujte připojení otevřením sešitu v aplikaci Excel v prohlížeči. | Někdy může rozšíření zablokovat úlohu publikování. Pokud je stránka rozšířená nebo přizpůsobená, odeberte rozšíření a poté to zkuste znovu. |
| Data jsou špatná | Excel může zobrazovat časy a datumy v jiném formátu než [!INCLUDE [prod_short](includes/prod_short.md)]. Tato podmínka je nedělá špatně a data v [!INCLUDE [prod_short](includes/prod_short.md)] se nezkazí. |         |
| U některých stránek seznamu způsobuje úprava více řádků v Excelu soustavně chyby. K této podmínce může dojít, pokud volání OData zahrnují dynamické pole a pole mimo ovládací prvek opakovače. | Na stránce **Webové služby** zaškrtněte políčka **Vyloučit neupravitelná dynamické pole** a **Vyloučit pole mimo opakovač** pro publikovanou stránku. Zaškrtnutím těchto políček se z výpočtu eTag vyloučí pole a dynamické pole, které nelze upravovat. | Tato zaškrtávací políčka jsou ve výchozím nastavení skrytá. Chcete-li je zobrazit na stránce **Webové služby**, použijte [přizpůsobení](/dynamics365/business-central/ui-personalization-user). |
| Uživatelé se již nemohou přihlásit k doplňku. Když se pokusí přihlásit, proces se zastaví, aniž by byl dokončen. | Tento problém může být způsoben aktualizací doplňku, kterou jsme provedli někdy v červenci 2022. Další informace a opravu naleznete v tématu [Úprava konfigurace doplňku aplikace Excel pro podporu aktualizace z července 2022](/dynamics365/business-central/dev-itpro/administration/update-excel-addin-configuration). | Platí pro [!INCLUDE [prod_short](includes/prod_short.md)] pouze v místním prostředí |

<!--
## Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## Podívejte se na související školení na webu [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Viz také

[Analýza účetní uzávěrky v aplikaci Microsoft Excel](finance-analyze-excel.md)  
[Práce s Business Central](ui-work-product.md)  
[Vylepšení integrace Excelu ve druhé vlně vydání 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
