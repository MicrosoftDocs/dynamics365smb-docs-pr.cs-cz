---
    title: How to Correct Prepayments | Microsoft Docs
    description: You can make a correction to an order after you have posted a prepayment invoice for the order. You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.
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
# Oprava záloh
Po zaúčtování zálohové faktury za objednávku můžete provést opravu objednávky. Nové řádky můžete do objednávky přidat po vystavení zálohy a potom můžete zaúčtovat další zálohovou fakturu, ale po fakturaci zálohy pro řádek nelze odstranit řádek z objednávky.

## Oprava zálohy
Následující postup ukazuje, jak vydat dobropis zálohy a zrušit všechny fakturované zálohy na prodejní objednávce.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Otevřete příslušnou prodejní objednávku.
3. Vyberte akci **Záloha** a poté vyberte akci **Zaúčtovat dobropis zálohy** nebo **Zaúčtovat a vytisknout  dobropis  zálohy**.
4. Na stránce **Prodejní objednávka** pokračujte v opravě příslušných položek, jako u všech prodejních objednávek. Pro více informací navštivte [Zpracování prodejní vratky nebo stornování](sales-how-process-sales-returns-cancellations.md).

   > [!NOTE]
   > Chcete-li snížit částku v poli **Částka na řádku**, musíte nejprve zvýšit procento předplacení na řádku tak, aby hodnota v poli **Částka  řádku zálohy** neklesla pod hodnotu v poli **Fakt.  částka  zálohy**.

5. Chcete-li vytvořit zálohovou fakturu pro všechny nové řádky v prodejní objednávce, vyberte akci **Záloha** a poté vyberte akci **Zaúčtovat fakturu pro platbu předem** nebo **Zaúčtovat a vytisknout zálohovou  fakturu**.
6. Chcete-li vystavit další zálohovou fakturu, zvyšte částku zálohy na jednom nebo více řádcích a zaúčtujte zálohovou fakturu. Bude vytvořena nová faktura pro rozdíl mezi fakturovanými částkami zálohy a novými částkami zálohy.

## Viz také
[Fakturace záloh](finance-invoice-prepayments.md)  
[Návod: Nastavení a fakturace prodejních záloh](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
