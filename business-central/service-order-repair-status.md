---
title: Nastavení stavů pro Servisní zakázky a Opravy | Microsoft Docs
description: 'Musíte nastavit devět možností stavu opravy, které určují průběh opravy a údržby předmětů servisu v servisních zakázkách.'
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
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Nastavení stavů pro Servisní zakázky a opravy
Musíte nastavit devět možností stavu opravy, které určují průběh opravy a údržby předmětů servisu v servisních zakázkách. Musíte nastavit nejméně devět možností stavu opravy, které identifikují situace nebo kroky provedené při servisu předmětů servisu.  

Můžete nastavit úroveň priority pro možnosti stavu servisní zakázky. Tyto čtyři úrovně jsou Vysoká, Středně vysoká, Středně nízká a Nízká.  

Když změníte stav opravy předmětu servisu v servisní zakázce, stav servisní zakázky se aktualizuje. Stav opravy každého předmětu servisu je spojen se stavem servisní zakázky. Pokud jsou předměty servisu spojeny se dvěma nebo více možnostmi stavu servisní zakázky, je vybrán stav servisní zakázky s nejvyšší prioritou.  

## <a name="to-set-up-a-repair-status"></a>Nastavení stavu opravy  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Stav opravy** a poté vyberte související odkaz.
2. Vytvoření nového stavu opravy  
3. Vyplňte pole **Kód** a **Popis**.  
4. V poli **Stav servisní zakázky** zvolte stav zakázky, ke kterému chcete stav opravy připojit. Pole **Priorita** zobrazuje prioritu vybraného stavu servisní zakázky.  
5. Vyberte stav opravy. Můžete zvolit pouze jeden.  
6. Chcete-li, aby bylo možné zaúčtovat servisní zakázky, včetně předmětů servisu, v tomto stavu opravy, vyberte pole **Účtování povoleno**.  
7. Chcete-li manuálně měnit možnost stavu servisní zakázky na **Příprava**  v servisních zakázkách, včetně předmětů servisu s tímto stavem opravy, zaškrtněte políčko **Povolen stav Příprava**.  
8. Stejným způsobem zaškrtněte políčka **Povolen stav Zpracovává se**, **Povolen stav Dokončeno**, a **Povolen stav Vyčkávat**.
  
## <a name="to-set-up-service-status-priorities"></a>Nastavení priority stavu servisu  
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Stav Servisních zakázek** a poté vyberte související odkaz.  
2. Vyberte stav servisní zakázky, pro kterou chcete nastavit prioritu.  
3. V poli **Priorita** vyberte prioritu, kterou chcete nastavit pro tento stav servisní zakázky. Tento krok opakujte pro každý stav.  

## <a name="see-also"></a>Viz také  
[Stav servisní zakázky a opravy](service-service-order-status-and-repair-status.md)  
[Nastavení Správy servisu](service-setup-service.md)  
