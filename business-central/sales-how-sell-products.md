---
title: Create a Sales Order and Sell Products | Microsoft Docs
description: Describes how to create a sales order to record your agreement with a customer to sell or trade products under specific terms.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 10/01/2019
ms.author: sgroespe

---
# Prodávání produktů
Vytvořením prodejní objednávky nebo prodejní faktury zaznamenáte vaši smlouvu se zákazníkem o prodeji určitých produktů za určitých dodacích a platebních podmínek.

> [!NOTE]
> Prodejní objednávky používáte, pokud váš prodejní proces vyžaduje, abyste mohli poslat části objednaného množství, například proto, že plné množství není k dispozici najednou. Pokud prodáváte zboží, které doručujete přímo vašemu zákazníkovi, jako přímou dodávku zboží musíte také použít prodejní objednávky. Pro více informací navštivte [Vytvoření přímé dodávky](sales-how-drop-shipment.md). Ve všech ostatních aspektech fungují prodejní objednávky a prodejní faktury stejným způsobem. Další informace naleznete v [Prodejní faktury](sales-how-invoice-sales.md).

Se zákazníkem můžete jednat nejprve vytvořením prodejní nabídky, kterou, když se na prodeji dohodnete, můžete převést na prodejní objednávku. Pro více informací navštivte [Vytváření prodejních nabídek](sales-how-make-offers.md).

Poté, co zákazník potvrdí smlouvu, například po procesu nabídky, můžete zaslat potvrzení objednávky k zaznamenání vaší povinnosti dodat produkty podle dohody.

Při dodání produktů, zcela nebo částečně, zaúčtujete prodejní objednávku jako dodané, nebo jako dodané a fakturované k vytvoření souvisejících položek zboží a zákazníka v systému. Když účtujete prodejní objednávku, můžete doklad poslat e-mailem, nebo také jako přílohu PDF. Můžete také mít tělo e-mailu předem vyplněné souhrnem informací o objednávce a platbě, například odkazem na PayPal. Pro více informací navštivte [Odesílání dokladů e-mailem](ui-how-send-documents-email.md).

V obchodních prostředích, kde zákazník platí nějaký čas po dodání, podle platebních podmínek zůstane zaúčtovaná prodejní faktura otevřená (nezaplacená), dokud oddělení pohledávek neověří, že platba byla přijata, a nepoužije platbu na zaúčtovanou prodejní fakturu. Pro více informací navštivte [Automatické odsouhlasení plateb](receivables-how-reconcile-payments-auto-application.md).

V obchodních prostředích, kde zákazník okamžitě zaplatí, například prostřednictvím PayPal nebo v hotovosti, je platba zaznamenána okamžitě, jakmile zaúčtujete prodejní objednávku jako fakturovanou, tj. Zaúčtovaná prodejní faktura je uzavřena v plném rozsahu. Příslušnou metodu vyberete na prodejní objednávce v poli **Kód způsobu platby**. Viz krok 8. U elektronických plateb, jako je PayPal, musíte také vyplnit pole **Služba po platby**. Pro více informací navštivte [Povolení plateb zákazníků prostřednictvím platebních služeb](sales-how-enable-payment-service-extensions.md).

Můžete dokonce vytvořit přímo placené objednávky pro neregistrované zákazníky tak, že nejprve nastavíte kartu „hotovostní zákazník“, na kterou na prodejní objednávce odkážete. Pro více informací navštivte [Nastavení zákazníků platících hotovosti](finance-how-to-set-up-cash-customers.md).

Zaúčtované prodejní faktury vyplývající z nákupní objednávky můžete před zaplacením snadno opravit nebo zrušit. To je užitečné, pokud chcete opravit chybu při psaní nebo pokud zákazník požaduje včasnou změnu objednávky. Pro více informací navštivte [Opravit nebo zrušit nezaplacené prodejní faktury](sales-how-correct-cancel-sales-invoice.md). Pokud je zaúčtovaná prodejní faktura již zaplacena, musíte vytvořit prodejní dobropis, abyste tento prodej stornovali. Pro více informací navštivte [Zpracování prodejní vratky nebo stornování](sales-how-process-sales-returns-cancellations.md).


Karta zboží může být typu **Zásoby**, **Služby**, nebo **Neskladované** k určení, zda je zboží fyzickou skladovou jednotkou, jednotkou pracovní doby nebo fyzickou jednotkou, která není ve skladě. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md). Proces prodejní objednávky je stejný pro všechny tři typy položek.

Pole zákazníka na prodejní objednávce můžete vyplnit dvěma způsoby v závislosti na tom, zda je zákazník již zaregistrován. Viz kroky 2 a 3 v následujícím postupu.

