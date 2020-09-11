---
title: Manage database access intent in Business Central | Microsoft Docs
description: Change the database access intent for reports, API pages, and queries.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 04/30/2020
ms.author: jswymer
---
# Správa přístupu databáze

Jako super uživatel nebo správce můžete změnit přístup k databázi například, k sestavám, stránkám typu API a databázovým dotazům, abyste zlepšili výkon služby.

## Přehled

[!INCLUDE[d365fin](includes/d365fin_md.md)] lze nastavit tak, aby používaly repliky primární (číst-psát) databáze pouze pro čtení. Použití replikování databáze snižujete zatížení primární databáze. V některých případech to také zlepší výkon při prohlížení dat v klientovi. Repliky jsou výhodné pro objekty, jako jsou sestavy, dotazy a stránky rozhraní API, které se používají pouze pro zobrazení dat, nikoli pro úpravu dat.

Při spuštění objektů určuje záměr přístupu k databázi, zda se použije replika pouze pro čtení, pokud je k dispozici, nebo se použije primární databáze. Sestavy, stránky API a databázové dotazy jsou vyvíjeny s předdefinovaným záměrem přístupu do databáze [vlastnostní DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

Stránka **Seznam přístupu k databázi** umožňuje přepsat předdefinovaný záměr přístupu k databázi pro objekty při jejich spuštění.

Z hlediska databáze je tato funkce běžně označována jako  *škálování čtení*. Další informace o možnostech škálování čtení a záměru přístupu k datům naleznete v [!INCLUDE[prodshort](includes/prodshort.md)], viz [využití škálování čtení pro lepší výkon](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) v [!INCLUDE[prodshort](includes/prodshort.md)] Vývojařské a Administrátorské nápovědě.

## Změna přístupu k databázi

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Seznam přístupů k databázi** a poté vyberte související odkaz.

   Na stránce jsou uvedeny všechny sestavy, stránky a dotazy. Sloupec **Záměr přístupu** obsahuje jednu z následujících hodnot:

   | **Nastavení** | **Popis** |
   |------------|-------------|  
   | **Výchozí** | Označuje, že objekt používá předdefinovaný záměr přístupu k databázi. |
   | **Povolit zápis** | Nastaví objekt pro použití primární databáze, což umožňuje uživateli upravovat data. |
   | **Jen pro čtení** | Nastaví objekt pro použití repliky databáze, což znamená, že uživatel může pouze zobrazit data, nikoli změnit data. |

2. Vyberte akci **Upravit seznam**.

3. Na stránce **Upravit - Seznam záměru přístupu k databázi**, změňte pole **Záměr přístupu** pro objekt.

   > [!NOTE]
   > Pokud je objekt, který lze upravovat, stejně jako zákaznická karta, nastaven na  **Jen pro čtení**, bude primární databáze stále používána, bez ohledu na záměr přístupu, který umožní uživatelům provádět změny obvyklým způsobem.

## Viz souvisejnící školení [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## Viz také
[Obchodní funkce](across-business-functionality.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Začínáme](product-get-started.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
