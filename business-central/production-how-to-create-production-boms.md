---
    title: How to Create Production BOMs | Microsoft Docs
    description: A production BOM holds master data that describes the components and subassemblies used in the production of a parent item. Once a production order is created for that parent item, its production BOM will govern the calculation of material requirements as represented on the **Prod. Order Components** page.
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
# Vytvoření výrobních kusovníků
Výrobní kusovník uchovává hlavní data popisující komponenty a sestavení použité při výrobě nadřízeného zboží. Jakmile je pro toto nadřazené zboží vytvořena výrobní zakázka, bude její výrobní kusovník řídit výpočet požadavků na materiál, jak je znázorněno na řádku **Komponenty  výrobní zakázky**.

[!INCLUDE[d365fin](includes/d365fin_md.md)] také podporuje kusovníky montáže. Montážní zakázky slouží k provádění koncového zboží z komponent v jednoduchém procesu, který lze provést jedním nebo více základními zdroji, které nejsou strojním nebo pracovním střediskem, nebo bez jakýchkoli prostředků. Proces montáže by například mohl být, z výběru dvou láhví vína a jednoho pytlíku kávy a následného zabalení jako dárek. Pro více informací navštivte [Výrobní kusovníky a kusobníky montáže](inventory-how-work-boms.md#assembly-boms-or-production-boms).

Dříve než můžete TNG postup založit, musí být nastaveno následující:

- Karty zboží se vytvářejí pro nadřazené položky, které se podílejí na výrobě. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).
- Jsou nastaveny výrobní zdroje. Pro více informací navštivte [Nastavení pracovních center a strojních center](production-how-to-set-up-work-and-machine-centers.md)

## Vytvoření výrobních kusovníků
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kusovník** a poté vyberte související odkaz.
2. Vyberte tlačítko **Nový**.
3. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Pro úpravy kusovníku nastavte **Stav** na **Nový** nebo **Ve vývoji**. Chcete-li jej aktivovat, nastavte pole **Stav** na **Certifikováno**.

   Pokračujte vyplněním řádků výrobního kusovníku.
5. V poli **Typ** vyberte, zda je zboží v tomto řádku kusovníku běžným zbožím nebo výrobním kusovníkem. Pokud je zboží na řádku výrobní kusovník, musí již existovat jako certifikovaný.
6. V poli **Číslo** vyhledejte a vyberte příslušné zboží, výrobní kusovník nebo jej zadejte do pole.
7. Do pole **Množství za** zadejte, kolik jednotek zboží přejde do nadřazeného zboží, například 4 kola pro 1 auto.
8. Do pole **Zmetky%** můžete zadat pevné procento komponent vyřazených během výroby. Jakmile jsou komponenty připraveny k spotřebě ve vydané výrobní zakázce, bude toto procento přidáno k očekávanému množství v poli **Množství spotřeby** ve deníku výroby. Pro více informací navštivte [Evidence spotřeby a výstupu](production-how-to-register-consumption-and-output.md).

   > [!NOTE]
   > Toto procento šrotu představuje komponenty, které jsou vyřazeny během výroby při výběru ze zásob, zatímco procento šrotu na směrovacích linkách představuje vyřazený výstup před uvedením na sklad.

9. V poli **Kód vazby TNG** zadejte kód pro připojení komponenty k určité operaci. Pro více informací navštivte [Vytvoření TNG vazeb](production-how-to-create-routings.md#to-create-routing-links).
10. Chcete-li kopírovat řádky z existujícího výrobního kusovníku, zvolte položku **Kopie kusovníku** a vyberte existující řádky.
11. Certifikace výrobního kusovníku
12. Nyní můžete připojit nový výrobní kusovník ke kartě příslušného nadřazeného zboží. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).

> [!NOTE]
>  Chcete-li přepočítat standardní cenu zboží z karty zboží, vyberte tlačítko **Výroba** a poté **Výpočet  pevné pořizovací ceny**.

## Vytvoření nových verzí výrobního kusovníku
Nové verze výrobních kusovníků se používají například tehdy, když je zboží nahrazeno jinou položkou, nebo když zákazník vyžaduje speciální verzi produktu. Princip verze umožňuje spravovat různé verze výrobního kusovníku. Struktura verze výrobního kusovníku odpovídá struktuře výrobního kusovníku. Základní rozdíl je v době platnosti verzí. Platnost je definována počátečním datem.

Počáteční datum označuje začátek období, ve kterém je tato verze platná. Pro všechny ostatní úvahy je počáteční datum filtrovacím kritériem pro výpočty a vyhodnocení. Verze kusovníku je platná až do doby, kdy další verze začne platit pro nové počáteční datum.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kusovník** a poté vyberte související odkaz.
2. Vyberte výrobní kusovník, který se má zkopírovat, a pak zvolte tlačítko **Verze**.
3. V záložce **Domovská stránka ** ve skupině **Nový** vyberte tlačítko **Nový** .
4. Vyplňte pole podle potřeby.
5. Do pole **Kód verze** zadejte jedinečný identifikátor pro danou verzi. Je povolena jakákoli kombinace číslic a písmen.

   Nově vytvořené verzi se automaticky přiřadí stav **Nový** .
6. Po dokončení verze kusovníku nastavte pole **Stav** na **Certifikovaný**.

Časová platnost verze je určena políčkem **Počáteční datum**.

> [!NOTE]
>  Vyberte možnost **Zboží** v poli **Typ** a použijte zboží z kmenových dat vašeho zboží ve výrobním kusovníku. Pokud má položka také kusovník, přičemž na kartě zboží je vyplněno pole **Výrobní kusovník č.**, bude se také uvažovat o tomto kusovníku výroby.
> Pokud chcete na řádku použít Fantom **Výrobního kusovník**, vyberte možnost kusovník.
> Fantom kusovníky slouží ke strukturování produktů. Tento typ výrobního kusovníku nikdy nevede k hotovému produktu, ale používá se výhradně k určení závislého požadavku. Fantom kusovníky nemají vlastní kmenová data zboží.

## Vzorec pro výpočet množství na kusovnících
Množství se počítá s přihlédnutím k různým rozměrům, které jsou také zadávány na výrobních kusovnících. Rozměry se vztahují k objednávkové jednotce příslušného zboží. Délku, šířku, hloubku a hmotnost lze zadat jako rozměry.

Sloupce vzorec výpočtu, délka, šířka, hloubka a hmotnost nejsou zobrazeny, protože je používají pouze někteří uživatelé. Pokud chcete použít výpočet množství, musíte tyto sloupce nejprve zobrazit.

Vztah jednotlivých komponent je definován vzorcem výpočtu. Jako vzorec pro výpočet jsou k dispozici následující možnosti:

- **Prázdné** - Bez ohledu na rozměry. (Množství = Množství za)
- **Délka** - Množství = Množství za * Délka
- **Délka x Šířka** - Množství = Množství za * Délka x Šířka
- **Délka x Šířka x Hloubka** - Množství = Množství za x Délka x Šířka x Hloubka
- **Hmotnost** - Množství = Množství za x Hmotnost

### Příklad
Ve výrobním kusovníku je vyžadováno sedmdesát kovových dílů s rozměry: Délka = 0,20m na Šířka = 0,15m. Hodnoty se zadávají následovně: Vzorec výpočtu = délka x šířka, délka = 20, šířka = 15, množství = 70. Množství je dáno množstvím za * délka * šířka, tj. Množství = 70 x 0,20 m x 0,15 m = 2,1 m2.

## Viz také
[Vytvoření TNG postupů](production-how-to-create-routings.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroby](production-manage-manufacturing.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s  [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
