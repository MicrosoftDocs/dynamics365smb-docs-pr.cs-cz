---
title: Teams FAQ
description: Get answers for some typical questions about working with Teams and Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors
ms.date: 05/19/2021
ms.author: jswymer
---
# Teams Nejčastěji pokládané otázky a odpovědi

[!INCLUDE [online_only](includes/online_only.md)]

Tento článek odpovídá na některé z vašich otázek ohledně práce s Teams a [!INCLUDE [prod_short](includes/prod_short.md)].

## [Obecné](#tab/general)

### Jak se přihlásím k aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] v Teams?

Po instalaci aplikace budete požádáni o přihlášení při prvním použití, když vložíte odkaz z [!INCLUDE [prod_short.md](includes/prod_short.md)] do chatu Teams nebo při volbě tlačítka **Detaily** na kartě v Teams. V závislosti na vašem klientovi Teams možná budete muset zadat své přihlašovací údaje, které používáte pro přístup do [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Jak se odhlásím z aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] v Teams?

Chcete-li se odhlásit ze své aktuální identity uživatele v Teams použitých k připojení k [!INCLUDE [prod_short.md](includes/prod_short.md)], přejděte do libovolného pole pro psaní chatu, klikněte pravým tlačítkem dole na ikonu [!INCLUDE [prod_short.md](includes/prod_short.md)] a poté zvolte **Nastavení**. Po zobrazení okna zkontrolujte aktuálně přihlášenou identitu a zvolte **Odhlásit**.

### Připojuje se aplikace pro Teams k [!INCLUDE [prod_short.md](includes/prod_short.md)] on premises?

Ne.  Aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams pracuje pouze s [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Neexistují žádné plány na podporu [!INCLUDE [prod_short.md](includes/prod_short.md)] pro &mdash; on-premises, hybrid cloud nebo privátní cloud&mdash;, který společnost Microsoft přímo nehostuje ani nespravuje

### Funguje aplikace s více společnostmi a prostředími?

Ano. Chcete-li vyhledat kontakty v jiné společnosti, přejděte do [Nastavení](across-teams-settings.md). Když aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] rozbalí odkaz na kartu, odkaz musí obsahovat prostředí a názvy společností aplikace, aby odpovídaly záznamu ve správné společnosti. Můžete vložit odkazy na jakékoli společnosti a prostředí, ke kterým máte ve své organizaci přístup a z účtu [!INCLUDE [prod_short.md](includes/prod_short.md)], který jste použili k přihlášení. Účastníkům chatu se karta zobrazí. Nemohou však zobrazit podrobnosti o kartě, pokud nemají oprávnění pro společnost nebo prostředí, kde je tento záznam uložen.

### Ve kterých zemích nebo regionech je aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] k dispozici?

Aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro není omezena podle země nebo regionu. Aplikace je k dispozici na všech trzích, které aktuálně podporuje Teams marketplace.

### Funguje aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] s jakoukoli lokalizací [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Ano. Aplikace je určena pro práci s jakoukoli lokalizací [!INCLUDE [prod_short.md](includes/prod_short.md)], ať už je tato lokalizace nabízena přímo od Microsoftu nebo prostřednictvím partnera. Pro více informací navštivte [Dostupnost Země/Oblasti a podporované jazyky](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="language"></a>Jaký jazyk aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] podporuje?

Jazyk používaný pro karty a detaily karet v Teams určují dvě věci:

