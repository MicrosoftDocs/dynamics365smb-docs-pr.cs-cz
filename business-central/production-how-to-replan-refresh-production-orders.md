---
    title: How to Replan or Refresh Production Orders Directly| Microsoft Docs
    description: The production order lines contain the items that are to be produced in the production order.
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
# Přeplánování nebo přímá aktualizace výrobních zakázek
Funkce **Přeplánování** na výrobních zakázkách se obvykle používá poté, co jste přidali nebo změnili komponenty, které tvoří základní výrobní zakázky. Funkce vypočítá změny provedené u součástí a řádků technologického postupu a zahrnuje zboží na nižších úrovních výrobního kusovníku, pro které může generovat nové výrobní zakázky.

Na základě změn provedených v součástech a řádcích technologického postupu, funkce přeplánování vypočítá a naplánuje novou poptávku pro výrobní zakázku.

Funkce **Aktualizovat** na výrobních zakázkách se obvykle používá po provedení jedné z následujících akcí:

- Ručním vytvořením hlavičky výrobní zakázky pro první výpočet a vytvoření dat řádku.
- Provedením změn v záhlaví výrobní zakázky, aby se přepočítaly všechna data linky.

Funkce Aktualizovat vypočítá změny provedené v hlavičce výrobní zakázky a nezahrnuje úrovně výrobního kusovníku. Funkce vypočítá a iniciuje hodnoty řádků komponenty a řádků postupu na základě hlavních dat definovaných v přiřazeném výrobním kusovníku a postupu podle množství objednávky a data splatnosti v hlavičce výrobní zakázky.

Řádky výrobní zakázky můžete vložit buď ručně, nebo použít funkci, která vypočítá řádky výrobní zakázky z hlavičky.

> [!NOTE]
> Použijete-li funkci aktualizovat pro přepočet řádků výrobních zakázek, staré výrobní řádky se odstraní a vypočtou se nové řádky.

## Přeplánování výrobní zakázky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pevně plánovaná výr. zakázka** a poté vyberte související odkaz.
2. Otevřete výrobní zakázku, kterou chcete přeplánovat.
3. Na záložce s náhledem **Řádky**, zvolte akci **Řádky**, a potom vyberte akci **Komponenty**.
4. Pro přidání součásti, která je vyrobenou položkou nebo podsestavou.
5. Z výrobní zakázky zvolte akci **Přeplánovat**.

   Na stránce **Přeplánovat výrobní zakázku**, pokračujte v definování jak a co znovu naplánovat.
6. V poli **Způsob plánování**, vyberte jednu z následujících možností.

   | Možnost | Popis |
   |----------------------------------|---------------------------------------|  
   | **Zpět** | Vypočítá posloupnost operací zpět od nejbližšího možného data ukončení, definovaného podle data splatnosti a / nebo jiných naplánovaných příkazů, do posledního možného data zahájení. **Poznámka:**  Tato výchozí možnost je relevantní ve většině situací. |
   | **Vpřed** | Vypočítá posloupnost operací vpřed od nejbližšího možného data ukončení, definovaného podle data splatnosti a / nebo jiných naplánovaných příkazů, do posledního možného data zahájení. **Poznámka:**  Tato možnost je relevantní pouze pro urychlené zpracování objednávky. |

7. V poli **Plán** vyberte, zda se mají vypočítat výrobní požadavky na vyráběné položky na kusovníku produkce následujícím způsobem.

   | Možnost | Popis |
   |----------------------------------|---------------------------------------|  
   | **Bez úrovní** | Nezvažujete výrobu nižší úrovně. Tím se aktualizuje pouze plán zboží, například aktualizace. |
   | **Jedna úroveň** | Plánování poptávky po produkci první úrovně. Mohou být vytvořeny výrobní zakázky první úrovně. |
   | **Všechny úrovně** | Plán pro všechny úrovně výrobní poptávky. Mohou být vytvořeny výrobní zakázky všech úrovní. |

8. Vyberte **Jedna úroveň**, a zvolte tlačítko **OK** chcete-li znovu naplánovat výrobní zakázku, vypočítat a vytvořit novou základní výrobní zakázku pro zavedenou podsestavu, pokud není plně k dispozici.

> [!NOTE]
> Změny implementované pomocí funkce **Přeplánovat** s velkou pravděpodobností změní potřebu kapacity výrobní zakázky, a proto bude pravděpodobně nutné operace později přeřadit.

## Aktualizace výrobní zakázky
Pokud jste změnili řádky výrobní zakázky, komponenty nebo řádky TNG postupu, musíte také aktualizovat informace o výrobní zakázce. V následujícím postupu se komponenty počítají pro pevně plánovanou výrobní zakázku. Kroky jsou podobné pro řádky TNG postupu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pevně plánovaná výr. zakázka** a poté vyberte související odkaz.
2. Zvolte akci **Nový**. Pro více informací navštivte [Vytvoření montážní zakázky](production-how-to-create-production-orders.md).
3. Vyberte akci **Aktualizovat**.
4. Na stránce **Aktualizace výrobní zakázky**, vyberte jednu z následujících možností::

   | Možnost | Popis |
   |----------------------------------|---------------|---------------------------------------|  
   | **Směr plánování** | **Vpřed** | Plánování začíná od data zahájení a pokračuje dopředu k datu ukončení. Chcete-li použít tuto možnost, musíte vyplnit počáteční datum. |
   |  | **Zpět** | Plánování začíná od data ukončení a pokračuje zpět k počátečnímu datu. |
   | **Vypočítat** | **Řádky** | Toto pole vyberte, chcete-li vypočítat řádky výrobní zakázky. |
   |  | **TNG postupy** | Toto pole nemá žádný vliv na výpočet výrobních řádků. |
   |  | **Potřebné komponenty** | Toto pole nemá žádný vliv na výpočet výrobních řádků. |
   | **Sklad** | **Vytvořit vstupní požadavek** | Toto pole nemá žádný vliv na výpočet výrobních řádků. |

5. Zvolte tlačítko **OK** pro potvrzení vašeho výběru. Nyní se vypočítají řádky výrobní linky.

> [!NOTE]
> Vypočtením komponent výrobní zakázky se odstraní předchozí změny v komponentách.

## Viz také
[Plánování](production-planning.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)  
[Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
