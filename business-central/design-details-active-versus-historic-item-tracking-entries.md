---
    title: Design Details - Active versus Historic Item Tracking Entries | Microsoft Docs
    description: When parts of a document line quantity are posted, only that particular quantity is transferred to the item ledger entries and its item tracking numbers. However, you will want to access all relevant item tracking information directly from the active document line. That is, not only will you want to see the entries that are related to the remaining quantity, you will also want information about the units that have been posted. When you view or modify the **Item Tracking Lines** page, the collective contents of the **Tracking Specification** table (T336) and **Reservation Entry** table (T337) are presented in a temporary version of T336. This ensures that historic and active item tracking data is accessed as one.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Aktivní versus historické položky sledování zboží
Při zaúčtování částí řádku dokladu je do položek zboží a jeho čísel sledování zboží převedeno pouze toto určité množství. Nicméně budete chtít získat přístup ke všem relevantním informacím o sledování položek přímo z aktivního řádku dokumentu. To znamená, že budete chtít nejen zobrazit položky, které souvisejí se zbývajícím množstvím, ale budete také chtít informace o položkách, které byly zaúčtovány. Když zobrazíte nebo upravíte stránku **Řádky sledování zboží**, celkový obsah tabulky (T336) **Specifikace sledování** a tabulky (T337) **Položky rezervace** jous zobrazeny v dočasné verzi tabulky T336. Tím je zajištěno, že historické a aktivní sledování zboží je přístupné jako jedno.

The following table shows how T336 and T337 are used in a purchase scenario. Tučná čísla představují hodnoty, které uživatel ručně zadá na stránce  **Řádky sledování zboží**.

Krok 1: Vytvořte řádek nákupní objednávky se sedmi kusy se sledování zboží.

||**Množství (Základ)**|**Množství ke zpracování**|**Množství k fakturaci (Základ)**|**Zpracované množství (Základ)**|**Fakturované množství (Základ)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|

Krok 2: Napřímujte čtyři kusy.

||**Množství (Základ)**|**Množství ke zpracování**|**Množství k fakturaci (Základ)**|**Zpracované množství (Základ)**|**Fakturované množství (Základ)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Stránka **Řádky sledování zboží**|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|

Krok 3: Napřímujte a vyfakturujte dva kusy.

||**Množství (Základ)**|**Množství ke zpracování**|**Množství k fakturaci (Základ)**|**Zpracované množství (Základ)**|**Fakturované množství (Základ)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Stránka **Řádky sledování zboží** |7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|

Krok 4: Napřímujte jeden kus.

||**Množství (Základ)**|**Množství ke zpracování**|**Množství k fakturaci (Základ)**|**Zpracované množství (Základ)**|**Fakturované množství (Základ)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Stránka **Řádky sledování zboží**|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|

Vyfakturujte pět kusů.

||**Množství (Základ)**|**Množství ke zpracování**|**Množství k fakturaci (Základ)**|**Zpracované množství (Základ)**|**Fakturované množství (Základ)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Stránka **Řádky sledování zboží**|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|

## Viz také
[Detaily návrhu: Sledování zboží](design-details-item-tracking.md)   
[Detaily návrhu: Stránka řádky sledování zboží](design-details-item-tracking-lines-window.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]