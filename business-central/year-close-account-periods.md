---
title: Close Accounting Periods for a Fiscal Year | Microsoft Docs
description: Describes how to close the accounting periods that make up the fiscal year.
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
# Uzavírání účetního období
Když skončí fiskální rok, musíte uzavřít období, která jej tvoří.

## Uzavírání účetních období
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní období** a poté vyberte související odkaz.
2. Na stránce **Účetní období** vyberte akci **Uzavřít rok**.

   Pokud je otevřeno více než jeden fiskální rok, je nejbližší fiskální rok automaticky vybrán k uzavření. Zobrazí se zpráva identifikující rok, který bude ukončen, a důsledky uzavření roku.
3. Chcete-li rok zavřít, vyberte tlačítko **Ano**.

Fiskální rok je uzavřen a jsou vybrána pole **Uzavřeno** a **Datum uzavřeno** pro všechna období v roce. Fiskální rok nelze znovu otevřít a nelze zrušit zaškrtnutí z polí **Uzavřeno** nebo **Datum uzavřeno**.

> [!NOTE]
> Fiskální rok nelze zavřít dříve, než vytvoříte nový. Všimněte si, že po uzavření fiskálního roku nelze změnit počáteční datum následujícího fiskálního roku.

Přestože byl fiskální rok uzavřen, můžete do něj stále zaúčtovat položky hlavní knihy. Když tak učiníte, budou položky označeny jako zaúčtované do uzavřeného fiskálního roku a bude vybráno pole **Položka předchozího roku**.

Po uzavření fiskálního roku musíte uzavřít účty výkazu zisku a ztráty a převést výsledky roku na účet v rozvaze. Tuto akci můžete opakovat pokaždé, když pošlete příspěvek do uzavřeného fiskálního roku.

## Viz také
[Uzavírání knih](year-close-books.md)  
[Účtování položky konce roku](year-how-post-year-end-close-entry.md)  
[Otevření nového fiskálního roku](finance-how-open-new-fiscal-year.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
