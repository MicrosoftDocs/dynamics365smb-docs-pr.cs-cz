---
title: Přehled úkolů pro správu nákupu | Micorosoft Docs
description: 'Popisuje úkoly pro správu procesů nákupu a nákupu, včetně způsobu práce nákupních faktur a nákupních objednávek.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.date: 08/10/2017
ms.author: sgroespe
---
# <a name="purchasing"></a>Nákup
Můžete vytvářet nákupní fakturu nebo nákupní objednávku za účelem zaznamenání nákladů na nákupy a sledování závazků. Pokud potřebujete kontrolovat zásoby, nákupní faktury se také používají k dynamické aktualizaci úrovní zásob, takže můžete minimalizovat náklady na zásoby a poskytovat lepší služby zákazníkům. Náklady na nákup, včetně nákladů na služby a hodnoty zásob, které vyplývají z účtování nákupních faktur, přispívají k údajům o zisku a dalším finančním ukazatelům výkonnosti ve Vašem Centru rolí.

Nákupní objednávky musíte použít, pokud nákupní proces vyžaduje, abyste evidovali částečné příjmy z množství objednávky, například proto, že celé množství nebylo u dodavatele k dispozici. Pokud prodáváte zboží s dodáním přímo od dodavatele zákazníkovi jako přímou dodávku, musíte také použít nákupní objednávky. Pro více informací navštivte [Vytvoření přímé dodávky](sales-how-drop-shipment.md). Ve všech ostatních aspektech fungují nákupní objednávky stejným způsobem jako nákupní faktury.

Nákupní faktury lze vytvářet automaticky pomocí služby OCR (Optical Character Recognition) k převodu faktur PDF od dodavatelů na elektronické dokumenty, které jsou pak převedeny na nákupní faktury. Chcete-li tuto funkci použít, musíte se nejprve zaregistrovat do služby OCR a poté provést různá nastavení. Pro více informací navštivte [Zpracování Došlých dokladů](across-process-income-documents.md).      

Produkty mohou být skladové položky i služby. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).

Pro všechny nákupní procesy můžete zahrnout Workflow pro schvalování, například pro vyžadování, aby účetní manažer schválil velké nákupy. Pro více informací navštivte [Použití Workflow Schvalování](across-how-use-approval-workflows.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.


|                                                                                       Viz                                                                                        |                                                 také                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
|                          Vytvoření nákupní faktury za účelem zaznamenání smlouvy s dodavatelem za účelem zakoupení produktů s určitými dodacími a platebními podmínkami                           |                        [Evidence nákupů](purchasing-how-record-purchases.md)                        |
|                            Vytvořte nákupní poptávku, která bude odrážet požadavek na nabídku od vašeho dodavatele, kterou můžete později převést na nákupní objednávku.                            |                          [Požadavky poptávky](purchasing-how-request-quotes.md)                          |
|                                                     Vytvoření nákupní faktury pro všechny nebo vybrané řádky na prodejní faktuře.                                                     |                [Nákup zboží pro prodej](purchasing-how-purchase-products-sale.md)                 |
| Provedení akce s neplacenou zaúčtovanou nákupní fakturou pro automatické vytvoření dobropisu a stornování nákupní faktury nebo její opětovné vytvoření, aby bylo možné provést opravy | [Opravit nebo zrušit nezaplacené prodejní faktury](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Vytvoření nákupního dobropisu pro vrácení určité zaúčtované nákupní faktury, která odráží produkty vracející se dodavateli a kterou částku platby shromáždíte. |         [Zpracovat nákupní vratky nebo zrušení](purchasing-how-register-new-vendors.md)          |
|                                    Příprava fakturace více příjmů od stejného dodavatele, a to kombinací příjemek na jedné faktuře.                                     |            [Kombinace příjmů na jedné faktuře](purchasing-how-to-combine-receipts.md)             |
|                         Naučte se, jak <x0 /> počítá, když musíte objednat zboží, aby se bylo přijato k určitému datu.[!INCLUDE [d365fin](includes/d365fin_md.md)]                          |            [Výpočet data pro nakupy](purchasing-date-calculation-for-purchases.md)            |

## <a name="see-also"></a>Viz také
[Nastavení nákupu](purchasing-setup-purchasing.md)  
[Evidence nových dodavatelům](purchasing-how-register-new-vendors.md)  
[Správa závazků](payables-manage-payables.md)  
[Správa projektů](projects-manage-projects.md)     
[Práce s[!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)

## [!INCLUDE [d365fin](includes/free_trial_md.md)]  
## [!INCLUDE [d365fin](includes/training_link_md.md)]
