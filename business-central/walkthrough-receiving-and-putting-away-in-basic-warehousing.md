---
    title: Walkthrough - Receiving and Putting Away in Basic Warehouse Configurations | Microsoft Docs
    description: In Business Central, the inbound processes for receiving and putting away can be performed in four ways using different functionalities depending on the warehouse complexity level.
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
# Návod: Příjem a zaskladnění v základních konfiguracích skladu

**Poznámka**: Tento návod musí být proveden na demonstrační společnost s možností **Úplné vyhodnocení - úplný vzorek dat**, která je k dispozici v prostředí Sandbox. Pro více informací navštivte [Vytváření prostředí Sandbox](across-how-create-sandbox-environment.md).

V [!INCLUDE[d365fin](includes/d365fin_md.md)], příchozí procesy pro příjem a zaskladnění lze provádět čtyřmi způsoby pomocí různých funkcí v závislosti na úrovni složitosti skladu.

| Metoda | Vstupní proces | Přihrádky | Příjmy | Zaskladnění | Úroveň složitosti (viz [Detaily návrhu: Nastavení skladu](design-details-warehouse-setup.md)) |
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
| A | Zaúčtování příjemky a zaskladnění z řádku objednávky | X | 2 |
| B | Zaúčtování příjemky a zaskladnění z dokladu zaskladnění skladu | X | 3 |
| C | Zaúčtování příjemky a zaskladnění z příjemky skladu | X | 4/5/6 |
| D | Zaúčtování příjemky z příjemky skladu a zaúčtování zaskladnění z dokladu zaskladnění skladu | X | X | 4/5/6 |

Pro více informací navštivte [Detaily návrhu: Vstupní procesy skladu](design-details-inbound-warehouse-flow.md).

Následující návod ukazuje metodu B v předchozí tabulce.

## Návod
V základních konfiguracích skladu, kde je vaše lokace nastavena tak, aby vyžadovala zpracování zaskladnění, ale nepřijímala zpracování, použijte stránku **Zaskladnění zásob** k zaznamenávání a zaúčtování informací o zaskladnění a příjmu pro vaše vstupní původní doklady. Vstupním původním dokladem může být nákupní objednávka, objednávka prodejní vratky, vstupní objednávka transferu nebo výrobní zakázka s výstupem, který je připraven k odeslání.

> [!NOTE]
> Přestože se nastavení nazývá **Vyžadovat vyskladnění** a **Vyžadovat zaskladnění**, můžete stále účtovat příjemky a dodávky přímo z původních obchodních dokladů v lokacích, kde zaškrtnete tato políčka.

Tento návod ukazuje následující úkoly.

- Nastavení lokace SILVER pro zaskladněné dodávky zásob.
- Nastavení lokace SILVER pro manipulaci s  přihrádky.
- Definování výchozí přihrádky pro zboží LS-81. (LS-75 je již nastaven v programu CRONUS.)
- Vytvoření nákupní objednávky pro dodavatele 10000 pro 40 reproduktorů.
- Ověření, zda jsou přihrádky zaskadnění přednastaveny pomocí nastavení.
- Vydání nákupní objednávky pro manipulaci se skladem.
- Vytvoření zaskladněných zásob na základě vydaného původního dokladu.
- Ověření, zda jsou přihrádky zaskladnění zděděny z nákupní objednávky.
- Registrace pohybu skladu do skladu a zároveň zaúčtování nákupní příjemky pro původní nákupní objednávku.

## Role
Tento návod ukazuje úkoly, které jsou prováděny následujícími uživatelskými rolemi:

- Manažer skladu
- Nákupčí
- Skladník

## Předpoklady
K dokončení tohoto návodu budete potřebovat:

- Nainstalovaný CRONUS CZ s.r.o.  
- Chcete-li se stát zaměstnancem skladu v lokaci SILVER, postupujte takto:

   1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaměstnanci skladu** a poté vyberte související odkaz.
   2. Vyberte pole **ID uživatele** a na stránce **Uživatelé** vyberte svůj vlastní uživatelský účet.
   3. Do pole **Kód lokace** zadejte SILVER.
   4. Vyberte pole **Výchozí**.

