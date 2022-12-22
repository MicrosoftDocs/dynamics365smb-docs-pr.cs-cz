---
title: Create Users According to Licenses
description: Describes how to add users to Business Central online or on-premises based on licenses.
author: edupont04

ms.topic: conceptual
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 6300, 6301, 6302, 8930, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9061, 9069, 9173
ms.date: 05/09/2022
ms.author: edupont

---
# Vytváření uživatelů podle licencí

Tento článek popisuje, jak administrátoři vytvářejí uživatele a definují, kdo se může přihlásit k [!INCLUDE[prod_short](includes/prod_short.md)]. Tento článek také popisuje, jak přiřadit oprávnění různým typům uživatelů podle licencí produktu.

Když vytvoříte uživatele v [!INCLUDE[prod_short](includes/prod_short.md)], můžete jim přiřadit oprávnění prostřednictvím sad oprávnění a organizovat uživatele do skupin uživatelů. Skupiny uživatelů usnadňují správu oprávnění pro více uživatelů současně. Další informace o oprávněních naleznete v tématu [Přiřazení práv uživatelům a uživatelským skupinám](ui-define-granular-permissions.md).

Pro další informace o různých typech licencí a o tom, jak funguje licencování v [!INCLUDE[prod_short](includes/prod_short.md)], [si stáhněte Průvodce licencí v Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Proces správy uživatelů a licencí se liší v závislosti na tom, zda je [!INCLUDE[prod_short](includes/prod_short.md)] nasazen online nebo on-premises (lokálně). Pro [!INCLUDE [prod_short](includes/prod_short.md)] online, musíte přidat uživatele z Microsoftu 365. V on-premimses (lokálních) nasazeních můžete vytvářet, upravovat a odstraňovat uživatele přímo.

## Správa uživatelů a licencí v online tenantech

Vaše předplatné [!INCLUDE[prod_short](includes/prod_short.md)] online definuje počet uživatelů, který máte povolený. Uživatelé jsou přidáváni do vašeho tenanta v Microsoft Partner Center, obvykle vaším partnerem Microsoftu. Pro více informací, navštivte [Správa Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration).

Licence na produkty přidělujete uživatelům podle práce, kterou každý uživatel bude dělat v [!INCLUDE[prod_short](includes/prod_short.md)]. Licence můžete přiřadit několika způsoby:

- Správce Microsoftu 365 vaší společnosti to může udělat v [Centru pro správu Microsoft 365](https://admin.microsoft.com). Pro více informací navštivte [Jednotlivé nebo hromadné přidání uživatelů do Microsoft 365](/microsoft-365/admin/add-users/add-users).
- Partner společnosti Microsoft může přidělovat licence v Microsoft 365 Admin Center nebo v Microsoft Partner Center. Pro více informací navštivte [Úkoly správy uživatelů pro účty zákazníků](/partner-center/assign-licenses-to-users) v nápovědě Microsoft Partner Center.

Pro více informací, navštivte [Správa Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) v nápovědě pro správu.

> [!NOTE]
> Po přidání uživatelů v Centru pro správu Microsoft 365 vám doporučujeme co nejdříve aktualizovat informace o uživatelích v [!INCLUDE[prod_short](includes/prod_short.md)]. Udržování informací o uživatelích v aktuálním stavu je snadné a pomáhá zajistit, aby se uživatelé mohli vždy přihlásit. Více informací naleznete v [Přidání uživatelů nebo aktualizace informací o uživatelích a přiřazení licencí v Business Central](#adduser).<br>
>
> Aktualizace informací o uživateli je obzvláště důležitá, pokud jste přizpůsobili sady oprávnění pro licenci. Pokud se nový uživatel pokusí přihlásit k [!INCLUDE[prod_short](includes/prod_short.md)] předtím, než je přidáte, nemusí se mu to podařit. Pro více informací navštivte [Konfigurace oprávnění na základě licencí](#licensespermissions).
>
> Uživatelé, kteří se s tímto problémem setkají, však nejsou ve skutečnosti blokováni. Mohou buď použít akci **Vrátit se domů** nebo se jednoduše znovu přihlásit a problém tím vyřešit.

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

Pro více informací navštivte [Delegovaný administrátorský přístup k Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).

### <a name="licensespermissions"></a>Konfigurace oprávnění na základě licencí

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Správci mohou konfigurovat sady oprávnění a skupiny uživatelů na základě různých typů licencí.<!--Note to translators: The names in *italics* or capitalized in this section must not be translated.-->

Například běžně používaná licence *Dynamics 365 Business Central Team Member* obsahuje skupiny uživatelů *D365 Team Member* a *Excel Export Action* plus následující nastavení oprávnění ve výchozím nastavení:

- D365 READ
- D365 TEAM MEMBER
- EDIT IN EXCEL - VIEW
- EXPORT REPORT EXCEL
- LOCAL

Pokud tato výchozí konfigurace není pro konkrétního tenanta vhodná, může ji správce změnit. Přizpůsobená oprávnění však ovlivní pouze nové uživatele, kterým je tato licence přiřazena. Oprávnění pro stávající uživatele, kterým je přiřazena licence, nebudou ovlivněna.

1. Přihlaste se k [!INCLUDE[prod_short](includes/prod_short.md)] pomocí účtu správce.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Konfigurace licence** a vyberte související odkaz.

   Případně, pokud už jste na stránce **Uživatelé** můžete spustit průvodce **Aktualizovat uživatele z Microsoftu 365** a pak na první stránce průvodce zvolit odkaz **Konfigurovat oprávnění pro jednotlivé licence**.
3. Na stránce **Konfigurace licence** vyberte licenci, kterou chcete přizpůsobit, a poté vyberte akci **Konfigurovat**.
4. Výběrem pole **Přizpůsobit oprávnění** zapněte přizpůsobení a poté proveďte příslušné změny.

   V našem příkladu chce správce odebrat oprávnění k úpravám v aplikaci Excel, takže odebere skupinu uživatelů *Excel Export*  z licence Team Member. Do budoucna noví uživatelé, kterým je přiřazena licence Team Member, nebudou mít možnost exportovat data do aplikace Excel. Pokud organizace změní názor na toto téma, může se jednoduše vrátit na stránku **Konfigurace licence** a vypnout přizpůsobení pro daný typ licence.

> [!IMPORTANT]
> Toto přizpůsobení oprávnění se projeví pouze u nových uživatelů, kterým přiřadíte příslušnou licenci. Stávající uživatelé nejsou aktualizováni. Doporučujeme přizpůsobit oprávnění před zahájením přiřazování uživatelských licencí v Centru pro správu Microsoft 365.

### <a name="adduser"></a>Přidání uživatelů nebo aktualizace informací o uživatelích a přiřazení licencí v Business Central

Po přidání uživatelů nebo změně informací o uživatelích v Centru pro správu Microsoft 365 můžete informace o uživateli rychle importovat do [!INCLUDE[prod_short](includes/prod_short.md)]. Import zahrnuje přiřazení licencí.

1. Přihlaste se k [!INCLUDE[prod_short](includes/prod_short.md)] pomocí účtu správce.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uživatelé** a poté vyberte související odkaz.
3. Zvolte **Aktualizovat uživatele z Microsoftu 365**.

Pro nové uživatele je dalším krokem přiřazení skupin uživatelů a oprávnění. Další informace o oprávněních naleznete v tématu [Přiřazení práv uživatelům a uživatelským skupinám](ui-define-granular-permissions.md). Pokud aktualizujete informace o uživateli a aktualizace zahrnuje změnu licence, uživatelé jsou přiřazeni k příslušné skupině uživatelů a jejich sady oprávnění se aktualizují. Pro více informací navštivte [Správa oprávnění prostřednictvím skupin uživatelů](ui-define-granular-permissions.md).

> [!NOTE]
> Všichni uživatelé v prostředí musí mít přiřazenu stejnou licenci, buď Essential, nebo Premium. Podrobné informace o licencích naleznete v příručce Microsoft Dynamics 365 Business Central Licensing Guide. Příručka je k dispozici ke stažení na webu [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Další informace o synchronizaci informací uživatelů s Microsoft 365 najdete v části [Synchronizace s Microsoftem 365](#m365) .

> [!NOTE]
> Pokud pro správu účetnictví a finančního výkaznictví používáte externího účetního, můžete ho pozvat do služby Business Central, aby s vámi mohl pracovat na vašich fiskálních údajích. ro více informací navštivte [Pozvání externího účetního do Business Cental](finance-accounting.md#inviteaccountant).

### Odebrání přístupu uživatele do systému

Můžete odebrat přístup uživatele k [!INCLUDE[prod_short](includes/prod_short.md)] online. Všechny odkazy na uživatele se zachovají. Uživatel se však nemůže přihlásit a aktivní relace pro uživatele jsou zastaveny.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uživatelé** a poté vyberte související odkaz.
2. Otevřete stránku **Karta uživatele** pro příslušného uživatele a poté v poli **Stav** vyberte možnost **Zakázáný**.
3. Chcete-li uživateli znovu udělit přístup, nastavte pole **Stav** na hodnotu **Povolený**.

Licenci můžete také odebrat uživateli v Centru pro správu Microsoft 365. Uživatel se pak nemůže přihlásit. Pro více informací navštivte [Odebrání licencí uživatelům](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="m365"></a>Synchronizace s Microsoft 365

Když přiřadíte licenci pro [!INCLUDE[prod_short](includes/prod_short.md)] pro uživatele v Microsoftu 365, existují dva způsoby, jak vytvořit uživatele v [!INCLUDE[prod_short](includes/prod_short.md)].

- Správce může přidat uživatele výběrem akce **Aktualizovat uživatele z Microsoft 365** na stránce **Uživatelé**, jak je popsáno v části [Přidání uživatele nebo aktualizace informací o uživateli v Business Central](#adduser) 
- Informace o licenci se aktualizují automaticky při prvním přihlášení uživatele.

V obou případech se automaticky provede několik nastavení. Tato nastavení jsou uvedena ve druhém a třetím sloupci v následující tabulce.

Pokud změníte informace o uživateli v Microsoftu 365, můžete aktualizovat [!INCLUDE[prod_short](includes/prod_short.md)], aby odrážely změnu. V závislosti na tom, co chcete aktualizovat, použijte jednu z akcí na stránce **Uživatelé**. Akce jsou popsány v posledních třech sloupcích v následující tabulce.

> Akce popsané v následující tabulce jsou přesné, ale jedinou, kterou potřebujete, je **Aktualizovat uživatele z Microsoft 365**, která byla přidána za účelem zjednodušení procesu. Ostatní akce budou odstraněny v budoucí verzi [!INCLUDE[prod_short](includes/prod_short.md)].

|Co se stane, když:|První uživatel, první přihlášení|Získání uživatelů z Microsoft 365|Aktualizace uživatelů z Microsoft 365|Obnovení výchozích skupin uživatelů|Obnovení skupin uživatelů|Aktualizace informací o uživatelích z Microsoft 365|
|-|-|-|-|-|-|-|
|Rozsah:|Aktuální uživatel|Noví uživatelé v Microsoft 365|Více vybraných uživatelů|Jeden vybraný uživatel (kromě aktuálního)|Více vybraných uživatelů|Více vybraných uživatelů|
|Vytvořte nového uživatele a přidělte mu SUPER sadu oprávnění.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Aktualizujte uživatele na základě informací v Microsoft 365: stav, celé jméno, kontaktní e-mail, ověřovací e-mail.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Synchronizujte uživatelské plány (licence) s licencemi a rolemi přiřazenými v Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Přidat uživatele do skupin uživatelů podle aktuálních uživatelských plánů. Odeberte sadu oprávnění SUPER pro všechny uživatele kromě prvního přihlášeného uživatele a [správců](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Je vyžadován alespoň jeden SUPER.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Odstraní ručně přiřazené skupiny uživatelů a oprávnění.|**X**<br /><br />Aktualizovat přiřazení skupin uživatelů.||

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## Správa uživatelů a licencí v on-premise nasazeních

Pro on-premises nasazení je počet uživatelských licencí uveden v licenčním souboru (.flf). Když správce nebo partner Microsoftu nahraje licenční soubor, může určit, kteří uživatelé se mohou přihlásit k [!INCLUDE[prod_short](includes/prod_short.md)].

U on-premises nasazení správce vytváří, upravuje a odstraňuje uživatele přímo ze stránky **Uživatelé**.

### Úprava nebo odstranění uživatele v on-premises nasazení

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uživatelé** a poté vyberte související odkaz.
2. Vyberte uživatele, kterého chcete upravit, a pak zvolte akci **Upravit**.
3. Na stránce **Karta uživatele** změňte informace podle potřeby.
4. Chcete-li odstranit uživatele, vyberte uživatele, kterého chcete odstranit, a pak zvolte akci **Odstranit**.

> [!NOTE]
> U on-premises nasazení může správce určit způsob ověřování uživatelských ověření v nástroji [!INCLUDE[server](includes/server.md)] instance. Při vytváření uživatele zadáte typ ověření, který používáte.
>
> Pro více informací navštivte [Typy ověřování a pověření](/dynamics365/business-central/dev-itpro/administration/users-credential-types) v nápovědě pro správu pro [!INCLUDE[prod_short](includes/prod_short.md)].

## Viz také

[Přiřazení oprávnění uživatelům a skupinám](ui-define-granular-permissions.md)  
[Správa profilů](admin-users-profiles-roles.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
[Přizpůsobení [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Příprava na podnikání](ui-get-ready-business.md)  
[Správa](admin-setup-and-administration.md)  
[Licencování v Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Přidání uživatelů do Microsoft 365 pro firmy](/microsoft-365/admin/add-users/add-users)  
[Zabezpečení a ochrana v Business Central (obsah pro správu)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Přiřazení ID telemetrie uživatelům](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)


[!INCLUDE[footer-include](includes/footer-banner.md)]