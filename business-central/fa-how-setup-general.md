---

title: Nastavení hlavní knihy DM | Microsoft Docs
description: 'Než začnete pracovat s dlouhodobým majetkem, musíte nastavit výchozí finanční účty, účto skupiny, alokační klíče, šablony deníků a listy a kódy tříd.'
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2019
ms.author: edupont

---

# <a name="set-up-general-fixed-assets-information"></a>Nastavení obecných informací o dlouhodobém majetku
Než budete moci spravovat dlouhodobý majetek, musíte nastavit výchozí finanční účty, alokační klíče, šablony deníků a listy pro zaúčtování dlouhodobého majetku a reklasifikaci a klasifikovat dlouhodobý majetek ve třídách, jako je Hmotný a Nehmotný.

## <a name="to-set-up-general-default-values-for-fixed-assets"></a>Nastavení obecných výchozích hodnot pro dlouhodobý majetek
Definujte obecné chování nebo funkčnost dlouhodobého majetku a nastavte číselnou řadu majetku na stránce **Nastavení DM**.


1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení DM** a vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]


## <a name="to-set-up-fixed-asset-posting-groups"></a>Nastavení účto skupin dlouhodobého majetku
Pomocí účto skupin můžete definovat skupiny dlouhodobého majetku. Položky pro tyto účtovací skupiny jsou zaúčtovány na stejných účtech hlavní knihy.


1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Účto skupiny DM** a vyberte související odkaz.
2. Zvolte tlačítko **Nový**.
3. Na stránce **Karta účto skupiny MD** vyplňte pole podle potřeby.


    > [!NOTE]  
    >   Chcete-li se ujistit, že rozvahové účty pro různá účtování dlouhodobého majetku jsou automaticky vloženy, když zvolíte akci **Vložit protiúčet DM** na řádcích deníku, postupujte podle následujícího kroku na základě účtování zhodnocení.
4. Na pevné záložce **Vyrovnávací účet**, v poli **Protiúčet zhodnocení** zvolte účet hlavní knihy, proti kterému chcete zaúčtovat zhodnocení.

Pro více informací o používání akce **Vložit protiúčet DM** v řádcích finančního deníku DM navštivte například [Přecenění dlouhodobého majetku](fa-how-revalue.md).


## Nastavení klíčů přidělení dlouhodobého majetku
Transakce mohou být přiděleny různým oddělením nebo projektům podle uživatelem definovaných alokačních klíčů. Můžete například nastavit alokační klíč pro přidělení odpisových nákladů na automobily s 35% na oddělení správy a 65%  na prodejní oddělení. Pro více informací navštivte [Přidělení nákladů a výnosů](year-allocate-costs-income.md).


Přidělovací klíče platí pro účto skupiny dlouhodobého majetku, nikoli pro jednotlivý majetek.


1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Účto skupiny DM** a vyberte související odkaz.
2. Na stránce **Účto skupiny DM**, vyberte tlačítko **Rozdělení** a zvolte typ účtování.
3. Na stránce **Rozdělení DM** vyplňte pole podle potřeby.
4. Opakujte kroky 2 a 3 pro každý typ účtování, pro který chcete definovat alokační klíče.

## Nastavení šablon deníku dlouhodobého majetku
Šablona je předdefinované rozvržení deníku. Šablona obsahuje informace o trasovacích kódech, sestavách a číselných řadách. Pro další informace se běžte na Práce s demenzemi.


[!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky vytvoří šablonu deníku DM při prvním otevření stránky **Deník dlouhodobého majetku**, ale můžete nastavit další šablony deníku.  


1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Šablony deníků DM** a vyberte související odkaz.
2. Podle potřeby vyplňte pole.


## <a name="to-set-up-fixed-asset-journal-batches"></a>Nastavení listů deníku dlouhodobého majetku
Můžete nastavit více listů deníku, což jsou jednotlivé deníky pro každou šablonu deníku. Zaměstnanci mohou například mít vlastní list  deníku, který používá iniciály zaměstnanců jako název listu šablony deníku. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).  


1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Šablony deníků DM** a vyberte související odkaz.
2. Vyberte příslušnou šablonu deníku a poté vyberte akci **Listy**.
3. Na stránce **Listy deníku DM**, vyplňte pole dle potřeby.


## <a name="to-set-up-fixed-asset-reclassification-journal-templates"></a>Nastavení šablon deníku přeřazení dlouhodobého majetku
Pokud potřebujete převádět, rozdělit nebo kombinovat dlouhodobý majetek, použijte konkrétní deníky přeřazení. [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky vytvoří šablonu deníku přeřazení DM při prvním otevření stránky **Deník přeřazení DM**, ale můžete nastavit další šablony deníku přeřazení. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).  


