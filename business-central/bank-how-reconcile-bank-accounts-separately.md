---
title: Odsouhlasení bankovních účtů po jednom | Microsoft Docs
description: 'Popisuje, jak je hodnota vašeho skladu sladěna s hlavní knihou.'
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
# <a name="reconcile-bank-accounts-separately"></a>Odsouhlasení bankovních účtů po jednom
K odsouhlasení bankovních účtů v [!INCLUDE[d365fin](includes/d365fin_md.md)] s výpisy obdrženými z banky. Začnete s vyplňováním podokna na levé straně na stránce **Odsouhlasení bankovního účtu** s informacemi o bankovních výpisech, které poté porovnáte (odsouhlasíte) s položkami účetní knihy v pravém podokně. Inteligentní způsob vyplnění řádků bankovních výpisů je importem souboru nebo zdroje bankovních výpisů.

> [!NOTE]  
> V severoamerických verzích můžete tuto práci provádět také na **Odsouhlasení bank. účtu. Stránka výkazu**, která je vhodnější pro šeky a vklady, ale nenabízí import souborů výpisu z účtu. Pokud chcete používat tuto stránku **Odsouhlasení bank. Účtu,**, vypněte **Automatické odsouhlasení bank. účtu Pole Shoda** na stránce **Nastavení financí**. Další informace naleznete v části „Odsouhlasit bankovní účty“ v části lokální funkce Spojených států.

> [!TIP]  
> Bankovní účty můžete také odsouhlasit na stránce **Deník odsouhlasení plateb**. Veškeré položky bankovních účtů, které se vztahují k položkám účtů zákazníků nebo prodejců budou uzavřeny, když zvolíte akci **Zaúčtování plateb a odsouhlasení bankovních účtů**. To znamená, že bankovní účet je automaticky odsouhlasen pro platby, které zaúčtujete do deníku. Pro více informací bežte na [Automatické odsouhlasení plateb](receivables-how-reconcile-payments-auto-application.md).

Chcete-li povolit import bankovních výpisů jako bankovní zdroje, musíte nejprve nastavit a povolit službu Envestnet Yodlee Bank Feed a poté propojit své bankovní účty se souvisejícími online bankovními účty. Pro více informací běžte na [Nastavení Envestnet  yodlee Bank služby](bank-how-setup-bank-statement-service.md).

Řádky na stránce **Odsouhlasení bankovních účtů** jsou rozděleny do dvou tabulek. V podokně **Řádky bankovní výpisů** se zobrazují buď importované bankovní transakce nebo položky knihy s nevyrovnanými platbami. V podokně **Položky hlavních bankovních účtů** se zobrazují záznamy položek na bankovním účtu.

Činnost zjišťování a používání položek, které mají být odsouhlaseny, se označuje jako *Shoda*. Můžete provést automatické přiřazování pomocí funkce **Automatická shoda**. Případně můžete ručně vybrat řádky v obou panelech, abyste propojili každý řádek bankovního výpisu s jednou nebo více souvisejícími položkami knihy bankovních účtů a poté použijte funkci **Ruční shoda**. Zaškrtávací políčko **Použito** je vybráno na řádcích, kde se položky shodují.

Můžete vyplnit podokno **Řádky bankovních výpisů** na stránce **Odsouhlasení bankovních účtů** následujícím způsobem:

* Automaticky funkce **Importovat bankovní výpisy** vyplní řádky podle skutečných bankovních výpisů na základě souboru poskytnutého bankou.
* Ručně pomocí funkce **Návrh řádků** zaplňte řádky s položkami knihy pro faktury, které mají nevyřízené platby.

Pokud se hodnota v poli **Celkový zůstatek** v podokně **Řádky bankovních výpisů** rovná hodnotě v poli **Zústatek k odsouhlasení** v podokně **Položky knihy bankovních účtů**, můžete zvolit akci **Zaúčtovat** za účelem odsouhlasení položek bankovního účtu. Veškeré nepoužité položky knihy bankovních účtů zůstanou na stránce, což znamená, že platby zpracované pro bankovní účet se nezobrazují v posledním bankovním výpisu nebo že některé platby byly obdrženy při kontrolách.

