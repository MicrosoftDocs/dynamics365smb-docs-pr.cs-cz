---
title: Process Sales Returns or Cancellations | Microsoft Docs
description: Describes how to create a sales credit memo, directly or through a sales return order, to process a return, cancellation, or reimbursement for items or services you have been received payment for.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2020
ms.author: edupont

---
# Zpracování prodejních vratek nebo zrušení
Pokud chce zákazník vrátit zboží nebo chce, aby mu byly vráceny peníze za zboží nebo služby, které jste mu prodali a obdrželi platbu, musíte vytvořit a účtovat  prodejní dobropis, který specifikuje požadovanou změnu. Chcete-li zahrnout správné informace o prodejní faktuře, můžete vytvořit prodejní dobropis přímo z účtované prodejní faktury nebo můžete vytvořit nový prodejní dobropis se zkopírovanými fakturačními údaji.

Pokud potřebujete větší kontrolu nad procesem prodejní vratky, například nad doklady skladu pro zpracování zboží nebo lepší přehled při příjmu zboží z více prodejních dokladů s jednou prodejní vratkou, můžete vytvořit objednávky prodejní vratky. Objednávka prodejní vratky automaticky vydá související prodejní dobropis a další doklady týkající se vrácení, například náhradní prodejní objednávku, pokud je potřeba. Více informací viz [Vytvoření objednávky prodejní vratky na základě jednoho nebo více účtovaných prodejních dokladů](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).

> [!POZNÁMKA]  
> Pokud účtovaná prodejní faktura ještě nebyla zaplacena, můžete pro obrácení transakcí použít funkce **Opravit** nebo **Zrušit** na účtované prodejní faktuře. Tyto funkce fungují pouze pro nezaplacené faktury a nepodporují částečné vrácení nebo zrušení. Více informací viz [Oprava nebo zrušení nezaplacených prodejních faktur](sales-how-correct-cancel-sales-invoice.md).

Vrácení nebo náhrada se může týkat pouze některého zboží nebo služeb na původní prodejní faktuře. V takovém případě je nutné upravit informace na řádcích na prodejním dobropisu nebo objednávce prodejní vratky. Když účtujete prodejní dobropis nebo objednávku prodejní vratky, prodejní doklady, které jsou změnou ovlivněny, jsou stornovány a pro zákazníka lze vytvořit refundaci platby. Více informací viz [Provádění plateb](payables-make-payments.md).

Kromě původní účtované prodejní faktury můžete použít prodejní dobropis nebo objednávku prodejní vratky na jiné prodejní doklady, například jinou účtovanou prodejní fakturu, protože zákazník také vrací zboží dodané s touto fakturou.

Účtovaný prodejní dobropis můžete odeslat zákazníkovi, abyste potvrdili vrácení nebo zrušení a sdělili, že související hodnota bude vrácena, například při vrácení zboží.

Účtování dobropisu také vrátí veškeré poplatky za zboží, které byly přiřazeny k účtovanému dokumentu, tak aby položky hodnot zboží byly stejné jako před přiřazením poplatku za zboží.

> [!POZNÁMKA]
> Aspekty účetnictví prodejních vratek, jako jsou platby zákazníkům jako refundace, jsou považovány za účetní práce a nejsou zde popsány. Více informací viz [Správa závazků](payables-manage-payables.md).

## Zásoby a ocenění
Chcete-li zachovat správné ocenění zásob, obvykle chcete vrátit vrácené zboží zpět do skladu za pořizovací cenu, za kterou byly prodány, nikoli za aktuální cenu. Toto se označuje jako přesné obrácení nákladů.

Pro automatické přiřazení přesného stornování nákladů existují dvě funkce.

| Funkce | Popis |
|------------------|---------------------------------------|  
| Funkce **Získat účtované řádky dokladu ke stornování** na stránce **Objednávka prodejní vratky**. | Zkopíruje řádky jednoho nebo více účtovaných dokladů, které mají být vráceny do objednávky prodejní vratky. Více informací viz [Vytvoření objednávky prodejní vratky na základě jednoho nebo více účtovaných prodejních dokladů](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents). |
| Funkce **Kopírovat z dokladu** na stránkách **Prodejní dobropis** a **Objednávka prodejní vratky** | Zkopíruje záhlaví i řádky jednoho účtovaného dokladu, který má být stornován. <br /><br /> Vyžaduje, aby bylo zaškrtnuto políčko **Nutné přesné vrácení nákladů** na stránce **Nastavení prodeje a pohledávek**. |

