---
    title: Electronic documents in Business Central   | Microsoft Docs
    description: Introduction to sending and receiving electronic documents in Business Central.
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

# Elektronická výměna dat
Rozhraní výměny dat můžete použít pro výměnu obchodních dokladů, bankovních souborů, směnných kurzů a dalších datových souborů s vašimi obchodními partnery.

## Elektronické doklady
Jako alternativu k odesílání obchodních dokladů v přílohách e-mailů můžete obchodní dokumenty zasílat a přijímat elektronicky. Elektronickým dokladem se rozumí soubor vyhovující standardu představující obchodní doklad, jako například faktura od dodavatele, kterou můžete obdržet a převést na nákupní fakturu v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Výměnu elektronických dokladů mezi dvěma obchodními partnery provádí externí poskytovatel služeb pro výměnu dokladů. Obecná verze [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje odesílání a přijímání elektronických faktur a dobropisů ve formátu PEPPOL, který je podporován největšími poskytovateli služeb pro výměnu dok. Hlavní poskytovatel služeb pro výměnu dokladů je předem nakonfigurován a připraven k nastavení ve vaší společnosti. K poskytování podpory pro jiné formáty elektronických dokladů vytvořte novou definici výměny dat pomocí rozhraní pro výměnu dat.

Z PDF nebo souborů s obrázky reprezentujících příchozí doklady můžeme nechat externí službu OCR (Optical Character Recognition - Optické rozpoznávání znaků) vytvořit elektronické doklady, které pak můžeme převést na došlé doklady v [!INCLUDE[d365fin](includes/d365fin_md.md)], stejně jako elektronické došlé doklady formátu PEPPOL. Pokud například od svého dodavatele obdržíte fakturu ve formátu PDF, můžete ji odeslat službě OCR na stránce **Došlé doklady**. Po několika sekundách obdržíte soubor zpět jako elektronickou fakturu, kterou lze pro dodavatele převést na nákupní fakturu. Pokud soubor odešlete do služby OCR pomocí e-mailu, bude automaticky vytvořen nový záznam příchozího dokladu, v momentě, kdy obdržíte elektronický doklad zpět.

Chcete-li například odeslat prodejní fakturu jako elektronický doklad PEPPOL, vyberte v dialogovém okně **Účtovat a Odeslat** možnost **Elektronický doklad**. Zde můžete také nastavit zákazníkův výchozí profil odesílání dokladů. Nejprve je nutné nastavit různá hlavní data, například informace o společnosti, zákazníky, zboží a měrné jednotky.  Používají se k identifikaci obchodních partnerů a zboží, když převádíte data v polích [!INCLUDE[d365fin](includes/d365fin_md.md)] na prvky v odchozích dokladech. Převod dat a odesílání prodejní faktury PEPPOL se provádí pomocí vyhrazených codeunit a XMLportů, reprezentovaných formátem elektronických dokladů **PEPPOL**.

Chcete-li například přijmout fakturu od dodavatele jako elektronický doklad PEPPOL, zpracujete doklad na stránce **Došlé doklady** a převedete jej na nákupní fakturu v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Můžete buď nastavit funkci Fronta úloh pro pravidelné zprovávání těchto souborů, nebo můžete spustit proces manuálně. Nejprve je nutné nastavit různá hlavní data, například informace o společnosti, dodavatele, zboží a měrné jednotky. Tyto položky slouží k identifikaci obchodních partnerů a zboží když převádíme data prvků příchozích dokumentů do polí v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Přijímací a datové konverze dokladů PEPPOL jsou prováděny rozhraním výměny dat, zastoupeným definicí výměny dat **PEPPOL - Faktura**.

Chcete-li například obdržet fakturu jako elektronický doklad OCR, zpracujete ji jako při obdržení elektronického dokladu PEPPOL. Příjem a převod elektronických dokladů z OCR je prováděn rozhraním výměny dat, reprezentovaný definicí výměny dat **OCR – Faktura**.

## Bankovní soubory
Formáty souborů pro výměnu bankovních dat se systémy ERP se liší v závislosti na dodavateli souboru a na zemi či oblasti. [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje import a export bankovních souborů SEPA (Single Euro Payments Area) a rozšíření AMC Banking 365 Fundamentals, které vám umožňuje připojit se ke službě pro převod bankovních dat, která je poskytována externím poskytovatelem, společností AMC Consult. K poskytování podpory pro jiné formáty elektronických dokladů použijte rozhraní pro výměnu dat.

Chcete-li exportovat převody SEPA, zvolte možnost **Export plateb do souboru** na stránce **Deník plateb** a poté soubor odešlete pro zpracování plateb ve vaší bance. Nejprve musíte nastavit různá hlavní data, jako například bankovní účty, dodavatelé, nebo platební metody. Převod dat a export bankovních dat SEPA je prováděn pomocí vyhrazených codeunit a XMLportů, reprezentovaných nastavením pro bankovní export/import **SEPA – peněžní převod**. Alternativně můžete nastavit export AMC Banking 365 Fundamentals pro provedení exportu, reporezentovaný službou **Služba konverze bankovních dat - Převedení kreditu**.

Chcete-li exportovat pokynu k inkasu SEPA, zvolte tlačítko **Exportovat soubor přímého inkasa** na stránce **Přímé inkaso**, poté odešlete své bance, pro automatické shromažďování zapojených plateb odběratelů. Nejprve musíte nastavit bankovní účty, zákazníky, Povolení přímého inkasa a způsoby platby. Převod dat a export bankovních dat SEPA je prováděn pomocí vyhrazených codeunit a XMLportů, reprezentovaných nastavením pro bankovní export/import **SEPA – příkaz k inkasu**.

Chcete-li importovat bankovní výpisy SEPA, zvolte tlačítko Importovat bankovní výpis v **Deník odsouhlasení plateb** a **Bankovní účet. Odsouhlasení** a poté můžete ručně nebo automaticky párovat každou položku bankovního výpisu s platbami nebo se záznamy hlavní knihy. Nejprve musíte nastavit bankovní účty. Import a převod bankovních dat SEPA se provádí pomocí Rámce výměny dat, reprezentovaného Definicí výměny dat **SEPA CAMT**. Případně můžete nastavit rozšíření AMC Banking 365 Fundamentals k provedení importu, reprezentovaného definicí výměny dat **Služba výměny bankovních dat - Bankovní výpis**.

Kromě toho místní verze aplikace [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje různé další formáty souborů pro import a export bankovních dat, mzdových transakcí a dalších dat. Pro více informací navštivte část nápovědy "Místní funkcionality" týkající se vaší země v [!INCLUDE[d365fin](includes/d365fin_md.md)].

## Směnné kurzy
Můžete nastavit externí službu, která udrží směnné kurzy měn aktuální. Služba, která poskytuje aktualizované směnné kurzy, je povolena díky definici výměny dat. Tudíž stránka **Karta nastavení aktualizace sm. kurzů** je zúženým zobrazením pro stránku **Definice výměny dat** s dotyčnou definicí vyměny dat.

Pro všechny výměny dat v souborech XML můžete připravit nastavení výměny dat načtením souvisejícího souboru schématu XML na stránce **Náhled XML schématu**. Zde vyberte datové prvky, které chcete vyměnit, s [!INCLUDE[d365fin](includes/d365fin_md.md)] a poté inicializujete definici výměny dat, nebo vygenerujete XMLport.

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| Viz | Navštivte |
|--------|---------|  
| Zjistění, jak funguje Rozhraní výměny dat. | [O rozhraní výměny dat](across-about-the-data-exchange-framework.md) |
| Připravení se na výměnu dat v souboru opakovaným použitím schématu XML souboru. Nastavení definice výměny dat. Nastavení hlavních dat pro odesílání elektronického dokladu. Nastavení různých polí pro bankovní import/export. | [Nastavení výměny dat](across-set-up-data-exchange.md) |
| Posílání a příjmání faktur PEPPOL, importování bankovních výpisů a exportování bankovních platebních souborů na základě definice výměny dat. | [Výměna dat](across-exchange-data.md) |

## Viz také
[O rozhraní výměny dat](across-about-the-data-exchange-framework.md)
[Použití schémat XML k přípravě definic datových výměn](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)
[Nastavení výměny dat](across-set-up-data-exchange.md)
[Výměna dat](across-exchange-data.md)
[Došlé doklady](across-income-documents.md)
[Obecné obchodní funkcionalityy](ui-across-business-areas.md)
