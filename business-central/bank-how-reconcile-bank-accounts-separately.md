---
title: Odsouhlasení bankovních účtů odděleně | Microsoft Docs
description: 'Popisuje, jak je hodnota zásob odsouhlasena s financemi.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bank account balance, bank statement'
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="reconcile-bank-accounts-separately"></a>Odsouhlasit bankovní účty samostatně

Chcete-li odsouhlasit bankovní účty [!INCLUDE[d365fin](includes/d365fin_md.md)] s výpisy obdrženými z banky, začněte vyplněním podokna na stránce **Odsouhlasení bankovního účtu** informacemi z bankovního výpisu, které pak porovnáte (odsouhlasíte) s položkami bankovních účtů v pravém podokně. Inteligentní způsob vyplnění řádků bankovních výpisů je importem souboru nebo zdrojem bankovních výpisů.

> [!NOTE]  
> V severoamerických verzích můžete tuto práci provést také v **Sešitu  odsouhlasení bankovního účtu**,  který je vhodnější pro šeky a vklady, ale nenabízí import souborů výpisu z účtu Chcete-li místo stránky **Odsouhlasení bankovního účtu** použít tuto stránku, odznačte volbu ** Automatické Odsouhlasení bankovního účtu **  pole shoda v  **Nastavení financí**. Další informace naleznete v části „Odsouhlasit bankovní účty“ v části lokální funkce Spojených států.

> [!TIP]  
> Bankovní účty můžete také odsouhlasit na stránce **Deníky odsouhlasení plateb** . Všechny otevřené položky účetní knihy vztahující se k použitým položkám účetní knihy odběratele nebo dodavatele budou uzavřeny, pokud zvolíte akci **Účtování plateb a odsouhlasení bankovního účtu**. To znamená, že bankovní účet je automaticky odsouhlasen pro platby, které zaúčtujete do deníku. Pro více informací bežte na [Automatické odsouhlasení plateb.](receivables-how-reconcile-payments-auto-application.md)

Chcete-li povolit import bankovních výpisů jako bankovní zdroje, musíte nejprve nastavit a povolit službu Envestnet Yodlee Bank Feed a poté propojit své bankovní účty se souvisejícími online bankovními účty. Pro více informací navštivte [Nastavení Envestnet  yodlee Bank služby](bank-how-setup-bank-statement-service.md).

Řádky na stránce **Odsouhlasení bankovního účtu** jsou rozděleny do dvou podoken. V podokně **Řádky bankovního výpisu** se zobrazují buď importované bankovní transakce nebo položky s nezaplacenými platbami. V podokně **Položky bankovního účtu** se zobrazí položky bankovního účtu.

Aktivita hledání a vyrovnání položek, které mají být odsouhlaseny, se označuje jako *Shoda*. Můžete zvolit, aby se porovnávání provádělo automaticky pomocí funkce **Shoda automaticky** . Alternativně můžete ručně vybrat řádky v obou podoknech pro propojení jednotlivých řádků bankovního výpisu s jednou nebo více souvisejícími položkami bankovního účtu a potom použít funkci **Shoda ručně** . V řádcích, kde se položky shodují, je vybráno **Vyrovnané** zaškrtávací políčko.

Můžete vyplnit podokno **Řádky bankovních výpisů** v **Odsouhlasení bankovního účtu** následujícími způsoby:

* Automaticky pomocí funkce **Import bankovního výpisu** k vyplnění řádků podle skutečných bankovních výpisů na základě souboru poskytovaném bankou.
* Ručně, pomocí funkce **Navrhnout řádky** vyplňte řádky s položkami pro faktury, které mají nezaplacené platby.

Když se hodnota v poli **Celkové saldo** v podokně **Řádky bankovního výpisu** rovná hodnotě v poli **Saldo k odsouhlasení** v okně **Položky bankovního účtu** , můžete zvolit akci **Zaúčtování** , která bude odsouhlasovat vyrovnání položek bankovního účtu. Všechny nevyrovnané položky bankovního účtu zůstanou na stránce, což znamená, že platby zpracované pro bankovní účet se neodrážejí v posledním bankovním výpisu nebo že některé platby byly přijaty při kontrolách.

