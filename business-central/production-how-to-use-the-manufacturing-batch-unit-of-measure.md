---
    title: How to Use the Manufacturing Batch Unit of Measure | Microsoft Docs
    description: If an item is stocked in one unit of measure but produced in another, then the production order must be use a manufacturing batch unit of measure to calculate the correct quantity of components. An example of a manufacturing batch unit of measure calculation is when a manufactured item is stocked in pieces but produced in tons.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2019
    ms.author: sgroespe

---
# Práce s měrnými jednotkami výrobní dávky
Pokud je zboží skladováno v jedné měrné jednotce, ale vyráběno v jiné, vytvoří se výrobní zakázka, která používá měrnou jednotku výrobní dávky k výpočtu správného množství komponent během dávkové úlohy **Aktualizace výrobní zakázky** . Příkladem výpočtu měrné jednotky výrobní dávky je, když je vyrobeno zboží skladované v kusech, ale vyrobené v tunách.

## Vytvoření výrobního kusovníku pomocí měrné jednotky dávky
1. Měrná jednotka výrobní dávky je nastavena jako alternativní měrná jednotka na stránce **Měrné jednotky zboží** u zboží, které má být vyrobeno. Měrná jednotka dávky nenahrazuje základní měrnou jednotku zboží.
2. Vytvořte výrobní kusovník pro položku nastavenou s měrnou jednotkou výrobní dávky. Pro více informací navštivte [Vytvoření výrobního kusovníku](production-how-to-create-production-boms.md).
3. V poli **Kód měrné jednoty** zvolte měrnou jednotku výrobní dávky.
4. Pro každý řádek výrobního kusovníku v poli **Množství za** zadejte množství této položky komponenty, které je potřebné k vytvoření této měrné jednotky dávky.
5. Otevřete **Kartu zboží** pro související zboží.

   V záložce **Doplnění** v poli **Číslo výrobního kusovníku** a vyberte výše vytvořený výrobní kusovník.
6. Vytvořte hlavičku výrobní zakázky pomocí zboží nastavené s měrnou jednotkou výrobní dávky. Pro více informací navštivte [Vytvoření montážní zakázky](production-how-to-create-production-orders.md).
7. Vyberte akci **Aktualizace** a poté stiskněte tlačítko **OK**.

V záložce **Řádky** vyberte talčítko **Řádek** a pak zvolte tlačítko **Komponenty** . Program vypočte správné množství komponent potřebných ke splnění výrobního kusovníku na základě měrné jednotky výrobní dávky.

## Výpočet měrné jednotky výrobní dávky na výrobní zakázce
1. Vytvořte hlavičku výrobní zakázky pomocí zboží nastavené s měrnou jednotkou výrobní dávky.
2. Do pole **Číslo zboží** na řádku výrobní zakázky zadejte stejné číslo zboží použité v hlavičce.
3. Do pole **Množství** zadejte stejné množství použité v hlavičce.
4. V poli **Kód měrné jednotky** vyberte kód měrné jednotky výrobní dávky.
5. Vyberte tlačítko **Aktualizovat**.
6. V záložce **Vypočítat** zrušte zaškrtnutí políčka **Řádky**.
7. Klikněte na tlačítko **OK**.
8. V záložce **Řádky** vyberte talčítko **Řádek** a pak zvolte tlačítko **Komponenty** . Správné množství komponent potřebných k uspokojení výrobního kusovníku se vypočítá na základě výrobní šarže měrné jednotky.

## Viz také
[Vytvoření TNG postupů](production-how-to-create-routings.md)  
[Vytvoření výrobního kusovníku](production-how-to-create-production-boms.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
