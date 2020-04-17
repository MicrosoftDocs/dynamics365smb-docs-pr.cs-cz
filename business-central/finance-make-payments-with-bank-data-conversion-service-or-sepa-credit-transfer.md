---
    title: Make Payments with the AMC Banking 365 Fundamentals extension or SEPA Credit Transfer | Microsoft Docs
    description: Process payments to your vendors by exporting a file together with the payment information from the journal lines.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: bholtorf

---
# Provádění plateb pomocí rozšíření AMC Banking 365 Fundamentals nebo převodem SEPA
Na stránce **Deník plateb**, můžete zpracovat platby svým dodavatelům exportem souboru společně s platebními informacemi z řádků deníku. Soubor pak můžete nahrát do svého elektronického bankovnictví, kde jsou zpracovávány související převody peněz. [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje formát Převedení kreditu SEPA, ale ve vaši zemi / oblasti mohou být k dispozici jiné formáty elektronických plateb.

V obecné verzi [!INCLUDE[d365fin](includes/d365fin_md.md)], je nastaven a připojen globální poskytovatel služeb pro převod bankovních dat do jakéhokoli formátu souboru, který vaše banka vyžaduje. V severoamerických verzích lze stejnou službu použít k odesílání platebních souborů jako elektronický převod finančních prostředků (EFT), avšak s mírně odlišným procesem. Viz krok 6 v [Export plateb do souboru banky](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

Chcete-li povolit převedení kreditu SEPA, musíte nejprve nastavit bankovní účet, dodavatele a list finančního deníku, na který je deník plateb založen. Poté připravíte platby dodavatelům automatickým vyplněním stránky **Deník plateb** obsahující splatné platby se specifickými daty zúčtování.

> [!NOTE]
> Po ověření, že banka platby úspěšně zpracovala, můžete pokračovat v účtování řádků deníku plateb.

## Nastavení rozšíření AMC Banking 365 Fundamentals
Aktivujte rozšíření AMC Banking 365 Fundamentals, aby byl jakýkoli soubor výpisu z bankovního účtu převeden do formátu, který můžete importovat, nebo aby exportované platební soubory byly převedeny do formátu, který vaše banka vyžaduje. Pro více informací navštivte [Používání rozšíření AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).

## Nastavení převodu SEPA
Ze stránky **Deník plateb**, můžete exportovat platby do souboru a nahrát je do své elektronického bankovnictví pro zpracování souvisejících převodů peněz. [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje formát Převedení kreditu SEPA, ale ve vaši zemi / oblasti mohou být k dispozici jiné formáty elektronických plateb.

Chcete-li povolit export formátů bankovních souborů, které nejsou podporovány po vybalení z krabice v [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete nastavit definici výměny dat pomocí rámce pro výměnu dat. Více informací viz [Nastavení definic výměny dat](across-how-to-set-up-data-exchange-definitions.md).

Než budete moci zpracovat platbu elektronicky pomocí exportu souborů plateb ve formátu převedení kreditu SEPA, musíte provést následující kroky nastavení:

* Nastavte příslušný bankovní účet pro zpracování formátu převedení kreditu SEPA.
* Nastavte karty dodavatele ke zpracování plateb exportem souborů ve formátu SEPA – peněžní převod.
* Nastavte související listy finančního deníku, které umožní export plateb ze stránky **Deník plateb**
* Propojte definici výměny dat pro jeden nebo více typů plateb s příslušným způsobem nebo způsoby platby

### Nastavení bankovního účtu pro SEPA – příkaz k inkasu
1. V poli **Hledat**, zadejte **Bankovní účty**, a pak zvolte související odkaz.
2. Otevřete kartu bankovního účtu, ze kterého budete exportovat platební soubory ve formátu převedení kreditu SEPA.
3. Na záložce **Převod** v poli **Formát exportu plateb**, vyberte možnost **SEPAADD**.
4. Na poli **SEPA CT ZPR číselná řada**, vyberte číselnou řadu, ze které budou přiřazeny čísla k převedení kreditu SEPA.
5. Ujistěte se, že je vyplněno pole **IBAN**.

   > [!NOTE]
   > Pole **Kód měny** musí být nastaveno na **EUR**, protože převedení kreditu SEPA  lze provádět pouze v měně EURO.

### Nastavení karty dodavatele pro převedení kreditu SEPA
1. V poli **Hledat**, zadejte **Dodavatelé**, a pak zvolte související odkaz.
2. Otevřete kartu dodavatele, ze kterého budete exportovat platební soubory ve formátu převedení kreditu SEPA.
3. Na záložce **Platba** v poli **Kód způsobu platby**, vyberte možnost **BANKA**.
4. V poli **Kód preferovaného bankovního účtu**, vyberte banku, do které se budou peníze převádět při zpracovávání vaší elektronickou bankou.

   Hodnota v poli **Preferovaný bankovní účet** je zkopírována do pole **Bankovní účet příjemce** na stránce **Deník plateb**.

### Nastavení deníku plateb na export souborů plateb
1. V poli **Hledat**, zadejte **Deník plateb**, a pak zvolte související odkaz.
2. Otevřete deník plateb, který používáte ke zpracování plateb, exportováním souborů ve formátu Převedení kreditu SEPA.
3. V poli **Název Dávky** zvolte tlačítko rozevíracího seznamu.
4. Na stránce **Listy finančního deníku**, vyberte akci **Upravit seznam**.
5. Na řádku deníku plateb, který budete používat k exportu plateb, zaškrtněte políčko **Povolen export úhrad**.

### Propojení definice výměny dat pro jeden nebo více typů plateb s příslušným způsobem nebo způsoby platby
1. V poli **Hledat**, zadejte **Metody platby**, a pak zvolte související odkaz.
2. Na stránce **Způsoby platby**, vyberte způsob platby, ze kterého se exportují platby, a poté vyberte pole **Definice  řádku plat. exportu**.
3. Na stránce **Definice řádku plat. exportu** vyberte kód, který jste zadali v poli **Kód** na záložce s náhledem **Definice řádků** v kroku 4 sekce “Popis formátování řádků a sloupců v souboru-To describe the formatting of lines and columns in the file” v proceduře [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).

Zmocnění k přímému debetu je automaticky vloženo do **ID zmocnění k přímému debetu** při vytváření prodejní faktury pro odběratele, kterého jste vybrali v kroku 2. Další informace naleznete v části [Vytvoření periodických nákupních a prodejních řádků](sales-how-work-standard-lines.md).

## Příprava deníku plateb
Vyplňte deník plateb řádky pro splatné platby dodavatelům, s možností vložení dat zaúčtování na základě dat splatností souvisejících nákupních dokladů. Pro více informací navštivte [Správa závazků](payables-manage-payables.md)

## Export plateb do souboru banky
Pokud jste připraveni provádět platby svým dodavatelům nebo refundovat své zaměstnance, můžete exportovat soubor s platebními informacemi na řádcích na stránce **Deník plateb**. Poté můžete soubor nahrát do své banky a zpracovat související převody peněz.

V obecné verzi [!INCLUDE[d365fin](includes/d365fin_md.md)], je dostupné rozšíření AMC Banking 365 Fundamentals. V severoamerických verzích lze stejné rozšíření použít k odesílání platebních souborů jako elektronický převod peněžních prostředků (EFT), avšak s poněkud odlišným procesem. Viz krok 6 v [Export plateb do souboru banky](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]
> Než budete moci exportovat platební soubory z deníku plateb, musíte zadat elektronický formát příslušného bankovního účtu a musíte povolit rozšíření AMC Banking 365 Fundamentals. Pro více informací navštivte [Nastavení bankovních účtů](bank-how-setup-bank-accounts.md) a [Používání rozšíření AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md). Kromě toho musíte zaškrtnout pole **Povolen export úhrad** nacházející se na stránce **Listy finančního deníku**. Další informace naleznete v části [Práce s Finančním deníkem](ui-work-general-journals.md).

Pomocí stránky **Bezhotovostní převody** můžete zobrazit platební soubory, které byly exportovány z deníku plateb. Z této stránky můžete také znovu exportovat soubory plateb v případě technických chyb nebo změn souborů. Všimněte si však, že exportované soubory EFT nejsou na této stránce zobrazeny a nelze je znovu exportovat.

### Export plateb do bankovního souboru
Následující text popisuje, jak zaplatit dodavateli šekem. Kroky jsou podobné pro vrácení peněz šekem zákazníkovi.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky plateb** a poté vyberte související odkaz.
2. Vyplňte řádky deníku plateb. Pro více informací navštivte [Záznam plateb a vrácení peněz](payables-how-post-payments-refunds.md)

> [!NOTE]
> Pokud používáte EFT, musíte nejdříve vybrat buď **Elektronická platba** nebo **Elektronická Platba–IAT** v poli **Typ platby v bance**. Různé služby exportu souborů a jejich formáty vyžadují různé hodnoty nastavení na stránkách **Karta bankovního účtu** a **Karta bank.účtu dodavatele**. Při pokusu o export souboru budete informováni o chybných nebo chybějících hodnotách nastavení.

3. Po dokončení všech řádků platebního deníku vyberte akci **Exportovat**.
4. Na stránce **Export elektronických plateb**, vyplňte pole podle potřeby.

   Jakékoli chybové hlášky se zobrazí v záložce s náhledem **Chyby platebního souboru**, kde můžete také zvolit chybovou zprávu a zobrazit tak podrobné informace. Před exportem souboru plateb je nutné vyřešit všechny chyby.

   > [!TIP]
   > Při použití rozšíření AMC Banking 365 Fundamentals běžná chybová zpráva uvádí, že číslo bankovního účtu nemá délku, kterou vaše banka vyžaduje. Chcete-li se této chybě vyhnout nebo ji vyřešit, musíte odebrat hodnotu v poli **IBAN** na stránce **Karta bankovního účtu** a poté v poli **Číslo bankovního účtu**, zadejte číslo bankovního účtu ve formátu, který vyžaduje vaše banka.

5. Na stránce **Uložit jako**, určete umístění, do kterého je soubor exportován, a poté zvolte **Uložit**.

   > [!NOTE]
   > Pokud používáte EFT, uložte výsledný formulář úhrady dodavatele jako dokument aplikace Word nebo vyberte, zda chcete, aby byl zaslán e-mailem přímo dodavateli. Platby jsou nyní přidány na stránku **Generovat soubor EFT** odkud můžete vygenerovat několik platebních příkazů najednou, abyste ušetřili náklady na přenos. Pro více informací se podívejte na následující kroky
6. Na stránce **Deníky plateb** zvolte akci **Generovat soubor EFT**.

   Na stránce **Generovat soubor EFT**, jsou všechny platby nastavené pro EFT, které jste exportovali z platebního deníku pro určený bankovní účet, ale dosud nebyly vygenerovány, uvedeny na záložce s náhledem **Řádky**.
7. Zvolte akci **Generovat soubor EFT** pro export jednoho lokálního souboru pro všechny platby EFT.
8. Na stránce **Uložit jako**, určete umístění, do kterého je soubor exportován, a poté zvolte **Uložit**.

Bankovní platební soubory se exportují do vámi zadaného umístění a můžete jej odeslat na svůj elektronický bankovní účet a provést skutečné platby. Poté můžete zaúčtovat exportované řádky deníku plateb.

### Plánování kdy zaúčtovat exportované platby
Pokud nechcete pro exportovanou platbu zaúčtovat řádek platebního deníku, například proto, že čekáte na potvrzení, že transakce byla zpracována bankou, můžete řádek deníku smazat. Když později vytvoříte řádek deníku plateb, abyste zaplatili zbývající částku na faktuře, pole **Exportovaná částka celkem** zobrazuje, jak velká část částky platby již byla exportována. Podrobné informace o exportovaném součtu můžete také najít výběrem tlačítka **Položky bezhotovostního  převodu** pro zobrazení detailů o exportovaných platebních souborech.

Pokud budete postupovat podle procesu, kdy neúčtujete platby, dokud nebudete mít potvrzení, že byly zpracovány v bance, toto můžete ovládat dvěma způsoby.

* V deníku plateb s navrženými řádky platby můžete seřadit buď podle sloupce **Exportováno do platebního souboru**, nebo **Exportovaná částka celkem** a poté odstranit návrhy plateb otevřených faktur, pro které byly platby již provedeny a za které nechcete provádět platby
* Na stránce **Navrhnout platby dodavateli**, kde určíte, které platby vložit do deníku plateb, můžete zaškrtnout políčko **Přeskočit exportované platby**, pokud nechcete vložit řádky deníku plateb, které již byly exportovány.

Chcete-li zobrazit informace o exportovaných platbách, zvolte akci **Historie exportu plateb**.

### Zpětný export plateb do bankovního souboru
Ze stránky **Bezhotovostní převody** můžete znovu exportovat platební soubory. Před odstraněním nebo zaúčtováním řádků deníku plateb můžete také znovu exportovat soubor plateb ze stránky **Deník plateb** jednoduchým exportem. Pokud jste řádky platebních deníků po exportu odstranili nebo zaúčtovali, můžete stejný exportní soubor znovu exportovat ze stránky **Bezhotovostní převody**. Vyberte řádek pro dávku kreditních převodů, které chcete znovu exportovat, a poté použijte akci  **Reexport plateb do souboru**.

> [!NOTE]
> Exportované soubory EFT se nezobrazí na stránce **Bezhotovostní převody** a nelze je znovu exportovat.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bezhotovostní převody** a poté vyberte související odkaz.
2. Vyberte export plateb, který chcete znovu exportovat, a poté vyberte akci **Reexport platby do souboru**.

## Zaúčtování plateb
Když je elektronická platba úspěšně zpracována bankou, zaúčtujete platby. Pro více informací navštivte [Provedené platby](payables-make-payments.md)

## Viz také
[Používání rozšíření AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Nastavení převodu SEPA](finance-how-to-set-up-sepa-credit-transfer.md)  
[Správa závazků](payables-manage-payables.md)  
[Práce s Finančním deníkem](ui-work-general-journals.md)  
[Sběr plateb pomocí SEPA – příkaz k inkasu](finance-collect-payments-with-sepa-direct-debit.md)
