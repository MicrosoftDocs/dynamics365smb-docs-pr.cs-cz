---
    title: Walkthrough - Planning Supplies Manually | Microsoft Docs
    description: This walkthrough demonstrates the process of planning supply orders to fulfill new demand. You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.
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
# Návod: Ruční plánování dodávek

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

Tento návod ukazuje proces plánování dodávek na uspokojení nové poptávky. Plánování dodávek můžete iniciovat v pevných intervalech, například každé ráno nebo každé pondělí, nebo když jste upozorněni prodejem nebo výrobou v závislosti na typu poptávky. V tomto návodu použijete stránku **Plánování objednávek**, jednoduchý nástroj pro plánování zásobování, který je založen na manuálním rozhodování místo na automatickém plánování založeném na parametrech.

## Návod
Tento návod ilustruje následující úkoly:

- Plánování nákupní objednávky pro výrobu komponentů.
- Plánování objednávky transferu pro splnění prodejní poptávky.
- Plánování výrobní zakázky pro víceúrovňové zboží.

## Role
Tento návod ukazuje úkoly, které jsou prováděny následujícími uživatelskými rolemi:

- Výrobní plánovač
- Nákupní agent
- Zpracovatel prodejní objednávky

## Předpoklady
Než začnete s tímto návodem, musíte si nainstalovat [!INCLUDE[prod_short](includes/prod_short.md)]. V databázi musí být provedeny následující změny:

- Odstraňte všechny existující prodejní objednávky jízdních kol.
- Vytvořte jednu prodejní objednávku na 10 jízdních kol na lokaci EAST.
- Odstraňte všechny plánované a pevně plánované výrobní zakázky. Neodstraňujte spuštěné objednávky s položkami, které jsou již zaúčtovány.

Zpravidla použijte navrhovaná data v tomto návodu, protože tato data mají potřebné záznamy.

## Příběh
Eduardo, plánovač výroby malé výrobní společnosti, se chystá plánovat výrobní a nákupní objednávky, aby uspokojil novou poptávku po prodeji.

Protože produkty mají několik úrovní kusovníku a tok objednávek je relativně nízký, používá Eduardo stránku **Plánování objednávek** k ručnímu vytváření objednávek dodávek po jedné úrovni produktu.

Ve složitějším výrobním prostředí se plánovací sešit používá k plánování nabídky na základě parametrů položky, jako je období přeplánování, doba vedení bezpečnosti, bod přiobjednání a dávkové výpočty konsolidované poptávky ze všech úrovní produktu.

## Nastavení ukázkových dat
Standardní demonstrační společnost CRONUS má v současné době spoustu neplánovaných požadavků. Během různých plánovacích úkolů v tomto návodu se budete muset odchýlit od realistického obchodního toku ignorováním poptávky s blízkými daty splatnosti a místo toho použít poptávku s pozdějšími daty splatnosti.

## Použití stránky Plánování objednávek

Na stránku **Plánování objednávek** lze přistupovat z několika různých míst:

- Výroba, Plánování
- Prodej a marketing, Zpracování objednávek
- Nákup, Plánování
- Kromě toho můžete tuto stránku otevřít pro konkrétní výrobní zakázku výběrem akce **Plánování**.

### Použití stránky Plánování objednávek

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Plánování objednávek** a poté vyberte související odkaz.

   Když se nejprve otevře stránka **Plánování objednávek**, je třeba vypočítat plán, aby se zobrazila nová poptávka od posledního výpočtu.

2. Vyberte akci **Vypočítat plán**.

   Systém plánování analyzuje každou novou poptávku, která byla zavedena, například nový prodej, změněný prodej nebo výrobní zakázky.

   Na základě celkové dostupnosti se vypočítá množství potřebné pro každý řádek poptávky. Tento výpočet se provádí po jednotlivých objednávkách. To znamená, že jako první bude vypočítána objednávka, která obsahuje řádek poptávky s nejbližším datem splatnosti nebo datem odeslání. Poté budou další řádky poptávky vypočítány ve stejné objednávce bez ohledu na datum splatnosti nebo datum odeslání.

