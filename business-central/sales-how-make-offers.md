---
title: Create a Sales Offer to a Customer | Microsoft Docs
description: Describes how to create a sales offer or a request for proposal (RFQ) document to record your offer to a customer to sell products under certain terms.
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2019
ms.author: sgroespe

---
# Vytváření prodejních nabídek
Prodejní nabídku vytvoříte pro zaznamenání vaší nabídky zákazníkovi k prodeji určitých produktů za určitých dodacích a platebních podmínek. Prodejní nabídku můžete zákazníkovi sdělit, tak, že ji odešlete. Dokument můžete odeslat e-mailem jako přílohu PDF. Můžete také nechat tělo e-mailu předem vyplnit souhrnem nabídky. Pro více informací navštivte [Odesílání dokladů e-mailem](ui-how-send-documents-email.md).

Během vyjednávání se zákazníkem můžete prodejní nabídku změnit a znovu odeslat podle potřeby. Když zákazník přijme nabídku, převedete prodejní nabídku na prodejní fakturu nebo prodejní objednávku, ve které zpracujete prodej. Pro více informací navštivte [Prodejní faktura](sales-how-invoice-sales.md) nebo [Prodávat výrobky](sales-how-sell-products.md).

Pole zákazníka můžete do prodejní nabídky vyplnit dvěma způsoby, podle toho, zda je zákazník již zaregistrován. Viz kroky 2 a 3 v následujícím postupu.

## Vytvoření prodejní nabídky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní nabídky** a poté vyberte související odkaz.
2. Do pole **Zákazník** zadejte jméno stávajícího zákazníka.

   Ostatní pole na stránce **Prodejní nabídka** obsahují standardní informace o vybraném zákazníkovi. Pokud zákazník není zaregistrován, postupujte takto:
3. Do pole **Zákazník**, zadejte jméno nového zákazníka.
4. V dialogovém okně o registraci nového zákazníka vyberte tlačítko **Ano**.
5. Na stránce **Vybrat šablonu pro nového zákazníka** vyberte šablonu, kterou chcete použít pro novou kartu zákazníka a zvolte tlačítko **OK**.
6. Nová zákaznická karta zobrazuje informace o vybrané zákaznické šabloně. Vyplňte zbývající pole. Pro více informací navštivte [Evidence nového zákazníka](sales-how-register-new-customers.md).  
7. Po dokončení karty zákazníka se stisknutím tlačítka **OK** vrátíte na stránku **Prodejní nabídka**.

   Několik polí v prodejní nabídce je nyní vyplněno informacemi, které jste zadali na nové kartě zákazníka.
8. Podle potřeby vyplňte zbývající pole na stránce **Prodejní nabídka**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   Nyní jste připraveni vyplnit řádky prodejní objednávky u produktů, které prodáváte zákazníkovi, nebo pro jakoukoli transakci se zákazníkem, kterou chcete zaznamenat na účet hlavní knihy.

   Pokud jste pro zákazníka nastavili opakující se prodejní řádky, například měsíční objednávky doplnění, tyto řádky můžete vložit do objednávky výběrem akce **Získat periodické prodejní řádky**.  

9. V záložce s náhledem **Řádky**, v poli **Typ**, vyberte, jaký typ produktu, platby nebo transakce, které zaúčtujete zákazníkovi s prodejní řádkem.
10. V poli **Číslo**, vyberte záznam, který chcete odeslat, podle hodnoty v poli **Typ**.

   Pole **Číslo** ponecháte prázdné v následujících případech:
   - Pokud je řádek pro komentář. Napište do pole **Popis** komentář.
   - Pokud je řádek pro položku katalogu. Vyberte akci **Vybrat zboží katalogu**. Pro více informací navštivte [Práce se katalogovým zbožím](inventory-how-work-nonstock-items.md).

11. V poli **Množství**, zadejte, kolik jednotek produktu, poplatku nebo transakce bude řádek pro zákazníka zaznamenávat.

   > [!NOTE]
   > Pokud je zboží typu **Služba**, nebo pole **Typ** obsahuje **Zdroj**, pak je množství časovou jednotkou, jako například hodiny, jak je uvedeno na řádku v poli **Kód měrné jednotky**. Pro více informací navštivte [Nastavení měrných jednotek zboží](inventory-how-setup-units-of-measure.md)

   Hodnota v poli **Částka řádku** se vypočítá jako *Jednotková cena* krát *Množství*.

   Částky ceny a řádku jsou s nebo bez DPH, v závislosti na tom, co jste vybrali v poli **Ceny včetně daně** na kartě zákazníka.  
12. Pokud chcete poskytnout slevu, zadejte procento do pole **Řádková sleva %**. Hodnota v poli **Částka řádku** se odpovídajícím způsobem aktualizuje.

   Pokud jsou speciální ceny položek nastaveny na záložce s náhledem **Prodejní ceny a prodejní řádkové slevy** na kartě zákazníka, nebo zboží, cena a částka na prodejním řádku se automaticky aktualizují, pokud jsou cenová kritéria splněna. Pro více informací navštivte [Evidence speciálních prodejních cen a slev](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Opakujte kroky 9 až 12 pro každý produkt, který chcete zákazníkovi nabídnout.

   Součty pod řádky se automaticky počítají při vytváření nebo úpravách řádků.  
14. Do pole **Částka fakturační slevy**, zadejte částku, která má být odečtena z hodnoty uvedené v poli **Celkem včetně  DPH**.

   Pokud jste pro zákazníka nastavili slevy na faktuře, zadaná procentuální hodnota se automaticky vloží do pole **Fakturační sleva %** pokud jsou splněna kritéria, a související částka je vložena do pole **Částka fakturační slevy bez DPH**. Pro více informací navštivte [Evidence speciálních prodejních cen a slev](sales-how-record-sales-price-discount-payment-agreements.md).  

   > [!TIP]
   > Chcete-li, aby se **Nabídka platná do data** automaticky vyplňovala s určitým počtem dní po vytvoření nabídky, můžete vypnlit pole **Kalkulace platnosti poptávky** na stránce **Nastavení prodeje a pohledávek**.

15. Po dokončení řádků prodejních nabídek vyberte akci **Odeslat Emailem**.
16. Na stránce **Odeslat emailem**, vyplňte všechna zbývající pole a zkontrolujte vloženou prodejní nabídku. Pro více informací navštivte [Odesílání dokladů e-mailem](ui-how-send-documents-email.md).
17. Pokud zákazník nabídku přijme, vyberte akci **Vytvořit fakturu** nebo **Vytvořit objednávku**.

Prodejní nabídka je odstraněna z databáze. Prodejní faktura nebo prodejní objednávka je vytvořena na základě informací v prodejní nabídce, ve které můžete prodej zpracovat. V poli **Číslo nabídky** na prodejní faktuře nebo prodejní objednávce můžete vidět číslo prodejní nabídky, ze které bylo vyrobeno. Pro více informací navštivte [Nákupní objednávky](sales-how-invoice-sales.md) nebo [Prodávat výrobky](sales-how-sell-products.md).

## Viz také
[Prodej](sales-manage-sales.md)  
[Nastavení Prodeje](sales-setup-sales.md)  
[Odesílání dokladů e-mailem](ui-how-send-documents-email.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
