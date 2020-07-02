---
title: Use OCR to Turn PDF into E-Invoices| Microsoft Docs
description: Describes how you can use an OCR service to convert incoming PDF or image files to electronic documents.
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2019
ms.author: sgroespe

---
# Použití funkce OCR k převedení souborů PDF a obrázkových souborů do elektronických dokumentů
Ze souborů PDF nebo obrázkových souborů, které obdržíte od svých obchodních partnerů, můžete pomocí externí služby OCR (Optical Character Recognition) generovat elektronické dokumenty, které lze převést na záznamy dokumentů v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pokud například od dodavatele obdržíte fakturu ve formátu PDF, můžete ji odeslat do služby OCR ze stránky **Došlé doklady**. Toto je popsáno v první proceduře.

Jako alternativu k odeslání souboru ze stránky **Příchozí dokumenty**, můžete odeslat soubor službě OCR e-mailem. Poté, když obdržíte elektronický dokument zpět, automaticky se vytvoří související záznam příchozího dokumentu. Toto je popsáno v druhé proceduře.

Po několika sekundách obdržíte soubor zpět od služby OCR jako elektronickou fakturu, kterou lze převést na nákupní fakturu dodavatele. Toto je popsáno v třetí proceduře.

Vzhledem k tomu, že OCR je založen na optickém rozpoznávání, je pravděpodobné, že služba OCR interpretuje znaky ve vašem souboru PDF nebo obrázkovém souborů nesprávně, když například nejprve zpracuje dokumenty konkrétního dodavatele. Nesmí se stát, že bude interpretovat logo společnosti jako jméno prodávajícího nebo nesprávně interpretovat celkovou částku na účtenku z důvodu jejího uspořádání. Chcete-li se těmto chybám vyhnout, můžete chyby opravit v samostatné verzi na stránce **Došlý doklad**. Poté odešlete opravy zpět do služby OCR, abyste ji naučili správně interpretovat konkrétní znaky při příštím zpracování PDF nebo obrazového dokumentu u stejného dodavatele. Další informace naleznete v [Zlepšení služby OCR k vyhnutím se chybám](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Přenos souborů do a ze služby OCR je zpracována položka vyhrazená frontou úloh, která se automaticky vytvoří při povolení příslušného připojení služby. Pro více informací navštivte [Nastavení došlých dokladů](across-how-setup-income-documents.md).

## Odeslání souboru PDF nebo obrázku do služby OCR ze stránky **Došlé doklady**
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Došlé doklady** a poté vyberte související odkaz.
2. Vytvořte nový záznam příchozího dokumentu a připojte soubor. Pro více informací navštivte [Vytvoření záznamu došlého dokladu](across-how-create-income-document-records.md).
3. Na stránce **Došlé doklady**, vyberte jeden nebo více řádků a pak zvolte akci **Odeslat do fronty úloh**.

   Hodnota v poli **Stav OCR** se změní na **Připraveno**. Přiložený soubor PDF nebo obrázkový soubor je odeslán do služby OCR frontou úloh podle plánu za předpokladu, že se nevyskytnou žádné chyby.
4. Případně na stránce **Došlé doklady**, vyberte jeden nebo více řádků a poté zvolte akci **Send to OCR Service**.

Hodnota v poli **Stav OCR** se změní na **Odesláno**, za předpokladu, že neexistují žádné chyby.

## Odeslání souboru PDF nebo obrázku do služby OCR e-mailem
Z vaší e-mailové aplikace můžete odeslat e-mailové zprávy poskytovateli služby OCR s připojeným souborem PDF nebo obrázkovým souborem. Informace o e-mailové adrese, na kterou chcete odeslat, naleznete na webu poskytovatele služeb OCR.

Protože pro soubor neexistuje žádný záznam příchozího dokumentu, bude nový záznam vytvořen automaticky na stránce **Příchozí dokumenty** jakmile obdržíte výsledný elektronický dokument ze služby OCR. Pro více informací navštivte [Vytvoření záznamu došlého dokladu](across-how-create-income-document-records.md).

> [!NOTE]
> Pokud pracujete s tabletem nebo telefonem, můžete soubor odeslat službě OCR, jakmile pořídíte fotografii dokumentu nebo tak, že vytvoříte přímo příchozí dokument. Další informace naleznete v části [Vytvoření záznamu příchozího dokumentu pořízením fotografie](across-how-create-income-document-records.md#to-create-an-incoming-document-record-by-taking-a-photo).

## Získání výsledného elektronického dokumentu ze služby OCR.
Elektronický dokument, který je vytvořen službou OCR ze souboru PDF nebo obrázkového souboru, je automaticky přijat na stránku **Příchozí dokumenty** položkou fronty úloh, která je nastavena při aktivaci služby OCR.

Pokud nepoužíváte frontu úloh nebo chcete přijmout dokončený dokument OCR dřív, než je v rozvrhu fronty úloh tlačítko **Přijmout ze služby OCR**. Tím získáte všechny dokumenty, které jsou vyplněny službou OCR.

> [!NOTE]
> Pokud je služba OCR nastavena tak, aby vyžadovala manuální ověření zpracovávaných dokumentů, poté bude pole **Stav OCR** obsahovat **Čeká na ověření**. V takovém případě proveďte následující kroky pro přihlášení k webové stránce služby OCR, abyste ručně ověřili dokument OCR.

1. Na poli **Stav OCR**, zvolte hypertextový odkaz **Čeká na ověření**.
2. Na webu služby OCR se přihlaste pomocí přihlašovacích údajů vašeho účtu služby OCR. Toto jsou pověření, která jste použili při nastavení služby. Pro více informací navštivte [Nastavení služby OCR](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   Zobrazí se informace o dokumentu OCR, které zobrazují zdrojový obsah souboru PDF nebo obrázkového souboru a výsledné hodnoty pole OCR.
3. Zkontrolujte různé hodnoty polí a ručně upravte nebo zadejte hodnoty v polích, které služba OCR označila za nejisté.
4. Zvolte tlačítko **OK**. Proces OCR je dokončen a výsledný elektronický dokument je odeslán na stránku **Došlé doklady** v [!INCLUDE[d365fin](includes/d365fin_md.md)], podle plánu fronty úloh.
5. Opakujte krok 4 pro ověření jakéhokoliv jiného dokumentu OCR.

Nyní můžete manuálně nebo automaticky vytvářet záznamy dokumentů pro přijaté elektronické dokumenty v [!INCLUDE[d365fin](includes/d365fin_md.md)], ručně nebo automaticky. Další informace naleznete v dalším postupu. Nový záznam příchozího dokumentu můžete také připojit k existujícímu zaúčtovanému či nezaúčtovanému dokumentu, takže zdrojový soubor je snadno přístupný z aplikace [!INCLUDE[d365fin](includes/d365fin_md.md)]. Další informace naleznete v části [Proces příchozích dokumentů](across-process-income-documents.md).

## Vytvoření nákupní faktury z elektronického dokumentu obdrženého od služby OCR
Následující postup popisuje, jak vytvořit záznam o nákupní faktuře z faktury dodavatele obdržené jako elektronický dokument od služby OCR. Postup je stejný, jako když vytvoříte například řádek finančního deníku z výdajů příjemky, nebo objednávku prodejní vratky od zákazníka.

> [!NOTE]
> Pole**Popis** a **Číslo** na vytvořených řádcích dokumentu budou vyplněny pouze tehdy, pokud jste poprvé namapovali text v dokumentu OCR na dvě pole v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)]. Můžete to udělat buď jako křížové odkazy položky pro řádky dokumentů typu Zboží. Pro více informací navštivte [Křížové odkazy Sledované zboží](inventory-how-use-item-cross-refs.md). Můžete také použít funkci Mapování z účtu na účet. Další informace naleznete v části [Mapování textu příchozího dokladu na účet určitého dodavatele](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Vyberte řádek pro příchozí dokument a pak zvolte akci **Vytvořit doklad**.

V [!INCLUDE[d365fin](includes/d365fin_md.md)] bude vytvořena nákupní faktura na základě informací v elektronickém dokumentu dodavatele, který jste obdrželi od služby OCR. Informace budou vloženy do nové nákupní faktury na základě mapování, které jste definovali jako křížový odkaz nebo jako mapování textu na účet.

Jakékoliv chyby ověřování, které se typicky týkají nesprávných nebo chybějících hlavních dat v [!INCLUDE[d365fin](includes/d365fin_md.md)], se zobrazí v záložce s náhledem **Chyby a varování**. Další informace naleznete v části [Vypořádání se s chybami při přijímání elektronických dokumentů](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### Mapování textu příchozího dokladu na účet určitého dodavatele
U příchozích dokumentů typicky použijete **Mapovat text na účet** abyste definovali, že určitý text na faktuře dodavatele je přijatý ze služby OCR a je mapován na určitý účet dodavatele. Jakákoliv část popisu příchozího dokumentu, která existuje jako mapovací text, znamená, že pole **Číslo** na výsledných dokumentech nebo řádcích finančního deníku je vyplněno dotyčným prodejcem.

Kromě mapování na účet prodejce nebo na finanční účet můžete také mapovat na bankovní účet. To je praktické například u elektronických dokladů o výdajích, které jsou již zaplaceny, vytvořeny na řádcích finančního deníku a připraveny k zaúčtování na bankovní účet.

1. Vyberte příslušný řádek příchozích dokumentů a poté vyberte akci **Mapování textu na účet**. Otevře se stránka **Textové mapování účtů**.
3. Na poli **Text mapování**, zadejte jakýkoli text, který se objeví na dodavatelských fakturách, pro které chcete vytvořit nákupní dokumenty nebo řádky deníku. Můžete zadat až 50 znaků.
4. Na poli **Číslo dodavatele**, zadejte dodavatele, pro který bude výsledný nákupní dokument nebo řádek deníku vytvořen.
5. V poli **Č. účtu  MD**, zadejte účet debetního typu hlavní knihy, který bude vložen do výsledného dokladu o nákupu nebo do řádku deníku typu účet hlavní knihy.
6. V poli **Č. účtu  Dal**, zadejte účet debetního typu hlavní knihy, který bude vložen do výsledného dokladu o nákupu nebo do řádku deníku typu účet hlavní knihy.

   > [!NOTE]
   > Nepoužívejte pole **Typ. zdroje protiúčtu** a pole **Číslo  zdroje protiúčtu** v souvislosti s příchozími dokumenty. Používají se pouze pro automatické odsouhlasení plateb. Další informace naleznete v [Namapovaný text o opakovaných platbách na účtech pro automatické odsouhlasení](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

7. Opakujte kroky 2 až 5 pro všechny texty, pro které chcete automaticky vytvářet dokumenty.

## Řešení chyb při přijímání elektronických dokumentů
1. Na stránce **Došlé doklady**, vyberte řádek elektronického dokumentu přijatého ze služby OCR s chybami. To je označeno hodnotou Chyba v poli **Stav OCR**.
2. Zvolte akci **Upravit** a otevřete stránku **Došlý doklad**.
3. Na záložce s náhledem **Chyby a varování**, vyberte zprávu a poté zvolte akci **Otevřít související záznamy**.
4. Otevře se stránka, která obsahuje nesprávná nebo chybějící data, například kartu dodavatele s chybějící hodnotou pole.
5. Opravte chybu nebo chyby popsané v každé chybové zprávě.
6. Pokračujte ve zpracování příchozího elektronického dokumentu výběrem možnosti **Vytvořit ručně**.
7. Opakujte kroky 5 a 6 pro všechny zbývající chyby, dokud nebude elektronický dokument úspěšně přijat.

## Zlepšení služby OCR, abyste předešli chybám
Vzhledem k tomu, že OCR je založen na optickém rozpoznávání, je pravděpodobné, že služba OCR interpretuje znaky ve vašem souboru PDF nebo obrázkovém souboru nesprávně, když například nejprve zpracuje dokumenty konkrétního dodavatele. Nemusí správně interpretovat logo společnosti jako jméno prodejce nebo může nesprávně interpretovat celkovou částku na příjemce kvůli jejímu rozložení. Chcete-li zabránit takovým chybám, můžete opravit data přijatá službou OCR a poslat službě zpětnou vazbu.

Stránka **Opravy dat OCR**, kterou otevřete ze stránky **Příchozí dokument** zobrazuje pole ze záložky s náhledem **Finanční informace** ve dvou sloupcích, z nichž jedna může být upravitelná pomocí OCR a jedna pouze pro čtení. Pokud zvolíte tlačítko **Poslat zpětnou vazbu OCR** obsah stránky **Oprava dat OCR** je odeslán do služby OCR. Příště, vždy když služba zpracuje soubory PDF nebo obrázkové soubory, které obsahují dotyčná data, budou vaše opravy začleněny, aby se předešlo stejným chybám.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Došlé doklady** a poté vyberte související odkaz.
2. Otevřete záznam příchozího dokumentu, který obsahuje data přijatá službou OCR, které chcete opravit.
3. Na stránce **Příchozí dokumenty**, zvolte akci **Opravit data OCR**.
4. Na stránce **Oprava dat OCR**, přepište data v upravitelném sloupci pro každé pole, které má nesprávnou hodnotu.
5. Zrušte opravy, které jste provedli od otevření stránky **Oprava dat OCR**, a zvolte akci **Resetovat data OCR**.
6. Chcete-li opravy odeslat do služby OCR, zvolte akci **Odeslat zpětnou vazbu OCR**.
7. Chcete-li uložit opravy, zavřete stránku **Oprava dat OCR**.

Pole záložky s náhledem **Finanční informace** na stránce **Příchozí dokumenty** jsou aktualizovány novými hodnotami, které jste zadali v kroku 4.

## Viz také
[Zpracování došlých dokladů](across-process-income-documents.md)  
[Došlé doklady](across-income-documents.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