## Vytvoření prodejní objednávky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Do pole **Zákazník** zadejte jméno stávajícího zákazníka.

   Ostatní pole na stránce **Prodejní objednávky** jsou nyní vyplněna standardními informacemi vybraného zákazníka. Pokud zákazník není registrován, postupujte takto:
3. Do pole **Zákazník**, zadejte jméno nového zákazníka.
4. V dialogovém okně o registraci nového zákazníka vyberte tlačítko **Ano**.
5. Na stránce **Vybrat šablonu pro nového zákazníka** vyberte šablonu, kterou chcete použít pro novou kartu zákazníka a zvolte tlačítko **OK**.

   Otevře se nová karta zákazníka s předvyplněnými informacemi o vybrané šabloně zákazníka. Pole **Název**, předvyplněno názvem nového zákazníka, které jste zadali do prodejní objednávky.
6. Pokračujte vyplněním zbývajících polí na kartě zákazníka. Pro více informací navštivte [Evidence nového zákazníka](sales-how-register-new-customers.md).  
7. Po dokončení karty zákazníka zvolte tlačítko **OK** k vrácení se na stránku **Prodejní objednávka**.

   Několik polí v prodejní objednávce je nyní vyplněno informacemi, které jste zadali na nové zákaznické kartě.  
8. Podle potřeby vyplňte zbývající pole na stránce **Prodejní objednávka**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Pokud zákazníkovi umožníte okamžitou platbu, například kreditní kartou nebo PayPal, vyplňte pole  **Kód způsobu platby**. Platba je pak zaznamenána, jakmile zaúčtujete prodejní objednávku. Pokud vyberete možnost HOTOVĚ, bude platba zaznamenána na určeném protiúčtu.

   Nyní jste připraveni vyplnit řádky prodejní objednávky skladovými položkami nebo službami, které chcete zákazníkovi prodat.

   Pokud jste pro zákazníka nastavili opakující se prodejní řádky, například měsíční objednávky doplnění, tyto řádky můžete vložit do objednávky výběrem akce **Získat periodické prodejní řádky**.  
9. Do záložky s náhledem **Řádky**, v poli **Zboží**, zadejte číslo skladové položky, nebo služby. 
10. V poli **Kvalita**, zadejte počet položek, které mají být prodány.

   > [!NOTE]
   > U položek typu Služba je množstvím časová jednotka, jako například hodina, jak je uvedeno na řádku v poli **Kód měrné jednotky**.

   Pole **Částka řádku** se aktualizuje tak, aby zobrazovala hodnotu v poli **Jednotková cena** vynásobenou hodnotou v poli **Množství**.

   Částky ceny a řádku jsou s nebo bez DPH, v závislosti na tom, co jste vybrali v poli **Ceny včetně daně** na kartě zákazníka.  
11. V poli **Řádková sleva %**, zadejte procento, pokud chcete zákazníkovi poskytnout slevu na produkt. Hodnota v poli **Částka řádku** se odpovídajícím způsobem aktualizuje.

   Pokud jsou speciální ceny položek nastaveny na záložce s náhledem **Prodejní ceny a prodejní řádkové slevy** na kartě zákazníka nebo zboží, cena a částka na řádku nabídky se automaticky aktualizují, pokud jsou splněna dohodnutá kritéria ceny. Pro více informací navštivte [Evidence speciálních prodejních cen a slev](sales-how-record-sales-price-discount-payment-agreements.md).  
12. Chcete-li přidat komentář k řádku nabídky, který může zákazník vidět v tištěné prodejní nabídce, napište text do prázdného řádku v poli **Popis**.  
13. Opakujte kroky 9 až 12 pro každou položku, kterou chcete zákazníkovi prodat.

   Součty pod řádky se automaticky počítají při vytváření nebo úpravách řádků.  
14. Nová zákaznická karta zobrazuje informace o vybrané zákaznické šabloně. Vyplňte zbývající pole. Pro více informací navštivte [Evidence nového zákazníka](sales-how-register-new-customers.md).  
15. Po dokončení karty zákazníka zvolte tlačítko **OK** k vrácení se na stránku **Prodejní objednávka**.

   Několik polí v prodejní objednávce je nyní vyplněno informacemi, které jste zadali na nové zákaznické kartě.  
16. Podle potřeby vyplňte zbývající pole na stránce **Prodejní objednávka**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   Nyní jste připraveni vyplnit řádky prodejní objednávky u produktů, které prodáváte zákazníkovi, nebo pro jakoukoli transakci se zákazníkem, kterou chcete zaznamenat na účet hlavní knihy.

   Pokud jste pro zákazníka nastavili opakující se prodejní řádky, například měsíční objednávky doplnění, tyto řádky můžete vložit do objednávky výběrem akce **Získat periodické prodejní řádky**.  
17. V záložce s náhledem **Řádky**, v poli **Typ**, vyberte, jaký typ produktu, platby nebo transakce, které zaúčtujete zákazníkovi s prodejní řádkem.

