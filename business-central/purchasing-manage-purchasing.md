---
title: Přehled úloh pro správu nákupu | Micorosoft Docs
description: 'Popisuje úlohy pro správu procesů nákupu, včetně způsobu práce s nákupními fakturami a nákupními objednávkami.'
services: project-madeira
documentationcenter: ''
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.date: 01/15/2020
ms.reviewer: v-zdbice
ms.author: sgroespe
---
# Nákup

Můžete vytvářet nákupní fakturu nebo nákupní objednávku za účelem zaznamenání nákladů na nákupy a sledování závazků. Pokud potřebujete kontrolovat zásoby, nákupní faktury se také používají k dynamické aktualizaci úrovně zásob, takže můžete minimalizovat náklady na zásoby a poskytovat lepší služby zákazníkům. Náklady na nákup, včetně nákladů na služby, a hodnoty zásob, které vyplývají z účtování nákupních faktur, přispívají k údajům o zisku a dalším finančním ukazatelům výkonnosti (KPI) ve Vašem Centru rolí.

Nákupní objednávky musíte použít, pokud nákupní proces vyžaduje, abyste evidovali částečné příjmy na objednávce, například proto, že celé množství nebylo u dodavatele k dispozici. Pokud prodáváte zboží s dodáním přímo od dodavatele zákazníkovi jako přímou dodávku, musíte také použít nákupní objednávky. Pro více informací navštivte [Vytvoření přímé dodávky](sales-how-drop-shipment.md). Ve všech ostatních případech fungují nákupní objednávky stejným způsobem jako nákupní faktury.

Nákupní faktury lze vytvářet automaticky s využitím služby OCR (Optical Character Recognition) k převodu PDF faktur od dodavatelů na elektronické dokumenty, které jsou pak převedeny na nákupní faktury. Chcete-li tuto funkci použít, musíte se nejprve zaregistrovat do služby OCR a poté provést různá nastavení. Pro více informací navštivte [Zpracování Došlých dokladů](across-process-income-documents.md).

Produkty mohou být skladové položky i služby. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).

Do všech nákupních procesů můžete zahrnout Workflow pro schvalování, které například vyžaduje, aby byl velký nákup schválen finančním manažerem. Pro více informací navštivte [Použití Workflow schvalování](across-how-use-approval-workflows.md).

Následující tabulka popisuje přehled úloh s odkazy na témata, které je popisují.

| Funkce | Odkaz |
| --- | --- |
|Vytvořte kartu dodavatele pro každého dodavatele, od kterého nakupujete.|[Evidence nových dodavatelů](purchasing-how-register-new-vendors.md)|
|Vytvořte nákupní poptávku, která bude odrážet požadavek na nabídku od Vašeho dodavatele, kterou můžete později převést na nákupní objednávku.|[Vytvoření nákupní poptávky](purchasing-how-request-quotes.md)|
|Vytvořte nákupní fakturu za účelem zaznamenání smlouvy s dodavatelem za účelem zakoupení produktů s určitými dodacími a platebními podmínkami.|[Evidence nákupu](purchasing-how-record-purchases.md) |
|Vytvořte nákupní fakturu pro všechny nebo vybrané řádky na prodejní faktuře.|[Nákup zboží pro prodej](purchasing-how-purchase-products-sale.md) |
|Pochopte, co se stane, když zaúčtujete nákupní doklady.|[Účtování účtování](ui-post-purchases.md) |
|Proveďte akce u nezaplacené zaúčtované nákupní faktury pro automatické vytvoření dobropisu a stornování nákupní faktury nebo jejího opětovné vytvoření, aby bylo možné provést opravy.|[Opravit nebo zrušit nezaplacené nákupní faktury](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)|
|Vytvořte nákupní dobropis pro vrácení určité zaúčtované nákupní faktury, který odráží produkty vracející se dodavateli a částku platby, kterou chcete vrátit.|[Zpracování nákupní vratky nebo storna](purchasing-how-register-new-vendors.md) |
|Spravujte svůj závazek vůči dodavateli nakupovat velké množství dodávané v několika zásilkách v průběhu času.|[Práce s hromadnými nákupními objednávkami](purchasing-how-to-create-blanket-purchase-orders.md)|
|Připravte fakturaci více příjmů od stejného dodavatele  kombinací příjemek do jedné faktury.|[Kombinování příjmů do jedné faktury](purchasing-how-to-combine-receipts.md)|
|Převeďte, např. elektronickou fakturu od dodavatele na nákupní fakturu v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Příjem a převod elektronických dokumentů](purchasing-how-to-receive-and-convert-electronic-documents.md)|
|Naučte se, jak [!INCLUDE[d365fin](includes/d365fin_md.md)] počítá, kdy musíte objednat zboží, aby se bylo přijato k určitému datu.|[Výpočet dat pro nákupy](purchasing-date-calculation-for-purchases.md)|
|Vyřešte konflikt, pokud existují dva nebo více záznamů pro stejného dodavatele.|[Sloučit duplicitní záznamy](sales-how-merge-duplicate-records.md)|

## Navštivte související školení na [Microsoft Learn](/learn/paths/sell-items-services-dynamics-365-business-central/)

## Viz také

[Nastavení nákupu](purchasing-setup-purchasing.md)  
[Evidence nových dodavatelům](purchasing-how-register-new-vendors.md)  
[Správa pohledávek](receivables-manage-receivables.md)  
[Správa závazků](payables-manage-payables.md)  
[Správa projektů](projects-manage-projects.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
