---
title: Customizing Business Central Online Using Extensions
description: Learn all about adding functionality and customizing Business Central by installing extensions here.
author: edupont04


ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.search.form: 2500, 2502
ms.date: 03/22/2022
ms.author: edupont

---
# Přizpůsobení Business Central Online Použitím Rozšíření

Můžete změnit [!INCLUDE[prod_short](includes/prod_short.md)] online instalací rozšíření, která například přidávají funkce, mění chování nebo umožňují přístup k novým online službám.

> [!NOTE]
> Chcete-li nainstalovat nebo odinstalovat rozšíření z AppSource nebo přidat rozšíření pro jednotlivé klienty, musíte mít správná oprávnění. Musíte být členem skupiny uživatelů **D365 Extension Mgt.** nebo musíte mít **EXTEN. MGT. - ADMIN** sadu oprávnění. Pokud jste správce, můžete přiřadit skupiny uživatelů a oprávnění ostatním uživatelům ve vaší společnosti. Pro více informací navštivte [Vytvoření uživatelů dle licencí](ui-how-users-permissions.md).
>
> Chcete-li použít funkce poskytované rozšířením, jako je otevírání stránek, spouštění sestav, výběr akcí a další, musíte mít přiřazené sady oprávnění, které jsou nainstalovány jako součást rozšíření.

<!-- [!NOTE]  
> The **EXTEN. MGT. - ADMIN** permission set was introduced in 2021 release wave 1 as a replacement for the **D365 EXTENSION MGT** permission set in earlier versions.-->

> [!IMPORTANT]  
> Nahrávání rozšíření pro jednotlivé klienty a instalace rozšíření AppSource není podporováno prostřednictvím stránky **Správa rozšíření** pro místní instalace. Rozšíření AppSource nemůžete nainstalovat lokálně, včetně aplikací založených na Dockeru.

Při prvním spuštění [!INCLUDE[prod_short](includes/prod_short.md)], jsou již některá rozšíření nainstalována. Postupem času vám budou zpřístupněna další rozšíření a pak si můžete vybrat, zda chcete rozšíření použít nebo ne.

Společnost Microsoft například poskytuje rozšíření, které zajišťuje integraci s PayPal Payments Standard. Toto rozšíření je nainstalováno ve výchozím nastavení.
Pokud je však k dispozici jiné rozšíření, které nabízí integraci s jinou platební službou, můžete nainstalovat nové rozšíření a poté zvolit, kterou ze dvou služeb chcete použít.

Rozšíření se spravují na stránce **Správa rozšíření**. Na tuto stránku se dostanete z Domovské stránky. Případně vyberte ikonu **Hledat stránku nebo sestavu** Žárovku, která otevře funkci Řekněte mi ![](media/ui-search/search_small.png "Řekněte mi, co chcete udělat") v pravém horním rohu zadejte **Rozšíření** a poté vyberte související odkaz. Pro více informací navštivte [Instalace a odinstalování rozšíření](ui-extensions-install-uninstall.md).

> [!NOTE]  
> Pokud si myslíte, že byste měli mít přístup k rozšíření, ale nemůžete najít jeho funkce, podívejte se na stránku **Správa rozšíření** - pokud tam rozšíření není uvedeno, můžete ho nainstalovat podle popisu v následující části.

> [!NOTE]  
> Přihlaste se na [AppSource.microsoft.com](https://appsource.microsoft.com/) pomocí e-mailového účtu, který používáte pro [!INCLUDE[prod_short](includes/prod_short.md)] online. Pro bezproblémové používání prostředí používejte stejný e-mailový účet.

Na marketplace se můžete také dostat z [!INCLUDE[prod_short](includes/prod_short.md)]. Na stránce **Správa rozšíření** uvidíte rozšíření, která jsou aktuálně nainstalována, a můžete otevřít stránku **Tržiště rozšíření**, která zobrazuje [!INCLUDE[prod_short](includes/prod_short.md)] rozšíření, která jsou aktuálně dostupná v AppSource. Pokud zvolíte odkaz *Více aplikací* budete přesměrováni na [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

Pokud vyberete rozšíření, můžete si přečíst, co rozšíření dělá, a můžete získat přístup k nápovědě k rozšíření a dozvědět se více. Pokud se rozhodnete získat rozšíření, musíte souhlasit s podmínkami použití. Pokud získáte rozšíření z webu AppSource, budete pro dokončení instalace přihlášeni k [!INCLUDE[prod_short](includes/prod_short.md)].

Když nainstalujete rozšíření, budete jej možná muset nastavit, například zadat účet pro použití s rozšířením **Platební standard PayPal pro [!INCLUDE[prod_short](includes/prod_short.md)]**.
Jiná rozšíření jednoduše přidají pole na existující stránku nebo například přidají novou stránku.

Pokud odinstalujete rozšíření a poté změníte názor, můžete ji nainstalovat znovu. Pokud odinstalujete rozšíření, které používáte, data se zachotá, takže pokud rozšíření znovu nainstalujete, budou data stále k dispozici. Jsou požadována některá rozšíření. Nelze je odinstalovat ze stránky **Správa rozšíření**. Pokud to zkusíte, zobrazí se chybová zpráva.

Některá rozšíření poskytuje společnost Microsoft a jiná rozšíření poskytují [jiné společnosti](ui-extensions-other.md). Všechna rozšíření jsou testována před tím, než jsou k dispozici, ale doporučujeme abyste před instalací prošli odkazy, které jsou k dispozici, abyste se o rozšíření dozvěděli více, než se rozhodnete jej nainstalovat.

> [!NOTE]  
> Nová rozšíření od společnosti Microsoft a dalších dodavatelů můžete sledovat na [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## Rozšíření a přenos dat

Protože následující rozšíření komunikují s jinými službami, mohou přenášet data mimo oblast prostředí [!INCLUDE[prod_short](includes/prod_short.md)]:

* AMC Banking 365 Fundamentals Extension
* Obrazový analyzátor
* Predikce opožděných plateb
* Standardní platby PayPal
* Prognóza prodeje a zásob
* WorldPay Payments Standard

To se týká i některých funkcí základní aplikace, například následujících možností:

* Prognóza peněžních toků
* Služba výměny dokladů
* Dataverse connections
* Služba OCR
* Online Mapy
* Nařízení o DPH EU Čísla. Služba

## Doporučené aplikace
Microsoft partneři a prodejci mohou vytvářet rozšíření, která mohou používat k sestavování seznamů aplikací, které často doporučují svým zákazníkům. Pokud ano a nasadili rozšíření do vašeho tenanta, aplikace budou dostupné na stránce **Doporučené aplikace**. Zde si můžete přečíst o každé aplikaci a rozhodnout se, zda ji nainstalovat.

> Pokud jste partnerem nebo prodejcem společnosti Microsoft a máte zájem o poskytnutí seznamu doporučených aplikací, viz [Doporučení aplikací z AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

## Viz také

[Instalace a odinstalace rozšíření](ui-extensions-install-uninstall.md)  
[Přizpůsobení Business Central](ui-customizing-overview.md)  
[Rozšíření Business Central od jiných poskytovatelů](ui-extensions-other.md)  
[Nastavení služby Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Povolení plateb zákazníků prostřednictvím služby PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrace obchodních dat z jiných finančních systémů](across-import-data-configuration-packages.md)  
[Nastavení rozšíření GetAddress.io pro poštovní směrovací číslo Spojeného království](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Rozšíření od jiných poskytovatelů](ui-extensions-other.md)  
[Příprava na podnikání](ui-get-ready-business.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
