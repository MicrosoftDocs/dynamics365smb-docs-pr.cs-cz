---
title: Vyhledávání a filtrování v Business Central
description: Odpovědi na často kladené otázky týkající se Hledání a Filtrování.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'keyboarding, productivity, how do i, filter pane'
ms.date: 10/01/2018
ms.author: mikebc
---

# <a name="searching-and-filtering-faq"></a>Vyhledávání a Filtrování FAQ
Tento článek odpovídá na běžné otázky, které můžete mít ohledně vyhledávání a filtrování.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Existuje rozdíl mezi vyhledáváním a filtrováním?
Ano.
- Vyhledávání je jednoduché a široké: odpovídá záznamům, které obsahují hledaný text ve všech viditelných polích na stránce a nerozlišuje velká a malá písmena.
- Filtrování je vysoce flexibilní a lze jej použít na určitá pole, včetně těch, která nejsou na stránce viditelná: zobrazuje záznamy s přesnými shodami rozlišujícími velká a malá písmena, ale lze jej upravit pomocí výkonných vyhledávacích symbolů, tokenů a vzorců. Další informace o použití těchto funkcí naleznete v části [Řazení, Vyhledávání a Filtrování v Seznamech](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Existuje možnost použití pouze klávesnice pro vyhledávání a filtrování?
Vyhledávání a filtrování byla vysoce optimalizována pro uživatele, kteří dávají přednost interakci bez myši, aby s daty pracovali efektivně. Existuje celá řada klávesových zkratek, které lze použít postupně pro rychlou práci. Další informace naleznete v [Klávesové zkratky](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Je podokno filtrů dostupné ve všech seznamech?
Podokno filtrů je k dispozici na stránkách, kde je seznam primárním obsahem na stránce, jako jsou sešity a stránky seznamu, včetně seznamů dostupných na navigačním panelu. Podokno filtrů zatím není k dispozici pro vložené seznamy, například prodejní řádky v prodejních objednávkách, ani pro seznamy s dynamickými sloupci (často označované jako maticové stránky)

## <a name="how-can-i-save-my-filters"></a>Jak mohu uložit mé filtry?

Vaše filtry a úpravy předdefinovaných filtrů jsou zapamatovány po celou dobu relace (po dobu, co jste přihlášeni), i když opustíte stránku. V současné době není možné trvale ukládat filtry. Na rozdíl od filtrů hledaný text není zapamatován, když opustíte stránku.

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Je to stejné jako Pokročilé filtry a Omezení součtů v Microsoft Dynamics NAV?
[!INCLUDE[d365fin](includes/d365fin_md.md)] staví na těchto oblíbených funkcích a poskytuje moderní a vysoce použitelné zkušenosti pro vyhledávání a analýzu vašich dat. Pomocí více klávesových zkratek a zavedení vyhledávání [!INCLUDE[d365fin](includes/d365fin_md.md)] překonává funkce poskytované v Dynamics NAV.

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Mohu vyhledávat a filtrovat pomocí aplikací pro doprovodná zařízení a aplikace Outlook AddIn?
Na různých zobrazení, jako jsou mobilní zařízení nebo v aplikaci Outlook, můžete vyhledávat v seznamech, ale ve většině případů nelze filtrovat v jednotlivých polích.

## <a name="is-the-filter-pane-available-for-filtering-reports"></a>Je podokno filtrů dostupné pro filtrování sestav?
Ne. V současné době dialogové okno filtru sestav, běžně označované jako stránka požadavku, používá jinou možnost, která poskytuje některé, ale ne všechny, možnosti podokna filtrů.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Rozšíří Microsoft možnosti podokna filtrů?
V Microsoftu neustále posloucháme zpětnou vazbu od naší rozmanité komunity uživatelů a jednáme podle nejlepších návrhů této komunity. Pokud máte zájem rozšířit podokno filtrů do více provedeních, více typů seznamů a sestav, nebo máte skvělý nápad, jak jej vylepšit, přidejte tento nápad nebo hlasujte pro existující nápady na stránce [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Mohu něco udělat se zprávou “Hledání řádků trvá příliš dlouho“?

Existuje časový limit, jak dlouho může operace vyhledávání trvat. Nejprve zkuste změnit kritéria vyhledávání a znovu hledat. Pokud používáte místní [!INCLUDE[prodshort](includes/prodshort.md)], obraťte se na správce systému, protože správce může prodloužit lhůtu pro vyhledávání.

Jako místní správce zvýšíte časový limit pro vyhledává změnou nastavení **Časový limit hledání** [!INCLUDE[prodshort](includes/prodshort.md)] serveru. Pro více informací navštivte [Konfigurace Business Central serveru](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) v Business Central Developer and IT Pro Help.

## <a name="see-also"></a>Viz také
[Začínáme](product-get-started.md)  
[Třídění Vyhledávání a Filtrování Seznamů](ui-enter-criteria-filters.md)
