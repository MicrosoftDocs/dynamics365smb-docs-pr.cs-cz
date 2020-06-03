---
    title: How to work With VAT on Sales and Purchases | Microsoft Docs
    description: This topic describes how perform tasks such as correcting posted VATIn EU countries/regions, every sales and purchase transaction is subject to VAT calculations. This topic describes how.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: VAT, sales, purchases,
    ms.date: 01/13/2020
    ms.author: bholtorf

---
# Práce s DPH z prodeje a nákupu
Pokud vaše země nebo region vyžaduje, abyste vypočítali daň z přidané hodnoty (DPH) z prodejních a nákupních transakcí, abyste mohli nahlásit částky daňovému úřadu, můžete nastavit [!INCLUDE[d365fin](includes/d365fin_md.md)] pro automatický výpočet DPH v prodejních a nákupních dokladech. Pro více informací navštivte [Nastavení výpočtů a metod účtování daně z přidané hodnoty](finance-setup-vat.md).

Existují však některé úkoly související s DPH, které můžete provádět ručně. Například může být nutné opravit zaúčtované částky, pokud zjistíte, že dodavatel používá jinou metodu zaokrouhlení.

## Výpočet a zobrazení částek DPH v prodejních a nákupních dokladech
Částky DPH v prodejních a nákupních dokladech můžete vypočítat a zobrazit odlišně v závislosti na typu zákazníka nebo dodavatele. Vypočtenou částku DPH můžete také přepsat tak, aby odpovídala částce DPH vypočtené vaším dodavatelem na danou transakci.

### Jednotková cena a částka řádku včetně/bez DPH na prodejních dokladech
Když vyberete číslo položky v poli **Číslo** na prodejním dokladu, [!INCLUDE[d365fin](includes/d365fin_md.md)] vyplní pole **Jednotková cena**. Jednotková cena pochází buď z karty **Zboží**, nebo z povolených cen zboží pro zboží a zákazníka. [!INCLUDE[d365fin](includes/d365fin_md.md)] vypočítá **Částku na řádku**, když zadáte množství pro řádek.

Pokud prodáváte maloobchodním spotřebitelům, můžete chtít, aby ceny na prodejních dokladech zahrnovaly DPH. Za tímto účelem zaškrtněte v dokumentu políčko **Ceny včetně DPH**.

### Včetně nebo bez DPH
Pokud je v prodejním dokladu zaškrtnuto políčko **Ceny včetně DPH**, pole  **Jednotková cena** a **Částka na řádku** zahrnují DPH a názvy polí to také budou zobrazovat. Ve výchozím nastavení není v těchto polích zahrnuta DPH.

Pokud pole není vybráno, aplikace vyplní pole **Jednotková cena** a **Částka na řádku** bez DPH a názvy polí to budou zobrazovat.

Můžete nastavit výchozí nastavení **ceny včetně DPH** pro všechny prodejní doklady pro zákazníka v poli **Ceny včetně DPH** na kartě **Zákazník**. Můžete také nastavit ceny zboží tak, aby zahrnovaly nebo vyloučily DPH. Ceny zboží obsažené v kartě zboží obvykle budou cenou bez DPH. Aplikace používá informace z pole **Ceny včetně DPH** na kartě **Zboží** k určení výše jednotkové ceny pro prodejní doklady.

Následující tabulka poskytuje přehled o tom, jak aplikace počítá částky jednotkové ceny pro prodejní doklad, pokud jste nenastavili ceny na stránce **Prodejní ceny**:

| **Cena zahrnuje pole DPH na kartě zboží** | **Ceny zahrnují pole DPH v prodejní hlavičce** | **Provedená akce** |
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
| Bez zaškrtnutí | Bez zaškrtnutí | **Jednotková cena** na kartě zboží je zkopírována do pole **Jednotková cena  DPH** na prodejních řádcích. |
| Bez zaškrtnutí | Zaškrtnutí | Aplikace vypočítá částku DPH na jednotku a připočítá ji k **jednotkové ceně** na kartě zboží. Tato celková jednotková cena je poté zadána do pole **Jednotková cena včetně  DPH** na prodejních řádcích. |
| Zaškrtnutí | Bez zaškrtnutí | Aplikace vypočítá částku DPH zahrnutou v poli **Jednotková cena** na kartě zboží pomocí DPH% vztahující se k obchodní DPH. Kombinace účto skupiny (Cena) a DPH účto  skupiny zboží. **Jednotková cena** na kartě zboží snížená o částku DPH je pak zadána do pole **Jednotková cena  bez DPH** v prodejních řádcích. |
| Zaškrtnutí | Zaškrtnutí | **Jednotková cena** na kartě zboží je zkopírována do pole **Jednotková cena včetně  DPH** na prodejních řádcích. |

