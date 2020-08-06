---
    title: How to Plan Warehouse Movements in Worksheets | Microsoft Docs
    description: Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.
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
# Plánování skladových přesunů v sešitech
Pokud chcete přesuny vytvořit jako pokyny pro přesun, můžete je plánovat v sešitu pomocí funkce doplnění přihrádky nebo ručního plánování řádků.

## Výpočet pohybu doplnění
Při dodávce zboží ze skladu zákazníkům obsahují přihrádky s nejvyšším pořadím stále méně zboží. Chcete-li vyplnit tyto vysoce postavené přihrádky vyskladnění zbožím z jiných přihrádek, spusťte funkci **Vypočítat doplnění přihrádky** na stránce **Sešit přesunu**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit přesunu** a poté vyberte související odkaz.
2. Vyberte akci **Vypočítat doplnění přihrádky**.

   [!INCLUDE[d365fin](includes/d365fin_md.md)] vytvoří řádky, které přesně označují, jak byste měli přesunout zboží z přihrádek s nízkým pořadím do přihrádek s vyšším pořadím.

   > [!NOTE]
   > Pohyb je navržen podle FEFO, když aktivujete funkci **Vytvořit přesun**, pokud jsou pro zboží splněny následující podmínky:
   > - Zboží má datum vypršení platnosti.
   > - Na kartě lokace je zaškrtnuto políčko **Vybrat na základě metody FEFO**.
   - Na kartě lokace je zaškrtnuto políčko **Přihrádka nutná**.
   - Pole **Ze zóny** a **Z přihrádky** jsou prázdná.


   Pro více informací navštivte [Vyskladnění podle FEFO](warehouse-picking-by-fefo.md).

3. Prohlédněte si řádky a v případě potřeby je změňte nebo některé z nich odstraňte, pokud není dostatek času na jejich provedení.
4. Vyberte akci **Vytvořit přesun**, chcete-li vytvořit pokyn skladu pro zaměstnance.

## Přesunutí celého obsahu jedné nebo více přihrádek pomocí funkce Načíst obsah přihrádky
Sešit přesunu můžete také použít k plánování dalšího pohybu zásob ve skladu. Pokud například chcete umístit zboží do přihrádky pro kontrolu kvality, můžete pomocí sešitu přesunu naplánovat tuto akci a potom vytvořit pohyb, který vytvoří pokyny pro zaměstnance.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit přesunu** a poté vyberte související odkaz.
2. Vyberte akci **Načíst obsah přihrádky**. Stránka požadavku slouží k filtrování přihrádek a zboží, které se mají zobrazit na řádcích sešitu přesunu.
3. Vyplňte příslušná pole na stránce žádosti o dávkovou úlohu. Chcete-li například zobrazit obsah všech přihrádek v určité zóně v lokaci, vyplňte pole **Kód zóny**. Pokud chcete načíst řádky pro každou přihrádku, která obsahuje určité zboží, vyplňte pole **Číslo zboží**.

   > [!NOTE]
Zboží, které je v přihrádke typu Příjem, nelze ručně přesunout do nebo z přihrádky typu Příjem, protože zboží, které je v přihrádke typu Příjem, musí být zaregistrováno jako zaskladněné, než jsou součástí dostupných zásob.

4. Pokud načítáte mnoho řádků, zvolte **Seřadit**, chcete-li určit pořadí, v jakém se řádky zobrazí v sešitu, a pak zvolte tlačítko **OK**.

   > [!NOTE]
Po aktivaci funkce **Načíst obsah přihrádky** jsou řádky načteny podle FEFO, pokud jsou u zboží splněny následující podmínky:
   - Zboží má datum vypršení platnosti.
   - Na kartě lokace je zaškrtnuto políčko **Vybrat na základě metody FEFO**.
   - Na kartě lokace je zaškrtnuto políčko **Přihrádka nutná**.
   - Pole **Ze zóny** a **Z přihrádky** jsou prázdná.


5. Dokončete některé načtené řádky tak, aby odrážely změny, které chcete provést. Pro každé zboží, které chcete přesunout, je nutné vyplnit pole **Číslo zboží**, **Z kódu přihrádky**, **Do kódu přihrádky** a **Množství**.
6. Odstraňte neúplné řádky, které jste použili pro informace.
7. Jakmile řádky sešitu přesunu přesně odrážejí, jak má zaměstnanec skladu provádět akci přesunu, zvolte akci **Vytvořit přesun** a vytvořte pokyny pro zaměstnance.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
