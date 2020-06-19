---
title: Synchronization and Data Integration | Microsoft Docs
description: The synchronization copies data between Dynamics 365 Sales entries and Business Central records, and keeps the data in both systems up-to-date.
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf

---

# Synchronizace dat v Business Central a Dynamics 365 for Sales
Když integrujete [!INCLUDE[crm_md](includes/crm_md.md)] s [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete rozhodnout, zda chcete synchronizovat data ve vybraných polích záznamů [!INCLUDE[d365fin](includes/d365fin_md.md)] (například zákazníci, kontakty a prodejci) s ekvivalentními záznamy v [!INCLUDE[d365fin](includes/d365fin_md.md)] (jako jsou účty, kontakty a uživatelé). V závislosti na typu záznamu můžete synchronizovat data z [!INCLUDE[crm_md](includes/crm_md.md)] do [!INCLUDE[d365fin](includes/d365fin_md.md)] nebo naopak. Pro více informací, navštivte [Integrace s Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

Synchronizace používá následující prvky:

* Mapování tabulky integrace
* Mapování polí integrace
* Pravidla synchronizace
* Párování záznamů

Při nastavení synchronizace můžete párovat záznamy [!INCLUDE[d365fin](includes/d365fin_md.md)] se záznamy [!INCLUDE[crm_md](includes/crm_md.md)] na synchronizaci jejich dat. Synchronizaci můžete spustit ručně nebo na základě plánu. Následující tabulka obsahuje přehled způsobů, jakými lze synchronizovat záznamy.

| Typ | Metoda | Viz |
|--------|----------|-------|  
| Ruční synchronizace | Synchronizuje na základě záznamů.<br /><br /> Jednotlivé záznamy lze synchronizovat v [!INCLUDE[d365fin](includes/d365fin_md.md)], jako je například zákazník, s odpovídajícím záznamem [!INCLUDE[crm_md](includes/crm_md.md)], například účet. To je obvykle způsob, jak uživatelé budou pracovat s daty [!INCLUDE[crm_md](includes/crm_md.md)] v [!INCLUDE[d365fin](includes/d365fin_md.md)]. | [Ruční párování a synchronizace záznamů](admin-manual-synchronization-of-table-mappings.md) |
|  | Synchronizuje na základě mapování tabulky.<br /><br /> Všechny záznamy v tabulce [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete synchronizovat s entitou [!INCLUDE[crm_md](includes/crm_md.md)]. | [Synchronizace mapování jednotlivých tabulek](admin-manual-synchronization-of-table-mappings.md) |
|  | Synchronizuje všechny upravené záznamy pro všechna mapování tabulek.<br /><br /> Můžete synchronizovat všechny záznamy, které byly změněny v tabulkách [!INCLUDE[d365fin](includes/d365fin_md.md)] od poslední synchronizace. | [Synchronizace všech změněných záznamů](admin-manual-synchronization-of-table-mappings.md) |
|  | Plná synchronizace všech dat pro všechna mapování tabulek.<br /><br /> Můžete synchronizovat všechna data v tabulkách [!INCLUDE[d365fin](includes/d365fin_md.md)] a entitách [!INCLUDE[crm_md](includes/crm_md.md)], které jsou mapovány, a vytvářejí nové záznamy v cílovém řešení pro neoddělené záznamy ve zdrojovém řešení.<br /><br /> Úplná synchronizace synchronizuje všechna data a ignoruje párování. Obvykle provádíte úplnou synchronizaci, když nastavíte integraci a pouze jedno řešení obsahuje data. Úplná synchronizace může být také užitečná v demonstračním prostředí. | [Spuštění úplné synchronizace](admin-manual-synchronization-of-table-mappings.md) |
| Plánovaná synchronizace | Synchronizuje všechny změny dat pro všechna mapování tabulek.<br /><br /> Můžete synchronizovat [!INCLUDE[d365fin](includes/d365fin_md.md)] s [!INCLUDE[crm_md](includes/crm_md.md)] v plánovaných intervalech nastavením úloh ve frontě úloh. | [Plánovaní synchronizace](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md) |

## Standardní mapování entit prodeje pro synchronizaci
Entity v [!INCLUDE[crm_md](includes/crm_md.md)], jako jsou například účty, jsou integrovány s ekvivalentnými typy entit v [!INCLUDE[d365fin](includes/d365fin_md.md)], jako jsou například zákazníci. Chcete-li pracovat s daty [!INCLUDE[crm_md](includes/crm_md.md)], nastavte propojení, nazývané párování, mezi entitami v [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)].

Následující tabulka uvádí standardní mapování mezi entitami v [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)], které poskytuje [!INCLUDE[d365fin](includes/d365fin_md.md)].

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Směr synchronizace | Výchozí filtr |
|-------------------------------------------|-----|-------------------------|--------------|
| Prodejce/nákupčí | Uživatel | [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtr kontaktu prodeje: **Stav** je **Ne**, **Uživatel licencován** je **Ano**, Režim integrace uživatelů je **Ne** |
| Zákazník | Účet | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtr kontaktu prodeje: **Typ vztahu** je **Zákazník** a **Stav** je **Aktivní**. |
| Kontakt | Kontakt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] filtr kontaktu: **Typ** je **Osoba** a kontakt je přiřazen firmě. Filtr kontaktu prodeje: Kontakt je přiřazen společnosti a typ nadřazeného zákazníka je **Účet** |
| Měna | Měna transakce | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Měrná jednotka | Skupina jednotek | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Zboží | Produkt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtr kontaktu prodeje: **Typ produktu** je **Prodejní zásoba** |
| Zdroj | Produkt | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtr kontaktu prodeje: **Typ produktu** je **Služba** |
| Cenová skupina zákazníka | Ceník | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Prodejní cena | Ceník produktu | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] filtr kontaktu: **Kód prodeje** není prázdný, **Typ prodeje** je **Cenová skupina zákazníka** |
| Příležitost | Příležitost | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |
| Hlavička prodejní faktury | Faktura | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Řádek prodejní faktury | Produkt na faktuře | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Záhlaví prodejní objednávky | Prodejní objednávka | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[d365fin](includes/d365fin_md.md)] Filtr prodejní hlavičky: **Typ dokumentu** je Objednávka, **Stav** je Vydaná |
| Poznámky prodejní objednávky | Poznámky prodejní objednávky | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |

