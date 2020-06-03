---
title: Czech Local Functionality - General ledger entries application | Microsoft Docs
description: This section describes local functionality - General ledger entries application
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, finance, CZ, General ledger, Entries
ms.date: 12/30/2019
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Vyrovnání věcných položek

Kromě vyrovnání položek zákazníka a položek dodavatele byla doplněna funkcionalita vyrovnání věcných položek. Vyrovnání věcných položek se obvykle používá s cílem umožnit společnostem práci s dočasnými a převodovými účty ve financích. Dočasné a převodové účty se používají jako dočasné "úložiště" a obsahují částky (věcné položky), které čekají na další zpracování. Nová funkce umožňuje uživatelům propojit jednotlivé položky na účtu (např. předpis se zúčtováním) pomocí nových funkcí vyrovnání a zrušení vyrovnání a společnostem umožňuje vidět analytické souhrny pomocí nových sestav: Otevřené věcné položky k datu nebo Inventura účtu k datu pro určitý den.

Struktura věcných položek byla doplněna o nové úložiště informací o vyrovnání věcných položek. Tabulka Detailní věcné položky obsahuje všechny položky vztahující se k původní věcné položce a ukládá částku vyrovnání, zatímco v tabulce Věcná položka se nachází v kalkulovaném poli Vyrovnaná částka tato částka celkově.  

Do uživatelského rozhraní na stránce Věcné položky byly přidány funkce **Vyrovnat položky** a **Zrušit vyrovnání položek**.  
Částečné vyrovnání je povoleno. Zbývající částka pro vyrovnání je zobrazena ve věcné položce. Uživatel může nastavit vyrovnání položek i před účtováním ve finančním deníku nebo v pokladně.  

Uživatel může spustit dávkové vyrovnání položek pomocí sestavy **Párování věcných položek**.

## Viz také  

[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](finance.md)
