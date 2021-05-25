---
    title: Design Details - Revaluation | Microsoft Docs
    description: You can revalue the inventory based on the valuation base that most accurately reflects the inventory value. You can also backdate a revaluation, so that the cost of goods sold (COGS) is correctly updated for items that have already been sold. Items using the Standard costing method that have not been completely invoiced can also be revalued.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2021
    ms.author: edupont

---
# Detaily návrhu: Přecenění
Zásoby můžete přeceněnit na základě ocenění základu, který nejpřesnější odráží hodnotu zásob. Můžete také zpětně datovat přecenění, aby byly náklady na prodané zboží (NNPZ) správně aktualizovány pro zboží, které již bylo prodáno. Zboží používá metodu standardních nákladů a to které nebylo zcela fakturováno, lze také přecenět.

V [!INCLUDE[prod_short](includes/prod_short.md)], je podporována následující flexibilita, pokud jde o přecenění:

- Přeceněné množství lze vypočítat pro libovolné datum, také zpět v čase.
- U zboží, které používá metodu standardních nákladů jsou položky očekávaných nákladů zahrnuty do přecenění.
- Jsou zjištěny poklesy zásob ovlivněné přeceněním.

## Výpočet přeceněného množství
Přeceněné množství je zbývající množství na skladě, které je k dispozici k přecenění k danému datu. Vypočítá se jako součet množství zcela fakturovaných položek zboží, které mají zúčtovací datum stejný nebo dřívější než zúčtovací datum přecenění.

> [!NOTE]  
> Se zbožím, které používá standardní metodu ocenění se při výpočtu přeceněného množství podle zboží, lokace a variantu zaobchází odlišně. Množství a hodnoty položek zboží, které nejsou zcela fakturovány, jsou zahrnuty do přeceněného množství.

Po zaúčtování přecenění můžete zaúčtovat zvýšení nebo snížení zásob s datem zaúčtování, které předchází datu zaúčtování přecenění. Toto množství však přehodnocení neovlivní. Pro vyvážení zásob se uvažuje pouze původní přeceněné množství.

Vzhledem k tomu, že přecenění lze použít k libovolnému datu, musíte mít znalosti o tom, kdy je zboží z finančního hlediska považováno za součást zásob. Například kdy je zboží na skladě a kdy je zboží v procesu práce (NV).

### Příklad
Následující příklad ilustruje, kdy zboží NV přechází a stává se součásti zásob. Příklad je založen na výrobě řetězu se 150 částmi.

![Zásoby a přecenění NV](media/design_details_inventory_costing_10_revaluation_wip.png "Zásoby a přecenění NV")

**1Q**: Uživatel zaúčtuje zakoupené části jako přijaté. V následující tabulce je uvedena výsledná položka zboží.

| Zúčtovací datum | Zboží | Typ položky | Množství | Číslo položky |
|------------------|----------|----------------|--------------|---------------|  
| 01.01.20 | ČÁST | Nákup | 150 | 1 |

> [!NOTE]  
> Nyní je pro přecenění k dispozici zboží používající metodu standardního ocenění.

**1V**: Uživatel zaúčtuje zakoupené části řetězu jako fakturované a tyto části se z finančního hlediska stanou součástí zásob. Následující tabulka ukazuje výsledné hodnoty.

| Zúčtovací datum | Typ položky | Datum ocenění | Částka nákladů (skutečná) | Číslo položky zboží | Číslo položky |
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
| 15.01.20 | Přímé náklady | 01.01.20 | 15000 | 1 | 1 |

**2Q + 2V**: Uživatel zaúčtuje zakoupené části řetězu jako spotřebované pro výrobu železného řetězu. Z finančního hlediska se části stávají součástí zásob nedokončené výroby.  V následující tabulce je uvedena výsledná položka zboží.

| Zúčtovací datum | Zboží | Typ položky | Množství | Číslo položky |
|------------------|----------|----------------|--------------|---------------|  
| 01.02.20 | ČÁST | Spotřeba | -150 | 1 |

Následující tabulka ukazuje výsledné hodnoty.

| Zúčtovací datum | Typ položky | Datum ocenění | Částka nákladů (skutečná) | Číslo položky zboží | Číslo položky |
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
| 01.02.20 | Přímé náklady | 01.02.20 | -150,00 | 2 | 2 |

Datum ocenění je nastaveno na datum účtování spotřeby (02-01-20) jako pravidelné snížení zásob.

**3Q**: Uživatel zaúčtuje řetěz jako výstup a dokončí výrobní zakázku. V následující tabulce je uvedena výsledná položka zboží.

| Zúčtovací datum | Zboží | Typ položky | Množství | Číslo položky |
|------------------|----------|----------------|--------------|---------------|  
| 15.02.20 | ŘETĚZ | Výstup | 1 | 3 |

