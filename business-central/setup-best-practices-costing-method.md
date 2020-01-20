---
title: Nastavení osvědčených postupů - Metoda ocenění | Microsoft Docs
description: 'Metoda ocenění na kartě zboží určuje, jaký je tok nákladů zboží a jestli je aktuální hodnota nebo hodnota rozpočtu aktivována a použita v kalkulaci nákladů.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="setup-best-practices-costing-method"></a>Nastavení osvědčených postupů: Metody ocenění
**Metoda ocenění** na kartě zboží určuje, jaký je tok nákladů zboží a jestli je aktuální hodnota nebo hodnota rozpočtu aktivována a použita v kalkulaci nákladů.  

 Nastavení správné Metody ocenění odpovídající typu zboží a podnikatelského prostředí je důležitým aspektem pro zajištění ekonomických zásob.  

 Následující tabulka obsahuje doporučené postupy, jak nastavit vybraná pole **Metod ocenění**. Pro více informací navštivte [Podrobnosti o designu: Metody ocenění](design-details-costing-methods.md).  

|Možnosti nastavení|Osvědčený postup|Komentář|  
|------------------|-------------------|-------------|  
|Metoda FIFO|Použijte, kde je produkt stabilní.<br /><br /> Používejte pro věci s omezenou trvanlivostí, protože nejstarší položky musí být prodané před uplynutím data prodeje.|Jednotková cena položky je skutečná hodnota jakékoliv přijaté položky vybraná podle metody FIFO.<br /><br /> Při oceňování skladu se předpokládá, že první položky umístěné do skladu se prodávají jako první. **Poznámka:**  Když ceny rostou, rozvaha vykazuje vyšší hodnotu. To znamená, že se zvyšuje daňová povinnost, také se ale zlepšují kreditní skóre a schopnost půjčit si hotovost.|  
|Metoda LIFO|Použijte tam, kde jsou úrovně položek na skladu v průběhu času trvale udržovány nebo zvyšovány.|Jednotková cena položky je skutečná hodnota jakékoliv přijaté položky vybrané podle metody FIFO.<br /><br /> Při oceňování skladu se předpokládá, že poslední položky umístěné do skladu se prodávají jako první. **Poznámka:**  Když ceny rostou, hodnota ve výsledovce klesá. To znamená, že se snižuje daňová povinnost, zhoršuje se tím ale schopnost půjčit si hotovost. **Důležité:**  Zakázáno v mnoha státech / regionech, protože se může použít ke snížení zisku.|  
|Průměr|Použijte, kde je produkt nestabilní.<br /><br /> Použije se tam, kde se zásoby hromadí nebo mísí dohromady a nelze je rozlišit, jako jsou například chemikálie.|Jednotková cena položky je přesná cena, za kterou byla konkrétní jednotka přijata.|  
|Specifikum|Použijte při výrobě nebo obchodu snadno identifikovatelných položek s poměrně vysokými jednotkovými náklady.<br /><br /> Použijte pro položky, na které jsou subjektem regulací.<br /><br /> Používá se pro položky se sériovými čísly.|Jednotková cena položky je vypočítaná jako průměrná jednotková cena v každém časovém bodě po nákupu.<br /><br /> Pro oceňování zásob se předpokládá, že všechny zásoby se prodávají současně.|  
|Standardní|Použijte tam, kde je klíčová kontrola nákladů.<br /><br /> Použijte při opakované výrobě k ocenění nákladů na přímý materiál, přímou práci a výrobní režii.<br /><br /> Používejte tam, kde je disciplína a personál pro udržení standardů.|Jednotková cena položky je přednastavena na základě odhadu.<br /><br /> Když se skutečné náklady realizují později, musí být standardní náklady upraveny na skutečné náklady prostřednictvím odchylky hodnot.|  

## <a name="see-also"></a>Viz také  
 [Podrobnosti návrhu: Metody ocenění](design-details-costing-methods.md)   
 [Podrobnosti návrhu: Zásoby a ocenění](design-details-inventory-costing.md)   
 [Osvědčené postupy při nastavení komplexních oblasti aplikace](set-up-complex-application-areas-using-best-practices.md)  
 [Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