### Tip pro Administrátoři: zobrazení mapování entit
Můžete si zobrazit mapování mezi entitami v [!INCLUDE[crm_md](includes/crm_md.md)] a tabulkami v [!INCLUDE[d365fin](includes/d365fin_md.md)] na stránce **Mapování tabulky integrace**, kde můžete také použít filtry. Mapování definujete mezi poli v tabulkách [!INCLUDE[d365fin](includes/d365fin_md.md)] a pole v entitách [!INCLUDE[crm_md](includes/crm_md.md)] na stránce **Mapování pole integrace**, kde můžete přidat další logiku mapování. To může být užitečné například v případě, že potřebujete vyřešit synchronizaci.

### Tip pro vývojáře: Mapování polí v Business Central na sady možností v prodeji
Pokud jste vývojář a chcete přidat možnosti do sad možností v [!INCLUDE[crm_md](includes/crm_md.md)], musíte to vědět. V [!INCLUDE[d365fin](includes/d365fin_md.md)] jsou tři tabulky, které jsou mapovány do polí voleb entity **Účet** v [!INCLUDE[crm_md](includes/crm_md.md)]. Záznamy v tabulkách, které nejsou propojeny s možnostmi v [!INCLUDE[crm_md](includes/crm_md.md)], nebudou synchronizovány. To znamená, že pole **Volba** bude prázdné v [!INCLUDE[crm_md](includes/crm_md.md)].

V následující tabulce jsou uvedena mapování z tabulek [!INCLUDE[d365fin](includes/d365fin_md.md)] pro pole **Volba** v entitě **Účet** v [!INCLUDE[crm_md](includes/crm_md.md)].

| Tabulka | Pole Volba v entite účet |
|----------------------|-------------------------------------------|
| Platební podmínky | Platební podmínky |
| Způsob dodávky | Adresa 1: Dodací podmínky |
| Přepravce | Adresa 1: Způsob dopravy |

### Pravidla synchronizace
Následující tabulka popisuje pravidla, která řídí synchronizaci mezi aplikacemi.

