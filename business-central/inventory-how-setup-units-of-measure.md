---
title: Jak nastavit měrné jednotky | Microsoft Docs
description: 'Pro zboží můžete nastavit více měrných jednotek, takže můžete ke zboží přiřadit měrné jednotky.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 10/01/2018
ms.author: SorenGP
---
# <a name="set-up-item-units-of-measure"></a>Nastavení Měrné jednotky
Pro zboží můžete nastavit více měrných jednotek, takže ke zboží můžete přiřadit měrné jednotky pro následující účely:

- Na kartě zboží přiřaďte danému zboží základní měrnou jednotku, abyste určili, jak se bude ukládat v zásobách, a sloužit jako základ převodu pro alternativní měrné jednotky.
- Přiřaďte alternativní měrné jednotky k nákupním, výrobním nebo prodejním dokladům a určete, kolik jednotek základní měrné jednotky v těchto procesech zpracováváte současně. Například můžete zakoupit položku na paletách a ve výrobě používat pouze jednotlivé kusy.

Pokud je zboží na skladě v jedné měrné jednotce, ale je vyrobené v jiné měrné jednotce, vytvoří se výrobní zakázky, která používá výrobní dávkovou měrnou jednotku k výpočtu správného množství komponent během dávkové úlohy **Aktualizace výrobní zakázky**. Příkladem výpočtu výrobní jednotky je, když je vyrobená položka skladována v kusech, ale je vyrobena v tunách. Pro více informací navštivte [Práce s výrobními měrnými jednotkami](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Nastavení Měrné jednotky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky** a poté vyberte související odkaz.
2. Otevřete kartu zboží, pro kterou chcete nastavit alternativní měrné jednotky.
3. Vyberte akci **Měrné jednotky**. Otevře se stránka **Měrné jednotky zboží**.
4. Pokud je pole **Základní měrné jednotky** na kartě zboží vyplněno, je tato měrná jednotka již nastavena.
5. Zvolte akci **Nový**. Vloží se nový prázdný řádek.
6. Do pole **Kód** zadejte název měrné jednotky. Případně vyberte pole pro výběr z kódů měrných jednotek, které jsou v databázi.
7. Do pole **Množství v jednotce** zadejte, kolik jednotek základní měrné jednotky obsahuje nová měrná jednotka.
8. Opakováním kroků 5 až 7 nastavte všechny alternativní měrné jednotky, které chcete pro tuto položku použít v různých procesech.

Nyní můžete použít alternativní měrné jednotky pro nákupní, výrobní a prodejní doklady. Pro více informací navštivte Zadání výchozích jednotek měrných kódů pro nákupní a prodejní transakce nebo Použití měrné jednotky výrobní dávky.

## <a name="to-set-up-unit-of-measure-translations"></a>Nastavení překladů měrné jednotky
Pokud prodáváte zboží zahraničním zákazníkům, můžete chtít určit měrnou jednotku v jazyce zákazníka. To můžete provést poté, co jste nastavili potřebné překlady měrné jednotky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Měrné jednotky** a poté vyberte související odkaz.
2. Vyberte kód pro transakci, kterou chcete nastavit, a poté vyberte akci **Překlady**.
3. V poli **Kód jazyka** vyberte šipku rozevíracího seznamu a zobrazí se seznam dostupných jazykových kódů. Vyberte kód jazyka, pro který chcete vložit překlad, a poté stisknutím tlačítka OK zkopírujte kód do pole.
4. Do pole **Popis** zadejte příslušný text.
5. Opakujte kroky 2 až 4 pro kódy měrné jednotky a jazyky, pro které chcete zadat překlady.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Zadávaní výchozího kódu měrné jednotky pro prodejní a nákupní transakce
Pokud obvykle nakupujete nebo prodáváte v jednotkách odlišných od základní měrné jednotky, můžete zadat samostatné měrné jednotky pro nákupy a prodeje. Za tímto účelem musí být měrné jednotky nastaveny na stránce **Měrné jednotky zboží**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky** a poté vyberte související odkaz.
2. Otevřete kartu příslušného zboží, pro kterou chcete zadat výchozí kód prodejní nebo nákupní měrné jednotky.
3. V případě prodeje otevřete v záložce **Fakturace** v poli **Prodejní jednotka** stránku **Měrné jednotky zboží**.
4. Pro nákup, na záložce **Doplnění**, v poli **Nákupní  jednotka**, otevřete stránku **Měrné jednotky zboží**.
5. Vyberte kód, který chcete nastavit jako výchozí měrnou jednotku pro prodej nebo nákup, a poté zvolte tlačítko **OK**.

## <a name="see-also"></a>Viz také
[Práce s měřítkem výrobních dávkových jednotek](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Správa zásob](inventory-manage-inventory.md)  
[Správa nákupu](purchasing-manage-purchasing.md)  
[Správa prodeje](sales-manage-sales.md)    
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
