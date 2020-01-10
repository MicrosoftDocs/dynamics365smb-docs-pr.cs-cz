---
title: Klasifikace citlivosti dat
description: 'Musíte určit, jaký typ údajů o lidech ukládáte, abyste mohli reagovat na požadavky subjektů.'
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2018
---

# <a name="classifying-data-sensitivity"></a>Klasifikace citlivosti dat
Pro klasifikaci polí, která obsahují citlivá nebo osobní data, může partner společnosti Microsoft nastavit ```DataClassification``` vlastnost na polích. To vyžaduje přístup k databázovým tabulkám, buď prostřednictvím vývojového prostředí nebo spuštěním skriptu Windows PowerShell. Pro více informací navštivte [Klasifikace dat](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data).  

Jako zákazník můžete přidat druhou úroveň klasifikace zadáním úrovní citlivosti pro data, která ukládáte ve standardních a vlastních polích. Klasifikace citlivosti údajů pomáhá zajistit, abyste věděli, kde ve svém systému uchováváte osobní údaje, a usnadňuje to reagovat na požadavky na údaje subjektů. Například, pokud vás kontakt nebo zákazník požádá o export svých osobních údajů. Pro více informací navštivte [Odpovědi na žádosti o osobní údaje](admin-responding-to-requests-about-personal-data.md)

> [!Important]
> Společnost Microsoft poskytuje funkci Klasifikace citlivosti dat pouze pro větší pohodlí. Je vaší odpovědností za patřičnou klasifikaci dat a dodržování všech zákonů a předpisů, které se na vás vztahují. Společnost Microsoft se zříká veškeré odpovědnosti za jakékoli nároky související s vaší klasifikací dat  

Následující tabulka popisuje úrovně citlivosti dat, které můžete přiřadit.

|Citlivost|Popis|
|----|----|
|Citlivá | Informace o rasovém nebo etnickém původu subjektu údajů, politických názorech, náboženských vyznáních, zapojení do odborů, fyzickém nebo duševním zdraví, sexualitě nebo podrobnosti o trestných činech. |
|Osobní | Informace, které lze použít k identifikaci subjektu, buď přímo, nebo v kombinaci s jinými údaji nebo informacemi.|
|Důvěrná pro společnost | Obchodní data, která používáte pro účetní nebo jiné obchodní účely a nechcete je vystavovat jiným subjektům. Může to například zahrnovat položky účetní knihy.|
|Normální | Obecná data, která nepatří do žádné jiné kategorie.|

## <a name="how-do-i-classify-my-data"></a>Jak mohu klasifikovat svá data?
Klasifikace citlivosti velkého počtu polí po jednom by vyžadovala dlouhou dobu. Abychom urychlili proces klasifikace, poskytujeme nástroje, které můžete použít k hromadné klasifikaci citlivosti polí, a poté můžete doladit detaily klasifikace pro konkrétní pole. Nástroje najít nástroj Klasifikace dat, který je k dispozici v centru rolí Administrace uživatelů, uživatelských skupin a oprávnění . Abyste mohli seznam používat, musíte být správce systému.

> [!Important]
> Při prvním otevření seznamu Klasifikace dat bude prázdný. Chcete-li vygenerovat seznam polí, musíte spustit Průvodce klasifikací dat. Chcete-li spustit průvodce, vyberte akci **Nastavit klasifikaci dat**.

Například pracovního seznamu Klasifikace dat umožňuje provádět následující činnosti:  

* Pomocí Průvodce klasifikací dat exportujte svá pole do listu aplikace Excel, kde je můžete hromadně klasifikovat. Použití listu Excel je zvláště užitečné, pokud spolupracujete s partnerem společnosti Microsoft. Po aktualizaci listu můžete pomocí průvodce importovat a použít klasifikace. Průvodce můžete také použít k ruční klasifikaci polí.  
* Vyberte pole a poté filtrujte seznam a vyhledejte podobná pole, která pravděpodobně patří do stejné klasifikace jako pole, na kterém jste založili vyhledávání.  
* Prohlédněte si pole zobrazením jeho obsahu.  

> [!Tip]
> Definovali jsme klasifikace vzorků citlivosti pro tabulky a pole v demonstrační společnosti Cronus. Klasifikaci však můžete použít jako inspiraci při klasifikaci vlastních tabulek a polí.

## <a name="see-also"></a>Viz také
[Klasifikace dat](https://docs.microsoft.com/en-us/dynamics-nav/classifying-data)  
