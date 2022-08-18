---
title: OneDrive for Business FAQ
description: Get answers for some typical questions about working with OneDrive for Business and Business Central.
author: brentholtorf

ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, integration, share, browser
ms.date: 05/19/2021
ms.author: bholtorf
---
# Nejčastější dotazy k OneDrive pro firmy

[!INCLUDE [online_only](includes/online_only.md)]

Tento článek odpovídá na některé otázky, které můžete mít při práci s OneDrive a [!INCLUDE [prod_short](includes/prod_short.md)].

## Funguje to se všemi [!INCLUDE[prod_short](includes/prod_short.md)] klienty?

Ano. Soubory na OneDrive můžete otevírat z mobilních aplikací [!INCLUDE[prod_short](includes/prod_short.md)], při prohlížení karty v Microsoft Teams nebo dokonce z doplňku Outlooku.

## Je OneDrive stejný jako SharePoint pro ukládání souborů?

V rámci předplatného Microsoftu 365 vám vaše organizace poskytuje OneDrive, úložiště souborů v cloudu. Služba OneDrive je ve výchozím nastavení soukromá a můžete si v ní uspořádat obsah a vybrat, které soubory nebo složky chcete sdílet a s kým. SharePoint naproti tomu poskytuje úložiště souborů v cloudu, které je sdíleno s ostatními v organizaci.

## Má [!INCLUDE[prod_short](includes/prod_short.md)] podporu služby OneDrive pro spotřebitele?

Ne. Tato integrace je určena výhradně pro OneDrive pro firmy a podporuje pouze váš pracovní účet.

## Podporují se všechny plány OneDrivu pro firmy?

[!INCLUDE[prod_short](includes/prod_short.md)] epodporuje samostatné plány pro OneDrive pro firmy. OneDrive se musí koupit jako součást plánu Microsoft 365 Business nebo Enterprise. Pro více informací navštivte [Porovnání cen a plánů cloudového úložiště OneDrive](https://www.microsoft.com/microsoft-365/onedrive/compare-onedrive-plans?market=af&activetab=tab:primaryr2).

## Kde najdu stav služby OneDrive?

Správci mají přístup k řídicímu panelu stavu služby jako součást Centra pro správu Microsoft 365. Řídicí panel obsahuje dostupnost služby OneDrive.

## Je integrace OneDrivu k dispozici pro [!INCLUDE[prod_short](includes/prod_short.md)] on premises?

Ano, ale na rozdíl od [!INCLUDE[prod_short](includes/prod_short.md)] online vyžaduje další nastavení. Pro více informací, navštivte [Konfigurace Business Central On-Premises](admin-onedrive-integration.md#configuring-business-central-on-premises).

## Propojuje se [!INCLUDE[prod_short](includes/prod_short.md)] v místě se serverem SharePoint?

Ne. Tato kombinace nasazení není podporována, a to ani v případě, že má SharePoint Server povolené osobní weby.

## Má [!INCLUDE[prod_short](includes/prod_short.md)] online připojení k serveru SharePoint Server?

Ne. Tato kombinace nasazení není podporována, a to ani v případě, že má SharePoint Server povolené osobní weby.

## Jak to funguje v organizaci s více prostředími?

Integrace předpokládá, že názvy společností jsou v prostředích [!INCLUDE[prod_short](includes/prod_short.md)] jedinečné. Když jsou názvy společností v rámci organizace jedinečné, otevřením souboru na OneDrive se soubor zkopíruje do složky pojmenované po aktuální společnosti. Pokud názvy společností nejsou v různých prostředích jedinečné, mohou být soubory z identických názvů společností umístěny společně do stejné složky

## Změnili jsme název společnosti. Co se stane s mými předchozími soubory?

[!INCLUDE[prod_short](includes/prod_short.md)] automaticky nemigruje soubory, které jste otevřeli dříve na OneDrivu, do nové složky. Po přejmenování vaší společnosti akce Otevřít na OneDrivu zkopíruje soubory do složky s novým názvem společnosti.

## Při připojování souborů k [! INCLUDE[prod_short](includes/prod_short.md)], jak vyberu soubor z OneDrivu?
[!INCLUDE[prod_short](includes/prod_short.md)] neposkytuje výběr cloudového souboru. Soubor si musíte stáhnout z OneDrivu do svého zařízení a pak ho nahrát do [!INCLUDE[prod_short](includes/prod_short.md)].

## Chci místo toho otevřít soubory ve službě SharePoint. Jak to mám udělat?

[!INCLUDE[prod_short](includes/prod_short.md)] eposkytuje funkce pro kopírování souborů do služby SharePoint a jejich otevření z knihovny služby SharePoint. Chcete-li porozumět vašim možnostem, kontaktujte svého partnera společnosti Microsoft nebo vyhledejte aplikace na AppSource.

## Jak vypnu integraci na OneDrive?

[!INCLUDE[prod_short](includes/prod_short.md)]  online neposkytuje způsob, jak povolit nebo zakázat integraci do OneDrive.

## Mám se ke službě SharePoint připojit pomocí stránky Nastavení připojení služby SharePoint?

Jedná se o starší funkci, kde všechny [!INCLUDE[prod_short](includes/prod_short.md)] soubory od všech uživatelů jsou odesílány do jedné složky služby SharePoint. Doporučujeme nekonfigurovat pevnou záložku Sdílené dokumenty na stránce Nastavení připojení služby SharePoint, protože pracujeme na vyřazení této funkce.

## Která verze [!INCLUDE[prod_short](includes/prod_short.md)] podporuje OneDrive?

Integrace s OneDrivem byla k dispozici ve vlně vydání 2 v roce 2021.

## Bude Microsoft i nadále vylepšovat integraci do OneDrivu?

Ve společnosti Microsoft neustále nasloucháme zpětné vazbě od naší rozmanité komunity uživatelů a jednáme na základě nejlepších návrhů. Další informace o integraci s aplikacemi Microsoft 365 najdete v [Plán vydání Dynamics 365](/dynamics365-release-plan/2021wave1).

Pokud se chcete podílet na zlepšování integrace OneDrive nebo máte nápad, který by zlepšil sdílení souborů a spolupráci v [!INCLUDE[prod_short](includes/prod_short.md)] přidejte nápad nebo hlasujte pro stávající nápady na [https:/ /aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## Řešení potíží

Tato část obsahuje informace o tom, jak identifikovat a opravit problémy, se kterými se můžete setkat při používání OneDrivu s [!INCLUDE[prod_short](includes/prod_short.md)].

### Musím se přihlásit při každém otevření souboru

Je nám líto, ale je to známý problém a pracujeme na něm. Očekáváme, že v nadcházející aktualizaci poskytneme plynulejší přihlášení.

### Business Central nemůže najít můj OneDrive

Když se zobrazí tato zpráva "Nelze určit umístění vašeho OneDrivu pro firmy, obraťte se na svého partnera a nastavte to.", Zkontrolujte, jestli uživatel alespoň jednou přistupoval ke svému OneDrivu. Pokud tomu tak není, požádejte osobu, aby šla do portal.office.com/onedrive a nastavila ji. To může chvíli trvat. Pokud se zpráva zobrazuje i po 24 hodinách, kontaktujte podporu.


## Viz také
[Integrace Business Central a OneDrive](across-onedrive-overview.md)  
[Správa integrace OneDrive s Business Central](admin-onedrive-integration.md)  
[Otevírání souborů Business Central na OneDrive](across-share-onedrive.md)
