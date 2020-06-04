---
title: Nastavení pojištění Dlouhodobého majetku | Microsoft Docs
description: Nastavte kartu pojištění a všeobecné informace o pojistných podmínkách ke správě pojistného krytí dlouhodobého majetku.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'policy, coverage'
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="set-up-fixed-asset-insurance"></a>Nastavení pojištění dlouhodobého majetku
Ke správě pojistného krytí dlouhodobého majetku musíte nejprve nastavit nějaké obecné informace o pojištění a kartu pojištění dle podmínek.

## <a name="to-set-up-general-insurance-information"></a>Pro nastavení obecných informací o pojištění
Pro používání pojišťovacích funkcí v [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte nastavit nějaké obecné informace o pojištění.  

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Nastavení DM** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Nastavení typů pojištění
Pojistné smlouvy můžete seskupit do kategorií, např. pojištění proti krádeži nebo pojištění proti požáru. Typy pojištění jsou používány na kartě pojištění.

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Typy pojištění** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby.

## <a name="to-set-up-insurance-cards"></a>Nastavení karet pojištění
Na kartě pojištění můžete shromažďovat informace o každé pojistné smlouvě.  

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Pojištění** a poté vyberte související odkaz.  
2. Na stránce **Pojištění** zvolte akci **Nový** pro vytvoření nové karty pojištění.  
3. Vyplňte pole podle potřeby.

## <a name="to-set-up-insurance-journal-templates"></a>Nastavení šablon deníku pojištění
[!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky vytvoří šablonu deníku pojištění při prvním otevření stránky **Deník pojištění**, ale můžete nastavit další šablony deníku. Další informace naleznete v části [Práce s Finančním deníkem](ui-work-general-journals.md).  

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Šablony deníku pojištění** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby.

## <a name="to-set-up-insurance-journal-batches"></a>Pro nastavení listů deníku pojištění
Listy můžete nastavit v šabloně deníku pojištění. Hodnoty v listu deníku jsou používány jako výchozí hodnoty, pokud pole na řádcích deníku nejsou vyplněny. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).  

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Šablony deníku pojištění** a poté vyberte související odkaz.  
2. Vyberte šablonu deníku pojištění a pak zvolte akci **Listy**.
3. Na stránce **Listy deníku pojištění** vyplňte pole podle potřeby.

> [!NOTE]  
>   Čísla mají v názvech deníků zvláštní funkci. Pokud název šablony deníku nebo listu deníku obsahuje číslo, toto číslo je automaticky inkrementováno o jedna pokaždé, když je deník zaúčtován. Např. pokud je v poli **Název** zvoleno HH1, název deníku se změní na HH2 potom, co se zaúčtuje deník HH1.

## <a name="see-also"></a>Viz také
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Dlouhodobý majetek](fa-manage.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
