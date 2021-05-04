---
    title: Dimension Set Entries Overview | Microsoft Docs
    description: This topic describes how dimension set entries are stored and posted in Dynamcis 365.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: dimension
    ms.date: 10/01/2020
    ms.author: edupont

---
# Přehled položek sad dimenzí
Toto téma popisuje, jak jsou položky sady dimenzí uloženy a zaúčtovány v [!INCLUDE[prod_short](includes/prod_short.md)].

## Sady dimenzí
Sada dimenzí je jedinečná kombinace hodnot dimenzí. Je uložena jako položky sady dimenzí v databázi. Každá položka sady dimenzí představuje jednu hodnotu dimenze. Sada dimenzí je identifikována společným ID sady dimenzí, které je přiřazeno každé položce sady dimenzí, která patří do sady dimenzí.

Následující příklad ukazuje sadu dimenzí, která má tři položky sady dimenzí. Sada dimenzí je identifikována ID sady dimenzí, což je 108.

| ID sady dimenzí | Kód dimenze | Kód hodnoty dimenze | Název hodnoty dimenze |
|----------------------|--------------------|--------------------------|--------------------------|  
| 108 | AREA | 70 | Severní Amerika |
| 108 | BUSINESSGROUP | HOME | Domácí |
| 108 | DEPARTMENT | SALES | Prodej |

## Položky sady dimenzí
Sady dimenzí jsou uloženy v tabulce **Položky sady dimenzí** jako položky sady dimenzí se stejným ID sady dimenzí.

![Tok položek sady dimenzí](media/dimensionentrynav7.png "Tok položek sady dimenzí")

Když vytvoříte nový řádek deníku, hlavičku dokladu nebo řádek dokladu, můžete zadat kombinaci hodnot dimenze. Namísto explicitního ukládání každé hodnoty dimenze v databázi je k řádku deníku, hlavičce dokladu nebo řádku dokladu přiřazeno ID sady dimenzí k určení sady dimenzí.

Když upravíte a zavřete stránku **Upravit položky sady dimenzí** provede se kontrola, aby se zjistilo, zda kombinace hodnot dimenzí existuje jako dimenze nastavená v tabulce. Pokud k kombinaci dojde v tabulce, bude odpovídající ID sady dimenzí přiřazeno řádku deníku, hlavičce dokladu nebo řádku dokladu. V opačném případě je do tabulky přidána nová sada dimenzí a nové ID sady dimenzí je přiřazeno řádku deníku, hlavičce dokladu nebo řádku dokladu.

## Codeunita 408 Správa dimenzí
Codeunita 408, Správa dimenzí, je knihovna funkcí, která zpracovává běžné úkoly, které souvisejí s dimenzemi, jako je kopírování z jedné tabulky do druhé nebo z jednoho dokumentu do druhého.

## Zlepšení výkonu
Uložením sad dimenzí jednou v databázi se zachová databázový prostor a zlepší se celkový výkon.

## Viz také
[Detaily návrhu: Vyhledávání kombinace dimenzí](design-details-searching-for-dimension-combinations.md)   
[Detaily návrhu: Struktura tabulky](design-details-table-structure.md)   
[Detaily návrhu: Položky sady dimenzí](design-details-dimension-set-entries.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]