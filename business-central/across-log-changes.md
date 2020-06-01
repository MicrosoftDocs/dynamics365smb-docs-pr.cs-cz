---
title: Auditing changes| Microsoft Docs
description: You can activate a user log so that you have a history of any changes made to data in tracked tables. You can also track activities with certain types of activity logs.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont

---
# Změny auditování v Business Central

Abyste v [!INCLUDE[d365fin](includes/d365fin_md.md)] měli historii aktivit, můžete povolit protokol změn. Protokol je založen na změnách dat provedených v tabulkách, které sledujete. Na stránce **Položky protokolu změn**, jsou položky chronologicky seřazeny a zobrazují změny, které jsou provedeny v polích v zadaných tabulkách. Protokol změn shromažďuje všechny změny provedené v tabulce.

> [!Important]
> Změny uživatele nejsou v **Položkách protokolu změn** viditelné, dokud není relace uživatele restartována, což se děje v následujících případech:
<br />
> * Platnost relace vypršela a byla obnovena.
> * Uživatel vybral jinou společnost nebo Centrum rolí.
> * Uživatel se odhlásil a znovu se přihlásil.

## Práce s protokolem změn

Běžným problémem v mnoha finančních systémech je nalezení původu chyb a změn v datech. Může to být cokoli od nesprávného telefonního čísla zákazníka po nesprávné zaúčtování do hlavní knihy. Protokol změn umožňuje sledovat všechny přímé úpravy dat v databázi, které uživatel provádí. Je nutné zadat každou tabulku a pole, které má systém protokolovat, a potom je nutné protokol změn aktivovat.

Protokol změn aktivujete a deaktivujete na stránce **Nastavení protokolu změn**. Když uživatel aktivuje nebo deaktivuje protokol změn, je tato aktivita zaznamenána, takže můžete vždy vidět, který uživatel deaktivoval nebo aktivoval protokol změn.

Pokud na stránce **Nastavení protokolu změn** zvolíte akci **Tabulka**, můžete určit, pro které tabulky chcete sledovat změny a které změny chcete sledovat. [!INCLUDE[d365fin](includes/d365fin_md.md)] také sleduje řadu systémových tabulek.

Po nastavení protokolu změn, jeho aktivaci a změně dat můžete zobrazit a filtrovat změny na stránce **Položky protokolu změn**. Chcete-li odstranit položky, můžete tak učinit na stránce **Odstranění položek prot.změn**, kde můžete nastavit filtry na základě dat a času.

## Práce s protokoly aktivit

Na některých stránkách v [!INCLUDE [prodshort](includes/prodshort.md)], můžete zobrazit protokol aktivity, který zobrazuje stav a případné chyby souborů, které exportujete nebo importujete do [!INCLUDE [prodshort](includes/prodshort.md)].

Informace je zobrazena na stránce **Protokol aktivity**, podle kontextu, ze kterého je otevřena. Okno můžete například otevřít ze stránek **Nastavení služby výměny dokladů**, **Došlý doklad**, **Zaúčtovaná faktura servisu**, a **Účtovaný prodejní dobropis**. Můžete také vyprázdnit seznam záznamů v protokolu, nebo pouze vymazat seznam položek starších než 7 dnů.

## Viz také
[Změna základního nastavení](ui-change-basic-settings.md)  
[Řazení, vyhledávání a filtrování](ui-enter-criteria-filters.md)  
[Hledání funkcí a informací](ui-search.md)  
[Přiřazení oprávnění uživatelům a skupinám](ui-define-granular-permissions.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
