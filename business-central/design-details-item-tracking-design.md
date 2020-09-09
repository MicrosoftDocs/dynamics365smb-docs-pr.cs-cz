---
    title: Design Details - Item Tracking Design | Microsoft Docs
    description: This topic describes the design behind item tracking in Business Central.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: design, item, tracking, tracing
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Detaily návrhu: Design sledování zboží
V prvních verzích sledování zboží v [!INCLUDE[d365fin](includes/d365fin_md.md)] 2.60, byla sériová čísla a čísla šarží evidována přímo v položkách zboží. Tento design poskytoval úplné informace o dostupnosti a jednoduché sledování historických položek, ale postrádal flexibilitu a funkčnost.

Od verze [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.00, je funkce sledování zboží v samostatné struktuře objektů se složitějšími odkazy na účtované doklady a položky zboží. Tento design byl flexibilní a bohatý co se týče funkcionality, ale sledování zboží nebylo plně zapojeno do výpočtů dostupnosti zboží.

Od verze [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 je funkce sledování zboží integrována s rezervačním systémem, který zpracovává rezervace, sledování objednávek a zasílání zpráv o akcích. Pro více infomací navštivte “Detaily návrhu: Rezervace, sledování zboží a zasílání zpráv o akcích” v “Detaily návrhu: Plánování dodávek”.

Tento nejnovější návrh zahrnuje položky sledování zboží do výpočtů celkové dostupnosti v celém systému, včetně plánování, výroby a skladování. Starý koncept přenášení sériových čísel a čísel šarží v položkách zboží je znovu zaveden, aby byl zajištěn jednoduchý přístup k historickým datům pro účely sledování zboží. V souvislosti se zlepšením sledování zboží v [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60, byl rezervační systém rozšířen na ne-objednávkové entity, jako jsou deníky, faktury a dobropisy.

S přidáním sériových čísel nebo čísel šarží zpracovává rezervační systém trvalé atributy položek a zároveň zpracovává přerušované propojení mezi nabídkou a poptávkou ve formě položek sledování objednávek a položek rezervace. Další odlišnou charakteristikou sériových čísel nebo čísel šarží ve srovnání s konvenčními údaji o rezervaci je skutečnost, že mohou být zaúčtovány, a to buď částečně, nebo úplně. Proto tabulka **Položky rezervace** (T337) nyní pracuje se související tabulkou **Specifikace sledování** (T336), která spravuje a zobrazuje sčítání mezi aktivním a zaúčtovaným množství položek sledování množství. Pro více informací navštivte [Detaily návrhu: Aktivní versus Historické položky sledování zboží](design-details-active-versus-historic-item-tracking-entries.md).

Následující diagram popisuje design funkce sledování zboží v [!INCLUDE[d365fin](includes/d365fin_md.md)].

![Příklad toku sledování zboží](media/design_details_item_tracking_design.png "Příklad toku sledování zboží")

Objekt centrálního účtování je přepracován tak, aby zpracovával jedinečnou subklasifikaci řádku dokladu ve formě sériových čísel nebo čísel šarží, a přidávají se speciální relační tabulky, které vytvářejí relace jedna k více mezi zaúčtovanými doklady a jejich položkami a hodnotami rozdělených položek položky hlavní knihy.

Codeunita 22, **Deník zboží – účtování řádku**, nyní rozdělí účtování podle čísel sledování zboží, která jsou zadaná na řádku dokladu. Každé jedinečné číslo sledování zboží na řádku vytvoří pro zboží vlastní položku zboží. To znamená, že propojení z řádku zaúčtovaného dokladu na přidružené položky zboží je nyní vztahem jedna k více. Tento vztah je zpracován následujícími tabulkami vztahů sledování zboží.

| Pole | Popis |
|---------------|---------------------------------------|  
| **Relace položky zboží** (T6507) | Spojuje dodané nebo přijaté řádky s položkami zboží. |
| **Relace položky ocenění** (T6508) | Spojuje fakturované řádky s položkami ocenění. |

Pro více informací navštivte [Detaily návrhu: Struktura účtování sledování zboží](design-details-item-tracking-posting-structure.md)

## Viz také
[Detaily návrhu: Sledování zboží](design-details-item-tracking.md)
