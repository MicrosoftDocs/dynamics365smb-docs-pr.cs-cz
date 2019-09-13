---
title: Nastavení obsahu e-mailu specifického pro doklad | Microsoft Docs
description: 'Můžete definovat obsah, který se má vložit do těma e-mailové zprávy, například odkaz na PayPal. K e-mailovým zprávám můžete také připojit doklady.'
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'SMTP, mail, Office 365, cover, body, PayPal, layout'
ms.date: 03/01/2019
ms.author: sgroespe
---
# <a name="send-documents-by-email"></a>Odeslat dokumenty e-mailem
Chcete-li svým obchodním partnerům rychle sdělit obsah obchodních dokladů, například platební informace o prodejních dokladech, můžete pomocí funkce Rozvržení sestavy definovat obsah specifický pro doklad, který se automaticky vloží do těla e-mailu. Pro více informací navštivte [Správa rozvržení sestav a dokladů](ui-manage-report-layouts.md).

Chcete-li povolit e-maily z prostředí [!INCLUDE[d365fin](includes/d365fin_md.md)], spusťte v Centru rolí asistované nastavení **Nastavit e-mail**.

Můžete poslat e-mailem prakticky všechny typy dokladů jako přílohy k e-mailovým zprávám přímo ze stránky, která doklad zobrazuje. Kromě přílohy, můžete nastavit těla e-mailů specifických pro doklad se základními informacemi z dokladu, kterému předchází standardní text, který uvítá příjemce a představí dotyčný doklad. Chcete-li svým zákazníkům nabídnout, aby elektronicky platili za prodej pomocí platební služby, jako je Paypal, můžete do těla e-mailu také vložit informace o PayPal a hypertextový odkaz.

Ze všech podporovaných dokladů zahájíte zasílání e-mailů výběrem akce **Odeslat** na zaúčtovaných dokladech nebo akce **Účtovat a Odeslat** na nezaúčtovaných dokladech.

Pokud je pole **E-mail** na stránce **Odeslat doklad (komu)** nastaveno na **Ano (Výzva pro nastavení)**, otevře se stránka **Odeslat e-mail**, která je předvyplněná kontaktní osobou v poli **Komu:** a doklad je připojený jako soubor PDF. V poli **Tělo** můžete buď zadat text ručně nebo můžete nechat vyplnit pole tělem e-mailu specifickým pro doklad, který jste nastavili.

Následující postup popisuje, jak nastavit sestavu **Prodej - Faktura** tak, aby byla použita pro těla e-mailů specifická pro doklad, když zasíláte účtované prodejní faktury.

## <a name="to-set-up-a-document-specific-email-body-for-sales-invoices"></a>Chcete-li nastavit tělo e-mailu specifické pro prodejní faktury
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Výběry sestav - prodej** a poté vyberte související odkaz.
2. Na stránce **Výběry sestav - prodej** v poli **Použití** vyberte **Faktura**.
3. Na novém řádku v poli **ID sestavy** vyberte například standardní sestavu 1306.
4. Zašktněte políčko **Použít pro předmět e-mailu**.
5. Zvolte **Kód rozvržení textu e-mailu** a poté vyberte rozvržení z rozevíracího seznamu.

    Rozvržení sestavy definují jak styl, tak obsah těla e-mailu, včetně standardního textu, který předchází hlavním informacím o dokladu v těle e-mailu. Pokud v rozevíracím seznamu stisknete tlačítko **Výběr z úplného seznamu**, zobrazí se všechna dostupná rozvržení sestav.
6. Chcete-li zobrazit nebo upravit rozvržení, na kterém je tělo e-mailu založeno, vyberte rozvržení ve stránce **Vlastní rozvržení sestav** a poté vyberte akci **Upravit rozvržení**.
7. Chcete-li zákazníkům nabídnout, aby elektronicky platili za prodej pomocí příslušné platební služby, jako je Paypal, můžete do těla e-mailu také vložit informace o PayPal a hypertextový odkaz. Pro další informace navštivte [Povolení plateb zákazníkům prostřednictvím služby PayPal](sales-how-enable-payment-service-extensions.md).
8. Zvolte tlačítko **OK**.

Když nyní zvolíte například akci **Odeslat** na stránce **Účtovaná prodejní faktura**, bude tělo e-mailu obsahovat informace o dokladu sestavy 1306, které předchází stylizovaný standardní text podle rozvržení sestavy, které jste vybrali v kroku 5.

Následující postup popisuje, jak odeslat účtovanou prodejní fakturu jako e-mailovou zprávu s dokladem přiloženým jako soubor PDF a s tělem e-mailu specifickým pro doklad.

## <a name="to-send-documents-by-email"></a>Chcete-li odeslat doklad e-mailem
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Účtovaná prodejní faktura** a poté vyberte související odkaz.
2. Vyberte příslušnou účtovanou prodejní fakturu a poté zvolte akci **Odeslat**. Otevře se stránka **Odeslat doklad (komu)**.
3. V poli **E-mail** vyberte **Ano (Výzva pro nastavení)**. Pro více informací navštivte [Nastavení profilů odesílání dokladů](sales-how-setup-document-send-profiles.md).
4. Zvolte tlačítko **OK**. Otevře se stránka **Odeslat e-mail**.
5. Do pole **Komu:** zadejte platnou e-mailovou adresu. Výchozí hodnota je e-mailová adresa zákazníka.
6. Do pole **Předmět** zadejte popisný název e-mailu. Výchozí hodnota je jméno zákazníka a číslo faktury.
7. V poli **Příloha** je vygenerovaná faktura standardně připojena jako soubor PDF. Stisknutím vyhledávacího tlačítka otevřete soubor nebo připojíte další.
8. Do pole **Tělo** zadejte krátkou zprávu příjemci.

    Pokud je na stránce **Výběr sestavy - prodej** nastaveno tělo e-mailu specifické pro doklad, pak se pole **Tělo** automaticky vyplní. Více informací naleznete v tomto tématu v části [Nastavení těla e-mailu specifické pro doklad pro prodejní faktury](ui-how-send-documents-email.md#to-set-up-a-document-specific-email-body-for-sales-invoices).
9. Pro odeslání e-mailové zprávy volte tlačítko **OK**.

> [!NOTE]  
>   Pokud nechcete specifikovat nastavení e-mailu při každém odeslání dokladu e-mailem, můžete vybrat možnost **Ano (Použít výchozí nastavení)** v poli **E-mail** na stránce **Odeslat doklad (komu)**. V takovém případě se stránka **Odelat e-mail** neotevře. Viz krok 4. Pro více informací navštivte [Nastavení profilů odesílání dokladů](sales-how-setup-document-send-profiles.md).

## <a name="see-also"></a>Viz také
[Správa rozvržení Sestav a Dokumentů](ui-manage-report-layouts.md)  
[Nastavení e-mailu](admin-how-setup-email.md)  
[Fakturace prodeje](sales-how-invoice-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
