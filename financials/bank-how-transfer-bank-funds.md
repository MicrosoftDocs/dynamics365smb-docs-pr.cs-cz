---
title: Převod bankovních prostředků | Microsoft Docs
description: 'Částky z jednoho bankovního účtu na druhý, včetně různých měn, můžete převést zaúčtováním transakce do finančního deníku.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bank account transfer, multiple currencies'
ms.date: 06/02/2017
ms.author: sgroespe
---
# <a name="transfer-bank-funds"></a>Převod bankovních prostředků
Někdy budete možná muset převést částku z jednoho bankovního účtu na jiný. Chcete-li to provést, musíte odeslat transakci do finančního deníku. Úloha se liší v závislosti na tom, zda bankovní účty používají stejnou měnu nebo různé měny.

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a>Zaúčtování převodu mezi bankovními účty se stejným kódem měny
1. Zvolte pravém horním rohu zvolte ikonu ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png ""), zadejte **Finanční deník** a pak vyberte související odkaz.
2. Na řádku deníku vyplňte pole **Datum zaúčtování** a **Číslo dokumentu**
3. V poli **Typ účtu** vyberte **Bankovní účet**.
4. V poli **Číslo účtu** vyberte bankovní, ze kterého chcete peníze převést.
5. Do pole **Částka** zadejte částku, kterou chcete převést.
6. V poli **Typ protiúčtu** vyberte **Bankovní účet**.
7. V poli **Číslo Protiúčtu** vyberte bankovní účet, na který chcete peníze převést.
8. Zaúčtovat deník.

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a>Zaúčtování převodu mezi bankovními účty s různými kódy měn
Chcete-li převádět finanční prostředky mezi bankovními účty, které používají různé měny, musíte zaúčtovat dva řádky finančního deníku.

1. Zvolte pravém horním rohu zvolte ikonu ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png ""), zadejte **Finanční deník** a pak vyberte související odkaz.
2. Vytvořte dva řádky deníku a vyplňte pole **Datum zaúčtování** a **Číslo dokumentu**
3. Na prvním řádku deníku v poli **Typ** vyberte **Bankovní účet**.
4. V poli **Číslo účtu** vyberte bankovní účet, na který chcete peníze převést.
5. V poli **Částka** zadejte částku v měně bankovního účtu. Zadejte částku Dal se znaménkem mínus. Zadejte částku MD se znaménkem mínus.
6. V poli **Číslo protiúčtu** vyberte **Bankovní účet**.
7. V poli **Číslo Protiúčtu** vyberte bankovní účet, na který chcete peníze převést.
8. Na druhém řádku deníku v poli **Typ** vyberte **Bankovní účet**.
9. V poli **Číslo účtu** vyberte bankovní účet, na který chcete peníze převést.
10. V poli **Částka** zadejte částku v měně bankovního účtu. Zadejte částku Dal se znaménkem mínus. Zadejte částku MD se znaménkem mínus.
11. V poli **Číslo protiúčtu** vyberte **Bankovní účet**.  
12. V poli **Číslo Protiúčtu** vyberte bankovní účet, na který chcete peníze převést.

    > [!NOTE]  
    >   Pokud se kurzy používané v deníku liší od směnných kurzů v okně **Směnné kurzy**, zadejte třetí řádek pro kurzový zisk nebo ztrátu. Zadejte **Finanční účet** v poli **Typ účtu**. Zadejte číslo finančního účtu pro kurzový zisk nebo ztrátu v poli **Číslo účtu** Zadejte kurzový zisk nebo ztrátu v poli **Částka** s nebo bez znaménka mínus pro částku Dal a MD.
13. Zaúčtovat deník.

## <a name="see-also"></a>Viz také
[Správa bankovních účtů](bank-manage-bank-accounts.md)  
[Nastavení bankovnictví](bank-setup-banking.md)  
[Práce s finančními deníky](ui-work-general-journals.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
