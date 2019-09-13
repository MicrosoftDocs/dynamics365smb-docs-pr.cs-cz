---
title: Nastavení cen a nákladů za Servis | Microsoft Docs
description: 'Naučte se, jak nastavit ceny a další náklady za servis.'
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

# <a name="set-up-pricing-and-additional-costs-for-services"></a>Nastavení cen a dodatečných nákladů za servis
Pomocí funkcí stanovení ceny [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete nastavit a přizpůsobit svou aplikaci tak, abyste mohli aplikovat a upravovat ceny za předměty servisu, servisní opravy a servisní zakázky. Tato cenová rozhodnutí jsou poté snadno předána do fakturačního procesu.  
  
Jak vyžaduje implementace, můžete nastavit cenové skupiny a namapovat je na konkrétní časová období, zákazníky nebo měnu. Můžete nastavit pevné, minimální, nebo maximální ceny, podle toho, jaké servisní smlouvy máte uzavřené se zákazníky. Nakonec, jak upravujete své ceny, můžete si prohlížet a schvalovat změny před jejich odevzdáním do hlavní knihy.  

## <a name="to-set-up-a-service-price-group"></a>Nastavení cenové skupiny servisu
Můžete nastavit skupiny obsahující předměty servisu, které chcete dostávat za stejné speciální ceny servisu. Předmětům servisu na řádcích předmětů servisu přiřazujete cenové skupiny servisu. Skupinám předmětů servisu můžete také přiřadit cenové skupiny servisu.  

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Cenové skupiny servisu** a poté vyberte související odkaz.  
2. Vytvořit novou cenovou skupiny servisu.  
3. Vyplňte pole **Kód** a **Popis**.  
4. Zvolte akci **Nastavení**.  
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Pole **Typ úpravy** a **Částka** společně určují, zda se úprava týká pevné částky, nebo se použije pouze v případě, že celková cena servisu překročí, nebo je nižší než částka v poli **Částka**.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Nastavení skupiny úpravy ceny servisu  
Můžete nastavit skupiny úpravy ceny, pro úpravu cen servisu u předmětů servisu. Můžete například nastavit skupiny úpravy ceny, které upravují cenu přepravného nebo náhradních dílů.  
  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny úprav ceny servisu** a poté vyberte související odkaz.  
2. Vytvoření nové skupiny úpravy ceny servisu  
3. Vyplňte pole **Kód** a **Popis**.  
4. Do pole **Typ** zadejte typ záznamu, který chcete upravit.  
  
    * Chcete-li upravit pouze jeden konkrétní záznam, zadejte číslo tohoto záznamu do pole **Číslo** . Pokud toto pole ponecháte prázdné, vaše skupina úpravy ceny upraví všechny položky typu definovaného v poli **Typ**.  
    * Chcete-li upravit ceny služeb vztahující se pouze k jedné konkrétní službě, vyplňte pole **Typ práce**. Pokud toto pole necháte prázdné, bude to ignorováno.  
  
5. Do pole **Popis** zadejte krátký popis úpravy ceny servisu.  
6. Chcete-li upravit ceny servisu vztahující se pouze na jednu konkrétní obecnou účto skupinu zboží, vyplňte pole **Obecná účto skupina zboží**.

> [!Tip]
> Chcete-li přidat další informace o skupině úprav ceny, můžete vybrat **Podrobnosti**. Můžete například určit, které zboží patří do skupiny úpravy ceny servisu a zda se jedná o zboží, zdroj, skupinu zdrojů nebo poplatek za servis.  

## <a name="to-set-up-additional-costs-for-services"></a>Stanovení dodatečných nákladů za servis
Při práci s předměty servisu a servisními zakázkami budete možná muset zaregistrovat další náklady, například cestovní náklady do konkrétních zón servisu, nebo počáteční poplatky. Když vytvoříte servisní zakázku, můžete vložit tyto náklady, a do objednávky bude přidán řádek  **Náklady**. Alternativně, pokud chcete použít náklady na všechny servisní zakázky, můžete nastavit výchozí náklad. Pokud například chcete vždy použít počáteční poplatek.
  
### <a name="to-set-up-service-costs"></a>Nastavení Servisních nákladů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Náklady na servis** a poté vyberte související odkaz. 
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Nastavení výchozích nákladů na servisní zakázky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení servisu** a poté vyberte související odkaz. 
2. V poli **Počáteční poplatek servisní zakázky** vyberte příslušné servisní náklady.

## <a name="see-also"></a>Viz také
[Nastavení Správce servisu](service-setup-service.md)  
[Správce servisu](service-service.md)  
