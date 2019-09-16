---
title: Nastavení Pracovní doby a Servisních hodin | Microsoft Docs
description: 'Můžete určit obvyklou pracovní dobu ve vaší společnosti. Tyto servisní hodiny se používají k výpočtu data a času odezvy u servisních zakázek a nabídek, a k odeslání varování o času odezvy.'
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
# <a name="set-up-work-hours-and-service-hours"></a>Nastavení Pracovní doby a Servisních hodin
Systém správy servisu obvykle sleduje hodiny zdrojů a stav servisní zakázky, aby předpovídal pracovní zatížení a potřeby servisu. [!INCLUDE[d365fin](includes/d365fin_md.md)] má vestavěné nástroje, které můžete přizpůsobit pro zaznamenávání tohoto druhu informací.  
  
Po nastavení výchozích servisních hodin vaší společnosti můžete vypočítat čas odezvy u servisních zakázek, nebo poslat varování nebo upozornění, když se objeví servisní volání. Funkce upozornění je implementována společně s plánovačem úloh.   
  
Při práci na servisní zakázce budete chtít aktualizovat její stav, abyste mohli sledovat pokrok. Stav servisní objednávky odráží stav opravy všech předmětů servisu v servisní zakázce. Pro více informací navštivte sekci [Porozumění stavu servisní zakázky a stavu opravy](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours"></a>Nastavení výchozích servisních hodin  
Použijte stránku **Výchozí servisní hodiny** pro nastavení obvyklé pracovní doby ve vaší společnosti. Tyto servisní hodiny se používají k výpočtu data a času odezvy u servisních zakázek a nabídek, a k odeslání varování o času odezvy. Výchozí servisní hodiny se používají pro servisní smlouvy, pokud pro smlouvu nestanovíte zvláštní servisní hodiny.  
  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výchozí servisní hodiny** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Pokud ponecháte řádky na stránce **Výchozí servisní hodiny** prázdné, výchozí hodnota je 24 hodin; toto platí pouze pro kalendářní pracovní dny.  
  
## <a name="to-set-up-work-hour-templates"></a>Nastavení šablon pracovní doby
Na stránce **Šablona pracovní doby** můžete nastavit šablony, které obsahují typickou pracovní dobu ve vaší společnosti. Můžete například vytvořit šablony pro techniky na plný úvazek a pro techniky na částečný úvazek. Šablony pracovní doby můžete použít, když přidáte kapacitu ke zdrojům.  
  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony pracovní doby ** a poté vyberte související odkaz.  
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Po zadání pracovních hodin pro každý den se automaticky vypočítá hodnota v poli **Celkem za týden**.  

## <a name="to-set-up-contract-specific-service-hours"></a>Nastavení servisních hodin specifických pro smlouvu  
Na stránce **Servisní hodiny** můžete nastavit konkrétní servisní hodiny pro zákazníka, který vlastní servisní smlouvu. Servisní hodiny se používají k výpočtu data a času odezvy u servisních zakázek a nabídek, které patří do servisní smlouvy.  
  
Pokud pro servisní smlouvu nestanovíte konkrétní servisní hodiny, použijí se výchozí servisní hodiny pro servisní smlouvy.  
  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Servisní smlouvy** a poté vyberte související odkaz.  
2. Otevřete servisní smlouvu, pro kterou chcete nastavit konkrétní servisní hodiny, a zvolte **Servisní hodiny**.  
4. Chcete-li nastavit servisní hodiny na základě výchozích servisních hodin, vyberte akci **Kopírovat výchozí servisní hodiny**.  
5. Upravte pole v položkách servisních hodin. Vložením nebo odstraněním položek nastavíte servisní hodiny smlouvy. Všimněte si, že pro každý řádek jsou vyžadována pole **Den**, **Čas zahájení** a **Čas ukončení**.  
6. Pokud chcete, aby servisní hodiny byly platné od určitého data, vyplňte pole **Datum zahájení**.  
7. Pokud chcete, aby servisní hodiny byly platné o svátcích, zaškrtněte políčko v poli **Platí během volna**.  

## <a name="see-also"></a>Viz také  
[Porozumění Stavu přidělení a Stavu opravy](service-allocation-status-and-repair-status.md)  
[Nastavení Správce servisu](service-setup-service.md)  
[Porozumění Servisní zakázce a Stavu opravy](service-order-repair-status.md)  
