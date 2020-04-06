---
title: Create new companies using an assisted setup guide | Microsoft Docs
description: It's easy to create a new, blank company in Business Central. An assisted setup guide helps you through the steps, and you can import your existing business data.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 11/01/2019
ms.author: edupont

---
# Vytváření nových společností v [!INCLUDE[d365fin](includes/d365fin_md.md)]
V [!INCLUDE[d365fin](includes/d365fin_md.md)], se kontejnery pro obchodní data, která patří obchodní jednotce nebo právnické osobě, označují jako *společnost*. Když se v [!INCLUDE[d365fin](includes/d365fin_md.md)] zaregistrujete, dostanete demonstrační společnost a prázdnou společnost, *Moje společnost*. Přepínání mezi společnostmi je snadné, stačí jít do **Moje nastavení** a přejít na druhou společnost. Můžete však také vytvořit nové společnosti v [!INCLUDE[d365fin](includes/d365fin_md.md)] v závislosti na vašich obchodních potřebách. Když vytvoříte novou společnost, pomůže vám průvodce asistovanou instalací. Poté můžete importovat relevantní data z vaší starší verze systému nebo jiné společnosti do [!INCLUDE[d365fin](includes/d365fin_md.md)].

## Vytvoření nové společnosti
Pokud se rozhodnete přidat společnost do svého [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete použít průvodce asistovanou instalací **Vytvořit novou společnost**, který vám pomůže začít. Průvodce nastavením je k dispozici na stránce **Společnosti** a z vyhledávání v poli **Společnost** na stránce **Moje nastavení**.

Průvodce nastavením nabízí tři šablony:

- **Vyhodnocení - vzorek dat**
Tímto se vytvoří společnost, která je podobná demonstrační společnosti s ukázkovými daty a instalačními daty.
- **Provozní sada - pouze nastavení dat**
Tím se vytvoří společnost, která je podobná  **Mé společnosti** s daty nastavení, ale bez ukázkových dat.
- **Úplné vyhodnocení - úplný vzorek dat**
Tím se vytvoří společnost s daty nastavení a úplnými ukázkovými daty pro všechny funkce, včetně výroby a správy služeb.
- **Vytvořit novou - žádná data**
Tím se vytvoří prázdná společnost bez nastavovacích dat.

Pokud chcete snadno začít s novou společností, zvolte **Provozní sada - pouze nastavení dat** importujte vlastní obchodní data, jako jsou zákazníci, zboží a dodavatelé. Vyberte šablonu **Nové** pokud chcete vše nastavit od začátku. V takovém případě můžete použít průvodce nastavením **Nastavení společnosti**, který vám pomůže začít se základními daty nastavení.

> [!NOTE]
> Když vytvoříte novou společnost, trvá několik minut, než k ní získáte přístup v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Stav nastavení na stránce **Společnosti** ukazuje, kdy je nová společnost pro vás připravena. Poté můžete přejít na novou společnost pomocí **Má nastavení**.

Během vaší 30denní zkušební verze, můžete vytvořit libovolný počet nových společností, ty ale budou k dispozici pouze během zkušebního období. Pro více informací, kontaktujte vašho [!INCLUDE[d365fin](includes/d365fin_md.md)] partnera.

## Kopírování společnosti
Na stránce  **Společnosti**, můžete pomocí akce **Kopírovat** vytvořit druhou společnost založenou na obsahu existující společnosti. To je užitečné například v případě, že chcete otestovat společnost bez narušení výrobních dat.

> [!Important]
> Tuto funkci nelze použít k vytvoření zálohy společnosti. Zálohování společnosti začíná exportem databáze jako souboru .bacpac. Pro více informací navštivte [Exportování databází](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) v nápovědě ITPro a pro vývojáře.

## Nastavení společnosti
Když se přihlásíte k nové společnosti, automaticky se spustí průvodce **Nastavení společnosti** a pomůže vám začít. Budete požádáni o informace o vaší firmě, jako je adresa, bankovní údaje a metoda ocenění zásob. Tyto informace požadujeme, protože se používají jako základ pro mnoho oblastí v [!INCLUDE[d365fin](includes/d365fin_md.md)], které nebudete muset později nastavovat ručně.

Například adresa vaší společnosti je zahrnuta ve fakturách a dalších dokumentech, informace o vaší bance se používají v platbách a metoda ocenění se používá k výpočtu cen a ocenění zásob.

Jakmile máte základy na místě, můžete nastavit zbývající základní oblasti. Potom jste připraveni přidat obchodní data, jako jsou zákazníci a dodavatelé. Pro více informaci navštivte [Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).

## Viz také
[Přizpůsobení Business Central](ui-customizing-overview.md)  
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Import obchodních dat z jiných finančních systémů](across-import-data-configuration-packages.md)  
[Změna základního nastavení](ui-change-basic-settings.md)  
[Začínáme](product-get-started.md)
