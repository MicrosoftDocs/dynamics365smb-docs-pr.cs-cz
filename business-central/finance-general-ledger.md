---
title: Learn About General Ledger and COA| Microsoft Docs
description: Describes the general ledger, the chart of accounts, and account categories.
services: project-madeira
documentationcenter: ''
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 10/01/2019
ms.author: edupont

---
# Znalost o hlavní knize a certifikátu pravosti
Hlavní kniha ukládá vaše finanční údaje a účetní osnova zobrazuje účty, do kterých jsou zaúčtovány všechny položky hlavní knihy. [!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje standardní tabulku účtů, která je připravena podpořit vaše podnikání.

## Nastavení financí a obecného účtování
Nastavení financí je jádrem finančních procesů, protože definuje, jak účtovat data.

Na stránce **Nastavení financí** určete, jak řešit určité účetní problémy ve vaší společnosti, například:

* Detaily zaokrouhlení faktury
* Formáty adres
* Finanční výkaznictví

Podobně na stránce **Nastavení obecného účtování** určete, jak chcete nastavit kombinace obecných skupin účtování firem a obecných produktů. Účto skupiny mapují entity, jako jsou zákazníci, dodavatelé, zboží, zdroje a doklady prodeje a nákupu, na finanční účty. Vyplňte řádek pro každou kombinaci obchodní účto skupiny a účto skupiny produktu. Pro více informací navštivte [Nastavení účto skupin](finance-posting-groups.md)

## Účetní osnova
Účetní osnova zobrazuje všechny účty hlavní knihy. Z účetní osnovy můžete dělat věci jako:

* Zobrazit sestavy, které ukazují položky a zůstatky hlavní knihy.
* Zavřít svou výsledovku.
* Chcete-li přidat nebo změnit nastavení, otevřete kartu finančního účtu.
* Podívat se na seznam účto skupin, které účtují na tento účet.
* Zobrazit souhrn MD a DAL částek pro jeden účet

Můžete přidat, změnit nebo odstranit účty hlavní knihy. Chcete-li však zabránit nesrovnalostem, nemůžete smazat účet hlavní knihy, pokud jsou jeho data použita v účetní osnově.

## Kategorie účtu
Strukturu finančních výkazů můžete přizpůsobit mapováním finančních účtů na kategorie účtů.

Na stránce **Kategorie finančního účtu** jsou uvedeny vaše kategorie a podkategorie a účty hlavní knihy, které jsou jim přiřazeny. Můžete vytvořit nové podkategorie a přiřadit tyto kategorie k existujícím účtům.

Skupinu kategorií vytvoříte odsazením dalších podkategorií pod řádkem na stránce **Kategorie finančního účtu**. To vám usnadní získání přehledu, protože každé seskupení vykazuje celkový zůstatek. Můžete například vytvořit podkategorie pro různé typy datových zdrojů a potom vytvořit skupiny kategorií pro dlouhodobý majetek versus běžná aktiva.

Můžete určit, zda účty v každé podkategorii musí být zahrnuty do konkrétních typů sestavy. Kategorie účtů pomáhají definovat rozvržení vašich finančních výkazů.

Například výchozí zůstatek má podkategorii pro hotovost v části běžné aktiva. Pokud chcete, aby výpis zůstatku bral v úvahu pokladní hotovost a kontrolu, můžete:

1. Přidat dvě nové podkategorie. Jednu pro pokladní hotovost a jednu pro váš běžný účet.
2. Pro tyto podkategorie zadat další definici sestavy **Pokladní účty**.
3. Odsadit je v podkategorii **Hotovost**.

Při příštím vygenerování plánů účtu se ve vašem výpisu zůstatku zobrazí celkový zůstatek za hotovost a dva řádky s zůstatky pro pokladní hotovost a běžný účet.

## Viz také
[Finance](finance.md)  
[Nastavení nebo změna účetní osnovy](finance-setup-chart-accounts.md)  
[Business Intelligence](bi.md)
