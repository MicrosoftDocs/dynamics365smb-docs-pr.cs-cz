---
title: Manage Customers Using Dynamics 365 Sales| Microsoft Docs
description: You can use Dynamics 365 Sales from inside Business Central to map data and have seamless integration and synchronization in the lead-to-cash process.
documentationcenter: ''
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 04/01/2020
ms.author: bholtorf
---
# Použití aplikace Dynamics 365 for Sales z aplikace Business Central
Používáte-li Dynamics 365 for Sales pro zapojení zákazníků, můžete provést bezproblémovou integraci do procesu vedoucího k získání hotovosti pomocí [!INCLUDE[d365fin](includes/d365fin_md.md)] pro back-endové aktivity, jako je například zpracování objednávek nebo správa zásob.

Než začnete používat integrační funkce, musí správce systému nastavit připojení a definovat uživatele v [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací navštivte [Integrace s Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Tyto kroky popisují proces integrace online verzí [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Informace o konfiguraci on-premises instalace naleznete v části [Příprava Dynamics 365 for Sales pro integraci on-premises instalace](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Integrace aplikací umožňuje přístup k datům v prodeji z [!INCLUDE[d365fin](includes/d365fin_md.md)] a v některých případech i naopak. Můžete pracovat s daty, která mají obě služby společné, jako jsou zákazníci, kontakty a informace o prodeji, a udržovat data aktuální v obou aplikacích.

Například prodejce v [!INCLUDE[crm_md](includes/crm_md.md)] může při vytváření prodejní objednávky použít ceníky z [!INCLUDE[d365fin](includes/d365fin_md.md)]. Když se přidá položka do řádku prodejní objednávky v [!INCLUDE[crm_md](includes/crm_md.md)] je možné vidět úroveň zásob (dostupnost) zboží z [!INCLUDE[d365fin](includes/d365fin_md.md)].

Naopak procesory objednávek v [!INCLUDE[d365fin](includes/d365fin_md.md)] mohou zpracovávat prodejní objednávky, které jsou automaticky nebo ručně přeneseny z [!INCLUDE[crm_md](includes/crm_md.md)]. Mohou například vytvářet a účtovat řádky prodejních objednávek pro zboží nebo zdroje, které byly zadány v [!INCLUDE[crm_md](includes/crm_md.md)] jako produkty pro zápis. Pro více informací navštivte [Zpracování dat prodejní objednávky](marketing-integrate-dynamicscrm.md).

> [!IMPORTANT]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] je možné integrovat pouze s [!INCLUDE[crm_md](includes/crm_md.md)]. Další aplikace Dynamics 365, které mění standardní workflow nebo datový model v [!INCLUDE[crm_md](includes/crm_md.md)] například Project Service Automation, může přerušit integraci mezi [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)].

## Párování záznamů
Průvodce asistovaným nastavením umožňuje zvolit data, která chcete synchronizovat. Později můžete také nastavit synchronizaci pro určité záznamy. Toto se označuje jako *Párování*. Můžete například spojit konkrétní účet v [!INCLUDE[crm_md](includes/crm_md.md)] s konkrétním zákazníkem v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tato část popisuje, co je třeba vzít v úvahu při párování záznamů.

Například pokud chcete vidět účty v [!INCLUDE[crm_md](includes/crm_md.md)] jako zákazníky v [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte spárovat dva typy záznamů. Chcete-li to provést, na stránce **Zákazníci** v [!INCLUDE[d365fin](includes/d365fin_md.md)] použijte akci **Nastavení párování**. Poté určete, kteří zákazníci [!INCLUDE[d365fin](includes/d365fin_md.md)] se shodují s účty v [!INCLUDE[crm_md](includes/crm_md.md)].

Můžete také vytvořit (a spárovat) účet v [!INCLUDE[crm_md](includes/crm_md.md)] například na základě záznamu zákazníka v [!INCLUDE[d365fin](includes/d365fin_md.md)] použitím **Vytvorění účtu v Dynamics 365 for Sales**, nebo naopak, pomocí **Vytvorění zákazníka v [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

Když nastavíte párování mezi dvěma záznamy, můžete také ručně požádat, aby byl aktuální záznam, například zákazník, okamžitě přepsán údaji o účtu z prodeje (nebo z [!INCLUDE[d365fin](includes/d365fin_md.md)]) pomocí akce **Synchronizovat nyní**. Akce **Synchronizovat nyní** se zeptá, zda má přepsat data prodeje nebo data záznamu v [!INCLUDE[d365fin](includes/d365fin_md.md)].

V některých případech musíte spárovat určité sady dat před jinými sadami dat, jak je uvedeno v následující tabulce.

| Data | Co se nejprve páruje |
|-----|----|
| Zákazníci a účty | Spárování prodejců s uživateli [!INCLUDE[crm_md](includes/crm_md.md)] |
| Zboží a zdroje | Spárování jednotek měření se skupinami jednotek [!INCLUDE[crm_md](includes/crm_md.md)] |
| Ceny zboží a zdrojů | Spárování cenových skupin zákazníků s cenami [!INCLUDE[crm_md](includes/crm_md.md)] prices |

> [!NOTE]
> Pokud vaše ceny nebo zákazníci používají cizí měny, ujistěte se, že spojujete měny s měnami prodejních transakcí.

V [!INCLUDE[crm_md](includes/crm_md.md)] závisí prodejní objednávka na informacích, jako jsou zákazníci, měrné jednotky, měny, cenové skupiny zákazníků a zboží a/nebo zdroje. Pro integraci s prodejními objednávkami musíte spojit zákazníky, měrné jednotky, měny, cenové skupiny zákazníků a zboží nebo zdroje.

## Úplná synchronizace záznamů
Na konci průvodce asistovaným nastavením si můžete vybrat akci **Spustit úplnou synchronizaci** a zahájit synchronizaci všech záznamů [!INCLUDE[d365fin](includes/d365fin_md.md)] se všemi souvisejícími záznamy v [!INCLUDE[crm_md](includes/crm_md.md)]. Na stránce **Kontrola úplné synchronizace Dynamics 365 for Sales** vyberte akci **Start**. Úplná synchronizace může nějakou dobu trvat, ale můžete pokračovat v práci v [!INCLUDE[d365fin](includes/d365fin_md.md)], zatímco běží na pozadí.

Chcete-li zkontrolovat průběh jednotlivých úloh v úplné synchronizaci, zvolte na stránce **Kontrola úplné synchronizace Dynamics 365 for Sales** záznam pro zobrazení podrobností. Chcete-li aktualizovat stav během synchronizace, aktualizujte stránku.

Ze stránky **Nastavení připojení Microsoft Dynamics 365** můžete kdykoli získat podrobnosti o úplné synchronizaci. Zde můžete také otevřít stránku **Mapování tabulky integrace** a zobrazit podrobnosti o tabulkách v [!INCLUDE[d365fin](includes/d365fin_md.md)] a prodej, který musí být synchronizován.

## Zpracování dat prodejní objednávky
Prodejní objednávky, které lidé zadají v [!INCLUDE[crm_md](includes/crm_md.md)] , budou automaticky převedeny na [!INCLUDE[d365fin](includes/d365fin_md.md)], pokud zaškrtnete políčko **Automaticky vytvářet prodejní objednávky** na stránce **Nastavení připojení k Microsoft Dynamics 365**.
Alternativně můžete ručně převést zadané prodejní objednávky z [!INCLUDE[crm_md](includes/crm_md.md)] pomocí akce **Vytvořit v [!INCLUDE[d365fin](includes/d365fin_md.md)]**, která je k dispozici na stránce **Prodejní objednávky - Dynamics 365 for Sales**.
U takových prodejních objednávek se pole **Název** v původní objednávce převede a mapuje do pole **Číslo externího dokumentu** v prodejní objednávce v [!INCLUDE[d365fin](includes/d365fin_md.md)].

To může také fungovat, pokud původní prodejní objednávka obsahuje produkty nezahrnuté do katalogu, což znamená zboží nebo zdroje, které nejsou zaregistrovány v žádné aplikaci. V takovém případě musíte vyplnit pole **Typ produktu nezahrnutého v katalogu** a **Číslo produktu nezahrnutého v katalogu** na stránce **Nastavení prodeje a pohledávek** tak, aby byl prodej neregistrovaných produktů mapován na zadané číslo zboží/zdroje pro finanční analýzu.

Pokud je popis zboží na původní prodejní objednávce dlouhý, vytvoří se další řádek prodejní objednávky typu **Poznámka**, který zachová celý text prodejní objednávky v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Aktualizace polí v hlavičkách prodejních objednávek, například pole Posl.datum dodávky nebo Požadované datum dodávky, které jsou mapovány v Prodejní objednávka-objednávka **Mapování tabulky integrace**, jsou periodicky synchronizovány do [!INCLUDE[crm_md](includes/crm_md.md)]. Procesy, jako je uvolnění prodejní objednávky a odeslání nebo fakturace prodejní objednávky, jsou zaúčtovány na časovou osu prodejní objednávky v [!INCLUDE[crm_md](includes/crm_md.md)]. Pri více informací navštivte [Úvod do informačních kanálů o aktivitách](/dynamics365/sales-enterprise/developer/introduction-activity-feeds). <!--The link is broken. Should this actually point to https://docs.microsoft.com/en-us/dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]
> Periodická synchronizace založená na Prodejní objednávka-objednávka **Mapování tabulky integrace** bude fungovat, pouze pokud je povolena integrace prodejní objednávky. Pro více informací navštivte [Nastavení připojení na stránce Nastavení připojení prodeje](admin-prepare-dynamics-365-for-sales-for-integration.md). Synchronizovány jsou pouze prodejní objednávky vytvořené z odeslaných prodejních objednávek v [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací navštivte [Integrace zpracování prodejních objednávek](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## Zpracování údajů o prodejních nabídkách
Prodejní nabídky, které jsou aktivovány v [!INCLUDE[crm_md](includes/crm_md.md)], budou převedeny na [!INCLUDE[d365fin](includes/d365fin_md.md)], pokud zaškrtnete políčko **Automaticky zpracovat nabídky** na stránce **Nastavení připojení k Microsoft Dynamics 365**.
Případně můžete ručně převést aktivované prodejní nabídky z [!INCLUDE[crm_md](includes/crm_md.md)] pomocí akce **Zpracovat v [!INCLUDE[d365fin](includes/d365fin_md.md)]** na stránce **Prodejní nabídky - Dynamics 365 for Sales**.
Na takových prodejních nabídkách se pole **Název** v původní nabídce převede a mapuje do pole **Číslo externího dokumentu** na prodejní objednávce v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Také pole **Platí do** v nabídce je přeneseno a mapováno do pole **Nabídka platná do data** v prodejní nabídce v  [!INCLUDE[d365fin](includes/d365fin_md.md)].

Prodejní nabídky procházejí mnoha revizemi, zatímco jsou dokončovány. Ruční i automatické zpracování prodejních nabídek v [!INCLUDE[d365fin](includes/d365fin_md.md)] zajišťuje, že předchozí verze prodejních nabídek jsou archivovány před zpracováním nových revizí prodejních nabídek z [!INCLUDE[crm_md](includes/crm_md.md)].

## Zpracování zaúčtovaných prodejních faktur, plateb zákazníkům a statistiky
Po splnění prodejní objednávky budou pro ni vytvořeny faktury. Při fakturaci prodejní objednávky můžete převést zaúčtovanou prodejní fakturu do [!INCLUDE[crm_md](includes/crm_md.md)], pokud zašrtnete políčko **Vytvořit fakturu v [!INCLUDE[crm_md](includes/crm_md.md)]** na stránce **Účtovaná prodejní faktura**. Účtované faktury jsou převedeny do [!INCLUDE[crm_md](includes/crm_md.md)] se stavem **Fakturováno**.

Když obdržíte zákaznickou platbu za prodejní fakturu v [!INCLUDE[d365fin](includes/d365fin_md.md)], stav prodejní faktury se změní na **Zaplaceno** s polem **Důvod stavu** nastaveným na **Částečně**, je-li částečně zaplaceno, nebo **Kompletně**, pokud je zcela zaplaceno, když vyberete akci **Aktualizace statistiky účtu** na stránce zákazníka v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Funkce **Aktualizace statistiky účtu** aktualizuje hodnoty, například **Saldo** a **Celkový prodej** v okně s fakty **Statistika účtu [!INCLUDE[d365fin](includes/d365fin_md.md)]** v [!INCLUDE[crm_md](includes/crm_md.md)]. Případně můžete mít naplánované úlohy, statistiky zákazníků a POSTEDSALESINV-INV, které můžete automaticky spustit na pozadí.

## Viz také
[Integrace s Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Řízení vztahů](marketing-relationship-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
[Přiřazení oprávnění uživatelům a skupinám](ui-define-granular-permissions.md)  
[Přehled prodejů a centra prodeje](/dynamics365/customer-engagement/sales-enterprise/overview)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
