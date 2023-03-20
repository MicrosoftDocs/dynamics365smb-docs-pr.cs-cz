---
title: Run and Print Reports
description: Learn about entering a report into a job queue and scheduling it to be processed at a specific date and time.
author: jswymer


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.search.form:
ms.date: 03/20/2023
ms.author: jswymer

---
# Spouštění a tisk sestav

Sestava shromažďuje informace na základě zadané sady kritérií. Informace jsou uspořádány a prezentovány ve snadno čitelném formátu, který lze vytisknout nebo uložit jako soubor. Existuje mnoho sestav, ke kterým máte v rámci aplikace přístup. Tyto sestavy obvykle obsahují informace týkající se kontextu stránky, na které se právě nacházíte. Například stránka **Zákazníci** obsahuje sestavy pro 10 nejlepších zákazníků, statistiky prodeje a další.

Dávkové úlohy a XMLporty fungují víceméně stejně jako sestavy, ale používají se více pro zpracování nebo export dat. Například dávková úloha **Vytvořit upomínky** vytvoří upomínky pro zákazníky s opožděnými platbami.

> [!NOTE]
> Toto téma se týká převážně „sestavy“, ale podobné informace platí i pro dávkové úlohy.

## Začínáme

Sestavy můžete najít v záložce **Sestavy** na vybraných stránkách, nebo můžete použít ![vyhledávací žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), abyste našli sestavy podle jména.

Když otevřete sestavu, dávkovou úlohu nebo XMLport, obvykle se zobrazí stránka požadavku, kde nastavíte různé možnosti a filtry, které určují, co se má do sestavy zahrnout. Následující části vysvětlují, jak používat stránku požadavku k vytvoření, náhledu a tisku sestavy.

## <a name="SavedSettings"></a>Použití výchozích hodnot – předdefinovaná nastavení

Většina stránek požadavků obsahuje pole **Použít výchozí hodnoty z**. Toto pole umožňuje vybrat předdefinovaná nastavení pro sestavu, která automaticky nastaví možnosti a filtry pro sestavu. Vyberte položku ze seznamu a uvidíte, že možnosti a filtry na stránce požadavku se odpovídajícím způsobem změní.

Položka s názvem **Naposledy použité možnosti a filtry** je vždy k dispozici. Tato položka nastaví sestavu tak, aby používala možnosti a filtry, které byly použity při posledním spuštění sestavy.

Pole **Použít výchozí hodnoty z** poskytuje rychlý a spolehlivý způsob konzistentního generování sestav obsahujících správná data. Po výběru položky můžete před zobrazením náhledu nebo tiskem sestavy změnit kteroukoli z možností a filtrů. Změny, které provedete, se neuloží do položky předdefinovaných nastavení, kterou jste vybrali, ale uloží se do položky **Naposledy použité možnosti a filtry**.

> [!NOTE]
> Předdefinovaná nastavení obvykle nastavuje a spravuje správce. Pokud se chcete dozvědět více, přečtěte si [Správa uložených nastavení pro sestavy a dávkové úlohy](reports-saving-reusing-settings.md).

## Určení dat, která mají být zahrnuta do sestavy