## Ruční oprava částek DPH v prodejních a nákupních dokladech
Můžete provádět opravy zaúčtovaných položek DPH. To vám umožní změnit celkové částky prodeje nebo nákupu DPH beze změny základu DPH. To může být nutné provést, například pokud obdržíte fakturu od dodavatele, který správně vypočítal DPH.

Přestože jste pro zpracování dovozní DPH nastavili jednu nebo více kombinací, musíte nastavit alespoň jednu DPH účto skupinu zboží. Můžete jej například pojmenovat **SPRÁVNĚ** pro účely korekce, pokud nemůžete použít stejný účet hlavní knihy v poli **Účet nákupní DPH** v řádku nastavení účtování DPH. Pro více informací navštivte [Nastavení výpočtů a metod účtování u daně z přidané hodnoty](finance-setup-vat.md).

Pokud bylo skonto vypočteno na základě částky faktury, která zahrnuje DPH, vrátíte část skonta částky DPH při udělení skonta. Všimněte si, že musíte aktivovat pole **Úprava o slevu na platby** jak v obecném nastavení hlavní knihy, tak v nastavení účtování DPH pro konkrétní kombinace skupiny účtování firem na základě DPH a skupiny účtování produktů na bázi DPH.

### Nastavení systému pro ruční zadávání DPH do prodejních dokladů
Následující text popisuje, jak povolit ruční změny DPH v prodejních dokladech. Kroky jsou podobné jak na stránce **Nastavení nákupu a závazků**.

1. Na stránce **Nastavení financí** zadejte **Max.povolená  odchylka DPH** mezi částkou vypočítanou podle aplikace a manuální částkou.
2. Na stránce **Nastavení prodeje a pohledávek** zaškrtněte pole **Povolit odchylku DPH**.

### Úprava DPH u prodejního dokladu
1. Otevřete příslušnou prodejní objednávku.
2. Vyberte akci **Statistika**.
3. Na záložce **Fakturace** vyberte hodnotu v poli **Počet řádků  částek DPH**.
4.  Upravte pole **Částka DPH**.

> [!NOTE]
> V řádcích se zobrazí celková částka DPH na faktuře, seskupená podle identifikátoru DPH. Částku můžete ručně upravit v poli **Částka DPH** na řádcích pro každý identifikátor DPH. Když upravíte pole **Částka DPH**, aplikace zkontroluje, zda jste nezměnili DPH o více než částku, kterou jste určili jako maximální povolený rozdíl. Pokud je částka mimo rozsah zadaný v poli **Max.povolená  odchylka DPH** zobrazí se varování s uvedením maximálního povoleného rozdílu. Nebudete moci pokračovat, dokud nebude částka upravena v rámci přijatelných parametrů. Klikněte na **OK** a zadejte další  **částku DPH**, která je v povoleném rozsahu. Je-li rozdíl v DPH roven nebo nižší než maximální povolené množství, bude DPH rozdělena úměrně mezi řádky dokladů, které mají stejný identifikátor DPH.

## Ruční výpočet DPH pomocí deníků
Obecně můžete také upravit částky DPH, deníky prodeje a nákupu. Možná to budete muset udělat, když do svého deníku zadáte dodavatelskou fakturu a je rozdíl mezi částkou DPH, kterou vypočte [!INCLUDE[d365fin](includes/d365fin_md.md)] a částou DPH na faktuře dodavatele.

### Nastavení systému pro ruční zadávání DPH ve finančních denících
Před manuálním zadáním DPH do finančního deníku musíte provést následující kroky.

1. Na stránce **Nastavení financí** zadejte **Max.povolená  odchylka DPH** mezi částkou vypočítanou podle aplikace a manuální částkou.
2. Na stránce **Šablony finančního deníku** zaškrtněte políčko **Povolit odchylku DPH** pro příslušný deník.

### Nastavení systému pro ruční zadání DPH v deníku prodeje a nákupu
Než ručně zadáte DPH do prodejního nebo nákupního deníku, musíte provést následující kroky.

1. Na stránce **Nastavení nákupu a závazků** zaškrtněte políčko **Povolit odchylku DPH**.
2. Opakujte krok 1 pro stránku  **Nastavení prodeje a pohledávek**.
3. Po dokončení výše popsaného nastavení můžete upravit pole **Částka DPH** na řádku finančního deníku nebo pole **Částka  DPH protiúčtu** na řádku prodejního nebo nákupního deníku. [!INCLUDE[d365fin](includes/d365fin_md.md)] zkontroluje, zda rozdíl není větší než zadané maximum.

   > [!NOTE]
   > Pokud je rozdíl větší, zobrazí se upozornění s uvedením maximálního povoleného rozdílu. Chcete-li pokračovat, je nutné upravit částku. Zvolte **OK** a zadejte částku, která je v povoleném rozsahu. Pokud je rozdíl DPH roven nebo nižší než maximální povolená hodnota, [!INCLUDE[d365fin](includes/d365fin_md.md)] zobrazí rozdíl v poli **Odchylka DPH**.

