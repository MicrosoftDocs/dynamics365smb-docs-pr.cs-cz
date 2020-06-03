---
title: Vyhledávání a filtrování v Business Central
description: Odpovědi na často kladené otázky týkající se hledání a filtrování.
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'keyboarding, productivity, how do i, filter pane'
ms.date: 01/13/2020
ms.reviewer: v-zdbice
ms.author: mikebc
---

# Vyhledávání a filtrování - Otázky a odpovědi

Tento článek odpovídá na běžné otázky, které můžete mít ohledně vyhledávání a filtrování.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Existuje rozdíl mezi vyhledáváním a filtrováním?

Ano.

- Vyhledávání je jednoduché a široké: odpovídá záznamům, které obsahují hledaný text ve všech viditelných polích na stránce a nerozlišuje velká a malá písmena.
- Filtrování je vysoce flexibilní a lze jej použít na určitá pole, včetně těch, která nejsou na stránce viditelná: zobrazuje záznamy s přesnými shodami rozlišujícími velká a malá písmena, ale lze jej upravit pomocí výkonných vyhledávacích symbolů, tokenů a vzorců. Další informace o použití těchto funkcí naleznete v části [Řazení, vyhledávání a filtrování](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Je vyhledávání a filtrování podporováno pro striktní použití klávesnice?

Vyhledávání a filtrování byla vysoce optimalizována pro uživatele, kteří dávají přednost interakci bez myši, aby s daty pracovali efektivně. Existuje celá řada klávesových zkratek, které lze použít postupně pro rychlou práci. Další informace naleznete v [Klávesové zkratky](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Je podokno filtrů dostupné ve všech seznamech?

Podokno filtrů je k dispozici na stránkách, kde je seznam primárním obsahem na stránce, jako jsou sešity a stránky seznamu, včetně seznamů dostupných z navigačního panelu. Podokno filtru zatím není k dispozici pro seznamy, které jsou zobrazeny jako části stránek, jako jsou například informační podokna (FactBox) nebo Centra rolí. Pokud je seznam  vložen na stránku, například prodejní řádky na prodejní objednávce, je podokno filtru k dispozici při zobrazení detailu tohoto seznamu pomocí tlačítka režimu detailu. Další informace viz [Zobrazení detailu pro řádkové položky](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>Jak mohu uložit mé filtry?

Vaše filtry a úpravy předdefinovaných filtrů jsou zapamatovány po celou dobu relace (po dobu, co jste přihlášeni), i když opustíte stránku. Filtry můžete trvale uložit jako pojmenované pohledy na seznam výběrem ikony ![Save View](media/save_view_icon.png "Uložit pohled") v podokně filtru. Další informace naleznete v části [Často kladené otázky týkající se zobrazení seznamů](ui-views-faq.md). Nezapomeňte, že na rozdíl od filtrů se text vyhledávání nezapamatuje, když odcházíte ze stránky, a při uložení pohledu se neuloží.

Na stránkách požadavku sestav můžete také uložit filtry nebo použít předdefinované filtry. Další informace viz [Používání uložených nastavení](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Je to stejné jako Rozšířené filtry a Omezit součty v Microsoft Dynamics NAV?

[!INCLUDE[d365fin](includes/d365fin_md.md)] staví na těchto oblíbených funkcích a poskytuje moderní a vysoce použitelné zkušenosti pro vyhledávání a analýzu vašich dat. S pomocí více klávesových zkratek a zavedením vyhledávání [!INCLUDE[d365fin](includes/d365fin_md.md)] překonává funkce poskytované v Dynamics NAV.

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Mohu vyhledávat a filtrovat pomocí doprovodných aplikací a aplikace Outlook AddIn?

Na jiných cílech zobrazení, jako jsou mobilní zařízení nebo v aplikaci Outlook, můžete vyhledávat v seznamech, ale ve většině případů nelze filtrovat v jednotlivých polích.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Rozšíří Microsoft možnosti podokna filtrů?

V Microsoftu neustále nasloucháme zpětné vazbě od naší rozmanité komunity uživatelů a jednáme podle nejlepších návrhů této komunity. Pokud máte zájem rozšířit podokno filtrů do více typů klientů, více typů seznamů a sestav, nebo máte skvělý nápad, jak jej vylepšit, přidejte tento nápad nebo hlasujte pro existující nápady na stránce [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Mohu něco udělat se zprávou "Hledání řádků trvá příliš dlouho"?

Existuje časový limit, jak dlouho může operace vyhledávání trvat. Nejprve zkuste změnit kritéria vyhledávání a znovu hledat. Pokud používáte [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, obraťte se na správce systému, protože správce může prodloužit časový limit pro vyhledávání.

Jako on-premises správce zvýšíte časový limit pro vyhledává změnou nastavení **Search Timeout** [!INCLUDE[prodshort](includes/prodshort.md)] serveru. Pro více informací navštivte [Konfigurace Business Central serveru](/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) v nápovědě [!INCLUDE[prodshort](includes/prodshort.md)] pro vývojáře a IT odborníky.

## Viz také

[Řazení, vyhledávání a filtrování](ui-enter-criteria-filters.md)  
[Použití funkce Řekněte mi k nalezení funkcí a informací](ui-search.md)  
[Hledání stránek pomocí Průzkumníka rolí](ui-role-explorer.md)  
[Začínáme](product-get-started.md)  