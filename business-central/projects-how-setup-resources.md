---
title: 'Nastavení pořizovacích cen zdrojů, cen a kapacity | Microsoft Docs'
description: 'Chcete-li použít zdroje a usnadnit správu projektů, určete náklady a ceny pro jednotlivé zdroje nebo skupiny zdrojů a nastavte kapacitu zdrojů.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff'
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="set-up-resources"></a>Nastavení zdrojů
Chcete-li správně spravovat činnosti zdrojů, musíte nastavit své zdroje a související náklady a ceny. Pravidla týkající se cen souvisejících s prací, slev a nákladových faktorů jsou stanovena na kartě projektu. Můžete určit náklady a ceny pro jednotlivé zdroje, skupiny zdrojů nebo všechny dostupné zdroje společnosti.

Pokud jsou v projektu použity nebo prodány zdroje, ceny a náklady s nimi spojené se získají z informací, které jste nastavili.

Při vytvoření zdroje zadáte výchozí částku za hodinu. Například, pokud používáte konkrétní stroj na projekt po dobu pěti hodin, tento projekt by se vypočítal na základě částky za hodinu.

## <a name="to-set-up-a-resource"></a>Nastavení zdrojů
Vytvořte kartu pro každý zdroj, který chcete použít v projektech.

1. Vyberte ikonu ![Žárovku, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Zdroje** a poté vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a>Nastavení skupiny zdrojů
V jedné skupině zdrojů můžete kombinovat několik zdrojů. Všechny kapacity a rozpočty skupin zdrojů se sčítají z jednotlivých zdrojů. Je také možné zadat kapacity pro skupiny zdrojů buď nezávisle na kumulovaných hodnotách, nebo k nim navíc.

1. Vyberte ikonu ![Žárovku, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Skupiny zdrojů** a poté vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Vyplňte pole podle potřeby.

## <a name="to-set-capacity-for-a-resource"></a>Nastavení kapacity zdroje
Chcete-li vypočítat, kolik času odvede zdroj  na projektu, musí být kapacita zdroje nejprve nastavena jako dostupný čas za období v pracovním kalendáři. Toho docílíte, když vyplníte řádky plánování projektu, které obsahují daný zdroj. Pro více informací navštivte [Vytváření projektů](projects-how-create-jobs.md).

1. Vyberte ikonu ![Žárovku, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Zdroje** a poté vyberte související odkaz.
2. Otevřete příslušnou kartu zdroje a potom vyberte akci **Kapacita zdroje**.
3. Na stránce **Kapacita zdroje** zadejte v poli **Zobrazit podle** délku období, například **Den**, která se zobrazí ve sloupcích na pevné záložce **Matice kapacity zdroje**.
4. U každého zdroje na řádku zadejte pro každé období ve sloupcích počet hodin, po které je zdroj k dispozici.
5. Chcete-li podrobně zobrazit týdenní kapacitu zdroje v počátečním a konečném datu, vyberte akci **Nastavit kapacitu**.
6. Na stránce **Nastavení kapacity zdroje** vyplňte pole podle potřeby.
7. Vyberte akci **Aktualizovat kapacitu**. Stránka **Kapacita zdroje** je aktualizována o zadanou kapacitu.
8. Zavřete stránku.

## <a name="to-set-up-alternate-resource-costs"></a>Pro nastavení alternativních pořizovacích cen zdrojů
Kromě cen uvedených na kartě zdroje můžete pro každý zdroj nastavit také alternativní ceny. Například, pokud platíte zaměstnanci vyšší hodinovou sazbu za přesčasy, můžete nastavit pořizovací cenu zdroje pro přesčasovou sazbu. Alternativní cena, kterou pro zdroj nastavíte, přepíše cenu na kartě zdroje, když zdroj použijete v deníku zdrojů.

1. Vyberte ikonu ![Žárovku, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Zdroje** a poté vyberte související odkaz.  
2. Vyberte zdroj, pro který chcete nastavit jednu nebo více alternativních nákladů, a poté vyberte akci **Náklady**.  
3. Na stránce **Pořizovací ceny zdrojů** podle potřeby vyplňte pole na řádku.  
4. Opakujte krok 3 pro každou alternativní pořizovací cenu zdroje, kterou chcete nastavit.

**Poznámka**. Chcete-li nastavit pořizovací ceny zdrojů, které se budou vztahovat na všechny zdroje a skupiny zdrojů, otevřete stránku **Pořizovací ceny zdrojů** a vyplňte pole.

## <a name="to-set-up-alternate-resource-prices"></a>Pro nastavení alternativních prodejních cen zdrojů
Kromě ceny uvedené na kartě zdrojů můžete pro každý zdroj nastavit také alternativní ceny. Tyto alternativní ceny mohou být podmíněné. Mohou záviset na tom, zda se zdroj používá při konkrétní úloze nebo typu práce.

1. Vyberte ikonu ![Žárovku, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Zdroje** a poté vyberte související odkaz.
2. Vyberte zdroj, pro který chcete nastavit jednu nebo více alternativních cen, a poté vyberte akci **Ceny**.
3. Na stránce **Prodejní ceny zdrojů** vyplňte podle potřeby pole na řádku.
4. Opakujte krok 3 pro každou alternativní prodejní cenu zdroje, kterou chcete nastavit.

## <a name="see-also"></a>Viz také
[Nastavení správy projektu](projects-setup-projects.md)  
[Správa projektu](projects-manage-projects.md)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)         
[Prodej](sales-manage-sales.md)      
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
