---
title: Nastavení přidělení zdrojů | Microsoft Docs
description: 'Naučte se, jak vám systém může pomoci zajistit přiřazení osoby, která má odbornost potřebnou pro poskytování servisu.'
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resource, skill, service, zones'
ms.date: 10/01/2018
ms.author: bholtorf
---

# <a name="set-up-resource-allocation"></a>Nastavení přidělení zdrojů
Aby bylo zajištěno, že servisní úloha bude vykonána dobře, je důležité najít zdroj, který je kvalifikovaný pro požadovanou práci. [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete nastavit tak, aby bylo snadné alokovat někoho, kdo má pro danou práci správnou odbornost. V [!INCLUDE[d365fin](includes/d365fin_md.md)] se toto nazývá _přidělení zdrojů_. Zdroje můžete přidělit na základě jejich odbornosti, dostupnosti nebo toho, zda jsou ve stejné zóně servisu jako zákazník. 

Chcete-li použít přidělení zdrojů, musíte nastavit:  
  
* Odbornost potřebnou k opravě a údržbě předmětů servisu. Přiřadíte ji předmětům servisu a prostředkům.  
* Geografické oblasti zvané zóny, které definujete pro svůj trh. Například Východní, Západní, Centrální a tak dále. Přiřadíte je zákazníkům a prostředkům.  
* Zda se má zobrazovat odbornost a zóny zdrojů a zda se má zobrazit varování, pokud si někdo vybere nekvalifikovaný zdroj, nebo zdroj který není v zákaznické zóně.  

## <a name="to-set-up-skills"></a>Nastavení odbornosti
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Odbornosti**, a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Přiřazení odbornosti předmětům servisu a zdrojům
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Předměty servisu** nebo **Zdroje**, a poté vyberte související odkaz.  
2. Otevřete kartu pro předmět servisu nebo zdroj a poté vyberte jednu z následujících možností:  
  
    * U předmětů servisu zvolte **Odbornosti zdroje**.  
    * U zdroje zvolte **Odbornost**.  

## <a name="to-set-up-zones"></a>Nastavení zón
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zóny**, a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Pro přiřazení zón zákazníkům a zdrojům 
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** nebo **Zdroje**, a poté vyberte související odkaz.  
2. Otevřete kartu pro předmět servisu nebo zdroj a poté vyberte jednu z následujících možností:  
  
    * Pro zákazníky vyberte zónu v poli **Kód zóny servisu**.  
    * Pro zdroje vyberte akci **Zóny servisu**.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Chcete-li určit, co se má zobrazit, když je vybrán zdroj
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení servisu** a poté vyberte související odkaz. 
2. V poli **Volba odbornosti zdroje** vyberte jednu z možností popsaných v následující tabulce.  
  
    |**Možnost**|**Popis**|  
    |------------|-------------|  
    |Zobrazen kód | Zobrazí pouze kód.|  
    |Zobrazeno varování | Zobrazí informace a zobrazí varování, pokud zvolíte zdroj, který není kvalifikovaný.|  
    |Nepoužito | Nezobrazuje tyto informace.|  

## <a name="to-update-resource-capacity"></a>Aktualizace kapacity zdroje  
Možná budete muset změnit kapacitu zdrojů.  
  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kapacita zdroje**, a poté vyberte související odkaz.  
2. Zvolte zdroj a poté zvolte akci **Nastavit kapacitu**.  
3. Proveďte změny a poté zvolte **Aktualizovat kapacitu**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Chcete-li aktualizovat odbornost pro zboží, předměty servisu nebo skupiny předmětů servisu
Pokud chcete změnit kódy odbornosti přiřazené k položkám, například z **PC** na **PCS**, můžete tak učinit buď pro zboží, předmět servisu, nebo pro všechny předměty ve skupině předmětů servisu.  
  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky**, **Předmět servisu**, nebo **Skupiny předmětů servisu**,  a poté vyberte související odkaz.  
2. Vyberte entitu, kterou chcete aktualizovat, a poté vyberte akci **Odbornosti zdroje**.  
3. Na řádku s kódem, který chcete změnit, vyberte v poli **Kód odbornosti** příslušný kód odbornosti.  
4.  Pokud má položka přidružené předměty servisu, otevře se dialogové okno s následujícími dvěma možnostmi:  
  
    * Změňte kódy na vybranou hodnotu: Tuto možnost vyberte, pokud chcete nahradit starý kód odbornosti novým kódem u všech souvisejících servisních předmětů.  
    * Odstraňte kódy odbornosti nebo aktualizujte jejich vztah: Tuto možnost vyberte, pokud chcete změnit kód odbornosti pouze u této položky. Kód odbornosti u souvisejících předmětů servisu bude znovu přiřazen. To znamená, že pole **Přiděleno od** bude aktualizováno.  
  
## <a name="see-also"></a>Viz také
[Přidělení zdrojů](service-how-to-allocate-resources.md)  
[Nastavení Pracovní doby a Servisních hodin](service-how-setup-work-service-hours.md)  
[Nastavení hlášení poruch](service-how-setup-fault-reporting.md)  
[Nastavení kódů standardního servisu](service-how-setup-service-coding.md)  
 

