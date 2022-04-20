---
title: Inventory and Warehouse Reports and Analytics
description: See which inventory and warehouse reports and analytics are available in the standard version of Business Central so that you can keep track of your business.
author: AndreiPanko

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa

---
# Přehledy a analýzy zásob a skladů v Business Central

Reporting zásob a skladu v [!INCLUDE [prod_short](includes/prod_short.md)] umožňuje skladovým a obchodním profesionálům získat přehledy a statistiky o současných a minulých zásobách a skladových aktivitách.

## Sestavy

Následující tabulka popisuje některé klíčové sestavy v rámci reportingu o zásobách a skladech.

| Sestava | ID Objektu | Popis |
|---------|---------|---------|
| **Plán dostupnosti zásob** | 707 | Pokud byste chtěli mít přehled o konkrétním zboží/skladových jednotkách a jejich dostupnosti. Tato sestava zobrazuje kumulované hodnoty, jako jsou hrubé požadavky, plánované a plánované příjmy, zásoby a další. |
| **Hodnota zásob** | 1001 | Zobrazí ocenění zásob pro vybrané zboží ve vašich zásobách. Sestava také zobrazuje informace o hodnotě zvýšení a snížení zásob v průběhu času. |
| **Expirace zboží - množství** | 5809 | Zobrazuje přehled množství vybraného zboží ve vašich zásobách, jejichž data expirace spadají do určitého období. Seznam zobrazuje počet jednotek vybraného zboží, jehož platnost vyprší v daném časovém období. Pro každou z položek, které zadáte do nastavení sestavy, se v tištěném dokumentu zobrazí jako počet jednotek, jejichž platnost vyprší během každého ze tří stejně dlouhých období a celkové množství zásob vybrané položky.<br>Nastavením filtrů můžete určit, co bude do sestavy zahrnuto. Pokud nenastavíte žádné filtry, bude sestava obsahovat všechny záznamy. Množství v sestavě odrážejí pouze množství položky, pro které byla definována data expirace. |
| **Skladba stáří zboží - množství** nebo **Skladba stáří zboží - hodnota** | 5807 nebo 5808 | Zobrazí přehled aktuálního stáří složení vybraného zboží v zásobách. Seznam zobrazuje počet jednotek nebo hodnotu vybraného zboží, které bylo přidáno nebo odebráno ze zásob a v jakém okamžiku. Zboží lze přidat nebo odebrat ze zásob v důsledku nákupů, prodejů a kladných a záporných úprav. |
| **Náklady na zásoby a ceník** | 716 | Zobrazí seznam informací o ceně pro vybraného zboží nebo skladové jednotky: přímé jednotkové náklady, poslední přímé náklady, jednotková cena, procento zisku a zisk. |
| **Přehled přihrádek skladu** | 7319 | Zobrazuje přehled skladových přihrádek, jejich nastavení a množství položek v přihrádkách. Tento přehled lze použít pro všechna umístění, která mají jako povinné pole "Přihrádka". |
| **Stav dodávky ze skladu** | 7313 | Zobrazuje přehled otevřených zdrojových dokladů s dodaným zbožím nebo zbožím, které má být odesláno, podle lokace. Tento přehled lze použít pro všechny lokace, které mají nastaveno **Vyžadovat dodání**. **Stav dodávky ze skladu** zobrazuje lokace, kódy přihrádek, stav dokladů a množství. |
| **Přehled vyskladnění zásob** | 813 | Zobrazí seznam prodejních objednávek, ve kterých je zboží zahrnuta. U každého zboží se zobrazují následující informace: řádek prodejní objednávky se jménem zákazníka, kód varianty, kód lokace, kód přihrádky, datum odeslání, množství k odeslání a měrná jednotka. U každého zboží se sečte množství, které má být dodáno. Sestava může být použita, kdyý se zboží bude vybírat ze zásob <br>Poznámka: tato funkce není k dispozici pro pokročilé funkce skladu. |
| **Adjustační přihrádka skladu** | 7320 | Tato speciální sestava je určena pouze pro pokročilé nastavení skladu a zobrazuje zbývající množství, která jsou ještě uložena v samotné adjustační přihrádce. Za normálních okolností by tato konkrétní přihrádka měla být prázdná. Jediným důvodem, proč se tato přihrádka zaplní, je výsledek fyzického počítání při inventuře nebo pokud bylo množství zboží odebráno nebo přidáno do skladu. |


## Úlohy

Následující články popisují některé klíčové úlohy pro analýzu stavu vaší firmy:

* [Vytváření sestav analýz](bi-how-create-analysis-views-reports.md)
* [Zobrazit dostupnost zboží](inventory-how-availability-overview.md)


## Viz také

[Nastavení zásob](inventory-setup-inventory.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa skladu](warehouse-manage-warehouse.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
