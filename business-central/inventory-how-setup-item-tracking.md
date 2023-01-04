---
    title: Set Up Item Tracking with Serial, Lot, and Package Numbers
    description: Set up item tracking with serial numbers, lot numbers, and package numbers

    author: SorenGP

    
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 08/31/2021
    ms.author: edupont

---
# Nastavte sledování zboží pomocí sériových čísel, čísel šarží a čísel balíků

Sledujte skladové položky i ve složitých skladových konfiguracích pomocí čísel, která jsou specifická pro každou položku, ať už jako jednotlivý objekt, šarži nebo balíček. Pomocí sledování zboží můžete sledovat položky v rámci interních skladových pohybů a u odesílaných a přijímaných dokladů.

Zboží se sériovými čísly a čísly šarží lze v dodavatelském řetězci sledovat jak zpětně tak i dopředu. To je užitečné pro obecné zajištění kvality a pro případné stažení výrobků z oběhu Pro více informací navštivte [Sledování položek sledovaného zboží](inventory-how-to-trace-item-tracked-items.md).

> [!TIP]
> V roce 2021 ve vlně 1 a novějších zapněte aktualizaci funkce *Použít sledování podle čísla balíku v rezervačním a sledovacím systému*, pokud chcete pracovat s čísly balíků a také sériovými čísly a čísly šarží.. Pro další informace se podívejte na [Povolení nadcházejících funkcí s předstihem](admin-feature-management.md). Jakmile je funkce zapnutá, můžete přiřadit čísla balíků odchozím a příchozím dokladům podobně jako při práci s čísly šarží.

## Čísla a sledování zboží

Jako součást vašich skladových procesů můžete své zásoby do dát balíčků, krabic, kontejnerů a dalších. Ale abyste měli přehled o položkách, přidělujete jedinečná čísla pro identifikaci. Například vyrábíte a prodáváte židli, která má číslo zboží *1900-S*. Každá jednotlivá židle má sériové číslo *1001* ale také sdružíte čtyři židle do šarže *LOT0001* a židle odešlete v kontejneru s číslem balení *CONTAINER010*, který také obsahuje další položky, jako je *LOT0100* s odkládacími stolky a *LOT200* s lampami.

V závislosti na konfiguraci můžete tato různá čísla používat ke sledování zásob v [!INCLUDE [prod_short](includes/prod_short.md)]  v různých fázích nákupu, prodeje, skladových operací atd.

## Nastavení Kódů sledování zboží

Kód sledování zboží odráží odráží různé úvahy společnosti týkající se používání sériových čísel a čísel šarží u položek, které procházejí skladem.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kódy sledování zboží** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. V záložce **Sériové číslo**, **Číslo šarže** a **Číslo balení** definujte zásady sledování zboží podle sériového čísla, čísla šarže a balení.

> [!NOTE]  
> IPokud chcete sledovat konkrétní položky nebo konkrétní šarže po celou dobu jejich životnosti, musíte zvolit pole **Sledování sériových čísel**, respektive **Sledování šarže**. V důsledku toho musíte při manipulaci s odchozí jednotkou zboží s tímto kódem sledování položky vždy určit, které stávající sériové číslo nebo které stávající číslo šarže se má zpracovat. To znamená, že při prodeji jednotky zboží musí být použita proti určitému souboru sériových čísel nebo konkrétnímu číslu šarže ve skladu. Nebo jinými slovy, sériové číslo nebo číslo šarže přiřazené ke zboží při vstupu do zásob musí následovat tento typ položky mimo zásoby.

Vzhledem k tomu, že toto konkrétní pole nastavení zahrnuje všechny možné transakce s daným zbožím, budou vybrána i jednotlivá příchozí/odchozí pole. Jednotlivá příchozí/odchozí pole však nemají nic společného s aplikací napříč skladem – pouze definují pracovní tok vaší společnosti, pokud jde o to, kdy přiřadit čísla sledování zboží.

> [!NOTE]  
> Aby bylo možné při skladových činnostech přiřadit sledovací čísla položek, musí být na kartě kódu položky vybrána pole **Sledování s.čísel ve skladu** a **Sledování šarže ve skladu**.

## Nastavení pravidel pro vypršení platnosti sériových čísel nebo čísel šarží

U některého zboží můžete chtít v kódu pro sledování položek nastavit konkrétní data a pravidla expirace. Tato funkce umožňuje sledovat, kdy končí platnost konkrétních sériových čísel a čísel šarží.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kódy sledování zboží** a poté vyberte související odkaz.
2. Vyberte existující kód sledování zboží a poté vyberte akci **Upravit**.
3. Na záložce **Různé** vyberte následující pole:

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Přísné účtování expirace** | Určuje, že datum vypršení platnosti přiřazené ke sledovacímu číslu zboží při zadaném stavu zásob musí být respektováno při vydávání zásob. |
   | **Vyžadovat Položku data záruky** | Určuje, že je nutné zadat datum expirace platnosti na řádku sledování zboží. |
   | **Použít data expirace** | Určuje, že chcete vypočítat data vypršení platnosti. |

## Nastavení záruk pro sériová čísla nebo čísla šarží

U některého zboží můžete chtít nastavit konkrétní záruku v kódu sledování zboží. Tato funkce vám umožní sledovat, kdy skončí záruky na konkrétních sériových číslech nebo šaržích ve vašich zásobách.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kódy sledování zboží** a poté vyberte související odkaz.
2. Vyberte existující kód sledování zboží a poté vyberte akci **Upravit**.
3. V záložce **Různé** vyplňte pole **Vzorec data záruky** a poté vyberte pole následujícím způsobem:

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Vzorec data záruky** | Určuje poslední den záruky zboží |
   | **Vyžadovat zadání data záruky** | Určuje, že musíte ručně zadat datum záruky na řádek sledování zboží. |


## Nastavení zboží pro správné sledování zboží

Chcete-li povolit sledování zboží, musíte nejprve přiřadit kódy sledování zboží ke zboží. Existují dva způsoby, jak přidat kódy sledován zboží, a to výběrem kódu z předdefinovaného seznamu nebo přiřazením nového jedinečného kódu. Najeďte myší na pole a přečtěte si krátký popis.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte existující zboží ze seznamu a otevřete stránku **Karta zboží**.
3. V záložce **Sledování zboží** přiřaďte příslušné kódy sledování zboží a zvolte **Kód sledování zboží**, **Sériová čísla** a **Čísla šarže**.
   1. Případně můžete také vytvořit nový kód sledování zboží výběrem akce **Nový**.

## Viz také

[Práce se sériovými čísly a čísly šarží](inventory-how-work-item-tracking.md)
[Sledování zboží - Sledované zboží](inventory-how-to-trace-item-tracked-items.md)  
[Zásoby](inventory-manage-inventory.md)  
[Detaily návrhu: Sledování zboží](design-details-item-tracking.md)  
[Detaily návrhu:  ledování zboží a Rezervace](design-details-item-tracking-and-reservations.md)  
[Rezervace zboží](inventory-how-to-reserve-items.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]