---
title: Assistive features
description: This article provides information about keyboard shortcuts and other assistive features in Business Central for people with disabilities.
author: jswymer

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, charts, tooltips, screen reader
ms.search.form: 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017
ms.date: 06/23/2021
ms.author: jswymer

---
# Usnadnění přístupu a klávesové zkratky

Tento článek obsahuje informace o funkcích, které vytvářejí [!INCLUDE[prod_short](includes/prod_short.md)] snadno dostupný osobám se zdravotním postižením. [!INCLUDE[prod_short](includes/prod_short.md)] podporuje následující funkce usnadnění:

- Klávesové zkratky. Viz [Klávesové zkratky.](keyboard-shortcuts.md).
- Dotyková gesta a gesta pera na tabletech a telefonech. Viz [Dotyková gesta a gesta pera na tabletech a telefonech.](touch-gestures.md).
- Navigace
- Záhlaví
- Alternativní text pro obrázky a odkazy
- Podpora běžných asistenčních technologií
- Přiblížit nebo oddálit libovolnou stránku
- Popisky prvků v uživatelském rozhraní

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="Navigation"></a> Navigace

K pohybu mezi prvky na stránce můžete použít různé kombinace kláves Tab, Shift a šipek na klávesnici. Prvky zahrnují akce, pole a sloupce, součásti a další ovládací prvky. Obecně se stisknutím klávesy Tab nebo Shift+Tab přesunete na další nebo předchozí prvek.

Když se zaměříte na oblast, která obsahuje akce, jako je navigační panel v horní části centra rolí nebo panel akcí na jiných stránkách, můžete pomocí kláves se šipkami procházet různými akcemi a skupinami. Stisknutím klávesy Enter u skupiny otevřete její základní akce a pokračujte pomocí kláves se šipkami. Stisknutím klávesy Tab nebo Shift+Tab se přesuňte z oblasti akcí.

Pomocí pořadí ovládacích prvků můžete také přepínat mezi hlavní stránkou prohlížeče a dialogovými okny, která požadují například potvrzení, nebo přihlašovací stránkou

## <a name="Headings"></a> Nadpisy v obsahu

Zdrojový kód HTML pro [!INCLUDE[prod_short](includes/prod_short.md)] používá značky, které pomáhají uživatelům asistenčních technologií porozumět struktuře a obsahu stránky. Například na stránkách seznamu jsou sloupce definovány ve značkách TH a záhlaví sloupců jsou nastavena s atributem TITLE uvnitř značky. Popisky prvků, jako jsou Záložky, Informační okna a pole, jsou součástí značek nadpisů (H1, H2, H3 a H4).

## <a name="Images"></a> Obrázek a odkazy

Popisný text pro obrázky je nastaven s atributem ALT uvnitř tagu IMG. Popisný text pro hypertextové odkazy je nastaven s atributem title uvnitř tagu A.

## <a name="AssistiveTech"></a> Asistenční technologie

[!INCLUDE[prod_short](includes/prod_short.md)] podporuje různé asistenční technologie, jako je vysoký kontrast, čtečky obrazovky a software pro rozpoznávání hlasu. Některé asistenční technologie nemusí s určitými prvky na stránkách [!INCLUDE[prod_short](includes/prod_short.md)] fungovat správně.

## <a name="zoom"></a> Zvětšení

Většina prohlížečů používá k přiblížení a oddálení aktuální stránky standardní klávesové zkratky. Tyto klávesové zkratky nejsou specifické pro [!INCLUDE [prod_short](includes/prod_short.md)], ale fungují, když použijete [!INCLUDE [prod_short](includes/prod_short.md)] v prohlížeči. Seznam podporovaných klávesových zkratek naleznete v [Klávesové zkratky pro přiblížení a oddálení](keyboard-shortcuts.md#zoomshortcuts).

## Tooltipy

Tooltipy jsou k dispozici u většiny prvků v uživatelském rozhraní, jako jsou stránková pole a sloupce, akce, dlaždice nápovědy a grafy. Tooltipy poskytuje další text, který vysvětluje prvek, aby vám pomohl lépe porozumět jeho účelu.

Popisky se otevírají různými způsoby v závislosti na klientovi (webovém nebo mobilním) a zařízení, se kterým pracujete. Použijte následující tabulku jako vodítko. Některé tooltipy mohou číst programy pro čtení z obrazovky.en-readers. V takovém případě přistupujete k popiskům tak, jak je popsáno v tabulce, a pak pomocí programu pro čtení z obrazovky přejdete na popisek stejně jako u jakéhokoli jiného prvku.

#### Přístup k tooltipům

| Element | Akce myši pro webového klienta | Klávesové zkratky pro webového klienta | Dotykové gesto na tabletu/telefonu pro mobilní aplikaci | Podpora čtečky obrazovky |
|-------|-----------------|------------|--------------------------|---------------------|
| Pole stránek a záhlaví sloupců | Najeďte myší nebo klikněte na titulek pole nebo záhlaví sloupce | Přesuňte fokus na záhlaví pole nebo sloupce a stiskněte Alt+šipka nahoru | Klepněte na titulek pole | ano |
| Prvky grafů, jako je pruh, čára, výseč výseč | Najeďte myší na prvek | Přesunout fokus na prvek, například pomocí kláves se šipkami | Klepněte a podržte prvek | ano |
| Akce | Najeďte myší na akci | žádný | žádný | ne |
| Popis dlaždice | Najeďte myší na dlaždici | žádný | žádný | ne |


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## Další informace o usnadnění přístupu

Další informace o usnadnění pomocí produktů a technologií usnadnění společnosti Microsoft naleznete na webu [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160).

## Viz také

[Příprava na podnikání](ui-get-ready-business.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Často kladené otázky](across-faq.yml)

[!INCLUDE[footer-include](includes/footer-banner.md)]
