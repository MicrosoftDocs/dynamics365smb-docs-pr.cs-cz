---
title: Use Excel to import data into Business Central| Microsoft Docs
description: Use the default configuration package to add customer data in Excel and import the data back into Business Central .
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/01/2020
ms.author: edupont

---
# Import obchodních dat z jiných finančních systémů.
Když si zaregistrujete [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete si zvolit novou prázdnou společnost, kam můžete nahrát vaše vlastní data a testovat Váš nový [!INCLUDE[d365fin](includes/d365fin_md.md)]. V závislosti na finančním řešení, které vaše firma používá dnes, můžete přenášet informace o zákaznících, dodavatelích, zásobách a bankovních účtech.

V Centru rolí můžete spustit průvodce nastavením, který vám pomůže přenášet obchodní data ze souboru Excel nebo z jiných formátů. Typ souborů, které můžete nahrát, závisí na dostupných příponách. Můžete například migrovat data z  QuickBooks protože [!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje rozšíření, které zpracovává převod z QuickBooks. Pokud chcete migrovat data z jiných finančních programů, musíte buď zkontrolovat, zda je pro toto řešení k dispozici rozšíření, nebo importovat z aplikace Excel.

[!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje šablony pro účty, zákazníky, dodavatele a skladové položky, které můžete použít při importu dat.

Můžete importovat hlavní data a některá transakční data z jiných finančních systémů založených na výchozím konfiguračním balíčku v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Na stránce **Konfigurační balíčky** můžete pracovat s balíčkem, tedy importovat a ověřit data před použitím balíčku.

> [!TIP]  
> Případně použijte průvodce přenesením dat k importu dat z QuickBooks nebo Dynamics GP. Pro více infortmací navštivte [Migrace QuickBooks dat](ui-extensions-quickbooks-data-migration.md) nebo [Migrace Dynamics GP Dat](ui-extensions-dynamicsgp-data-migration.md).

> [!NOTE]  
> Pro objemnější implementační práci můžete použít služby RapidStart Services v [!INCLUDE[d365fin](includes/d365fin_md.md)], které jsou rozsáhlá sada nástrojů pro nastavení nových řešení na základě obchodních požadavků zákazníků a dat o nastavení. RapidStart Services také nabízí funkce pro import obchodních dat. Pro více informací navštivte [Nastavení společnosti pomocí RapidStart Services](admin-set-up-a-company-with-rapidstart.md)

Chcete-li importovat obrázky zboží, můžete použít vyhrazenou funkci na stránce **Nastavení zásob** page. Pro více informací navštivte [Hromadný import obrázků](inventory-how-import-item-pictures.md).

## Import dat z konfiguračních balíčků
[!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje konfigurační balíček, který můžete exportovat do aplikace Excel a vyplnit data v něm. Potom můžete data importovat znovu z aplikace Excel. Balíček se skládá z 27 tabulek, včetně hlavních dat, jako jsou zákazníci, dodavatelé, zboží a obchodní vztahy, dalších základních tabulek nastavení, jako jsou způsoby expedice a tabulek transakcí, jako je prodejní hlavička a řádky.

> [!NOTE]  
> Práce s konfiguračními balíčky je pokročilá funkce a doporučujeme vám kontaktovat správce. Pro více informací navštivte [ Import dat ze staršího účetního softwaru pomocí konfiguračních balíčků](across-import-data-configuration-packages.md).

## Práce s daty v Excelu
Při exportu výchozího konfiguračního balíčku do Excelu vygenerovaný sešit obsahuje list pro každou tabulku v balíčku. Pro zjednodušení vašich úkolů můžete využít mapovací nástroje XML, které jsou zabudovány do Excelu. Můžete také použít vestavěné funkce aplikace Excel, které vám pomohou s formátováním dat a vložením dat do správné buňky. Například, přidání prázdného listu a zkopírování starších dat. Potom vytvořte vzorec aplikace Excel pro mapování dat v transformačním listu mezi poli v exportovaném listu a staršími daty zákazníků. Po namapování všech dat zkopírujte oblast dat do listu tabulky.

> [!IMPORTANT]  
> Neměňte sloupce v listech. Pokud jsou přesunuty, změněny nebo odstraněny, nelze list importovat do [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Pole typu Blob nelze exportovat/importovat pomocí Excelu.

## Tabulky ve Výchozím konfiguračním balíčku
Výchozí konfigurační balíček podporuje následující tabulky:

- Platební podmínky
- Cenová skupina zákazníka
- Způsob dodávky
- Prodejci/Nákupčí
- Lokace
- Účet hlavní knihy
- Zákazník
- Dodavatele
- Zboží
- Prodejní hlavička
- Prodejní řádek
- Nákupní hlavička
- Nákupní řádek
- Obecné finančího deníku
- Řádek deníku zboží
- Účto skupiny zákazníků
- Účto skupiny dodavatele
- Účto skupiny zboží
- Měrné jednotky
- Obecné obchodní účto skupiny
- Obecné účto skupiny zboží
- Nastavení obecného účtování
- Teritoria
- Kategorie zboží
- Prodejní ceny
- Nákupní ceny

## Viz také
[Nastavení společnosti pomocí RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Migrace dat pomocí QuickBooks](ui-extensions-quickbooks-data-migration.md)  
[Migrace dat pomocí Dynamics GPn](ui-extensions-dynamicsgp-data-migration.md)  
[Hromadné importování obrázků zboží](inventory-how-import-item-pictures.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
