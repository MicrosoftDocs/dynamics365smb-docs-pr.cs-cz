---
title: Výběr uživatelského prostředí pro zobrazení nebo skrytí rozšířených funkcí | Microsoft Docs
description: 'Zjistěte, co znamenají úrovně uživatelského prostředí Essential a Premium pro uživatelské rozhraní, oblasti aplikací a vaši společnost.'
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.date: 03/01/2019
ms.author: edupont
---
# <a name="changing-which-features-are-displayed"></a>Změna zobrazovaných funkcí
[!INCLUDE[d365fin](includes/d365fin_md.md)] je navržen tak, aby vám pomohl řídit vaše podnikání, bez ohledu na to, ve které oblasti podnikání jste. V jádru [!INCLUDE[d365fin](includes/d365fin_md.md)] najdete finanční výkaznictví a procesy prodeje a nákupu. K tomu přidáváte funkce podle svých obchodních potřeb přidáním rozšíření z AppSource nebo změnou nastavení Zkušenosti pro vaši společnost. Pro více informací navštivte [Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] pomocí rozšíření](ui-extensions.md) nebo [Výběr uživatelského prostředí pro zobrazení nebo skrytí funkcí](ui-experiences.md#choosing-a-user-experience-to-show-or-hide-features).

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Výběr uživatelského prostředí pro zobrazení nebo skrytí funkcí
Uživatelské prostředí určuje, kolik obecných funkcí je k dispozici, když vy a vaši kolegové používáte [!INCLUDE[d365fin](includes/d365fin_md.md)]. Uživatelské prostředí pro vaši společnost si můžete vybrat na stránce **Informace o společnosti** v poli **Zkušenosti**.

> [!NOTE]  
> Toto nastavení se vztahuje na všechny uživatele ve vaší společnosti. Uživatelé si mohou své vlastní prostředí ještě více přizpůsobit změnou rozvržení stránky a obsahu. Pro více informací navštivte [Přizpůsobení vašeho pracovního prostoru a Stránek](ui-personalization-user.md).  

Následující tabulka obsahuje seznam aktuálně dostupných prostředí.

| Prostředí | Dopad na uživatelské rozhraní |
| --- | --- |
| **Essential** |Zobrazuje všechny akce a pole pro běžné obchodní funkce.|
| **Premium** |Zobrazuje všechny akce a pole pro všechny obchodní funkce, včetně Výroby a Správy služeb.|

> [!NOTE]  
> Prostředí, které si můžete vybrat v [!INCLUDE[d365fin](includes/d365fin_md.md)], závisí na vaší licenci řešení, nazývané plán. Pro více informací o plánech **Essential** a **Premium** navštivte Business Central[](https://go.microsoft.com/fwlink/?linkid=870242) na marketingovém webu Microsoft Dynamics 365. Viz také [Průvodce licencemi [!INCLUDE[d365fin](includes/d365fin_md.md)]](https://go.microsoft.com/fwlink/?linkid=2068931) (vyžaduje přístup k CustomerSource nebo PartnerSource).

> [!IMPORTANT]  
> Všem běžným uživatelům musí být přidělen v řešení stejný plán, Essential nebo Premium, než bude možné toto prostředí vybrat pro společnost. Jeden uživatel proto nemůže přistupovat k funkci Premium, pokud jeden nebo více dalších uživatelů má přístup pouze k funkci Essential. To neplatí pro nepravidelné uživatele typu Člen týmu, Interní správce a Delegovaný správce, kterým lze každému z nich přiřadit jiný plán než ostatním uživatelům v řešení.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Povolení funkcí Premium po aktualizaci plánu
Uživatelé jsou přiřazeni k plánům v centru pro správu Office 365 v souvislosti s obecnou prací na vytvoření uživatelů Business Central. Pro více informací navštivte [Přidání uživatelů k Office 365 pro firmy](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Poté můžete definovat, ke kterým konkrétním funkcím a stránkám v rámci prostředí mají uživatelé přístup, přidělením sad oprávnění. Pro více informací navštivte [Správa uživatelů a oprávnění](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Aktualizace změn plánu ve skupinách uživatelů
Pokud jste provedli změnu v uživatelských právech v centru pro správu Office 365, jako například přidělení více uživatelů do plánu Premium, musíte brát tuto změnu v [!INCLUDE[d365fin](includes/d365fin_md.md)] na vědomí.

1. Přihlašte se jako správce.
2. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Uživatelé** a poté vyberte související odkaz.
3. Na stránce **Uživatelé** zvolte akci **Aktualizovat všechny skupiny uživatelů**.

Všechny nové informace o plánech uživatelů a jejich přiřazených skupinách uživatelů jsou nyní aktualizovány podle změn plánu.

### <a name="to-select-the-premium-experience"></a>Výběr prostředí Premium
Nyní můžete přistoupit k výběru nového prostředí.
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Informace o společnosti** a poté vyberte související odkaz.
2. Na stránce **Informace o společnosti** v záložce s náhledem **Zkušenost uživatele** zvolte Premium v poli **Zkušenosti**.

## <a name="help-assumes-premium-experience"></a>Nápověda předpokládá zkušenost Premium
Všechny popisy funkcí v uživatelské dokumentaci k [!INCLUDE[d365fin](includes/d365fin_md.md)] předpokládají zkušenost **Premium**, což znamená, že popisy pokrývají celý rozsah prvků uživatelského rozhraní. Textová poznámka je vložena do témat nápovědy na vysoké úrovni pro oblasti funkcí Výroba a Správa služeb, v nichž je uvedeno, že vyžadují zkušenost **Premium**.

## <a name="see-also"></a>Viz také
[Vytvoření nové společnosti](about-new-company.md)  
[Správa uživatelů a práv](ui-how-users-permissions.md)    
[Změna základního nastavení](ui-change-basic-settings.md)  
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] Pomocí rozšíření](ui-extensions.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Průvodce licencemi](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