1. Váš jazyk v Teams, který můžete vidět z nastavení účtu v Teams.
2. Váš jazyk v [!INCLUDE [prod_short.md](includes/prod_short.md)], který můžete videt ve webovém klientu [!INCLUDE [prod_short.md](includes/prod_short.md)] (Bežte na [Změna základního nastavení - Jazyk](ui-change-basic-settings.md#language)).

Následující tabulka vysvětluje, jak se prostředí liší pro autory a příjemce zpráv v závislosti na jazykovém nastavení a dostupnosti jazyků.

|Kdo|Karta|Detaily karty|
|-|----|--------------|
|Autor zprávy|Zobrazuje se v jazyku, který je pro Vás nastaven v Teams. Pokud [!INCLUDE [prod_short.md](includes/prod_short.md)] nenabízí stejný jazyk, karta se zobrazí v angličtině. |Zobrazí se v jazyce, který je pro vás nastaven v [!INCLUDE [prod_short.md](includes/prod_short.md)].  Můžou zde být zahrnuté jazyky poskytnuté partnery |
|Adresát zprávy |Zobrazuje se v jazyce autora zprávy. |Zobrazí se v jazyce, který je pro vás nastaven v [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Pro seznam podporovaných jazyků pro [!INCLUDE [prod_short.md](includes/prod_short.md)], bežte na [Podporované jazyky](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### Podporuje aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] práci s průmyslovými řešeními?

Ano. Jen pouze některé funkce aplikace fungují s [Vloženými aplikacemi](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview):

- Aplikace pracuje s odkazy založenými na **\*.bc.dynamics.com**, které se obvykle používají ve Vložených aplikacích.
- Vyhledávání kontaktů není k dispozici pro vložené aplikace, které nahrazují základní aplikaci od společnosti Microsoft.

### Kde můžu najít integraci Teams ve webovém klientu [!INCLUDE [prod_short.md](includes/prod_short.md)]?

V současné době není do webového klienta [!INCLUDE [prod_short.md](includes/prod_short.md)] možné vkládat ovládací prvky Teams nebo jeho funkce.

### Pracuje [!INCLUDE [prod_short.md](includes/prod_short.md)] s mobilní aplikací Teams?

Ano. Aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] lze nainstalovat z desktopové aplikace nebo prohlížeče Teams nebo administrátorem pro všechny uživatele. Po instalaci je aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] automaticky dostupná v Teams pro iOS a Android. Na mobilních zařízeních můžete v mobilní aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] zobrazit pouze karty odeslané ostatními, přistupovat k detailům karty nebo kartu otevřít. Nelze vkládat odkazy, které se při psaní zprávy nebo hledání kontaktů rozbalí na karty. Minimální požadavky na mobilní zařízení naleznete v [Minimální požadavky na používání Business Central](product-requirements.md).

### Je aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams stejná jako aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro iOS a Android?

Ne.  Aplikace pro Teams je doplňkem Microsoft Teams a je určena výhradně pro prostředí spolupráce, která se v Teams rozvíjí. Na druhou stranu mobilní aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] poskytuje bohaté prostředí pro práci s daty [!INCLUDE [prod_short.md](includes/prod_short.md)] na vašich mobilních zařízeních.

Uživatelům mobilních zařízení se doporučuje, aby si nainstalovali mobilní aplikaci i desktopovou aplikaci Teams, aby z [!INCLUDE [prod_short.md](includes/prod_short.md)] vytěžili maximum. S oběma nainstalovanými můžete zvolit **Vyskakovací okno** na kartě v Teams a otevřít podrobnosti o kartě v mobilní aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)]. pro více informaí o instalaci [!INCLUDE [prod_short.md](includes/prod_short.md)] a mobilní aplikaci Teams, bežte na:

- [Získání Business Central pro mobilní zařízení](install-mobile-app.md)
- [Získání mobilní aplikace Teams](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) na stránkách podpory Microsoftu

### Funguje aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] se všemi Teams klienty?

Ne.  Aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams není podporována, pokud je nainstalována jako balíček pro macOS nebo Linux. Na těchto platformách můžete místo toho přistupovat k Teams pomocí podporovaného prohlížeče.

