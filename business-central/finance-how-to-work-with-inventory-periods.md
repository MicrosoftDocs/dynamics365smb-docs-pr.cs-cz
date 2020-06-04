---
    title: How to Work with Inventory Periods | Microsoft Docs
    description: You can control the timeframe in which people can post post changes to inventory by defining inventory periods.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: inventory, periods
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Práce s obdobím zásob
Období zásob definuje časové období, ve kterém můžete zaúčtovat změny v zásobách. Období zásob je definováno koncovým datem. Když uzavřete období zásob, nemůžete před tímto datem ukončení zaúčtovat žádné změny zásob, očekávané ani fakturované. Nemůžete zaúčtovat žádné nové hodnoty do zásob před datem ukončení. Pokud máte otevřené položky zboží v uzavřeném období, což znamená kladná množství, která ještě nebyla vyrovnána s výstupními transakcemi, můžete pro tyto položky vyrovnat výstupní množství, a to i v případě, že je období uzavřeno.

Následující části popisují, jak:

* Vytvořit období zásob.
* Uzavřít období zásob.
* Znovu otevřít období zásob.

## Vytvoření období zásob
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Období zásob** a poté vyberte související odkaz.
2. Vytvořte nový řádek.
3. Do pole **Koncové datum** zadejte poslední datum v období zásob, které chcete definovat. Po uzavření období nebudete moci zaúčtovat změny zásob před tímto datem.
4. Do pole **Název** zadejte popisný název. Vyberte tlačítko **OK**.

## Uzavření období zásob
Pole **Uzavřeno** označuje, zda je období zásob uzavřeno pro změny hodnot zásob. Toto pole nelze upravit.

Můžete uzavřít libovolné období zásob za předpokladu, že platí následující:

* V tomto období neexistují žádné otevřené odchozí položky zboží, což znamená záporný sklad.
* Cena všech položek byla upravena pomocí dávkové úlohy **Adjustace nákladů položek zboží**.

To znamená, že všechna množství odchozích transakcí, například množství z prodejních objednávek, odchozích převodů, prodejních faktur, nákupních vratek nebo nákupních dobropisů, musí být použita na existující množství ve skladu.

### Uzavření období skladu
1. Před uzavřením období skladu vyberte akci **Adjustace nákladů položek zboží** abyste zajistili, že budou zaúčtovány všechny úpravy nákladů.

   Spusťte sestavu **Uzavření období zásob - test** a zjistěte, zda existují nějaké otevřené vyrovnávací položky v období zásob nebo položky, jejichž náklady ještě nebyly upraveny.
2. Vyberte akci **Uzavření období zásob - test**.

   Spusťte dávkovou úlohu **Účtování nákladů na zboží** a zajistěte, aby byly všechny náklady zaúčtovány do hlavní knihy.
3. Vyberte akci **Zaúčtovat fakturu**.
4. Na stránce **Období zásob** vyberte období zásob, které chcete zavřít.
5. Vyberte akci **Uzavřít období**. Po uzavření období zásob nemůžete zaúčtovat změny zásob před datem ukončení. Než zavřete období zásob, náklady na všechny položky musí být upraveny dávkovou úlohou **Adjustace nákladů položek zboží**.
6. Stisknutím tlačítka **Ano** potvrďte, že chcete období uzavřít, nebo volbou **Ne** uzavření zrušte.
7. Období zásob je uzavřeno a po dokončení se zobrazí potvrzovací zpráva.

## Znovuotevření období zásob
Po uzavření období zásob nelze toto období odstranit. Můžete ji však znovu otevřít, pokud chcete povolit zaúčtování před koncovým datem období zásob. Znovuotevření období také znovu otevře všechna období zásob s konečnými daty později než znovuotevřené období.

### Opětovné otevření období zásob
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Období zásob** a poté vyberte související odkaz.
2. Vyberte období zásob, které chcete znovu otevřít.
3. Vyberte akci **Znovu otevřít období**. Potvrďte, že chcete období znovu otevřít.
4. Znovu se otevřou všechna období zásob s konečnými daty později než vybrané období.

## Viz také
[Detaily návrhu: Období zásob](design-details-inventory-periods.md)  
[Finance](finance.md)  
[Zásoby](inventory-manage-inventory.md)  
[Práce s financemi](ui-work-product.md)