3. Ujistěte se, že je stránka **Plánování objednávek** maximalizována a že velikost sloupců polí se změní tak, aby zobrazovala všechny výchozí názvy polí.

   Po dokončení výpočtu stránka zobrazí všechny nesplněné požadavky jako sbalené řádky záhlaví objednávky seřazené podle nejbližšího data poptávky.

   Všimněte si, že CRONUS má několik objednávek s nesplněnou poptávkou. Každý tučný řádek plánování představuje objednávku, prodejní objednávku nebo výrobní zakázku, včetně alespoň jednoho řádku objednávky s nedostatečnou dostupností.

4. V poli **Zobrazit poptávku jako** vyberte filtr **Veškerá poptávka**.

   V poli **Typ poptávky** můžete zvolit, jaké typy objednávek chcete zobrazit.

   Objednávky, které nemají problémy s dostupností, se nezobrazí. Pokud při výpočtu plánu neexistují žádné objednávky, zobrazí se zpráva a nezobrazí se žádné plánovací řádky.

## Plánování nákupní objednávky k uspokojení poptávky po komponentách
V tomto postupu vytvoříte nákupní objednávku pro potřebné výrobní komponenty.

### Plánování nákupní objednávky pro splnění potřeby komponent ve výrobě

1. Rozbalte první řádek (vyberte symbol +).
2. Vyberte první řádek poptávky se zbožím **LSU-15** a poté vyberte akci **Zobrazit doklad**.
3. Zavřete otevřenou výrobní zakázku a vraťte se na stránku **Plánování objednávek**.
4. V poli **Systém doplnění** vyberte **Nákup**.

   Výchozí hodnota je z karty zboží nebo karty SKJ, ale můžete ji změnit na jednu z následujících možností:

   - **Nákup** – Chcete-li vytvořit nákupní objednávku.
   - **Transfer** – Chcete-li vytvořit objednávku transferu.
   - **Výr. zakázka** – Chcete-li vytvořit výrobní zakázku.

5. V poli **Dodávka od** vyberte jednu z následujících možností podle vybraného doplňovacího systému:

   - **Dodavatel** – pro nákupy
   - **Lokace** - pro transfery

   Pokud pole není vyplněno, zobrazí se při pokusu o vytvoření zásobovacích objednávek chybová zpráva.

   > [!NOTE]  
   > Pokud mají komponenty na kartách položek nastaveno výchozí číslo dodavatele, budou řádky přednastaveny.

6. Vyberte pole **Dodávka od**.
7. Na stránce **Katalog dodavatelů zboží** vyberte akci **Nový** a poté vyberte dodavatele **30000**.
8. Kliknutím na tlačítko **OK** se vrátíte na stránku **Plánování objednávek**.
9. Zkopírujte dodavatele **30000** na další řádky pro komponenty v této výrobní zakázce.

   Nyní jste připraveni vytvořit nákupní objednávku.

10. Vyberte akci **Vytvořit objednávky**. Otevře se stránka **Vytvořit objednávky dodávek**.
11. Na záložce **Plánování objednávek** vyberte v poli **Vytvořit objednávky pro** možnost **Aktivní objednávka**.
12. Na záložce **Možnosti** v poli **Vytvořit nákupní objednávku** vyberte možnost **Vytvořit nák. objednávky**.
13. Kliknutím na tlačítko **OK** vytvoříte nákupní objednávky pro všechny součásti objednávky.

   Nákupní objednávky jsou nyní vytvořeny a uloženy jako poslední objednávky v seznamu nákupních objednávek.

## Plánování objednávky transferu pro splnění prodejní poptávky
V tomto postupu naplánujte poptávku z prodejní objednávky. Řádky poptávky představují prodejní řádky, nikoli řádky komponent, jako je tomu v případě poptávky po výrobě.

### Plánování objednávky transferu pro splnění prodejní poptávky

