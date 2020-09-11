---
    title: Picking and Shipping in Basic Warehouse Configurations | Microsoft Docs
    description: In Business Central, the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Návod: Vyskladnění a přeprava v základních konfiguracích skladu

**Poznámka**: Tento návod musí být proveden na demonstrační společnost s možností **Úplné vyhodnocení - úplný vzorek dat**, která je k dispozici v prostředí Sandbox. Pro více informací navštivte [Vytváření prostředí Sandbox](across-how-create-sandbox-environment.md).

V [!INCLUDE[d365fin](includes/d365fin_md.md)] lze odchozí procesy pro výdej a expedici provádět čtyřmi způsoby pomocí různých funkcí v závislosti na úrovni složitosti skladu.

| Metoda | Vstupní proces | Přihrádky | Vyskladnění | Dodávky | Úroveň složitosti (viz [Detaily návrhu: Nastavení skladu](design-details-warehouse-setup.md)) |
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
| A | Zaúčtování vyskladnění a dodávky z řádku objednávky | X | 2 |
| B | Zaúčtování vyskladnění a dodávky z dokladu vyskladnění skladu | X | 3 |
| C | Zaúčtování vyskladnění a dodávky z dokladu dodávky ze skladu | X | 4/5/6 |
| D | Zaúčtování vyskladnění z dokladu o vyskladnění a zaúčtování dodávky z dokladu dodávky ze skladu | X | X | 4/5/6 |

Pro více informací navštivte [Detaily návrhu: Výstupní procesy skladu](design-details-outbound-warehouse-flow.md).

Následující návod ukazuje metodu B v předchozí tabulce.

## Návod
V základních konfiguracích skladu, kde je lokace nastavena tak, aby vyžadovala zpracování vyskladnění, ale ne zpracování dodávky, použijete stránku **Vyskladnění zásob** k zaznamenání a zaúčtování informací o vyskladnění a dodání výstupních zdrojových dokladů. Výstupním zdrojovým dokladem může být prodejní objednávka, objednávka nákupní vratky, výstupní objednávka transferu nebo výrobní zakázka s potřebou komponenty.

Tento návod ukazuje následující úkoly:

- Nastavení lokace SILVER pro vyskladnění zásob.
- Vytvoření prodejní objednávky pro zákazníka 10000 pro 30 reproduktorů.
- Vydání prodejní objednávky pro zpracování skladu.
- Vytvoření vyskladnění zásob na základě vydaného původního dokladu.
- Registrace přesunu skladu ze skladu a současně zaúčtování prodejní dodávky pro původní prodejní objednávku.

## Role
Tento návod ukazuje úkoly, které jsou prováděny následujícími uživatelskými rolemi:

- Manažer skladu
- Zpracovatel objednávek
- Skladník

## Předpoklady
K dokončení tohoto návodu budete potřebovat:

- Nainstalovaný CRONUS CZ s.r.o.  
- Chcete-li se stát zaměstnancem skladu v lokaci SILVER, postupujte takto:

   1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaměstnanci skladu** a poté vyberte související odkaz.
   2. Vyberte pole **ID uživatele** a na stránce **Uživatelé** vyberte svůj vlastní uživatelský účet.
   3. Do pole **Kód lokace** zadejte SILVER.
   4. Vyberte pole **Výchozí**.

- Zpřístupněte položku LS-81 v lokaci SILVER podle následujících kroků:

   1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky zboží** a poté vyberte související odkaz.
   2. Otevřete výchozí deník a vytvořte dva řádky deníku zboží s následujícími informacemi o pracovním datu (23. ledna).

      | Typ položky | Číslo zboží | Kód lokace | Kód přihrádky | Množství |
      |----------------|-----------------|-------------------|--------------|--------------|  
      | Příjem | LS-81 | SILVER | S-01-0001 **Poznámka:**  Výchozí přihrádka zboží v CRONUS | 20 |
      | Příjem | LS-81 | SILVER | S-01-0002 | 20 |

   3. Vyberte akci **Účtovat** a pak vyberte tlačítko **Ano**.

## Příběh
Ellen, vedoucí skladu společnosti CRONUS, nastaví sklad SILVER pro základní zpracování vyskladnění, kde pracovníci skladu zpracovávají odchozí objednávky jednotlivě. Zuzana, zpracovatelka objednávek, vytvoří prodejní objednávku na 30 jednotek zboží LS-81, které mají být dodány zákazníkovi 10000 ze skladu SILVER. John, pracovník skladu musí zajistit, že dodávka je připravena a doručena zákazníkovi. John řídí všechny úkoly na stránce **Vyskladnění zásob**, která automaticky odkazuje na přihrádky, ve kterých je uložena LS-81.

## Nastavení lokací
Nastavení stránky **Karta lokace** definuje toky skladu společnosti.

### Nastavení lokace
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete kartu lokace SILVER.
3. Zaškrtněte políčko **Vyžadovat vyskladnění**.

## Vytvoření prodejní objednávky
Nejběžnějším typem výstupního původního dokladu jsou prodejní objednávky.

### Vytvoření prodejní objednávky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vytvořte prodejní objednávku pro zákazníka 10 000 v pracovní den (23. ledna) s následujícím řádkem prodejní objednávky.

   | Zboží | Kód lokace | Množství |
   |----------|-------------------|--------------|  
   | LS_81 | SILVER | 30 |

   Pokračujte oznámením skladu, že prodejní objednávka je připravena pro zpracování skladu.

4. Vyberte akci **Vydat**.

   John poté pokračuje činnostmi vyskladnit a odeslat pro prodané zboží.

## Vyskladnění a přeprava zboží
Na stránce **Vyskladnění zásob** můžete spravovat všechny aktivity výstupního skladu pro konkrétní původní doklad, například prodejní objednávku.

### Vyskladnění a dodání zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění zásob** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vyberte pole **Původní doklad** a poté vyberte **Prodejní objednávka**.
4. Vyberte pole **Číslo původu**, vyberte řádek prodeje zákazníkovi 10000 a pak zvolte tlačítko **OK**.

   Případně vyberte akci **Kopie původ.dokladu** a poté vyberte prodejní objednávku.
5. Vyberte akci **Automat.vyplnit  množ.ke zprac.**.

   Alternativně v poli **Množství  ke zpracování** zadejte 10 a 30 na dvou řádcích vyskladnění zásob.
6. Vyberte akci **Účtovat** vyberte **Dodání** a poté zvolte tlačítko **OK**.

   30 reproduktorů je nyní zaregistrováno jako vyskladněno z přihrádek S-01-0001 a S-01-0002 a je vytvořen záporný záznam položky zboží odrážející zaúčtovanou prodejní dodávku.

## Viz také
[Vyskladnění zboží pomocí vyskladnění zásob](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Vyskladnění zboží pro dodávku ze skladu](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Nastavení základních skladů s provozními oblastmi](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Přesouvání komponent do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Vyskladnění pro výrobu nebo montáž v základních konfiguracích skladu](warehouse-how-to-pick-for-production.md)  
[Ad Hoc přesun zboží v základních konfiguracích skladu](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Detaily návrhu: Výstupní procesy skladu](design-details-outbound-warehouse-flow.md)  
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
