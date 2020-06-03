---
title: Často kladené otázky o Řekněte mi | Microsoft Docs
description: 'Tento článek poskytuje odpovědi na otázky, které naši partneři a zákazníky často kladou na Řekněte mi.'
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 01/13/2020
ms.reviewer: v-zdbice
ms.author: bholtorf
---

# **Řekněte mi** - Otázky a odpovědi
Toto téma odpovídá na otázky, na které se naši pokročilí uživatelé často ptají o funkci **Řekněte mi**.

## Otázky a odpovědi

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>Jsou všechny akce z mé aktuální stránky zjistitelné v **Řekněte mi**?


Ne. Akce v částech, jako je například část Prodejní řádky nebo Okna s fakty, se v **Řekněte mi** nezobrazí.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>Jsou výsledky v **Řekněte mi** filtrovány podle oprávnění?

Pokud uživatel nemá oprávnění, akce se nezobrazí. Nicméně, stránky a sestavy se ve výsledcích objeví, ale vyžadují, aby k nim měl uživatel přístup. Pokud uživatel nemá oprávnění k prohlížení objektu, zobrazí se zpráva.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>Zobrazuje funkce **Řekněte mi** obsah z mých vlastních přizpůsobení nebo nainstalovaných rozšíření třetích stran?

Akce, stránky a sestavy, které pocházejí z rozšíření se funkcí **Řekněte mi** zobrazí, ale vlastní dokumentace nápovědy ne. Technické informace o tom, jak učinit vlastní stránky a sestavy zjistitelnými, naleznete v části [Přidávání stránek a sestav do vyhledávání](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>Čím se to liší od toho, co bylo dříve známé jako Hledat stránku nebo sestavu?

**Hledat stránku nebo sestavu** se vyvinulo do **Řekněte mi**, aby vám pomohlo rychle dokončit práci. **Hledat stránku nebo sestavu** vám může pomoci pouze při vyhledávání stránky nebo sestavy. Na technické úrovni již Řekněte mi není založen na starém konceptu MenuSuite.

### <a name="i-use-on-premises-included365finincludesd365fin_mdmd-does-that-include-tell-me"></a>Využívám [!INCLUDE[d365fin](includes/d365fin_md.md)] on-premises. Zahrnuje to funkci **Řekněte mi**?

Můžete používat funkci **Řekněte mi** v on-premises  webovém klientovi pro vyhledání akce, stránky a zprávy, ale nikoli však dokumentace nebo aplikace a poradenských služeb na AppSource.

### <a name="is-tell-me-available-for-all-form-factors"></a>Je funkce **Řekněte mi** k dispozici pro všechna typy klientů?

**Řekněte mi** je k dispozici pouze ve webovém klientovi nebo v aplikaci pro Windows.

### <a name="are-the-documentation-results-available-in-any-language"></a>Jsou výsledky dokumentace k dispozici v jakémkoli jazyce?

Články nápovědy se zobrazují v jazyce, který jste si zvolili v **Moje nastavení**, pokud je v tomto jazyce nápověda k dispozici.

### Proč se u výsledků vyhledávání nezobrazuje ikona záložek?

Ikona záložky se nezobrazí v okně **Řekněte mi**, pokud je zakázáno přizpůsobení role uživatele.

## Viz také

[Ukládaní a přizpůsobení zobrazení seznamů](ui-views.md)  
[Použití funkce Řekněte mi k nalezení funkcí a informací](ui-search.md)  
[Hledání stránek pomocí Průzkumníka rolí](ui-role-explorer.md)