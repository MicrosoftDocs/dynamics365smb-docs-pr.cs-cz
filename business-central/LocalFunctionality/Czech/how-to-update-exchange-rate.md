---
title: Czech Local Functionality - Exchange Rate Updating
description: The ability to automatically update currency exchange rates from the CNB (Czech National Bank) in the Czech version of Business Central.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: CZ, Czech, Finance, Exchange Rate, Localization
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Aktualizace směnného kurzu

Společnosti je umožněno automaticky aktualizovat směnné kurzy měn pomocí funkcí Služby směnného kurzu.
Ty byly vylepšeny o možnost automaticky aktualizovat směnné kurzy měn z ČNB (České Národní Banky).
Uživatel si může v nastavení služby směnného kurzu definovat http adresu služby a další parametry aktualizace směnných kurzů.

![Aktualizace směnného kurzu](Media/update-exchange-rates.png)
## Spuštění služby aktualizace směnného kurzu pomocí ČNB
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Služby směnného kurzu** a poté vyberte související odkaz.
2. V seznamu Služeb směnného kurzu vyberte **CNB-EXCHANGE-RATES - Nastavení směnných kurzů České národní banky**.
3. Na kartě služby směnného kurzu vyberte políčko **Povoleno** pro zapnutí služby.
4. Po zapnutí služby systém na pozadí založí položu fronty úloh: **Procedura ∙ 1281 ∙ Update Currency Exchange Rates**, zároveň se Vás systém zeptá, jestli chcete otevřít okno položky fronty úloh a zda chcete tuto položku nastavit.
5. V případě potvrzení, se Vám otevře položka fronty úloh, kterou můžete nastavit dle Vašich potřeb. Můžete zde například nastavit jakou periodou a v kolik hodin se mají směnné kurzy aktualizovat.
6. Po nastavení položky frotny úloh nastavte stav na **Vyčkávat**. Jakmile nastane okamžik aktualizace dle nastavení, procedura se spustí a aktualizuje měny.
7. Kartu položky fronty úloh můžete zavřít.



## Viz také

[Základní lokalizační balíček pro Česko](ui-extensions-core-localization-pack-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
[Finance](finance.md)  

