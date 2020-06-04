---
title: Apply and Modify Saved Settings on Reports | Microsoft Docs
description: Describes using predefined options and filters to customize a report, and to generate the correct data.
author: jswymer

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2019
ms.author: jswymer

---
# Správa uložených nastavení sestav
Při spuštění sestav se uživatelům obvykle zobrazí stránka, která umožňuje nastavit určité možnosti a filtry pro změnu dat zahrnutých do generované sestavy. Tato stránka se nazývá stránka úpravy sestavy. Sestava může obsahovat jedno nebo více *uložených nastavení*, která mohou uživatelé použít pro sestavu na stránce požadavků. *Uložené nastavení* jsou v podstatě přednastavené možnosti a filitry. Použití uložených nastavení představuje rychlý a spolehlivý způsob, jak důsledně generovat sestavy obsahující správná data. Další informace o použití uložených nastavení naleznete v části <x5 />Používání uložených nastavení](ui-work-report.md#SavedSettings).

Pokud máte příslušná oprávnění, můžete prohlížet, vytvářet a upravovat uložená nastavení pro všechny sestavy pro všechny uživatele ve společnosti. Uložená nastavení pro sestavu můžete přiřadit jednotlivým uživatelům nebo všem uživatelům ve společnosti.

<!--
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## Vytvořit a upravit uložené nastavení pro všechny uživatele
Uložená nastavení se spravují na stránce **1560 Nastavení sestav** . Tuto stránku lze otevřít dvěma způsoby:
- Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení sestav** a poté vyberte související odkaz.
- Otevřete sestavu, vyberte vyhledávání vedle pole **Použít výchozí hodnoty z:**, vyberte **Vybrat z úplného seznamu**.

Stránka zobrazuje všechny existující položky nastavení ukládání pro všechny uživatele. Pokud je ve sloupci **Přiřazeno k** jméno uživatele, uložená nastavení pro přidruženou sestavu může použít pouze tento uživatel. Pokud je zaškrtnuto políčko **Sdílet se všemi uživateli **, mohou použít uložené nastavení sestavy všichni uživatelé.

Na stránce **Nastavení sestav** můžete:
- Zvolit **Nový** k vytvoření nové položky uloženého nastavení sestav.
- Vybrat uloženou položku nastavení ze seznamu a zvolit **Kopírovat** pro vytvoření kopie.
- Vyberat položku uloženého nastavení ze seznamu a zvolit **Upravit** pro úpravu uložené položky nastavení.


> [!Important]
> Zvažte jméno, které zadáte pro uloženou položku nastavení.. Pokud vytvoříte uloženou položku nastavení pro všechny uživatele a přiřadíte jí stejný název jako existující položka nastavení přiřazená pouze určitému uživateli, nebude moci tento uživatel použít uloženou položku nastavení přiřazenou všem.  V části **Uložená nastavení** na stránce požadavku na sestavu uvidí uživatelé dvě uložené položky nastavení se stejným názvem. Avšak bez ohledu na to, kterou možnost uživatel zvolí, bude použita uložená položka nastavení specifická pro uživatele.

> [!NOTE]
<x3 /> Funkce uloženého nastavení je dostupná pouze u sestav, kde je vlastnost [Uložit hodnoty​](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) na stránce sestavy nastavena na `Ano`. Vlastnost **SaveValues - Uložit hodnoty** se nastavuje ve vývojovém prostředí.

## Viz také
[Práce se sestavami a dávkovými úlohami ](ui-work-report.md)
