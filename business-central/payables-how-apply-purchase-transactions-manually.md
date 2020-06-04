---
title: Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries| Microsoft Docs
description: To process, match, or reconcile vendor payments or refunds manually, you apply the amount to one or more open vendor ledger entries.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment application, payment processing, match payments
ms.date: 10/01/2019
ms.author: sgroespe

---
# Odsouhlasení plateb dodavatele s deníkem plateb nebo z položek dodavatele
Při odeslání platby nebo vrácení peněz od dodavatele se musíte rozhodnout, zda platbu nebo refundaci použijete na jednu nebo více otevřených položek. Můžete určit přesnou částku, kterou chcete použít na potvrzení o platbě nebo vrácení peněz, a poté jen částečně použít položky dodavatele. K získání správné statistiky dodavatelů nebo sestavy výpisů z účtu a finančních nákladů, je nutné vyrovnat všechny položky dodavatele.

> [!NOTE]
> Dodavatelé mohou někdy poskytnout vrácení platby namísto dobropisu, aby částku započetli proti budoucím fakturám a to se děje zejména když vrátíte položky, které jste již zaplatili, nebo když jste fakturu přeplatili.

Položky dodavatele můžete vyrovnat třemi různými způsoby:

* Zadáním informací na vyhrazených stránkách, například na stránce **Deník plateb** a **Deník odsouhlasení plateb**.
* Z nákupních dobropisu
* Z položek dodavatele po zaúčtování nákupních dokladů, ale nejsou použity.

> [!NOTE]
> Pokud pole **Metoda vyrovnání** na kartě dodavatele obsahuje **Vyrovnat nejstarší**, budou platby, pokud ručně nezadáte, který záznam se má vyrovnat, automaticky vyrovnány na nejstarší otevřený úvěr. Pokud je metoda vyrovnání zákazníka **Ručně**, tak musíte položky vyrovnat ručně.

Platby dodavatele můžete vyrovnat ručně na související nákupní doklady při zaúčtování plateb na stránku **Deník plateb**. Pro více informací o vyplňování platebního deníku naleznete v části [Provádění plateb](payables-make-payments.md).

Můžete také vyrovnat platby dodavatele a platby zákazníka poté, co se platby objeví ve vaší bance jako negativní bankovní transakce. Na stránce **Deník odsouhlasení plateb**, můžete použít funkce pro import bankovních výpisů, automatické vyrovnání a odsouhlasení bankovních účtů. Pro více informací navštivte [Automatické odsouhlasení plateb](receivables-how-reconcile-payments-auto-application.md).

## Vyrovnání platby s jednou nebo více položkami dodavatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník plateb** a poté vyberte související odkaz.
2. Na stránce **Deník plateb** zadejte na první řádek deníku příslušné informace o položce platby.
3. Pro vyrovnání jedné položky dodavatele:
   1. Na poli **Č. vyrovnání  dokladu**, vyberte pole pro otevření stránky **Vyrovnat položky dodavatele**.
   2. Na stránce **Vyrovnat položky dodavatele**, vyberte položku, se kterou chcete platbu vyrovnat.
   3. Na řádku v poli **Částka k vyrovnání**, zadejte částku, kterou chcete použít pro položku.
4. Pro vyrovnání několika položek dodavatele:

   1. Vyberte akci **Vyrovnat položky**.
   2. Na stránce **Vyrovnat položky dodavatele**, vyberte řádky s položkami, se kterými má být platba vyrovnána
   3. Vyberte akci **Nastavit ID vyrovnání**.
   4. Na každém řádku v poli **Částka k použití**, zadejte částku, která má být pro jednotlivé položky aplikována.

      Pokud částku nezadáte, bude automaticky vyrovnána maximální částka. Ve spodní části stránky **Vyrovnat položky dodavatele**, můžete vidět částku a to v poli Vyrovnaná částka a můžete také vidět vyrovnané zůstatky.
5. Zvolte tlačítko **OK**.
6. Pro zaúčtování deníku plateb zvolte akci **Účtovat**.

## Vyrovnání dobropisu pro jednu nebo více položek dodavatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní dobropis** a poté vyberte související odkaz.
2. Otevřete dobropis, který chcete použít.
3. Do záhlaví zadejte příslušné informace.
4. Vyrovnání jedné položky dodavatele na záložce **Vyrovnání** v poli **Č. vyrovnání  dokladu**, vyberte položku, se kterou chcete vyrovnat účet dal, a poté v poli **Částka k vyrovnání**, zadejte částku, která má být s položkou vyrovnána.
5. Pro vyrovnání několika položek dodavatele:

   1. Vyberte akci **Vyrovnat položky**.
   2. Vyberte řádky s položkami, se kterými má být dobropis vyrovnán.
   3. Vyberte akci **Nastavit ID vyrovnání**.
   4. Na každém řádku v poli **Částka k použití**, zadejte částku, která má být pro jednotlivé položky aplikována.

      Pokud částku nezadáte, bude automaticky vyrovnána maximální částka. Ve spodní části stránky **Vyrovnat položky dodavatele**,  můžete vidět částku a to v poli Vyrovnaná částka a můžete také vidět vyrovnané zůstatky.
