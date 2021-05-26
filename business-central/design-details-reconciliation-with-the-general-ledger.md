---
    title: Design Details - Reconciliation with the General Ledger | Microsoft Docs
    description: This topic describes reconciliation with the general ledger when you post inventory transactions, such as sales shipments, production output, or negative adjustments.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: design, reconciliation, general ledger, inventory
    ms.date: 04/01/2021
    ms.author: edupont

---
# Detaily návrhu: Odsouhlasení s hlavní knihou
Při zaúčtování skladových transakcí, jako jsou prodejní dodávky, výstup výroby nebo záporné úpravy, jsou změny množství a hodnoty zásob zaznamenány v položkách zboží a v položkách ocenění. Dalším krokem v procesu je zaúčtování hodnot zásob na účty zásob ve financích.

Existují dva způsoby, jak sladit položky inventury s financemi:

* Ručně spuštěním dávkové úlohy **Účtování nákladů na zboží**.
* Automaticky, pokaždé, když zaúčtujete skladovou transakci.

## Dávková úloha Účtování nákladů na zboží
Když spustíte dávkovou úlohu **Účtování nákladů na zboží** jsou věcné položky vytvořeny na základě položek ocenění. Máte možnost shrnout věcné položky pro každou položku ocenění nebo vytvořit věcné položky pro každou kombinaci data zaúčtování, kódu lokace, účto skupiny zboží, obecné účto skupiny zboží a obecné obchodní účto skupiny.

Zúčtovací data věcných položek jsou nastavena na zúčtovací datum odpovídající položky ocenění, s výjimkou případů, kdy položka ocenění spadá do uzavřeného účetního období. V tomto případě je položka ocenění přeskočena a je nutné změnit nastavení financí nebo nastavení uživatele, aby bylo možné zaúčtování v rozsahu dat.

Když spustíte dávkovou úlohu **Účtování nákladů na zboží** se mohou zobrazit chyby z důvodu chybějícího nastavení nebo nekompatibilního nastavení dimenze. Pokud dávková úloha narazí na chyby v nastavení dimenze, přepíše tyto chyby a použije dimenzi položky ocenění. U dalších chyb dávková úloha nezaúčtuje položky ocenění a vypíše je na konci sestavy v části s názvem **Přeskočené položky**. Chcete-li tyto položky zaúčtovat, musíte nejprve opravit chyby. Chcete-li zobrazit seznam chyb před spuštěním dávkové úlohy, můžete spustit sestavu **Účtování nákladů  na zboží - test**. Tato sestava obsahuje seznam všech chyb, ke kterým došlo během testovacího účtování. Chyby můžete opravit a poté spustit dávkovou úlohu zaúčtování nákladů skladu, aniž byste přeskakovali jakékoli položky.

## Automatické zaúčtování nákladů
Chcete-li nastavit účtování nákladů do financí tak, aby se spouštěla automaticky při zaúčtování skladové transakce, zaškrtněte políčko **Automatické účtování nákladů** na stránce **Nastavení zásob**. Datum zaúčtování věcné položky je stejné jako datum zaúčtování položky zboží.

## Typy účtů
Během odsouhlasení jsou hodnoty zásob zaúčtovány v rozvaze na skladový účet. Stejná částka, ale s opačným znaménkem, je zaúčtována na příslušný vyrovnávací účet. Vyrovnávacím účtem je obvykle účet vvýsledovky. Když však zaúčtujete přímé náklady související se spotřebou nebo výstupem, je vyrovnávací účet konečný účet rozvažný. Typ položky zboží a položky ocenění určuje, na který účet hlavní knihy se má účtovat.

Typ položky označuje, na který účet hlavní knihy se má zaúčtovat. To je určeno buď znaménkem množství na vstupu na položke zboží nebo oceněným množstvím na vstupu na položce ocenění, protože množství mají vždy stejné znaménko. Například položka prodeje s kladným množstvím popisuje pokles zásob způsobený prodejem a položka prodeje se záporným množstvím popisuje nárůst zásob způsobený výnosem z prodeje.

### Příklad
Následující příklad ukazuje řetěz kol, která je vyrobena ze zakoupených částí. Tento příklad ukazuje, jak se v typickém scénáři používají různé typy účtů hlavní knihy.

Je zaškrtnuto políčko **Účtování oček.nákladů do fin.** na stránce **Nastavení zásob** a je definováno následující nastavení.

Následující tabulka ukazuje, jak jsou části nastavené na kartě zboží.

| Nastavení pole | Hodnota |
|-----------------|-----------|  
| **Metoda ocenění** | Standardní |
| **Pevná pořizovací cena** | 1,00 LM |
| **Režijní náklady** | 0,02 LM |

