---
    title: How to Flush Components According to Operation Output | Microsoft Docs
    description: For items that are set up with backward flushing method, the default behavior is to calculate and post component consumption when you change the status of a released production order to **Finished**. For more information, see Flushing Method.
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
# Spotřeba komponent podle výstupní operace
U položek nastavených metodou zpětné spotřeby je výchozím chováním výpočet a zaúčtování spotřeby komponent při změně stavu vydané výrobní zakázky na **Dokončená** .

Pokud definujete také kódy vazeb TNG, pak výpočet a zaúčtování proběhne po dokončení každé operace a zaúčtování množství, které bylo skutečně spotřebováno v dané operaci. Pro více informací navštivte [Vytvoření TNG postupů](production-how-to-create-routings.md).

Pokud například výrobní zakázka na výrobu 800 metrů vyžaduje 8 kg komponenty, potom při účtovaní 200 metrů jako výstup, 2 kg se automaticky zaúčtuje jako spotřeba.

Tato funkce je užitečná z následujících důvodů:

- **Hodnota zásob** - položky ocenění pro výstup a spotřebu jsou vytvářeny souběžně, jak postupuje výrobní zakázka. Bez kódů TNG postupů se hodnota zásob zvýší při zaúčtování výstupu a potom se sníží v čase, kdy je hodnota spotřeby komponent zaúčtována společně s dokončenou výrobní objednávkou.
- **Dostupnost zásob** - s postupným účtováním spotřeby je dostupnost položek komponent více aktuální, což je důležité pro zachování vnitřní rovnováhy mezi poptávkou a nabídkou. Bez kódů vazeb technologického postupu se mohou jiné požadavky na komponentu domnívat, že jsou k dispozici tak dlouho, dokud čeká na zpožděné účtování spotřeby.
- **Just-in-time** – s možností vlastního nastavení produktů na požadavky zákazníků, můžete minimalizovat plýtvání tím, že práce a změny systému nastanou pouze v případě potřeby.

Následující postup ukazuje, jak kombinovat zpětnou spotřebu a směrovací kódy odkazů tak, aby množství, které je spotřebování pro každou operaci, bylo úměrné skutečnému výstupu dokončené operace.

## Spotřeba komponent podle výstupu operace
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte tlačítko **Úpravy**.
3. V záložce **Doplnění**, v poli **Metoda spotřeby**, vyberte **Předem**.

   > [!NOTE]
   > Pokud je komponenta použita v lokaci, která je nastavena pro řízené zaskladnění a vyskladnění, vyberte možnost **Vyskladnění + předem**.

4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **TNG postupy** a poté vyberte související odkaz.
5. Definujte kódy vazeb technologického postupu pro každou operaci, která zpracovává komponentu. Pro více informací navštivte [Vytvoření TNG postupů](production-how-to-create-routings.md).
6. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kusovník** a poté vyberte související odkaz.
7. Definujte kódy vazeb technologického postupu z každé instance komponenty k operaci, kde je spotřebováno.

   > [!IMPORTANT]
   > Komponenta musí obsahovat propojení s poslední operací v TNG postupu.

## Viz také
[Vytvoření výrobního kusobníku](production-how-to-create-production-boms.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
