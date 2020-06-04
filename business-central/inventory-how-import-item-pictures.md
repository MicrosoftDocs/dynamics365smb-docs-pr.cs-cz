---
title: Importing Many Item Pictures from a ZIP File| Microsoft Docs
description: You can import multiple item pictures in one go. Simply name your picture files with names corresponding to your item numbers, compress them to a zip file, and then use the Import Item Pictures page to manage which item pictures to import.
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 10/01/2019
ms.author: sgroespe

---
# Hromadný import obrázků zboží
Můžete hromadně importovat obrázky zboží. Jednoduše pojmenujte soubory obrázků názvy odpovídajícími číslům zboží, zkomprimujte je do souboru ZIP a potom pomocí stránky **Importovat obrázky zboží** určete, které obrázky zboží chcete importovat.

Podporovány jsou všechny běžné formáty souborů.

## Pojmenování souborů obrázků podle názvů zboží a příprava ZIP souboru
1. V místě, kde jsou obrázky zboží uloženy, pojmenujte každý soubor podle čísla souvisejícího zboží. Například:

   |Číslo zboží|Název souboru|
   |-|-|
   |1000|1000.bmp|
   |1001|1001.bmp|
   |1002|1002.bmp|

2. Seskupte všechny soubory do jednoho souboru ZIP. Například v Průzkumníkovi Windows vyberte soubory a poté kliknete pravým tlačítkem myši a zvolíte **Odeslat do** a dále **Komprimovaná složka (metoda ZIP)**.

## Import obrázků zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení zásob** a vybrat související odkaz.
2. Vyberte funkci **Importovat obrázky zboží**.
3. V poli **vyberte soubor ZIP**, vyberte příslušnou ZIP složku, a potí vyberte tlačítko **Otevřít**.

   Na stránce **Importovat obrázky zboží** je vytvořen řádek pro každé zboží a obrázek.

   > [!NOTE]
   > U karet zboží, kde již **Obrázky existují** je zaškrtnuto políčko. Pokud nechcete nahrazovat žádné stávající obrázky, zrušte zaškrtnutí políčka **Nahradit obrázky**. Pokud nechcete, aby byly jednotlivé existující obrázky nahrazeny, odstraňte dotyčné řádky.

3. Zvolte tlačítko **Importovat obrázky**.

Pole **Stav importu** je aktualizováno, aby ukazovalo, zda byl import obrázku přeskočen nebo dokončen.

## Viz také
[Evidence nového zboží](inventory-how-register-new-items.md)  
[Vytváření číselných řad](ui-create-number-series.md)  
[Zásoby](inventory-manage-inventory.md)  
[nakupování](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
