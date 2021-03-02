---
    title: Walkthrough - Conducting a Sales Campaign | Microsoft Docs
    description: A campaign is any kind of activity that involves several contacts. An important part of setting up a campaign involves selecting the target audience for your campaign. For this purpose, in Business Central, you create a segment, or a group of contacts using filters.
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
# Návod: Vedení prodejní kampaně
Kampaň je jakýkoli druh aktivity, který zahrnuje několik kontaktů. Důležitou součástí nastavení kampaně je výběr cílové skupiny pro vaši kampaň. Z tohoto důvodu v [!INCLUDE[prod_short](includes/prod_short.md)] vytvoříte pomocí filtrů segment nebo skupinu kontaktů.

Tyto funkce v oblasti Prodeje a marketingu používáte k pečlivému plánování svých marketingových aktivit a ke správě svých interakcí s kontakty a zákazníky. Můžete vytvářet kampaně a nastavovat segmenty kontaktů pro korespondenci a další typy interakcí s kontakty a potenciálními zákazníky.

Funkce Kampaně a segmentu s automatizovanými procesy umožňují plánovat, organizovat a sledovat vaše marketingové aktivity. Tím se zvýší šance na získání nových zákazníků a udržení stávajících zákazníků.

## Návod
Tento návod ukazuje proces sledování veletrhu a cílení na potenciální zákazníky (kontakty) v následné kampani.

Návod představuje funkci správy kampaní a segmentů v oddělení prodeje a marketingu. Tento návod ilustruje následující úkoly:

- Nastavení kampaně.
- Výběr cílové skupiny.
- Dolování dat.
- Odesílání dopisů kontaktům.
- Registrace odpovědí na kampaň.

## Role
Tento návod ukazuje úkoly, které jsou prováděny následujícími uživatelskými rolemi:

- Marketingový manažer nebo Manažer prodeje
- Marketingový pracovník

## Předpoklady
Než budete moci provést úkoly v tomto návodu, musíte si nainstalovat [!INCLUDE[prod_short](includes/prod_short.md)].

## Příběh
Marketingový manažer v obchodním oddělení CRONUS je zodpovědný za plánování kampaní a jejich provádění. Rovněž rozhoduje o tom, kterých veletrhů se má účastnit, a hodnotí postup kampaně.

Pracovník marketingu v marketingovém oddělení zpracovává produkci, distribuci a umisťování marketingových materiálů.

Společnost právě uvedla na trh nový produkt s názvem Millennium Server. Produkt byl nedávno propagován na veletrhu Computer Futurus. Mnoho zákazníků projevilo o produkt velký zájem a v rámci propagačního úsilí byla zákazníkům, kteří si během období kampaně zakoupili server Millennium Server, nabídnuta speciální cena.

Jedním z úkolů marketingového pracovníka po veletrhu je zadat všechny potenciální zákazníky jako kontakty.

Marketingový manažer nastaví kampaň, vytvoří segment, který obsahuje všechny nové kontakty, a poté vytěží kontaktní údaje, aby vybral cílové publikum pro kampaň.

Pracovník pomáhá rozesílat děkovné dopisy všem kontaktům, které zanechaly své karty zaměstnancům ve stánku, a nakonec manažer zaznamená všechny odpovědi, které obdrží od potenciálních zákazníků.

## Nastavení kampaně
Jakmile zaměstnanec vstoupí do vizitek přijatých na veletrhu, marketingový manažer nastaví kartu kampaně pro správu aktivit zapojených do kampaně.

### Nastavení kampaně

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kampaně** a poté vyberte související odkaz.
2. Chcete-li vytvořit novou kampaň, vyberte akci **Nový**. Na kartě kampaně stiskněte Enter, aby se číslo kampaně automaticky vložilo.
3. Do pole **Popis** zadejte popis kampaně, například **veletrh FUTURUS**.
4. Vyberte pole **Kód stavu** a vyberte stavový kód ze seznamu, který se otevře na stránce **Stav kampaně**.
5. Podle potřeby vyplňte pole **Počáteční datum** a **Koncové datum** kampaně.

## Výběr Cílové skupiny.
Marketingový manažer vytvoří segment pro výběr kontaktů, se kterými chce komunikovat.

### Vytvoření segmentu s příslušnými kontakty