> [!NOTE]
> Změny dat v [!INCLUDE[crm_md](includes/crm_md.md)], které byly provedeny uživatelským účtem [!INCLUDE[crm_md](includes/crm_md.md)], nejsou synchronizovány. Doporučujeme proto, abyste během používání tohoto účtu neměnili data. Pro více informací navštivte [Nastavení uživatelských účtů pro integraci s Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

| Tabulka | Pravidlo |
|-----|----|
| Zákazníci | Dříve než může být zákazník synchronizován s účtem, musí být prodejce, který je přiřazen k zákazníkovi, spojen s uživatelem v [!INCLUDE[crm_md](includes/crm_md.md)]. Proto když spustíte úlohu synchronizace Zákazníci - Dynamics 365 for Sales a nastavíte ji tak, aby vytvořila nové záznamy, nezapomeňte před synchronizací zákazníků s účty synchronizovat prodejce s uživateli [!INCLUDE[crm_md](includes/crm_md.md)] v [!INCLUDE[crm_md](includes/crm_md.md)]. <br /> <br />Úloha synchronizace zákazníci-Dynamics 365 for Sales synchronizuje pouze účty prodeje, které mají typ vztahu Zákazník. |
| Kontakty | V [!INCLUDE[crm_md](includes/crm_md.md)] budou vytvořeny pouze kontakty v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hodnota kódu prodejce definuje vlastníka spojené entity v [!INCLUDE[crm_md](includes/crm_md.md)]. |
| Měny | Měny jsou spojeny s měnami transakcí v [!INCLUDE[crm_md](includes/crm_md.md)] na základě kódů ISO. Pouze měny, které mají standardní kód ISO, budou spojeny a synchronizovány s měnami transakcí. |
| Měrné jednotky | Měrné jednotky jsou synchronizovány se skupinami jednotek v [!INCLUDE[crm_md](includes/crm_md.md)]. Ve skupině jednotek může být definována pouze jedna měrná jednotka. |
| Zboží | Při synchronizaci zboží s produkty [!INCLUDE[crm_md](includes/crm_md.md)] vytvoří produkt automaticky [!INCLUDE[d365fin](includes/d365fin_md.md)] ceník v  [!INCLUDE[crm_md](includes/crm_md.md)]. Chcete-li se vyhnout chybám synchronizace, neměli byste tento ceník upravovat ručně. |
| Prodejci | Prodejci jsou spojeni s uživateli systému v [!INCLUDE[crm_md](includes/crm_md.md)]. Uživatel musí být aktivován a licencován a nesmí být uživatelem integrace. Všimněte si, že se jedná o první tabulku, kterou je třeba synchronizovat, protože se používá ve zákaznících, kontaktech, příležitostech a prodejních fakturách. |
| Zdroje | Zdroje jsou synchronizovány s produkty [!INCLUDE[crm_md](includes/crm_md.md)], které mají typ produktu Služba. |
| Cenové skupiny zákazníka | Cenové skupiny zákazníka jsou synchronizovány s ceníky. |
| Prodejní ceny | Prodejní ceny, které mají typ prodeje Cenová skupina zákazníka a mají definovaný prodejní kód, jsou synchronizovány s řádky ceníku [!INCLUDE[crm_md](includes/crm_md.md)] |
| Příležitosti | Příležitosti jsou synchronizovány s příležitostmi [!INCLUDE[crm_md](includes/crm_md.md)]. Hodnota kódu prodejce definuje vlastníka spojené entity v [!INCLUDE[crm_md](includes/crm_md.md)]. |
| Účtované prodejní faktury | Účtované prodejní faktury jsou synchronizovány s prodejními fakturami. Před synchronizací faktury je lepší synchronizovat všechny ostatní subjekty, které se mohou faktury účastnit, od prodejců po ceníky. Hodnota kódu prodejce v záhlaví faktury definuje vlastníka propojené entity v prodeji. |
| Prodejní objednávky | Když je integrace prodejních objednávek povolena, jsou prodejní objednávky v [!INCLUDE[d365fin](includes/d365fin_md.md)], které jsou vytvořeny z odeslaných prodejních objednávek v [!INCLUDE[crm_md](includes/crm_md.md)], synchronizovány s prodejními objednávkami v Zahrnutých prodejích, když jsou vydané. Před synchronizací objednávek doporučujeme nejprve synchronizovat všechny entity, které se na objednávce podílejí, jako jsou prodejci a ceníky. Pole Kód prodejce v záhlaví objednávky definuje vlastníka spojené entity v [!INCLUDE[crm_md](includes/crm_md.md)]. |

## Viz také
[Ruční párování a synchronizace záznamů](admin-how-to-couple-and-synchronize-records-manually.md)  
[Plánování synchronizace](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Integrace s Dynamics 365 fot Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
