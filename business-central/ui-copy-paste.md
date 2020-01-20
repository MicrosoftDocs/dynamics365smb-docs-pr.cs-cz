---
title: Kopírování a vkládání dat
description: Zkopírujte pole a řádky ze stránek Business Central a vložte je na jiné místo.
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accessibility, shortcuts, keyboarding'
ms.date: 01/14/2020
ms.reviewer: -zdbice
ms.author: jswymer
---

# <a name="copying-and-pasting"></a>Kopírování a vkládání - Otázky a odpovědi

Můžete zkopírovat jeden nebo více řádků (záznamů) ze seznamu nebo jedno pole na stránce a poté vložit zkopírovaný obsah na stejnou stránku, jinou stránku nebo externí dokument (například Microsoft Excel a Outlook e-mail). Stručně řečeno, chcete-li kopírovat, stiskněte klávesy **CTRL+C** (cmd+C v MacOS) na klávesnici. Chcete-li vložit, stiskněte klávesy **CTRL+V** (cmd+V v systému MacOS).

Existuje několik dalších klávesových zkratek pro kopírování a vkládání, které vám ušetří čas při zadávání dat. Pro více informací navštivte [Klávesové zkratky](keyboard-shortcuts.md#CopyRows)

Tento článek odpovídá na běžné otázky týkající se kopírování a vkládání.  

## <a name="what-can-i-copy-and-paste"></a>Co mohu kopírovat a vložit?

- Zkopírujete jeden nebo více řádků v [!INCLUDE[d365fin](includes/d365fin_md.md)] do stejného seznamu nebo do libovolného seznamu se stejnými sloupci.
- Zkopírujete jeden nebo více řádků v [!INCLUDE[d365fin](includes/d365fin_md.md)] a vložíte je do Excelu nebo jiných aplikací.
- Zkopírujete jeden nebo více řádků v Excelu a vložíte je do seznamu v [!INCLUDE[d365fin](includes/d365fin_md.md)].
- Zkopírujete hodnotu konkrétního pole v [!INCLUDE[d365fin](includes/d365fin_md.md)] a vložíte ji kamkoli.

## <a name="does-copy-and-paste-work-with-tiles"></a>Funguje kopírování a vkládání s dlaždicemi?

Ano, ale pouze pro jednu vybranou dlaždici.

## <a name="how-do-i-copy-rows"></a>Jak zkopíruji řádky?

Chcete-li zkopírovat jeden řádek, vyberte jej a stiskněte **Ctrl+C**.

Pokud chcete kopírovat více řádků:

- Stiskněte Ctrl a klikněte na další řádek, nebo stiskněte Shift a klikněte pro vyběr řádku a všech řádků mezi nimi. Navštivte [Klávesové zkratky](keyboard-shortcuts.md#CopyRows) pro další kombinace výběru řádků pomocí myši a klávesnice.
- Zvolte ![Zobrazit více možností](media/show-more-options-icon.png "Ikona Zobrazit více možností") v prvním sloupci řádku, zvolte **Vybrat více**, zaškrtněte políčko vedle každého řádku, který chcete zkopírovat, a poté stiskněte **Ctrl+**C.

## <a name="how-do-i-paste-rows"></a>Jak vložím řádky?

Vyberte prázdný řádek a stiskněte **Ctrl+V**.

Pokud chcete nahradit stávající řádky, vyberte řádky a poté stiskněte **Ctrl+V**. V takovém případě můžete vložit pouze stejný počet řádků, jaký jste vybrali.

> [!NOTE]
> Seznam, do kterého vkládáte, musí být editovatelný.

<!-- Řádky se vkládají přímo na místo, kde se nachází kurzor. Pokud vložíte na prázdný řádek, budou všechny následující následující řádky přesunuty za vložené řádky. Pokud vložíte do existujícího řádku nebo řádků, bude přepsán.-->

## <a name="can-i-paste-rows-into-an-outlook-email"></a>Mohu vložit řádky do aplikace Outlook?

Ano. Takový obsah je vložen jako pěkně naformátovaná tabulka, která zachovává odsazení, zarovnání čísel a zbarvení, jaké by jste viděli v [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>V jakých seznamech mohu kopírovat a vložit řádky?

Řádky můžete kopírovat v libovolném seznamu, včetně deníků, oken s fakty nebo seznamů, které jsou vloženy na stránce (jako například řádky prodejní objednávky). Chcete-li však řádky vložit, seznam musí být editovatelný.

Na některých stránkách vám design aplikace může zabránit ve vkládání řádků. Pro změnu [vlastnosti Editable](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) na stránce nebo změnu [vlastnosti PasteIsValid](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) ve zdrojové tabulce kontaktujte svého administrátora nebo vývojáře aplikací.

## <a name="on-which-clients-is-copy-and-paste-available"></a>V rámci kterých klientů je kopírování a vkládání k dispozici?

Kopírování a vkládání je k dispozici v prohlížeči nebo v [!INCLUDE[d365fin](includes/d365fin_md.md)] aplikaci pro Windows 10.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>Jaký je maximální počet řádků, který lze kopírovat?

Můžete kopírovat tolik řádků, kolik jste jich zobrazili. Chcete-li například zkopírovat všech 1000 řádků na stránce, musíte nejprve sjet do dolní části stránky a před kopírováním počkat, až se řádky zobrazí. Maximální počet řádků, který můžete kopírovat, je omezen pouze pamětí zařízení.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>Musím mít při vkládání řádků stejný počet sloupců?

Ano. Ať už kopírujete z [!INCLUDE[d365fin](includes/d365fin_md.md)], z Excelu nebo z jiného zdroje tabulky, řádky které vložíte musí mít přesně shodné sloupce - ne více nebo méně.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>Proč při vkládání řádků dostávám chyby?

Při vkládání do [!INCLUDE[d365fin](includes/d365fin_md.md)] se u každého řádku kontroluje, zda jsou hodnoty v každém sloupci platné. Pokud sloupec obsahuje hodnotu, která není platná, vkládání se zastaví a zobrazí se chybová zpráva. Chcete-li tomu zabránit, ujistěte se, že sloupce mají platné hodnoty před jejich vložením.

## Viz také

[Pomocné funkce](ui-accessibility.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Často kladené otázky](across-faq.md)  
