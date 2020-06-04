---
title: Process Returns or Cancellations | Microsoft Docs
description: Explains how to create and post a purchase credit memo when you want to return items to a vendor or cancel purchased services.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 04/01/2020
ms.author: sgroespe

---
# Zpracování nebo zrušení nákupní vratky
Pokud chcete vrátit zboží svému dodavateli nebo zrušit zakoupené služby, můžete vytvořit a zaúčtovat nákupní dobropis, který specifikuje požadovanou změnu s ohledem na původní nákupní fakturu. Chcete-li zahrnout správné informace o nákupní faktuře, můžete vytvořit nákupní dobropis přímo z zaúčtované nákupní faktury nebo můžete vytvořit nový nákupní dobropis se zkopírovanými fakturačními údaji.

Pokud potřebujete větší kontrolu nad procesem nákupní vratky, například doklady skladu pro zpracování zboží nebo lepší přehled při zpětném odesílání zboží z více nákupních dokladů s jednou nákupní vratkou, můžete vytvořit objednávky nákupní vratky. Objednávka nákupní vratky automaticky vydá související nákupní dobropis. Pro více informací navštivte [Vytvoření objednávky nákupní vratky na základě jednoho nebo více zaúčtovaných nákupních dokladů](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

> [!NOTE]
> Pokud zaúčtovaná nákupní faktura ještě nebyla zaplacena, můžete použít funkce **Opravit** nebo **Zrušit** na účtované nákupní faktuře a automaticky stornujte zúčastněné transakce. Tyto funkce fungují pouze pro nezaplacené faktury a nepodporují částečné vrácení nebo zrušení. Pro více informací navštivte [Opravení nebo zrušení nezaplacených nákupních faktur](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Obvykle vytvoříte nákupní dobropis nebo objednávku nákupní vratky v reakci na dobropis, který vám byl zaslán dodavatelem. Nákupní dobropis nebo objednávka nákupní vratky slouží jako interní dokumentace procesu dobropisu pro účely účetnictví nebo pro kontrolu přepravy zboží.

Změna se může týkat všech produktů na původní nákupní faktuře nebo pouze některých produktů. V souladu s tím můžete částečně vrátit přijaté zboží nebo požadovat částečné vrácení přijatých služeb. V takovém případě je nutné upravit informace na nákupním dobropisu nebo objednávce nákupní vratky.

Kromě původní zaúčtované nákupní faktury můžete použít nákupní dobropis nebo objednávku nákupní vratky na jiné nákupní doklady, například na jinou zaslanou nákupní fakturu, protože vracíte i zboží dodané s touto fakturou.

Účtování dobropisů také vrátí všechny poplatky za zboží, které byly přiřazeny k zaúčtovanému dokladu, takže položly ocenění zboží jsou stejné jako před přiřazením poplatku za zboží.

## Zásoby a ocenění
Chcete-li zachovat správné ocenění zásob, obvykle chcete vybrat vrácené zboží ze skladu za jednotkové náklady, za které byly zakoupeny, nikoli za aktuální pořizovací cenu. Tomu se říká vrácení přesných nákladů.

Existují dvě funkce pro automatické přiřazení vrácení přesných nákladů.

| Funkce | Popis |
|------------------|---------------------------------------|  
| Funkce **Získat účt. řádky pro stornování** na stránce **Objednávka nákupní vratky** | Zkopíruje řádky jednoho nebo více zaúčtovaných dokladů, které mají být vráceny do objednávky nákupní vratky. Pro více informací navštivte [Vytvoření objednávky nákupní vratky na základě jednoho nebo více zaúčtovaných nákupních dokladů](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents). |
| Funkce **Kopírování z dokladu** ze stránek **Nákupní dobropis** a **Objednávka nákupní vratky** | Zkopíruje záhlaví i řádky jednoho zaúčtovaného dokladu, který má být stornován. <br /><br /> Vyžaduje, aby bylo zaškrtnuto políčko **Nutné vrác.přesn.nákladů** na stránce **Nastavení nákupu a závazků**. |

Chcete-li manuálně přiřadit vrácení přesných nákladů, musíte vybrat pole **Vyrovnáno položkou zboží** na libovolném typu vráceného dokladu a poté vybrat číslo původní nákupní položky. Tím propojíte nákupní dobropis nebo objednávku nákupní vratky s původní nákupní položkou a zajistíte, že zboží bude oceněno původní pořizovací cenou.

Pro více informací navštivte [Detaily návrhu: Ocenění zásob](design-details-inventory-costing.md).

## Vytvoření nákupního dobropisu ze zaúčtované nákupní faktury
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované nákupní faktury** a poté vyberte související odkaz.
2. Na stránce **Účtované nákupní faktury** vyberte zaúčtovanou fakturu, kterou chcete stornovat, a poté vyberte akci **Vytvořit opravný dobropis**.

   Většina polí v hlavičce nákupního dobropisu je vyplněna informacemi ze zaúčtované nákupní faktury. Můžete upravit všechna pole, například novými informacemi, které odrážejí dohodu o vrácení.
3. Upravte informace na řádcích podle dohody, například počet vráceného zboží nebo částka, která má být vrácena.
4. Vyberte akci **Vyrovnat položky**.
5. Na stránce **Vyrovnat položky dodavatele** vyberte řádek se zaúčtovaným nákupním dokladem, na který chcete použít nákupní dobropis, a poté vyberte akci **ID vyrovnání**. Číslo nákupního dobropisu se vloží do pole **ID vyrovnání**.
6. Do pole **Částka k vyrovnání** zadejte částku, kterou chcete použít, pokud je menší než původní částka.

   Ve spodní části stránky **Vyrovnat položky dodavatele** můžete vidět celkovou částku, která se má použít pro stornování všech zúčastněných položek, konkrétně když je hodnota v poli **Saldo** nulová.
7. Vyberte tlačítko **OK**. Když zaúčtujete nákupní dobropis, použije se na zaúčtování nákupních dokladů.

   Pokud jste vytvořili nebo upravili potřebné řádky nákupních dobropisů a jsou zadány jednotlivé nebo více aplikací, můžete pokračovat v účtování nákupních dobropisů.
8. Vyberte akci **Účtovat**.

Zaúčtované nákupní faktury, na které použijete dobropis, jsou nyní stornovány. Pokud jste již zaplatili původní fakturu, měl by vám nyní dodavatel platbu vrátit. Pokud je dobropis pouze pro část produktu na původní faktuře, můžete zaplatit pouze zbývající částku na původní nákupní faktuře a uzavřít ji.

Nákupní dobropis je odstraněn a nahrazen novým dokladem v seznamu zaúčtovaných nákupních dobropisů.

## Vytvoření nákupního dobropisu, zkopírováním zaúčtovanýh nákupních faktur
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní dobropisy** a poté vyberte související odkaz.
2. Vyberte akci **Nový** a otevřete nový prázdny nákupní dobropis.
3. Do pole **Dodavatel** zadejte název existujícího dodavatele.
4. Vyberte akci **Kopírovat z dokladu**.
5. Na stránce **Kopie nákupního dokladu** vyberte v poli **Typ dokladu** možnost **Zaúčtovaná faktura**.
6. Vyberte pole **Číslo dokladu**, chcete-li otevřít stránku **Účtované nákupní faktury** a pak vyberte zaúčtovanou nákupní fakturu obsahující řádky, které chcete stornovat.
7. Zaškrtněte políčko **Přepočítat řádky**, pokud chcete, aby byly kopírované řádky zúčtovaných nákupních faktur aktualizovány o jakékoli změny v ceně zboží a jednotkových nákladech od zaúčtování faktury.
8. Vyberte tlačítko **OK**. Zkopírované řádky faktury jsou vloženy do nákupního dobropisu.
9. Vyplňte nákupní dobropis, jak je vysvětleno v [Vytvoření dobropisu na nákup ze zaúčtované nákupní faktury](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

## Vytvoření objednávky nákupní vratky na základě jednoho nebo více zaúčtovaných nákupních dokladů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Objednávky nákupní vratky** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Podle potřeby vyplňte pole na záložce **Obecné**.
4. Na záložce **Řádky** vyplňte řádky ručně nebo zkopírujte informace z jiných dokladů a řádky vyplňte automaticky:

   - Pomocí funkce **Získat účt. řádky pro stornování** zkopírujte jeden nebo více řádků zaúčtovaných dokladů z jednoho nebo více zaúčtovaných dokladů. Tato funkce vždy přesně stornuje náklady z řádku zaúčtovaného dokladu. Tato funkce je popsána v následujících krocích.
   - Pomocí funkce **Kopírovat z dokladu** zkopírujte existující doklad do objednávky vratky. Pomocí této funkce zkopírujete celý doklad. Může to být buď zaúčtovaný doklad, nebo doklad, který ještě není zaúčtován. Tato funkce umožňuje vrácení přesných nákladů pouze tehdy, je-li na stránce **Nastavení prodeje a pohledávek** zaškrtnuto políčko **Nutné vrác.přesn.nákladů**.

4. Vyberte akci **Získat účt. řádky pro stornování**.
5. V horní části stránky **Účtované řádky nákupního dokladu** zaškrtněte políčko **Zobrazit pouze vratné řádky**, pokud chcete vidět pouze řádky, jejichž množství dosud nebylo stornováno. Například, pokud již bylo stornováno množství zaúčtované nákupní faktury, možná nebudete chtít zahrnout toto množství do nového dokladu vratky.

   > [!NOTE]
   > Toto pole funguje pouze pro zaúčtované příjemky a zaúčtované řádky faktur, nikoli pro řádky zaúčtovaných vratek nebo zaúčtovaných dobropisů.

   Na levé straně stránky jsou uvedeny různé typy dokladů a číslo v závorce zobrazuje počet dostupných dokladů pro každý typ.

6. V poli **Filtr typů dokladů** vyberte typ řádků zaúčtovaných dokladů, které chcete použít.
7. Vyberte řádky, které chcete zkopírovat do nového dokladu.

   > [!NOTE]
   > Pokud použijete kombinaci kláves Ctrl+A k výběru všech řádků, budou zkopírovány všechny řádky v nastaveném filtru, ale filtr **Zobrazit pouze vratné množství** bude ignorován. Předpokládejme například, že jste řádky filtrovali na konkrétní číslo dokladu se dvěma řádky, z nichž jeden již byl vrácen. I když je vybráno pole **Zobrazit pouze vratné množství**, stisknete-li Ctrl+A pro zkopírování všech řádků, zkopírují se oba řádky, nikoli pouze ten, který ještě nebyl vrácen.

8. Stisknutím tlačítka **OK** zkopírujte řádky do nového dokladu.

   Dochází k následujícím procesům:

   - U řádků zaúčtovaných dokladů typu **Zboží** se vytvoří nový řádek s dokladem, který je kopií řádku zaúčtovaného dokladu, s množstvím, které ještě nebylo vráceno. Pole **Vyrovnat položkou zboží** se vyplní podle potřeby číslem položky zboží v řádku zaúčtovaného dokladu.

   - Pro zaúčtované řádky dokladu, které nejsou typu **Zboží**, například poplatky za zboží, je vytvořen nový řádek dokladu, který je kopií původního řádku zaúčtovaného dokladu.

   - Vypočítá pole **Pořizovací cena (LM)** na novém řádku z nákladů v odpovídajících položkách zboží.

   - Pokud je zkopírovaným dokladem zaúčtovaná dodávka, zaúčtovaná příjemka, účtovaná příjemka vratky nebo účtovaná dodávka vratky, jednotková cena se vypočítá automaticky z karty zboží.

   - Pokud je zkopírovaným dokladem zaúčtovaná faktura nebo dobropis, zkopírují se jednotková cena, fakturační slevy a řádkové slevy z řádku zaúčtovaného dokladu.

   - Pokud řádek zaúčtovaného dokladu obsahuje řádky pro sledování zboží, pole **Vyrovnat položkou zboží** na řádcích pro sledování zboží je vyplněno příslušnými čísly polžek zboží z řádků pro sledování účtovaného zboží.
   Při kopírování z zaúčtované faktury nebo zaúčtovaného dobropisu aplikace zkopíruje všechny příslušné fakturační slevy a řádkové slevy jako platné v době zaúčtování tohoto dokladu z řádku zaúčtovaného dokladu do nového řádku dokladu. Uvědomte si však, že pokud je aktivována možnost **Výpočet  fakt. slevy** na stránce **Nastavení nákupu a závazků** poté, co zaúčtujete nový řádek dokladu, bude nově vypočítána sleva na faktuře. Částka na řádku pro nový řádek se proto může lišit od částky na řádku pro řádek zaúčtovaného dokladu, v závislosti na novém výpočtu slevy na faktuře.

   > [!NOTE]
   > Pokud již byla část množství na řádku zaúčtovaného dokladu stornována, prodána nebo spotřebována, vytvoří se řádek pouze pro množství, které zůstává v zásobách nebo které nebylo vráceno. Pokud již bylo stornováno celé množství zaúčtovaného řádku dokladu, nebude vytvořen nový řádek dokladu.
   > Pokud je tok zboží v zaúčtovaném dokladu stejný jako tok zboží v novém dokladu, vytvoří se kopie původního řádku zaúčtovaného dokladu v novém dokladu. Pole **Vyrovnáno položkou zboží** není vyplněno, protože v tomto případě není možné stornovat přesné náklady. Pokud například použijete funkci **Získat účt. řádky pro stornování** k získání zaúčtovaného řádku nákupního dobropisu pro nový nákupní dobropis, zkopíruje se do nového dobropisu pouze původní zaúčtovaný řádek dobropisu.
   > 
8. Na stránce **Objednávka nákupní vratky** v poli **Kód příčiny vratky** na každém řádku vyberte důvod vrácení.
9. Vyberte akci **Účtovat**.

## Vytvoření náhradní objednávky z objednávky nákupní vratky
Můžete se dohodnout se svým dodavatelem, že vám zakoupené zboží odškodní tím, že jej vymění. Náhradní zboží může být stejné nebo odlišné. K této situaci může dojít, pokud dodavatel omylem dodal nesprávné zboží.
1. Na stránce **Objednávka nákupní vratky** pro aktivní proces vrácení na prázdném řádku vytvořte zápornou položku pro náhradní zboží vložením záporné částky do pole **Množství**.
2. Vyberte akci **Přesunout záporné řádky**.
3. Na stránce **Přesun záporných nák.řádků** vyplňte pole podle potřeby.
4. Vyberte tlačítko **OK**. Záporný řádek se z objednávky nákupní vratky odstraní a vytvoří se nová objednávka. Pro více informací navštivte [Záznam nákupu](purchasing-how-record-purchases.md).

## Vytvoření příspěvku na nákup
Pokud od svého dodavatele obdržíte zboží, které není to, co jste chtěli, například pokud je mírně poškozené, nesprávné barvy nebo nesprávné velikosti, může vám dodavatel nabídnout příspěvek na nákup.

Tuto sníženou nákupní cenu můžete zaúčtovat jako poplatek za zboží na dobropis nebo vrátit objednávku a propojit ji s účtovanou příjemkou. Následující text popisuje objednávku nákupní vratky, ale stejné kroky platí pro nákupní dobropis.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní dobropisy** a poté vyberte související odkaz.
2. Vyberte akci **Nový** a otevřete nový prázdny nákupní dobropis.
3. Vyplňte záhlaví dobropisu informacemi o dodavateli, který vám poslal příspěvek na nákup.
4. na záložce **Řádky** v poli **Typ** vyberte **Poplatek (zboží)**.
5. V poli **Číslo** vyberte příslušnou hodnotu poplatku za zboží.

   Můžete vytvořit speciální číslo poplatku za zboží, které by pokrylo příspěvek na nákup.
6. Do pole **Množství** zadejte **1**.
7. Do pole **Nákupní cena** zadejte částku příspěvku na nákup.
8. Přiřaďte příspěvek na nákup jako poplatek za zboží v zaúčtované příjemce. Pro více informací navštivte [Použití poplatků za zboží k účtování dalších obchodních nákladů](payables-how-assign-item-charges.md). Po přiřazení příspěvku se vraťte na stránku **Nákupní dobropis**.

Při zaúčtování objednávky nákupní vratky se příspěvek na nákup přičte k příslušné částce nákupní položky. Tímto způsobem můžete udržovat přesné ocenění zásob.

## Sloučení vrácených zásilek
Pokud chcete vrátit zboží, na které se vztahují různé objednávky na vrácení zboží, stejnému dodavateli, můžete použít funkci **Kombinovat dodávky vratky**.

Při dodání zboží zaúčtujte související objednávky nákupní vratky, jak byly odeslány, a vytvoří se tak zásilky s vrácením nákupu.

Až budete připraveni k fakturaci tohoto zboží, můžete místo fakturace každé objednávky nákupní vratky samostatně vytvořit nákupní dobropis a automaticky zkopírovat zaúčtované řádky dodávky nákupní vratky do tohoto dokladu. Poté můžete zaúčtovat nákupní dobropis a pohodlně fakturovat všechny otevřené objednávky na vrácení nákupu současně.

Když jsou vrácené zásilky kombinovány v dobropisu a zaúčtovány, vytvoří se pro fakturované řádky účtovaný nákupní dobropis. Pole **Fakturované množství** na původní vrácené objednávce se aktualizuje na základě fakturovaného množství. Tato původní objednávka nákupní vratky však není odstraněna, a to ani v případě, že byla plně přijata a fakturována, a proto je nutné objednávku nákupní vratky odstranit ručně.

> [!NOTE]
Následující postup předpokládá, že existuje několik objednávek nákupní vratky pro dodavatele a že byly zaúčtovány jako dodané.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní dobropisy** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Na záložce **Obecné** vyplňte pole podle potřeby.
4. Vyberte akci **Kopie řádků dodávky vratky**.
5. Vyberte více řádků pro vrácení zásilky, které chcete zahrnout do faktury.

   Pokud byla vybrána nesprávná vrácená zásilka nebo chcete začít znovu, stačí smazat řádky v dobropisu a poté znovu použít funkci **Kopie řádků dodávky vratky**.
6. Vyberte akci **Účtovat**.

### Odebrání otevřených objednávek nákupní vratky po kombinovaném zaúčtování dodávky vratky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Odstranit fakturované obj. nákupní vratky** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole a poté zvolte tlačítko **OK**.
3. Alternativně můžete jednotlivé objednávky nákupní vratky odstranit ručně.

## Viz související školení na [Microsoft Learn](/learn/paths/return-items-dynamics-365-business-central/)

## Viz také
[Nákup](purchasing-manage-purchasing.md)  
[Záznam nákupu](purchasing-how-record-purchases.md)  
[Opravit nebo zrušit nezaplacené nákupní faktury](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
