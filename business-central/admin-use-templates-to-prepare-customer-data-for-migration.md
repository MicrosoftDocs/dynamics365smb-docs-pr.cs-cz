---
    title: Prepare Customer Data Migration | Microsoft Docs
    description: After you import and apply setup data in the new database, you can start migrating the customer’s existing master data, such as item and customer numbers and names. To make sure that this data is created quickly and accurately in the new company, you should use templates to structure the data.
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
# Příprava na migraci zákaznických dat
Po importu a použití dat nastavení v nové databázi můžete začít migrovat existující hlavní data zákazníka, například čísla a názvy zákazníků. Chcete-li se ujistit, že se tato data v nové společnosti vytvářejí rychle a přesně, měli byste je strukturovat pomocí šablon.

Obvykle vytvoříte datové šablony pro následující tabulky hlavních dat:

- **Kontakty**
- **Zákazníci**
- **Zboží**
- **Dodavatelé**

Můžete však vytvořit strukturu šablony a použít ji na libovolnou tabulku v [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!TIP]
> Můžete také použít datové šablony pro každodenní operace k vytvoření nových záznamů založených na šablonách. Tyto datové šablony fungují pouze pro podporované tabulky hlavních dat. Pro více informací navštivte [Evidence nového zboží].

Při importu zákaznických dat, například u zboží, ze souboru jsou povinná pole, která jste zadali, převzata z propojené datové šablony. Když vytvoříte nové zboží, zadáte pouze obecné informace, jako je název, popis a cena, a poté shromáždíte zbývající data povinného pole z vybrané datové šablony.

Při vytváření nového záznamu kmenových dat, například zákaznické karty, jsou některá pole povinná a musí být vyplněna. Můžete seskupovat většinu povinných polí, jako jsou například účto skupiny a platební podmínky, aby bylo vytváření záznamů hlavních dat snazší a stabilnější. Můžete například seskupit povinná pole pro tabulku 18, pro typy **Zákazníků**, jako jsou **Domácí** , **Zahraniční** nebo **Exportní**.

## Výběr datové šablony
Když vyberete existující datovou šablonu, musíte posoudit, zda šablony, které jste vytvořili pro novou společnost, jsou pro zákazníka dostačující. Zkontrolujte poskytnutá pole a hodnoty a určete, které šablony jsou vhodné pro novou společnost.

> [!TIP]
> Můžete také použít datové šablony pro rychlé vytvoření nových záznamů.. Používejte je k rychlejšímu a přesnějšímu vytváření dat. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit konfigurace** a poté vyberte související odkaz.
2. Na stránce **Šablony konfigurace** vyberte ze seznamu datovou šablonu a poté vyberte akci **Upravit**.

Pokud výchozí šablony nesplňují vaše potřeby, můžete vytvořit nové šablony nebo přidat pole do existující šablony. Pokud jsou výchozí šablony dostatečné, můžete je použít k vytvoření záznamů na základě šablon kmenových dat.

## Vytvoření nové datové šablony
Pokud výchozí šablony neodpovídají potřebám nové společnosti, můžete vytvořit novou datovou šablonu. Pokud vytváříte více než jednu, může být užitečné přijmout konvenci pojmenování pro pole **Kód**.

Každá šablona se skládá z hlavičky a řádků. Když vytvoříte šablonu, můžete určit, která pole mají být vždy použita pro data určitého typu. Můžete například vytvořit různé šablony zákazníků, které se použijí na různé typy zákazníků. Když vytvoříte zákazníka pomocí šablony, můžete použít data šablony k předběžnému vyplnění určitých polí.

### Kopírování existující datové šablony
Novou šablonu dat můžete rychle vytvořit zkopírováním informací z existující šablony dat, kterou potom upravíte.

1. Otevřete stránku **Konfigurační šablony**.
2. Vyberte tlačítko **Nový**.
3. Vyplňte pole **Kód**.
4. Zvolte tlačítko **Kopírovat konfig. šablonu**.
5. Na stránce **Konfigurační šablony**, vyberte existující šablonu, kteoru chcete kopírovat a poté zbolte talčítko **OK**.

ID tabulky, název tabulky a řádky existující šablony dat jsou vloženy do nové šablony.

### Ruční vytvoření záhlaví šablony dat
1. Otevřete stránku **Konfigurační šablony**.
2. Vyberte tlačítko **Nový**.
3. Vyplňte pole **Kód**.
3. Do pole **ID tabulky** zadejte tabulku, na kterou se tato šablona vztahuje. Pole **Název tabulky** se vyplní automaticky, když je nastaveno pole **ID tabulky**.

### Ruční vytvoření řádku šablony dat
1. Na prvním řádku vyberte pole **Název pole**. Na stránce **Seznam polí** se zobrazí seznam polí v tabulce.
2. Vyberte pole a pak klepněte na tlačítko **OK**. Pole **Titutelk pole** je vyplněno názvem pole.
3. Do pole **Výchozí hodnota** zadejte příslušnou hodnotu. V některých případech je vhodné použít hodnotu, která není hodnotou dostupnou v databázi. V takovém případě můžete zaškrtnout políčko **Přeskočit kontrolu vztahů**, aby bylo možné použít data bez chyb.

   > [!TIP]
   > Protože pole **Výchozí hodnota** nemá náhled odpovídající volby pole v [!INCLUDE[d365fin](includes/d365fin_md.md)], zkopírujte a vložte požadovanou hodnotu ze související stránky do šablony.

