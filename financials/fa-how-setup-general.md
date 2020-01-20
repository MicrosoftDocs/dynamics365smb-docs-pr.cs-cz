---
title: Nastavení hlavní knihy DM | Microsoft Docs
description: 'Než začnete pracovat s dlouhodobým majetkem, musíte nastavit výchozí finanční účty, účtovací skupiny, alokační klíče, šablony deníků a listy a kódy tříd.'
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 29/01/2018
ms.author: edupont
---
# <a name="set-up-general-fixed-assets-information"></a>Nastavení obecných informací o dlouhodobém majetku
Než budete moci spravovat dlouhodobý majetek, musíte nastavit výchozí finanční účty, alokační klíče, šablony deníků a dávky pro zaúčtování dlouhodobého majetku a reklasifikaci a klasifikovat dlouhodobý majetek v třídách, jako je Hmotný a Nehmotný.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Nastavení obecných výchozích hodnot pro dlouhodobý majetek
Definujte obecné chování nebo funkčnost dlouhodobého majetku a nastavte řadu čísel dokumentu v okně **Nastavení dlouhodobého majetku**.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Dlouhodobý majetek** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-fixed-asset-posting-groups"></a>Nastavení účtovacích skupin dlouhodobého majetku
Pomocí účtovacích skupin můžete definovat skupiny dlouhodobého majetku. Položky pro tyto účtovací skupiny jsou zaúčtovány na stejných účtech hlavní knihy.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), vstupte do **Účto skupiny projektů** a poté vyberte související odkaz.  
2. Zvolte akci **Nový**.
3. V okně **Karta účtovacích skupin DM** vyplňte pole podle potřeby.

    > [!NOTE]  
   >   Chcete-li se ujistit, že rozvahové účty pro různé účtování dlouhodobého majetku jsou automaticky vloženy, když zvolíte akci **Vložit protiúčet DM** na řádcích deníku, postupujte podle následujícího kroku na základě účtování zhodnocení.
4. Na pevné záložce **Vyrovnávací účet**, v poli **Protiúčet pole Účet** obsahuje účet hlavní knihy, na který chcete zaúčtovat zůstatkové položky pro zhodnocení.

Pro více informací o používání akce **Vložit protiúčet DM** v řádkách finančního deníku DM navštivte například [Přecenění dlouhodobého majetku](fa-how-revalue.md).

## <a name="to-set-up-fixed-asset-allocation-keys"></a>Nastavení přidělovacích klíčů dlouhodobého majetku
Transakce mohou být přiděleny různým oddělením nebo projektům podle uživatelsky definovaných přidělovacích klíčů. Například byste mohli nastavit přidělovací klíč pro přidělení nákladů na odpisy vozidel s 35% administrativnímu oddělení a 65% prodejnímu oddělení. Pro více informací navštivte [Přidělení nákladů a výnosů](year-allocate-costs-income.md).

Přidělovací klíče platí pro třídy dlouhodobého majetku, nikoli pro jednotlivý majetek.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Účto skupiny projektů** a poté vyberte související odkaz.  
2. V okně **Účtovací skupiny DM** vyberte akci **Přidělení** a poté vyberte typ účtování.
3. V okně **Přidělení DM** vyplňte pole podle potřeby.
4. Opakujte kroky 2 a 3 pro každý typ účtování, pro který chcete definovat přidělovací klíče.

## <a name="to-set-up-fixed-asset-journal-templates"></a>Nastavení šablon deníku dlouhodobého majetku
Šablona je předdefinované rozložení pro deník. Šablona obsahuje informace o sledovacích kódech, výkazech a číselných řadách. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).

[!INCLUDE [d365fin](includes/d365fin_md.md)] automaticky vytvoří šablonu deníku DM při prvním otevření okna **Deník dlouhodobého majetku**, ale můžete nastavit další šablony deníku.  

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Šablony deníku DM** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby.

## <a name="to-set-up-fixed-asset-journal-batches"></a>Nastavení dávek deníku dlouhodobého majetku
Můžete nastavit více dávek deníku, což jsou jednotlivé deníky pro každou šablonu deníku. Zaměstnanci mohou například mít vlastní dávku deníku, která používá iniciály zaměstnanců jako název šablony deníku. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).  

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Šablony deníku DM** a poté vyberte související odkaz.  
2. Vyberte příslušnou šablonu deníku a pak zvolte akci **Dávky**.
3. V okně **Dávky deníku DM** vyplňte pole podle potřeby.

## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Nastavení šablon přeřazení deníku dlouhodobého majetku
Pokud potřebujete převádět, rozdělit nebo kombinovat dlouhodobý majetek, použijte konkrétní deníky přeřazení. [!INCLUDE [d365fin](includes/d365fin_md.md)] automaticky vytvoří šablonu deníku přeřazení DM při prvním otevření okna **Deník přeřazení DM**, ale můžete nastavit další šablony deníku přeřazení. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).  

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Šablony deníku přeřazení DM** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby.

