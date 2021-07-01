---
title: Troubleshooting Microsoft Teams Integration
description: Learn about what you can do as an administrator to control Microsoft Teams integration.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 04/12/2021
ms.author: jswymer
---

# Odstraňování problémů s integrací Microsoft Teams a [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Tento článek obsahuje informace o tom, jak identifikovat a opravit problémy, ke kterým může dojít při používání Microsoft Teams s [!INCLUDE [prod_short](includes/prod_short.md)] jako typický uživatelem nebo správcem.

## Přihlašovací odkaz nefunguje

Pokud se pokusíte přihlásit k aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams ihned po instalaci aplikace a přihlašovací odkaz nereaguje, může to být proto, že aplikace ještě nedokončila úplně instalaci. Pokud se chcete problém pokusit vyřešit, odhlaste se z klienta Teams a pak se znovu přihlaste.

## Stránka Nastavení je prázdná

Chcete-li dosáhnout nastavení, musíte se nejprve přihlásit. Chcete-li se do aplikace přihlásit, vložte odkaz záznamu v [!INCLUDE [prod_short.md](includes/prod_short.md)] nebo zkuste vyhledat kontakty. Obě tyto akce vás povedou k přihlašení, po kterém můžete jít na stránku **Nastavení**.

## Změnil jsem společnost, ale nezdálo se mi, že by to fungovalo

Po změně společnosti na stránce **Nastavení** si můžete všimnout, že rozbalovací seznam příkazového pole označuje, že stále hledáte v předchozí společnosti. K tomuto problému dochází, když otevřete stránku **Nastavení** přímo z příkazového pole. V tomto případě byla společnost úspěšně změněna a ve skutečnosti budete vyhledávat ve společnosti, na kterou jste se přepli. Problém je v tom, že rozevírací seznam příkazového pole ještě nebyl aktualizován. Rozbalovací nabídka přesně odráží společnost, ve které budete hledat, zavírat nebo odepínat [!INCLUDE [prod_short.md](includes/prod_short.md)] z příkazového pole, a poté znovu otevřete aplikaci.


<!--When you change company from the **Settings** page that you reach from the command box, returning to the command box drop-down continues to show the previous company even though the company was successfully changed. For the drop-down accurately reflect the company you'll search in, you must close or unpin [!INCLUDE [prod_short.md](includes/prod_short.md)] from the command box and then find it again.-->

## Při hledání kontaktů došlo k chybě „Něco se pokazilo“

K této chybě může dojít při hledání ve společnosti, která nebyla inicializována nebo nereaguje. Například nemůžete hledat v nové zkušební společnosti, ve které dosud nebyly přijaty podmínky použití. Chcete-li tento problém vyřešit, pokuste se přihlásit k webovému klientu [!INCLUDE [prod_short.md](includes/prod_short.md)] a proklikejte všechna dialogová okna, která se zobrazí.

## Při hledání kontaktů došlo k chybě „Nelze najít rozhraní API kontaktů/souhrných kontaktů“

Tento problém může být způsoben přizpůsobením nebo průmyslovými řešeními, která ovlivňují nebo upravují [!INCLUDE [prod_short.md](includes/prod_short.md)] nebo neposkytují rozhraní API pro kontakty nebo souhrné kontakty. Pokud problém přetrvává, obraťte se na správce nebo partnera, který poskytuje podporu.

## Žádný z mých odkazů se nerozbalí na kartu

Pokud máte tento problém, je třeba vyzkoušet několik věcí:

1. Nejprve se ujistěte, že aplikace [!INCLUDE [prod_short](includes/prod_short.md)] pro Teams nainstalovaná.

   Chcete-li to zkontrolovat, přihlaste se k desktopové aplikaci Teams nebo Teams v prohlížeči. Pak na levé straně vyberte **Aplikace**nebo vyhledejte **[!INCLUDE [prod_short](includes/prod_short.md)]**. Když najdete aplikaci **[!INCLUDE [prod_short](includes/prod_short.md)]**, vyberte ji a otevřete stránku s podrobnostmi o aplikaci. Pokud je zobrazeno tlačítko **Přidat pro mě**, pak aplikace [!INCLUDE [prod_short](includes/prod_short.md)] není naistalovaná. Další informace o instalaci aplikace naleznete v tématu [Instalace aplikace [!INCLUDE [prod_short](includes/prod_short.md)] pro Microsoft Teams](across-install-app-for-teams.md).

   > [!NOTE]
   > Hostující uživatelé nemohou ihned instalovat aplikaci. Další informace o uživatelích typu host najdete v nejčastějších dotazech v tématu spolupráci s hosty.

