---
title: Set up data exchange | Microsoft Docs
description: Set up the data exchange framework in Business Central.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 10/01/2019
ms.author: sgroespe

---
# Nastavení výměny dat
Než budete moci odesílat a přijímat elektronické dokumenty nebo importovat a exportovat bankovní soubory, musíte nastavit rámec pro výměnu dat pro zpracování příslušných datových souborů. Kromě toho je nutné nastavit související oblasti, jako například zákazníky, kterým odesíláte elektronické faktury, nebo rozšíření AMC Banking 365 Fundamentals, pokud používáte externí poskytovatele služeb k převodu bankovních souborů. Pro více informací navštivte [Elektronická výměna dat](across-data-exchange.md).

Když je [!INCLUDE[d365fin](includes/d365fin_md.md)] nastaven na výměnu dat s externími soubory, mohou uživatele toto nastavení použít v běžných obchodních úlohách, jako je odesílání a přijímání elektronických dokumentů a import a export bankovních souborů.

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| **Viz** | **Také** |
|------------|-------------|  
| Nastavte předkonfigurovanou službu výměny dokumentů tak, aby umožňovala odesílání a přijímání elektronických dokumentů do a z [!INCLUDE[d365fin](includes/d365fin_md.md)]. | [Nastavení služby směnných kurzů](across-how-to-set-up-a-document-exchange-service.md) |
| Nastavte předkonfigurovanou službu OCR tak, aby přeměnila soubory obrazové, nebo PDF soubory na elektronické dokumenty, které lze převést na záznamy dokumentů v [!INCLUDE[d365fin](includes/d365fin_md.md)] | [Nastavení Příchozích dokumentů](across-how-setup-income-documents.md) |
| Nastavte jednu ze dvou předkonfigurovaných služeb pro aktualizované směnné kurzy, abyste získali nejnovější směnné kurzy na stránce **Měny**. | [Aktualizace směnných kurzů](finance-how-update-currencies.md) |
| Nastavte různá hlavní data, jako jsou informace o společnosti, zákaznících, dodavatelích, zboží a měrné jednotky, související s mapováním dat v [!INCLUDE[d365fin](includes/d365fin_md.md)] | [Nastavení odesílání a přijímání elektronického dokladu](across-how-to-set-up-electronic-document-sending-and-receiving.md) |
| Nastavte bankovní účet, dodavatele a deník plateb pro převod SEPA. | [Nastavení převodu SEPA](finance-how-to-set-up-sepa-credit-transfer.md) |
| Připravte si formáty bankovních účtů, způsoby platby a smlouvy se zákazníky pro příkaz k inkasu SEPA. | [Nastavení SEPA – příkaz k inkasu](finance-how-to-set-up-sepa-direct-debit.md) |
| Nastavte ověřování uživatelů a adresu URL poskytovatele služeb převodu bankovních údajů, který má převádět bankovní soubory do formátu vaší banky. | [Používání rozšíření AMC Banking 365 Fundamentals ](ui-extensions-amc-banking.md) |
| Nastavte a povolte externí službu, která umožňuje importovat bankovní výpisy přímo jako bankovní kanál. | [Nastavení služby bankovních výpisů](bank-how-setup-bank-statement-service.md) |
| Po aktivaci služby Bankovní výpisů propojte bankovní účty v [!INCLUDE[d365fin](includes/d365fin_md.md)] | [Nastavení bankovních účtů](bank-how-setup-bank-accounts.md) |
| Připravte se na nastavení nové definice výměny dat pro datový soubor nebo datový proud pomocí souborového schéma XML a předvyplňte záložky **Definice sloupce** na stránce **Definice výměny účtovaných dat**. | [Použití schémat XML k přípravě definic datových výměn](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md) |
| Nastavte rámec pro výměnu dat, který uživatelům umožní přijímat nový formát nákupních dokladů, odesílat nový formát prodejních dokladů, importovat nový bankovní soubor nebo vyměňovat jiné údaje. | [Nastavení definice výměny dat](across-how-to-set-up-data-exchange-definitions.md) |

## Viz také
[Elektronická výměna dat](across-data-exchange.md)  
[Výměna dat](across-exchange-data.md)  
[Došlé doklady](across-income-documents.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)
