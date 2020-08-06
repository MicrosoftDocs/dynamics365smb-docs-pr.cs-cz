---
    title: How to Create Production Order Headers | Microsoft Docs
    description: You can create a production order manually, and the first step is to create a production order header.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Vytváření výrobních zakázek
Výrobní zakázku můžete vytvořit ručně s tím, že prvním krokem je vytvoření záhlaví výrobní zakázky.

Výrobní zakázky jsou obvykle vytvořeny automaticky pomocí funkce plánování ke splnění známé poptávky. Pro více informací navštivte [Plánování](production-planning.md).

V následujícím postupu je vytvořena pevně plánovaná výrobní zakázka. Můžete také vytvořit výrobní zakázky s jiným stavem.

## Vytvoření hlavičky výrobní zakázky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pevně plánované výr.  zak.** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Do pole **Číslo** zadejte další číslo v řadě.
4. V poli **Typ původu** vyberte zdroj výrobní zakázky.

   Zde si můžete vybrat, zda chcete vyrábět pro skupinu zboží. Pro více informací navštivte [Práce se skupinami výrobků](production-how-work-family.md).
5. V poli **Číslo původu** vyberte číslo zboží, skupinu nebo hlavičku prodeje, pro kterou má být výrobní zakázka generována.
6. Vyplňte pole **Množství** a **Datum plánování** podle vašich požadavků.

Při změně výrobních požadavků, jako jsou komponenty nebo operace, můžete výrobní zakázku rychle přeplánovat. Pro více informací navštivte [Přeplánování nebo přímá aktualizace výrobních zakázek](production-how-to-replan-refresh-production-orders.md).

## Viz také
[Výroba](production-manage-manufacturing.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
