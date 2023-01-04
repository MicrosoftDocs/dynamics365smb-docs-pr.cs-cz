---
title: The Data Archive Extension
description: Archiving data creates a low-cost backup of your records.
author: brentholtorf


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 630
ms.date: 06/14/2021
ms.author: bholtorf

---

# Rozšíření Archiv dat
Časem se ve vaší firmě nahromadí značné množství dat a jako správce je pravděpodobně dobré mít strategii pro jejich archivaci. Množství dat může zpomalit práci, například generování sestav nebo dokonce uzamčení záznamů může trvat o něco déle. Velké množství dat navíc může vést ke zvýšeným nákladům na ukládání.

Rozšíření Archiv dat poskytuje základní balík pro archivaci a zálohování dat v rámci komprese dat. Při použití komprese dat se související záznamy sloučí do jediného záznamu a originály se odstraní. Pro více informací navštivte [Komprese dat pomocí komprimování dat](admin-manage-documents.md#compress-data-with-date-compression). Může se však stát, že si tato data ponecháte,a místo abyste je smazali je můžete archivovat pro pozdější použití.

## Zahájení archivace dat
Rozšíření je předinstalované a dostupné na **Správa rozšíření**, takže pro spuštění nemusíte nic dělat. Rozšíření je také k dispozici na Microsoft AppSource.

Vaše archivy dat jsou uvedeny na stránce **Přehled archivace dat**. Každý archiv může obsahovat data z více tabulek a může obsahovat až 10 000 záznamů. Pokud je v tabulce více než 10 000 záznamů, vytvoří se druhý archiv pro dalších 10 000 záznamů a tak dále. Pokud například archivujete 10 100 položky hlavní knihy, Business Central vytvoří jeden archiv "Položky" pro prvních 10 000 záznamů a poté druhý archiv pro zbývajících 100 záznamů.

Po archivaci dat je možné prozkoumat data pomocí aplikace Microsoft Excel nebo jako soubor CSV.

* Pokud použijete možnost Aplikace Excel, sešit bude obsahovat jeden list pro každou tabulku archivu dat.
* Pokud použijete možnost CSV, získáte soubor ZIP s jedním souborem CSV pro každou tabulku archivu dat.

> [!TIP]
> Možnosti Excel a CSV usnadňují použití jiné aplikace nebo služby pro přesun dat do jiného umístění, například do úložiště Azure Blob, nebo do analytického nástroje, například Microsoft Power BI.

Rozšíření Archiv dat používají následující dávkové úlohy pro kompresi data.

| Dávkové úlohy |
|---------|
| Datum Porov. Položky rozpočtu zboží |
| Datová komprese bankovních účtů   |
| Komprese položek zákazníka |
| Komprese položek DM |
| Komprese věcných položek |
| Komprese položek pojištění |
| Komprese dat údržby   |
| Komprese dat údržby   |
| Komprese položek zdrojů |
| Komprese DPH položek |
| Komprese položek dodavatele |
| Kompere skladových položek Položky |
| Datová kompere Položky finančního rozpočtu |

Chcete-li zahájit archivaci dat při spuštění jedné z dávkových úloh, zapněte přepínač **Archivovat odstraněné položky**.

## Důležité informace o úložišti
Archivovaná data jsou uložena v tabulce **Tenant Media**. Tato tabulka není zahrnuta při výpočtu velikosti databáze podle vašich licenčních podmínek. Místo toho se počítá jako úložiště souborů. Doporučujeme však exportovat staré archivy například do souboru CSV a poté odstranit staré záznamy archivu.

## Viz také
[Správa úložiště odstraněním dokumentů nebo kompresí dat](admin-manage-documents.md)