Pro minimální požadavky na [!INCLUDE [prod_short.md](includes/prod_short.md)], bežte na [Minimální požadavky na používání Business Central](product-requirements.md#teams).

Informace o výběru klientů Teams a o tom, jak je nainstalovat, najdete v tématu [Získání klientů pro Microsoft Teams](/microsoftteams/get-clients) v dokumentaci Teams.

### Který klient Teams je nejlepší pro [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Mezi klienty Teams existují pouze drobné rozdíly a omezení, které mohou ovlivnit vaši práci s aplikací [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams. Při výběru klienta Teams berte v úvahu:

- Ke kameře a umístění nelze získat přístup z okna detailů v desktopové aplikaci Teams.
- Telefonní čísla se nemůžou aktivovat z okna detailu v Teams pro iOS, Teams pro Android nebo Teams v prohlížeči.
- Pomocí Microsoft Edge s Teams (v prohlížeči) můžete snadno pracovat napříč s více účty přihlášením do Teams z různých profilů. Další informace o používání profilů v Microsoft Edge najdete v [Přihlášení a vytvoření více profilů v Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) na stránkách podpory Microsoft.

### Jaký je nejlepší způsob, jak demonstrovat [!INCLUDE [prod_short.md](includes/prod_short.md)] a Microsoft Teams potencionálním zákazníkům?

Pokud jste prodejním partnerem, možná budete chtít mít prostředí, na kterém můžete ukazovat předprodejní ukázky. Abyste se vyhnuli zásahu do Microsoft Teams ve vaší organizaci, můžete získat demo účet Microsoft 365 na [https://aka.ms/CDX](https://aka.ms/CDX). Tento účet vám poskytuje plnou kontrolu nad nezávislou organizací Azure, která zahrnuje Microsoft Teams a [!INCLUDE [prod_short.md](includes/prod_short.md)]. Pro více informací navštivte [Příprava demonstračních prostředí Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### Zajišťuje aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams mé úpravy a přizpůsobení?

Aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams může zobrazit karty pro odkazy na stránky zákazníků a tabulky v [!INCLUDE [prod_short.md](includes/prod_short.md)], například stránky a tabulky pocházející z vlastních rozšíření nebo z AppSource

Na pole zobrazená na kartě v Teams mohou mít vliv také [!INCLUDE [prod_short.md](includes/prod_short.md)] přizpůsobení nainstalované pro vaší organizaci. Karty nezohledňují žádná přizpůsobení specifická pro roli nebo personalizaci uživatele. Okno s podrobnostmi o kartě však zobrazuje podrobnosti o záznamu tak, jak byste je viděli v [!INCLUDE [prod_short.md](includes/prod_short.md)],včetně všech rozšíření, přizpůsobení rolí a přizpůsobení uživatelů.

Při hledání kontaktů nejsou pole přizpůsobená v tabulce **Kontakty** a pole zobrazená ve výsledcích vyhledávání nijak ovlivněna žádným přizpůsobením ani přizpůsobením.

### Jak oprávnění požadovaná aplikací ovlivňují mé soukromí?

Před instalací aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams, můžete zkontrolovat minimální oprávnění požadovaná pro fungování aplikace. Instalací aplikace souhlasíte s tím, že aplikace má oprávnění přijímat zprávy a data, která mu poskytnete a Teams má oprávnění tyto zprávy ukládat a zpracovávat.

Také některé funkce [!INCLUDE [prod_short.md](includes/prod_short.md)] vyžadují otevření externích odkazů, přístup ke kameře nebo zeměpisné údaje o poloze. Předpokládejme například, že chcete vytvořit fotografii nákupní faktury k následnému zpracování. Aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)]tyto funkce bez vašeho souhlasu nepoužívá a používají je pouze konkrétní funkce v okně **Detaily**. Když poprvé použijete jednu z těchto funkcí, Teams zobrazí dialogové okno s žádostí o udělení přístupu k požadovaným možnostem zařízení.

- V desktopové aplikaci Teams, zkontrolujete a upravíte oprávnění aplikace z okna **Nastavení**. Vyberte svůj profilový obrázek v horní části aplikace a vyberte **Nastavení** > **Oprávnění apliakce** a zvolte aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)].

- U Teams v prohlížeči a Teams pro iOS nebo Android můžete zkontrolovat nebo upravit oprávnění z nastavení prohlížeče nebo zařízení.

