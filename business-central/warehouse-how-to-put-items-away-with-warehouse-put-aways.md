---
    title: How to Put Items Away with Warehouse Put-aways | Microsoft Docs
    description: When your location is set up to require warehouse put-away processing and warehouse receive processing, you use the warehouse put-away documents function to control the putting away of items.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Zaskladnění zboží pomocí skladového zaskladnění
Pokud je lokace nastavena tak, aby vyžadovala zpracování zaskladnění a zpracování příjmů na sklad, použijete funkci dokladů zaskladnění k řízení zaskladnění zboží.

Když zaúčtujete příjemku na sklad, aktualizují se původní doklady, jako je nákup, vstup transferu nebo objednávky prodejní vratky, přijaté množství se zaúčtuje do položek zboží a řádky o přijatém zboží se odešlou pomocí funkce zaskladnění do skladu. Pokud máte interní zaskladnění a vyskladnění, pak může vnitřní zaskladnění také vytvořit řádky pro zaskladnění.

V závislosti na nastavení skladu jsou řádky buď zpřístupněny listu zaskladnění, nebo jsou použity k okamžitému vygenerování pokynů k zaskladnění. Pro více informací navštivte [Plánování v sešitech zaskladění](warehouse-how-to-plan-put-aways-in-worksheets.md).

Kromě standardních způsobů vytváření zaskladnění skladů, které jsou popsány v tomto tématu, můžete vytvořit zaskladnění z příslušné zaúčtované příjemky na sklad. To je užitečné, pokud jste odstranili řádky zaskladnění nebo pokud používáte řízené zaskladnění a vyskladnění a rozhodli jste se nepoužívat list zaskladnění, protože můžete vytvořit nebo znovu vytvořit pokyny k zaskladnění ze zaúčtovaných řádků příjemky.

## Zaskladnění zboží bez řízeného zaskladnění a vyskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaskladnění** a poté vyberte související odkaz.
2. Otevřete zaskladnění skladu, které je připravené k zpracování.

   Řádky zaskladnění můžete seřadit podle různých kritérií, například podle zboží, čísla police nebo data splatnosti, a optimalizovat tak proces zaskladnění.
3. Na každém řádku v poli **Množ. ke zprac.** zadejte množství, které chcete zaskladnit.
4. Po dokončení zaskladnení zboží vyberte akci **Zápis zaskladnění**, která zaznamená dokončení aktivity a zpřístupní zboží k vyskladnění.

## Zaskladnění zboží pomocí řízeného zaskladnění a vyskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zaskladnění** a poté vyberte související odkaz.
   Pokud byly vytvořeny pokyny k vyskladnění, je viditelné vyskladnění skladu.
2. Otevřete zaskladněný sklad, se kterým chcete pracovat.
3. Pokud to váš sklad vyžaduje, zadejte své uživatelské ID na záložce **Obecné**, když začnete pracovat na konkrétním zaskladňování.
4. Proveďte akce Vzít a Vložit uvedené v poli **Typ akce** na řádcích.

   Všimněte si, že každý řádek příjmu se stal nejméně dvěma řádky ve skladu:

   - První řádek s hodnotou **Vzít** v poli **Typ akce** označuje, kde je zboží umístěno v přijímací oblasti. Na tomto řádku nemůžete změnit zónu a pole přihrádky.
   - Další řádek s hodnotou **Vložit** v poli **Typ akce** ukazuje, kam je nutné umístit zboží do skladu. Pokud sklad obdržel velký počet zboží na jednom řádku příjemky, může se stát, že bude muset být zaskladněno v několika přihrádkách, takže pro každou přihrádku bude existovat řádek Vložit.

      Pokud řádky Vzít a Vložit pro každý řádek příjemky na sebe bezprostředně nenasledují a chcete, aby to tak bylo, můžete řádky seřadit výběrem hodnoty **Zboží** v poli **Způsob třídění** na záložce **Obecné**.

      Pokud fyzické rozložení skladu odráží pořadí přihrádek, můžete použít metodu třídění **Pořadí přihrádky** k přípravě kola zaskladnění, které minimalizuje vaše kroky ve skladu.

5. Pokud jste umístili všechny položky do přihrádek podle pokynů, zvolte akci **Zápis zaskladnění**.

V lokacích, které jsou nastavené na použití směrovaného zaskladnění a vyskladnění, jsou pro výše uvedený postup nezbytná následující nastavení:

- Nastavení šablony zaskladnění. Pro více informací navštivte [Nastavení šablon zaskladnění](warehouse-how-to-set-up-put-away-templates.md).
- Je definována hmotnost, objem a zvláštní požadavky na skladování zboží nebo skladové jednotky. Pro více informací navštivte Hrubá hmotnost.
- Kapacita, typ přihrádky a pořadí přihrádek. Pro více informací navštivte Pořadí přihrádky.

Pořadí přihrádky se zohlední, pokud více než jedna přihrádka odpovídá kritériím šablony zaskladnění. Pokud jsou kritéria šablony zaskladnění i pořadí přihrádky stejné pro více než jednu přihrádku, je vybrána přihrádka s nejvyšším číslem.

## Vytvoření zaskladnění ze zaúčtované příjemky
Pokud vaše lokace používá zpracování zaskladnění i zpracování příjmu a odstranili jste řádky zaskladnění nebo pokud používáte řízené zaskladnění a vyskladnění a rozhodli jste se nepoužívat list zaskladnění, můžete vytvořit nebo znovu vytvořit pokyny pro zaskladnění pro zaúčtované řádky příjemky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované příjemky  na sklad** a poté vyberte související odkaz.
2. Vyberte zaúčtovanou příjemku, kterou bude pravděpodobně třeba zaskladnit.
3. Vyberte akci **Carta**.

   Pokud je pole **Stav dokladu** prázdné, příjemka nebyla vůbec zaskladněna. Jinak pole označuje, že účtenka je částečně nebo zcela zaskladněna.

4. Pokud je příjemka částečně zaskladněná nebo není zaskladněná vůbec, zvolte akci **Vytvořit vyskladnění**.
5. Vyplňte stránku žádosti o dávkovou úlohu a vytvořte zaskladnění a pak zvolte tlačítko **OK**.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)    
[Zásoby](inventory-manage-inventory.md)    
[Nastavení správy skladu](warehouse-setup-warehouse.md)       
[Správa montáže](assembly-assemble-items.md)      
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]