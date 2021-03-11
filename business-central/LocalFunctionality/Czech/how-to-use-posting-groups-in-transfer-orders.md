---
title: Czech Local Functionality - Posting groups in Transfer Orders | Microsoft Docs
description: In the Transfer Orders functionality, fields for Gen. Bus. Post. Groups for Ship and Receive posting were added.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Finance, Localization, Transfer Order, Transfer Route, CZ
ms.date: 01/31/2021
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Účto skupiny v Objednávkách transferu

České účetní standardy vyžadují, aby byly transfery účtovány s předepsaným Účtem adjustace Zásob odlišným od ostatních účtování v deníku zboží.

V Trasách transferu byla doplněna pole umožňující zadat obecné obchodní účto skupiny pro účtování dodávky a příjmu. Toto nastavení je automaticky kopírováno do Objednávky transferu na základě použité Trasy transferu. Tato funkcionalita umožňuje účtovat různé Objednávky transferu s různým nastavením obecného účtování a současně lze nastavit odlišné účtování oproti Deníku zboží.  

## Nastavení Tras transferu

Nejprve nastavte pole Obecná obch.úč.sk.dodání a Obecná obch.úč.sk.příjem pro Trasy transferu.

1. Pomocí vyhledávací funkce ![Žárovky, která otevře funkci Řekněte mi, co chcete dělat (Alt + Q)](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat (Alt + Q)") vyhledejte **Trasy transferu**.
2. Zvolte požadovanou kombinaci lokací pro transfer a otevřete **Detaily spec.transferu**.
3. Vyplňte požadované pole a pole Obecná obch.úč.sk.dodání a Obecná obch.úč.sk.příjem.
4. Potvrďte pomocí Zavřít.

## Použití  

Při vytváření Objednávky transferu jsou nastavené účto skupiny automaticky vloženy z Tras transferu pro odpovídající kombinaci skladů, mezi kterými je realizován přesun zboží.

1. Pomocí vyhledávací funkce ![Žárovky, která otevře funkci Řekněte mi, co chcete dělat (Alt + Q)](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat (Alt + Q)") vyhledejte **Objednávky transferu**.
2. Klikněte na funkci **Nový** pro založení nové Objednávky transferu.
3. Zvolte požadovanou lokaci v poli **Transfer z-kód** a **Transfer do-kód**.
4. Dle nastavení Trasy transferu jsou automaticky předvyplněna pole **Obecná obch.úč.sk.dodání** a **Obecná obch.úč.sk.příjem**. Uživatel může dle potřeby tyto výchozí účto skupiny změnit.
5. V řádcích Objednávky transferu vyplňte požadované zboží a množství, které chcete přesouvat z jednoho skladu do druhého.
6. Skladník z prvního skladu zaúčtuje dodání.
7. Skladník z druhého skladu zaúčtuje příjem.
8. Ve Věcných položkách lze provést kontrolu správnosti účtování.

## Viz Také

[Rozšířený lokalizační balíček pro Česko](ui-extensions-advanced-localization-pack-cz.md)  
[Česká lokální funkcionalita](czech-local-functionality.md)
