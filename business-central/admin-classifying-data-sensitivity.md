---
title: "Classifying Data Sensitivity"
description: You must specify which type of data you store about people so that you can respond to data subject requests.
author: brentholtorf

ms.author: bholtorf
ms.custom: na
ms.reviewer: na

ms.topic: conceptual
ms.search.form: 1752
ms.date: 06/14/2021
---

# Klasifikace citlivosti dat
Chcete-li klasifikovat pole, která obsahují citlivá nebo osobní data, může partner společnosti Microsoft nastavit vlastnost ```Klasifikace Dat``` na polích. To vyžaduje přístup k databázovým tabulkám, a to buď prostřednictvím vývojového prostředí, nebo spuštěním skriptu prostředí Windows PowerShell. Pro více informací navštivte [Klasifikaci dat].

Jako zákazník můžete přidat druhou úroveň klasifikace zadáním úrovní citlivosti pro data, která ukládáte do standardních a vlastních polí. Klasifikace citlivosti dat pomáhá zajistit, abyste věděli, kde uchováváte osobní údaje ve svém systému, a usnadňuje reakci na požadavky subjektů údajů. Například pokud vás kontakt nebo zákazník požádá o export svých osobních údajů. Další informace naleznete v části [Odpovídání na žádosti o osobní údaje](admin-responding-to-requests-about-personal-data.md).

> [!Important]
> Společnost Microsoft poskytuje tuto funkci klasifikace citlivosti dat pouze z důvodu pohodlí. Je vaší odpovědností vhodně klasifikovat data a dodržovat všechny zákony a předpisy, které se na vás vztahují. Společnost Microsoft se zříká veškeré odpovědnosti vůči jakýmkoli nárokům souvisejícím s vaší klasifikací dat.

Následující tabulka popisuje úrovně citlivosti dat, které můžete přiřadit.

| Citlivost | Popis |
|----|----|
| Citlivá | Informace o rasovém nebo etnickém původu subjektu údajů, politických názorech, náboženském přesvědčení, zapojení do odborů, fyzickém nebo duševním zdraví, sexualitě nebo podrobnostech o trestných činech. |
| Osobní | Informace, které lze použít k identifikaci subjektu údajů, a to buď přímo, nebo v kombinaci s jinými údaji nebo informacemi. |
| Důvěrný | Obchodní data, která používáte pro účetní nebo jiné obchodní účely a nechcete je vystavit jiným účetním jednotkám. Může se jednat například o položky účetní knihy. |
| Normální | Obecné údaje, které nepatří do žádné jiné kategorie. |

## Jak mohu klasifikovat svá data?
Klasifikace citlivosti velkého počtu polí jeden po druhém by trvala dlouho. Abychom urychlili proces klasifikace, poskytujeme nástroje, které můžete použít k hromadné klasifikaci citlivosti polí, a poté můžete doladit detaily klasifikace pro konkrétní pole. Nástroje najdete v sešitu Klasifikace dat, který je k dispozici v Centru rolí Správa uživatelů, skupin uživatelů a oprávnění. Chcete-li list používat, musíte být správcem systému.

> [!Important]
> Když otevřete list Klasifikace dat poprvé, bude prázdný. Chcete-li vygenerovat seznam polí, je nutné spustit Průvodce klasifikací dat. Chcete-li spustit průvodce, vyberte akci **Nastavit klasifikaci dat**.

Například sešit Klasifikace dat umožňuje provádět následující činnosti:

* Pomocí Průvodce klasifikací dat exportujte svá pole do listu aplikace Excel, kde je můžete hromadně klasifikovat. Použití listu Excel je zvláště užitečné, pokud spolupracujete s partnerem společnosti Microsoft. Po aktualizaci listu můžete pomocí průvodce importovat a použít klasifikace. Průvodce můžete také použít k ruční klasifikaci polí.
* Vyberte pole a poté filtrujte seznam a vyhledejte podobná pole, která pravděpodobně patří do stejné klasifikace jako pole, na kterém jste založili vyhledávání.
* Prohlédněte si pole zobrazením jeho obsahu.

> [!Tip]
> Definovali jsme klasifikaci citlivosti vzorků pro tabulky a pole v demonstrační společnosti Cronus. Klasifikaci však můžete použít jako inspiraci při klasifikaci vlastních tabulek a polí.

## Viz také

[Klasifikace dat](/dynamics365/business-central/dev-itpro/developer/devenv-classifying-data)


[!INCLUDE[footer-include](includes/footer-banner.md)]