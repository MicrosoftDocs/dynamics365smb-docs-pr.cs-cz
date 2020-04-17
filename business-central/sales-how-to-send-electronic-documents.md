---
    title: Send Electronic Documents | Microsoft Docs
    description: learn how to send invoices electronically.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Posílání elektronických dokladů
Obecná verze [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje odesílání elektronických faktur a dobropisů ve formátu PEPPOL, který je podporován největšími poskytovateli služeb výměny dokladů. Poskytovatel služeb výměny dokumentů zasílá elektronické doklady mezi obchodními partnery. K poskytování podpory pro jiné formáty elektronických dokladů použijte rozhraní pro výměnu dat.

V obecné verzi [!INCLUDE[d365fin](includes/d365fin_md.md)], je služba výměny dokladů předkonfigurována a připravena k nastavení pro vaši společnost. Pro více informací navštivte [Nastavení služby směnných kurzů](across-how-to-set-up-a-document-exchange-service.md).

Chcete-li odeslat prodejní fakturu jako elektronický doklad PEPPOL, vyberte v dialogovém okně **Účtovat a Odeslat** možnost **Elektronický doklad**, můžete také zvolit výchozí profil odeslání dokladu zákazníka. Nejprve je nutné nastavit různá hlavní data, například informace o společnosti, zákazníky, zboží a měrné jednotky.  Tyto se používají se k identifikaci obchodních partnerů a položek při převodu dat v polích v [Nastavení odesílání a přijímání elektronického dokladu](across-how-to-set-up-electronic-document-sending-and-receiving.md).

### Chcete-li odeslat elektronickou prodejní fakturu

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktury** a poté vyberte související odkaz.

2. Vytvořte novou prodejní fakturu.

3. Když je prodejní faktura připravena k fakturaci, zvolte akci**Účtovat a Odeslat**.

   Pokud je výchozím odesílajícím profilem zákazníka **Elektronický doklad**, pak to bude zobrazeno v dialogovém okně **Zaúčtovat a odeslat potvrzení** a vy pouze zvolíte tlačítko **Ano** pro účtování a odeslání elektronických dokladů ve vybraném formátu.

4. V dialogovém okně **Zaúčtovat a odeslat potvrzení**, vyberte tlačítko AssistEdit napravo od pole **Odeslat doklad (komu)**.

5. V dialogovém okně **Odeslat doklad (komu)** v poli **Elektronický doklad**, vyberte **Prostřednictvím služby výměny dokumentů**.

6. V poli **Formát** vyberte **PEPPOL**.

7. Zvolte tlačítko **OK**. Objeví se dialogové okno **Zaúčtovat a odeslat potvrzení**. **Elektronický Doklad (PEPPOL)** je přidán do pole **Odeslat doklad (komu)**.

8. Vyberte tlačítko **Ano**.

   Prodejní faktura je zaúčtována a odeslána zákazníkovi jako elektronický doklad ve formátu PEPPOL.

   > [!NOTE]
   > Zaúčtované prodejní faktury můžete také odeslat jako elektronický doklad. Postup je stejný, jak je popsáno v tomto tématu pro nezaúčtované prodejní doklady. Na stránce **Účtovaná prodejní faktura**, vyberte akci **protokol aktivity** pro zobrazení stavu elektronického dokladu. Pro více informací navštivte **protokol aktivity**.

## Viz také
[Fakturace prodeje](sales-how-invoice-sales.md)
[Nastavení profilů odesílání dokladů](sales-how-setup-document-send-profiles.md)
[Nastavení odesílání a přijímání elektronického dokladu](across-how-to-set-up-electronic-document-sending-and-receiving.md)
[Nastavení služby směnných kurzů](across-how-to-set-up-a-document-exchange-service.md)
[Nastavení definice výměny dat](across-how-to-set-up-data-exchange-definitions.md)
[Elektronická výměna dat](across-data-exchange.md)
[Obecné obchodní funkcionality](ui-across-business-areas.md)