> [!NOTE]
> Přesně ty funkce [!INCLUDE [prod_short.md](includes/prod_short.md)], které vás vyzývají k povolení závisí na doplňkových aplikacích a přizpůsobeních použitých v prostředí [!INCLUDE [prod_short.md](includes/prod_short.md)], ke kterému se připojujete.

### Kde se mohu dozvědět o svém soukromí?

Informace o tom, jak společnost Microsoft na zpracovává vaše data, se dozvíte v [Prohlášení o zásadách ochrany osobních údajů společnosti Microsoft](https://go.microsoft.com/fwlink/?linkid=2030602).

Požádejte svého správce, aby zjistil, jak vaše organizace zachází s ochranou osobních údajů.

### Jak odinstalovat aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams?

Chcete-li odebrat aplikaci, kterou jste si nainstalovali sami, přejděte do libovolného pole pro psaní chatu, najděte ikonu [!INCLUDE [prod_short.md](includes/prod_short.md)] klepněte na ni pravým tlačítkem a vyberte **Odinstalovat**.

### Bude Microsoft i nadále vylepšovat aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams?

Ve společnosti Microsoft neustále nasloucháme zpětné vazbě od naší rozmanité komunity uživatelů a jednáme na základě nejlepších návrhů. Další informace o tom, co bude následovat pro aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams, bežte na [Plán vydání Dynamics 365](/dynamics365-release-plan/2021wave1/).

Pokud se chcete podílet na vylepšování aplikace pro Teams nebo máte nápad, který by vám pomohl zjednodušit práci nebo spolupráci v Teams, přidejte nápad nebo hlasujte na [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## [Vyhledávání kontaktů](#tab/contacts)

### Ve kterých tabulkách aplikace vyhledává?

Při hledání kontaktů z aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams, vaše hledané výrazy jsou porovnány se záznamy v tabulce **Kontakty** v [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Ve kterých polích v tabulce kontaktů mohu vyhledávat?

Při psaní hledaných výrazů do vyhledávacího pole jsou termíny porovnány s většinou polí v tabulce **Kontaktů**. Mezi tato pole patří například pole **Číslo**, **Jméno**, **Adresa**, **Telefonní číslo**, **Mobil**, a **Email**.

Search terms aren't matched against any custom fields added to the **Contacts** table by apps and extensions.

### Zahrnují výsledky vyhledávání společnosti a osoby?

Ano. V [!INCLUDE [prod_short.md](includes/prod_short.md)] mohou být kontakty typu **Společnost** nebo **Osoba**, kde může být jedna nebo více osob přidružena ke společnosti. Ve výsledcích vyhledávání mají společnosti a osoby různé ikony.

### Objevují se ve výsledcích kontakty jakéhokoli obchodního vztahu?

Ano. Některé kontakty mohou představovat zákazníky, dodavatele nebo obojí. Další kontakty bez definovaného obchodního vztahu obvykle představují potenciální zákazníky. Kontakty s jinými obchodními vztahy, včetně všech vlastních vztahů, které jste nakonfigurovali v [!INCLUDE [prod_short.md](includes/prod_short.md)], se také zobrazí ve výsledcích hledání.

### Mohu si během schůzky vyhledat kontaktní údaje?

Ano. Během schůzky nebo hovoru v Teams, aniž byste opustili Teams, můžete pro svého zákazníka nebo dodavatele najít kontaktní informace, historii interakcí a související doklady.

Kontaktní údaje můžete ve skutečnosti zobrazit odkudkoli v Teams pomocí příkazového pole. Můžete si například najít kontaktní údaje z kalendáře Teams, které vám pomůžou zakládat schůzky.

### Jak zobrazím své poslední interakce s kontaktem?

Okno podrobností kontaktu zobrazuje položky protokolu interakce. Položky protokolu interakce poskytují historii interakcí, které vaše organizace měla s konkrétním kontaktem. Interakce mohou zahrnovat e-maily, které jste si vyměnili, přijaté hovory nebo doklady, které jste odeslali.

Aby se interakce mohly zobrazovat, [!INCLUDE [prod_short.md](includes/prod_short.md)] musí být nakonfigurován pro sledování interakcí. Další informace o protokolování interakcí najdete v [Záznam interakcí s kontakty](marketing-interactions.md).

### Jak zaeviduji hovor nebo schůzku Teams jako interakci?

V okně podrobností kontaktu najděte tlačítko  **Vytvořit Interakci** a vyberete si z příchozích nebo odchozích hovorů jako šablon interakce. Můžete si také vytvořit vlastní šablony interakce speciálně pro použití s konverzacemi v Teams.

### Mohu zavolat kontaktu z aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] má omezenou integraci na možnosti volání Teams. Z karty kontaktu nebo okna s podrobnostmi kontaktu nelze okamžitě zahájit VOIP volání. Když si však zobrazíte kontaktní údaje v desktopové aplikaci Teams, můžete vybrat pole telefonní číslo pro vytočení, pokud jsou Teams nastaveny jako výchozí aplikace pro vytáčení telefonu na vašem zařízení. Chcete-li vytočit pevné linky nebo čísla mobilních telefonů pomocí tradičního telefonního systému PSTN, Teams vyžaduje, abyste měli aplikaci Microsoft 365 Business Voice. Pro více informací navštivte [Co je Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice).

### Jak zobrazím poslední doklady pro zákazníka nebo dodavatele?

[!INCLUDE [prod_short.md](includes/prod_short.md)] obvykle spojuje kontakt se záznamem zákazníka nebo dodavatele, který zase souvisí se záznamy obchodních transakcí, jako jsou prodejní nabídky nebo nákupní faktury. Chcete-li zobrazit související doklady pro kontakt, přejděte do okna podrobností kontaktu, vyberte pole **Obchodní vztah** nebo použijte akce k navigaci k přidruženému zákazníkovi nebo dodavateli. Na stránce zákazníka nebo dodavatele rozbalte podokno - Okna s fakty a zobrazte statistiky pro různé doklady, na kterých můžete přejít k podrobnostem. Vaše prostředí se může lišit v závislosti na vlastním nastavení a přizpůsobení.

### Jak mohu vyhledat kontakty pomocí speciálních znaků?

Kritéria hledání můžete zadat téměř pomocí libovolných znaků unicode. Nicméně, [!INCLUDE [prod_short.md](includes/prod_short.md)] si však vyhrazuje následující symboly pro další použit: **=**, **.**, **\***, and **@**. Použití těchto symbolů ve vyhledávacích dotazech nemusí vrátit očekávané výsledky. Pokud nevidíte očekávané výsledky, přiložíte symboly do hledaných výrazů do jednotlivých uvozovek, například, **Contoso'='2**.

### Jak mohu vyhledávat kontakty uložené v jiné společnosti?

Aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] může vyhledávat zákazníky, dodavatele a další kontakty v jedné společnosti najednou.  
Chcete-li vyhledat kontakty uložené v jiné [!INCLUDE [prod_short.md](includes/prod_short.md)] společnosti, otevřete [Nastavení](across-teams-settings.md) a odtud změňte prostředí a společnost.

### Jsou [!INCLUDE [prod_short.md](includes/prod_short.md)] kontakty jiné než ty na obrazovce kontaktů v Teams?

Ano. Kontakty uložené v [!INCLUDE [prod_short.md](includes/prod_short.md)] představují obchodní kontakty dostupné vaší organizaci. Jsou to kontakty, se kterými máte zavedený a dobře definovaný obchodní vztah, nebo kontakty, které představují potenciální zákazníky. Tyto kontakty jsou obvykle externí. Ve srovnání s tím jsou kontakty zobrazené v seznamu kontaktů Teams Calling vaše vlastní kontakty. Tyto kontakty nemusí být nutně sdíleny s ostatními ve vaší organizaci a obvykle představují interní kontakty pro vaši organizaci.

### Synchronizuje [!INCLUDE [prod_short.md](includes/prod_short.md)] kontakty s Teams?

Ne.  Kontakty uložené v [!INCLUDE [prod_short.md](includes/prod_short.md)] zůstávají oddělené od vašich kontaktů uložených v Teams.
V současné době nejsou žádné plány na synchronizaci obou seznamů dohromady.

### Jaká je minimální verze [!INCLUDE [prod_short.md](includes/prod_short.md)] pro vyhledávání kontaktů?

Vyhledávání kontaktů vyžaduje, abyste si nainstalovali aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams verze 1.0.4 nebo novější a být připojení k prostředí [!INCLUDE [prod_short.md](includes/prod_short.md)]  verze 18 a novější.

### Mohu vyhledávat ze svého mobilního zařízení?

Vyhledávání kontaktů není v současné době k dispozici v Teams pro iOS a Teams pro Android.

### Jaká oprávnění potřebuji pro vyhledávání kontaktů?

Chcete-li hledat kontakty, potřebujete oprávnění na úrovni objektu k tabulce **Kontakty** v rámci společnosti v [!INCLUDE [prod_short.md](includes/prod_short.md)]. Chcete-li zobrazit okno podrobností kontaktu, potřebujete alespoň oprávnění ke čtení na stránce **Kontakty** ve společnosti [!INCLUDE [prod_short.md](includes/prod_short.md)] a dalším souvisejícím objektům

### Mohu použít vyhledávání kontaktů, pokud jsem pověřený správce?

Ano. Kontakty a kontaktní údaje můžete také zobrazit, pokud máte v organizaci delegované role správce.

### Je vyhledávání kontaktů ovlivněno omezeními rozhraní API?

Ano. Hledání kontaktů z Teams je založeno na [!INCLUDE [prod_short.md](includes/prod_short.md)] v2.0 API a podléhá jakýmkoli limitům rozhraní API, které spravují využití. Další informace o limitech se dozvíte na [Aktuální API Limity](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### Proč jsem někdy požádán o nastavení aplikace?

Po prvním přihlášení do aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams se aplikace se pokusí určit preferovanou společnost v [!INCLUDE [prod_short.md](includes/prod_short.md)]. Pokud aplikace nemůže určit společnost, možná budete muset přejít do **Nastavení** a vybrat společnost, ve které chcete hledat. K této situaci dochází například v případě, že máte přístup k více společnostem napříč prostředími ve vaší organizaci. V takovém případě si budete muset vybrat společnost, než začnete hledat.

Aplikace vás také může požádat abyste navštívili **Nastavení** pokud nemáte předplatné [!INCLUDE [prod_short.md](includes/prod_short.md)] a pokud neexistují žádné [!INCLUDE [prod_short.md](includes/prod_short.md)] prostředí, nebo váš účet nemá licenci [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Chci vyhledat položky nebo záznamy z jiných tabulek. Mohu to udělat z Teams?

Hledání v jiných tabulkách není v tuto chvíli možné. Aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams yhledává pouze v seznamu kontaktů [!INCLUDE [prod_short.md](includes/prod_short.md)],který může zahrnovat dodavatele, zákazníky a další kontakty.

Pokud chcete, aby se možnosti vyhledávání vyvíjely tak, aby zahrnovaly další tabulky, doporučujeme naší komunitě, aby přidala nápad nebo hlasovala pro existující nápady na adrese  https://aka.ms/BusinessCentralIdeas.

## [Práce s kartami](#tab/cards)

### Jaké typy odkazů aplikace podporuje?

Aplikace [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams eaguje na většinu [!INCLUDE [prod_short.md](includes/prod_short.md)] odkazů Webového klienta. Pokud odkaz odkazuje na jeden záznam na stránce, karta zobrazí pole pro tento záznam. Mezi podporované typy stránek patří:

- Stránky karet, například Karta zboží
- Stránky dokladu, například doklad prodejní objednávky
- Stránky ListPlus, které představují jeden záznam složený z dalších záznamů, například výpisu odsouhlasení bankovního účtu
- Stránky jednoduchého seznamu, kde záznam nenabízí možnost přejít k podrobnostem na samostatnou stránku podrobností, například seznam PSČ

Při vkládání odkazu na kořenovou adresu URL webového klienta, například https://businesscentral.dynamics.com, se na kartě místo toho zobrazí informace, které pomáhají novým uživatelům začít s přístupem k [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Jak odstraním kartu odeslanou do chatu?

Kartu, kterou jste již odeslali do chatu, nemůžete smazat. Můžete však odstranit celou zprávu, jejíž součástí je karta.

Jako autor zprávy můžete odstranit všechny zprávy odeslané do chatů s osobou, skupinou nebo kanálem, pokud správce nenastaví zásady, které brání odstranění zpráv. Pokud moderujete kanál jako vlastník kanálu, může vám správce také udělit oprávnění k mazání všech zpráv v kanálu, včetně zpráv odeslaných jinými uživateli.

Smazáním zprávy, která obsahuje kartu, se neodstraní ani neovlivní žádná data v [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Mají karty vždy aktuální informace?

Ne.  Hodnoty polí na kartě v Teams, včetně všech obrázků, jsou založeny na datech dostupných při odeslání této karty do chatu. Karty [!INCLUDE [prod_short.md](includes/prod_short.md)] se v Teams automaticky neobnovují.

### Uvidí ostatní moji kartu, pokud nemají aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams?

Když vytvoříte a odešlete zprávu do chatu, která obsahuje kartu, uvidí ji všichni uživatelé - i když si nenainstalovali aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] pro Teams.

### Jak zjistím, ke které společnosti karta v Teams patří?

Pokud pracujete napříč společnostmi [!INCLUDE [prod_short.md](includes/prod_short.md)], promluvte se svým správcem o povolení odznaku společnosti pro každou společnost. Pokud je tato nápověda povolená, zobrazí se v okně podrobností v Teams, zobrazí společnost a prostředí, do které záznam patří. Informace o tom, jak nastavit odznáček společnosti naleznete v [Zobrazení firemního odznaku pro rychlý přístup k informacím o společnosti](ui-change-basic-settings.md#badge).

## [Práce s podrobnostmi karty](#tab/carddetails)

### Kde je tlačítko uložit v okně podrobností v Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] automaticky uloží změny provedené v libovolném poli, jakmile opustíte pole. Chcete-li pole opustit, klepněte na libovolné místo mimo pole nebo se pomocí klávesy tabulátor přesuňte do dalšího pole. Když se data zobrazí v dialogovém okně podrobností, možná budete muset zvolit **OK**, aby se v [INCLUDE [prod_short.md](includes/prod_short.md)] uložily změny.

### Pokud se rozhodnu zobrazit podrobnosti karty, uvidí ostatní uživatelé okno s mými podrobnostmi?

Ne.  Zatímco všichni v chatu nebo na schůzce mohou zobrazit samotnou kartu, okno podrobností se zobrazí pouze na vašem zařízení, když zvolíte **Podrobnosti**. Ostatní uživatelé musí zvolit **Podrobnosti**, pokud si chtějí na svém zařízení prohlédnout okno s podrobnostmi.

### Můžu Teams hovor zahájit z okna podrobností?

Ano. Pokud používáte desktopovou aplikaci Teams, začněte hovor výběrem propojeného čísla v poli telefonního čísla jako je pole **Mobil** na kartě **Kontaktu**. Teams musí být Vaše výchozí aplikaci pro volání.

Pro volání na místní nebo mezinárodní pevné linky a mobilní telefony teams vyžaduje, abyste měli licenci Business Voice pro podnikové volání. Navíc musíte mít nastaveny Teams jako řešení pro volání. Pro více informací navštivte [Plánování hlasového řešení v Teams](/microsoftteams/cloud-voice-landing-page) v dokumetaci Teams.

### Můžu tisknout doklady z okna podrobností v Teams?

Ano. Sestavy a další doklady tisknete pomocí standardní funkce pro tisk v [!INCLUDE [prod_short.md](includes/prod_short.md)] a libovolné cloudové tiskárny nakonfigurované na stránce **Správa tiskáren** v [!INCLUDE [prod_short.md](includes/prod_short.md)]. Z Teams nemůžete tisknout na místních tiskárnách známých vašemu klientskému zařízení, například na tiskárny, na které byste obvykle tiskli z vašeho prohlížeče. Z tohoto důvodu nemůžete tisknout z okna náhledu sestavy, ale pouze ze stránky požadavku na sestavu, přímo do cloudových tiskáren.

Pro více informací o cloudovém tisku navštivte [Nastavení tiskáren](ui-specify-printer-selection-reports.md).

### Můžu ke kameře přistupovat z okna podrobností v Teams?

Ano. Veškeré funkce [!INCLUDE [prod_short.md](includes/prod_short.md)] v okně podrobností, které používají kameru, jsou k dispozici všem klientům Teams.

### <a name="location"></a>Mohu získat přístup ke své poloze z okna podrobností v Teams?

Pokud používáte funkce v [!INCLUDE [prod_short.md](includes/prod_short.md)], které přistupují k vašim aktuálním souřadnicím polohy, například s mapami, musíte teams používat v prohlížeči nebo v mobilní aplikaci Teams. Poloha není k dispozici při použití desktopové aplikace Teams.

## [Spolupráce s hosty](#tab/collaborating)

### Mohu sdílet karty s uživateli mimo organizaci?

Ano. Když vytvoříte a odešlete zprávu, která obsahuje kartu, všichni příjemci v chatu uvidí kartu, i když jsou hosty nebo jsou pro vaší organizaci externí. Hosté mohou také otevřít okno s podrobnostmi, pokud jim byla udělena oprávnění pro přístup k těmto datům v [!INCLUDE [prod_short.md](includes/prod_short.md)].

### Liší se prostředí pro uživatele, kteří jsou hosty?

Ano. Pozvání uživatelů typu host ze zemí mimo vaši organizaci k účasti na chatu nebo kanálu jim poskytuje podobné, ale ne totožné prostředí ve srovnání s uživateli ve vaší organizaci. Když host obdrží zprávu, která obsahuje kartu, může ji zobrazit. Hosté mohou také otevřít okno podrobností, pokud jim byla udělena oprávnění k přístupu k těmto údajům v [!INCLUDE [prod_short.md](includes/prod_short.md)] a přiřadit [!INCLUDE [prod_short.md](includes/prod_short.md)] v rámci vaší organizace Když host napíše zprávu, odkazy na jeho [!INCLUDE [prod_short.md](includes/prod_short.md)] nebo vaše se nerozbalí na karty.

Další podobnosti a rozdíly mezi hosty a členy týmu najdete v tématu [Zkušenosti hostů v Teams](/MicrosoftTeams/guest-experience) v dokumentaci Teams.

### Jak si hostující uživatel nainstaluje aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Hosté nemají přístup k tržišti aplikací, aby si mohli instalovat aplikace sami. Aplikaci však lze pro ně automaticky nainstalovat na základě zásad vaší organizace. Další způsob, jak může uživatel typu host nainstalovat aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] je, když obdrží chatovou zprávu, která obsahuje kartu [!INCLUDE [prod_short.md](includes/prod_short.md)] card. V tomto případě uživatel zvolí tlačítko **Podrobnosti** nebo nabídku na kartě a poté nainstaluje aplikaci [!INCLUDE [prod_short.md](includes/prod_short.md)] pro použití s vaší organizací. Po instalaci aplikace uživatel automaticky neobdrží žádná oprávnění pro přístup k datům z vašeho [!INCLUDE [prod_short.md](includes/prod_short.md)].

---

## Viz také

[Přehled integrace [!INCLUDE [prod_short](includes/prod_short.md)] a Microsoft Teams](across-teams-overview.md)  
[Instalace aplikace [!INCLUDE [prod_short](includes/prod_short.md)] pro Microsoft Teams](across-install-app-for-teams.md)  
[Řešení problémů Teamss](admin-teams-troubleshooting.md)  
[Vývoj pro integraci Teamsn](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]