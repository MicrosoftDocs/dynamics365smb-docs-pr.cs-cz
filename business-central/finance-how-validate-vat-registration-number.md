---
title: Validate a VAT Registration Number | Microsoft Docs
description: Validate a VAT Registration Number
author: andregu
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2020
ms.author: andregu

---

# Ověření daňového identifikačního čísla

## Ověření daňového identifikační čísla
Je důležité, aby čísla DIČ pro zákazníků, dodavatelů a kontaktů byla platná. Společnosti například někdy změní svůj status daňové povinnosti a v některých zemích vás daňové úřady mohou požádat o poskytnutí výkazů, například výkaz přehledu ES přehled prodeje, které uvádějí DIČ, která používáte při podnikání.

Evropská komise poskytuje na svých internetových stránkách službu VIES k ověření daňového identifikačního čísla. [!INCLUDE[d365fin](includes/d365fin_md.md)] ám může ušetřit krok a umožní vám použít službu VIES k ověření a sledování čísel DIČ pro zákazníky, dodavatele a kontakty přímo z karet zákazníka, dodavatele a kontaktů. Služba se v  [!INCLUDE[d365fin](includes/d365fin_md.md)] jmenuje **Nastavení služby Ověření EU DIČ**. Služba je k dispozici na stránce **Služba spojení** a můžete ji ihned začít používat. Připojení služby je zdarma a registrace není vyžadována.

Aby bylo možné povolit **Nastavení . služby ověření EU DIČ** otevřete položku na stránce **Služba spojení**. Pole **Koncový bod služby** by již mělo být vyplněno. Pokud ne, můžete použít **Nastavit výchozí koncový bod služby**. Poté nastavte pole **Povoleno** a můžete začít.

> [!Note]
> Pro zapnutí Nastavení služby ověření EU DIČ, musíte mít oprávnění správce.

Když používáte naše servisní připojení, zaznamenáváme historii čísel DPH a ověření pro každého zákazníka, dodavatele nebo kontakt v **Protokol ověření DIČ**, takže je můžete snadno sledovat. Protokol je specifický pro každého zákazníka. Protokol je například užitečný pro prokázání, že jste ověřili, že aktuální DIČ je správné. Při ověření DIČ bude sloupec **Identifikátor požadavku** v protokolu odrážet, že jste podnikli příslušné kroky.

Protokol registrace DPH můžete zobrazit na kartách zákazníka, dodavatele nebo kontaktu na záložce **Fakturace** výběrem vyhledávacího tlačítka v poli **DIČ**.

Naše služby vám také mohou ušetřit čas při vytváření zákazníka nebo dodavatele. Pokud znáte DIČ zákazníka, můžete ho zadat do pole **DIČ** na kartě zákazníka nebo dodavatele a my pro vás vyplníme jméno zákazníka. Některé země také poskytují adresy společností ve strukturovaném formátu. V těchto zemích také vyplníme adresu.

O službě ověření DIČ ve VIES je potřeba myslet na několik věcí:

* Služba používá protokol http, což znamená, že data přenášená prostřednictvím služby nejsou šifrována.
* U této služby může dojít k výpadkům, za kterou společnost Microsoft nenese odpovědnost. Služba je součástí široké sítě vnitrostátních registrů DPH v EU.

## Viz také
[Nastavení daně z přidané hodnoty ](finance-setup-vat.md)  
[Nastavení nerealizované daně z přidané hodnoty](finance-setup-unrealized-vat.md)      
[Reportování DPH finančímu úřadu](finance-how-report-vat.md)  
[Práce s DPH v prodeji a nákupu](finance-work-with-vat.md)  
[Lokální funkcionality v Business Central](about-localization.md)
