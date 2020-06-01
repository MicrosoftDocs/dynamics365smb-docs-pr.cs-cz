---
    title: How to Remove and Reapply Item Entries | Microsoft Docs
    description: You can view and manually change certain item application entries that are created automatically during inventory transactions.
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
# Odebrat a znovu vyrovnat položky zboží
Na stránce **Sešit vyrovnání** můžete zobrazit a ručně změnit určité položky vyrovnání zboží, které jsou vytvářeny automaticky během skladových transakcí.

Když odešlete transakci, ve které je zboží přesunuto nebo vyřazeno ze zásob, vytvoří se mezi každým zvýšením a poklesem zásob vyrovnání zboží. Toto vyrovnání určuje tok nákladů ze zboží, které je přijato na skladě, do nákladů na zboží, které vychází ze skladu. Z důvodu způsobu výpočtu jednotkových nákladů by nesprávné vyrovnání zboží mohlo vést k překročení průměrných nákladů a zkreslení jednotkových nákladů. Pro více informací navštivte Detaily návrhu: Vyrovnání zboží.

Následující scénáře mohou vyžadovat, abyste vyrovnání zrušili nebo znovu vyrovnali položky zboží:

- Zapomněli jste určit pevné vyrovnání.
- Udělali jste nesprávné pevné vyrovnání.
- Musíte vrátit zboží, které již bylo prodáno.

Pokud je to možné, použijte doklad k opětovnému použití položky zboží. Pokud například musíte provést nákupní vratku zboží, na které již byl prodej vyrovnán, můžete znovu použít vytvoření a zaúčtování dokladu nákupní vratky pomocí správného vyrovnání v poli **Vyrovnat položkou zboží** na řádku nákupní vratky. Chcete-li to usnadnit, můžete použít funkci **Získat účt. řádky pro stornování** nebo funkci **Kopírovat z dokladu**. Když zaúčtujete doklad, položka zboží se automaticky znovu použije. Pro více informací navštivte [Zpracování nebo zrušení nákupní vratky](purchasing-how-process-purchase-returns-cancellations.md).

Pokud nemůžete doklad opětovně použít, například když je třeba opravit pevné vyrovnání, opravte vyrovnání pomocí stránky **Sešit vyrovnání**.

> [!Warning]
> Při práci s sešitem vyrovnání je důležité si pamatovat následující:
- Položky vyrovnání byste neměli ponechat dlouho nepoužívané, protože ostatní uživatelé pak nemohou zpracovat zboží, dokud znovu nevyrovnáte položky vyrovnání nebo nezavřete stránku **Sešit vyrovnání**. Uživatelé, kteří se pokoušejí provádět akce, které zahrnují nepoužívané položky vyrovnání, obdrží následující chybovou zprávu: „Tuto akci nemůžete provést, protože pro položky zboží XXX je vyrovnání zrušeno v pracovním sešitě vyrovnání uživatelem XXX.“
- Položky zboží byste měli znovu vyrovnat pouze během nepracovních hodin, abyste zabránili konfliktům s ostatními uživateli, kteří účtují transakce se stejným zbožím.
- Když zavřete sešit vyrovnání, [!INCLUDE[d365fin](includes/d365fin_md.md)] provede kontrolu, aby se ujistil, že jsou použity všechny položky. Pokud například odeberete žádost o množství, ale nevytvoříte nové vyrovnání a potom zavřete sešit vyrovnání, vytvoří se nové vyrovnání. To pomáhá udržet náklady neporušené. Pokud však odstraníte pevné vyrovnání, nové pevné vyrovnání se po zavření sešitu automaticky nevytvoří. Musíte to udělat ručně vytvořením nového vyrovnání v sešitu.
- V sešitu vyrovnání je možné odstranit vyrovnání z více než jedné položky najednou. Protože však vyrovnávací položky ovlivňují sadu položek, které jsou k dispozici pro vyrovnání, nemůžete vytvořit vyrovnání pro více než jednu položku najednou.
- Sešit vyrovnání nemůže vytvořit vyrovnání v následující situaci: Pokud není na skladě dostatek množství k vyrovnání, nelze vytvořit sešit vyrovnání, když se pokoušíte vyrovnat položku snížení zásob bez informací o sledování zboží na položku zvýšení zásob s informacemi o sledování zboží.

