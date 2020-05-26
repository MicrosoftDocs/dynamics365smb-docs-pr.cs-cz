---
title: Overview of the Tasks for Closing the Books | Microsoft Docs
description: Learn about the process of closing the books for a fiscal year or period, and what happens after you close at the end of a year.
services: project-madeira
documentationcenter: ''
author: jswymer

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2019
ms.author: jswymer

---
# Uzavírání knih
Poté, co se ujistíte, že všechny vaše účty jsou aktuální a náklady a příjmy jsou přideleny, můžete knihy uzavřít na fiskální rok nebo období.

Nejste povinni uzavřít rok, ale díky tomu bude práce v systému pro vás snazší, protože budete moci využít výhodných dostupných možností filtrování. Také se nemusíte starat o ztrátu podrobností o transakcích při uzavření, protože všechny podrobnosti jsou zachovány, a to i po uzavření roku.

## Proces uzavírání knih
Proces uzavření knihy zahrnuje tyto hlavní úkoly:

1. Uzavření účetního období

   Fiskální rok je definován jako jedno nebo více otevřených období, jak je definováno na stránce **Účetní období**. Typický fiskální rok obsahuje 12 období po jednom měsíci, ale můžete také zvolit jinou metodu definování roku.

   Pro více informací navštivte [Uzavírání účetního období](year-close-account-periods.md).
2. Registrace položek z předchozího roku.

   Při uzavření fiskálního roku je nutné zadat počet administrativních transakcí (například předplacené a časově rozlišené položky). Tyto transakce se nazývají úprava položek. Neexistují žádná zvláštní pravidla pro zaúčtování těchto položek a obsahují (stejně jako ostatní položky) zaškrtávací políčko v poli **Položka předchozího roku**, pokud jsou zaúčtovány k datu v uzavřeném fiskálním roce. Přestože byl fiskální rok uzavřen, můžete do něj stále zaúčtovat položky hlavní knihy.
3. Převod zůstatků z účtů výsledovky do rozvahy.

   Po uzavření fiskálního roku a zaúčtování všech záznamů za předchozí rok musí být účty výsledovky uzavřeny a čistý zisk za rok musí být převeden na účet pod vlastním kapitálem v rozvaze. K tomuto účelu použijte dávkovou úlohu Uzavření výsledovky. Dávková úloha zpracuje všechny účty hlavní knihy typu Výsledovka a vytvoří položky, které obrátí jejich zůstatky. Tyto položky jsou umístěny v deníku, ze kterého mohou být zveřejněny. Dávková úloha je nezveřejňuje automaticky, kromě případů, kdy je použita další měna vykazování. Při použití další měny pro hlášení se dávková úloha účtuje přímo do hlavní knihy.

   Pro více informací navštivte [Uzavření výsledovky](year-close-income-statement.md).
4. Zaúčtování položky roční uzávěrky spolu s vyrovnáním položek kapitálového účtu.

   Po dokončení dávkové úlohy Uzavření výsledovky zaúčtujte položky generované touto úlohou. Pokud jste v dávkové úloze nezadali účet nerozděleného zisku, zadejte jeden řádek s vyrovnávací položkou, která zaúčtuje čistý příjem na správný účet hlavní knihy pod vlastním kapitálem v rozvaze. Nakonec zaúčtujte deník.

   Pro více informací navštivte [Účtování položky konce roku](year-how-post-year-end-close-entry.md).

## Co se stane při uzávěrke
Když provedete uzávěrku na konci roku, systém přesune vaše příjmy z vypočtených příjmů na účet nerozděleného zisku. Systém také označí fiskální rok jako „uzavřený“ a všechny následné položky za uzavřený rok označí jako „záznamy předchozího roku“.

Systém poté vygeneruje závěrečný záznam, ale nezaúčtuje jej automaticky. Máte příležitost provést zápis nebo záznamy o započítání vlastního kapitálu, což vám umožní rozhodnout se, jak přiřadit svůj závěrečný záznam. Například, pokud má vaše společnost několik divizí, můžete nechat systém vygenerovat jediný uzavírací záznam pro všechny divize a pak můžete provést vyrovnávací zápis pro majetkový účet každé divize.

Můžete zaúčtovat v předchozím fiskálním roce, a to i po uzavření účtů výsledovky, pokud potom znovu spustíte dávkovou úlohu Uzavření výsledovky.

## Viz také
[Otevření nového fiskálního roku](finance-how-open-new-fiscal-year.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
