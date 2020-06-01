---
title: Set Up FA Depreciation| Microsoft Docs
description: You specify in a depreciation book how you want fixed assets to be depreciated or written-down.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 04/01/2020
ms.author: sgroespe

---
# Nastavení odpisování dlouhodobého majetku
Pro přípravu účetní závěrky a přiznání k dani z příjmu můžete použít různé metody odpisů. Mnoho velkých korporací používá ve svých účetních závěrkách lineární odpisy, protože to obecně umožňuje vykazovat vyšší zisky. Pro účely daně z příjmu však mnoho podniků používá metodu zrychleného odpisování, jako je odpis s klesajícím zůstatkem. Metodu odpisování majetku nastavíte v poli **Metoda odpisu** na stránce **Karta dlouhodobého majetku**. Další informace o různých metodách odepisování naleznete v [Metododách odpisu](fa-depreciation-methods.md).

V knihách odpisů definujete různé způsoby, jak musí být odpisy kalkulovány pro váš dlouhodobý majetek. V každé knize můžete zadat jednotlivé podmínky odpisu. Můžete například určit, že v jedné knize se bude dlouhodobý majetek odepisovat po dobu tří a v druhé pěti let.

Po vytvoření příslušných odpisových knih musíte ke každému dlouhodobému majetku přiřadit právě jednu nebo více odpisových knih. Kniha odpisů, která je přiřazena dlouhodobému majetku, se označuje jako Kniha odpisů dlouhodobého majetku. Pro dlouhodobý majetek můžete nastavit neomezený počet knih odpisů.

## Vytvoření knihy odpisů
V knize odpisů dlouhodobého majetku určíte způsob odpisování dlouhodobého majetku. Chcete-li vyhovět různým způsobům odpisování, můžete nastavit několik knih odpisů.

1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Knihy odpisů** související odkaz.
2. Na stránce **Knihy odpisů**, vybrte tlačítko **Nový**.
3. Na stránce **Karta knihy odpisů** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]  
   > Transakce s dlouhobým majetkem můžete evidovat na stránkách **Finanční deníky dlouhodobého majetku** nebo **Deník DM**, v závislosti na tom, zda jsou transakce určeny pro finanční výkazy nebo interní řízení. Dalším krokem definujte, který typ deníku se ve výchozím nastavení používá pro různé aktivity dlouhodobého majetku.
4. V záložce **Integrace**, zaškrtněte políčko pro každou aktivitu dlouhodobého majetku, jejíž transakce chcete účtovat na stránce **Finanční deníky dlouhodobého majetku**.
5. Opakujte kroky 2 až 4 pro každou metodu odpisování nebo metodu účtování, kterou chcete přiřadit dlouhodobému majetku jako odpisovou knihu.

## Přiřazení knihy odpisů k dlouhodobému majetku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Dlouhodobý majetek** a vyberte související odkaz.
2. Vyberte dlouhodobý majetek, pro který chcete nastavit knihu odpisů dlouhodobého majetku.
3. V záložce **Kniha odpisů** vyplňte pole podle potřeby.
4. Pokud potřebujete k dlouhodobému majetku přiřadit více než jednu knihu odpisů, zvolte tlačítko **Přidat další knihy odpisů.**
5. Případně zvolte **Knihy odpisů** a určete jednu nebo více knih odpisů dlouhodobého majetku.

   > [!NOTE]  
   > Pokud používáte metodu ručního odpisování, musíte do deníku deníky dlouhodobého majetku zadávat odpisy ručně. Funkce **Vypočet odpisů** vynechává dlouhodobý majetek, který používá metodu ručního odpisování. Tuto metodu můžete použít pro majetek, který nepodléhá odpisům, například pozemky.

## Přiřazení knihy odpisů k více DM pomocí dávkové úlohy
Pokud chcete přiřadit knihu odpisů k několika dlouhodobým majetkům, můžete použít dávkovou úlohu **Vytvořit knihy odpisů DM** k vytvoření knih odpisů dlouhodobého majetku.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Dlouhodobý majetek** a vyberte související odkaz.
2. Vyberte dlouhodobý majetek, pro který chcete nastavit knihu odpisů, a poté vyberte akci **Upravit**.
3. Na stránce **Karta knihy odpisů** vyberte funkci **Vytvořit knihy odpisů DM**.
4. Na stránce **Vytvořit knihy odpisů DM**, vyplňte pole **Knihy odpisů**.
5. Vyberte pole **Kopie z DM číslo:** a vyberte číslo dlouhodobého majetku, které chcete použít jako základ pro vytváření nových knih odpisů dlouhodobého majetku.

   Pokud toto pole vyplníte, budou pole odpisů v nových knihách odpisů dlouhodobého majetku obsahovat stejné informace jako odpovídající pole v knize odpisů dlouhodobého majetku, ze které kopírujete. Pokud chcete vytvořit nové knihy odpisů dlouhodobého majetku s prázdnými poli odpisů, ponechejte toto pole prázdné.
6. Na záložce **Dlouhodobý majetek**, můžete nastavit filtr pro výběr majetku, pro který chcete vytvořit knihy odpisů dlouhodobého majetku.
7. Vyberte tlačítko **OK**.

## Nastavení typů účtování odpisů
Pro každou knihu odpisů je nutné nastavit požadované nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)] pro zpracování různých typů účtování. Například, zda by účtování mělo být debetní nebo kreditní a zda by typ účtování měl být zahrnut do odpisovatelného základu.

1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Knihy odpisů** související odkaz.
2. Vyberte knihu odpisů, kterou chcete nastavit, a zvolte **Nastavení typu účtování DM**.
3. Na stránce **Nast.typu účtování DM** vyplňte pole podle potřeby.

   > [!NOTE]  
   > Na stránce **Nast.typu účtování DM** nelze vkládat ani mazat řádky. Můžete upravit pouze existující řádky.

Doporučujeme neměnit nastavení pro odpisy u položek, které již byly zaúčtovány. Změny neovlivní položky, které jsou již zaúčtovány, což by učinilo statistiky knihy odpisů zavádějícími.

## Nastavení výchozích šablon a dávek pro odpisy dlouhodobého majetku
Pro každou knihu odpisů definujete výchozí nastavení šablon a dávek. Tato výchozí nastavení použijete k duplikování řádků z jednoho deníku do druhého, k vytváření řádků deníku pomocí dávkových úloh **Výpočet odpisů** nebo **Indexace dlouhodobého majetku**, zdvojení pořizovacích nákladů v deníku pojištění .

1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Knihy odpisů** související odkaz.
2. Vyberte knihu odpisů, pro kterou chcete definovat výchozí deníky, a pak zvolte **Nastavení deníku DM**.
3. Pokud chcete mít výchozí nastavení pro každého uživatele, vyberte pole **ID uživatele** ze stránky **Uživatelé**.
4. V ostatních polích vyberte šablonu deníku nebo list deníku, který musí být použit ve výchozím nastavení.

## Viz také
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Dlouhodobý majetek](fa-manage.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