1. Vyberte akci **Segmenty**.
2. Vyberte akci **Nový** a vytvořte nový segment. Na kartě segmentu stiskněte Enter, aby se číslo segmentu automaticky vložilo.
3. Na záložce **Obecné** zadejte do pole **Popis** například **Návštěvníci veletrhu FUTURUS**.

   Po zadání obecných informací o segmentu vyberte kontakty, které chcete do segmentu zahrnout.

   Můžete použít různá kritéria pro výběr kontaktů, například můžete vybrat kontaktní osoby, které pracují na webu zákazníka nebo potenciálního zákazníka, který je zodpovědný za nákupy ve své společnosti.

   Pomocí filtrů přidáváte kontakty podle kritérií, která nejlépe vyhovují vašim účelům. Můžete například filtrovat podle pracovní odpovědnosti kontaktní osoby nebo obchodního vztahu nebo odvětví kontaktní společnosti. V tomto návodu vyberte filtr **Pracovní odpovědnost** a vyberte kontakty.

4. Na stránce **Segment** vyberte akci **Přidat kontakty** a otevřete filtr **Přidat kontakty**.
5. Na záložce **Pracovní odpovědnost** vyberte filtr **Nákup** jako **Kód pracovní odpovědnosti** a klikněte na tlačítko **OK**.

   Stránka **Segment** nyní obsahuje seznam kontaktů na základě vámi zadaného filtru. Na záložce **Obecné** v poli **Počet  řádků** můžete na první pohled vidět počet kontaktů, které splňují tato kritéria.

   > [!NOTE]  
   > Kritéria segmentace můžete uložit, abyste je mohli později znovu použít.

   1. Na stránce **Segment** vyberte akci **Segment** a poté vyberte akci **Uložit kritéria**.
   2. Na stránce **Uložit kritéria segmentu** zadejte kód segmentu. Do pole **Popis** zadejte popis kritérií segmentu.
   3. Zvolte tlačítko **OK**.

## Dolování dat
Marketingový manažer se blíže podívá na segmentovaný seznam kontaktů a uvědomí si, že seznam je příliš velký. Rozhodne se snížit seznam na základě skutečných potenciálních zákazníků, aby se ujistil, že se zaměřuje na správnou cílovou skupinu. Tento proces rafinace a snížení dat se také označuje jako dolování dat.

### Odebrání kontaktů ze segmentu

1. Na stránce **Segment** vyberte akci **Kontakty** a poté akcí **Odebrat kontakty** otevřete stránku **Odstranit kontakty - odebrat**.
2. Na záložce **Obchodní vztah** vyberte filtr **POTENC** jako **Kód obchodního vztahu** a klikněte na tlačítko **OK**.

   Stránka **Segment** nyní obsahuje omezený seznam kontaktů a v poli **Počet  řádků** můžete vidět počet kontaktů, které nyní splňují tato nová kritéria.

   > [!NOTE]  
   > Pokud musíte toto odebrání skupiny kontaktů zvrátit, můžete to provést pomocí funkce **Zpět**. Jinými slovy, můžete vrátit zpět poslední segmentaci.
   >
   > Na stránce **Segment** vyberte akci **Segment** a poté vyberte akci **Zpět**.
   >
   > Kontakty, které jste právě odebrali, se přidají zpět do seznamu kontaktů.

## Propojení segmentu s kampaní
Marketingový manažer rozhodne, že zmenšený seznam je konečným seznamem kontaktů, které chce mít součástí kampaně. Proto tento segment spojuje s kampaní na veletrhu FUTURUS.

### Propojení segmentu s kampaní

1. Na stránce **Segment** na záložce **Campaň** vyberte pole **Číslo kampaně** a vyberte kampaň, ke které chcete segment připojit, například: **CP0001**.
2. Vzhledem k tomu, že cílem kampaně je tento segment, zaškrtněte políčko **Cíl kampaně**.

## Odesílání dopisů a e-mailových zpráv kontaktům
Marketingový zaměstnanec pomáhá marketingovému manažerovi rozesílat budoucím zákazníkům korespondenci, ve které jim děkuje za návštěvu veletrhu.

### Odeslání dopisu kontaktu pomocí segmentu

1. Otevřete kartu **Segment** pro **návštěvníky veletrhu FUTURUS**.
2. Na záložce **Interakce** v poli **Kód šablony interakce** vyberte šablonu Business Letter, kód **BUS**.
3. Do pole **Předmět (výchozí)** zadejte následující ukázkový text: **Děkujeme vám za návštěvu veletrhu**.

   > [!NOTE]  
   > Tato šablona se skládá z více než jednoho dokumentu přílohy, každý z nich je napsán v jiném jazyce. Mezi příklady jazyků patří angličtina a dánština.