1. Přesuňte ukazatel na plánovací řádek pro objednávku **2008**.
2. Rozbalte řádek a přesuňte ukazatel na řádek poptávky.

   Prodejní objednávka **2008** je pro deset reproduktorů, zboží **LS-120**, objednané společností UNIVERSAL-TREND a.s.

   Zobrazí se definovaný doplňovací systém zboží a výchozího prodejce.

   > [!NOTE]  
   > Ve spodní části stránky jsou čtyři informační pole. V poli **Nejbližší dostupné datum** bude k dispozici deset kusů, které jsou potřeba, u příchozí objednávky dodávky, o devět dní později než aktuální datum splatnosti. Pokud je pro zákazníka příliš pozdě, pole **K dispozici pro transfer** zobrazuje 13 kusů zboží na jiné lokaci. Tuto akci budete chtít naplánovat.

3. Vyberte pole **K dispozici pro transfer** a otevřete stránku **Získat alternativní dodávku**.
4. Kliknutím na tlačítko **OK** zarezervujete deset dostupných položek.

   > [!NOTE]  
   > V řádku poptávky byl navržený nákup vyměněn s převodem z HLAVNÍ lokace. Funkce **Vytvořit objednávky** vytvoří převodní příkaz z HLAVNÍ do požadované lokace. Pole **Existuje náhrada** funguje stejným způsobem.

5. Vyberte akci **Vytvořit objednávky**. Otevře se stránka **Vytvořit objednávky dodávek**.
6. Na záložce **Plánování objednávek** vyberte v poli **Vytvořit objednávky pro** možnost **Aktivní objednávka**.
7. Na záložce **Možnosti** v poli **Vytvořit objednávku transferu** vyberte možnost **Vytvořit objednávky  transferu**.
8. Zvolte tlačítko **OK** a vytvořte objednávku transferu, která dodá prodejní objednávku.

   Převodní příkaz je nyní vytvořen a uložen v seznamu jako poslední objednávka v seznamu otevřených objednávkach transferu.

## Plánování víceúrovňové výrobní zakázky pro splnění prodejní poptávky
V tomto postupu budete plánovat, jak uspokojit prodejní poptávku po vyrobeném zboží s více úrovněmi produktu, přičemž každá vytvoří závislou výrobní poptávku.

### Plánování víceúrovňové výroby pro splnění prodejní poptávky

1. Vyberte řádek plánování s prodejní poptávkou pro objednávku **1001**, vytvořený dříve jako data požadavků.

   Tato poptávka je řádek prodeje, ale zboží má definovaný doplňovací systém **Výr. zakázka**. Pokračujte přidáním dalšího zvonku k potřebným komponentám každého kola.

2. Výběrem akce **Komponenty** otevřete stránku **Plánované komponenty**.
3. Na řádku s položkou Zvonek změňte pole **Množství za** z hodnoty **1** na **2**.
4. Na stránce **Plánování objednávek** zvažte alternativy plánování. V tomto případě nemáte žádné alternativní způsoby dodání, žádný transfer, náhradní nebo pozdější doručení. Je nutné vytvořit navrhovanou objednávku dodávky, výrobní zakázku.
5. Zvolte akci **Vytvořit objednávky** a vytvořte výrobní zakázku.

   Na stránce **Plánování objednávek** si všimněte, že plánovací řádek pro prodejní objednávku **1001** již neexistuje a že byla pokryta počáteční poptávka.

6. Zavřete stránku **Plánování objednávek**.

   Nyní byste se mohli rozhodnout zůstat v tomto zobrazení a dokončit všechny plánovací úkoly. Místo toho nyní převezmete roli plánovače výroby tím, že přejdete na produkční zakázku, kterou jste právě vytvořili, a přejdete na stránku **Plánování objednávek**.

Jako plánovač výroby nyní musíte naplánovat konkrétní výrobní zakázku.

### Plánování konkrétní výrobní zakázky

