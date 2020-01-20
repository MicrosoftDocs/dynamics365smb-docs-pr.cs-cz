---
title: Přehled úkolů pro správu prodeje | Microsoft Docs
description: Popisuje způsob správy prodejních aktivit.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, sell'
ms.date: 09/08/2017
ms.author: sgroespe
---
# <a name="sales"></a>Prodej
Můžete vytvářet prodejní fakturu nebo prodejní objednávku, abyste evidovali smlouvu se zákazníkem za účelem prodeje určitých produktů za určité dodací a platební podmínky.

Prodejní objednávky je nutné použít, pokud prodejní proces vyžaduje, aby bylo možné dodat části množství objednávky, například proto, že celé množství není najednou k dispozici. Pokud prodáváte zboží dodáním přímo od dodavatele zákazníkovi jako přímou dodávku, musíte také použít prodejní objednávky. Ve všech ostatních aspektech fungují prodejní objednávky stejným způsobem jako prodejní faktury. Pomocí prodejních objednávek můžete také pomocí funkce Slíbení objednávky sdělit vašim zákazníkům určitá data dodání.  

Se zákazníkem můžete jednat nejprve vytvořením prodejní nabídky, kterou můžete převést na prodejní fakturu nebo prodejní objednávku, když se na prodeji dohodnete. Poté, co zákazník potvrdí smlouvu, můžete zaslat potvrzení objednávky, aby se zaznamenala vaše povinnost dodat produkty podle dohody.

Zaúčtovanou prodejní fakturu můžete snadno opravit nebo stornovat před zaplacením. To je užitečné v případě, že chcete opravit překlepy, nebo pokud zákazník požádá o změnu v počátečním procesu objednávky. Pokud je Účtovaná prodejní faktura zaplacena, je nutné vytvořit prodejní dobropis nebo objednávku prodejní vratky, aby bylo možné prodej stornovat.

Dobré prodejní a marketingové postupy jsou o tom, jak učinit nejlepší rozhodnutí ve správný čas. Funkce marketingu v aplikaci [!INCLUDE [d365fin](includes/d365fin_md.md)] poskytuje přesný a včasný přehled o kontaktních informacích, aby bylo možné efektivněji obsluhovat potenciální zákazníky a zvýšit spokojenost zákazníků. Pro více informací navštivte [Správa vztahů](marketing-relationship-management.md).

V obchodních prostředích, kde musí zákazník zaplatit před dodáním produktů, například v maloobchodě, musíte před dodáním produktů počkat na obdržení platby. Ve většině případů jsou příchozí platby zpracovány několik týdnů po dodání uplatněním plateb na související zaúčtované, nezaplacené prodejní faktury. Pro více informací bežte na [Automatické odsouhlasení plateb](receivables-how-reconcile-payments-auto-application.md)

Prodejní doklady mohou být odeslány jako soubory PDF připojené k e-mailu. Tělo e-mailu bude obsahovat výpis prodejního dokladu, například produkty, celkovou částku a odkaz na web služby PayPal. Pro více informací navštivte[Odeslání dokumentů e-mailem](ui-how-send-documents-email.md).

U všech prodejních procesů můžete zahrnout workflow schvalování, který například vyžaduje, aby byl manažer účtování schválen velkým prodejem určitým zákazníkům. Pro více informací navštivte [Použití Workflow](across-use-workflows.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| Viz | také |
| --- | --- |
| Vytvořte prodejní nabídku, kde nabízíte produkty za obchodovatelné podmínky před převodem nabídky na prodejní fakturu. |[Vytváření nabídek](sales-how-make-offers.md) |
| Vytvoření prodejní faktury za účelem zaznamenání smlouvy se zákazníkem za účelem prodeje produktů za určité dodací a platební podmínky |[Fakturace prodeje](sales-how-invoice-sales.md) |
| Zpracování prodejní objednávky, která zahrnuje částečné doručení nebo odeslání. |[Prodávání produktů](sales-how-sell-products.md) |
|Nastavte standardní prodejní nebo nákupní řádky, které můžete rychle vložit do dokladů, například pro opakující se objednávky doplnění.|[Vytvořit opakující se prodejní a nákupní řádky](sales-how-work-standard-lines.md)|  
| Propojení prodejní objednávky s nákupní objednávkou pro prodej zboží pro přímou dodávku, které bude dodáno přímo od vašeho dodavatele k zákazníkovi. |[Vytvoření přímé dodávky](sales-how-drop-shipment.md) |
|Neskladované zboží doručené od dodavatele do vašeho skladu, za účelem dodání vašemu zákazníkovi.|[Vytvoření speciální objednávky](sales-how-to-create-special-orders.md)|
| Provedení akce u neplacené zaúčtované prodejní faktury za účelem automatického vytvoření dobropisu a stornování prodejní faktury nebo její opětovné vytvoření, aby bylo možné provést opravy |[Opravit nebo zrušit nezaplacené prodejní faktury](sales-how-correct-cancel-sales-invoice.md) |
| Vytvoření prodejního dobropis pro vrácení určité zaúčtované prodejní faktury, která odráží produkty vrácené zákazníkem a částku platby, kterou budete refundaci. |[Zpracování prodejní vratky nebo stornování](sales-how-process-sales-returns-cancellations.md) |
|Správa závazků vašich zákazníků pro nakupování velkého množství dodávaného v několika zásilkách v průběhu času.|[Práce s hromadnými prodejními objednávkami](sales-how-to-create-blanket-sales-orders.md)|
|Prodej zboží montáže, které momentálně není k dispozici vytvořením propojení montáže na zakázku pro dodání úplného nebo částečného množství prodejní objednávky.|[Prodejn zboží montáže na obejdnávku](assembly-how-to-sell-items-assembled-to-order.md)|
|Fakturujte zákazníkovi jednou za více zásilek kombinováním dodávek na jedné faktuře.|[Kombinování dodávek na jednu fakturu](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Informujte své zákazníky o datech dodání, a to výpočtem buď data "možné slíbit", nebo data "Lze slíbit".|[Výpočet data příslibu objednávek](sales-how-to-calculate-order-promising-dates.md)|

## <a name="see-also"></a>Viz také
[Nastavení prodeje](sales-setup-sales.md)  
[Evidence nových zákazníků](sales-how-register-new-customers.md)  
[Správa pohledávek](receivables-manage-receivables.md)  
[Správa závazků](payables-manage-payables.md)  
[Správa projektu](projects-manage-projects.md)     
[Práce s[!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)

## [!INCLUDE [d365fin](includes/free_trial_md.md)]  
## [!INCLUDE [d365fin](includes/training_link_md.md)]
