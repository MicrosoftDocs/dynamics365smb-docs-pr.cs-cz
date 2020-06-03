---
title: Create a Sales Invoice or Sales Order | Microsoft Docs
description: Describes how to create a bill of sale, or a sales invoice or sales order, to record your agreement with a customer to sell products under specific terms.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 10/01/2019
ms.author: sgroespe

---
# Fakturace prodeje
Můžete vytvořit prodejní fakturu nebo prodejní objednávku, která zaznamená vaši smlouvu se zákazníkem o prodeji určitých produktů za určitých dodacích a platebních podmínek.

Existuje několik scénářů, ve kterých musíte místo prodejní faktury použít prodejní objednávku:

* Pokud potřebujete zasílat pouze část množství objednávky, například proto, že celé množství není na skladě.
* Pokud prodáváte zboží, které váš dodavatel doručuje přímo zákazníkovi, označované jako přímá dodávka zboží. Pro více informací navštivte [Vytvoření přímé dodávky](sales-how-drop-shipment.md).

Ve všech ostatních aspektech fungují prodejní objednávky a prodejní faktury stejným způsobem. Pro více informací navštivte [Prodej produktů](sales-how-sell-products.md).

Se zákazníkem můžete jednat nejprve vytvořením prodejní nabídky, kterou, když se na prodeji dohodnete, můžete převést na prodejní fakturu. Pro více informací navštivte [Vytváření prodejních nabídek](sales-how-make-offers.md).

Pokud se zákazník rozhodne koupit, zaúčtujete prodejní fakturu a vytvoříte související položky množství a hodnoty. Když zaúčtujete prodejní fakturu, můžete dokument odeslat také e-mailem, jako přílohu PDF. Můžete mít tělo e-mailu předvyplněno souhrnem faktury a platebními údaji, jako je například odkaz na PayPal. Pro více informací navštivte [Odesílání dokladů e-mailem](ui-how-send-documents-email.md). Když zákazník pak zaplatí fakturu, můžete tuto platbu zaregistrovat různými způsoby v závislosti na velikosti a upřednostňovaných pracovních postupech vaší organizace. Pro více informací navštivte sekci [Registrace plateb](#registering-payments) section.


Zaúčtované prodejní faktury můžete před zaplacením snadno opravit nebo zrušit. To je například užitečné, pokud chcete opravit chybu při psaní nebo pokud zákazník požaduje změnu v rané fázi procesu objednávky. Pro více informací navštivte [Opravit nebo zrušit nezaplacené prodejní faktury](sales-how-correct-cancel-sales-invoice.md). Pokud je zaúčtovaná prodejní faktura již zaplacena, musíte vytvořit prodejní dobropis, abyste tento prodej stornovali. Pro více informací navštivte [Zpracování prodejní vratky nebo stornování](sales-how-process-sales-returns-cancellations.md).


Karta zboží může být typu **Zásoby**, **Služby**, nebo **Neskladované** k určení, zda je zboží fyzickou skladovou jednotkou, jednotkou pracovní doby nebo fyzickou jednotkou, která není ve skladě. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md). Otevřete seznam prodejních faktur, kde můžete fakturovat zboží nebo služby.

Pole zákazníka na prodejní faktuře můžete vyplnit dvěma způsoby v závislosti na tom, zda je zákazník již zaregistrován. Viz kroky 2 a 3 v následujícím postupu.

## Vytvoření prodejní faktury
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktury** a poté vyberte související odkaz.
2. Do pole **Zákazník** zadejte jméno stávajícího zákazníka.

   Ostatní pole na stránce **Prodejní faktury** obsahují standardní informace o vybraném zákazníkovi. Pokud zákazník není zaregistrován, postupujte takto:
3. Do pole **Zákazník**, zadejte jméno nového zákazníka.
4. V dialogovém okně o registraci nového zákazníka vyberte tlačítko **Ano**.
5. Na stránce **Vybrat šablonu pro nového zákazníka** vyberte šablonu, kterou chcete použít pro novou kartu zákazníka a zvolte tlačítko **OK**.
6. Nová zákaznická karta zobrazuje informace o vybrané zákaznické šabloně. Vyplňte zbývající pole. Pro více informací navštivte [Evidence nového zákazníka](sales-how-register-new-customers.md).  
7. Po dokončení nové šablony zákazníka vyberte tlačítko **OK** a vraťte se na stránku **Prodejní faktury**.

   Několik polí na prodejní faktuře je nyní vyplněno informacemi, které jste zadali na nové kartě zákazníka.
8. Podle potřeby vyplňte zbývající pole na stránce **Prodejní faktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Pokud zákazníkovi dovolíte platit okamžitě, například v hotovosti nebo PayPal, vyplňte pole **Kód způsobu platby**. Platba je pak zaznamenána, jakmile zaúčtujete prodejní fakturu. Pokud vyberete možnost HOTOVĚ, bude platba zaznamenána na určeném protiúčtu.

   Nyní jste připraveni vyplnit řádky prodejní faktury pro produkty, které prodáváte zákazníkovi, nebo pro jakoukoli transakci se zákazníkem, kterou chcete zaznamenat na finančních účtech.

   Pokud jste pro zákazníka nastavili opakující se prodejní řádky, například měsíční objednávky doplnění, tyto řádky můžete vložit do objednávky výběrem akce **Získat periodické prodejní řádky**.  
9. V záložce s náhledem **Řádky**, v poli **Typ**, vyberte, jaký typ produktu, platby nebo transakce, které zaúčtujete zákazníkovi s prodejní řádkem.
10. V poli **Číslo**, vyberte záznam, který chcete odeslat, podle hodnoty v poli **Typ**.

   Pole **Číslo** ponecháte prázdné v následujících případech:

   * Pokud je řádek pro komentář. Napište do pole **Popis** komentář.
   * Pokud je řádek pro položku katalogu. Vyberte akci **Vybrat zboží katalogu**. Pro více informací navštivte [Práce se katalogovým zbožím](inventory-how-work-nonstock-items.md).

11. V poli **Množství**, zadejte, kolik jednotek produktu, poplatku nebo transakce bude řádek pro zákazníka zaznamenávat.

   > [!NOTE]
   > Pokud je zboží typu **Služba**, nebo pole **Typ** obsahuje **Zdroj**, pak je množství časovou jednotkou, jako například hodiny, jak je uvedeno na řádku v poli **Kód měrné jednotky**. Pro více informací navštivte [Nastavení měrných jednotek zboží](inventory-how-setup-units-of-measure.md)

   Hodnota v poli **Částka řádku** se vypočítá jako *Jednotková cena* krát *Množství*.

   Částky ceny a řádku jsou s nebo bez DPH, v závislosti na tom, co jste vybrali v poli **Ceny včetně daně** na kartě zákazníka.  
