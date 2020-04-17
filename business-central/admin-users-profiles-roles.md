---
title: Správa uživatelů a rolí | Microsoft Docs
description: Dozvěďte se více o správě uživatelů a centech rolí v Business Cental.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: 'profiles, users'
ms.date: 10/24/2018
ms.author: edupont
---
# <a name="understanding-users-profiles-and-role-centers"></a>Porozumění uživatelům, profilům a centrům rolí

V [!INCLUDE[d365fin](includes/d365fin_md.md)] jsou uživatelé přidáváni administrátorem, který také dává uživatelům přístup k oblastem v [!INCLUDE[d365fin](includes/d365fin_md.md)], které potřebují v jejich práci.  

Přístup k funkcím je řízen prostřednictvím *skupin uživatelů* a *profilů*. Jako správce můžete v rámci předplatného [!INCLUDE[d365fin](includes/d365fin_md.md)] přidávat a odebírat uživatele a přiřazovat uživatelská oprávnění prostřednictvím skupin uživatelů.  

## <a name="adding-users"></a>Přidávání uživatelů

Chcete-li přidat uživatele do [!INCLUDE[d365fin](includes/d365fin_md.md)] online, musí správce vaší společnosti Office 365 nejprve vytvořit uživatele v Office 365 Admin Center. Pro více informací navštivte [Přidejte uživatele k Office 365 pro firmy](https://aka.ms/CreateOffice365Users).

Poté může správce přiřadit oprávnění každému uživateli a skupinám uživatelů. Pro více informací navštivte [Správa uživatelů a oprávnění](ui-how-users-permissions.md).  

Nejsilnější oprávnění, které může mít uživatel je sada oprávnění SUPER. Každá společnost musí mít alespoň jednoho uživatele s touto sadou oprávnění, ale nejlepší postup je udělit každému uživateli oprávnění, která odpovídají jejich pracovním potřebám v [!INCLUDE[prodshort](includes/prodshort.md)], a ne více než to. To pomáhá zajistit, aby uživatelé měli například přístup pouze k datům, která jsou relevantní pro jejich práci.  

> [!TIP]
> Doporučujeme zajistit, aby měl správce Office 365 také oprávnění SUPER v [!INCLUDE[prodshort](includes/prodshort.md)], protože to usnadňuje mnoho administrativních úkolů, včetně nastavení integrace s jinými aplikacemi.

### <a name="users-of-on-premises-deployments"></a>On-premises uživatelé

V případě on-premises [!INCLUDE[d365fin](includes/d365fin_md.md)] administrátor si může vybrat mezi různými mechanismy autorizace pověření pro uživatele. Poté, když vytvoříte uživatele, poskytnete různé informace v závislosti na typu pověření, které používáte v konkrétní [!INCLUDE[server](includes/server.md)] instanci. Pro více informací navštivte [Typy ověřování a pověření ](/dynamics365/business-central/dev-itpro/administration/users-credential-types)v části Správa Vývojáře a obsahu ITPro pro [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profily

Lidé ve vaší společnosti, kteří mají přístup k [!INCLUDE[d365fin](includes/d365fin_md.md)], mají přiřazený *profil*, který jim umožňuje přístup do *Centra rolí*.

Profily jsou sbírky [!INCLUDE[d365fin](includes/d365fin_md.md)] uživatelů, kteří sdílejí stejné Centrum rolí. Centrum rolí je vstupní bod a domovská stránka v [!INCLUDE[d365fin](includes/d365fin_md.md)], která vám poskytuje rychlý přístup k nejdůležitějším úkolům, zobrazuje různé statistiky a klíčové ukazatele výkonu (KPI) o vaší práci.  

> [!NOTE]  
>  V aktuální online verzi [!INCLUDE[d365fin](includes/d365fin_md.md)] nemůžete přidávat, upravovat ani mazat profily.  

### <a name="CreateProfile"></a>Vytváření profilů

1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Profily** a pak vyberte související odkaz.  

2.  Na stránce **Seznam profilů** vyberte akci **Nový**, která otevřete stránku **Nová karta profilu.**.  

3.  Do pole **ID profilu** zadejte název, které popisuje zamýšlenou roli uživatelů.  

4.  Do pole **Popis** zadejte popis ID profilu, například **Zpracovatel objednávek**.  

5.  Nastavte pole **ID centra rolí** na Centrum rolí, které chcete profilu přiřadit.  

Postup úpravy existujícího profilu je stejný, kromě toho, že vyberete existující profil na stránce **Profily** namísto výběru tlačítka **Nový**.  


### <a name="copy-a-profile"></a>Kopírování profilů
Kopírování profilu vám může ušetřit čas, pokud chcete v profilu použít podobné nastavení a chcete změnit pouze několik nastavení.

1.  Otevřete profil, který chcete zkopírovat, a pak vyberte tlačítko **Kopírovat profil**.

2.  Do pole **Nové ID profilu** zadejte název profilu, který chcete zkopírovat.

3.  Nastavte pole **Obor nového profilu** na jednu z následujících možností:

    - **Systém** zpřístupní nový profil všem nájemcům databáze, kteří aplikaci používají.
    - **Tenant** zpřístupní nový profil pouze aktuální databázi nájemců.
4. Po dokončení zvolte tlačítko **OK**.

### <a name="ExportImportProfile"></a>Export a import profilů

Profily můžete exportovat a importovat jako soubory XML z a do databáze [!INCLUDE[d365fin](includes/d365fin_md.md)]. Export a import profilu vám může ušetřit čas při konfiguraci uživatelského rozhraní, protože znovu použijete existující konfiguraci profilu místo toho, abyste museli profil konfigurovat od nuly. Pokud máte profil nakonfigurovaný v databázi [!INCLUDE[d365fin](includes/d365fin_md.md)] a chcete znovu použít všechny nebo některé stejné konfigurace profilu v jiné databázi, můžete jej exportovat do souboru XML. Poté můžete importovat soubor XML profilu do jiné databáze.

-   Chcete-li exportovat profil, můžete buď vybrat akci **Exportovat profilů** na stránce **seznam Profilů** nebo na **kartě profilu** nebo můžete vyhledat a otevřít stránku **Export profilů**. Uložte soubor XML v počítači nebo síti.

-   Chcete-li importovat profil, můžete buď vybrat tlačítko **Importovat profil** na stránce **seznam Profilů**, nebo můžete vyhledat a otevřít stránku **Importovat profil**. 

    > [!NOTE]  
    >  Nelze importovat profil, který již v databázi existuje, přestože je soubor XML pojmenován odlišně nebo má jiný obsah. Před importem nového profilu musíte odstranit existující profil.


## <a name="configuration-and-personalization"></a>Konfigurace a přizpůsobení
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

Uživatelé si přizpůsobují své uživatelské rozhraní pomocí svého uživatelského nastavení pod svým vlastním loginem. Tyto přizpůsobení může správce odstranit. Pro více informací navštivte [Přizpůsobení pracovního prostředí](ui-personalization-user.md).  

## <a name="see-also"></a>Viz také  
[Správa uživatelů a práv](ui-how-users-permissions.md)  
[Správa Personalizace jako správce](ui-personalization-manage.md)  
[Přizpůsobení pracovního prostředí](ui-personalization-user.md)  
