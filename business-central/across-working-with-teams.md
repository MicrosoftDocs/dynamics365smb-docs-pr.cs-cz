---
title: Sharing Business Central Records in Microsoft Teams
description: Learn how to use the Business Central app for Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
---

# Sharing Business Central Records in Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] nabízí aplikaci, která propojuje Microsoft Teams s vašimi obchodními daty v  [!INCLUDE [prod_short](includes/prod_short.md)], abyste mohli rychle sdílet podrobnosti mezi členy týmu a rychleji reagovat na dotazy. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

## Přehled

Aplikace [!INCLUDE [prod_short](includes/prod_short.md)] Vás nechá:

- Kopírovat odkaz na jakýkoli záznam Business Central a vložte jej do konverzace Teams, kterou chcete sdílet se svými spolupracovníky. Aplikace poté rozšíří odkaz na kompaktní interaktivní kartu, která zobrazuje informace o záznamu.
- Jakmile jste v konverzaci,  tak vy a vaši spolupracovníci můžete zobrazovat další podrobnosti o záznamu, upravit data a podniknout kroky - aniž byste opustili Teams.

[![Teams integrace s Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## Předpoklady

- Máte přístup do Microsoft Teams.
- Nainstalovali jste aplikaci [!INCLUDE [prod_short](includes/prod_short.md)] v Teams. Více informací naleznete v [Instalace aplikace [!INCLUDE [prod_short](includes/prod_short.md)] pro Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Všichni účastníci konverzace v Teams si budou moci prohlédnout karty záznamů Business Central, které do konverzace odešlete. Chcete-li zobrazit více podrobností o záznamech pomocí **Detaily** nebo **Vyskakovacího okna** na katě, musíte mít přístup do [!INCLUDE [prod_short](includes/prod_short.md)]. Pro více informací navštivte [Správa integrace Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).

## Zahrnutí karty Business Central do konverzace Teams

1. Přihlašte se do [!INCLUDE [prod_short](includes/prod_short.md)] pomocí Vašeho prohližeče.
2. Otevřete záznam, který chcete sdílet.

   Aplikace je navržena tak, aby zobrazovala stránky typu karta z [!INCLUDE [prod_short](includes/prod_short.md)]. Otevřete stránku, která zobrazuje jeden záznam, například Zboží, Zákazníka nebo Pprodejní objednávku. Nelze jej použít pro centra rolí nebo stránky, které zobrazují několik záznamů v seznamu.

3. Zkopírujte celou adresu URL z adresního řádku prohlížeče.

   ![Kopírování URL Business Central z prohlížeče](media/teams-url-v2.png)
4. Přejděte do Teams a začněte konverzaci, pomocí které můžete chatovat s osobou, skupinou osob nebo týmovám kanálem.

   <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Vložíte URL adresu do okna se zprávou, kde ji píšete.

   ![Vložení URL Business Central do Teams](media/teams-paste-url-v2.png)
6. Při prvním vložení odkazu do konverzace budete požádáni, abyste se přihlásili k [!INCLUDE [prod_short](includes/prod_short.md)] a udělili aplikaci souhlas k načtení dat. Postupujte podle pokynů na obrazovce.

   > [!NOTE]
   > Tento krok budete muset udělat pouze jednou.

7. Chvilku počkejte, než se karta vygeneruje v okně se zprávou.

8. Když se karta zobrazí, před odesláním zprávy pečlivě zkontrolujte její obsah, zda neobsahuje citlivé informace. Tento krok je důležitý, protože jakmile zprávu odešlete, všichni v konverzaci kartu uvidí.

9. Pokud karta vypadá dobře, pomocí **Odeslat** ji přidáte do konverzace.

   > [!TIP]
   > Jakmile se karta objeví a před tím, než zvolíte **Send** můžete smazat URL, které jste vložili.

10. Chcete-li zobrazit další podrobnosti nebo provést změny záznamu zobrazeném na kartě, vyberte možnost **Podrobnosti**. Další informace naleznete v následující části.

## Zobrazení podrobností karty

Po odeslání karty do konverzace mohou všichni účastníci se [správnými oprávněními](admin-teams-integration.md#permissions) vybrat **Detaily** a otevřít okno, které zobrazuje další informace o záznamu a případně provést změny záznamu. Nezáleží na tom, jestli jste ten, kdo kartu posílá, nebo ten, kdo kartu přijímá. Funkce **Podrobnosti** je obzvláště užitečná pro příjemce, protože jim rychle poskytuje stručné a cílené informace o záznamu, na rozdíl od toho, že musí zobrazovat celý záznam.

Okno podrobností je podobné tomu, co byste viděli v záznamu [!INCLUDE [prod_short](includes/prod_short.md)]. Ale pro Teams je to trošku ořezáné. Až dokončíte prohlížení a provádění změn, zavřete okno a vraťte se do konverzace Teams.

Při práci s údaji na kartě je na paměti několik věcí:

- K otevření karty musí mít uživatelé oprávnění ke stránce a jejím údajům v [!INCLUDE [prod_short](includes/prod_short.md)].
- Karty v chatu Teams se automaticky neaktualizují podle změn. Všechny změny, které provedete na záznamu v okně podrobností, jsou uloženy v  [!INCLUDE [prod_short](includes/prod_short.md)]. Karta v Teams nezobrazí změn v konverzaci, dokud nevložíte odkaz znovu.

Další informace o práci s kartami a jejich údaji naleznete v [Teams FAQ](teams-faq.md).

## Viz také

[Přehled integrace Business Central a Microsoft Teams](across-teams-overview.md)  
[Instalace aplikace [!INCLUDE [prod_short](includes/prod_short.md)] pro Microsoft Teams](across-install-app-for-teams.md)  
[Teams FAQ](teams-faq.md)  
[Řešení problémů Teams](admin-teams-troubleshooting.md)  
[Vývoj pro integraci Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]