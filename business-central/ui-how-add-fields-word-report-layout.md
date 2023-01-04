---
    title: How to Add Fields to a Word Report Layout
    description: This topic describes how to add fields of a report dataset to an existing Word report layout for a report.
    author: jswymer
    
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 11/25/2021
    ms.author: jswymer

---

# Práce s rozvrženími aplikace Word

Rozvržení sestavy aplikace Word určuje obsah a formát sestavy při náhledu a tisku z Business Central. Tato rozvržení můžete vytvořit a upravit pomocí aplikace Microsoft Word.

[![Příklad dokumentu s rozvržením sestavy ve Wordu pro Business Central.](media/word-layout.png)](media/word-layout.png#lightbox)

Když upravujete rozvržení sestavy aplikace Word, určíte pole datové sady sestavy, která chcete zahrnout do sestavy a také způsob uspořádání polí. Definujete také obecný formát sestavy, například písmo a velikost textu, okraje a obrázky na pozadí. Obsah sestavy obvykle uspořádáte přidáním tabulek do rozvržení.

Chcete-li provádět obecné změny formátování a rozvržení, jako je například změna textového písma, přidání a úprava tabulky nebo odstranění datového pole, stačí použít základní editační funkce aplikace Word, jako to děláte u jakéhokoli dokumentu Word.

Pokud navrhujete rozvržení sestavy aplikace Word od nuly nebo přidáváte nová datová pole, začněte přidáním tabulky, která obsahuje řádky a sloupce, které budou nakonec obsahovat datová pole.

> [!TIP]  
> Zobrazte si čáry mřížky tabulky, abyste viděli hranice buněk tabulky Nezapomeňte skrýt mřížku, až dokončíte úpravy. Chcete-li zobrazit nebo skrýt mřížky tabulky, vyberte tabulku a v části **Rozvržení** na kartě **Tabulka** zvolte **Zobrazit mřížky**.

## Vkládání fontů do aplikace Word z důvodu konzistence

Chcete-li zajistit, aby se sestavy vždy zobrazovaly a tiskly s zamýšlenými písmy, bez ohledu na to, kde uživatelé otevírají nebo tisknou sestavy, můžete fonty vložit do dokumentu Word. Mějte však na paměti, že vkládání fontů může výrazně zvětšit velikost souborů aplikace Word. Další informace o vkládání fontů do aplikace Word naleznete v tématu [Vkládání písem do aplikací Word, PowerPoint nebo Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

## Přidání datových polí

Sada dat sestavy se může skládat z polí zobrazujících popisky, data a obrázky. Toto téma popisuje postup pro přidání polí sady dat sestavy do existujícího Word rozvržení sestavy pro sestavu. Pole přidáte pomocí vlastní části XML aplikace Word pro sestavu a přidáním ovládacích prvků obsahu, které se mapují do polí sady dat sestavy. Přidání polí vyžaduje určitou znalost sady dat sestavy, abyste mohli identifikovat pole, která chcete přidat do rozvržení.

> [!NOTE]  
> Nelze upravovat vestavěné rozvržení sestavy<!--Onprem. Built-in layouts can only be modified by using the development environment-->.

### <a name="OpenXMLPart"></a> Otevření vlastní části XML pro zprávu v aplikaci Word

1. Pokud ještě není otevřený, otevřete dokument rozvržení sestavy ve Wordu.

   Pro více informací navštivte [Vytvoření a úprava vlastního rozvržení sestavy](ui-how-create-custom-report-layout.md).

2. Zobrazte kartu **Vývojář** v pásu karet aplikace Microsoft Word.

   Ve výchozím nastavení není karta **Vývojář** zobrazena na pásu karet. Pro více informací navštivte [Zobrazení karty Vývojář v pásu karet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).

3. Na kartě **Vývojář** zvolte **Podokno mapování XML**.

4. V podokně **Mapování XML** v rozevíracím seznamu **Vlastní XML část** zvolte vlastní [!INCLUDE[prod_short](includes/prod_short.md)] sestavu, která je obvykle v seznamu poslední. Název vlastní XML části má následující formát:

   `urn:microsoft-dynamics-nav/reports/<report_name>/<ID>`

   `<report_name>` je název, který je přiřazen k sestavě

   `<ID>` je identifikační číslo sestavy.

   Po výběru vlastní XML části se v podokně Mapování XML zobrazí popisky a ovládací prvky pole, které jsou k dispozici pro sestavu.

### Přidání popisu nebo datového pole

1. Umístěte kurzor do dokumentu, kam chcete přidat ovládací prvek.

2. V podokně **Mapování XML** klepněte pravým tlačítkem myši na ovládací prvek, který chcete přidat, zvolte **Vložit ovládací prvek obsahu** a poté zvolte **Prostý text**.

   > [!NOTE]  
   > Pole nelze přidat ručně zadáním názvu pole sady dat do ovládacího prvku obsahu. K mapování polí musíte použít podokno **Mapování XML**.

### Přidání opakujících se řádků datových polí k vytvoření seznamu

1. V tabulce přidejte řádek tabulky, který obsahuje sloupec pro každé pole, které chcete opakovat.

   Tento řádek bude sloužit jako zástupný symbol pro opakující se pole.

2. Vyberte celý řádek.

3. V podokně **Mapování XML** klepněte pravým tlačítkem myši na ovládací prvek, který odpovídá datové položce sestavy, která obsahuje pole, která chcete opakovat, zvolte **Vložit ovládací prvek obsahu** a poté zvolte **Opakovaná**.

4. Přidejte opakující se pole do řádku následujícím způsobem:

   1. Umístěte ukazatel do sloupce.

   2. V podokně **Mapování XML** klepněte pravým tlačítkem myši na ovládací prvek, který chcete přidat, zvolte **Vložit ovládací prvek obsahu** a poté zvolte **Prostý text**.

   3. Pro každé pole opakujte kroky A a B.

## Přidávání obrázkových polí

Sada dat sestavy může zahrnovat pole, které obsahuje obrázek, například logo společnosti nebo obrázek položky. Pro přidání obrázku ze sady dat sestavy, vložte ovládací prvek obsahu **Obrázek**.

Obrázky jsou zarovnány v levém horním rohu ovládacího prvku obsahu a automaticky upraví jejich velikost v poměru odpovídajícím hranici ovládacího prvku obsahu.

> [!IMPORTANT]  
> Můžete přidat pouze obrázky, které mají formát podporovaný aplikací Word, například typy souborů .bmp, .jpeg a .png. Pokud přidáte obrázek, který má formát nepodporovaný aplikací Word, zobrazí se chyba při spuštění sestavy z klienta [!INCLUDE[prod_short](includes/prod_short.md)].

### Přidání obrázku

1. Umístěte ukazatel do dokumentu, kam chcete přidat ovládací prvek.

2. V podokně **Mapování XML** klepněte pravým tlačítkem myši na ovládací prvek, který chcete přidat, zvolte **Vložit ovládací prvek obsahu** a poté zvolte **Obrázek**.

3. Pro zvětšení nebo zmenšení obrázku, přetáhněte úchyt pro změnu velikosti z nebo do středu ovládacího prvku seznamu.

## <a name="RemoveField"></a> Odstranění popisku nebo datového pole

Popisky a datová pole sestavy jsou obsaženy v ovládacích prvcích obsahu v aplikaci Word. Následující obrázek znázorňuje ovládací prvek obsahu, když je vybrán v dokumentu Word.

![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")

Název popisku nebo datového pole se zobrazí v ovládacím prvku obsahu. V příkladu je název pole SpolečnostAddr1.

### Odstranění popisku nebo datového pole

1. Klepněte pravým tlačítkem myši na pole, které chcete odstranit, a pak zvolte **Odstranit kontrolu obsahu**.

   Ovládací prvek obsahu je odebrán, ale název pole zůstává jako text.

2. Odstraňte zbývající text podle potřeby.

## Přehled vlastní XML části

Rozvržení sestavy aplikace Word je založeno na *vlastních částech XML*. Vlastní XML část sestavy se skládá z prvků, které odpovídají datovým položkám, sloupcům a popiskům, které tvoří sadu dat sestavy. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Vlastní XML část se používá k mapování dat do sestavy, když je spuštěna.

### Struktura XML vlastní XML část

Následující tabulka poskytuje zjednodušený přehled XML vlastní XML části.

| Prvky XML | Popis |
|------------------|-----------------|  
| `<?xml version="1.0" encoding="utf-16"?>` | Hlavička |
| `<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"` | XML specifikace oboru názvů. `<reportname>` je název, který je přiřazen k sestavě `<id>` je ID přiřazené k sestavě |
| `..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>` | Obsahuje všechny popisy pro sestavu.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />- Prvky popisů, které se vztahují ke sloupcům, mají formát `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />- Prvky popisů mají formát `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />- Popisy jsou řazeny abecedně. |
| `..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>` | Datová položka a sloupce nejvyšší úrovně. Sloupce jsou abecedně seřazeny. |
| `....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>` | Datové položky a sloupce, které jsou vnořeny do datové položky nejvyšší úrovně. Sloupce jsou uvedeny v abecedním pořadí pod příslušnou datovou položkou. |
| `..</DataItem1>`<br /><br /> `</WordReportXmlPart>` | Uzavírací prvek. |

### Vlastní XML část v aplikaci Word

V aplikaci Word otevřete vlastní XML část v podokně **Mapování XML** a poté pomocí podokna mapujte prvky na ovládací prvky obsahu v dokumentu aplikace Word Podokno **Mapování XML** je přístupné z karty **Vývojář** (pro více informací navštivte [Zobrazení karty Vývojář v pásu karet](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon)).

Prvky v podokně **Mapování XML** se zobrazují ve struktuře podobné zdroji dat XML. Pole popisků jsou seskupena do společného prvku **Popisky** a datová položka a sloupce jsou uspořádány v hierarchické struktuře, která odpovídá zdroji XML, se sloupci uvedenými v abecedním pořadí. Prvky jsou identifikovány názvem sloupce, jak je definováno v datové sadě sestavy v kódu AL. Pro více informací navštivte [Definování datové sady sestavy](/dynamics365/business-central/dev-itpro/developer/devenv-report-dataset).

Následující obrázek znázorňuje jednoduchou vlastní XML část z předchozí sekce v podokně **Mapování XML** dokumentu aplikace Word.

![Klip podokna mapování XML v aplikaci Word.](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")

* Chcete-li do rozvržení přidat popisek nebo pole, vložíte ovládací prvek obsahu, který mapuje prvek v podokně.

* Chcete-li vytvořit opakující se řádky sloupců, vložte ovládací prvek obsahu **Opakování** pro prvek nadřazené datové položky a poté přidejte řízení obsahu pro sloupce.

* U popisků je skutečným textem, který se objeví ve vygenerované sestavě, hodnota vlastnosti **Titulek** pro pole v tabulce datových položek (pokud popisek souvisí se sloupcem v sadě dat sestavy) nebo popisek v Návrháři štítků sestav (pokud popisek nesouvisí se sloupcem v sadě dat).

* Jazyk popisku, který se zobrazí při spuštění sestavy, závisí na nastavení jazyka objektu sestavy.

## Viz také

[Vytvoření a úprava vlastní rozvržení sestavy](ui-how-create-custom-report-layout.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]