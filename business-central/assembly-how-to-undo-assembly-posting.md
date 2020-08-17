---
    title: How to Undo Assembly Posting | Microsoft Docs
    description: Sometimes you may need to undo a posted assembly order, for example when the order was posted with mistakes that must be corrected, or because it should not have been posted in the first place and must be rolled back.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: kit, kitting
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Zrušení účtování montáže
Někdy může být nutné vrátit zpět zaúčtované montážní zakázky, například když byla zakázka zaúčtována s chybami, které musí být opraveny, nebo protože neměla být zaúčtována na prvním místě a musí být vrácena zpět.

Když zrušíte zaúčtovanou montážní zakázku, vytvoří se sada opravných položek zboží pro stornování původních položek. Každá kladná výstupní položka pro zboží montáže je stornována zápornou výstupní položkou. Každá záporná položka spotřeby pro komponentu montáže je stornována kladnou položkou spotřeby. Pevné vyrovnání nákladů je automaticky vytvořeno mezi opravnými a původními položkami k zajištění stornování přesných nákladů.

Když vrátíte zpět plně zaúčtovanou montážní zakázku, můžete ji znovu vytvořit v původním stavu, například provést opravy před jejím opětovným zaúčtováním. Alternativně se můžete rozhodnout, že montážní zakázku znovu nevytvoříte.

Pokud zrušíte částečně zaúčtovanou montážní zakázku, budou všechna ovlivněná pole množství, například **Smontované možství**, **Spotřebované množství** a **Zbývající množství** obnoveny na hodnoty, které měli před dotyčným účtováním.

Chcete-li znovu vytvořit nebo obnovit montážní zakázku, musí být pro zboží montáže, které bylo výstupem v původním účtování, splněny následující podmínky:

- Musí být stále ve skladu, to znamená, že není prodáno nebo jinak spotřebováno pomocí odchozích transakcí.
- Nesmí být rezervováno.
- Musí existovat v přihrádce, do které bylo odesláno.

Kromě toho lze stávající příkazy sestavení obnovit pouze tehdy, pokud se nezmění počet řádků a pořadí řádků v původní montážní zakázce.

> [!TIP]
> Chcete-li vyřešit konflikty způsobené změnami řádků, můžete ručně zrušit změny na dotyčných řádcích před zrušením související zaúčtované montážní zakázky. Případně můžete montážní zakázku zaúčtovat v plném rozsahu a poté vybrat opětovné vytvoření při jejím zrušení.

Následující postup popisuje, jak zrušit zaúčtované montážní zakázky, kde bylo zboží sestaveno do skladu. Pokud chcete vrátit zpět zaúčtované montážní zakázky, kde bylo zboží sestaveno do prodejní objednávky, musíte použít funkci **Vrátit dodávku** na zaúčtované dodávce, která se vztahuje k zaúčtované montážní zakázkce. Pro více informací navštivte [Stornování účtování a vrácení příjemky/dodávky](finance-how-reverse-journal-posting.md). Zrušení zaúčtované montážní zakázky se pak stane automaticky stejným způsobem, jak je popsáno v tomto tématu.

## Zrušení zaúčtování montážní zakázky
1. Chcete-li vrátit zpět zcela nebo částečně zaúčtované montážní zakázky, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované montážní zakázky** a poté vyberte související odkaz.

   Otevře se stránka **Účtované montážní zakázky** která zobrazuje jednu nebo více zaúčtovaných montážních zakázek, které jsou zaúčtovány z příslušné montážní zakázky. Každé dílčí účtování vytvoří samostatnou zaúčtovanou montážní zakázku.
2. Otevřete zaúčtovanou montážní zakázku, kterou chcete vrátit zpět, a poté vyberte akci **Zrušit montáž**.

   Pokud zaúčtovaná montážní zakázka, kterou chcete vrátit zpět, souvisí s plně zaúčtovanou zakázkou, která je nyní odstraněna, máte možnost ji znovu vytvořit, obvykle proto, že ji chcete znovu zpracovat.
3. Pokud chcete znovu vytvořit montážní zakázku, zvolte tlačítko **Ano**. Chcete-li zrušit zaúčtování bez opětovného vytvoření související zakázky, zvolte tlačítko **Ne**.

Pole **Stornováno** v záhlaví omontážní zakázky se změní na **Ano**. Zaúčtování montážní zakázky je nyní stornováno a vy můžete pokračovat ve zpracování celé montážní zakázky, pokud jste se ji rozhodli znovu vytvořit nebo spracovat otevřenou montážní zakázku, kterou jste obnovili do původního stavu.

> [!NOTE]
> Chcete-li obnovit množství z více dílčích účtování v montážní zakázce, musíte zrušit všechny dotyčné zaúčtované montážní zakázky podle kroků 1 až 3 výše pro každou zaúčtovanou montážní zakázku.

## Viz také
[Správa montáže](assembly-assemble-items.md)  
[Stornování účtování a vrácení příjemky/dodávky](finance-how-reverse-journal-posting.md)  
[Zpracování prodejní vratky nebo stornování](sales-how-process-sales-returns-cancellations.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
