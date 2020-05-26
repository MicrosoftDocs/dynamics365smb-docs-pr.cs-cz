---
title: Count Inventory With Document-Based Functionality| Microsoft Docs
description: Describes how to perform physical inventory counting using the Physical Order Inventory and Physical Inventory Recording pages.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, status, negative, positive, increase, decrease
ms.date: 04/01/2020
ms.author: sgroespe

---
# Výpočet zásob pomocí dokumentů
Fyzickou inventuru zboží můžete provést pomocí objednávky fyzické inventury a dokladů pro záznamenání fyzické inventury. Stránka **Objednávky fyzické inventury** se používá k uspořádání celého projektu inventury zásob, například podle dimenzí. Stránka **Záznam fyz. inventury** se používá ke komunikaci a zachycení skutečného počtu zboží. Můžete vytvořit více záznamů pro jednu objednávku, například distribuovat skupiny zboží různým zaměstnancům.

Sestavu **Záznam fyz. inventury** lze vytisknout z každého záznamu a obsahuje prázdná pole množství pro zadání počítaných zásob. Když uživatel provádí počítání a množství jsou zadána na stránce **Záznam fyz. inventury**, vyberete akci **Dokončit**. Tím se převedou množství na související řádky na stránce **Objednávky fyzické inventury**. Funkčnost zajišťuje, že počet zboží nelze zaznamenat dvakrát.

> [!NOTE]
> Tento postup popisuje, jak provést fyzickou inventuru pomocí dokladů, což je metoda, která poskytuje větší kontrolu a podporuje distribuci počítání více zaměstnancům. Úkol můžete také provést pomocí deníků na stránkách **Deníky  fyzické inventury** a **Deník  fyz. inventury skladu**. Pro více informací navštivte [Počet, úprava a překlasifikace zásob pomocí deníků](inventory-how-count-adjust-reclassify.md).<br /><br />
> Upozorňujeme, že pokud používáte funkci Přihrádky nebo Zóny, nemůžete použít objednávky fyzické inventury. Místo toho použijte stránku **Deník  fyz. inventury skladu** pro počítání zboží na skladě před jejich synchronizací s položkami zboží.

Počítání zásob pomocí dokladů se skládá z následujících kroků:

1. Vytvořte objednávku fyzické inventury s předvyplněným očekávaným množstvím zboží.
2. Z objednávky vygenerujte jeden nebo více záznamů fyzické inventury.
3. Zadejte počty kusů zboží do záznamů, jak jsou zachyceny například na výtiscích, a nastavte je na **Dokončeno**.
4. Dokončete a zaúčtujte fyzickou inventuru.

## Vytvoření objednávky fyzické inventury
Objednávka fyzické inventury je úplný doklad, který se skládá z hlavičky a některých řádků objednávky fyzické inventury. Informace v hlavičce fyzické inventury popisují, jak provést fyzickou inventuru. Řádky fyzické inventury obsahují informace o zboží a jejich lokacích.

Chcete-li vytvořit řádky objednávek fyzické inventury, použijte funkci **Vypočítat řádky** tak, aby odrážela aktuální zásoby jako řádky v objednávce. Alternativně můžete pomocí funkce **Kopírovat z dokladu** vyplnit řádky obsahem jiné otevřené nebo zaúčtované objednávky fyzické inventury. Následující postup popisuje, jak používat funkci **Vypočítat řádky**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Objednávky fyzické inventury** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Vyplňte povinná pole na záložce **Obecné**. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vyberte akci **Vypočítat řádky**.
5. Podle potřeby vyberte možnosti.
6. Nastavte například filtry, aby zahrnovaly pouze podmnožinu zboží, která se má počítat při prvním záznamu.

   > [!TIP]
   > Chcete-li naplánovat počítání inventury pro více zaměstnanců, je vhodné nastavit různé filtry pokaždé, když použijete akci **Vypočítat řádky**, aby se objednávka vyplnila pouze podmnožinou zboží inventury, které bude zaznamenávat jeden uživatel. Při generování více záznamů fyzické inventury pro více zaměstnanců minimalizujete riziko počítání stejného zboží dvakrát. Pro více informací navštivte sekci "Vytvoření záznamu fyzické inventury".

