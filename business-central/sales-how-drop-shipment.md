---
title: Link a Sales Order to a Purchase Order for Direct Shipment | Microsoft Docs
description: Describes how to create a sales order linked to a purchase order to enable shipment directly from the vendor to the customer.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 10/01/2020
ms.author: edupont

---
# Vytvoření prodejních dodávek

Přímá dodávka je dodávka zboží od jednoho z vašich dodavatelů přímo jednomu z vašich zákazníků.

Je-li prodejní objednávka označena jako „přímá dodávka“ a vytvoříte nákupní objednávku s uvedením zákazníka v poli **Příjemce**, **Adresa zákazníka**, můžete tyto dva doklady propojit pro poučení dodavatele, aby odeslal zboží přímo zákazníkovi.
<br><br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## Chcete-li vytvořit prodejní objednávku pro přímou dodávku

Chcete-li připravit přímou dodávku, vytvořte prodejní objednávku pro zboží a na prodejním řádku označte, že prodej vyžaduje přímou dodávku.

1. Vytvoření prodejní objednávky pro zboží. Více informací viz [Prodej produktů](sales-how-sell-products.md).
2. Na řádku prodejní objednávky pro přímou dodávku zaškrtněte políčko **Přímá dodávka**. Pokud pole není viditelné, použijte funkci **Zvolit sloupce** . Více informací viz [Přizpůsobení pracovního prostoru](ui-personalization-user.md).

## Chcete-li vytvořit nákupní objednávku pro přímou dodávku

Chcete-li připravit přímou dodávku, uvedete na objednávce, že musí být odeslána zákazníkovi, nikoli sobě.

1. Vytvoření nákupní objednávky. Na řádcích nevyplňujte žádná pole. Více informací viz [Zaznamenávání nákupů](purchasing-how-record-purchases.md).
2. V poli **Příjemce** vyberte **Adresa zákazníka**.
3. V poli **Zákazník** vyberte zákazníka, kterému prodáváte.
4. Zvolte akci **Přímé dodávky** a pak zvolte akci **Získat prodejní objednávku.**.
5. Na stránce **Přehled prodeje** vyberte prodejní objednávku, kterou jste připravili v [Chcete-li vytvořit prodejní objednávku pro přímou dodávku](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
6. Zvolte tlačítko **OK**.

Informace o řádku z prodejní objednávky se vloží na řádek/řádky nákupní objednávky.

Nyní můžete dát pokyn dodavateli, aby zboží odeslal zákazníkovi, například zasláním nákupní objednávky ve formátu PDF.

## Chcete-li vytvořit více nákupních objednávek pro přímé dodávky

K vytvoření nákupní objednávky pro dodavatele můžete také použít sešit požadavků. Výhodou použití sešitu požadavků je, že může vytvářet nákupní objednávky pro všechny nevyřízené přímé dodávky, takže nemusíte vytvářet každou z nich jednotlivě.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešity požadavků** a poté vyberte související odkaz.
2. Zvolte akci **Přímé dodávky** a pak zvolte akci **Získat prodejní objednávku.**.
3. Zvolte tlačítko **OK**.
4. Zkontrolujte řádky nákupní objednávky a v poli **Číslo dodavatele** vyberte dodavatele, který dodává požadované zboží.
5. Vyberte akci **Provést zprávu o akci** pro převedení zkontrolovaných řádků na nákupní objednávku.

## Chcete-li zobrazit propojenou nákupní objednávku z prodejní objednávky

* Vyberte řádek prodejní objednávky přímé dodávky, zvolte akci **Objednat** , zvolte akci **Přímá dodávka** a pak zvolte akci **Nákupní objednávka**.

## Chcete-li účtovat přímou dodávku

Poté, co dodavatel dodá zboží, můžete účtovat prodejní objednávku tak, jak byla dodána. Můžete také účtovat nákupní objednávku, ale pouze s možností **Přijmout** , dokud nebude prodejní objednávka fakturována.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Otevřete prodejní objednávku, kterou jste vytvořili v [Chcete-li vytvořit prodejní objednávku pro přímou dodávku](#to-create-a-sales-order-for-drop-shipment).
3. V poli **Množství k dodání** , určete, kolik množství objednávky má být dodáno, úplné nebo částečné množství objednávky.
4. Zvolte akci **Účtovat** nebo **Účtovat a odeslat**.
5. Vyberte buď možnost **Dodání**, chcete-li fakturovat později, nebo možnost **Dodat a fakturovat**, chcete-li fakturovat okamžitě.

## Viz také

[Vytvoření speciálních objednávek](sales-how-to-create-special-orders.md)  
[Nákup zboží pro prodej](purchasing-how-purchase-products-sale.md)  
[Prodej produktů](sales-how-sell-products.md)  
[Zaznamenavání nákupů](purchasing-how-record-purchases.md)  
[Prodej](sales-manage-sales.md)  
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