**3V**: Uživatel spustí dávkovou úlohu **Adjustace nákladů položek zboží**, která zaúčtuje řetěz jako fakturovanou, což znamená, že veškerá spotřeba materiálu byla zcela fakturována. Z finančního hlediska již části řetězu nejsou součástí zásob nedokončené výroby, pokud je výstup zcela fakturován a adjustován. Následující tabulka ukazuje výsledné hodnoty.

| Zúčtovací datum | Typ položky | Datum ocenění | Částka nákladů (skutečná) | Číslo položky zboží | Číslo položky |
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
| 15.01.20 | Přímé náklady | 01.01.20 | 15000 | 2 | 2 |
| 01.02.20 | Přímé náklady | 01.02.20 | -150,00 | 2 | 2 |
| 15.02.20 | Přímé náklady | 15.02.20 | 15000 | 3 | 3 |

## Očekávané náklady při přecenění
Přeceněné množství se vypočítá jako součet množství pro zcela fakturované položky zboží se zúčtovacím datem rovnajícím se datu přecenění nebo dřívějšímu datu. To znamená, že pokud je některé zboží přijato/dodáno, ale není fakturováno, nelze vypočítat jeho hodnotu zásob. Zboží, které používají metodu standardního ocenění, nejsou v tomto ohledu omezeny.