## <a name="to-set-up-fixed-asset-reclassification-journal-batches"></a>Nastavení listů deníku přeřazení dlouhodobého majetku
Můžete nastavit více listů deníku, což jsou jednotlivé deníky pro každou šablonu deníku přeřazení. Zaměstnanci mohou například mít vlastní list deníku přeřazení, který používá iniciály zaměstnanců jako název listu deníku přeřazení. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Šablony deníku přeřazení DM** a poté vyberte související odkaz.  
2. Vyberte příslušnou šablonu deníku a pak zvolte akci **Dávky**.
3. V okně **Šablony deníku přeřazení DM** vyplňte pole podle potřeby.

## <a name="to-set-up-fixed-asset-class-codes"></a>Nastavení kódů tříd dlouhodobého majetku
Kódy tříd dlouhodobého majetku můžou být použity k seskupení dlouhodobého majetku, například do hmotného a nehmotného majetku.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Třídy DM** a poté vyberte související odkaz.
2. Zadejte kódy a názvy pro třídy, které chcete vytvořit.

## <a name="to-set-up-fixed-asset-subclass-codes"></a>Nastavení podtřídových kódů dlouhodobého majetku
Používáte podtřídové kódy dlouhodobého majetku k seskupení svého dlouhodobého majetku do kategorií, jako jsou budovy, vozidla, nábytek nebo strojní zařízení.  

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Podtřídy DM** a poté vyberte související odkaz.
2. Zadejte kódy a názvy pro třídy, které chcete vytvořit.

## <a name="to-set-up-fixed-asset-location-codes"></a>Nastavení kódů místa dlouhodobého majetku
Použijete kódy místa dlouhodobého majetku k registraci umístění dlouhodobého majetku, např. Oddělení prodeje, příjem, správa, výroba nebo sklad. Tyto informace jsou užitečné pro účely pojištění a inventáře.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Umístění DM** a poté vyberte související odkaz.
2. Zadejte kódy a názvy pro umístění dlouhodobého majetku, který chcete vytvořit.

## <a name="to-register-opening-entries"></a>Registrace počátečních stavů
Pokud používáte v [!INCLUDE [d365fin](includes/d365fin_md.md)] dlouhodobý majetek poprvé, musíte před nastavením dlouhodobého majetku nastavit oblast aplikace Finance. Jak to uděláte, závisí na tom, zda je dlouhodobý majetek integrován do hlavní knihy.  

 Následující postup se používá, pokud mají být transakce dlouhodobého majetku zaúčtovány do hlavní knihy.  

1. Ujistěte se, že jste dokončili základní nastavení procedury pro dlouhodobý majetek.  
2. Vytvořte kartu dlouhodobého majetku pro každý existující majetek.  
3. Vytvořte knihu odpisů dlouhodobého majetku pro každý účel odpisování (například daňové a účetní výkazy). Pro každou knihu odpisů musíte definovat podmínky, jako je integrace s hlavní knihou.  

    Povolte integraci hlavní knihy podle následujících kroků. Nejprve se ujistěte, že integrace hlavní knihy je zakázána pro všechny knihy odpisů, poté zaúčtujte počáteční stavy a nakonec zapněte integraci hlavní knihy.  
4. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), zadejte **Knihy odpisů** a poté vyberte související odkaz.  
5. Vyberte příslušnou odpisovou knihu. Na kartě **Domů** ve skupině **Správa** vyberte možnost **Upravit** a otevřete okno **Karta odpisové knihy**.
6. V záložce s náhledem **Integrace** se ujistěte, že všechna pole jsou prázdná odstraněním všech značek zaškrtnutí. Pokud máte více než jednu odpisovou knihu, vypněte integraci hlavní knihy pro každou z nich.  
7. V deníku dlouhodobého majetku zadejte následující řádky pro každý majetek:
   * Řádek s pořizovací cenou.
   * Řádek s akumulovaným odpisem do konce předchozího fiskálního roku.
   * Řádek s akumulovaným odpisem od začátku aktuálního fiskálního roku do data, kdy je [!INCLUDE [d365fin](includes/d365fin_md.md)] nastaven tak, aby začal vypočítávat odpisy.

     Pokud máte další počáteční zůstatky, můžete je nyní také zadat, například znehodnocení nebo zhodnocení.  
8. Po zadání a zaúčtování řádků deníku pro každý majetek zapněte integraci hlavní knihy do knih odpisů.

Pokud není dlouhodobý majetek integrován do hlavní knihy, přeskočte kroky 6 a 8.

## <a name="see-also"></a>Viz také
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Dlouhodobý majetek](fa-manage.md)  
[Finance](finance.md)  
[Vítejte v [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
