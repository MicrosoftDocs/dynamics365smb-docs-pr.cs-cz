---
    title: Service Order Status and Repair Status
    description: The Status field in the Service Order page and the service item repair status, which is represented by the Repair Status Code field in the Service Order page have a certain relationship in Service Management. The service order status reflects the repair status of all the service items in the service order.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/15/2020
    ms.author: edupont

---
# Stav servisní zakázky a Stav opravy
Pole **Stav** na stránce **Servisní zákazky** a stav opravy předmětu sevisu, který je reprezentován polem **Kód stavu opravy** na stránce **Servisní zakázky** spojuje ve správě servisu vzájemný vztah. Stav servisní zakázky odráží stav opravy všech předmětů sevisu v servisní zakázce.

> [!NOTE]  
> Tato dvě stavová pole nesouvisí s polem **Stav Vydáno** v záhlaví servisní zakázky, které určuje, jak sklad zachází s předměty servisu.

Pokaždé, když se stav opravy předmětu sevisu v servisní zakázce změní, stav zakázky se aktualizuje. Chcete-li zobrazit stav, který odráží celkový stav opravy jednotlivých předmětů servisu, musíte zadat následující:

* Stav servisní zakázky, se kterým je spojen každý stav opravy. Více informací viz Stav servisní zakázky.
* Úroveň priority každé možnosti stavu servisní zakázky. Více informací viz Priorita.

Když převedete nabídku servisu na servisní zakázku, stav opravy každého předmětu servisu se v zakázce změní  na **Počáteční** a stav servisní zakázky se změní na **Čekající**.

## Specifikace stavu servisní zakázky a stavu opravy
Každý stav opravy je spojen s konkrétním stavem servisní zakázky. Možnosti stavu servisní zakázky jsou následující: **Čekající**, **Zpracovává se**, **Vyčkat** a **Dokončeno**. Možnosti stavu opravy jsou následující: **Počáteční**, **Servis probíhá**, **Odesláno**, **Částečný servis**, **Cenová nabídka dokončena**, **Čekání na zákazníka**, **Náhr. díl objednán**, **Náhr. díl přijat** a **Servis byl dokončen**.

### Čekající
Stav servisní zakázky **Čekající** naznačuje, že servis může být zahájen nebo pokračovat kdykoli. Proto lze propojit možnosti stavu opravy **Počáteční**, **Odesláno**, **Částečný servis** a **Náhr. díl přijat** k tomuto stavu servisní zakázky.

### Zpracovává se
Stav servisní zakázky **Zpracovává se** označuje, že servis probíhá. Proto mohou být možnosti stavu opravy **Servis probíhá** a **Náhr. díl objednán** propojeny s tímto stavem servisní zakázky. Pokud propojíte stav **Náhr. díl objednán** se stavem servisní zakázky **Zpracovává se**, musíte k této servisní zakázce také připojit stav **Náhr. díl přijat**.

### Vyčkat
Stav servisní zakázky **Vyčkat** označuje, že servis je dočasně pozastavený, protože čekáte na odpověď zákazníka nebo náhradní díly, než bude možné servis zahájit. Možnosti stavu oprav **Cenová nabídka dokončena**, **Náhr. díl objednán** a **Čekání na zákazníka** proto mohou být propojeny s tímto stavem servisní zakázky.

### Dokončeno
Stav servisní zakázky **Dokončeno** označuje, že servis byl dokončen. Proto je stav opravy **Dokončeno** propojen s tímto stavem.

## Přiřazení priority stavu servisní zakázky
Když se změní stav opravy předmětu servisu, jsou identifikovány možnosti stavu servisní zakázky spojené s různými možnostmi stavu opravy všech předmětů servisu v zakázce. Pokud jsou předměty servisu propojeny se dvěma nebo více možnostmi stavu servisní zakázky, je vybrána možnost stavu servisní zakázky s nejvyšší prioritou.

Musíte se rozhodnout, který stav servisní zakázky obsahuje nejdůležitější informace o stavu servisní zakázky, a přiřadit tomuto stavu nejvyšší prioritu,  apod.

### Příklad
Typické přiřazení úrovně priority může být následující:

* Zpracovává se - Vysoká
* Čekající - Středně vysoká
* Vyčkat - Středně nízká
* Dokončeno - Nízká

Například pokud má jeden předmět servisu stav opravy **Počáteční**, spojený se stavem servisní zakázky **Čekající**, další má stav opravy **Servis probíhá**, propojen se stavem servisní zakázky **Zpracovává se** a třetí má stav opravy **Náhr. díl objednán**, spojený se stavem servisní zakázky **Vyčkat**, výsledný stav servisní zakázky bude **Zpracovává se**, protože má nejvyšší prioritu.

## Viz také
[Nastavení stavu Servisních zakázek a Oprav](service-order-repair-status.md)  
[Nastavení Správy servisu](service-setup-service.md)
