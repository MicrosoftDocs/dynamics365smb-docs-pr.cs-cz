---
    title: Design Details - Item Tracking and Reservations | Microsoft Docs
    description: This topic talks about item tracking and reservations, and describes the concepts behind the two.
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
# Detaily návrhu: Sledování zboží a Rezervace

Současné použití rezervace a sledování konkrétního zboží je neobvyklé, protože oba vytvářejí spojení mezi nabídkou a poptávkou. S výjimkou situací, kdy zákazník nebo plánovač výroby požaduje určitou šarži, kdy má zřídka smysl rezervovat skladové položky, které nesou čísla sledování zboží pro konkrétní výběr. I když je možné rezervovat zboží, které vyžaduje konkrétní sledování zboží, je zapotřebí speciálních funkcí, aby se zabránilo konfliktům dostupnosti mezi zpracovateli objednávek, kteří požadují stejné zboží sledované položkou.

Koncept "Pozdní vazby" zajišťuje, že nespecifická rezervace sériového čísla nebo čísla šarže zůstane volně spojena až do zaúčtování. V době zaúčtování může rezervační systém přemístil nespecifické rezervace, aby bylo zajištěno, že vyrovnání možné proti sériovému číslu nebo číslu šarže, které je skutečně vybráno. Mezitím je sériové číslo nebo číslo šarže k dispozici pro konkrétní rezervaci v jiných dokladech, které požadují toto konkrétní sériové číslo nebo číslo šarže.

Nespecifická rezervace je rezervace, ve které se uživatel nestará o to, která konkrétní položka je vybrána, a konkrétní rezervace je rezervace, ve které se uživatel ví, kterou chce.

> Funkce Pozdní vazba se týká pouze položek, které jsou nastaveny se sledováním konkrétního zboží a vztahuje se pouze na rezervace proti zísobám, nikoli proti příchozím objednávkám.

Rezervace čísel sledování zboží spadá do dvou kategorií, jak je znázorněno v následující tabulce.

| Rezervace | Popis |
|-----------------|---------------------------------------|  
| Specifikcé | Určité sériové číslo nebo číslo šarže vyberete při rezervaci skladové položky z poptávky, například v prodejní objednávce.<br /><br /> Jedná se o běžnou rezervace. Jedná se o pevnou vazbu mezi nabídkou a poptávkou, která nese sériová čísla i čísla šarží. **Poznámka:**  Poptávka nese sériová čísla nebo čísla šarží. <br /><br /> Příkladem je rezervace plechovky modré barvy ze šarže A, protože si o to zákazník požádá. Zákazníkovi je tedy dodána plechovka modré barvy ze šarže A. |
| Nespecifické | Při rezervaci skladového zboží z poptávky, například v prodejní objednávce, nebudete muset vybírat určité sériové číslo nebo číslo šarže.<br /><br /> Jedná se o stav, který je uložen u položky rezervace pro sériová čísla nebo čísla šarží, která nejsou vybrána specificky. **Poznámka:**  Poptávka nenese sériová čísla ani čísla šarží. <br /><br /> Chcete například rezervovat plechovku modré barvy z libovolné šarže pro prodejní objednávku. Zákazníkovi je odeslána plechovka modré barvy s náhodným sériovým číselem nebo číslem šarže. |

Hlavní rozdíl mezi specifickou a nespecifickou rezervací je definován existencí sériových čísel nebo čísel šarží na straně poptávky, jak je znázorněno v následující tabulce.

| Typ | Dodávka | Poptávka |
|-----------------|-----------------------|--------------------------|
| **Specifické** | Sériové číslo nebo číslo šarže. | Sériové číslo nebo číslo šarže. |
| **Nespicifické** | Sériové číslo nebo číslo šarže. | Žádné sériové číslo nebo číslo šarže. |

Pokud rezervujete zásoby zboží z řádku výstupního dokladu, které má přiřazeno číslo sledování zboží a je nastaveno pro konkrétní sledování zboží, stránka **Rezervace** Vás vede různými pracovními postupy v závislosti na potřebě sériových čísel nebo čísel šarží.

## Specifická rezervace
Když zvolíte **Rezervovat** z řádku výstupního dokladu, zobrazí se dialogové okno s informacemi o tom, zda chcete rezervovat konkrétní sériová čísla nebo čísla šarží Pokud zvolíte **Ano**, zobrazí se seznam se všemi sériovými čísly nebo čísly šarží přiřazenými k řádku dokladu. Stránka **Rezervace** se otevře po výběru jednoho ze sériových čísel nebo čísel šarží a můžete si je rezervovat mezi vybranými sériovými čísly nebo čísly šarží typickým způsobem.

Pokud jsou některá konkrétní čísla sledování zboží, která se pokoušíte rezervovat blokována v nespecifické rezervaci, pak vás zpráva v dolní části stránky **Rezervace** informuje, kolik z celkového rezervovaného množství je blokováno v nespecifické rezervaci a zda je stále k dispozici.

## Nespecifická rezervace
Pokud v zobrazeném dialogovém okně zvolíte **Ne** otevře se stránka **Rezervace** a umožní vám rezervovat mezi všemi sériovými čísly nebo čísly šarží v zásobách.