1. Otevřete výrobní zakázku **101001** pro deset jízdních kol, kterou jste právě vytvořili pomocí funkce **Vytvořit objednávky**.
2. Otevřete stránku **Komponenty  výrobní zakázky** a zkontrolujte, zda se zvláštní zvonek projeví ve výrobní zakázce.
3. Vyberte akci **Plánování**.

   Stránka **Plánování objednávek** se otevře v zobrazení, které je vždy filtrováno podle konkrétní poptávky po produkci. Prodejní poptávka není zobrazena. Před tím, než uvidíte další požadavky, je nutné vypočítat plán.

4. Vyberte akci **Vypočítat plán**.

   Všimněte si, že čtyři nové výrobní zakázky se zobrazují jako neplánovaná výrobní poptávka odvozená od objednávky **101001**. Nové řádky představují novou výrobní poptávku z podsestav, které je třeba vytvořit, aby byla zakázka vyrobena.

5. Zvolte akci **Rozbalit vše**, abyste získali přehled o všech produkčních poptávkách po výrobních objednávkách.

   Chcete-li poskytnout další informace o řádcích poptávky, můžete přidat pole **Množství poptávky** a **Dostupné množství  poptávky** do vašeho zobrazení.

   Nyní musíte dodat deset kusů z každé komponenty.

   Všimněte si, že čtyři řádky poptávky mají systém doplnění Výr. zakázka. Tyto čtyři podsestavy představují druhou úroveň produktu jízdního kola.

   Výchozí nastavení doplnění je již vyplněno a můžete pokračovat v objednávce.

6. Vyberte akci **Vytvořit objednávky**.

   Než kliknete na tlačítko **OK**, všimněte si textu na záložce **Plánování objednávek**. Tento text je důležitý, protože víte, že jízdní kolo má ve své produktové struktuře několik vyrobených komponent, podsestav, které mohou být při vytváření této výrobní zakázky žádané.

7. Na stránce **Vytvořit objednávky dodávek** v poli **Vytvořit objednávky pro** vyberte možnost **Všechny řádky** a poté klikněte na tlačítko **OK** k vytvoření produkčních objednávek pro druhou úroveň produktu objednávky.

   Všimněte si, že nejvyšší výrobní poptávka po výrobní zakázce 101001 již neexistuje. To znamená, že počáteční poptávka po výrobě podsestav byla plánována.

   Na stránce **Plánování objednávek** vypočítáte plán znovu, abyste mohli naplánovat strukturu kola.

8. Vyberte akci **Vypočítat plán** a přepočítejte plán podle pokynů vloženého textu nápovědy.

   Dva nové řádky představují další poptávku po produkci odvozenou z podsestav plánovaných v předchozích krocích. Navrhuje se, abyste pro dodávku nábojů kol udělali dvě výrobní zakázky, jednu pro 10 předních nábojů a jednu pro 10 zadních nábojů.

9. Zvolte akci **Rozbalit vše**, abyste získali přehled o veškeré poptávce po dvou produkčních objednávkách.

   Navrhovaný plán dodávek naznačuje, že pro komponenty budou vytvořeny celkem čtyři nákupní objednávky. Rozhodnete se provést navrhované objednávky.

10. Vyberte akci **Vytvořit objednávky**.
11. V poli **Vytvořit objednávky pro** vyberte možnost **Všechny řádky**a klikněte na tlačítko **OK**. Zkontrolujte, zda existuje další poptávka po výrobě nadřazeného zboží, jízdního kola, které se prodává na prodejní objednávce 1001.
12. Vyberte akci **Vypočítat plán**.

   Zpráva označuje, že je nyní dodáno všechno požadované zboží. Ověření firmou plánovaných výrobních zakázek, které jsou vytvořeny.

13. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pevně plánovaná výr. zakázka** a poté vyberte související odkaz.

   Na stránce **Pevně plánovaná výr. zakázka** zkontrolujte, jak jsou podle struktury produktu naplánovány počáteční a konečné časy jednotlivých objednávek. Komponenty nejnižší úrovně jsou vyráběny jako první. Proto je nutné naplánovat víceúrovňové objednávky, jak je znázorněno v tomto pracovním postupu plánování.

## Viz také
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)     
[Návod: Automatické plánování dodávek](walkthrough-planning-supplies-automatically.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]