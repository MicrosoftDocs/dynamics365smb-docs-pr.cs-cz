---
    title: Create XMLports based on XML schemas | Microsoft Docs
    description: Use XML schemas to set yup the document exchange framework.
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
# Použití schémat XML k přípravě definic datových výměn
Chcete-li povolit import / export dat v souborech XML prostřednictvím rámce pro výměnu dat v  [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete použít schémata XML k definování datových prvků, které chcete vyměnit s [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tuto práci provedete na stránce **Náhled XML schématu** načtením souboru schématu XML, výběrem příslušných datových prvků a poté inicializací definice výměny dat nebo XMLportu.

Pokud jste definovali, které datové prvky mají být zahrnuty na základě schématu XML, můžete použít akci **Generovat XMLport** k vytvoření objektu XMLport.

Alternativně můžete použít akci **Generovat definici výměny dat** k inicializaci definice výměny dat na základě vybraných datových prvků, které pak dokončíte v rámci výměny dat. Tím se na stránce **Definice výměny účtovaných dat** vytvoří záznam, kde budete pokračovat definováním, které prvky v souboru, se mapují do kterých polí v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Více informací viz [Nastavení definic výměny dat](across-how-to-set-up-data-exchange-definitions.md).

Toto téma obsahuje následující postupy:

- Načtení souboru schématu XML

- Výběr nebo vymazání uzlů ve schématu XML

- Generování definice výměny dat, která je založena na schématu XML

- Generování XMLportu pro soubor, který je založen na schématu XML

- Import XMLportu do Návrháře objektů

### Načtení souboru schématu XML

1. Zkontrolujte, zda je k dispozici příslušný soubor schématu XML. Přípona souboru je .xsd.

2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **XML Schéma** a poté vyberte související odkaz.

3. Zvolte akci **Nový**.

4. Vyplňte pole podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Kód** | Zadejte kód pro identifikaci schématu XML. |
   | **Popis** | Zadejte popis schématu XML. |

   Pole **Cílový obor názvů** určuje jakýkoli obor názvů v souboru schématu XML, který byl pro řádek načten.

5. Zvolte akci **Načíst schéma** a vyberte soubor schématu XML.

   Po načtení souboru jsou zbývající pole na řádku vyplněna informacemi ze souboru a políčko **Schéma je načteno** je zaškrtnuto.

   > [!NOTE]
   > Podle výchozího nastavení je strom načteného schématu XML sbalen. Každý uzel rozbalíte výběrem tlačítka **+** v uzlu. Chcete-li rozbalit všechny uzly, zvolte na pásu karet možnost **Rozbalit vše**.

### Výběr nebo vymazání uzlů ve schématu XML

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Náhled XML schématu** a poté vyberte související odkaz.

2. Vyplňte pole v záhlaví, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Kód XML schématu** | Určete soubor schématu XML, který jste načetli v kroku 5, v části „Načtení souboru schématu XML“. |
   | **Číslo nového XML portu** | Určete číslo XMLportu, který bude vytvořen z tohoto XML schématu, když zvolíte akci **Generovat XMLport**. |

   Řádky jsou nyní vyplněny uzly představujícími všechny prvky ve schématu XML. Ve výchozím nastavení jsou vybrány uzly pro prvky, které jsou povinné podle schématu XML.

3. Na prvním řádku ve sloupci **Název uzlu** rozbalte uzel **Dokument** a poté postupně rozbalte nově zobrazené uzly, které chcete zkontrolovat.

   Případně klikněte pravým tlačítkem myši na uzel a pak zvolte **Rozbalit vše**.

4. Zvolte některou z následujících akcí, chcete-li změnit, které uzly jsou zobrazeny.

   | **Akce** | Popis |
   |----------------|---------------------------------------|  
   | **Zobrazit vše** | Všechny uzly jsou zobrazeny. |
   | **Skrýt nepovinné** | Zobrazí se pouze uzly představující prvky, které jsou požadovány podle schématu XML. Tyto uzly jsou obvykle označeny jako **1** v poli **Minimální výskyt.**<br /><br />Chcete-li zobrazení obrátit, zvolte **Zobrazit vše**. |
   | **Skrýt nevybrané** | Zobrazí se pouze uzly, kde je zaškrtnuto políčko **Vybrané**. <br /><br /> Chcete-li zobrazení obrátit, zvolte **Zobrazit vše**. |

5. Vyberte akci **Upravit**.

6. V zaškrtávacím políčku **Vybráno**, zadejte pro každý uzel, zda má být prvek podporován v definici výměny dat pro související soubor banky SEPA.

   > [!NOTE]
   > Když vyberete povinný podřízený uzel, vyberou se také všechny nadřazené uzly nad ním.

7. Zvolte akci **Vybrat všechny povinné prvky** chcete-li znovu vybrat všechny uzly, které představují prvky, které jsou podle schématu XML povinné.

8. Zvolte akci **Odznačit všechny**, pro vymazání všech výběrů.

   Pole  **Volba** určuje, že uzel má dva nebo více uzlů na stejné úrovni, které fungují jako možnosti.

### Generování definice výměny dat, která je založena na schématu XML

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **XML Schéma** a poté vyberte související odkaz.

2. Vyberte příslušné schéma XML a pak zvolte akci **Otevřít prohlížeč schématu**.

3. Zkontrolujte, zda jsou vybrány příslušné uzly. Pro více informací navštivte sekci „Výběr nebo vymazání uzlů ve schématu XML“.

4. Na stránce **Náhled XML schématu** vyberte akci **Generovat definici výměny dat**.

Definice výměny dat je vytvořena na stránce **Definice výměny účtovaných dat**, kterou můžete dokončit zadáním, které prvky v souboru, se mají mapovat na která pole v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Více informací viz [ Nastavení definice výměny dat ](across-how-to-set-up-data-exchange-definitions.md).

> [!NOTE]
> Můžete také použít funkci **Získat strukturu souboru** ze stránky **Definice výměny účtovaných dat**, která používá funkcionalitu ze stránky **Náhled XML schématu** pro předvyplnění záložky **Definice sloupce**.

### Generování XMLportu, který je založen na XML schématu

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **XML Schéma** a poté vyberte související odkaz.

2. Vyberte příslušné schéma XML a pak zvolte akci **Otevřít prohlížeč schématu**.

3. V poli **Číslo nového XML portu** zadejte číslo, které bude novému objektu XMLportu při generování přiděleno.

4. Zkontrolujte, zda jsou vybrány příslušné uzly. Pro více informací navštivte sekci „Výběr nebo vymazání uzlů ve schématu XML“.

5. Vyberte akci **Generovat XMLport** a potom uložte objekt jako soubor .txt na vhodné místo.

6. Import nového XMLportu do vývojového prostředí [!INCLUDE[d365fin](includes/d365fin_md.md)] a jeho zkompilování.

## Viz také
[Nastavení definice výměny dat](across-how-to-set-up-data-exchange-definitions.md)  
[Export plateb do bankovního souboru](payables-how-export-payments-bank-file.md)  
[Sběr plateb pomocí SEPA – příkaz k inkasu](finance-collect-payments-with-sepa-direct-debit.md)  
[O rozhraní výměny dat](across-about-the-data-exchange-framework.md)