## Účtování dovozní DPH s nákupními fakturami
Namísto použití deníků k zaúčtování dovozní faktury s DPH můžete použít nákupní fakturu.

### Nastavení nákupu pro zaúčtování dovozních faktur DPH
1. Nastavit kartu dodavatele pro dovozní úřad, který vám pošle dovozní fakturu s DPH. **Obecná  obch.účto  skupina** a **DPH obchodní  účto skupina** musí být nastavena stejným způsobem jako účet hlavní knihy pro dovozní DPH.
2. Vytvořte **Obecnou účto  skupinu zboží** pro dovozní DPH a nastavte dovozní DPH na **Výchozí  DPH účto skupina zboží** pro související **Obecnou účto  skupinu zboží**.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účetní osnova** a poté vyberte související odkaz.
4. Vyberte účet hlavní knihy pro dovozní DPH a poté vyberte akci **Upravit**.
5. Na záložce **Účtování** vyberte nastavení **Obecná  účto  skupina zboží** pro dovozní DPH. [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky vyplní pole **DPH účto  skupina zboží**.
6. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení obecného účtování** a poté vyberte související odkaz.
7. Vytvořte kombinaci **Obecné  obch.účto  skupiny** pro finanční úřad a **Obecné  účto  skupiny** pro dovozní DPH. Pro tuto novou kombinaci vyberte v poli **Účet nákupu** účet hlavní knihy pro dovozní DPH.

### Vytvoření nové faktury pro dodavatele dovozního úřadu po dokončení nastavení
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktury** a poté vyberte související odkaz.
2. Vytvořte novou nákupní fakturu.
3. V poli **Nákup od dodavatele** zvolte dodavatele dovozního úřadu a pak zvolte tlačítko **OK**.
4. V nákupním řádku v poli **Typ** vyberte **Finanční účet** a v poli **Číslo** vyberte Účet hlavní knihy pro dovozní DPH.
5. V poli **Množství** zadejte **1**.
6. V poli **Nákupní cena bez DPH**, zadejte částku DPH.
7. Zaúčtujte fakturu.

## Zpracování certifikátů dodání
Při prodeji zboží zákazníkovi v jiné zemi nebo oblasti EU musíte zákazníkovi zaslat certifikát o dodávce, který musí zákazník podepsat a vrátit vám ho. Následující postupy platí pro zpracování certifikátu o dodávce pro prodejní dodávky, ale stejné kroky platí pro dodávky servisu zboží a pro vrácení dodávek dodavatelům.

### Zobrazení detailů o certifikátu dodání
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované prodejní dodávky** a poté vyberte související odkaz.
2. Vyberte příslušnou prodejní dodávku zákazníkovi v jiné zemi / regionu EU.
3. Zvolte **Detaily certifikátu dodání**.
4. Ve výchozím nastavení, pokud je pro nastavení účto. skupiny DPH pro zákazníka zaškrtnuto políčko **Požadován certifikát dodání**, je pole **Stav** nastaveno na **Povinné**. Toto pole můžete aktualizovat a uvést, zda zákazník certifikát vrátil.

   > [!Note]
   > Pokud v nastavení DPH není zaškrtnuto políčko **Požadován certifikát dodání**, je vytvořen záznam a pole **Stav** je nastaveno na **Nelze použít**. Pole můžete aktualizovat tak, aby zobrazovalo správné informace o stavu. Stav můžete podle potřeby ručně změnit z hodnoty **Nelze použít** na **Povinné** a z hodnoty **Povinné** na **Nelze použít**.

   Když aktualizujete pole **Stav** na **Povinné**, **Přijato** nebo **Nelze použít** certifikát se vytvoří.

   > [!TIP]
   > Na stránce **Certifikáty dodání** můžete zobrazit stav všech zaúčtovaných zásilek, pro které byl vytvořen certifikát dodávky.

5. Zvolte **Tisk certifikátu dodání**.

   > [!Note]
   > Doklad můžete zobrazit nebo vytisknout. Pokud vyberete **Tisk certifikátu dodání** a doklad vytisknete, automaticky se zaškrtne políčko **Vytištěno**. Kromě toho, pokud již není zadán, stav certifikátu je aktualizován na **Povinné**. V případě potřeby zahrnete k dodávce vytištěný certifikát.

### Tisk certifikátu dodání
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované prodejní dodávky** a poté vyberte související odkaz.
2. Vyberte příslušnou prodejní dodávku zákazníkovi v jiné zemi / regionu EU.
3. Vyberte akci **Tisk certifikátu dodání**.

   > [!NOTE]
   > Alternativně můžete vytisknout certifikát ze stránky **Certifikát dodání**.

4. Chcete-li do certifikátu zahrnout informace z řádků v dodacím dokladu, zaškrtněte políčko **Tisk detailů řádku**.
5. Zaškrtněte políčko **Vytvořit Certifikát dodání, jestliže ještě není vytvořen** a [!INCLUDE[d365fin](includes/d365fin_md.md)] vytvoří certifikáty pro zaúčtované dodávky, které jej nemají v okamžiku spuštění. Pokud zaškrtnete políčko, budou vytvořeny nové certifikáty pro všechny zaúčtované dodávky, které nemají certifikáty ve vybrané oblasti.
6. Ve výchozím nastavení se nastavení filtru vztahuje na vybraný doklad dodávky. Vyplňte informace o filtru a vyberte konkrétní certifikát o dodávce, který chcete vytisknout.
7. Na stránce **Certifikát dodání** vyberte akci **Tisk** pro tisk sestavy nebo zvolte akci **Náhled** a zobrazte ji na obrazovce.

   > [!Note]
   > Pole **Stav certifikátu dodání** a **Vytištěno** jsou aktualizovány pro dodávku na stránce **Certifikáty dodání**.

8. Tištěný certifikát o dodávce zašlete zákazníkovi k podpisu.

### Aktualizace stavu certifikátu o dodávce zásilky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované prodejní dodávky** a poté vyberte související odkaz.
2. Vyberte příslušnou prodejní dodávku zákazníkovi v jiné zemi / regionu EU.
3. V poli **Stav** zvolte příslušnou možnost.

   Pokud zákazník vrátil podepsaný certifikát o dodávce, zvolte **Přijato**. Pole **Datum příjmu** je aktualizováno. Ve výchozím nastavení je datum příjmu nastaven na aktuální pracovní datum.

   Datum můžete upravit tak, aby zobrazoval datum, kdy jste obdrželi podepsaný certifikát dodávky zákazníka. K podepsanému certifikátu můžete také přidat odkaz pomocí standardního propojení [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Pokud zákazník nevrátí podepsaný certifikát o dodávce, vyberte **Nepřijato**. Poté musíte zákazníkovi poslat novou fakturu, která zahrnuje DPH, protože původní faktura nebude daňovým úřadem akceptována.

Chcete-li zobrazit skupinu certifikátů, začněte na stránce **Certifikáty dodání** a poté aktualizujte informace o stavu zbývajících certifikátů, jakmile je obdržíte od svých zákazníků. To může být užitečné, když chcete hledat všechny certifikáty, které mají určitý stav, například **Povinné**, u kterých chcete aktualizovat jejich stav na **Nepřijato**.

### Aktualizace stavu skupiny certifikátů dodávky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Certifikáty dodání** a poté vyberte související odkaz.
2. Chcete-li vytvořit seznam certifikátů, které chcete spravovat, filtrujte pole **Stav** na hodnotu, kterou chcete.
3. Chcete-li aktualizovat informace o stavu, vyberte **Upravit přehled**.
4. V poli **Stav** zvolte příslušnou možnost.

   Pokud zákazník vrátil podepsaný certifikát o dodávce, zvolte **Přijato**. Pole **Datum příjmu** je aktualizováno. Ve výchozím nastavení je datum příjmu nastaven na aktuální pracovní datum.

   Datum můžete upravit tak, aby zobrazoval datum, kdy jste obdrželi podepsaný certifikát o dodávce. Odkaz na podepsaný certifikát můžete také přidat pomocí standardního propojení dokladů [!INCLUDE[d365fin](includes/d365fin_md.md)].

   > [!NOTE]
   > Když na stránku **Certifikáty dodání** přejdete tímto postupem nemůžete vytvořit nový certifikát spotřebního materiálu. Chcete-li vytvořit certifikát pro dodávku, která nebyla nastavena tak, aby vyžadovala certifikát, otevřete odeslanou prodejní dodávku a použijte jeden ze dvou výše popsaných postupů:
   > * Ruční vytvoření certifikátu dodávky
   > * Tisk certifikátu dodávky.


## Viz související školení na webu [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## Viz také
[Nastavení výpočtů a metod účtování daně z přidané hodnoty](finance-setup-vat.md)  
[Ohlásit DPH finančnímu úřadu](finance-how-report-vat.md)
