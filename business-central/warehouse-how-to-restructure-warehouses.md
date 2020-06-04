---
    title: How to Restructure Warehouses | Microsoft Docs
    description: You may want to restructure your warehouse with new bin codes and new bin characteristics.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2019
    ms.author: sgroespe

---
# Restrukturalizace skladů
Je možné, že budete chtít změnit strukturu skladu s novými kódy přihrádek a s vlastnostmi nových přihrádek. Tento druh aktivity nebudete provádět příliš často, ale situace může nastat, pokud je přeřazení nezbytné k dosažení nebo udržení účinnějšího provozu. Například:

- Je možné, že budete chtít přepnout kódy přihrádek, které podporují automatické zachycení dat, například pomocí ručních zařízení.
- Ve skladu může být zakoupen nový stojanový systém, který dává nové možnosti v skladování zboží.
- Společnost mohla změnit svůj sortiment zboží a přesunout sklad do nového fyzického umístění, aby se přizpůsobila této změně.

Pokud je sklad nastaven na používání přihrádek, ale nikoli na řízené zaskladnění a vyskladnění, proveďte restrukturalizaci skladu vytvořením nových přihrádek, které chcete v budoucnosti použít.

## Restrukturalizace skladu, který používá pouze přihrádky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. V záložce **Sklad**, nastavte pole **Volba výchozí přihrádky** na **Poslední použitá přihrádka**. 
3. Přesuňte veškerý obsah aktuálních přihrádek do nových přihrádek, které jste právě vytvořili.

   1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník přeřazení zboží** a poté vyberte související odkaz.
   2. Vyberte řádek deníku a pak zvolte akci **Načíst obsah přihrádky** .
   3. V záložce **Obsah přihrádky**, nastavte filtr **Kód lokace**, **Kód přihrádky** a **Číslo zboží** pro specifikaci obsahu, který chcete přemístit.
   4. Klikněte na tlačítko **OK** k naplnění řádku deníku.
   5. V poli **Nový kód přihrádky**, vyberte přihrádku, do které by se mělo zboží přemístit.
   6. Opakujte kroky b až e pro veškerý obsah přihrádky, který chcete přesunout.
   7. Vyberte tlačítko **Účtovat**.

Nyní jste vyprázdnili přihrádky, ve kterých se zboží používá. Výchozí přihrádky pro vaše položky byly nyní změněny na nové přihrádky.

## Restrukturalizace pokročilého skladu, který používá řízené zaskladnění a vyskladnění,

1. Vytvořte nové přihrádky, které chcete v budoucnosti použít. Pro více informací navštivte [Vytvoření přihrádek](warehouse-how-to-create-individual-bins.md).
2. Přesuňte veškerý obsah aktuálních přihrádek do nových přihrádek, které jste právě vytvořili.

   1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník přeřazení skladu** a poté vyberte související odkaz.
   2. Pro přihrádky, ve kterých se není žádný skutečný pohyb zboží, vytvořte řádek pro každou z aktuálních přihrádek v **Deníku přeřazení skladu**. Starý kód přihrádky do **Z kódu přihrádky** a nový kód přihrádky do **Do kódu přihrádky** .
   3. Pokud některé pohyby zahrnují skutečné fyzické pohyby, které mají zaměstnanci provádět, použijte **Sešity přesunu** k přípravě pokynů k pohybu namísto použití deníku přeřazení skladu. Pro více informací navštivte [Přesouvání zboží v rozšířených konfiguracích skladu](warehouse-how-to-move-items-in-advanced-warehousing.md).

3. Když jsou staré přihrádky vyprázdněny, přeřaďte je jako přihrádku typu **KVAL**, aby se zajistilo, že nebudou zahrnuty do toků zboží.

   1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
   2. Vyberte řádek s lokací a pak zvolte tlačítko **Přihrádky**.
   3. Na stránce **Přihrádky** zadejte do pole **Kód typu přihrádky** vložte **KVAL** pro každou starou přihrádku, kterou jste vyprázdnili v kroku 3 v předchozím postupu.

Nyní jste odstranili přihrádky z toku skladu a překlasifikovali je jako přihrádky KVAL (bez typu). Přihrádky KVAL nemají žádné pole aktivity na stránce **Typy přihrádek** , a proto nejsou považovány za tok zboží. Pro více informací navštivte [Nastavení přihrádek](warehouse-how-to-set-up-bin-types.md).

## Odstranění přihrádky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Vyberte lokaci, kde chcete odstranit přihrádky. Vyberte tlačítko **Přihrádky**.
3. Vyberte řádky pro přihrádky, které chcete odstranit.
4. Vyberte tlačítko **Odstranit**.

Pokud zvolíte tlačítko **Ano**, přihrádka bude odstraněna pro budoucí použití, ale kód přihrádky ve všech položkách skladu zůstane stejný.

Pokud chcete přejmenovat přihrádku tak, aby byly také přejmenovány všechny záznamy spojené s přihrádkou, včetně obsahu přihrádky, řádků aktivit skladu, evidovaných řádků aktivit skladu, řádků sešitu skladu, řádků příjemky na sklad, zaúčtovaných řádků příjemky na sklad, řádků dodávky ze skladu, zaúčtovaných řádků dodávky ze skladu a položek skladu, můžete tak učinit na stránce **Přihrádky**.

## Přejmenování přihrádky a změna kódu přihrádky ve všech záznamech

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Vyberte lokaci, kde chcete přejmenovat přihrádku nebo změnit kód přihrádky, a pak zvolte tlačítko **Přihrádky**.
3. Vyberte přihrádku, kterou chcete změnit, a do pole **Kód** zadejte nový kód přihrádky.
4. Klikněte na tlačítko **Ano**.

> [!NOTE]
> Pokud zvolíte **Ano** a existuje mnoho položek týkajících se této přihrádky, například proto, že jste po určitou dobu neodstranili doklady skladu, může nějakou dobu trvat než program přejmenuje všechny záznamy. Pokud tedy použijete tuto metodu, zvažte spuštění dávkové úlohy **Odstranit zapsané doklady  skladu** před začátkem procesu přejmenování. Všimněte si také, že jedinými dokumenty, které jsou v této dávkové úloze odstraněny, jsou zaskladnění, vyskladnění a přesuny.
> Pokud přejmenujete přijímací přihrádku nebo dodací přihrádku, budou všechny zaúčtované příjemky nebo dodávky, které se vztahují k dané přihrádce, přejmenovány.
> 
## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