6. Zvolte tlačítko **OK**.
Stránka **Nákupní dobropis** zobrazuje položku, kterou jste vybrali na poli **Typ vyrovnání dokladu** a na poli **Číslo vyrovnání dokladu**. Na této stránce je také uvedena částka dobropisu, který má být zaúčtován, upravený o případné platební slevy.
7. Zvolte tlačítko **Zaúčtovat** pro zaúčtování nákupního dobropisu.

## Vyrovnání zaúčtovaných položek dodavatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Otevřete příslušného dodavatele s položkami, které již byly zaúčtovány.
3. Vyberte akci **Položky hlavní knihy**, a poté vyberte akci **Vyrovnat položky**.
4. Na stránce **Vyrovnat položky dodavatele**, můžete vidět otevřené položky dodavatele.
5. Vyberte řádek s položkou, která bude vyrovnána.
6. Vyberte akci **Nastavit ID vyrovnání**.

   Pole **ID vyrovnání** zobrazuje tři hvězdičky, pokud pracujete v systému pro jednoho uživatele, nebo vaše ID uživatele, pokud pracujete ve víceuživatelském systému.
7. Pro každý řádek v poli **Částka k vyrovnání** pole, zadejte částku, která má být pro jednotlivé položky použita.

   Pokud částku nezadáte, bude automaticky vyrovnána maximální částka. Částku můžete zobrazit v poli **Vyrovnaná částka** v dolní části stránky **Vyrovnat položky dodavatele**.
8. Vyberte akci **Účtovat vyrovnání**.

   Stránka **Účtovat vyrovnání** se otevře s číslem dokladu vyrovnávané položky a se zúčtovacím datem položky s nejnovějším zúčtovacím datem.
9. Vyberte tlačítko **OK** pro účtování vyrovnání.

## Vyrovnání položek dodavatele v různých měnách mezi sebou
Pokud nakupujete od dodavatele v jedné měně a provádíte platbu v jiné měně, stále můžete platbu vyrovnat s fakturou.

Pokud vyrovnáte položku (položka 1) v jedné měně s položkou (položka 2) v jiné měně, zúčtovací datum v položce 1 se použije k nalezení příslušného směnného kurzu pro převod částek v položce 2. Příslušný směnný kurz se nachází na stránce **Směnné kurzy**. V takovém případě musíte povolit vyrovnání položek dodavatele v různých měnách. Další informace naleznete v části [Povolit vyrovnání položek v různých měnách](finance-how-enable-application-ledger-entries-different-currencies.md)

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník plateb** a poté vyberte související odkaz.
2. Otevřete požadovaný deník a vyplňte první prázdný řádek deníku pomocí kódu měny.
3. Vyberte akci **Vyrovnat položky**.
4. Select the line with the entry you want to apply to the entry in the payment journal, choose the **Set Applies-to ID** action, and then select the entry you want to apply to.
5. Zvolte tlačítko **OK** a vraťte se tak do deníku plateb.
6. Zaúčtování deník plateb

> [!IMPORTANT]
> Když použijete k sobě záznamy v různých měnách, položky se převedou na USD. I když jsou směnné kurzy pro obě příslušné měny pevné, například mezi USD a EUR, může existovat malá zbytková částka, pokud jsou tyto částky v cizí měně převedeny na USD. Tyto malé zbytkové částky jsou zaúčtovány jako zisky a ztráty na účet zadaný v polích **Účet realizovaných zisků** nebo **Účet realizovaných ztrát** na stránce **Měny**. Pole **Částka (USD)** je také upraveno pro příslušné položky dodavatele.

## Zrušení vyrovnání položek dodavatele
Když nepoužijete chybné vyrovnání, vytvoří se a zaúčtují pro všechny položky, včetně všech účtování hlavní knihy odvozených z vyrovnání, jako je skonto a měnové zisky/ztráty, nové opravné položky, které jsou shodné s původní položkou, ale s opačným znaménkem v poli částky. Položky, které byly srovnány, jsou znovu otevřeny.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Otevřete příslušnou kartu dodavatele.
3. Vyberte akci **Položky hlavní knihy**.
4. Vyberte příslušnou položku hlavní knihy a poté vyberte akci **Zrušit vyrovnání položek**.
5. Alternativně zvolte akci **Detailní položky knihy** .
6. Vyberte příslušnou položku vyrovnání a poté vyberte akci **Zrušit vyrovnání položek**.
7. Vyplňte pole v záhlaví a poté vyberte akci **Zrušit vyrovnání**.

> [!IMPORTANT]
> Pokud byla položka použita více než jednou položkou aplikace, musíte nejprve použít poslední položku aplikace.

## Viz také
[Správa závazků](payables-manage-payables.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
