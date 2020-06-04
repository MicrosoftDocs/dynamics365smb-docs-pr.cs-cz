---
title: Custom and Built-In Layouts for Reports and Documents | Microsoft Docs
description: Use report layouts to customize documents, for example, to personalize the font, logo, or page settings of PDF files you send to customers.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 05/22/2019
ms.author: solsen

---
# Správa rozvržení sestav a dokladů
Rozložení sestavy řídí obsah a formát sestavy, včetně těch datových polí datové sady sestavy, které se zobrazují v sestavě, jejich uspořádání, stylu textu, obrázků a dalších prvků. Z [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete změnit rozložení použité v sestavě, vytvořit nové rozložení nebo upravit existující rozložení.

> [!NOTE]
> V [!INCLUDE[d365fin](includes/d365fin_md.md)], zahrnuje pojem „sestava“ také externí dokumenty, jako jsou prodejní faktury a potvrzení objednávek, které posíláte zákazníkům jako soubory PDF.

Rozložení sestavy nastavuje zejména následující:

* Popisek a datová pole, která mají být zahrnuta z datové sady objektu [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Textový formát, například typ písma, velikost a barva.
* Logo společnosti a jeho pozice.
* Obecné nastavení stránky, například okraje a obrázky na pozadí.

Sestavu lze nastavit ve více rozloženích sestav, mezi kterými lze přepínat podle potřeby. Můžete použít jedno z vestavěných rozvržení přehledů nebo si můžete vytvořit vlastní rozvržení sestav a podle potřeby je přiřadit k vašim přehledům. Další informace naleznete v části [Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md).

Existují dva typy rozvržení sestav, které můžete použít v sestavách - Word a RDLC.

## Přehled rozvržení sestavy aplikace Word
Rozložení sestavy aplikace Word je založeno na dokumentu aplikace Word (typ souboru DOCX). Rozložení sestav aplikace Word umožňují navrhovat rozložení sestav pomocí aplikace Microsoft Word 2013 nebo novější. Rozložení sestavy aplikace Word určuje obsah zprávy - určuje, jak jsou tyto prvky obsahu uspořádány a jak vypadají. Dokument rozložení sestavy aplikace Word obvykle používá tabulky k uspořádání obsahu, kde mohou buňky obsahovat datová pole, text nebo obrázky.

![Příklad dokumentu rozložení sestavy aplikace Word pro NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")

## Přehled rozvržení RDLC
Rozložení RDLC je založeno na rozložení definic klientských sestav (typy souborů .rdlc nebo .rdl). Tato rozvržení jsou vytvářena a upravována pomocí SQL Server Report Builder. Koncepce návrhu rozvržení RDLC je podobná rozvržení aplikace Word, kde rozvržení definuje obecný formát sestavy a určuje pole z datové sady, která má být zahrnuta. Navrhování rozložení RDLC je pokročilejší než rozložení aplikace Word. Pro více informací navštivte [Navrhování rozvržení RDLC sestav](/dynamics-nav/Designing-RDLC-Report-Layouts)

## Vestavěné a vlastní rozvržení sestavy
[!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje několik vestavěných rozvržení. Vestavěná rozvržení jsou předdefinovaná rozvržení, která jsou navržena pro konkrétní sestavy. [!INCLUDE[d365fin](includes/d365fin_md.md)] bude mít vestavěné rozložení jako rozložení sestavy RDLC, rozložení sestavy aplikace Word nebo v některých případech obojí. Vestavěné rozvržení sestavy nelze změnit z [!INCLUDE[d365fin](includes/d365fin_md.md)], ale můžete je použít jako výchozí bod pro vytváření vlastních rozvržení vlastní sestavy.

Vlastní rozvržení jsou rozvržení sestavy, která navrhujete tak, aby změnila vzhled sestavy. Obvykle vytvoříte vlastní rozvržení na základě vestavěného rozvržení, ale můžete je vytvořit od nuly nebo jako kopie z existujícího vlastního rozvržení. Vlastní rozvržení vám umožní mít více rozvržení pro stejnou sestavu, mezi nimiž podle potřeby přepínáte. Například můžete mít různá rozvržení pro každou společnost [!INCLUDE[d365fin](includes/d365fin_md.md)], nebo můžete mít různá rozvržení pro stejnou společnost pro konkrétní příležitosti nebo události, jako je zvláštní kampaň nebo sváteční období.

## Rozhodnutí, zda použít rozvržení sestavy Word nebo RDLC
Rozložení sestavy může být založeno buď na dokumentu aplikace Word, nebo na souboru RDLC. Rozhodování o tom, zda použít rozvržení sestavy aplikace Word nebo typ rozvržení sestavy RDLC, bude záviset na tom, jak chcete, aby generovaná sestava vypadala, a na vašich znalostech aplikace Word a SQL Server Report Builder.

Obecné koncepční koncepce rozvržení Word a RDLC jsou velmi podobné. Každý typ má však určité konstrukční funkce, které ovlivňují, jak se vygenerovaná sestava zobrazí v [!INCLUDE[d365fin](includes/d365fin_md.md)]. To znamená, že stejná sestava může vypadat odlišně při použití rozvržení sestavy aplikace Word ve srovnání s rozvržením sestavy RDLC.

Proces nastavení rozvržení sestav aplikace Word a rozvržení sestav RDLC v sestavách je stejný. Hlavní rozdíl spočívá ve způsobu úpravy rozvržení. Rozložení sestav aplikace Word je obvykle snazší vytvořit a upravit než rozvržení sestav RDLC, protože můžete použít aplikaci Word. Rozložení sestav RDLC je upraveno pomocí nástroje SQL Server Report Builder, který cílí na pokročilejší uživatele.

Informace o tom, jak změnit rozložení, které se má použít, naleznete v tématu [Změna rozvržení, které je aktuálně použito v sestavě](ui-how-change-layout-currently-used-report.md) .

## Viz také
[Aktualizace rozvržení sestav a dokladů](ui-update-report-layouts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md)  
[Importování a exportování vlastního rozvržení sestavy nebo dokladu](ui-how-import-and-export-report-layout.md)  
[Odesílání dokladů e-mailem](ui-how-send-documents-email.md)  
[Práce se sestavami a dávkovými úlohami](ui-work-report.md)