> [!NOTE]  
> Dalším typem očekávaných nákladů, které lze přecenit, jsou zásoby NV v rámci určitých pravidel. Pro více informací navštivte [Přecenění zásob NV](design-details-revaluation.md#wip-inventory-revaluation).

Při výpočtu přeceněného množství pro zboží pomocí metody standardního ocenění jsou do výpočtu zahrnuty položky zboží, které nebyly zcela fakturovány. Tyto položky jsou pak při zaúčtování přecenění přeceněny. Při fakturaci přeceněné položky se vytvoří následující položky ocenění:

- Obvyklá fakturovaná položka ocenění s typem položky **Přímé náklady**. Výše nákladů na tento záznam je přímým nákladem ze zdrojového řádku.
- Položka ocenění s typem položky **Odchylka**. Tato položka zaznamenává rozdíl mezi fakturovanou cenou a přeceněnou standardní cenou.
- Položka ocenění s typem položky **Přecenění**. Tato položka zaznamenává stornování přecenění očekávaných nákladů.

### Příklad
Následující příklad, který je založen na výrobě řetězu v předchozím příkladu, ilustruje, jak jsou vytvořeny tři typy položek. Je založen na následujícím scénáři:

1. Uživatel zaúčtuje zakoupené části řetězu jako přijaté s jednotkovou cenou 2,00 CZK.
2. Uživatel poté zaúčtuje přecenění částí s novými jednotkovými náklady ve výši 3,00 CZK a aktualizuje standardní náklady na 3,00 CZK.
3. Uživatel zaúčtuje původní nákup částí jako fakturovaný, což vytváří následující:

   1. Fakturovaná položka ocenění s typem položky **Přímé náklady**.
   2. Položka ocenění s typem položky **Přecenění** pro záznam stornování přecenění očekávaných nákladů.
   3. Položka ocenění s typem položky Odchylka, zaznamenávající rozdíl mezi fakturovanou cenou a přeceněnou standardní cenou.  
      Následující tabulka ukazuje výsledné hodnoty.

| Krok | Zúčtovací datum | Typ položky | Datum ocenění | Částka nákladů (očekávaná) | Částka nákladů (skutečná) | Číslo položky zboží | Číslo položky |
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
| 1. | 15.01.20 | Přímé náklady | 15.01.20 | 300,00 | 0,00 | 1 | 1 |
| 2. | 20.01.20 | Přecenění | 20.01.20 | 15000 | 0,00 | 1 | 2 |
| 3.a. | 15.01.20 | Přímé náklady | 15.01.20 | -300,00 | 0,00 | 1 | 3 |
| 3.b. | 15.01.20 | Přecenění | 20.01.20 | -150,00 | 0,00 | 1 | 4 |
| 3.c. | 15.01.20 | Odchylka | 15.01.20 | 0,00 | 450,00 | 1 | 5 |

## Určení, zda je snížení zásob ovlivněno přeceněním
Datum zaúčtování nebo přecenění se používá k určení, zda je pokles zásob ovlivněn přeceněním.

V následující tabulce jsou uvedena kritéria používaná pro zboží, které nepoužívá metodu průměrného ocenění.

| Scénář | Číslo položky | Načasování | Ovlivněno přeceněním |
|--------------|---------------|------------|-----------------------------|  
| A | Číslo položky před přeceněním | Zaúčtovací datum dřívější než přecenění | Ne |
| B | Číslo položky dřívější než přecenění | Rovno zúčtovacímu datu přecenění | Ne |
| C | Číslo položky dřívější než přecenění | Pozdější než zúčtovací datum přecenění | Ano |
| D | Později než číslo položky přecenění | Zaúčtovací datum dřívější než přecenění | Ano |
| E | Později než číslo položky přecenění | Rovno zúčtovacímu datu přecenění | Ano |
| F | Později než číslo položky přecenění | Pozdější než zúčtovací datum přecenění | Ano |

### Příklad
Následující příklad, který ilustruje přecenění zboží, které používá metodu ocenění FIFO, je založen na následujícím scénáři:

1. Uživatel 01.01.20 zaúčtuje nákup 6 jednotek.
2. Dne 01.02.20 zaúčtuje uživatel prodej 1 jednotky.
3. Dne 01.03.20 zaúčtuje uživatel prodej 1 jednotky.
4. Dne 01.04.20 zaúčtuje uživatel prodej 1 jednotky.
5. Dne 01.03.20 uživatel vypočítá hodnotu zásob pro zboží a zaúčtuje přecenění jednotkových nákladů zboží z 10,00 CZK na 8,00 CZK.
6. Dne 01.02.20 zaúčtuje uživatel prodej 1 jednotky.
7. Dne 01.03.20 zaúčtuje uživatel prodej 1 jednotky.
8. Dne 01.04.20 zaúčtuje uživatel prodej 1 jednotky.
9. Uživatel spustí dávkovou úlohu **Adjustace nákladů položek zboží**.

Následující tabulka ukazuje výsledné hodnoty.

| Scénář | Zúčtovací datum | Typ položky | Datum ocenění | Oceněné množství | Částka nákladů (skutečná) | Číslo položky zboží | Číslo položky |
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
|  | 01.01.20 | Nákup | 01.01.20 | 6 | 60,00 | 1 | 1 |
|  | 01.03.20 | Přecenění | 01.03.20 | 4 | -8,00 | 1 | 5 |
| A | 01.02.20 | Prodej | 01.02.20 | -1 | -10,00 | 2 | 2 |
| B | 01.03.20 | Prodej | 01.03.20 | -1 | -10,00 | 3 | 3 |
| C | 01.04.20 | Prodej | 01.04.20 | -1 | -10,00 | 4 | 4 |
|  | 01.04.20 | Prodej | 01.04.20 | -1 | 2,00 | 4 | 9 |
| D | 01.02.20 | Prodej | 01.03.20 | -1 | -10,00 | 5 | 6 |
|  | 01.02.20 | Prodej | 01.03.20 | -1 | 2,00 | 5 | 10 |
| E | 01.03.20 | Prodej | 01.03.20 | -1 | -10,00 | 6 | 7 |
|  | 01.03.20 | Prodej | 01.03.20 | -1 | 2,00 | 6 | 11 |
| F | 01.04.20 | Prodej | 01.04.20 | -1 | -10,00 | 7 | 8 |
|  | 01.04.20 | Prodej | 01.04.20 | -1 | 2,00 | 7 | 12 |

## Přecenění zásob NV
Přecenění zásob NV znamená přecenění komponent, které jsou v době přecenění registrovány jako součást zásob nedokončené výroby.

S ohledem na to je důležité stanovit konvence, kdy je zboží z finančního hlediska považováno za součást zásob NV. V [!INCLUDE[prod_short](includes/prod_short.md)], existují následující konvence:

- Zakoupená komponenta se stává součástí zásob suroviny od zaúčtování nákupu jako fakturovaného.
- Nakoupená/podsestavovaná komponenta se stává součástí zásob nedokončené výroby od zaúčtování spotřeby v souvislosti s výrobní zakázkou.
- Nakoupená/podsestavovaná komponenta zůstává součástí zásob nedokončené výroby až do doby, kdy je fakturována výrobní zakázka (vyrobené zboží).

Způsob, jakým je nastaveno datum ocenění pro zadání hodnoty spotřeby, se řídí stejnými pravidly jako u zásob jiných než NV. Pro více informací navštivte [Určení, zda je snížení zásob ovlivněno přeceněním](design-details-revaluation.md#determining-whether-an-inventory-decrease-is-affected-by-revaluation).

Zásoby nedokončené výroby lze přecenit, pokud datum přecenění není pozdější než zúčtovací datum odpovídajících položek zboží typu Spotřeba a pokud odpovídající výrobní zakázka ještě nebyla fakturována.

> [!CAUTION]  
> Sestava **Hodnota zásob – vl.výroba** zobrazuje hodnotu zaúčtovaného zboží výrobní zakázky, a proto může být trochu matoucí pro zboží NV, které bylo přeceněné.

## Viz také
[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)     
[Detaily návrhu: Metody ocenění](design-details-costing-methods.md)     
[Detaily návrhu: Hodnota zásob](design-details-inventory-valuation.md)  
[Správa nákladů zásob](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]