7. Vyberte tlačítko **OK**.

Řádek pro každé zboží, které existuje ve zvolené lokaci a podle nastavených filtrů a možností, je vložen do objednávky. U zboží, které jsou nastaveny pro sledování zboží, je zaškrtnuto políčko **Použít sledování zboží** a informace o očekávaném množství sériových čísel a čísel šarží jsou k dispozici výběrem akce **Řádky** a poté **Řádky sledování zboží**. Pro více informací navštivte sekci "Zpracování sledování zboží při počítání zásob".

Nyní můžete přistoupit k vytvoření jedné nebo více záznamů, což jsou pokyny pro zaměstnance, kteří provádějí skutečné počítání.

## Vytvoření záznamu fyzické inventury
Pro každou objednávku fyzické inventury můžete vytvořit jeden nebo více dokladů zaznamenávajících fyzickou inventuru, do kterých zaměstnanci zadávají počítaná množství, buď ručně, nebo pomocí integrovaného skenovacího zařízení.

Ve výchozím nastavení je záznam vytvořen pro všechny řádky v související objednávce fyzické inventury. Aby se předešlo tomu, že dva zaměstnanci počítají stejné zboží v případě distribuovaného počítání, je vhodné postupně vyplňovat pořadí fyzických zásob nastavením filtrů v dávkové úloze **Vypočítat řádky** (viz sekci "Vytvoření objednávky fyzické inventury") a poté vytvořit záznam fyzické inventury pomocí zaškrtnutí políčka **Pouze řádky, které nejsou v záznamech**. Toto nastavení zajišťuje, že každý nový záznam, který vytvoříte, obsahuje jiné zboží než to, které je na jiných záznamech.

V případě ručního počítání můžete vytisknout seznam pomocí sestavy **Záznam  fyz. inventury**, která má prázdný sloupec pro zápis spočítaného množství. Po dokončení počítání zadáte zaznamenaná množství do souvisejících řádků na stránce **Záznam  fyz. inventury**. Nakonec přenesete zaznamenaná množství do související objednávky fyzické inventury nastavením stavu na **Dokončeno**.

1. Na stránce **Objednávky fyzické inventury**, která obsahuje řádky pro zboží, které se mají spočítat v jednom záznamu, vyberte akci **Vytvořit nový záznam**.
2. Vyberte možnosti a podle potřeby nastavte filtry.
3. Vyberte tlačítko **OK**.

   Vytvoří se doklad záznamu fyzické inventury.

4. Pro každou sadu zboží, které se mají spočítat, je načtěte do příslušného pořadí fyzické inventury a opakujte kroky 1 až 3 se zaškrtnutým políčkem **Pouze řádky, které nejsou v záznamech**.

5. Vyberte akci **Záznamy** a otevřete stránku **Seznam  záznamů fyzické inventury**.
6. Otevřete příslušný záznam.
7. Na záložce **Obecné** vyplňte pole podle potřeby.
8. U zboží, které používají sledování zboží, vytvořte další řádek pro každé číslo šarže nebo kód sériového čísla výběrem akce **Funkce** a poté akce **Kopírovat řádek**. Pro více informací navštivte sekci "Zpracování sledování zboží při počítání zásob".
9. Vyberte akci **Tisk** a připravte fyzický doklad, který zaměstnanci použijí k zapsání započítaných množství.

## Dokončení záznamu fyzické inventury
Když zaměstnanci spočítají množství zásob, musíte se připravit na jejich zaznamenání do systému.

1. Ze stránky **Seznam  záznamů fyzické inventury** vyberte záznam fyzické inventury, který chcete dokončit, a poté vyberte akci **Upravit**.
2. Na záložce **Řádky** vyplňte skutečné počítané množství do pole **Množství** pro každý řádek.
3. U zboží se sériovým číslem nebo číslem šarže (je zaškrtnuto políčko **Použít sledování zboží**), zadejte započítaná množství na vyhrazených řádcích pro sériová čísla a čísla šarže. Pro více informací navštivte sekci "Zpracování sledování zboží při počítání zásob".
4. Zaškrtněte políčko **Zaznamenáno** na každém řádku.
5. Pokud jste zadali všechna data pro záznam fyzické inventury, vyberte akci **Dokončit**. Všimněte si, že na všech řádcích musí být zaškrtnuto políčko **Zaznamenáno**.

