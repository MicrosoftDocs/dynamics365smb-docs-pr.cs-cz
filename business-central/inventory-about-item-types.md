---
title: Understanding Item Types
description: You can adjust the inventory valuation of an item using the FIFO or Average costing methods when item costs change for reasons other than transactions.
documentationcenter: ''
author: SorenGP


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.search.form: 9297, 5845, 30, 
ms.date: 06/16/2021
ms.author: edupont


---
# O typech zboží
V poli **Typ** na stránce **Karta zboží** můžete vybrat, k čemu se položka používá ve vaší firmě, což ovlivňuje míru, do jaké můžete spravovat položku ve skladu. V následující tabulce jsou uvedeny a popsány tři typy položek, které jsou k dispozici.

| Možnost | Typický účel |
|------|-----------|
| Zásoby | Fyzické věci, jako jsou jízdní kola, telefony a stoly, pro které chcete mít možnost používat všechny inventarizační procesy. To může také zahrnovat nefyzické položky, jako jsou softwarové licence a předplatné, pokud mají položky identifikační čísla, jako jsou sériová čísla. Můžete plně sledovat hodnoty položek a dostupnost ve skladu. |
| Neskladové položky | Položky, které nejsou zásobami, jsou obvykle fyzické věci, jako jsou šrouby nebo pera, které podnik spotřebovává, ale nechce je plně sledovat v zásobách. Například proto, že se jedná o nízkonákladové položky a používají se pouze interně. |
| Služby | Jednotka pracovní doby, například poradenská hodina, pro omezenou podporu podnikání. |

> [!NOTE]
> Typy **Služba** a **Neskladové položky** nepodporují sledování množství a hodnot zásob. Podporovány jsou pouze vybrané typy transakcí a funkce položek.

V následující tabulce jsou uvedeny funkce, které tyto tři typy položek podporují.

|Typ zboží|Prodej|Nakupování|Spotřeba projektu|Spotřeba služeb|Spotřeba montáže|Spotřeba výroby|Montážní výstup|Výrobní výstup|Přesun místa|Fyzické počítání|Přecenění zásob|Zásoby a ocenění|Sledování zboží|Rezervace|Skladování|Plánování|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Zásoby|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|Ano|
|Neskladové položky|Ano|Ano|Ano|Ano|Ano|Ano|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|
|Služby|Ano|Ano|Ano|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|Ne|

## Metody kalkulace nákladů pro typy zboží
Při zaúčtování skladových transakcí jsou změny množství a hodnoty zásob zaznamenány v položkách zboží a položky ocenění.

U skladových položek jsou náklady zaznamenány v poli **Částka nákladů (skutečná)** na stránce **Položky ocenění** a při odsouhlasení s hlavní knihou se náklady zobrazí v poli **Náklady zaúčtované do Věcných položek**. Další informace naleznete v tématu [Podrobnosti návrhu: Kalkulace nákladů na zásoby](design-details-inventory-costing.md).

U neskladových a servisních položek se náklady zaznamenávají do pole **Částka nákladů (Neskladové)** na stránce **Položky hodnoty**. U neskladových a servisních položek jsou náklady uvedeny v prodejních, montážních a výrobních dokladech a denících. Výchozí náklady lze zadat v poli **Jednotkové náklady** na stránkách **Karta zboží** a **Skladová jednotka**. Náklady na tyto typy zboží nejsou odsouhlaseny s Věcnými položkami.

## Katalog a předměty servisu
Zboží, které nabízíte svým zákazníkům, ale nechcete je spravovat ve svém systému, dokud je nezačnete prodávat, lze nastavit jako položky katalogu. Položky katalogu nesmí být zaměňovány s běžnými položkami typu Neskladové. Pro více informací navštivte [Práce se katalogovým zbožím](inventory-how-work-nonstock-items.md).

Položky zákazníků, na kterých provádíte servis, jako je tiskárna, se nazývají servisní položky. Servisní položky nemají nic společného s běžnými nebo katalogovými položkami. Servisní komponenty však mohou být běžné položky. Pro více informací navštivte [Nastavení Předmětů servisu a Komponent předmětu servisu](service-how-setup-service-items.md).

## Viz také
[Evidence nového zboží](inventory-how-register-new-items.md)    
[Nastavení zásob](inventory-setup-inventory.md)    
[Řízení nákladů na zásoby](finance-manage-inventory-costs.md)    
[Zásoby](inventory-manage-inventory.md)    
[Pracovat s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]