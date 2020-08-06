---
    title: Receiving and Putting Away in Advanced Warehousing | Microsoft Docs
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
# Návod: Příjem a zaskladnění v rozšířených konfiguracích skladu

**Poznámka**: Tento návod musí být proveden na demonstrační společnost s možností **Úplné vyhodnocení - úplný vzorek dat**, která je k dispozici v prostředí Sandbox. Pro více informací navštivte [Vytváření prostředí Sandbox](across-how-create-sandbox-environment.md).

V [!INCLUDE[d365fin](includes/d365fin_md.md)], příchozí procesy pro příjem a zaskladnění lze provádět čtyřmi způsoby pomocí různých funkcí v závislosti na úrovni složitosti skladu.

| Metoda | Vstupní proces | Přihrádky | Příjmy | Zaskladnění | Úroveň složitosti (viz [Detaily návrhu: Nastavení skladu](design-details-warehouse-setup.md)) |
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
| A | Zaúčtování příjemky a zaskladnění z řádku objednávky | X | 2 |
| B | Zaúčtování příjemky a zaskladnění z dokladu zaskladnění skladu | X | 3 |
| C | Zaúčtování příjemky a zaskladnění z příjemky skladu | X | 4/5/6 |
| D | Zaúčtování příjemky z příjemky skladu a zaúčtování vyskladněnní z dokladu zaskladnění skladu | X | X | 4/5/6 |

Pro více informací navštivte [Detaily návrhu: Vstupní procesy skladu](design-details-inbound-warehouse-flow.md).

Následující návod ukazuje metodu D v předchozí tabulce.

## Návod
V pokročilých konfiguracích skladu, kde je lokace nastavena tak, aby vyžadovala příjem zpracování kromě zpracování zaskladněného zboží, použijete stránku **Příjemka na sklad** k zaznamenání a zaúčtování příjmu zboží na více vstupních objednávkách. Při zaúčtování příjemky na sklad je vytvořeno jedno nebo více dokladů zaskladnění, aby pracovníci skladu dostali pokyn, aby přijaté zboží převzali a umístili na určená místa podle nastavení přihrádky nebo do jiných přihrádek. Konkrétní lokace zboží se zaznamená při registraci zaskladněného zboží. Vstupním původním dokladem může být objednávka, objednávka prodejní vratky, objednávka vstupu transferu nebo montážní nebo výrobní objednávka s výstupem, která je připravena k odeslání. Pokud je příjemka vytvořena z příchozí objednávky, lze pro příjemku načíst více než jeden vstupní zdrojový doklad. Pomocí této metody můžete zaregistrovat mnoho zboží, které přichází z různých vstupních objednávek s jedním potvrzením.

Tento návod ukazuje následující úkoly.

- Nastavení lokace WHITE pro příjem a zaskladnění.
- Vytvoření a vydání dvou objednávek pro úplné zpracování ve skladu.
- Vytvoření a zaúčtování dokladu příjemky skladu pro více řádků nákupní objednávky od konkrétních dodavatelů.
- Registrace zaskladnění pro přijaté zboží.

## Role
Tento návod ukazuje úkoly, které jsou prováděny následujícími uživatelskými rolemi:

- Manažer skladu
- Nákupčí
- Zaměstnanci určení pro příjem
- Skladník

## Předpoklady
K dokončení tohoto návodu budete potřebovat:

- Nainstalovaný CRONUS CZ s.r.o.  
- Chcete-li se stát zaměstnancem skladu v lokaci WHITE, postupujte takto:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaměstnanci skladu** a poté vyberte související odkaz.
2. Vyberte pole **ID uživatele** a na stránce **Uživatelé** vyberte svůj vlastní uživatelský účet.
3. Do pole **Kód lokace** zadejte WHITE.
4. Vyberte pole **Výchozí**.

## Příběh
Ellen, vedoucí skladu společnosti CRONUS CZ s.r.o., vytvoří dvě nákupní objednávky pro zboží příslušenství od dodavatelů 10000 a 20000, které mají být dodány do skladu WHITE. Když dodávky dorazí do skladu, Sammy, který je zodpovědný za příjem zboží od prodejců 10000 a 20000, použije filtr k vytvoření řádků příjmu pro nákupní objednávky přicházející od těchto dvou dodavatelů. Sammy zaúčtuje přijaté zboží do zásob v jedné příjemke na skladu a zpřístupní zboží k prodeji nebo jiné poptávce. Jan, pracovník skladu, převezme zboží z přijímající přihrádky a zaskladní je. Všechny jednotky umístí do výchozích přihrádek, s výjimkou 40 ze 100 přijatých závěsů, které zaskladní v montážním oddělení pomocí rozdělení řádku zaskladnění. Když Jan zaeviduje zaskladnění, obsah přihrádky se aktualizuje a zboží je k dispozici pro vyskladnění ze skladu.

## Kontrola nastavení lokace WHITE
Nastavení stránky **Karta lokace** definuje toky skladu společnosti.

### Kontrola nastavení lokace

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete kartu lokace WHITE.
3. Všimněte si na záložce **Sklad**, že je zaškrtnuto políčko  **Řízené zaskladnění/vyskladnění**.

   To znamená, že lokace je nastavena na nejvyšší úroveň složitosti, což se odráží ve skutečnosti, že jsou zaškrtnuta všechna políčka pro manipulaci se skladem na záložce.

4. Všimněte si na záložce **Přihrádky**, že přihrádky jsou určeny v polích **Kód příjmové přihrádky** a **Kód dodací přihrádky**.

