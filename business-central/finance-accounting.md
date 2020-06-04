---
title: Business Central accountant experience | Microsoft Docs
description: Learn about the accountant portal for Business Central and the Accountant Role Center that supports internal and external accountants in the client company.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 01/06/2020
ms.author: edupont

---
# Zkušenosti účetních v [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
Každý podnik musí dělat své vlastní účetnictví. Některé podniky zaměstnávají externího účetního a jiné mají účetního jako zaměstnance. Bez ohledu na to, jaký typ účetního jste, můžete použít centrum rolí **Účetní** v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Odtud máte přístup ke všem stránkám, které potřebujete ke své práci.

## Centrum rolí pro účetní
Centrum rolí je řídicí panel s dlaždicemi aktivit, které zobrazují klíčová čísla v reálném čase a poskytují rychlý přístup k datům. Na pásu karet v horní části stránky máte přístup k dalším činnostem, například k otevření nejčastěji používaných finančních výkazů a výkazů v Excelu. Na navigačním panelu v horní části můžete rychle přepínat mezi seznamy, které používáte nejčastěji. Zde uvidíte další oblasti, například **Zaúčtované doklady** s různými typy dokladů, které společnost zaúčtovala.

Pokud jste novým uživatelem [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete spustit seznam videí přímo z Centra rolí. Můžete také spustit prohlídku **Začínáme**, která ukazuje na klíčové oblasti.

## <a name="inviteaccountant"></a>Pozvání externího účetního do vašeho [!INCLUDE[d365fin](includes/d365fin_md.md)]
Pokud ke správě finančního výkaznictví používáte externí účetní, může ji správce pozvat do svého [!INCLUDE[d365fin](includes/d365fin_md.md)], aby vám mohla pomoci při práci s vašimi finančními údaji. [!INCLUDE[d365fin](includes/d365fin_md.md)] zahrnuje tři licence typu externí účetní. Pro více informací o licencích navštivte [Příručka licencí Microsoft Dynamics 365 Business Central](https://go.microsoft.com/fwlink/?LinkId=871590).

Jakmile váš účetní získá přístup k vašemu [!INCLUDE[d365fin](includes/d365fin_md.md)], může použít Centrum rolí pro **Účetní**, které umožňuje snadný přístup k nejdůležitějším stránkám pro jejich práci.

Usnadnili jsme vám pozvání externího účetního. Jednoduše otevřete stránku **Uživatelé** a poté na pásu karet vyberte akci **Pozvat externí účetní**. Nyní je připraven e-mail na odeslání, stačí přidat pracovní e-mail svého účetního a odeslat pozvánku.

> [!Note]
> To vyžaduje, abyste nastavili e-mail SMTP. Pro více informací navštivte [Nastavení e-mailu](admin-how-setup-email.md).

<!-- ![Invite your accountant](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]
> E-mailová adresa účetního musí být pracovní adresa založená na Azure Active Directory. Pokud účetní používá jiný typ e-mailu, pozvánku nelze odeslat.
> Tento úkol vyžaduje přístup ke správě uživatelů a licencí v Azure Active Directory, uživateli, který odešle toto pozvání, musí být v Office 365 přiřazena role **Globální správce** nebo **Správce uživatelů**. Pro více informací navštivte [O rolích správce](/office365/admin/add-users/about-admin-roles) v obsahu administrátora Office 365.
> 
### Přidání vašeho účetního do Office 365 prostřednictvím portálu Azure

Pokud váš administrátor nebo prodávající partner nechce používat průvodce **Pozvat externí účetní**, může přidat externího uživatele do portálu Azure Portal a přiřadit tomuto uživateli licenci Externí účetní. Pro více informací navštivte [Rychlý start: Přidejte hostujícího uživatele do svého adresáře na portálu Azure](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### Přidání účetního jako hostujícího uživatele

1. Otevřete [portál Azure](https://portal.azure.com/).
2. V levém podokně vyberte **Azure Active Directory**.
3. V části **Správa** vyberte **Uživatelé**.
4. Vyberte **Nový uživatel typu host**.
5. Na stránce **Nový uživatel** vyberte **Pozvat uživatele** a poté přidejte informace o externím účetním.

   Případně přiložte k uvítacímu účtu osobní uvítací zprávu, která jim sdělí, že je přidáváte do svého [!INCLUDE [prodshort](includes/prodshort.md)].

6. Vyberte **Pozvat**, chcete-li automaticky odeslat pozvánku. V pravém horním rohu se zobrazí upozornění se zprávou **Uživatel je úspěšně pozván**.
7. Po odeslání pozvánky je uživatelský účet automaticky přidán do adresáře jako host.

Dále musíte novému uživateli přiřadit licenci k [!INCLUDE [prodshort](includes/prodshort.md)].

#### Předání přístupu účetnímu k vašemu [!INCLUDE [prodshort](includes/prodshort.md)]

1. Na portálu Azure vyberte na nově přidaném uživateli možnost **Profil** a poté zvolte akci **Upravit**.
2. Aktualizujte pole **Místo použití** na příslušnou zemi a poté vyberte akci **Uložit**.
3. Vyberte akci **Licence** a poté otevřete možnost **Přiřazení**.
4. Vyberte licenci **Dynamics 365 Business Central Externí účetní**.

   Pokud tato licence není k dispozici, musíte místo toho použít dostupnou licenci **Dynamics 365 Business Central for IWs**.
5. Uložte přiřazení.

V případě úspěchu je licence přidělena hostujícímu uživateli a je vytvořen hostitelský účet.

### Import nového uživatele do [!INCLUDE [prodshort](includes/prodshort.md)]

Účetní obdrží e-mail s upozorněním, že ji byl udělen přístup k vaší službě Active Directory. Dále ji musíte poskytnout přístup ke správné společnosti v [!INCLUDE [prodshort](includes/prodshort.md)].

#### Přidání účetní do správné společnosti

1. Otevřete společnost [!INCLUDE [prodshort](includes/prodshort.md)] jejíž přistup chcete poskytnout účetní na [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uživatelé** a poté vyberte související odkaz.
3. Vyberte akci **Získat nové uživatele z Office 365**.

Tím se importuje uživatelský účet, který jste vytvořili na portálu společnosti Azure. Pro více informací navštivte [Přidání uživatele v Business Central](ui-how-users-permissions.md#to-add-a-user-in-business-central).

Pokud chcete udělit přístup k více společnostem, potom se musíte přihlásit do každé společnosti a tento proces opakovat. Alternativně můžete aktualizovat skupiny oprávnění pro uživatelský profil účetní v [!INCLUDE [prodshort](includes/prodshort.md)], například přiřadit jim skupinu uživatelů *D365 Bus Premium*. Pro více informací navštivte [Přiřazení oprávnění uživatelům a skupinám](ui-define-granular-permissions.md).

## Centrum účetních

Pokud jste účetní s více klienty, můžete použít [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)] pro lepší přehled o svých klientech. Odtud máte přístup k systému každého klienta v [!INCLUDE[d365fin](includes/d365fin_md.md)] a můžete použít Centrum rolí pro účetní, jak je popsáno výše. Pro více informací navštivte [Vítejte v [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index).

> [!NOTE]
[!INCLUDE [d365acc_long_md](includes/d365acc_long_md.md)] je aktuálně ve veřejném náhledu na omezeném počtu trhů.

## Viz také

[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Věcné položky a účetní osnova](finance-general-ledger.md)  
[Uzavírání roků a období](year-close-years-periods.md)  
[Práce s dimenzemi](finance-dimensions.md)  
[Analýza finančních výkazů v aplikaci Excel](finance-analyze-excel.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Nastavení analýzy cashflow](finance-setup-cash-flow-analyses.md)  
[Vítejte v [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]](/dynamics365/accountants/index)  
[Dynamics 365 - Účetní Hub na Microsoft.com](https://www.microsoft.com/dynamics365/financial-insights-for-accountants)