1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Šablony deníku přeřazení DM**, a vyberte související odkaz..
2. Podle potřeby vyplňte pole.

## Nastavení listů deníku přeřazení dlouhodobého majetku
Můžete nastavit více listů deníku, což jsou jednotlivé deníky pro každou šablonu deníku přeřazení. Zaměstnanci mohou mít například vlastní list deníku přeřazení, který používá iniciály zaměstnance jako název listu deníku přeřazení. Pro další informace se běžte na [Práce deníky](ui-work-general-journals.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Šablony deníku přeřazení DM**, a vyberte související odkaz..
2. Vyberte příslušnou šablonu deníku a poté vyberte akci **Listy**.
3. Na stránce **Deník přeřazení zboží**, vyplňte podle dle potřeby.

## Nastavení kódů tříd dlouhodobého majetku
Kódy tříd dlouhodobého majetku lze použít k seskupení dlouhodobého majetku, například do hmotného a nehmotného majetku.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Třídy DM** a vyberte související odkaz.
2. Zadejte kódy a názvy tříd, které chcete vytvořit.


## <a name="to-set-up-fixed-asset-subclass-codes"></a>Nastavení kódů podtříd dlouhodobého majetku
Používáte kódy podtříd DM k seskupení svého dlouhodobého majetku do kategorií, jako jsou budovy, vozidla, nábytek nebo strojní zařízení.  

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Podtřídy DM** a poté vyberte související odkaz.
2. Zadejte kódy a názvy pro podtřídy, které chcete vytvořit.

## <a name="to-set-up-fixed-asset-location-codes"></a>Nastavení kódů umístění dlouhodobého majetku
Použijete kódy umístění dlouhodobého majetku k registraci umístění dlouhodobého majetku, např. Oddělení prodeje, příjem, správa, výroba nebo sklad. Tyto informace jsou užitečné pro účely pojištění a inventáře.


1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Umístění DM** a vyberte související odkaz.
2. Zadejte kódy a názvy skladových míst dlouhodobého majetku, které chcete vytvořit.

## Evidence vstupních záznamů
Pokud používáte dlouhodobý majetek v [!INCLUDE[d365fin](includes/d365fin_md.md)] poprvé, musíte nastavit oblast aplikace financí před nastavením dlouhodobého majetku. Způsob, jakým je to provést, závisí na tom, zda je dlouhodobý majetek integrován s financemi.

Následující postup se používá, pokud mají být transakce dlouhodobého majetku zaúčtovány do účtů účetní osnovy.

1. Ujistěte se, že jste dokončili základní postupy nastavení dlouhodobého majetku.
2. Vytvořte kartu dlouhodobého majetku pro každý existující majetek.
3. Vytvořte knihu odpisů dlouhodobého majetku pro každý účel odpisu (například daně a finanční výkazy). Pro každou knihu odpisů musíte definovat podmínky, jako je integrace s účty účetní osnovy.

   Povolte integraci účtů účetní osnovy podle následujících kroků. Nejprve se ujistěte, že je integrace účtů účetní osnovy zakázána je pro všechny knihy odpisů, potom zaúčtujte počáteční položky a nakonec zapněte integraci.
4. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Knihy odpisů** související odkaz.
5. Vyberte příslušnou knihu odpisů a pak zvolte **Upravit** k otevření stránky **Karta knihy odpisů**.
6. Na záložce **Integrace** se ujistěte ,že všechna pole jsou prázdná zrušením všech zaškrtávacích políček. Pokud máte více než jednu knihu odpisů, vypněte integraci financí pro každou z nich.
7. Do deníku dlouhodobého majetku zadejte pro každý majetek následující řádky:
   * Řádek s pořizovací cenou.
   * Řádek kumulovaného odpisu do konce předchozího fiskálního roku.
   * Řádek kumulovaného odpisu od začátku aktuálního fiskálního roku do data, které je v [!INCLUDE[d365fin](includes/d365fin_md.md)] nastaveno tak, aby začalo počítat odpisy.

   Pokud máte jiné počáteční zůstatky, můžete je také zadat nyní, například odpis a zhodnocení.
8. Po zadání a zaúčtování řádků deníku pro každý majetek zapněte integraci financí v knihách odpisů.

Pokud dlouhodobý majetek není integrován s financemi, přeskočte krok 6 a 8.

## Viz také
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Dlouhodobý majetek](fa-manage.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
