---
title: Jak přidat pole do Word rozvržení sestavy | Microsoft Docs
description: 'Popisuje, jak přidat pole sady dat sestavy do existujícího Word rozvržení sestavy pro sestavu.'
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/22/2018
ms.author: jswymer
---
# <a name="add-fields-to-a-word-report-layout"></a>Přidání pole do rozvržení sestavy aplikace Word
Sada dat sestavy se může skládat z polí zobrazujících popisky, data a obrázky. Toto téma popisuje postup pro přidání polí sady dat sestavy do existujícího Word rozvržení sestavy pro sestavu. Pole přidáte pomocí vlastní části XML aplikace Word pro sestavu a přidáním ovládacích prvků obsahu, které se mapují do polí sady dat sestavy. Přidání polí vyžaduje určitou znalost sady dat sestavy, abyste mohli identifikovat pole, která chcete přidat do rozvržení.  
  
> [!NOTE]  
>  Nemůžete upravovat rozvržení předdefinovaných sestav<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

##  <a name="OpenXMLPart"></a> Otevření vlastní XML části pro sestavu v aplikaci Word  
  
1.  Pokud již není otevřena, otevřete dokument rozvržení sestavy v aplikaci Word.  
  
     Pro více informací navštivte [Vytvoření a úprava vlastního rozvržení sestavy](ui-how-create-custom-report-layout.md).  
  
