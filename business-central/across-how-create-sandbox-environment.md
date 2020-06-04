---
title: Create a Sandbox Environment| Microsoft Docs
description: Create an environment for exploring, learning, demoing, developing, and testing.
author: SusanneWindfeldPedersen

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/10/2019
ms.author: solsen

---
# Vytváření Sandboxového prostředí v [!INCLUDE [prodshort](includes/prodshort.md)]S

S [!INCLUDE [prodshort](includes/prodshort.md)], můžete snadno vytvořit bezpečné prostředí, kde můžete testovat, trénovat nebo řešit problémy, aniž byste rušili pracovní procesy nebo obchodní data vaší společnosti. Takové neprodukční prostředí se nazývá *sandbox*. Díky izolaci od výroby, je prostředí sandbox místem, kde můžete bezpečně prozkoumat, učit se, předvádět, vyvíjet a testovat službu bez rizika ovlivnění dat a nastavení vašeho produkčního prostředí.

Váš správce může vytvořit prostředí sandboxu v [Centru pro správu](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), ale pokud chcete něco rychle otestovat sami, můžete vytvořit sandboxové prostředí uvnitř [!INCLUDE [prodshort](includes/prodshort.md)].

> [!NOTE]
> Sandboxové prostředí se po technické stránce velmi liší od produkčního prostředí a to i v případě, že váš správce vytvoří sandbox, který obsahuje výrobní data. Pro benchmarking nelze použít sandbox a nemůžete například požádat o export databáze. Pokud chcete vytvořit sandboxové prostředí pro benchmarking, může váš správce vytvořit vyhrazené produkční prostředí v centru pro správu. Pro více informací navštivte [Typy prostředí](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## Pro vytvoření prostředí sandboxu ve vašem [!INCLUDE [prodshort](includes/prodshort.md)]

1. Přihlaste se do své produkční instance v [!INCLUDE[d365fin](includes/d365fin_md.md)].

2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prostředí Sandbox**, a poté vyberte související odkaz.
   <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Vyberte tlačítko **Vytvořit**.

   Otevře se další záložka s [!INCLUDE[d365fin](includes/d365fin_md.md)], kde můžete dokončit nastavení sandboxového prostředí.

   > [!NOTE]
   > Pokud jsou ve Vašem prohlížeči blokována vyskakovací okna, povolte je pro URL adresu * .businesscentral.dynamics.com.

Když je prostředí sandboxu připravené, budete přesměrováni do uvítacího průvodce prostředím sandboxu.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Můžete vybrat tlačítko **Číst více** a přečíst si scénáře pro vývojáře, které můžete vyzkoušet v sandboxovém prostředí, nebo vybrat tlačítko **Zavřít** a pokračovat do Centra rolí instance [!INCLUDE[d365fin](includes/d365fin_md.md)] vašeho sandboxového prostředí.

V horní části centra rolí se zobrazí upozornění, které vás informuje, že se jedná o sandboxové prostředí. Můžete také zobrazit typ prostředí v záhlaví klienta.
<!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Sandboxové prostředí je vytvořené tímto způsobem obsahuje pouze výchozí demonstrační data pro společnost CRONUS. Z produkčního prostředí nejsou kopírována ani jinak přenášena žádná data.<br /><br />
> Můžete také vytvořit sandboxové prostředí obsahující produkční data. To musíte udělat prostřednictvím centra pro správu. Pro více informací navštivte nápovědu [Správa prostředí](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  v sekci Vývojář a IT-Pro.

Kdykoli se můžete vrátit na stránku **Prostředí Sandbox** a prostředí obnovit. 

> [!NOTE]
> Obnovení sandboxového prostředí jej zcela odstraní a poté jej znovu vytvoří s výchozími ukázkovými daty.

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Správce může omezit nebo dokonce zablokovat přístup některých uživatelů k sandboxovému prostředí. To lze provést pomocí standardních bezpečnostních funkcí produktu, jako je Karta uživatele, skupiny uživatelů a sady oprávnění. Pro více informací navštivte <x13/>Přiřazení oprávnění uživatelům a skupinám<x14/>.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## Pokročilé funkcionality Sandboxového prostředí

Sandboxové prostředí je v neposlední řadě užitečné, protože obsahuje několik praktických funkcí.

### Návrhář

V prostředí sandboxu najdete povolenou funkci **Návrh**. Navrhování můžete aktivovat na stránce výběrem ikony ![Návrh](./media/across-sandbox/sandbox-inclient-design-icon.png), nebo zvolením položky menu **Návrh** v menu ![Nastavení](media/ui-experience/settings_icon_small.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### Povolení pokročilého uživatelského prostředí
Je možné povolit a vyzkoušet plnou funkčnost standardní verze [!INCLUDE[d365fin](includes/d365fin_md.md)] v klientovi prostředí sandboxu nastavením pole**Zkušenost** na stránce **Informace o společnosti**.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Po povolení uživatelského prostředí *Premium* dostáváte přístup ke všem standartním profilům (rolím) a centru rolí jako ve standartní verzi. Můžete také vytvořit zkušební společnost, která je plně nastavena, včetně demonstračních dat a přístupu k pokročilým oblastem produktu. Případně se obraťte na prodejního partnera, který vám předvede možnosti. Pro více informací navštivte [Jak najdu obchodního partnera?](across-faq.md#findpartner).

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## Viz také

[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Zkušební verze a předplatné](across-preview.md)  
[Správa prostředí Business Central v centru pro správu ](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)