4. Vyberte pole **Kód jazyka (výchozí)** a otevřete stránku **Jazyky segmentu interakce**. Vyberte kód jazyka a poté klikněte na tlačítko **OK**.
5. Dokument můžete zobrazit ve vybraném jazyce. Vyberte akci **Příloha** a poté vyberte akci **Otevřít**.

   Chcete-li odpovědět na zprávu, která požaduje povolení ke spuštění aplikace Word, vyberte možnost **Povolit pro tuto relaci klienta**.

   Tím se otevře připojený dokument aplikace Word, abyste jej mohli zkontrolovat. Při této příležitosti můžete také dopis upravit. Po dokončení zavřete Word.

6. Zadejte předmět dopisu do pole **Předmět** v jazyce vybraném pro šablonu.
7. Vyberte akci **Protokol**.
8. Zaškrtněte políčko **Poslat přílohy**, aby se přílohy vytiskly.

   1. Zaškrtněte políčko **Vytvořit segment sledování**.
   2. Kliknutím na tlačítko **OK** spustíte dávkovou úlohu **Protokolovat segment**.

9. Přílohy jsou odeslány. Po dokončení procesu vyberte tlačítko **OK**, které uvádí, že segment byl zaznamenán.

   Listy se automaticky vytisknou a segment se zaprotokoluje. Protože segment byl zaprotokolován, již není v seznamu segmentů, ale je přesunut do seznamu protokolovaných segmentů. Chcete-li tento seznam zobrazit, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Protokolované segmenty** a poté vyberte související odkaz.

10. Po zaprotokolování segmentu je každý odeslaný list zaznamenán jako interakce, kterou můžete zobrazit v protokolu.

   Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky protokolu interakce** a poté vyberte související odkaz. Pro každý odeslaný dopis je k dispozici položka.

### Odeslání e-mailové zprávy kontaktu

1. Na záložce **Interakce** v poli **Kód šablony interakce** vyberte šablonu Business Letter, kód **BUS**.
2. Do pole **Předmět (výchozí)** zadejte následující ukázkový text: **Děkujeme vám za návštěvu veletrhu**.
3. V poli **Typ korespondence** vyberte možnost **E-mail**.
4. Zadejte nastavení jazyka, jako v předchozím postupu.
5. Vyberte akci **Protokol**. Otevře se stránka **Protokolovat segment**.
6. Zaškrtněte políčko **Poslat přílohy**, aby se přílohy odesílaly e-mailem.
7. Zaškrtněte políčko **Vytvořit segment sledování**.
8. Zvolte tlačítko **OK**.

   Dopisy jsou automaticky odesílány e-mailem a segment je zaprotokolován. Protože segment byl zaprotokolován, již není v seznamu segmentů, ale je uložen v seznamu protokolovaných segmentů. Chcete-li tento seznam zobrazit, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Protokolované segmenty** a poté vyberte související odkaz.

## Registrace odpovědí na kampaň
Během příštích několika týdnů budou potenciální zákazníci na dopis reagovat. Marketingový manažer chce sledovat odpovědi a zaznamenávat tyto interakce.

Za tímto účelem vytvořte segment pro kontakty, které na dopis odpověděly.

### Registrace odpovědí na kampaň

1. Na stránce **Segment** rozbalte záložku **Interakce**.
2. Vyberte pole **Kód šablony interakce**.

   Neexistuje žádná šablona interakce pro zaznamenávání odpovědí na kampaně. Proto vytvořte novou šablonu.

3. Na stránce **Šablony interakce** vyberte akci **Nový**.
4. Do pole **Kód** zadejte **RESP** a do pole **Popis** field, zadejte **Odpovědi kampaně**.
5. Zvolte tlačítko **OK**.
6. Vyberte tuto šablonu interakce v poli **Kód šablony interakce** a potvrďte zprávu s dotazem, zda chcete aktualizovat řádky segmentu stejným kódem šablony interakce.

   Nyní zadejte, že tyto kontakty odpověděly na kampaň:
7. Na záložce **Kampaň** v poli **Číslo kampaně** vyberte svou kampaň.
8. Ponechte pole **Číslo kampaně** a potvrďte zprávu s dotazem, zda chcete aktualizovat řádky segmentů stejným kódem šablony interakce.
9. Vyberte pole **Odpověď na kampaň** a potvrďte následující zprávu.

   Zaprotokolujte segment a ujistěte se, že jsou zaznamenány interakce.
10. Na stránce **Segment** vyberte akci **Protokol**.
11. Na stránce **Protokolovat segment** zrušte zaškrtnutí políčka **Poslat přílohy**, klikněte na tlačítko **OK** a potvrďte zobrazenou zprávu.

   Po zaznamenání segmentu se automaticky vytvoří záznam pro kampaň, který tuto akci zaznamená na stránce **Položky kampaně**.

## Viz také
[Řízení vztahů](marketing-relationship-management.md)    
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]