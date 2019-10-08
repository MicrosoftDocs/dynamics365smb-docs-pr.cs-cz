---
title: Přehled nastavení Předmětů servisu a Komponent předmětu servisu | Microsoft Docs
description: 'Naučte se o věcech, které musíte nastavit, než budete moci používat předměty servisu, včetně výchozích hodnot, jako je čas odezvy, procentní sleva smlouvy a cenová skupina servisu.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/01/2017
ms.author: sgroespe
---
# <a name="set-up-service-items-and-service-item-components"></a>Nastavení Předmětů servisu a Komponent předmětu servisu
Chcete-li pracovat s předměty servisu, musíte nastavit následující

* Skupiny předmětu servisu. 
* Volitelné

## <a name="to-set-up-service-item-groups"></a>Nastavení skupin předmětu servisu
Můžete nastavit skupiny zboží, které se týkají opravy a údržby. Můžete definovat výchozí hodnoty pro předměty servisu ve skupině předmětů servisu, jako je čas odezvy, procentní sleva smlouvy a cenová skupina servisu. U zboží ve skupině předmětů servisu můžete vybrat, zda chcete, aby bylo při prodeji automaticky zaregistrováno jako předměty servisu.  
  
Zboží na kartě **Zboží** a předmětům servisu na kartě **Předmět servisu** přiřazujete skupiny předmětů servisu.  
  
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Skupiny předmětu servisu** a pak vyberte související odkaz.  
2. Vytvoření nové skupiny předmětů servisu  
3. Vyplňte pole **Kód** a **Popis**.  
4. Do pole **Výchozí % slevy smlouvy** zadejte výchozí procentuální slevu smlouvy, kterou mají mít předměty servisu ve skupině.  
5. V poli **Výchozí kód Cenové skupiny servisu** zadejte výchozí kód cenové skupiny servisu, který mají mít předměty servisu ve skupině.  
6. V poli **Výchozí doba odezvy (hodiny)** zadejte výchozí dobu odezvy v hodinách, kterou mají mít předměty servisu ve skupině.  
7. Pokud chcete při prodeji zboží ve skupině zaregistrovat jako předměty servisu, vyberte pole **Vytvořit předmět servisu**.  

## <a name="to-set-up-service-item-components"></a>Nastavení komponent předmětu servisu
Předmět servisu se může skládat z několika součástí, které mohou být při opravě nahrazeny náhradními díly. Tyto komponenty jsou nastaveny na stránce **Přehled komponent předmětu servisu**. Navíc, pokud chcete nastavit komponenty pro předměty servisu, které jsou kusovníky, můžete zkopírovat položky kusovníku, a vytvořit je jako komponenty předmětu servisu. 
  
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Předměty servisu** a pak vyberte související odkaz. 
2. Otevřete předmět servisu, pro který chcete nastavit komponenty.  
3. Zvolte akci **Komponenty**. Otevře se okno **Přehled komponent předmětu servisu**.  
4. Přidání nové komponenty  
5. V poli **Typ** zvolte **Předmět servisu**, pokud je samotná komponenta registrovaným předmětem servisu. Jinak zvolte **Zboží**  
6. Do pole **č.** vyberte zboží nebo předmět servisu, který je součástí předmětu servisu.  

## <a name="to-set-up-service-item-components-from-a-bom"></a>Nastavení komponent předmětu servisu z kusovníku
1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Předměty servisu** a pak vyberte související odkaz.  
2. Otevřete předmět servisu, pro který chcete nastavit komponenty z kusovníku.  
3. Zvolte akci **Komponenty**. Otevře se okno **Přehled komponent předmětu servisu**.  
4. Zvolte akci **Kopie z kusovníku**.  
  
    Pokud je zboží, ke kterému je předmět servisu připojen kusovník, komponenty pro veškeré zboží v kusovníku se vytvoří automaticky.  

## <a name="to-set-up-a-service-shelf"></a>Nastavení servisního regálu
Můžete nastavit servisní regály, které určují, kam ukládáte své předměty servisu. Servisní regály přiřadíte předmětům servisu na stránkách **Servisní objednávky** a **Sešit předmětu servisu**.  
  
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Servisní regály** a pak vyberte související odkaz.
2. Vyplňte pole podle potřeby.

## <a name="see-also"></a>Viz také
[Nastavení kódů standardního servisu](service-how-setup-service-coding.md)   
[Nastavení řešení potíží](service-how-setup-troubleshooting.md)