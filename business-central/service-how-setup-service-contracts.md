---
title: Založení Servisních smluv | Microsoft Docs
description: 'Naučte se, jak nastavit servisní smlouvy'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'service, cost, service order'
ms.date: 10/01/2018
ms.author: sgroespe
---

# <a name="set-up-service-contracts"></a>Založení Servisních smluv
Než budete moci pracovat se smlouvami, musíte nastavit následující: 

* **Skupiny servisních smluv**, které shromažďují servisní smlouvy, které spolu nějakým způsobem souvisejí.
* **Skupiny účtů servisní smlouvy**, které se používají k seskupování účtů servisních smluv pro servisní faktury vytvořené pro servisní smlouvy. Tyto skupiny přiřadíte k servisním smlouvám.  
* **Šablony smluv**, které definují rozvržení smluv obsahujících nejčastěji používané detaily servisní smlouvy. Když vytváříte nabídky servisních smluv, můžete je vytvořit pomocí šablon. Při vytváření nabídky smlouvy pole automaticky obsahují obsah polí šablony.
* **Šablony zákazníků**, které vám umožňují vytvářet nabídky pro smlouvy nebo pro potenciální zákazníky a zároveň nejsou evidování jako zákazníci v [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Nastavení Skupiny servisních smluv  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny servisních smluv** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Zvolte pole **Sleva pouze na zak. ze smlouvy** pokud chcete, aby smluvní nebo servisní slevy byly platné pouze pro objednávky servisní smlouvy, jako je údržba.  

## <a name="to-set-up-a-service-contract-account-group"></a>Nastavení skupin účtů servisní smlouvy  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny účtů servisní smlouvy**, a pak vyberte související odkaz.  
2. Vytvořte novou skupinu účtů servisní smlouvy.   
3. Vyplňte pole **Kód** a **Popis**. Tato pole popisují Skupinu servisních účtů.  
4. Vyplňte pole **Účet smlouvy bez zálohy**, vyberte číslo účtu hlavní knihy pro účet bez zálohy.  
5. V poli **Účet smlouvy se zálohou** vyberte číslo účtu hlavní knihy pro účet se zálohou.  

## <a name="to-set-up-a-contract-template"></a>Nastavení šablony smlouvy  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony servisních smluv** a poté vyberte související odkaz.  
2. Vytvořte novou šablonu servisní smlouvy.  
3. Do pole **Číslo** zadejte číslo šablony smlouvy.  
  
     Alternativně, pokud jste nastavili číselné řady pro šablony smlouvy na stránce **Nastavení Správce servisu**, stisknutím klávesy Enter zadejte další dostupné číslo šablony smlouvy. Vyplňte ostatní pole podle potřeby.  
  
4. Na záložce **Faktura** s náhledem , vyplňte pole **Kód Skupiny účtů servisní smlouvy**, **Období fakturace** a tak dále. Vyplňte ostatní pole podle potřeby.  
5. Zvolte akci **Servisní slevy** pro přidání smluvních slev.  

## <a name="to-set-up-a-customer-template"></a>Nastavení šablony zákazníka  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony zákazníků** a poté vyberte související odkaz.  
2. Vytvořte novou kartu šablony zákazníka  
3. V záložce **Obecné** s náhledem zadejte kód a popis pro šablonu zákazníka do polí **Kód** a **Popis**. 
4. Chcete-li definovat vyhledávací kritéria, vyplňte další pole, například **Kód země/oblasti**, **Kód teritoria** a **Kód jazyka**.  
5. Vyplňte pole **Obecná Obch. účto skupina** a **Účto skupina zákazníka**.  

## <a name="see-also"></a>Viz také
[Nastavení Správy servisu](service-setup-service.md)