---
title: Vícejazyčné prostředí a lokalizace | Microsoft Docs
description: Naučte se, jak jazyk a národní prostředí ovlivňují vaše zkušenosti v Business Central.
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: language, locale, localization, culture
ms.date: 01/14/2020
ms.reviewer: v-zdbice
ms.author: edupont

---
# Změna jazyka a národního prostředí

[!INCLUDE[d365fin](includes/d365fin_md.md)]  je podporován na mnoha trzích a je k dispozici v jazycích, které tyto trhy vyžadují. Je to výsledek podpory více jazyků v kombinaci s podporou legislativních požadavků na podporovaných trzích. Znamená to, že [!INCLUDE[d365fin](includes/d365fin_md.md)] může být prezentován v různých jazycích. Můžete změnit jazyk používaný k zobrazení textů, a změna je okamžitá, jakmile jste byli automaticky odhlášeni a znovu přihlášeni. Toto nastavení platí pro vás a ne pro všechny ostatní ve vaší společnosti.

Pokud například používáte kanadskou verzi [!INCLUDE[d365fin](includes/d365fin_md.md)], uvidíte uživatelské rozhraní v angličtině a francouzštině, ale stále je to  stejná kanadská verze [!INCLUDE[d365fin](includes/d365fin_md.md)] ve všech ostatních aspektech. Není to to stejné, jako například [!INCLUDE[d365fin](includes/d365fin_md.md)] ve Spojeném království.

## Změna jazyka

Chcete-li změnit jazyk uživatelského rozhraní, přejděte na stránku **Má nastavení**. Pro více informací navštivte [Změna základního nastavení](ui-change-basic-settings.md#language).

Změna textů, které jsou uloženy jako data, není součástí vícejazyčných možností systému. Toto je problém designu aplikace. Příklady takových textů jsou názvy zboží ve skladu nebo poznámky pro zákazníka. Jinými slovy, tyto typy textu nejsou přeloženy.

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] pouze podporuje jednu znakovou sadu pro data. Proto některé znaky nemusí být podporovány při načítání dat, která byla zadána pomocí jiné znakové sady, díky tomu může docházet k problémům. Váš tenant může například podporovat pouze anglické a ruské znaky a pokud zadáváte data v jiném jazyce, nemusí být správně uložena. Měli byste se obrátit na správce systému a ujistit se, že víte, které jazyky jsou pro Váš [!INCLUDE[d365fin](includes/d365fin_md.md)] podporovány.

## Změna národního prostředí (oblasti)

Národní prostředí se liší od jazykových i legislativních požadavků na místních trzích. Národní prostředí určuje, jakým způsobem se data zobrazují ve smyslu oddělovače desetinných míst, zarovnání vlevo nebo vpravo a určitých dalších nastavení. Národní prostředí také určuje některé systémové prvky v prohlížeči, například akci pro vytvoření nové položky v seznamu.

Národní prostředí můžete změnit na kartě prohlížeče, který používáte pro práci v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Změna se týká pouze vás a nikoli ostatních uživatelů ve vaší společnosti.

> [!IMPORTANT]
> Když změníte národní prostředí, zobrazí se dlouhý seznam jazyků a národních prostředí. V aktuální verzi [!INCLUDE[d365fin](includes/d365fin_md.md)] se použije pouze nastavení národního prostředí.

Pro změnu národní prostředí (oblasti) běžte na stránku **Má nastavení**. Pro více informací navštivte [Změna základního nastavení](ui-change-basic-settings.md).

## Verze aplikace

Na stránce **Nápověda a podpora** můžete vidět verzi [!INCLUDE [prodshort](includes/prodshort.md)], na které je vaše společnost založena. Pokud chcete založit společnost na jiné verzi, může váš správce vytvořit nové produkční prostředí. Další informace naleznete v části [Vytvoření nového produkčního prostředí](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-production-environment) v obsahu pro vývojáře a IT odborníky.

## Jazyky nápovědy [!INCLUDE[d365fin](includes/d365fin_md.md)]

Obsah nápovědy pro základní funkce v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)] je publikována na webu Microsoft Docs a je k dispozici v mnoha různých jazycích. Pokud přistupujete k nápovědě z [!INCLUDE[d365fin](includes/d365fin_md.md)], zobrazí se obsah ve vašem jazyce. Pokud daná stránka ještě není ve vašem jazyce k dispozici, bude zobrazena v angličtině.

### Jak mohu změnit jazyk?

Je to jednoduché - přejděte do dolní části stránky prohlížeče a v levém dolním rohu vyberte symbol zeměkoule.

> [!NOTE]
> Seznam zobrazuje všechny jazyky, které jsou podporovány webem Microsoft Docs. [!INCLUDE[d365fin](includes/d365fin_md.md)] je k dispozici v omezeném počtu zemí/oblastí, ale obsah nápovědy je k dispozici ve více jazycích. Obsah nápovědy není k dispozici ve všech jazycích, které web Microsoft Docs podporuje.

## Viz také

[Zdroje pro nápovědu a podporu](product-help-and-support.md)  
[Změna základního nastavení](ui-change-basic-settings.md)  
[Začínáme](product-get-started.md)
