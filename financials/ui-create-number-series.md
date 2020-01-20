---
title: Vytváření číselných řad | Microsoft Docs
description: 'Naučte se, jak nastavit číselné řady, které přiřazují jedinečné kódy ID k účtům a dokladům v Business Central.'
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'numbers, numbering'
ms.date: 06/02/2017
ms.author: solsen
---
# <a name="create-number-series"></a>Vytváření číselné řady
Pro každou společnost, kterou jste založili, musíte přiřadit jedinečné identifikační kódy k věcem jako jsou účty hlavní knihy, účty zákazníků a dodavatelů, faktury, a další doklady. Číslování je důležité nejen pro identifikaci. Dobře navržený systém číslování také umožňuje lepší správu a snadnou analýzu společnosti, a může snížit počet chyb, ke kterým dochází při zadávání dat.

> [!NOTE]
>   Doporučujeme používat stejné kódy číselných řad, jaké jsou uvedeny v okně **Přehled číselných řad** v demonstrační společnosti CRONUS. Kódy, jako je *P-INV +*, vám nemusí nyní dávat smysl, ale [!INCLUDE [d365fin](includes/d365fin_md.md)] má řadu výchozích nastavení, která závisí na těchto kódech číselných řad.

Systém číslování vytvoříte nastavením jednoho nebo více kódů pro každý typ hlavních dat nebo dokladu. Můžete například nastavit jeden kód pro číslování zákazníků, jiný kód pro číslování prodejních faktur a jiný kód pro číslování dokladů ve finančních denících. Po nastavení kódu musíte nastavit alespoň jeden řádek číselné řady. Řádek číselné řady obsahuje takové informace, jako jsou první a poslední číslo v řadě a počáteční datum. Pro jeden kód číselné řady lze nastavit více než jeden řádek číselné řady, s odlišným počátečním datem pro každý řádek. Řady se budou používat postupně, zahájením každé série v příslušné počáteční datum.

Obvykle nastavíte svou číselnou řadu tak, aby se nové pořadové číslo automaticky vkládalo na nové karty nebo doklady, které vytvoříte. Můžete ale nastavit řadu čísel tak, abyste mohli nové číslo zadat ručně. Toto lze specifikovat zaškrtnutím políčka **Ruční čísla**.

Pokud chcete použít více než jeden číselný kód řady pro jeden typ hlavních dat - například pokud chcete použít různé číselné řady pro různé kategorie položek - můžete použít vztahy číselných řad.

## <a name="to-create-a-new-number-series"></a>Vytvoření nové číselné řady
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Číselná řada** a pak vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Na novém řádku vyplňte pole dle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

**TIP**: Chcete-li povolit ruční zadávání čísla do nových karet nebo dokladů, zrušte zaškrtnutí políčka **Výchozí čísla** a zaškrtněte políčko **Ruční čísla**.

Když nyní vytvoříte novou kartu nebo doklad, který je nastaven pro použití dané číselné řady, můžete ručně vyplnit pole **Číslo** jakoukoliv hodnotou.  

## <a name="to-set-up-where-a-number-series-is-used"></a>Chcete-li nastavit, kde se používá číselná řada
Následující postup ukazuje, jak nastavit číselné řady pro oblast Prodej. Kroky jsou podobné i pro další oblasti.
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Nastavení prodej a pohledávek** a pak vyberte související odkaz.
2. V okně **Prodej a Pohledávky** v pevné záložce **Číselné řady** vyberte požadovanou číselnou řadu pro každou prodejní kartu nebo doklad.

Vybrané číslo bude nyní použito k vyplnění pole **Číslo** na dotyčné kartě nebo dokladu, podle nastavení provedeného na řádku číselné řady.

## <a name="to-create-relationships-between-number-series"></a>Vytvoření vztahů mezi číselnými řadami
Pokud jste nastavili více než jeden kód číselné řady pro stejný druh základních informací nebo transakcí, můžete vytvořit vztahy mezi těmito kódy. Tato funkce vám může pomoci při rozhodování mezi kódy, pokud používáte číslo.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Číselná řada** a pak vyberte související odkaz.
2. Vyberte řádek s číselnou řadou, pro kterou chcete vytvořit vztah, a pak zvolte **Vztahy**.
3. Do pole **Kód řady** zadejte kód číselné řady, pro kterou chcete vytvořit vztah s řadou vybranou v kroku 2.
4. Přidejte řádek pro každý kód, který chcete spojit s vybranou číselnou řadou.
5. Zavřete okno.

V případě že nyní nastavíte něco, co vyžaduje číslo, můžete použít vztahy, které jste vytvořili, k výběru mezi souvisejícími číselnými řadami.

## <a name="see-also"></a>Viz také
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