Vzhledem ke struktuře rezervačního systému musí systém při umistování nespecifické rezervace zboží sledovaného zboží vybrat konkrétní položky zboží, proti které má být rezervováno. Protože položky zboží nesou i sledovací čísla zboží, rezervace si nepřímo vyhrazuje konkrétní sériová čísla nebo čísla šarží, i když jste to neměli v úmyslu. Aby se tato situace vyřešila, rezervační systém se před účtováním pokusí přesunout nespecifické položky rezervace.

Systém ve skutečnosti stále rezervuje proti konkrétním položkám, ale pak používá mechanismus přessunutí, kdykoli je v nespecifické rezervaci specifická poptávka po šarži nebo sériovém čísle. To může být případ, kdy účtujete transakci poptávky, například prodejní objednávku, deník spotřeby nebo objednávku transferu pro sériové číslo nebo číslo šarže nebo při pokusu o konkrétní rezervaci sériového čísla nebo čísla šarže. Systém přesunuje rezervace tak, aby byla šarže nebo sériové číslo k dispozici poptávce nebo konkrétní rezervaci, čímž se do nespecifické rezervace umístí jiné číslo šarže nebo sériové číslo. Pokud zásoby mají nedostatečné množství, systém provede co největší přesunutí a zobrazí se chyba dostupnosti, pokud v době zaúčtování stále není dostatečné množství.

> [!NOTE]  
> U nespecifické rezervace jsou pole čísla šarže nebo sériového čísla prázdné v záznamu rezervace, který ukazuje na poptávku, jako je prodej.

## Přesunutí
Když uživatel zaúčtuje odchozí doklad po výběru nesprávného sériového čísla nebo čísla šarže, ostatní nespecifické rezervace se přesunou tak, aby odrážely skutečné sériové číslo nebo číslo šarže, které je vyskladněno. To uspokojí účtovací modul pevným vyrovnání mezi nabídkou a poptávkou.

U všech podporovaných obchodních scénářů je přemístíní možné pouze proti kladným položkám zboží, které nesou čísla rezervací, sériová čísla nebo šarže, ale bez definovaných sériových čísel nebo čísel šarží na straně poptávky.

## Podporované obchodní scénáře
Funkce Pozdní vazba podporuje následující obchodní scénáře:

* Zadání určitého sériového čísla nebo čísla šarže do výstupního dokladu s nespecifickou rezervací nesprávného sériového čísla nebo čísla šarže.
* Rezervace konkrétního sériového čísla nebo čísla šarže.
* Účtování výstupního dokladu s nespecifickou rezervací sériového čísla nebo čísla šarže

### Zadání sériových čísel nebo čísel šarží do výstupního dokladu se špatnou nespecifickou rezervací
To je nejběžnější ze tří podporovaných scénářů. V tomto případě funkce Pozdní vazba zajišťuje, že uživatel může zadat sériové číslo nebo číslo šarže, které je skutečně vyskladněné do výstupního dokladu, který má nespecifické sledování jiného sériového čísla nebo čísla šarže.

Potřeba nastává například v případě, že zpracovatel objednávky poprvé provedl nespecifickou rezervaci libovolného sériového čísla nebo čísla šarže. Později, když je zboží skutečně vyskladněné ze skladu, musí být vyskladněné sériové číslo nebo číslo šarže zadáno do objednávky před jeho účtováním. Nespecifická rezervace je v době zaúčtování přesunuta, aby bylo zajištěno, že vyskladněné sériové číslo nebo číslo šarže lze zadat bez ztráty rezervace a aby bylo zajištěno, že vyskladěné sériové číslo nebo číslo šarže může být plně použito a zaúčtováno.

### Rezervace konkrétního sériových čísel nebo čísel šarže.
V tomto obchodním scénáři funkce Pozdní vazba zajišťuje, že uživatel pokoušející se rezervovat určité sériové číslo nebo číslo šarže, které je aktuálně nespecificky rezervováno, tak může učinit. Nespecifická rezervace je v době rezervace přesunuta, aby se pro konkrétní požadavek uvolnilo sériové číslo nebo číslo šarže.

K přesunutí dojde automaticky, ale vložená nápověda zobrazena ve spodní řástu stránky **Rezervace** zobrazí následující text:

**XX z celkového rezervovaného množství je nespicifikováno a může být k dispozici**.

Kromě toho pole **Nespecifické rezervované množství.** kazuje, kolik položek rezervace je nespecifických. Ve výchozím nastavení toto pole není viditelné pro uživatele.

### Účtování výstupních dokladů s nespecifickou rezervací sériových čísel nebo čísel šarží
Tento obchodní scénář je podporován funkcí Pozdní vazba, která umožňuje pevné vyrovnání a odchozí účtování toho, co je skutečně vyskladněno pomocí přesunutí na jinou nespecifickou rezervaci sériového čísla nebo čísla šarže. Pokud přesunutí není možné, zobrazí se při pokusu účtování dodávky následující standardní chybová zpráva:

**Zboží XX nemůže být plně vyrovnána.**

## Viz také
[Detaily návrhu: Sledování zboží](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]