4. Zaškrtněte políčko **Povinné** pokud uživatelé musí vyplnit příslušné pole.

   > [!NOTE]
   > Zaškrtávací políčko je pouze informativní. Není vynucena žádná obchodní logika. Například uživatelé nemohou zaúčtovat fakturu, pokud nebyly vytvořeny účto skupny. Zaškrtnutím políčka **Povinné** pro tato pole můžete vybrat, aby je uživatel vyplnil, a předejít tak chybě účtování později.
5. Do pole **Reference** zadejte informace o poli podle potřeby.
6. Klikněte na tlačítko **OK**.

## Export do šablony do aplikace Excel
Můžete vytvořit sešit aplikace Excel, který bude sloužit jako šablona, která se rychle zakládá na struktuře existující databázové tabulky. Poté můžete pomocí šablony shromáždit údaje o zákaznících v konzistentním formátu pro pozdější import do [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit konfigurace** a poté vyberte související odkaz.
2. Přidejte tabulku do seznamu nebo vyberte existující tabulku. Pro více informací navštivte [Správa společnosti v Sešitu konfiguraceu](admin-how-to-manage-company-configuration-in-a-worksheet.md).
3. Definujte pole z tabulky, která chcete zahrnout do šablony.
4. Vyberte tlačítko **Export do šablony**.
5. Pojmenujte a uložte soubor aplikace Excel. Sešit aplikace Excel se automaticky otevře.

Nyní můžete zadat údaje o zákaznících do sešitu aplikace Excel. Pokud jste exportovali více tabulek, bude každá tabulka na samostatném listu. Před dalším postupem uložte sešit.

> [!NOTE]
> Při spuštění anglické verze aplikace Excel se může objevit následující chyba, ale vaše místní nastavení je nakonfigurováno pro neanglický jazyk: „Starý formát nebo knihovna neplatných typů.“ Chcete-li tuto chybu opravit, ujistěte se, že je nainstalován jazykový balíček pro neanglický jazyk.

## Import ze šablony v aplikaci Excel
1. Na stránce **Sešitu konfigurace** a potom vyberte tlačítko **Import z šablony**.
3. Přejděte na vytvořený list šablony a vyberte akci **Otevřít**.
4. Chcete-li shromážděná data zákazníků přidat do databáze, vyberte akci **Použít data**.

Použijete-li data ze šablony aplikace Excel do tabulky, ve které je také Šablona konfigurace s touto šablonou propojena v konfiguračním balíčku, budou použity také výchozí hodnoty polí z šablony konfigurace.

Každý záznam, jehož data jsou použita tímto způsobem, je úplný, protože se skládá z dat zadaných uživatelem v Excelu plus výchozích hodnot určených konfigurační šablonou.

## Vytvoření záznamu z konfigurační šablony
Strukturu dat obsaženou v šablonách dat můžete použít k převedení informací na záznamy v databázi, jeden po jednom. Chcete-li tak učinit, použijte funkci **Vytvořit instanci** . Jedná se o miniaturní verzi procesu migrace dat, která může být užitečná při vytváření prototypů nebo zpracování menších úloh vytvoření dat.

Následující kroky popisují, jak vytvořit kartu zboží z šablony zboží. Stejným postupem můžete vytvořit záznam z libovolné datové šablony.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit konfigurace** a poté vyberte související odkaz.
2. Vyberte šablonu **Zboží** a poté vyberte tlačítko **Upravit**. Pro více informací navštivte [Příprava na migraci zákaznických dat](admin-use-templates-to-prepare-customer-data-for-migration.md#to-create-a-new-data-template).
3. Vyberte tlačítko **Vytvořit Instanci**. Vytvoří se karta zboží.
4. Klikněte na tlačítko **OK**.
5. Ke kontrole nové karty zboží, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
6. Otevřete novou kartu zboží.
7. Rozbalte záložky s náhledem a ověřte, zda byly informace na nich správně vytvořeny.

## Použití konfigurační šablony na záznamu
Šablonu dat můžete použít u všech záznamů v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)] a pomocí této techniky můžete změnit nebo upravit záznam. Když to však uděláte, přepíšete stávající hodnoty v záznamu hodnotami šablony. Proto byste měli být opatrní při použití šablony nad existujícími záznamy.

> [!WARNING]
> Funkce **Použít šablonu** přepíše existující data záznamu. Pokud je tato funkce použita při migraci kmenových dat, přepíše importovaná data při vytváření záznamů.

Následující postup je založen na nové kartě zákazníka.

1. Vytvoření zákazníka. Pro více informací navštivte [Evidence nových zákazníků](sales-how-register-new-customers.md).
2. Na stránce **Karta zákazníka** vyberte akci **Použít šablonu**.
3. Na stránce **Šablony zákazníků** vyberte jednu ze šablon a poté vyberte tlačítko **OK**.

Výchozí hodnoty z vybrané zákaznické šablony jsou vloženy na kartu zákazníka.

## Viz také
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)
[Administrace](admin-setup-and-administration.md)
[Evidence nových zákazníků](sales-how-register-new-customers.md)
