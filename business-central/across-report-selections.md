---
title: Report Selection in Business Central
description: Learn about how to set up the reports that you use to print various types of documents in Business Central.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 04/01/2021
ms.author: edupont

---
# Výber sestav v Business Central

Můžete nastavit výchozí sestavy, které se použijí k tisku různých dokladů pro nákup a prodej, jako jsou například objednávky, nabídky, faktury a dobropisy. Máte-li například určité rozložení pro prodejní faktury, můžete tuto sestavu zadat na stránce **Výběr sestav - prodej**, aby bylo použito rozložení k odesílání nebo tisku prodejních faktur.

Stránky **Výběry sestav** určují, které sestavy se vytisknou v různých situacích. [!INCLUDE [prod_short](includes/prod_short.md)] obsahuje výchozí konfiguraci, ale tyto výchozí hodnoty samozřejmě můžete změnit. Můžete například přidat sestavy na stránky **Výběry sestav**, pokud chcete, například, vytisknout více než jednu sestavu za každý typ dokladu.

## Dostupné výběry sestav

[!INCLUDE [prod_short](includes/prod_short.md)] obsahuje růžné **Výběry sestav** pro různé oblasti. Následující tabulky popisují, kde najdete informace o různých stránkách.

| Oblast nebo úkol | Zjistěte více |
|--------------|----------|
| Příklad, jak fungují Výběry sestav (Prodej) | [Výběry sestav pro prodejní doklady](#example-report-selection-for-sales-documents) |
| Výchozí rozložení e-mailů s prodejními a nákupními doklady | [Nastavení opakovaně použitelných e-mailů a rozvržení pro prodejní a nákupní doklady](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
| Definice rozvržení šeků | [Výběr rozvržení šeků](finance-how-define-check-layouts.md) |
| Definice sestavy pro vykazování DPH (Německo) | [Nastavení sestav pro DPH a intrastat](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> Váš [!INCLUDE [prod_short](includes/prod_short.md)] může zahrovat další stránky **Výběrů sestav** v závislosti na Vaší lokalitě a odvětví. Nastavení můžete kdykoli zkontrolovat tak, že vyberete ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") , zadejte **Výběry sestav** a poté vyberte související odkaz.

Výchozí verze [!INCLUDE [prod_short](includes/prod_short.md)] obsahuje následující stránky **Výběrů sestav**:

* **Výběr sestav - prodej**
* **Výběr sestav - nákup**
* **Výběr sestav - zásoby**
* **Výběr sestav - cash flow**
* **Výběr sestav - sklad**
* **Výběry sestav bankovního účtu**
* **Výběr sestav - upomínka/penále**

## Příklad: Výběr sestavy pro prodejní doklady

Stránka **Výběr sestav - prodej** definuje výchozí sestavy, které se mají použít v různých scénářích pro každý související typ dokladu. Vyberte typ dokladu v poli **Použití** a pak přidejte nebo zkontrolujte výběr sestavy. Můžete nastavit více sestav a pořadí, ve které budou sestavy odeslány nebo vytištěny.

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Některé typy dokladů lze odeslat jako přílohy e-mailu a jiné ne. každá stránka **Výběru sestav** zobrazuje další pole, pokud jsou podporovány pro e-maily.

Například, na stránkách **Výběr sestav - nákup** a **Výběr sestav - nákup** vám následující pole pomohou nastavit e-maily:

| Název pole | Popis |
|-----------|-------------|
| **Použít pro tělo e-mailu** | Určuje, že souhrnné informace, například číslo faktury, datum splatnosti a odkaz na platební bránu, budou vloženy do těla odesílaného e-mailu |
| **Použití pro přílohu e-mailu** | Určuje, že související doklad bude připojen k e-mailu. |
| **Popis rozvržení těla e-mailu** | Určuje použité rozvržení těla e-mailu, obvykle vlastní rozvržení sestavy. |

## Viz také

[Nastavení opakovaně používaných e-mailů a rozvržení pro prodejní a nákupní doklady](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[Výběr rozvržení šeku](finance-how-define-check-layouts.md)  
[Nastavení sestav pro DPH a intrastat (Germany)](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[Správa rozvržení sestav a dokladů](ui-manage-report-layouts.md)  
[Definice rozvržení dokladů pro zákazníky a dodavatele](ui-define-customer-vendor-document-layouts.md)  
[Nastavení tiskáren](ui-specify-printer-selection-reports.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]