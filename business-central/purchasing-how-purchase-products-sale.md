---
title: Purchase Items for a Sale by Creating Purchase Invoices | Microsoft Docs
description: From a sales invoice, to purchase products, you can create a purchase invoice for a vendor or supplier.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 04/01/2020
ms.author: sgroespe

---
# Nákup zboží pro prodej
Od prodejních objednávek a prodejních faktur můžete pomocí funkcí rychle vytvářet nákupní doklady pro chybějící množství zboží, které je vyžadováno prodejem. V závislosti na typu dokladu můžete použít dvě různé funkce.

> [!Note]
> Tato funkce slouží k doplnění položek prodeje do vašich vlastních zásob. Chcete-li zakoupit zboží pro přímé doručení od dodavatele zákazníkovi, musíte vytvořit přímou dodávku. Pro více informací navštivte [Provedení přímé dodávky](sales-how-drop-shipment.md).

| Funkce | Popis |
|--------|-----------|
| **Vytvořit nákupní objednávky** | Z prodejní objednávky vytvoří tato funkce nákupní objednávku pro každého dodavatele zboží na prodejní objednávce. Před vytvořením objednávek můžete upravit množství nákupu. Doporučuje se pouze nedostupné množství prodeje. |
| **Vytvořit nákupní fakturu** | Z prodejní objednávky a z prodejní faktury tato funkce vytvoří nákupní fakturu pro vybraného dodavatele pro všechny řádky nebo vybrané řádky v prodejním dokladu. Doporučuje se plné prodejní množství. |

## Vytvoření jedné nebo více nákupních objednávek z prodejní objednávky
Chcete-li vytvořit objednávku pro každé nedostupné množství zboží v prodejní objednávce, použijte funkci **Vytvořit nákupní objednávky**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Otevřete prodejní objednávku, pro kterou chcete zboží zakoupit.
3. Vyberte akci **Vytvořit nákupní objednávky**.

   Otevře se stránka **Vytvořit nákupní objednávky** a zobrazí se řádek pro každé jiné zboží v prodejní objednávce. Ve výchozím nastavení jsou zobrazeny řádky pro plně dostupná prodejní množství i nedostupná prodejní množství (šedá). Můžete vybrat akci **Zobrazit nedostupné** a zobrazit pouze řádky pro nedostupná množství prodeje.

   Pole **Množství k nákupu** obsahuje ve výchozím nastavení nedostupné množství prodeje.
4. Chcete-li zakoupit jiné množství, než je nedostupné množství k prodeji, upravte hodnotu v poli **Množství k nákupu**.

   > [!NOTE]
   > Na šedých řádcích můžete také změnit pole **Množství k nákupu**, i když představují plně dostupná množství k prodeji.
5. Vyberte tlačítko **OK**.

   Objednávka se vytvoří pro každého dodavatele zboží v prodejní objednávce, včetně všech změn množství, které jste provedli na stránce **Vytvořit nákupní objednávky**.
7. Pokračujte ve zpracování objednávky nebo objednávek, například úpravou nebo přidáním řádků objednávky. Pro více informací navštivte [Záznam nákupů](purchasing-how-record-purchases.md).


## Vytvoření nákupní faktury z prodejní objednávky nebo prodejní faktury
Chcete-li vytvořit jednu nákupní fakturu pro jeden nebo více řádků v prodejním dokladu, nejprve vyberte dodavatele, od kterého chcete zboží koupit a následně použijte funkci **Vytvořit nákupní fakturu**.

> [!NOTE]
> Tato funkce vytvoří nákupní fakturu za přesné množství zboží ve vybraném prodejním dokladu. Chcete-li změnit množství na nákup, musíte po vytvoření fakturu upravit.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Otevřete prodejní fakturu, pro kterou chcete zboží zakoupit.
3. Vyberte jeden nebo více řádků prodejní faktury, které chcete použít na nákupní faktuře. Chcete-li použít všechny řádky prodejní faktury, vyberte všechny z nich nebo nevyberte žádný.
4. Vyberte akci **Vytvořit nákupní fakturu**.
5. Vyberte buď **Všechny řádky** nebo **Vybrané řádky** a poté vyberte tlačítko **OK**.
6. V zobrazeném seznamu dodavatelů vyberte dodavatele, od kterého chcete koupit všechno zboží, a poté zvolte tlačítko **OK**.

   Je vytvořena nákupní faktura, která obsahuje jeden, více než jeden nebo všechny řádky na prodejní faktuře.
7. Pokračujte ve zpracování nákupní faktury, například úpravou nebo přidáním řádků nákupní faktury. Pro více informací navštivte [Záznam nákupů](purchasing-how-record-purchases.md).

## Viz také
[Nákup](purchasing-manage-purchasing.md)  
[Záznam nákupu](purchasing-how-record-purchases.md)  
[Fakturace prodeje](sales-how-invoice-sales.md)  
[Evidence nových dodavatelů](purchasing-how-register-new-vendors.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