> [!NOTE]
> Po dokončení záznamu fyzické inventury se každý řádek převede na řádek v příslušném pořadí fyzické inventury, který se s ním přesně shoduje. Aby se shodovaly hodnoty v polích **Číslo zboží**, **Kód varianty**, **Kód lokace** a **Kód přihrádky** musí být stejné záznamy a řádky objednávky.<br /><br />
> Pokud neexistuje odpovídající řádek objednávky fyzické inventury a pokud je zaškrtnuto políčko **Povolit záznam bez objednávky** tak se automaticky vloží nový řádek a políčko **Zaznamenáno bez objednávky** je zaškrtnuto na příslušném řádku objednávky fyzické inventury. Jinak se zobrazí chybová zpráva a proces se zruší.<br /><br />
> Pokud se více řádků záznamu fyzické inventury shoduje s řádkem objednávky fyzické inventury, zobrazí se zpráva a proces se zruší. Pokud z nějakého důvodu dva identické řádky fyzické inventury skončí na objednávce fyzické inventury, můžete ji vyřešit pomocí funkce. Pro více informací navštivte sekci "Vyhledání duplicitních řádků objednávek fyzické inventury".

## Dokončení objednávky fyzické inventury
Po dokončení záznamu fyzické inventury je pole související s objednávkou fyzické inventury **Množství  záznamů (Základ)** aktualizováno spočítanými (zaznamenanými) hodnotami a políčko **Záznam** je zaškrtnuto. Pokud se počítaná hodnota liší od očekávané, pak se tento rozdíl zobrazí v poli **Pozitivní množství  (Základ)** a **Negativní množství  (Základ)** v uvedeném pořadí.

Chcete-li zobrazit očekávaná množství a jakékoli zaznamenané rozdíly pro zboží se sledováním zboží, vyberte akci **Řádky** a poté vyberte akci **Řádky sledování zboží** a vyberte různé pohledy pro sériová čísla a čísla šarží zapojených do počtu fyzických zásob.

Můžete si také vybrat akci **Rozdíl  objednávky fyzické inventury** pro zobrazení jakýchkoli rozdílů mezi očekávaným množstvím a počítaným množstvím.

### Vyhledání duplicitních řádků fyzické inventury

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Objednávky fyzické inventury** a poté vyberte související odkaz.
2. Otevřete fyzickou inventuru, pro kterou chcete zobrazit duplicitní řádky.
3. Vyberte akci **Zobrazit duplicitní řádky**.

Zobrazí se všechny duplicitní řádky fyzické inventury, takže je můžete odstranit a zachovat pouze jeden řádek s jedinečnou sadou hodnot v polích **Číslo zboží**, **Kód varianty**, **Kód lokace** a **Kód přihrádky**.

### Zaúčtování objednávky fyzické inventury
Po dokončení objednávky fyzické inventury a změně jejího stavu na **Dokončeno** ji můžete zaúčtovat. Stav objednávky fyzické inventury můžete nastavit na **Dokončeno**, pokud jsou splněny následující podmínky:

- Všechny související záznamy fyzické inventury mají stav **Dokončeno**.
- Každý řádek fyzické inventury byl spočítán alespoň jedním záznamovým řádkem zásob.
- Zaškrtávací políčka **V řádcích záznamu** a **Očekávané  vypočítané  množství** byla vybrána pro všechny řádky objednávek fyzické inventury.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Objednávky fyzické inventury** a poté vyberte související odkaz.
2. Vyberte fyzickou inventuru, kterou chcete dokončit, a pak zvolte akci **Upravit**.

   Na stránce **Objednávky fyzické inventury** zobrazíte množství zaznamenané v poli **Zaznamenané  množstvi (Základ)**.
3. Vyberte akci **Dokončit**.

   Hodnota v poli **Stav** se změní na **Dokončeno** a nyní můžete změnit pořadí pouze tak, že vyberete akci **Znovu otevřít**.
4. Chcete-li objednávku zaúčtovat, vyberte akci **Účtovat** a poté vyberte tlačítko **OK**.

Příslušné položky zboží jsou aktualizovány spolu se všemi souvisejícími položkami sledování zboží.