18. V poli **Číslo**, vyberte záznam, který chcete odeslat, podle hodnoty v poli **Typ**.

   Pole **Číslo** ponecháte prázdné v následujících případech:

   * Pokud je řádek pro komentář. Napište do pole **Popis** komentář.
   * Pokud je řádek pro položku katalogu. Vyberte akci **Vybrat zboží katalogu**. Pro více informací navštivte [Práce se katalogovým zbožím](inventory-how-work-nonstock-items.md).

19. V poli **Množství**, zadejte, kolik jednotek produktu, poplatku nebo transakce bude řádek pro zákazníka zaznamenávat.

   > [!NOTE]
   > Pokud je zboží typu **Služba**, nebo pole **Typ** obsahuje **Zdroj**, pak je množství časovou jednotkou, jako například hodiny, jak je uvedeno na řádku v poli **Kód měrné jednotky**. Pro více informací navštivte [Nastavení měrných jednotek zboží](inventory-how-setup-units-of-measure.md).

   Hodnota v poli **Částka řádku** se vypočítá jako *Jednotková cena* krát *Množství*.

   Částky ceny a řádku jsou s nebo bez DPH, v závislosti na tom, co jste vybrali v poli **Ceny včetně daně** na kartě zákazníka.  
20. Pokud chcete poskytnout slevu, zadejte procento do pole **Řádková sleva %**. Hodnota v poli **Částka řádku** se odpovídajícím způsobem aktualizuje.

   Pokud jsou speciální ceny položek nastaveny na záložce s náhledem **Prodejní ceny a prodejní řádkové slevy** na kartě zákazníka, nebo zboží, cena a částka na prodejním řádku se automaticky aktualizují, pokud jsou cenová kritéria splněna. Pro více informací navštivte [Evidence speciálních prodejních cen a slev](sales-how-record-sales-price-discount-payment-agreements.md).  
21. Opakujte kroky 9 až 12 pro každý produkt nebo poplatek, který chcete zákazníkovi prodat.

   Pole součtů pod řádky se automaticky aktualizují při vytváření nebo úpravě řádků, aby se zobrazily částky, které budou zaúčtovány do účetních knih.

   > [!NOTE]
   > Ve velmi vzácných případech se zaúčtované částky mohou lišit od toho, co je zobrazeno v polích součtů. To je obvykle způsobeno výpočty zaokrouhlování ve vztahu k DPH nebo prodejní dani.<br /><br />Ke kontrole částek, které budou skutečně zaúčtovány, můžete použít stránku **Statistika**, která bere v úvahu výpočty zaokrouhlení. Pokud také zvolíte akci **Vydat**, budou součty aktualizovány tak, aby zahrnovaly výpočty zaokrouhlování.
22. Do pole **Částka fakturační slevy**, zadejte částku, která má být odečtena z hodnoty uvedené v poli **Celkem včetně  DPH**.

   Pokud jste pro zákazníka nastavili slevy na faktuře, zadaná procentuální hodnota se automaticky vloží do pole **Fakturační sleva %** pokud jsou splněna kritéria, a související částka je vložena do pole **Částka fakturační slevy bez DPH**. Pro více informací navštivte [Evidence speciálních prodejních cen a slev](sales-how-record-sales-price-discount-payment-agreements.md).  
23. Chcete-li odeslat pouze část objednaného množství, zadejte toto množství do pole **K dodání**. Hodnota je zkopírována do pole **K fakturaci**.  
24. K fakturaci pouze části dodaného množství, zadejte toto množství do pole **K fakturaci**. Množství musí být nižší než hodnota v poli **K dodání**.  
25. Po dokončení řádků prodejní objednávky vyberte akci **Účtovat a odeslat**.

Dialogové okno **Zaúčtovat a odeslat potvrzení** zobrazuje zákazníkův preferovaný způsob přijímání dokumentů. Metodu odesílání můžete změnit výběrem vyhledávacího tlačítka pro pole **Odeslat doklad (komu)**. Pro více informací navštivte [Nastavení profilů odesílání dokladů](sales-how-setup-document-send-profiles.md).

Související položky zboží a zákazníka jsou nyní vytvořeny ve vašem systému a prodejní objednávka je výstupem jako doklad PDF. Když je prodejní objednávka plně zaúčtována, je odebrána ze seznamu prodejních objednávek a nahrazena novými doklady v seznamu účtovaných prodejních faktur a v seznamu účtovaných prodejních dodávek.

## Viz také
[Prodej](sales-manage-sales.md)  
[Nastavení Prodeje](sales-setup-sales.md)  
[Zásoby](inventory-manage-inventory.md)  
[Odesílání dokladů e-mailem](ui-how-send-documents-email.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
