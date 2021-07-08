---
title: Manage user settings and preferences as the administrator
description: Manage user settings and preferences in Dynamics 365 Business Central.
author: sorenfriisalexandersen

ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 04/01/2021
ms.author: soalex

---
# Správa předvoleb a uživatelských nastavení

Jako správce můžete konfigurovat uživatelská nastavení v [!INCLUDE[prod_short](includes/prod_short.md)], podobně jako jednotliví uživatelé mohou spravovat své vlastní předvolby na stránce **Má nastavení** page.

Získejte přehled o všech uživatelích na přehledu **Uživatelé** a změňte jednotlivá nastavení výběrem funkce **Uživatelská nastavení** pro příslušného uživatele

> [!TIP]
> Seznam **Nastavení uživatelů** zobrazuje aktuální nastavení pro každého uživatele. Chcete-li zobrazit nebo upravit jednotlivé uživatele, vyberte talčítko **Zobrazit** nebo **Upravit**.

Stránka **Karta nastavení uživatelů** je podobný jako stránka **Má nastavení**, ke které má každý uživatel přístup, a je to výkonný nástroj pro vás jako správce například pro nastavení výchozího nastavení a vymazání přizpůsobených stránek.

## Typy uživatelských nastavení

*Uživatelská nastavení* nejsou stejná jako *Nastavení uživatelů*, které se týká uživatele jako entity a přístupu uživatele do systému. Uživatelské nastavení navíc nemá nic společného s přizpůsobením uživatele, jako jsou například lehké změny uživatelského rozhraní. Uživatelská nastavení určují předdefinovaná nastavení pro každého uživatele v různých aspektech způsobu, jakým se mu aplikace prezentuje. Následující odstavec uvádí pět typů uživatelských nastavení a předvoleb, které může nastavit jednotlivec nebo centrálně správce:

- **Společnost**

   Toto nastavení určuje společnost, ke které se má uživatel přihlásit při příštím přihlášení. Uživatel může mít přístup k více společnostem a může být aktivní v několika společnostech.

- **Role**

   Role nebo profil popisuje funkci uživatele ve společnosti, například *Manažer prodeje*, *Účetní* nebo *Nákupčí*. Profil pak určuje centrum rolí uživatele - domovskou stránku, kterou uživatelé uvidí při přihlášení. Profil nemá vliv na přístupová práva k funkcím v [!INCLUDE[prod_short](includes/prod_short.md)].

- **Jazyk**

   Definuje jazyk aplikace, který [!INCLUDE[prod_short](includes/prod_short.md)] zobrazuje texty, popisy a chybové hlášky. Pokud jsou uživatelé [!INCLUDE[prod_short](includes/prod_short.md)] synchronizováni z Microsoft 365, použije se jazykové nastavení z Microsoft 365 za předpokladu, že uživatel chce použít stejné nastavení v produktech Office a [!INCLUDE[prod_short](includes/prod_short.md)]. Správce může změnit výchozí nastavení a každý uživatel si může vybrat mezi dostupnými jazyky na stránce Moje nastavení. Po provedení další synchronizace, se hodnoty resetují dle Microsoft 365.

   Pokud se jazykové nastavení z Microsoftu 365 shoduje s podporovaným jazykem v [!INCLUDE[prod_short](includes/prod_short.md)], bude pro uživatele zvolen tento jazyk.

   > [!NOTE]
   > Možná budete muset nainstalovat jazykovou vrstvu pro [!INCLUDE[prod_short](includes/prod_short.md)], aby se jazyk mohl správně zobrazit.
   >  Proto je dobrým zvykem instalovat nezbytné jazykové aplikace před tím, než se jakýkoli uživatel přihlásí poprvé, aby měl dobrý zážitek z prvního dne. Další informace naleznete v seznamu  [podporované jazyky](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).

- **Oblast**

   Definuje způsob, jakým jsou data a čísla prezentována v klientu [!INCLUDE[prod_short](includes/prod_short.md)] například zda použít evropské nebo americké formáty data nebo jak zobrazit desetinné znaménko a oddělovače tisíců v částkách. If [!INCLUDE[prod_short](includes/prod_short.md)] users are synchronized from Microsoft 365, the regional settings from Microsoft 365 are used, assuming that the user wants to use the same settings in Office products and [!INCLUDE[prod_short](includes/prod_short.md)]. Správce nebo uživatel může tato nastavení změnit ručně v aplikaci [!INCLUDE[prod_short](includes/prod_short.md)], ale po provedení další synchronizace se obnoví na hodnotu z Microsoft 365.

- **Časové pásmo**

   Definuje časové pásmo, ve kterém se uživatel nachází. V současné době to není synchronizováno z Microsoft 365 a musí být nastaveno ručně.

- **Výukové tipy**

   [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]  Jako administrátor můžete vypnout výukové tipy pro všechny uživatele, například když právě připojujete uživatele, kteří již [!INCLUDE [prod_short](includes/prod_short.md)] znají.

> Pokud je synchronizace uživatelů Microsoft 365 provedena v době, kdy jsou uživatelé přihlášeni do [!INCLUDE[prod_short](includes/prod_short.md)], musí tito uživatelé obnovit prohlížeč nebo se odhlásit a znovu přihlásit do [!INCLUDE[prod_short](includes/prod_short.md)], aby viděli případný jiný jazyk nastavený synchronizační akcí.

## Přehled všech změn specifických pro uživatele

Jako správce můžete získat přehled o jednotlivých změnách v [!INCLUDE [prod_short](includes/prod_short.md)], které mohl každý uživatel provést na různých stránkách v [!INCLUDE [prod_short](includes/prod_short.md)]. Jakmile uživatelé provedou změny ve svých prostředích v [!INCLUDE [prod_short](includes/prod_short.md)], tyto změny se projeví v seznamu **Přizpůsobení uživatele**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## Kontrola nebo odstranění individuálních nastavení uživatelů

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "Hledat ikonu stránky nebo sestavy"), zadejte **Přizpůsobené stránky** a poté vyberte související odkaz.
2. Zobrazí se seznam uživatelů a jejich přizpůsobené stránky. Chcete-li vymazat personalizaci uživatele, klikněte na příslušný řádek nebo zvolte **Spravovat**a poté zvolte **Odstranit**.

Tím se odstraní přizpůsobení a uživatelské prostředí příslušné stránky se vrátí do výchozího stavu.

## Viz také

[Příprava na podnikání](ui-get-ready-business.md)  
[Dostupnost pro jednotlivé země a regiony a podporované jazyky](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Změna jazyka a oblasti](about-locale-language.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