To znamená, že při vytváření příjemky ze skladu je tento kód přihrádky ve výchozím nastavení zkopírován do hlavičky dokladu příjemky skladu a do řádků výsledného zaskladnění skladu.

## Vytvoření nákupních objednávek
Nákupní objednávky jsou nejběžnějším typem vstupního zdrojového dokladu.

### Vytvoření nákupních objednávek

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní objednávky** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vytvořte objednávku na dodavatele 10 000 v pracovní den (23. ledna) s následujícími řádky objednávek.

   | Zboží | Kód lokace | Množství |
   |----------|-------------------|--------------|  
   | 70200 | WHITE | 100 KS |
   | 70201 | WHITE | 50 KS |

   Pokračujte v oznámení skladu, že nákupní objednávka je připravena k zpracování ve skladu, jakmile dorazí dodávka.

4. Vyberte akci **Vydat**.

   Pokračujte vytvořením druhé nákupní objednávky.

5. Vyberte akci **Nový**.
6. Vytvořte nákupní objednávku na dodavatele 20000 v pracovní den s následujícími řádky objednávky.

   | Zboží | Kód lokace | Množství |
   |----------|-------------------|--------------|  
   | 70100 | WHITE | 10 plechovek |
   | 70101 | WHITE | 12 plechovek |

   Vyberte akci **Vydat**.

   Dodávky zboží od dodavatelů 10000 a 20000 dorazily do skladu WHITE a Sammy začíná zpracovávat nákupní příjemku.

## Příjem zboží
Na stránce **Příjemka na sklad** můžete spravovat více vstupních objednávek pro zdrojové doklady, například nákupní objednávku.

### Příjem zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Příjemky na sklad** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Do pole **Kód lokace** zadejte WHITE.
4. Vyberte akci **Použít filtry pro kopii pův. dokl.**.
5. Do pole **Kód** zadejte **PŘÍSLUŠENSTVÍ**.
6. Do pole **Popis** zadejte **Dodavatelé 10000 a 20000**.
7. Vyberte akci **Změnit**.
8. Na záložce **Nákup** v poli **Filtr čísla  dodavatele** zadejte **10000&#124;20000**.
9. Vyberte akci **Start**. Příjemka na sklad je vyplněna čtyřmi řádky představujícími řádky objednávek pro určené dodavatele. Pole **K  příjmu** je vyplněno, protože jste nezašktli políčko **Nevyplňovat množ. ke zprac.** na stránce **Výběr filtru původu skladu**.
10. Volitelně pokud chcete použít filtr, jak je popsáno výše v této části, zvolte akci **Kopie původ.dokladu** a pak vyberte nákupní objednávky od dotyčných dodavatelů.
11. Vyberte akci **Účtovat příjem** a poté zvolte tlačítko **Ano**.

   Vytvoří se kladní položky zboží odrážející účtované příjmy z příslušenství od prodejců 10000 a 20000 a toto zboží je připraveno k uložení do skladu z přijímací přihrádky.

## Zaskladnění zboží
Na stránce **Zaskladnění** můžete spravovat zaskladnění pro konkrétní příjemku skladu, která zahrnuje více původních dokladů. Stejně jako všechny doklady aktivity skladu je každé zboží na zaskladnění reprezentováno řádkem Vzít a Vložit. V následujícím postupu je kód přihrádky na řádcích Vzít nastaven na výchozí přijímací přihrádku lokace WHITE, W-08-0001.

### Zaskladnění zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaskladnění** a poté vyberte související odkaz.
2. Vyberte v seznamu jediný doklad zaskladnění skladu a pak zvolte akci **Upravit**.

   Doklad zaskladnění skladu se otevře s celkem osmi řádky Vzít nebo Vložit pro čtyři řádky nákupní objednávky.

   Pracovníkovi skladu je řečeno, že v montážním oddělení je zapotřebí 40 závěsů, a pokračuje v dělení jedného řádku Vložit, aby určil druhý řádek Vložit pro přihrádku W-02-0001 v oddělení montáže, kde umístí tuto část přijatých závěsů.

3. Vyberte druhý řádek Vložit na stránce **Zaskladnění** pro zboží 70200.
4. Do pole **Mn.  ke zprac.** změňte hodnotu ze 100 na 60.
5. Na záložce **Řádky** zvolte **Funkce** a poté zvolte **Rozdělit řádek**. Pro položku 70200 se vloží nový řádek s hodnotou 40 v poli **Množ. ke zprac.**.
6. Do pole **Kód přihrádky** zadejte W-02-0001. Pole **Kód zóny** je automaticky vyplněno.

   Pokračujte v zápisu zaskladnění.

7. Vyberte akci **Zápis zaskladnění** a pak zvolte tlačítko **Ano**.

   Přijaté příslušenství je nyní zaskladněno do výchozích přihrádek a 40 závěsů je umístěno v oddělení montáže. Přijaté zboží je nyní k dispozici k vyzvednutí na interní poptávku, jako jsou montážní objednávky, nebo na externí poptávku, jako jsou například prodejní dodávky.

## Viz také
[Zaskladnění zboží pomocí skladového zaskladnění](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)  
[Přesouvání zboží v rozšířených konfiguracích skladu](warehouse-how-to-move-items-in-advanced-warehousing.md)  
[Detaily návrhu: Vstupní procesy skladu](design-details-inbound-warehouse-flow.md)  
[Návod: Příjem a zaskladnění v základních konfiguracích skladu](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)  
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)