2. Dále zkontrolujte, zda jste se přihlásili se správnou identitou.

   V Teams přejděte na libovolný chat a v poli pro psaní zpráv klikněte pravým tlačítkem myši na ikonu [!INCLUDE [prod_short](includes/prod_short.md)] a zvolte **Nastavení**. Když se zobrazí okno, zkontrolujte, zda se uživatel, který říká, že jste připojeni, shoduje s tím, co používáte pro připojení k [!INCLUDE [prod_short](includes/prod_short.md)].

3. Ujistěte se, že proedura 2718 **Page Summary Provider** je vypublikovaná jako webová služba.

   Teams se připojí k [!INCLUDE [prod_short](includes/prod_short.md)] pomocí koncového bodu k této procedury ve službě [!INCLUDE [prod_short](includes/prod_short.md)] service. Informace o publikování webových služeb naleznete v tématu [Publikování Webové Služby](across-how-publish-web-service.md).

4. Vaše organizace může také omezit vkládání odkazů, které se rozbalují na karty. Obraťte se na správce k porozumění zásadám organizace Teams, které se na vás mohou vztahovat.

## Můj odkaz se někdy nerozbalí na kartu

Odkaz se nerozbalí na kartu v následujících situacích:

- Odkaz cílí na stránku, která (na technické úrovni) není připojena ke zdrojové tabulce v [!INCLUDE [prod_short](includes/prod_short.md)]. Můžete zkontrolovat, zda má stránka zdrojovou tabulku, pomocí podokna kontroly stránky ve webovém klientovi v [!INCLUDE [prod_short](includes/prod_short.md)]. Další informace o kontrole stránek najdete v tématu [Prohlížení dat stránky](across-inspect-page.md).
- Teams nepodporuje náhledy odkazů v některých jeho funkcích. Například když vyskočíte z chatu nebo jste hostem jiné organizace.
- Teams se na pozadí vzdají pokusu o zobrazení karty po 15 sekundách, například kvůli problémům se sítí.
- Teams nemusí rozšířit odkaz, pokud jste již vložíly odkaz do stejného pole pro psaní zpráv a kartu jste již odstranili.

Odkaz musí také obsahovat všechny potřebné informace k vyhledání záznamu a zobrazení odpovídající karty. Tyto informace zahrnují:

- Název prostředí jeho, včetně URL cesty. Pokud nezadáte název prostředí, Teams předpokládá, že se pokoušíte dostat do prostředí "Produkčního".
- Název společnosti pomocí parametru *company=*
- Identifikátor stránky pomocí parametru *page=* 
- Záložka záznamu pomocí parametru *bookmark=* 

Například:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Technické podrobnosti o URL adresách [!INCLUDE [prod_short](includes/prod_short.md)] bežte na [Web Client URL](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) v [!INCLUDE [prod_short](includes/prod_short.md)] Developer a IT Pro Help.

## Otevře se okno s podrobnostmi, ale před zobrazením podrobností se zobrazí chyba

Tento problém může být způsoben několika věcmi: nedostatkem oprávnění v [!INCLUDE [prod_short](includes/prod_short.md)] nebo nastavením prohlížeče (když používáte Teams ve webovém prohlížeči).

1. Ověřte svá oprávnění v [!INCLUDE [prod_short](includes/prod_short.md)].

   Chcete-li zobrazit podrobnosti karty, [!INCLUDE [prod_short](includes/prod_short.md)] zkontroluje vaši licenci a oprávnění k zobrazení konkrétního záznamu a stránky v konkrétní společnosti a prostředí. Pokud nemáte oprávnění pro žádnou z těchto věcí, zobrazí se v okně podrobností standardní [!INCLUDE [prod_short](includes/prod_short.md)] chybové zprávy o oprávněních.

   Další informace o oprávněních naleznete v tématu [Přiřazení práv uživatelům a uživatelským skupinám](ui-define-granular-permissions.md)