> [!NOTE]  
>   Pokud řádky bankovního výpisu odkazují na položky knihy, nemůžete použít odpovídající funkce. Namísto toho musíte vybrat akci **Použít položky** a poté vyberte příslušnou položku knihy, která odpovídá řádku bankovního výpisu.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Vyplnění řádků odsouhlasených bankou importováním bankovního výpisu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Odsouhlasení bankovního účtu** a poté vyberte související odkaz.
2. Zvolte akci **Nový**.
3. V poli **Číslo bankovního účtu** vyberte příslušný bankovní účet. Položky bankovního účtu, které se na bankovním účtu vyskytují, se zobrazí v podokně **Položky bankovního účtu**.
4. Do pole **Datum výpisu** zadejte datum výpisu z banky.
5. Do pole **Zůstatek o konečném výpisu** zadejte zůstatek výpisu z banky.
6. Pokud máte soubor s bankovním výpisem, zvolte akci **Importovat bankovní výpis**.
7. Vyhledejte soubor a poté zvolte tlačítko **Otevřít**, chcete-li importovat bankovní transakce do řádků na stránce **Odsouhlasení bankovních účtů**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Vyplnění řádků odsouhlasených bankou pomocí funkce Návrh řádků
1. Na stránce **Odsouhlasení bankovních účtů** zvolte akci **Návrh řádků**.
2. Do pole **Počáteční datum** zadejte nejdřívější datum zaúčtování položek knihy, které chcete odsouhlasit.
3. Do pole **Konečné datum** zadejte nejpozdější datum zaúčtování položek knihy, které chcete odsouhlasit.
4. Zaškrtněte políčko **Včetně šeků** na všechny doporučené položky knihy namísto odpovídajících položek knih bankovních účtů.
5. Zvolte tlačítko **OK**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Automatická shoda řádků bankovních výpisů s položkami bankovních účtů
Stránka nabízí funkci automatického přiřazování, která aplikuje platby na související otevřené položky na základě shody textu na řádku výpisu z bankovního účtu (levý panel) s textem na jednom nebo více záznamech z bankovních účtů (pravý panel). Upozorňujeme, že můžete přepsat automaticky navrhované návrhy a můžete se rozhodnout, že automatické navrhování nebudete používat vůbec. Další informace naleznete v dalším postupu.

1. Na stránce **Odsouhlasení bankovních účtů** zvolte **Automatická shoda**. Otevře se stránka **Shoda bankovních položek**.
2. V poli **Tolerance data transakce (dny)** zadejte rozpětí dnů před a po datu zaúčtování položky účetní knihy, ve kterém bude funkce hledat odpovídající data transakce v bankovním výpisu.

    Pokud zadáte hodnotu 0 nebo ponecháte pole prázdné, funkce **Automatická shoda** vyhledá pouze odpovídající data transakce v datu zaúčtování položek knihy bankovního účtu.
3. Zvolte tlačítko **OK**.

    Všechny řádky bankovního výpisu a položky bankovních účtů, které lze porovnat, se změní na zelené písmo a zaškrtne se políčko **Použito**.
4. Chcete-li odstranit shodu, vyberte řádek výpisu banky a potom zvolte akci **Odebrat shodu**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Ruční shoda řádků bankovních účtů s položkami knihy bankovního účtu
1. Na stránce **Odsouhlasení bankovních účtů** vyberte nepoužité řádky v podokně **Řádky bankovních výpisů**.
2. V podokně **Položky knih bankovních účtů** vyberte jednu nebo více položek v knize bankovních účtů, které lze porovnat s vybraným řádkem výpisu banky. Chcete-li vybrat více řádků, stiskněte a podržte klávesu Ctrl.
3. Zvolte akci **Ruční shoda**.

    Vybraný řádek bankovního výpisu a vybrané položky knihy bankovního účtu se změní na zelené písmo a zaškrtne se políčko **Použito** v pravém podokně.
4. Opakujte kroky 1 až 3 pro všechny řádky bankovního výpisu, které nejsou shodné.
5. Chcete-li odstranit shodu, vyberte řádek výpisu banky a potom zvolte akci **Odebrat shodu**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Vytvoření chybějící položky knihy tak, aby odpovídaly bankovním transakcím
Někdy bankovní výpis obsahuje částky za úroky nebo poplatky. Takové bankovní transakce nemohou být shodné, protože v [!INCLUDE[d365fin](includes/d365fin_md.md)] neexistují žádné související položky knihy. Musíte zaúčtovat řádek deníku pro každou transakci a vytvořit příslušnou položku knihy, kterou lze porovnat.

1. Na stránce **Odsouhlasení bankovních účtů** zvolte akci **Převést do finančního deníku**.  
2. Na stránce **Převod Přev.odsouhl.bank.účtu  do fin.den.** určete, který obecný deník se má použít, a poté zvolte tlačítko **OK**.

    Na stránce **Finanční deník** se otevřou nové řádky deníku pro všechny řádky bankovních výpisů s chybějícími položkami hlavní knihy.
3. Dokončete řádek deníku příslušnými informacemi, jako je vyrovnávací účet. Další informace naleznete v části [Práce s Finančním deníkem](ui-work-general-journals.md).  
4. Chcete-li zkontrolovat výsledek účtování před zveřejněním, vyberte tlačítko **Náhled účtování**. Otevře se sestava **Výpis bankovního účtu** a zobrazí se stejná pole jako v záhlaví stránky **Odsouhlasení bankovního účtu**.
4. Zvolte akci **Zaúčtovat**.

    Po zaúčtování položky postupujte tak, aby bankovní transakce odpovídala.
5. Obnovte nebo znovu otevřete stránku **Odsouhlasení bankovních účtů**. Nová položka hlavní knihy se objeví v podokně **Položky knihy bankovního účtu**.
6. Řádek bankovního výpisu porovnejte s položkou knihy bankovního účtu, a to ručně nebo automaticky.

## <a name="see-also"></a>Viz také
[Správa bankovních účtů](bank-manage-bank-accounts.md)  
[Nastavení bankovnictví](bank-setup-banking.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
