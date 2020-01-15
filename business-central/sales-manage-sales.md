---
title: Přehled úkolů pro správu prodeje | Microsoft Docs
description: Popisuje způsob správy prodejních aktivit.
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, sell'
ms.date: 01/15/2020
ms.reviewer: v-zdbice
ms.author: sgroespe
---
# Prodej

Můžete vytvářet prodejní fakturu nebo prodejní objednávku, abyste evidovali smlouvu se zákazníkem za účelem prodeje určitých produktů za určité dodací a platební podmínky.

Prodejní objednávky je nutné použít, pokud prodejní proces vyžaduje, aby bylo možné dodat objednávku po částech, například proto, že celé množství není najednou k dispozici. Pokud prodáváte zboží dodáním přímo od dodavatele k zákazníkovi jako přímou dodávku, musíte také použít prodejní objednávky. Ve všech ostatních případech fungují prodejní objednávky stejným způsobem jako prodejní faktury. Pomocí prodejních objednávek můžete také pomocí funkce Slíbení objednávky sdělit vašim zákazníkům určitá data dodání.  

Se zákazníkem můžete vyjednávat nejprve vytvořením prodejní nabídky, kterou můžete převést na prodejní fakturu nebo prodejní objednávku, když se na prodeji dohodnete. Poté, co zákazník potvrdí smlouvu, můžete zaslat potvrzení objednávky, aby se zaznamenala vaše povinnost dodat produkty podle dohody.

Zaúčtovanou prodejní fakturu můžete snadno opravit nebo stornovat před zaplacením. To je užitečné v případě, že chcete opravit překlepy, nebo pokud zákazník požádá o změnu v počátečním procesu objednávky. Pokud je Účtovaná prodejní faktura zaplacena, je nutné vytvořit prodejní dobropis nebo objednávku prodejní vratky, aby bylo možné prodej stornovat.

Dobré prodejní a marketingové postupy jsou o tom, jak učinit nejlepší rozhodnutí ve správný čas. Funkcionalita marketingu v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)] poskytuje přesný a včasný přehled o informacích o kontaktech, aby bylo možné efektivněji obsluhovat potenciální zákazníky a zvýšit spokojenost zákazníků. Pro více informací navštivte [Správa vztahů](marketing-relationship-management.md).

V obchodních prostředích, kde musí zákazník zaplatit před dodáním produktů, například v maloobchodě, musíte před dodáním produktů počkat na obdržení platby. Ve většině případů jsou příchozí platby zpracovány několik týdnů po dodání vyrovnáním plateb se souvisejícími zaúčtovanými, nezaplacenými prodejními fakturami. Pro více informací navštivte [Automatické odsouhlasení plateb](receivables-how-reconcile-payments-auto-application.md)

Prodejní doklady mohou být odeslány jako soubory PDF připojené k e-mailu. Tělo e-mailu bude obsahovat výpis prodejního dokladu, například produkty, celkovou částku a odkaz na web služby PayPal. Pro více informací navštivte[Odeslání dokumentů e-mailem](ui-how-send-documents-email.md).

Do všech prodejních procesů můžete zahrnout workflow schvalování, které například vyžaduje, aby byl velký prodej určitým zákazníkům schválen finančním manažerem. Pro více informací navštivte [Použití Workflow](across-use-workflows.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| Funkce | Odkaz |
| --- | --- |
|Vytvořte kartu zákazníka pro každého zákazníka, kterému prodáváte.|[Evidence nových zákazníků](sales-how-register-new-customers.md)|
|Vytvořte prodejní nabídku, kde nabízíte produkty za obchodovatelných podmínek, před převodem nabídky na prodejní fakturu.|[Vytvoření prodejní nabídky](sales-how-make-offers.md) |
|Vytvořte prodejní fakturu za účelem potvrzení smlouvy se zákazníkem za účelem prodeje produktů za určité dodací a platební podmínky.|[Fakturace prodeje](sales-how-invoice-sales.md) |
|Zpracujte prodejní objednávku, která zahrnuje částečné dodání nebo přímou dodávku.|[Prodej produktů](sales-how-sell-products.md) |
|Pochopte, co se stane, když zaúčtujete prodejní doklady.|[Účtování prodeje](ui-post-sales.md) |
|Nastavte standardní prodejní nebo nákupní řádky, které můžete rychle vložit do dokladů, například pro opakující se objednávky na doplnění zásob.|[Vytvořit opakující se prodejní a nákupní řádky](sales-how-work-standard-lines.md)|  
|Propojte prodejní objednávku s nákupní objednávkou pro prodej zboží pomocí přímé dodávky, kdy bude zboží dodáno přímo od vašeho dodavatele k zákazníkovi. |[Vytvoření přímé dodávky](sales-how-drop-shipment.md) |
|Máte katalogové zboží od dodavatele dodané do vašeho skladu, aby bylo možné dodat zboží zákazníkovi.|[Vytvoření speciální objednávky](sales-how-to-create-special-orders.md)|
|Proveďte akce u nezaplacené zaúčtované prodejní faktury za účelem automatického vytvoření dobropisu a stornování prodejní faktury nebo jejího opětovného vytvoření, aby bylo možné provést opravy.|[Opravit nebo zrušit nezaplacené prodejní faktury](sales-how-correct-cancel-sales-invoice.md) |
|Vytvořte prodejní dobropis pro vrácení určité zaúčtované prodejní faktury, který odráží produkty vrácené zákazníkem a částku platby, kterou budete refundovat.|[Zpracování prodejní vratky nebo storna](sales-how-process-sales-returns-cancellations.md) |
|Spravujte závazek zákazníka nakupovat velká množství dodávaná v několika zásilkách v průběhu času.|[Práce s hromadnými prodejními objednávkami](sales-how-to-create-blanket-sales-orders.md)|
|Prodej montovaného zboží, které momentálně není k dispozici, vytvořením propojení na montážní zakázku pro dodání celkového nebo dílčího množství na prodejní objednávce.|[Prodej zboží montovaného na zakázku](assembly-how-to-sell-items-assembled-to-order.md)|
|Fakturujte zákazníkovi jednou za více dodávek kombinováním dodávek do jedné faktury.|[Kombinování dodávek do jedné faktury](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Informujte své zákazníky o datech dodání výpočtem buď data "možné slíbit", nebo data "lze slíbit".|[Výpočet data příslibu objednávek](sales-how-to-calculate-order-promising-dates.md)|
|Zaregistrujte své odhady budoucích prodejů dle zboží a období, aby fungovaly hlavně jako vstup do plánování výroby.|[Vytvořte prognózy](production-how-to-create-a-forecast.md)|
|Řešení konfliktu, pokud existují dva nebo více záznamů pro stejného zákazníka.|[Sloučit duplicitní záznamy](sales-how-merge-duplicate-records.md)|

## Navštivte související školení na [Microsoft Learn](/learn/paths/sell-items-services-dynamics-365-business-central/)

## Viz také

[Nastavení prodeje](sales-setup-sales.md)  
[Evidence nových zákazníků](sales-how-register-new-customers.md)  
[Správa pohledávek](receivables-manage-receivables.md)  
[Správa závazků](payables-manage-payables.md)  
[Správa projektů](projects-manage-projects.md)     
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