Následující tabulka ukazuje, jak je řetěz nastaven na kartě zboží.

| Nastavení pole | Hodnota |
|-----------------|-----------|  
| **Metoda ocenění** | Standardní |
| **Pevná pořizovací cena** | 150,00 LM |
| **Režijní náklady** | 25,00 LM |

Následující tabulka ukazuje, jak je pracovní centrum nastaveno na kartě pracovního centra.

| Nastavení pole | Hodnota |
|-----------------|-----------|  
| **Nákupní cena** | 2,00 LM |
| **Procento nepřímých nákladů** | 10 |

##### Scénář
1. Uživatel zakoupí 150 částí a zaúčtuje nákupní objednávku jako přijatou. (Nákup)
2. Uživatel zaúčtuje nákupní objednávku jako fakturovanou. Tím se vytvoří částka režijních nákladů 3,00 LM, která má být přidělena, a částka odchylky 18,00 LM. (Nákup)

   1. Pozatímní účty jsou vymazány. (Nákup)
   2. Přímé náklady jsou zaúčtovány. (Nákup)
   3. Nepřímé náklady se vypočítají a zaúčtují. (Nákup)
   4. Nákupní odchylka se vypočítá a zaúčtuje (pouze u položek se standardními náklady). (Nákup)
3. Uživatel prodá jeden řetězec a zaúčtuje prodejní objednávku tak, jak byla dodána. (Prodej)
4. Uživatel zaúčtuje prodejní objednávku jako fakturovanou. (Prodej)

   1. Pozatímní účty jsou vymazány. (Prodej)
   2. Náklady na prodané zboží (NNPZ) jsou zaúčtovány. (Prodej)

      ![Výsledky zaúčtování prodeje na finanční účty](media/design_details_inventory_costing_3_gl_posting_sales.png "Výsledky zaúčtování prodeje na finanční účty")
5. Uživatel zaúčtuje spotřebu 150 částí, což je počet částí použitých k vytvoření jednoho řetězce. (Spotřeba, Materiál)

   ![Výsledky zaúčtování materiálu na finanční účty](media/design_details_inventory_costing_3_gl_posting_material.png "Výsledky zaúčtování materiálu na finanční účty")
6. Pracovní centrum využilo na výrobu řetězu 60 minut. Uživatel zaúčtuje náklady převodu. (Spotřeba, Kapacita)

   1. Přímé náklady jsou zaúčtovány. (Spotřeba, Kapacita)
   2. Nepřímé náklady se vypočítají a zaúčtují. (Spotřeba, Kapacita)

      ![Výsledky účtování kapacity na finanční účty](media/design_details_inventory_costing_3_gl_posting_capacity.png "Výsledky účtování kapacity na finanční účty")
7. Uživatel zaúčtuje očekávané náklady na jeden řetězec. (Výstup)
8. Uživatel dokončí výrobní zakázku a spustí dávkovou úlohu **Adjustace nákladů položek zboží**. (Výstup)

   1. Pozatímní účty jsou vymazány. (Výstup)
   2. Přímé náklady se převádí z účtu NV na skladový účet. (Výstup)
   3. Nepřímé náklady (režijní náklady) se převádí z účtu nepřímých nákladů na účet zásob. (Výstup)
   4. Výsledkem je částka odchylky 157,00 LM. Odchylky se počítají pouze u položek se standardními náklady. (Výstup)

      ![Výsledky zaúčtování výstupu na finanční účty](media/design_details_inventory_costing_3_gl_posting_output.png "Výsledky zaúčtování výstupu na finanční účty")

      > [!NOTE]  
      > Kvůli zjednodušení je zobrazen pouze jeden účet odchylky. Ve skutečnosti existuje pět různých účtů:
      >
      > * Odchylka materiálu
      > * Odchylka kapacit
      > * Odchylka kapacitních rež.nákl.
      > * Odchylka subdodávky
      > * Odchylka režijních nákladů výroby

9. Uživatel přehodnocuje řetězec z 150,00 LM na 140,00 LM. (Adjustace/Přecenění/Zaokrouhlení/Transfer)

   ![Výsledky zaúčtování adjustace na finanční účty](media/design_details_inventory_costing_3_gl_posting_adjustment.png "Výsledky zaúčtování adjustace na finanční účty")

Pro více informací o vztahu mezi typy účtů a různými typy položek ocenění navštivte [Detaily návrhu: Účty hlavní knihy](design-details-accounts-in-the-general-ledger.md).

## Viz také
[Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md)     
[Detaily návrhu: Účtování očekávaných nákladů](design-details-expected-cost-posting.md)     
[Detaily návrhu: Úprava nákladů](design-details-cost-adjustment.md)  
[Správa nákladů zásob](finance-manage-inventory-costs.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]