### Zobrazení zaúčtovaných objednávek fyzické inventury
Po zaúčtování bude objednávka fyzické inventury odstraněna a můžete zobrazit a vyhodnotit doklad jako zaúčtovinovou fyzickou inventuru včetně jejích záznamů fyzické inventury a všech provedených poznámek.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované objednávky  fyz. inventury** a poté vyberte související odkaz.
2. Na stránce **Účtované objednávky  fyz. inventury** vyberte objednávku zaúčtovaného inventáře, kterou chcete zobrazit, a poté vyberte akci **Zobrazit**.
3. Chcete-li zobrazit seznam souvisejících záznamů fyzické inventury, vyberte akci **Záznamy**.

## Zpracování sledování zboží při počítání zásob
Sledování zboží se týká sériových čísel nebo čísel šarží přiřazených danému zboží. Při počítání zboží, které je uloženo na skladě jako například 10 různých čísel šarží, musí být zaměstnanec schopen zaznamenat, které a kolik jednotek každého čísla šarže je na skladě. Pro více informací o funkcionalitě sledování zboží navštivte [Práce se sériovými čísly a čísly šarží](inventory-how-work-item-tracking.md).

Zaškrtávací políčko **Použít sledování zboží** na řádcích objednávky fyzické inventury je automaticky vybráno, pokud je pro zboží nastaven kód sledování zboží, ale můžete jej také vybrat nebo zrušit výběr ručně.

### Příklad - Připravte záznam fyzické inventury pro zboží - sledované zboží
Zvažte fyzickou inventuru pro položku A, která je uložena ve skladu jako deset různých sériových čísel.
1. Na řádku záznamu pro zboží zaškrtněte políčko **Použít sledování zboží**.
2. Vyberte pole **Sériové číslo** a poté vyberte první sériové číslo, které existuje v zásobách pro zboží a poté zvolte tlačítko **OK**.

   Pokračujte v kopírování řádku pro první sledované zboží a vložte další řádky odpovídající počtu sériových čísel uložených v zásobách.

3. Vyberte akci **Funkce** a potom akci **Kopírovat řádek**.
4. Na stránce **Kopírovat řádky záznamů  fyz.   inventury**, zadejte 9 do pole **Počet  kopií** a poté vyberte tlačítko **OK**.
5. Na prvním kopírovaném řádku vyberte pole **Sériové číslo** a vyberte další sériové číslo pro zboží.
6. Opakujte krok 5 pro zbývajících osm sériových čísel, přičemž dbejte na to, abyste nezvolili stejné číslo dvakrát.
7. Vyberte akci **Tisk** a připravte si výtisk, který zaměstnanci použijí k zapsání započítaného zboží a sériových čísel/čísel šarží.

Všimněte si, že sestava **Záznamy  fyz. inventury** obsahuje deset řádků pro položku A, jeden pro každé sériové číslo.

### Příklad - Zaznamenejte a odečtěte rozdíly v číslech šarží
Sledovaná položka šarže je uložena v inventáři s číselnou řadou „LOT“.

**Očekávané zásoby**:

|Číslo šarže|Množství|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Celkem|120|

**Zaznamenané zmožství**:

|Číslo šarže|Množství|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|20|
|LOT1006|10|
|Celkem|112|

**Množství k zaúčtování**:

|Číslo šarže|Očekávané zásoby|Zaznamenané zmožství|Množství k zaúčtování|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|20|-10|
|LOT1006|10|0|-10|
|Celkem|120|112|-8|

Na stránce **Objednávky fyzické inventury** bude pole **Negativní  množství  (Základ)** obsahovat *8*. Pro dotyčný řádek objednávky bude stránka **Seznam sledovaného zboží  fyz.   inventury** obsahovat kladná nebo záporná množství pro jednotlivá čísla šarží.

## Viz také
[Počet, úprava a překlasifikace zásob pomocí deníků](inventory-how-count-adjust-reclassify.md)  
[Práce se sériovými čísly a čísly šarží](inventory-how-work-item-tracking.md)  
[Zásoby](inventory-manage-inventory.md)  
[Správa skladů](warehouse-manage-warehouse.md)  
[Prodej](sales-manage-sales.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