Pomocí polí v části **Možnosti** a **Filtry** můžete změnit omezení požadovaných informací v sestavě. Filtry v sestavě nastavujete víceméně stejným způsobem jako filtry v seznamech. Další informace naleznete v tématu [Filtrování](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> Sekce **Filtrovat dle** na stránce požadavku poskytuje obecnou možnost filtrování sestavy. Tyto filtry jsou volitelné.
>
> Některé sestavy budou ignorovat všechny takové filtry, což znamená, že bez ohledu na to, jaký filtr je nastaven v části **Zobrazit výsledky**, je výstup sestavy stejný. Není možné poskytnout seznam obsahující informace o tom, která pole jsou ignorována v kterých sestavách, takže při jejich užívání s nimi budete muset experimentovat.
>
> **Příklad**: Při použití dávkové úlohy **Vytvořit upomínky** bude filtr pro pole **Položky zákazníka** **Úrovně poslední vydané upomínky** ignorován, protože filtry jsou pro danou dávkovou úlohu pevně stanoveny..

## Náhled sestavy

Náhled sestavy vám umožní zjistit, jak bude sestava vypadat, ještě před jejím vytištěním. Náhled není založen na tiskárně vybrané v poli **Tiskárna** na stránce požadavku. Je řízen prohlížečem. Po zobrazení náhledu se můžete vrátit na stránku požadavku a podle potřeby provést změny možností a filtrů.

Chcete-li zobrazit náhled sestavy, zvolte tlačítko **Náhled** nebo **Náhled a zavřít** na stránce požadavku sestavy. Tlačítko, které se zobrazí, závisí na sestavě, takže některé sestavy mají tlačítko **Náhled**, zatímco jiné mají tlačítko **Náhled a zavřít**. Obě tlačítka otevřou náhled sestavy. Rozdíl je v tom, že **Náhled** udržuje stránku požadavku otevřenou, takže se k ní můžete vrátit, provést změny, znovu zobrazit náhled nebo vytisknout. Pomocí **Náhled a zavřít**se stránka požadavku zavře, takže budete muset zprávu znovu otevřít, abyste mohli provést změny nebo vytisknout.

> Pokud používáte verzi Business Central 2020, wave 1 nebo starší, je k dispozici pouze tlačítko **Náhled**, které zavře stránku požadavku při náhledu, jak je popsáno u **Náhled a zavřít**.

### Práce s náhledem

V náhledu použijte panel nabídek na náhledu sestavy, abyste:

- Procházeli stránkami
- Přibližovali a oddalovali
- Měnili velikost stránky
- Vybírali text

   Můžete zkopírovat text ze sestavy a pak ho vložit někam jinam, například na stránku do [!INCLUDE[prod_short](includes/prod_short.md)] nebo Microsoft Word.  Například pomocí myši stisknete a podržíte tlačítko v místě, kde chcete začít. Pak pohybem myši vyberte jedno nebo více slov, vět nebo odstavců. Stiskněte pravé tlačítko myši a vyberte **Kopírovat**. Potom vložte vybraný text na požadované místo.
- Posun dokumentu

   Viditelnou část sestavy můžete přesunout libovolným směrem, abyste si mohli prohlédnout jiné oblasti nebo sestavu. To je užitečné, pokud jste přiblížili zobrazení, aby jste viděli podrobnosti.  Pomocí myši stiskněte a podržte tlačítko myši kdekoli v náhledu zprávy a poté pohněte myší.

- Stáhnutí PDF souboru do počítače nebo po síti.
- Tisk

## Uložení sestavy do souboru

Sestavu můžete uložit do dokumentu PDF, dokumentu Microsoft Word nebo dokumentu Microsoft Excel tak, že vyberete možnost **Odeslat do** a poté provedete výběr.

> [!TIP]
> Možnosti **Dokument Microsoft Excel (pouze data)** a **Dokument XML** slouží většinou pro pokročilé účely. Tyto možnosti byste obvykle použili pro podrobnou analýzu dat. Další informace naleznete v části [Analýza dat sestav pomocí Excelu a XML](report-analyze-excel.md).
>
> Můžete také použít **Dokument aplikace Microsoft Excel (pouze data)** k vytvoření nových rozvržení aplikace Excel pro danou sestavu. Další informace naleznete v tématu  [Práce s rozvržením aplikace Excel](ui-excel-report-layouts.md).

<!--
### About sending to Word

Use the **Microsoft Word Document** option to generate a report as a Word document.  

> [!NOTE]
> You can specify the layout to use for each report on the **Report Selection** page in the **Selected Layout** field. The default setting for reports is **RDLC (built-in)**, which produces reports in the same, or similar, layout as the **Microsoft Word Document** layout. However, the key difference is whether you want to generate a single or multiple report documents. For single documents, you can use the RDLC (built-in) option. For multiple documents, set the **Microsoft Word Document** as the default layout for the report. For more information, see [Managing Report and Document Layouts](ui-manage-report-layouts.md).

-->

## <a name="ScheduleReport"></a> Plánování pozdějšího spuštění sestavy

Můžete naplánovat sestavu nebo dávkovou úlohu tak, aby se spouštěla k určitému datu a času. Naplánované sestavy a dávkové úlohy se zadávají do fronty úloh a zpracovávají se v naplánovaném čase, podobně jako u jiných úloh. Po klepnutí na tlačítko **Odeslat do** zvolíte možnost **Plán** a poté zadáte informace, jako je tiskárna, čas a datum. Sestava je poté přidána do fronty úloh a bude spuštěna ve specifikovaném čase. Po zpracování sestavy bude položka odstraněna z fronty úloh. Pro více informací navštivte [Použití fronty úloh na plánování úloh](admin-job-queues-schedule-tasks.md).

Když naplánujete spuštění sestavy, můžete určit, že se musí spouštět každý čtvrtek, například nastavením pole **Vzorec data dalšího spuštění** na *D4*. Pro více informací navštivte *Použití vzorců dat*.

Sestavu můžete uložit do souboru (například do Excelu, Wordu nebo PDF), vytisknout nebo sestavu pouze vygenerovat. Pokud se rozhodnete uložit sestavu do souboru, bude zpracovaná sestava odeslána do **Schránky sestav** ve vašem Centru rolí, kde si ji můžete prohlédnout.

## <a name="PrintReport"></a>Tisk sestavy

Chcete-li zobrazit náhled sestavy, zvolte tlačítko **Náhled** nebo **Náhled** na stránce požadavku sestavy.

Pokud sestava používá rozložení aplikace Excel, neuvidíte pole **Tiskárna**, tlačítko **Tisk** ani tlačítko **Náhled**. Místo toho je zde tlačítko **Stáhnout**. Pokud chcete tisknout, vyberte **Stáhnout**, otevřete stažený soubor v Excelu a vytiskněte odtud.

### <a name="Printer"></a>Tiskárna

Pole **Tiskárna** na stránce požadavku zobrazuje název tiskárny, do které bude sestava odeslána. Chcete-li změnit tiskárnu, stačí vybrat tiskárnu ze seznamu.

> [!NOTE]
> **(Zpracovává prohlížeč)** znamená, že pro sestavu není určena žádná tiskárna. V takovém případě prohlížeč zpracuje výtisk a zobrazí standardní prostředí, kde si můžete vybrat místní tiskárnu připojenou k vašemu zařízení. **(Zpracováno prohlížečem)** není k dispozici v [!INCLUDE[prod_short](includes/prod_short.md)] mobilní aplikaci nebo aplikaci pro Microsoft Teams.

> [!TIP]
> Tiskárna, která je pro vás ve výchozím nastavení vybrána, se nastavuje na stránce **Výběry tiskáren**. Informace o změně výchozí tiskárny naleznete v tématu [Postup při výběru tiskáren, které tisknou sestavy](ui-specify-printer-selection-reports.md#default).

### Tisk sestav v thajštině

Speciálně pro thajskou verzi [!INCLUDE[prod_short](includes/prod_short.md)], tlačítko **Tisk** nemůže správně vytisknout sestavy kvůli omezením ve službě, která generuje soubor PDF pro tisk. Místo toho můžete sestavu otevřít v aplikaci Word a uložit ji jako tisknutelný soubor PDF.

Nebo můžete požádat správce, aby pro nejpoužívanější sestavy vytvořil rozvržení sestavy aplikace Word. Další informace naleznete v tématu [Správa rozvržení sestav a dokladů](ui-manage-report-layouts.md).

## Přepínání rozložení sestav

Rozložení sestavy určuje, co se v sestavě zobrazuje, jak je uspořádaná a jak je stylizovaná. Chcete-li přepnout na jiné rozložení, přečtěte si téma [Nastavení rozložení pro sestavu](ui-set-report-layout.md). Nebo pokud chcete přizpůsobit vlastní rozložení sestavy, přečtěte si téma [Začínáme s vytvářením rozložení](ui-get-started-layouts.md).

## Pokročilé možnosti

Pole v části **Upřesnit** nastavují omezení generované sestavy pro řízení prostředků tiskárny. Tato nastavení obvykle nebudete muset měnit, pokud nemáte velký přehled. Pokud sestava při pokusu o náhled nebo tisk překročí tato omezení, zobrazí se zpráva s informací, které omezení bylo překročeno. Poté můžete změnit nastavení tak, aby vyhovovalo vašemu přehledu. Každé pole má maximální hodnotu, kterou byste měli znát:

| Pole | Maximální hodnota |
|-----|-------------|
| Maximální doba vykreslování | 12:00:00 |
| Maximální počet řádků | 1000000 |
| Maximální počet dokumentů | 500 |

> [!NOTE]
> Maximální hodnoty mohou být pro rozdílně pro [!INCLUDE[prod_short](includes/prod_short.md)] on-premises a správce je může změnit. Další informace naleznete v části [Konfigurace Business Central On-Premises](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports) Pro přehled omezení přehledů [!INCLUDE[prod_short](includes/prod_short.md)] online běžte na [Provozní limity](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## Viz také

[Nastavení tiskáren](ui-specify-printer-selection-reports.md)  
[Práce s kalendářními daty a časy](ui-enter-date-ranges.md)  
[Správa sestav a rozložení sestav](ui-manage-report-layouts.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]