> [!NOTE]  
>   Pokud se řádky bankovního výpisu vztahují k položkám šeků, nelze použít odpovídající funkce. Místo toho musíte zvolit akci **Vyrovnat položky** a pak vybrat příslušnou položku šeku, která bude odpovídat řádku bankovního výpisu.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Postup při vyplňování řádků odsouhlasení bankovního výpisu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Odsouhlasení bankovního účtu** a poté vyberte související odkaz.
2. Vyberte akci **Nová**.
3. V poli **Číslo bankovního účtu** vyberte příslušný bankovní účet. Položky bankovního účtu, které existují na bankovním účtu, se zobrazí v okně **Položky bankovního účtu**.
4. Do pole **Datum výpisu** zadejte datum výpisu z banky.
5. Do pole **Zůstatek** zadejte saldo výpisu z banky.
6. Pokud máte soubor bankovního výpisu, zvolte akci **Import bankovního výpisu** .
7. Najděte soubor a pak zvolte **Otevřit** tlačítko pro Import bankovních transakcí do řádků na stránce **Odsouhlasení bankovního účtu** .

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Chcete-li vyplnit řádky odsouhlasení banky funkcí Navrhnout řádky
1. Na stránce **Odsouhlasení bankovního účtu** zvolte akci **Navrhnout řádky** .
2. Do pole **Počáteční datum** zadejte nejstarší datum účtování, aby se položky účetní knihy shodovaly.
3. Do pole **Koncové datum** zadejte poslední zúčtovací datum položek, které se mají odsouhlasit.
4. Zaškrtněte políčko **Včetně šeků** pro všechny návrhy položek šeků namísto odpovídajících položek bankovního účtu.
5. Klepněte na tlačítko **OK** .

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Automatická shoda řádků bankovních výpisů s položkami bankovních účtů
Stránka nabízí funkci automatického přiřazování, která aplikuje platby na související otevřené položky na základě shody textu na řádku výpisu z bankovního účtu (levý panel) s textem na jednom nebo více záznamech z bankovních účtů (pravý panel). Upozorňujeme, že můžete přepsat automaticky navrhované návrhy a můžete se rozhodnout, že automatické navrhování nebudete používat vůbec. Další informace naleznete v dalším postupu.

1. Na stránce **Odsouhlasení bankovního účtu** zvolte **Automatická shoda**. Otevře se stránka **Mapuj položky banky**
2. V poli **Odchylka data transakce (dny)** určete rozsah dnů před a za zúčtovacím datem položky bankovního účtu, v rámci kterého bude funkce vyhledávat odpovídající data transakcí v bankovním výpisu.

    Pokud zadáte hodnotu 0 nebo necháte pole prázdné, bude funkce **Shoda automaticky** vyhledávat pouze odpovídající data transakcí v zúčtovacím datu položky bankovního účtu.
3. Klepněte na tlačítko **OK** .

    Všechny řádky bankovního výpisu a položky bankovního účtu, které lze přiřadit jsou zobrazeny zeleným písmem, a je zaškrtnuto políčko **Vyrovnáno** .
4. Chcete-li odebrat shodu, vyberte řádek bankovního výpisu a pak zvolte akci **Odstranit shodu** .

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Ruční přiřazení řádků bankovních výpisů k položkám účetní knihy
1. Na stránce **Odsouhlasení bankovního účtu** vyberte nepoužitý řádek v okně **Řádky bankovního výpisu** .
2. V podokně **Položky bankovního účtu** vyberte jednu nebo více bankovních položek bankovních účtů, které lze spárovat s vybraným řádkem bankovního výpisu. Chcete-li vybrat více řádků, stiskněte a podržte klávesu Ctrl.
3. Vyberte akci **Shoda ručně**.

    Vybraný řádek bankovního výpisu a vybrané položky bankovního účtu se změní na zelené písmo a je vybráno **Vyrovnané** zaškrtávací políčko v pravém podokně.
4. Opakujte kroky 1 až 3 pro všechny řádky bankovního výpisu, které nejsou shodné.
5. Chcete-li odebrat shodu, vyberte řádek bankovního výpisu a pak zvolte akci **Odstranit shodu** .

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Vytvoření chybějících položek pro odpovídající bankovní transakce
V některých případech bankovní výpis obsahuje částky úroků nebo účtovaných poplatků. Takové bankovní transakce nelze spárovat, protože v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)] neexistují žádné související položky. Poté je nutné zaúčtovat řádek deníku pro každou transakci a vytvořit tak související položku, se kterou lze spárovat.

1. Na stránce **Odsouhlasení bankovního účtu** zvolte položku **Transfer do finančního deníku** .  
2. Na stránce **Převod odsouhl.bank.účtu do fin.den.** určete, který obecný deník se má použít, a poté zvolte tlačítko **OK**.

    Otevře se stránka **Finanční deník** , která obsahuje nové řádky deníku pro všechny řádky výpisu z banky s chybějícími položkami.
3. Vyplňte řádek deníku odpovídajícími informacemi, například protiúčtem. Další informace naleznete v části [Práce s Finančním deníkem](ui-work-general-journals.md).  
4. Chcete-li si prohlédnout výsledek účtování před účtováním, zvolte akci **Testovací sestava** . Otevře se sestava **Výpis bankovního účtu** a zobrazí stejná pole jako v hlavičce stránky **Odsouhlasení bank. účtu**.
4. Vyberte akci **Účtovat**.

    Když je položka zaúčtována, pokračujte tak, aby odpovídala bankovní transakci.
5. Obnovte nebo znovu otevřete stránku **Odsouhlasení bankovního účtu** . Nová položka knihy se zobrazí v podokně **Položky knihy bankovních účtů**.
6. Řádek bankovního výpisu porovnejte s položkou účetní knihy, buď ručně nebo automaticky.

## <a name="see-also"></a>Viz také
[Správa bankovních účtů](bank-manage-bank-accounts.md)  
[Nastavení bankovnictví](bank-setup-banking.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