## Příběh
Ellen, vedoucí skladu společnosti CRONUS CZ s.r.o., vytvoří nákupní objednávku na 10 jednotek zboží LS-75 a 30 jednotek zboží LS-81 od dodavatele 10000, které mají být dodány do skladu SILVER. Když zásilka dorazí do skladu, John, pracovník skladu, zaskladní zboží do výchozích přehrádek definovaných pro zboží. Když Jan zaúčtuje zaskladnění, zboží se zaúčtuje jako přijaté do zásob a je k dispozici k prodeji nebo jiné poptávce.

## Nastavení lokací
Nastavení stránky **Karta lokace** definuje toky skladu společnosti.

### Nastavení lokace

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete kartu lokace SILVER.
3. Zaškrtněte políčko **Vyžadovat zaskladnění**.

   Pokračujte v nastavení výchozí přehrádky pro dvě čísla zboží, abyste určili, kde jsou zaskladněna.

4. Vyberte akci **Přihrádky**.
5. Vyberte první řádek pro přihrádku S-01-0001 a pak zvolte akci **Obsah**.

   Všimněte si, že na stránce **Obsah přihrádky** je položka LS-75 již nastavena jako obsah v přihrádce S-01-0001.

6. Vyberte akci **Nový**.
7. Vyberte pole **Pevné** a **Výchozí**.
8. Do pole **Číslo zboží** zadejte LS-81.

## Vytvoření nákupní objednávky
Nákupní objednávky jsou nejběžnějším typem vstupního původního dokladu.

### Vytvoření nákupní objednávky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vytvořte objednávku na dodavatele 10 000 v pracovní den (23. ledna) s následujícími řádky objednávek.

   | Zboží | Kód lokace | Kód přihrádky | Množství |
   |----------|-------------------|--------------|--------------|  
   | LS_75 | SILVER | S-01-0001 | 10 |
   | LS-81 | SILVER | S-01-0001 | 30 |

   > [!NOTE]
   > Kód přihrádky se zadává automaticky podle nastavení, které jste provedli v části “Nastavení lokace”.

   Pokračujte v oznámení skladu, že nákupní objednávka je připravena k zpracování ve skladu, jakmile dorazí dodávka.

4. Vyberte akci **Vydat**.

   Doručené reproduktory od prodejce 10000 dorazily do skladu SILVER, a John pokračuje, aby je zaskladnil.

## Příjem a zaskladnění zboží
Na stránce **Zaskladnění zásob** můžete spravovat všechny vstupní aktivity skladu pro konkrétní původní doklad, například nákupní objednávku.

### Přijem a zaskladnění zboží

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaskladnění zásob** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vyberte pole **Původní doklad** a poté vyberte **Nákupní objednávka**.
4. Vyberte pole **Číslo původu**, vyberte řádek pro nákup od dodavatele 10000 a poté stiskněte tlačítko **OK**.

   Případně zvolte akci **Kopie původ.dokladu** a poté vyberte nákupní objednávku.

5. Vyberte akci **Automat.vyplnit  množ.ke zprac.**.

   Alternativně v poli **Množství  ke zpracování** zadejte 10 a 30 v obou řádcích zaskladnění zásob.

6. Vyberte akci **Účtovat** poté vyberte **K příjmu** a poté vyberte tlačítko **OK**.

   40 reproduktorů je nyní zaregistrováno jako zaskladnění v přihrádce S-01-0001 a je vytvořen kladný záznam položky zboží odrážející zaúčtovanou nákupní příjemku.

## Viz také
[Zaskladnění zboží pomocí zaskladněními zásob](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  
[Nastavení základních skladů s provozními oblastmi](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Přesouvání komponent do provozní oblasti v základních konfiguracích skladu](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[Vyskladnění pro výrobu nebo montáž v základních konfiguracích skladu](warehouse-how-to-pick-for-production.md)  
[Ad Hoc přesun zboží v základních konfiguracích skladu](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Detaily návrhu: Vstupní procesy skladu](design-details-inbound-warehouse-flow.md)  
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
