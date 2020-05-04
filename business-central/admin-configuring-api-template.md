---
title: Configuring API Templates | Microsoft Docs
description: Describing the steps you must go through to configure API templates for Dynamics 365 Business Central.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 10/01/2019
ms.author: solsen
---

# Konfigurace šablon API
Knihovna API pro [!INCLUDE[d365fin_md](includes/d365fin_md.md)] poskytuje zjednodušenou reprezentaci základních entit. Všechny vlastnosti v aplikaci nejsou vystaveny prostřednictvím přidruženého rozhraní. Stránka **Nastavení API** vám umožňuje definovat šablony, které se používají k naplnění prázdných vlastností v entitě při vytvoření akce ÚČTOVAT prostřednictvím rozhraní API.

Například, pokud je pro položku entity definována konfigurační šablona, když se vytvoří nový záznam položky prostřednictvím položek API, budou z vybrané šablony naplněny všechny vlastnosti nové položky, které nejsou definovány ve volání rozhraní API. Pokud například není definováná žádná hodnota pro pole **Obecná Účto skupina zboží** prostřednictvím rozhraní API, avšak hodnota je definována ve vybrané šabloně, pak účtovací skupina definovaná v šabloně  bude použita pro novou položku.

## Nastavení šablony entity
Chcete-li používat šablony s knihovnou API, musíte nejprve nastavit a definovat vlastnosti šablon. Tyto šablony můžete nastavit na stránce **Konfigurační šablony**. Pro více informací navštivte [Příprava na migraci zákaznických dat](admin-use-templates-to-prepare-customer-data-for-migration.md).

## Přiřazení šablony k rozhraní API

Chcete-li přiřadit šablonu API, musíte provést následující kroky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení API** a poté vyberte související odkaz.
2. Zvolte **Nový**, a poté vyberte ze záznamu hodnotu **Pořadí**.
Pokud je pro rozhraní API (ID stránky) vybráno více než jedna šablona, budou použity v pořadí definovaném ve sloupci **Pořadí**.
Při použití každé šablony jsou hodnoty polí definované v šabloně použity pouze pro pole, která ještě neměla definovanou hodnotu, a to buď explicitně v rozhraní API, nebo v dříve použité šabloně v pořadí.
3. Vyberte hodnotu **ID stránky**.
Toto je stránka rozhraní API, na které bude šablona použita. Vyhledávání **ID stránky** poskytuje seznam všech rozhraní APIs dostupných v knihovně.
4. Vyberte hodnotu v poli **Kód šablony**.
Kód šablony je kód šablony, který byl definován na stránce **Konfigurační šablony**. Definované hodnoty šablony jsou použity pro rozhraní API.
5. V poli **Podmínky** určete, která šablona má být použita.
Definovaná šablona se použije na nový záznam vytvořený pomocí API, a to pouze tehdy, jsou-li podmínky definované v poli **Podmínky** shodné s hodnotami již nadefinovanými pro novou instanci entity.

## Viz také
[Dokumentace API](/dynamics-nav/fin-graph)  
[Vývoj aplikací Connec pro [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[Povolení API](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Koncové body API](/dynamics-nav/endpoints-apis-for-dynamics)  
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Správa](admin-setup-and-administration.md)