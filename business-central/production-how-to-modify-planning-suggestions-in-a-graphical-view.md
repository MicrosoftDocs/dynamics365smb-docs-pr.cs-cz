---
    title: How to Modify Planning Suggestions in a Graphical View | Microsoft Docs
    description: A typical planning activity is to change or add planning worksheet lines to modify the suggested supply orders before you commit them by running the **Carry out Action Message** function. An alternative to doing this in the planning worksheet is to use a graphical view.
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
# Změna návrhů plánování v grafickém zobrazení
Typickou plánovací činností je změna nebo přidání řádků plánovacího listu za účelem úpravy navrhovaných objednávek dodávek dříve, než je provedete, spuštěním funkce **Provést hlášené akce**. Alternativou k tomu v sešitu plánování je použití grafického zobrazení.

Na stránce **Dostupnost zásob v čase**, můžete upravit určité objednávky a návrhy dodávky přetažením prvků na ose x a změnit tak množství, nebo přetažením prvků na ose y změnit datum splatnosti.

Na stránce **Dostupnost zásob v čase** a stránce **Plánovací sešit** můžete provést následující změny:

- Upravte navrhovanou objednávku dodávky, která existuje pouze jako řádek plánování.
- Upravte existující objednávku dodávky, kterou systém plánování navrhuje změnit.
- Vytvořte novou doporučenou objednávku dodávky a upravte ji.

Další informace o zobrazených typech řádků plánování naleznete v poli Popis na záložce **Změny události**.

Pokud zvolíte **Uložit změny** na stránce **Dostupnost zásob v čase**, provedené změny se zkopírují do sešitu plánování nebo sešitu požadavků. Nyní je můžete implementovat pomocí funkce **Provést hlášení akce - plán.**.

Následující postup ukazuje, jak upravit návrhy nabídky přetažením. Alternativně můžete změnit pole **Datum splatnosti** a **Množství** na záložce **Změny události** a okamžitě zobrazit změny graficky na záložce **Časová osa** na stránce **Sešity plánování**.

## Chcete-li upravit navrhované objednávky dodávek v grafickém zobrazení
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dostupnost zásob v čase** a poté vyberte související odkaz.

   Stránka **Dostupnost zásob v čase** se otevře s číslem zboží, lokací, and variantou zboží na vybraném plánovacím řádku předvyplněném na záložce s náhledem **Možnosti**. Záložka s náhledem **Časová osa** zobrazuje grafické znázornění plánovaných zásob položky, včetně návrhů plánování