2. Pokud používáte Teams v prohlížeči, zkontrolujte nastavení prohlížeče.

   - Blokování automaticky otevíraných okna v prohlížeči musí být vypnuto nebo nastaveno tak, aby umožňovaly automaticky otevíraná okna z domén *businesscentral.dynamics.com* nebo *bc.dynamics.com*. Informace o povolení vyskakovacích oken pro [!INCLUDE [prod_short](includes/prod_short.md)], najdete v [Nastavení Vašeho prohližeče](across-browser-settings.md#popup).
   - Váš prohlížeč musí mít při práci přístup k místnímu úložišti prohlížeče pro soubory cookies a předvolby.
   - Pokud to není nutné, nepoužívejte hostování ani anonymní prohlížení, protože v některých prohlížečích zahodí nebo zablokuje určitý obsah.

   Další informace o minimálních požadavcích prohlížeče naleznete v tématu [Minimální požadavky pro používání [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers)

## Mám problémy s kamerou nebo lokací v Teams

Při použití funkcí [!INCLUDE [prod_short](includes/prod_short.md)] v okně podrobností, které vyžadují přístup k vaší poloze nebo kameře zařízení, musíte nejprve udělit souhlas s přístupem k těmto možnostem zařízení.

- U Teams v prohlížeči se ujistěte, že nastavení prohlížeče umožňuje přístup ke kameře a umístění pro https://teams.microsoft.com.

- U Teams pro iOS nebo Android se ujistěte, že nastavení vašeho zařízení umožňuje přístup k fotoaparátu a umístění pro mobilní aplikaci Teams.

Nápovědu ke změně těchto nastavení najdete v [Nefunguje mi kamera v Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) na stránkách podpory Microsoft.

Aplikace [!INCLUDE [prod_short](includes/prod_short.md)] nepodporuje informace o poloze v desktopové aplikaci Teams. Další informace o poloze najdete v [Nejčastějších dotazech Teams](teams-faq.md#location).

Některé prohlížeče, například nový Microsoft Edge, Vám umožňují zvolit, kterou kameru zařízení použít, když vaše zařízení podporuje více kamer.

## Teams zobrazuje pro mé karty podrobností a karty smíšené jazyky

Aby se karty a údaje o kartě zobrazovaly konzistentně ve stejném jazyce v Teams, jazyk vašeho klienta Teams a jazyk, který používáte ve webovém klientu [!INCLUDE [prod_short](includes/prod_short.md)] musí být stejný. 

- Další informace o změně jazyka v Teams najdete v tématu [Změna nastavení v Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) na stránkách podpory Microsoft.

- Další informace o změně jazyka v [!INCLUDE [prod_short](includes/prod_short.md)] naleznete v  [Změna základního nastavení - Jazyky](ui-change-basic-settings.md#language).

Další informace o tom, jak jazyky fungují mezi Teams a [!INCLUDE [prod_short](includes/prod_short.md)], najdete v [Nejčastěji pokládané otázky a odpovědi Teams](teams-faq.md#language).

## Upravil jsem pole v okně podrobností, ale moje změna nebyla uložena

Změny provedené v poli v podrobných oknech se automaticky uloží, když pole opustíte. Před zavřením okna po změně pole nezapomeňte stisknout klávesu Tab nebo kliknout/klepnout mimo pole.

## Ve spouštěči aplikace se objevila nová dlaždice. Jak ji odstraním?

Když si prohlížíte své aplikace na domovské stránce Office 365 (https://home.office.com) nebo ve spouštěči aplikací, po instalaci "Business Central Teams Integration Service Connector" se objeví aplikace [!INCLUDE [prod_short](includes/prod_short.md)] pro Teams. Tato dlaždice sama o sobě neposkytuje žádnou hodnotu a lze ji bezpečně skrýt.

Jako správce, který má oprávnění správce Azure Active Directory, můžete dlaždici skrýt provedením následujících kroků:

1. Přihlaste se do [Centra pro správu Azure Active Directory](https://aad.portal.azure.com/).
2. Vyberte **Enterprise apps**, a poté zvolte **Business Central Teams Integration Service Connector**.
3. Vyberte **Vlastnosti**, a poté nastavte **Viditelné uživatelům** na **Ne**.
4. Zvolte **Uložit**.

> [!NOTE]
> Než se tato změna projeví, bude to chvíli trvat.


## Viz také

[[!INCLUDE [prod_short](includes/prod_short.md)] and Microsoft Teams Integration Overview](across-teams-overview.md)  
[Instalace aplikace [!INCLUDE [prod_short](includes/prod_short.md)] pro Microsoft Teams](across-install-app-for-teams.md)  
[Teams FAQ](teams-faq.md)  
[Vývoj pro integraci Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]