2.  Zobrazte kartu **Vývojář** v pásu karet aplikace Microsoft Word.  
  
     Ve výchozím nastavení není karta **Vývojář** zobrazena na pásu karet. Pro více informací navštivte [Zobrazení karty Vývojář v pásu karet](https://go.microsoft.com/fwlink/?LinkID=389631).  
  
3.  Na kartě **Vývojář** zvolte **Podokno mapování XML**.  
  
4.  V podokně **Mapování XML** v rozevíracím seznamu **Vlastní XML část** zvolte vlastní XML část pro sestavu ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->, která je obvykle v seznamu poslední. Název vlastní XML části má následující formát:  
  
     urn:microsoft-dynamics-nav/reports/*report_name*/*ID*  
  
     *report_name* je název, který je přiřazen k sestavě<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.  
  
     *ID* je identifikační číslo sestavy.  
  
     Po výběru vlastní XML části se v podokně Mapování XML zobrazí popisky a ovládací prvky pole, které jsou k dispozici pro sestavu.  
  
### <a name="to-add-a-label-or-data-field"></a>Přidání popisku nebo datového pole  
  
1.  Umístěte kurzor do dokumentu, kam chcete přidat ovládací prvek.  
  
2.  V podokně **Mapování XML** klepněte pravým tlačítkem myši na ovládací prvek, který chcete přidat, zvolte **Vložit ovládací prvek obsahu** a poté zvolte **Prostý text**.  
  
    > [!NOTE]  
    >  Pole nelze přidat ručně zadáním názvu pole sady dat do ovládacího prvku obsahu. K mapování polí musíte použít podokno **Mapování XML**.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Přidání opakujících se řádků datových polí k vytvoření seznamu  
  
1.  V tabulce přidejte řádek tabulky, který obsahuje sloupec pro každé pole, které chcete opakovat.  
  
     Tento řádek bude sloužit jako zástupný symbol pro opakující se pole.  
  
2.  Vyberte celý řádek.  
  
3.  V podokně **Mapování XML** klepněte pravým tlačítkem myši na ovládací prvek, který odpovídá datové položce sestavy, která obsahuje pole, která chcete opakovat, zvolte **Vložit ovládací prvek obsahu** a poté zvolte **Opakovaná**.  
  
4.  Přidejte opakující se pole do řádku následujícím způsobem:  
  
    1.  Umístěte ukazatel do sloupce.  
  
    2.  V podokně **Mapování XML** klepněte pravým tlačítkem myši na ovládací prvek, který chcete přidat, zvolte **Vložit ovládací prvek obsahu** a poté zvolte **Prostý text**.  
  
    3.  Pro každé pole opakujte kroky a a b.  
  
## <a name="adding-image-fields"></a>Přidávání obrázkových polí  
 Sada dat sestavy může zahrnovat pole, které obsahuje obrázek, například logo společnosti nebo obrázek položky. Pro přidání obrázku ze sady dat sestavy, vložte ovládací prvek obsahu **Obrázek**.  
  
 Obrázky jsou zarovnány v levém horním rohu ovládacího prvku obsahu a automaticky upraví jejich velikost v poměru odpovídajícím hranici ovládacího prvku obsahu.  
  
> [!IMPORTANT]  
>  Můžete přidat pouze obrázky, které mají formát podporovaný aplikací Word, například typy souborů .bmp, .jpeg a .png. Pokud přidáte obrázek, který má formát nepodporovaný aplikací Word, zobrazí se chyba při spuštění sestavy z klienta ADD INCLUDE<!--[!INCLUDE[d365fin](../../includes/d365fin_md.md)]-->.  
  
#### <a name="to-add-an-image"></a>Přidání obrázku  
  
1.  Umístěte ukazatel do dokumentu, kam chcete přidat ovládací prvek.  
  
2.  V podokně **Mapování XML** klepněte pravým tlačítkem myši na ovládací prvek, který chcete přidat, zvolte **Vložit ovládací prvek obsahu** a poté zvolte **Obrázek**.  
  
3.  Pro zvětšení nebo zmenšení obrázku, přetáhněte úchyt pro změnu velikosti z nebo do středu ovládacího prvku seznamu.  

## <a name="custom-xml-part-overview"></a>Přehled vlastní XML části
Rozvržení sestavy aplikace Word je založeno na *vlastních částech XML*. Vlastní XML část sestavy se skládá z prvků, které odpovídají datovým položkám, sloupcům a popiskům, které tvoří sadu dat sestavy. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->Vlastní XML část se používá k mapování dat do sestavy, když je spuštěna.

  
### <a name="xml-structure-of-custom-xml-part"></a>Struktura XML vlastní XML části  
Následující tabulka poskytuje zjednodušený přehled XML vlastní XML části.  
  
|Prvky XML|Popis|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Hlavička|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|XML specifikace oboru názvů. `<reportname>` je název, který je přiřazen k sestavě. `<id>` je ID, které je přiřazeno k sestavě.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Obsahuje všechny popisky sestavy.<!--OnPren The element includes labels that are related to columns that have the [IncludeCaption Property](../FullExperience/Name%20Property-duplicate.md).--><br />-   Prvky popisků, které souvisejí se sloupci, mají formát `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />-   Prvky popisků mají formát `<LabelName>LabelName</LabelName`<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Popisky jsou abecedně seřazeny.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Datová položka a sloupce nejvyšší úrovně. Sloupce jsou abecedně seřazeny.<!--OnPrem <br /><br /> The element names and values are determined by the [Name Property-duplicate](../FullExperience/Name%20Property-duplicate.md) of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Datové položky a sloupce, které jsou vnořeny do datové položky nejvyšší úrovně. Sloupce jsou uvedeny v abecedním pořadí pod příslušnou datovou položkou.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Uzavírací prvek.|  
  
### <a name="custom-xml-part-in-word"></a>Vlastní XML část v aplikaci Word  
 V aplikaci Word otevřete vlastní XML část v podokně **Mapování XML** a poté pomocí podokna mapujte prvky na ovládací prvky obsahu v dokumentu aplikace Word. Podokno **Mapování XML** je přístupné z karty **Vývojář** (pro více informací navštivte [Zobrazení karty Vývojář v pásu karet](https://go.microsoft.com/fwlink/?LinkID=389631)).  
  
 Prvky v podokně **Mapování XML** se zobrazují ve struktuře podobné zdroji dat XML. Pole popisků jsou seskupena do společného prvku **Popisky** a datová položka a sloupce jsou uspořádány v hierarchické struktuře, která odpovídá zdroji XML, se sloupci uvedenými v abecedním pořadí. Prvky jsou identifikovány svým jménem, jak je definováno ve vlastnosti Jméno v Návrháři datových sestav v ADD INCLUDE<!--[!INCLUDE[nav_dev_short](../../includes/nav_dev_short_md.md)]-->.  
  
 Následující obrázek znázorňuje jednoduchou vlastní XML část z předchozí sekce v podokně **Mapování XML** dokumentu aplikace Word.  
  
 ![Klip podokna mapování XML v aplikaci Word](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
-   Chcete-li do rozvržení přidat popisek nebo pole, vložíte ovládací prvek obsahu, který mapuje prvek v podokně **Mapování XML**.  
  
-   Chcete-li vytvořit opakující se řádky sloupců, vložte ovládací prvek obsahu **Opakovaná** pro prvek nadřazené datové položky a poté přidejte řízení obsahu pro sloupce.  
  
-   U popisků je skutečným textem, který se objeví ve vygenerované sestavě, hodnota vlastnosti **Titulek** pro pole v tabulce datových položek (pokud popisek souvisí se sloupcem v sadě dat sestavy) nebo popisek v Návrháři štítků sestav (pokud popisek nesouvisí se sloupcem v sadě dat).  
  
-   Jazyk popisku, který se zobrazí při spuštění sestavy, závisí na nastavení jazyka objektu sestavy. <!--OnPrem For more information, see [Multiple Document Languages](../FullExperience/Viewing%20the%20Application%20in%20Different%20Languages.md).-->  
  
## <a name="see-also"></a>Viz také  
 [Vytvoření a úprava vlastní rozvržení sestavy](ui-how-create-custom-report-layout.md)   
