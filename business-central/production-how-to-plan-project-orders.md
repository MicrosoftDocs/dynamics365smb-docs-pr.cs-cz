---
    title: How to Plan Project Orders | Microsoft Docs
    description: This planning task starts from a sales order and uses the **Sales Order Planning** page. Once you have created a project production order, you can plan it further by using the **Order Planning** page.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Plánování projektové objednávky
Tato plánovací úloha začíná od prodejní objednávky a používá stránku **Plánování prod.objednávky**. Po vytvoření výrobní zakázky projektu ji můžete dále naplánovat pomocí stránky **Plánování objednávek**.

## Vytvoření výrobní zakázky projektu

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Vyberte prodejní objednávku, která představuje výrobní projekt, a pak zvolte akci **Plánování**.
4. Na stránce **Plánování prod.objednávky**, vyberte akci **Vytvořit výr. zakázku**.
5. Na stránce **Vytvořit výrobní zakázku z prodejní objednávky**, na poli **Typ objednávky**, vyberte **Projektové objednávky**.
6. Vyberte tlačítko **Ano**.
7. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
8. Otevřete právě vytvořenou výrobní zakázku.

   Všimněte si, že pole výrobní zakázky **Typ zdroje** obsahuje **Prodejní hlavičku** a objednávka má více řádků, jeden pro každou prodejní řádkovou položku, která musí být vyrobena.
9. Vyberte akci **Plánování**.
10. Na stránce **Plánování objednávek**, vyberte akci **Obnovit**  pro výpočet to nové poptávky.

Řádek záhlaví objednávky pro projektovou objednávku se zobrazí se všemi nevyplněnými řádky poptávky rozbalenými pod ním. Přestože výrobní zakázka obsahuje řádky pro několik vyrobených položek, celková poptávka pro všechny řádky výrobní zakázky je uvedena pod jedním řádkem hlavičky objednávky na stránce **Plánování objednávek**, a je zobrazeno původní jméno zákazníka. Nyní můžete pokračovat v plánování poptávky, jak je popsáno v [Plán nové poptávky podle objednávky](production-how-to-plan-for-new-demand.md).

> [!NOTE]
> Řádky výrobní zakázky ve výrobní zakázce, které mají **Výrobní zakázku** v jejich poli **Systém doplnění** představují základní výrobní zakázky. Po vygenerování těchto výrobních objednávek musíte znovu vypočítat plán na stránce **Plánování objednávek** abyste identifikovali případnou nevyplněnou poptávku po nich. V takovém případě se zobrazí jako řádky poptávky pod řádkem záhlaví normální výrobní zakázky, což znamená, že na stránce již není viditelný vztah projektu. Pokud však používáte funkci Sledování objednávek, můžete se podívat tam i zpět na všechny objednávky dodávek provedené v rámci původní prodejní objednávky.

## Viz také
[Plánování](production-planning.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)  
[Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
