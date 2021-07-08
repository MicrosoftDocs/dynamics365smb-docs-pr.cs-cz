---
title: Using Word Templates for Bulk Communications | Microsoft Docs
description: Word templates can make it easy to bulk create documents that are personalized for specific entities.
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf

---

# Použití šablon aplikace Word pro hromadnou komunikaci
Šablony Microsoft Word mohou usnadnit hromadnou komunikaci s entitami, jako jsou zákazníci a dodavatelé. Můžete například vytvořit brožury, které zákazníky upozorní na prodejní kampaň, dopisy informující dodavatele o nových zásadách nákupu nebo pozvánky k přilákání kontaktů na nadcházející událost.

Jako zdroj dat pro šablonu můžete použít entity v [!INCLUDE[prod_short](includes/prod_short.md)] a přidat slučovací pole k personalizaci dokumentů pro každou entitu. Slučovací pole pocházejí z entity v [!INCLUDE[prod_short](includes/prod_short.md)]. Když použijete šablonu Wordu na entitu, do dokumentu se vloží data ze slučovacích polí.

Na stránce **Šablony aplikace Word**můžete pomocí průvodce instalací s asistencí stáhnout soubor ZIP, který obsahuje DataSource.txt a soubor šablony Word pro entitu. Poté, co nastavíte šablonu a přidáte slučovací pole, použijete stejnou příručku k nahrání šablony. Můžete použít pouze soubory šablony Word a zdroje dat, které stáhnete z [!INCLUDE[prod_short](includes/prod_short.md)] a soubory musíte ukládat na stejném místě.

> [!NOTE]
> Když vyberete entitu, pro kterou chcete vytvořit šablonu, zobrazí se v seznamu všechny entity v [!INCLUDE[prod_short](includes/prod_short.md)]. Nelze však vytvořit šablony pro všechny entity. Pokud název entity obsahuje speciální znaky, například **/**, **.**, **_**, or **-**nelze pro něj vytvořit šablonu. Název entity se zobrazuje ve sloupci  **Popis objektu**.

Když nastavujete šablonu v aplikaci Word, můžete na kartě **Rozesílání e-mailů** přidat slučovací pole výběrem  **Vložit slučovací pole**.

> [!NOTE]
> Nelze použít slučovací pole, pokud název pole obsahuje 40 znaků nebo více. Například nemůžete použít pole Company__Information_Customs_Permit_Date, protože má 40 znaků.

Až bude vaše šablona Wordu připravena, můžete na stránce **Šablony aplikace Word** zvolit **Použít** a vygenerovat dokumenty. Můžete buď vytvořit jeden dokument, který obsahuje sekce pro každou entitu, nebo rozdělit operaci a vytvořit nový dokument pro každou entitu.

## Vytvoření šablony Wordu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony aplikace Word<x5/> a poté vyberte související odkaz.
2. Postupujte podle pokynů v průvodci nastavením. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Viz také
[Správa rozvržení sestav a dokladů](ui-manage-report-layouts.md)