2. Ujistěte se, že je vybráno pole **Zahrnout návrhy plánování**.
3. Najděte navrhovanou objednávku dodávky, kterou chcete upravit. Modifikovatelné prvky můžete identifikovat pomocí zeleného kruhu a ikony disku. Pro více informací o různých symbolech, navštivte [Symboly a ikony na záložce časové osy](production-how-to-modify-planning-suggestions-in-a-graphical-view.md#symbols-and-icons-on-the-timeline-fasttab).
4. Umístěte ukazatel nad zelený kruh, dokud se nezvětší a ukazatel se nezmění na Přesunout tvar (čtyři šipky).
5. Stisknutím a podržením tlačítka myši během tažení ukazatelem nahoru nebo dolů upravte množství. Stisknutím a podržením tlačítka myši při přetahování ukazatele doleva nebo doprava upravíte datum splnění.
6. Kromě pohyblivých prvků přetažením můžete upravovat návrhy plánování pomocí několika funkcí rozevírací nabídky. Otevřete rozbalovací nabídku zeleného kruhu navrhovaného prvku dodávky a vyberte jednu z následujících funkcí

   | Funkce | Popis |
   |--------------|---------------------------------------|  
   | **Vytvořit novou dodávku** | Vytvoří nový bod prvku, ve kterém přistupujete k rozevírací nabídce, která představuje novou navrhovanou objednávku dodávky. Když zvolíte **Uložit změny** stane se z něj nový řádek v sešitu plánování.<br /><br /> **NOTE:** Pokud jsou pole **Filtr lokace** nebo **Filtr varianty** na záložce s náhledem **Možnosti** prázdné, nebo mají více než jednu hodnotu filtru. Pak je nová dodávka vytvořena a později uložena do sešitu plánování nebo seš.požadavků s následujícími kódy:<br /><br /> * Pokud je pole filtru prázdné, nové dodávky jsou vytvořeny bez kódu lokace nebo varianty.<br /><br /> * Pokud je definováno více než jedna hodnota filtru, bude nové zboží vytvořeno pro první hodnotu filtru podle metody řazení.<br /><br />  Pokud chcete jinou variantu nebo kód lokace, musíte jej ručně změnit na novém řádku plánování. |
   | **Automaticky upravovaná dodávka** | Optimalizuje novou dodávku, kterou jste vytvořili v grafu, tím, že se ujistíte, že má za následek nulový počet zásob před další dodávkou. |
   | **Odstranit dodávku** | Odstraní prvek v záložce s náhledem **Časová ose** a vymaže plánovací řádek, když zvolíte **Uložit změny**. Po odstranění zdroje se ikona změní na disk, který má červený kříž.<br /><br /> **NOTE:** Smazat lze pouze dodávku typu zprávy o akci **Nový**. Potom co zvolíte **Uložit změny**, je nutné ručně odstranit plánování řádek plánování nebo sešitu požadavků. |

7. Vyberte akci **Znovu načíst** pokud chcete resetovat všechny změny, které jste provedli po posledním otevření stránky **Dostupnost zásob v čase** nebo vybrané **Znovu načíst**.
8. Když jsou prvky umístěny tam, kam je chcete v diagramu umístit, zvolte **Uložit změny** a zkopírujte změněné množství a datum do plánovacích nebo rekvizičních linek, které představují grafické prvky.

Chcete-li implementovat změny plánu zásobování, musíte dodržovat výsledné zprávy o akci z plánovacího nebo rekvizičního listu. Další informace naleznete v části Provést hlášení akce - plán.

## Symboly a ikony na časové ose záložky s náhledem
| Symbol/ikona | Popis |
|------------------|---------------------------------------|  
| Černý křížek | Objednávky (jak nabídky tak poptávky).<br /><br /> -   Nemohou být upravovány<br />-   Viditelné když pole **Zobrazit plánované zásoby** je vybráno (oranžový graf). |
| Rudý kruh | Existující objednávky dodávek, které nejsou v návrzích plánování.<br /><br /> -   Nemůže být upravena.<br />-   Viditelné, když je vybráno pole **Zobrazit plánované zásoby** (oranžový graf). |
| Žlutá hvězda | Předpověď poptávky.<br /><br /> -   Nemůže být upravena.<br />-   Viditelné, když má pole **Název předpovědi** hodnotu.<br /><br /> Když jsou vybrané oba dva pole **Zobrazit plánované zásoby** a **Zahrnout návrhy plánování**, pak každá žlutá hvězda má each yellow star has a propojený protějšek na opačné straně grafu. To ilustruje, jak navrhovaná nabídka splňuje předpokládanou poptávku. |
| Zelený kruh s ikonou ve tvaru disku, který má červený kříž | Navrhovaná objednávka dodávky se zprávou akce *Zrušit*.<br /><br /> -   Nemůže být modifikována.<br />-   Viditelná, když je vybráno pole **Zahrnout návrhy plánování** (zelený graf). |
| Zelený kruh s ikonou ve tvaru disku, který má hvězdu | Navrhované objednávky dodávek s akční zprávou *Nový*.<br /><br /> -   Mohou být modifikovány <br />-   Viditelné když je vybráno pole **Zahrnout návrhy plánování** (zelený graf). |
| Zelený kruh s ikonou ve tvaru disku, který má jednu nebo dvě šipky | Navrhované objednávky dodávek se zprávou akce *Přeplánovat*, *Změna množ.*, nebo *Přeplán. změna  množství*<br /><br /> -   Může být upraveno.<br />-   Viditelné když je vybráno pole **Zahrnout návrhy plánování** (zelený graf).<br /><br /> Šipky odrážejí směr návrhu plánování. Například šipka vlevo spolu se šipkou nahoru odráží akční zprávu *Přeplán. změna  množ.* která se skládá ze zpětného přeplánování a zvýšení množství. |

Když otevřete rozbalovací nabídku pro záložku **Časová osa**, zobrazí se následující funkce v závislosti na tom, co zvolíte

| Funkce | Popis |
|--------------|---------------------------------------|  
| **Vytvořit novou dodávku** | Vytvoří nový prvek v bodě, kde vstoupíte do rozbalovací nabídky, což představuje novou navrhovanou objednávku dodávky. Když zvolíte **Uložit změny** na záložce **Proces** stane se z něj nový řádek v sešitu plánování.<br /><br /> Jakékoliv hodnoty filtru, které jsou definovány na polích **Filtru lokace** nebo **Filtr varianty** na záložce s náhledem **Možnosti** budou použity pro novou objednávku dodávky. **Note:** Pokud jsou pole filtru prázdná nebo mají více než jednu hodnotu filtru, vytvoří se nová objednávka dodávky pomocí následujících kódů: <ul><li>Pokud je pole filtru prázdné, je nový zdroj vytvořen bez kódu umístění nebo varianty.</li><li>Je-li definována více než jedna hodnota filtru, vytvoří se nová dodávka pomocí první hodnoty filtru podle pořadí třídění.</li></ul> Pokud chcete v nové objednávce dodávek jinou variantu nebo kód lokace, musíte jej ručně změnit na novém řádku plánování. |
| **Automaticky upravovaná dodávka** | Optimalizuje novou dodávku, kterou jste vytvořili v grafu, tím, že se ujistí o tom, že vytvoří nulové zásoby před další dodávkou. |
| **Odstranit dodávku** | Odstraní prvek v záložce s náhledem **Časová osa** a vymaže plánovací řádek, když zvolíte **Uložit změny** na záložce **Proces**. Ikona se změní na disk, který má červený kříž, když byl zdroj odstraněn. **Note:** Můžete smazat pouze nabídku akční zprávy typu *Nový*. Po tom co zvolíte **Uložit změny** na kartě **Process** je nutné ručně odstranit plánování řádek plánování nebo sešitu požadavků. |
| **Zobrazit dokument** | Otevře objednávku, řádek plánování nebo prognózu, kterou prvek představuje. |
| **Oddálit (Ctrl++)** | Zvětší měřítko osy x, takže se zobrazí méně dní. **Note:**   To lze také provést stisknutím ctrl + kolečka myši. |
| **Přiblížit (Ctrl+-)** | Zmenší měřítko osy x, takže se zobrazí více dní. **Note:**   To lze také provést stisknutím ctrl + kolečka myši. |
| **Resetovat zvětšení (Ctrl+0)** | Vrací měřítko osy x podle toho, co bylo použito před zvětšením. |

Kromě akcí klávesnice, které byly zmíněny dříve, můžete také použít následující akce klávesnice v záložce s náhledem **Časová osa**.

| Akce klávesnice | Popis |
|---------------------|---------------------------------------|  
| Ctrl + kolečko myši | Mění měřítko osy x. |
| Vyberte prvek a poté stiskněte Shift + Šipka | Posune prvek ve směru šipky. |
| Tab | Přesune se na další prvek. |
| Shift+Tab | Přechod na předchozí prvek. |
| Při přesouvání prvku stisknutí klávesy Esc. | Zruší přesun. **Note:**  Nefunguje, pokud jste uvolnili tlačítko myši. |

## Viz také
[Plánování](production-planning.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)  
[Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