Chcete-li přiřadit přesné stornování nákladů ručně, musíte zvolit pole **Vyrovnáno položkou zboží** na libovolném typu řádku dokladu vratky a potom vybrat číslo původní prodejní položky. Tím propojíte prodejní dobropis nebo objednávku prodejní vratky s původní prodejní položkou a zajistíte, že zboží bude oceněno původní pořizovací cenou.

Více informací viz [Podrobnosti návrhu: Zásoby a ocenění](design-details-inventory-costing.md).

## Vytvoření prodejního dobropisu z účtované prodejní faktury
1. Zvolte ikonu ![Žárovky, která otevře funkci](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Účtované prodejní faktury** a vyberte související odkaz.
2. Na stránce **Účtované prodejní faktury** vyberte účtovanou prodejní fakturu, kterou chcete stornovat, a pak zvolte akci **Vytvořit opravný dobropis.**

   Záhlaví prodejního dobropisu obsahuje některé informace z účtované prodejní faktury. Toto můžete upravit například novými informacemi, které odrážejí dohodu o navrácení.
3. Upravte informace na řádcích podle dohody, například množství vráceného zboží nebo částku k vrácení.
4. Zvolte akci **Vyrovnat položky**.
5. Na stránce **Vyrovnat položky zákazníka** vyberte řádek s účtovaným prodejním dokladem, na který chcete vyrovnat prodejní dobropis, a pak zvolte akci **ID vyrovnání**.

   Identifikátor prodejního dobropisu se zobrazí v poli **ID vyrovnání**.
6. Do pole **Částka k vyrovnání** zadejte částku, kterou chcete použít, pokud je menší než původní částka.

   V dolní části stránky **Vyrovnat položky zákazníka** se zobrazí celková částka, která má být vyrovnáno pro storno všech zapojených položek, konkrétně pokud je hodnota v poli **Zůstatek** nulová.
7. Zvolte tlačítko **OK**. Když účtujete prodejní dobropis, bude vyrovnán s účtovanými prodejními doklady.

   Po vytvoření nebo úpravě řádků prodejního dobropisu a zadání jednoho nebo více vyrovnání můžete prodejní dobropis účtovat.
8. Zvolte akci **Účtovat a Odeslat**.

Otevře se dialogové okno **Zaúčtovat a odeslat potvrzení**, které zobrazuje upřednostňované metody odeslání pro zákazníka. Způsob odesílání můžete změnit výběrem vyhledávacího tlačítka v poli **Odeslat doklad**. Více informací viz [Nastavení profilů odesílání dokladů](sales-how-setup-document-send-profiles.md).

Účtované prodejní doklady, na které jste dobropis vyrovnáli, jsou nyní stornovány a pro zákazníka lze vytvořit refundační platbu. Prodejní dobropis je odebrán a nahrazen novým dokladem v seznamu účtovaných prodejních dobropisů.

## Vytvoření prodejního dobropisu zkopírováním účtované prodejní faktury
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Prodejní dobropisy** a poté vyberte související odkaz.
2. Zvolte akci **Nový** pro otevření nového prázdného prodejního dobropisu.
3. Do pole **Zákazník** zadejte jméno stávajícího zákazníka.
4. Zvolte akci **Kopírovat z dokladu**.
5. Na stránce **Kopírovat prodejní doklad** vyberte v poli **Typ dokladu** **Zaúčtovaná faktura**.
6. Zvolte pole **Číslo dokladu**, chcete-li otevřít stránku **Účtované prodejní faktury,** a pak vyberte účtovanou prodejní fakturu obsahující řádky, které chcete stornovat.
7. Zaškrtněte políčko **Přepočítat řádky**, pokud chcete, aby se zkopírované řádky účtované prodejní faktury aktualizovaly o jakékoli změny v ceně zboží a jednotkových nákladech od odeslání faktury.
8. Zvolte tlačítko **OK**. Zkopírované řádky faktury se vloží do prodejního dobropisu.
9. Vyplňte prodejní dobropis, jak je vysvětleno ve [Vytvoření prodejního dobropisu z účtované prodejní faktury](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## Chcete-li vytvořit objednávku prodejní vratky na základě jednoho nebo více účtovaných prodejních dokladů
1. Vyberte ikonu ![Žárovky, která otevře funkci](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Objednávky prodejní vratky** a pak zvolte související odkaz.
2. Vyberte akci **Nový**.
3. Vyplňte pole na pevné záložce **Obecné** podle potřeby.
4. Na pevné záložce **Řádky** vyplňte řádky ručně nebo zkopírujte informace z jiných dokladů pro vyplnění řádků automaticky:

   - Pomocí funkce **Získat řádky účtovaných dokladů k obrácení** můžete zkopírovat jeden nebo více řádků účtovaných dokladů z jednoho nebo více účtovaných dokladů. Tato funkce vždy přesně obrátí náklady z řádku účtovaného dokladu. Tato funkce je popsána v následujících krocích.
   - Pomocí funkce **Kopírovat z dokladu** zkopírujte existující doklad do objednávky vratky. Pomocí této funkce zkopírujete celý doklad. Může to být buď účtovaný doklad, nebo doklad, který ještě není účtován. Tato funkce umožňuje přesné obrácení nákladů pouze v případě, že je na stránce **Nastavení prodeje a pohledávek** zaškrtnuto políčko **Nutné přesné vrácení nákladů**.

5. Zvolte akci **Získat účtované řádky dokladu ke stornování**.
6. V horní části stránky **Řádky účtovaného prodejního dokladu** zaškrtněte políčko **Zobrazit pouze vratné řádky**, pokud chcete zobrazit pouze řádky, které mají množství, které ještě nebylo vráceno. Například pokud již bylo množství účtované prodejní faktury vráceno, možná nebudete chtít toto množství vrátit na novém dokladu prodejní vratky.

   > [!POZNÁMKA]  
   > Toto pole funguje pouze pro účtované dodávky a účtované řádky faktury, nikoli pro účtované vratky nebo účtované řádky dobropisu.

   Na levé straně stránky jsou uvedeny různé typy dokladů a číslo v závorkách udává počet dostupných dokladů pro každý typ dokladu.

7. V poli **Filtr typů dokladů** vyberte typ účtovaných řádků dokladu, které chcete použít.
8. Vyberte řádky, které chcete zkopírovat do nového dokladu.

   > [!POZNÁMKA]  
   > Pokud pomocí Ctrl+A vyberete všechny řádky, zkopírují se všechny řádky ve filtru, který jste nastavili, ale filtr **Zobrazit pouze reverzibilní množství** je ignorován. Předpokládejme například, že jste vyfiltrovali řádky na konkrétní číslo dokladu se dvěma řádky, z nichž jeden již byl vrácen. I když je vybráno pole **Zobrazit pouze reverzibilní množství**, stisknutím kláves Ctrl+A pro zkopírování všech řádků, se zkopírují oba řádky, nikoli pouze ten, který ještě nebyl obrácen.

9. Zvolte tlačítko **OK**, chcete-li řádky zkopírovat do nového dokladu.

   Nastanou následující procesy:

   - Pro řádky účtovaných dokladů typu **Zboží** se vytvoří nový řádek dokladu, který je kopií řádku účtovaného dokladu s množstvím, které ještě nebylo obráceno. Pole **Vyrovnáno položkou zboží** je podle potřeby vyplněno číslem položky zboží účtovaného dokladu.

   - Pro účtované řádky dokladu, které nejsou typu **Zboží**, například poplatky za zboží, je vytvořen nový řádek dokladu, který je kopií původního účtovaného řádku dokladu.

   - Vypočítá pole **Pořizovací cena (LM)** na novém řádku z nákladů na odpovídající položky zboží.

   - Pokud je zkopírovaným dokladem účtovaná dodávka, účtovaná příjemka, účtovaná příjemka vratky nebo účtovaná dodávka vratky, jednotková cena se vypočítá automaticky z karty zboží.

   - Pokud je zkopírovaným dokladem účtovaná faktura nebo dobropis, zkopíruje se jednotková cena, slevy na faktuře a řádkové slevy z řádku účtovaného dokladu.

   - Pokud řádek účtovaného dokladu obsahuje řádky pro sledování zboží, pole **Vyrovnáno položkou zboží** na řádcích pro sledování zboží je vyplněno příslušnými čísly položek zboží ze sledovacích řádků účtovaných zboží.

   Při kopírování z účtované faktury nebo účtovaného dobropisu aplikace zkopíruje všechny příslušné fakturační slevy a řádkové slevy platné v době účtování tohoto dokladu z účtovaného řádku dokladu do nového řádku dokladu. Uvědomte si však, že pokud je aktivovaná možnost **Výpočet fakt. slevy** na stránce **Nastavení prodeje a pohledávek**, pak bude fakturační sleva nově vypočtena při účtování nového řádku dokladu. Částka řádku pro nový řádek se proto může lišit od částky řádku účtovaného dokladu v závislosti na novém výpočtu fakturační slevy.

   > [!POZNÁMKA]  
   > Pokud část množství účtovaného řádku dokladu již byla obrácena nebo prodána nebo spotřebována, vytvoří se řádek pouze pro množství, které zůstane v zásobách nebo které nebylo vráceno. Pokud již bylo obráceno celé množství účtovaného řádku dokladu, nový řádek dokladu se nevytvoří.
   >
   > Pokud je tok zboží v účtovaném dokladu stejný jako tok zboží v novém dokladu, vytvoří se v novém dokladu kopie původního řádku účtovaného dokladu. Pole **Vyrovnáno položkou zboží** není vyplněno, protože v tomto případě není možné přesné obrácení nákladů. Například pokud použijete funkci **Získat účtované řádky dokladu pro obrácení** k získání účtovaného řádku dobropisu k novému dobropisu, do nového dobropisu se zkopíruje pouze původní účtovaný řádek dobropisu. .

10. Na stránce **Objednávka prodejní vratky** vyberte v poli **Kód příčiny vratky** na každém řádku důvod vrácení.
11. Zvolte akci **účtovat**.

## Vytvoření náhradní prodejní objednávky z objednávky prodejní vratky
Můžete se rozhodnout kompenzovat zákazníkovi zboží, které jste mu prodali, jeho výměnou. Můžete provést výměnu za stejné zboží nebo jiné zboží. Tato situace může nastat, například pokud jste zákazníkovi omylem dodali nesprávné zboží.

1. Na stránce **Objednávka prodejní vratky** pro aktivní proces vratky vytvořte na prázdném řádku zápornou položku pro náhradní zboží vložením záporné částky do pole **Množství**.
2. Vyberte akci **Přesunout záporné řádky**.
3. Na stránce **Přesunout záporné prodejní řádky** vyplňte pole podle potřeby.
4. Zvolte tlačítko **OK**. Záporný řádek pro náhradní zboží je odstraněn z objednávky prodejní vratky a vložen na novou stránku **Prodejní objednávky**. Více informací viz [Prodávání produktů](sales-how-sell-products.md).

## Vytvoření dokladů souvisejících s objednávkou prodejní vratky.
Během procesu prodejní vratky můžete automaticky vytvořit náhradní prodejní objednávky, objednávky nákupní vratky a náhradní nákupní objednávky. To je užitečné například v situacích, kdy chcete zpracovat zboží se zárukami poskytovanými dodavateli.

1. Na stránce **Objednávka prodejní vratky** pro aktivní proces vrácení zvolte akci **Vytvořit dokl.spoj.s vratkou**.
2. Pokud chcete automaticky vytvářet doklady dodavatele, do pole **Číslo dodavatele** zadejte číslo dodavatele.
3. Pokud musí být vrácené zboží vráceno dodavateli, vyberte zaškrtávací políčko **Vytvořit nák. obj. vratky**.
4. Pokud je nutné vrácenou položku objednat u dodavatele, zaškrtněte políčko **Vytvořit nákupní objednávku**.
5. Pokud je třeba vytvořit náhradní prodejní objednávku, zaškrtněte políčko **Vytvořit prodejní objednávku**.

## Vytvoření poplatku za doplnění zásob
Můžete se rozhodnout účtovat zákazníkovi poplatek za doplnění zásob na pokrytí fyzických nákladů na manipulaci s vrácením zboží. K tomu může dojít, například pokud si zákazník omylem objednal nesprávné zboží nebo změnil názor po obdržení zboží, které jste mu prodali.

Tuto zvýšenou cenu můžete účtovat jako poplatek za zboží v dobropisu nebo v objednávce vratky a přiřadit ji k účtované dodávce. Následující text popisuje objednávku prodejní vratky, ale stejné kroky platí pro prodejní dobropis.

1. Otevřete stránku **Objednávka prodejní vratky** pro aktivní proces vrácení.
2. Na novém řádku vyberte v poli **Typ** **Poplatek (zboží)**.
3. Vyplňte pole jako u každého řádku s účtováním zboží. Více informací viz [Používání poplatků za zboží k účtování dalších obchodních nákladů](payables-how-assign-item-charges.md).

Při účtování objednávky prodejní vratky se k příslušné částce prodejní položky přidá poplatek za zaskladnění. Tímto způsobem můžete udržovat přesné ocenění zásob.

## Vytvoření příspěvku na prodej
Pokud zákazník obdržel mírně poškozené zboží nebo zboží obdržel pozdě, můžete mu zaslat dobropis se sníženou cenou.  
Tuto sníženou cenu můžete zaúčtovat jako poplatek za zboží v dobropisu nebo v objednávce vratky a přiřadit ji k účtované dodávce. Následující text popisuje prodejní dobropis, ale stejné kroky platí pro objednávku prodejní vratky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Prodejní dobropisy** a poté vyberte související odkaz.
2. Zvolte akci **Nový** pro otevření nového prázdného prodejního dobropisu.
3. Vyplňte záhlaví dobropisu relevantními informacemi o zákazníkovi, kterému chcete poskytnout příspěvek na prodej.
4. Na pevné záložce **Řádky** v poli **Typ** vyberte **Poplatek (zboží)**.
5. V poli **Číslo** vyberte příslušnou hodnotu poplatku za zboží.  
   Možná budete chtít vytvořit speciální číslo poplatku za zboží k pokrytí příspěvků na prodej.
6. Do pole **Množství** zadejte **1**.
7. Do pole **Jednotková cena** zadejte částku příspěvku na prodej.
8. Přiřaďte příspěvek na prodej jako poplatek za zboží k zboží v účtované dodávce. Více informací viz [Používání poplatků za zboží k účtování dalších obchodních nákladů](payables-how-assign-item-charges.md). Pokud jste přidělili příspěvek, vraťte se na stránku **Prodejní dobropis**.

Při účtování objednávky prodejní vratky se příspěvek na prodej přidá k příslušné částce položky prodeje. Tímto způsobem můžete udržovat přesné ocenění zásob.

## Kombinování příjemek vratky
Příjemky vratky můžete kombinovat, pokud zákazník vrátí několik zboží, které jsou pokryty různými objednávkami prodejní vratky.

Když obdržíte zboží do skladu, účtujte příslušné objednávky prodejní vratky jako přijaté. Tím se vytvoří účtovaná příjemka vratky.

Až budete připraveni fakturovat tohoto zákazníka, můžete namísto fakturace každé objednávky prodejní vratky samostatně vytvořit prodejní dobropis a automaticky zkopírovat účtované řádky příjemky vratky do tohoto dokladu. Poté můžete účtovat prodejní dobropis a pohodlně fakturovat všechny otevřené objednávky prodejních vratek najednou.

Chcete-li kombinovat příjemky vratky, musí být na stránce **Karta zákazníka** zaškrtnuto políčko **Kombinovat dodávky**.

### Ručné kombinování příjemek vratky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Prodejní dobropis** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Na pevné záložce **Obecné** vyplňte pole podle potřeby.
4. Vyberte akci **Získat řádky příjemky vratky**.
5. Vyberte řádky příjmu vratky, které chcete zahrnout do dobropisu:

   - Chcete-li vložit všechny řádky, vyberte všechny řádky a klikněte na tlačítko **OK**.

   - Chcete-li vložit konkrétní řádky, vyberte řádky a klikněte na tlačítko **OK**.

6. Pokud byl vybrán nesprávný řádek dodávky nebo chcete začít znovu, můžete jednoduše řádky v dobropisu smazat a znovu spustit funkci **Získat řádky příjemky vratky**.
7. Účtování faktury.

### Automatické kombinování příjemek vratky
Můžete automaticky kombinovat příjemky vratky a mít možnost automatického účtování dobropisů pomocí funkce **Kombinovat příjemky vratky.**

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Kombinovat příjemky vratky** a poté vyberte související odkaz.
2. Na stránce **Kombinovat příjemky vratky** vyplňte pole a vyberte příslušné příjemky vratky.
3. Zaškrtněte políčko **Účtovat dobropisy**. Pokud ne, musíte ručně účtovat výsledné nákupní dobropisy.
4. Zvolte tlačítko **OK**.

### Odebrání přijaté a fakturované objednávky vratky
Když tímto způsobem fakturujete příjemky vratky, objednávky vratky, ze kterých byly účtovány příjemky vratky, stále existují, i když byly plně přijaty a fakturovány.

Když se v dobropisu zkombinují příjemky vratky a účtují se, účtované prodejní dobropisy se vytvoří pro připsané řádky. Pole **Fakturované množství** v původní objednávce prodejní vratky se aktualizuje na základě fakturovaného množství.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Smazat fakturované objednávky prodejní vratky** a poté vyberte odkaz.
2. Do pole filtru **Číslo** zadejte, které objednávky vratky mají být odstraněny.
3. Zvolte tlačítko **OK**.

Alternativně můžete jednotlivé objednávky prodejní vratky odstranit ručně.

## Viz související školení na [Microsoft Learn](/learn/paths/return-items-dynamics-365-business-central/)

## Viz také

[Prodej](sales-manage-sales.md)  
[Nastavení prodeje](sales-setup-sales.md)  
[Správa závazků](payables-manage-payables.md)  
[Odesílání dokumentů e-mailem](ui-how-send-documents-email.md)  
[Zpracování vrácení nebo zrušení nákupu](purchasing-how-process-purchase-returns-cancellations.md)
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
