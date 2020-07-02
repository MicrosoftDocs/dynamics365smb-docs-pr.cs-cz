---
title: Issue, Print, Cancel, and Void Checks| Microsoft Docs
description: Describes how to issue checks using the payment journal, print checks, and void or view check ledger entries in Business Central.  
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: sgroespe

---
# Provádění plateb šekem
Elektronické a ruční šeky můžete vydat v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Obě metody používají deník plateb k vydávání šeků dodavatelům. Můžete také šeky zrušit a zobrazit jejich položky.

Následující postup ukazuje, jak zaplatit dodavateli počítačovým šekem pomocí platby na příslušnou fakturu dodavatele, vytisknutím šeku a následným zaúčtováním platby jako zaplacené. Výsledkem je kladná položka dodavatele, která se aplikuje na záporné položky bankovního účtu, a fyzické šeky pro zpracování v bance.

Můžete platit dvěma typy šeků. Pro oba typy, musí pole **Typ  protiúčtu** nebo **Typ účtu** obsahovat **Bankovní účet**.

- **Počítačový šek**: Tuto možnost vyberte, pokud chcete vytisknout částku šeku na řádku deníku plateb. Šeky musíte vytisknout dříve, než budete moci zaúčtovat řádky deníku.
- **Ruční šek**: Tuto možnost vyberte, pokud jste vytvořili šek ručně a chcete pro tuto částku vytvořit odpovídající položku šeku. Pomocí této možnosti nelze šek vytisknout.

> [!NOTE]
> Abyste zajistili, že vaše banka smaže pouze ověřené šeky a částky, můžete jim odeslat soubor, který obsahuje informace o dodavateli, šeku a platbě. Pro více informací navštivte [Export souboru kladných plateb](finance-how-positive-pay.md).

Tiskárna musí být správně nastavena pomocí šekových formulářů a musíte definovat, které rozvržení šeku se má použít. Pro více informací navštivte [Výběr rozvržení šeku](finance-how-define-check-layouts.md)

Pro kontrolní kód můžete vytisknout až 10 faktur na stránce. Pokud se šek vztahuje na více než 10 faktur, při tisku zrušíme šek na první stránce a na šek vytiskneme slovo ZRUŠENO. Potom vytiskneme zbytek faktur a celkovou částku šeku na druhé stránce.

## Platba faktury dodavatele pomocí počítačového šeku
Následující text popisuje, jak zaplatit dodavateli šekem. Postup je podobný jako refundace šekem u zákazníka.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Deníky plateb** a poté vyberte související odkaz.
2. Vyplňte řádky deníku plateb. Pro více informací navštivte [Evidence plateb a náhrad](payables-how-post-payments-refunds.md).
3. V poli **Kód způsobu platby** vyberte **Šek**.
4. V poli **Typ platby v bance** vyberte **Počítačový šek**.
5. Vyberte akci **Tisk šeku**.
6. Na stránce **Šek** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Zvolte tlačítko **Odeslat do**, vyberte možnost **Dokument PDF** a poté zvolte tlačítko **OK**.

   Fyzické šeky lze nyní přenést do banky ke zpracování. Pokračujte v účtování platby, jak byla použita u dodavatele, a tím ji zaplaťte v systému.
8. Vyberte akci **Účtovat**.

Jsou vytvářeny plně vyrovnány položky dodavatele a položky banky.

> [!NOTE]
> Pokud chcete tisknout a platit šeky ve více než jedné měně z různých bankovních účtů, musíte pro každou měnu spustit samostatnou dávkovou úlohu **Tisk šeku** a zadat příslušný bankovní účet.

## Zrušení tištěných šeků, které nejsou zaúčtovány
Nezaúčtované šeky můžete zrušit po vytištění pomocí akce **Zrušit šek** na stránce **Deníky plateb**.

1. Na stránce **Deníky plateb** vyberte **Zrušit šek** poté vyberte, které šeky chcete zrušit.

## Zrušení šeků
Po zaúčtování platby šekem můžete zrušit (neplatné) šeky pouze z výsledných položek banky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Vyberte příslušný bankovní účet, vyberte akci **Upravit** a poté vyberte akci **Položky šeků**.
3. Na stránce **Položky šeků** vyberte akci **Zrušit šek**.
4. Zaškrtněte políčko **Pouze zrušit šek**.
5. Vyberte tlačítko **OK**.

## Zobrazení souhrnu zaúčtovaných šeků
Pokud chcete zkontrolovat zaúčtované šeky, například pro ověření více šeků zaplacených jednomu dodavateli, můžete použít sestavu **Bankovní účet-detaily šeku**.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účet-detaily šeku** a poté vyberte související odkaz.
2. Nastavte filtry jako relevantní a poté zvolte tlačítko **Náhled**.

## Viz také
[Provádění plateb](payables-make-payments.md)  
[Správa závazků](payables-manage-payables.md)  
[Nastavení bankovnictví](bank-setup-banking.md)  
[Export souboru kladných plateb](finance-how-positive-pay.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