## Odebrání vyrovnání zboží pomocí sešitu vyrovnání
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit vyrovnání** a poté vyberte související odkaz.
2. Otevře se stránka **Sešit vyrovnání** zobrazující existující položky zboží pro všechno zboží.
3. Zadejte filtry na záložce **Obecné**, aby bylo snazší najít položku zboží, pro kterou chcete vyrovnání změnit.
4. Vyberte položku zboží a poté vyberte akci **Vyrovnané položky**. Otevře se stránka **Zobrazit vyrovnané položky – Vyrovnané položky** která zobrazuje položku zboží nebo položky, které jsou aktuálně vyrovnány s vybranou položkou.
5. Vyberte položku zboží, pro kterou chcete vyrovnání odebrat.
6. Vyberte akci **Odebrat vyrovnání**. Tím odeberete položku vyrovnání zboží, která propojí dvě položky zboží, a přesunete ji na stránku **Zobrazit vyrovnané položky – Nevyrovnané položky**.
7. Zavřete stránku **Zobrazit vyrovnané položky – Vyrovnané položky**.

Pole **Zůstatek (množství)** dvou položek zboží je zvýšeno o množství, které nebylo vyrovnáno. Odebraná položka zboží je nyní k dispozici pro opětovné vyrovnání na stránce **Zobrazit vyrovnané položky – Nevyrovnané položky**.

> [!IMPORTANT]
> Neměli byste ponechat položky vyrovnání déle nevyrovnané, protože ostatní uživatelé nemohou zpracovat ovlivněné položky, dokud znovu položky vyrovnání nevyrovnáte nebo nezavřete stránku **Sešit vyrovnání**. Následující chybová zpráva se zobrazí, pokud se pokusíte provést akce, které se týkají  nevyrovnané položky vyrovnání:
> **Tuto akci nemůžete provést, protože položky pro zboží  <item> nejsou uživatelem vyrovnány v sešitu vyrovnání. <user>**
> 
## Opětovné vyrovnání položky pomocí sešitu vyrovnání
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit vyrovnání** a poté vyberte související odkaz.
2. Otevře se stránka **Sešit vyrovnání** zobrazující existující položky zboží pro všechno zboží.
3. Chcete-li znovu vyrovnat položky, které byly odebrány od otevření sešitu, vyberte položku zboží, kterou chcete znovu vyrovnat, a poté vyberte akci **Znovu vyrovnat**.

   > [!NOTE]
Toto opětovné vyrovnání se automaticky projeví v původní rozvaze, když zavřete stránku **Sešit vyrovnání**.
4. Chcete-li použít dostupnou otevřenou položku zboží s jinou položkou, vyberte položku zboží, kterou chcete použít. Vyberte akci **Nevyrovnané položky**. Otevře se stránka **Zobrazit vyrovnané položky – Nevyrovnané položky**.
5. Vyberte jednu nebo více položek zboží, které chcete použít pro vybranou položku na stránce **Sešit vyrovnání**, a poté vyberte tlačítko **OK**.

   Mezi dvěma položkami zboží je vytvořena položka vyrovnání zboží. Pole **Zůstatek (množství)** obou položek jsou snížena o použité množství.

   > [!NOTE]
Pokud jste se rozhodli vytvořit vyrovnání, které by v procesu úpravy nákladů vytvořilo nekonečnou smyčku, nebude navržené vyrovnání vytvořeno. K tomu může dojít, když původní položky vytvořily záporné zásoby. Žádost není podána. Proto je nutné vybrat jinou položku pro vyrovnání.
6. Pokud je pole **Automatická adjustace nákladů** v **Nastavení zásob** nastaveno na **Vždy**, pak se po provedení opětovného vyrovnání automaticky spustí dávková úloha pro úpravu nákladů. Jinak spusťte dávkovou úlohu **Adjustace nákladů položek zboží** a ujistěte se, že jsou všechny náklady aktuální.

## Viz také
[Uzavření otevřených položek zboží, které vyplývají z pevného vyrovnání z deníku zboží](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Zpracování nebo zrušení nákupní vratky](purchasing-how-process-purchase-returns-cancellations.md)  
[Správa nákladů zásob](finance-manage-inventory-costs.md)  
[Detaily návrhu: Vyrovnání zboží](design-details-item-application.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