12. Pokud chcete poskytnout slevu, zadejte procento do pole **Řádková sleva %**. Hodnota v poli **Částka řádku** se odpovídajícím způsobem aktualizuje.

   Pokud jsou speciální ceny položek nastaveny na záložce s náhledem **Prodejní ceny a prodejní řádkové slevy** na kartě zákazníka, nebo zboží, cena a částka na prodejním řádku se automaticky aktualizují, pokud jsou cenová kritéria splněna. Pro více informací navštivte [Evidence speciálních prodejních cen a slev](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Opakujte kroky 9 až 12 pro každý produkt nebo poplatek, který chcete zákazníkovi fakturovat.

   Pole součtů pod řádky se automaticky aktualizují při vytváření nebo úpravě řádků, aby se zobrazily částky, které budou zaúčtovány do účetních knih.

   > [!NOTE]
   > Ve velmi vzácných případech se zaúčtované částky mohou lišit od toho, co je zobrazeno v polích součtů. To je obvykle způsobeno výpočty zaokrouhlování ve vztahu k DPH nebo prodejní dani.<br /><br />Ke kontrole částek, které budou skutečně zaúčtovány, můžete použít stránku **Statistika**, která bere v úvahu výpočty zaokrouhlení. Pokud také zvolíte akci **Vydat**, budou součty aktualizovány tak, aby zahrnovaly výpočty zaokrouhlování.
14. Do pole **Částka fakturační slevy**, zadejte částku, která má být odečtena z hodnoty uvedené v poli **Celkem včetně  DPH**.

   Pokud jste pro zákazníka nastavili slevy na faktuře, zadaná procentuální hodnota se automaticky vloží do pole **Fakturační sleva %** pokud jsou splněna kritéria, a související částka je vložena do pole **Částka fakturační slevy bez DPH**. Pro více informací navštivte [Evidence speciálních prodejních cen a slev](sales-how-record-sales-price-discount-payment-agreements.md).  
15. Po dokončení řádků prodejní faktury vyberte akci **Účtovat a odeslat**.

Dialogové okno **Zaúčtovat a odeslat potvrzení** zobrazuje zákazníkův preferovaný způsob přijímání dokumentů. Metodu odesílání můžete změnit výběrem vyhledávacího tlačítka pro pole **Odeslat doklad (komu)**. Pro více informací navštivte [Nastavení profilů odesílání dokladů](sales-how-setup-document-send-profiles.md).

Související položky a účetní knihy zákazníka jsou nyní vytvořeny ve vašem systému a prodejní faktura je vydána jako dokument PDF. Prodejní faktura je odstraněna ze seznamu prodejních faktur a nahrazena novým dokumentem v seznamu zaúčtovaných prodejních faktur.

## Registrace plateb

V závislosti na vašich obchodních potřebách můžete tuto platbu získat a zaregistrovat ji různými způsoby: ručně, automaticky a prostřednictvím platebních služeb.

Platby můžete zpracovat přímo z karty zákazníka. Pomocí akce **Registrace plateb zákazníka** získáte přehled o nezaplacených fakturách pro daného zákazníka. Poté označte fakturu jako zaplacenou částečně nebo v plné výši. Toto odsouhlasení plateb zpracuje vaše platby zákazníkovi odpovídajícími částkami obdrženými na vašem bankovním účtu se souvisejícími nezaplacenými prodejními fakturami a poté platby odešle. Pro více informací navštivte [Individuální odsouhlasení plateb](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).

V obchodních prostředích, kde zákazník platí nějaký čas po dodání, podle platebních podmínek zůstane zaúčtovaná prodejní faktura otevřená (nezaplacená), dokud oddělení pohledávek neověří, že platba byla přijata, a nepoužije platbu na zaúčtovanou prodejní fakturu. To lze provést ručně nebo automaticky. Pro více informací navštivte [Odsouhlasení plateb zákazníků s deníkem přijaté hotovosti nebo z položek zákazníka](receivables-how-apply-sales-transactions-manually.md) a [Odsouhlasení plateb pomocí automatického vyrovnání](receivables-how-reconcile-payments-auto-application.md).

V obchodních prostředích, kde zákazník okamžitě zaplatí, například prostřednictvím PayPal nebo v hotovosti, je platba zaznamenána okamžitě po zaúčtování prodejní faktury, to znamená, že zaúčtovaná prodejní faktura je uzavřena v plném rozsahu. Příslušnou metodu vyberete na prodejní objednávce v poli **Kód způsobu platby**. Viz krok 8. U elektronických plateb, jako je PayPal, musíte také vyplnit pole **Služba po platby**. Pro více informací navštivte [Povolení plateb zákazníků prostřednictvím platebních služeb](sales-how-enable-payment-service-extensions.md).

Přímo uhrazené faktury pro neregistrované zákazníky můžete dokonce vytvořit tak, že nejprve nastavíte kartu "hotovostního zákazníka", na kterou na prodejní faktuře odkážete. Pro více informací navštivte [Nastavení zákazníků platících hotovosti](finance-how-to-set-up-cash-customers.md).

## Viz také
[Prodej](sales-manage-sales.md)  
[Nastavení Prodeje](sales-setup-sales.md)  
[Zásoby](inventory-manage-inventory.md)  
[Odesílání dokladů e-mailem](ui-how-send-documents-email.md)  
[Provádět hromadnou fakturaci z Microsoft Bookings v Business Central](finance-bookings.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
