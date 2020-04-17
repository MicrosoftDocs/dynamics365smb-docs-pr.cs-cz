---
title: Jak nakonfigurovat společnost pomocí Průvodce RapidStart | Microsoft Docs
description: 'Pomocí průvodce konfigurací služeb RapidStart Services můžete rychle nakonfigurovat novou společnost, kterou jste vytvořili.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 03/06/2018
ms.author: sgroespe
---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Konfigurace společnosti s průvodcem RapidStart
Pomocí průvodce konfigurací služeb RapidStart Services můžete rychle nakonfigurovat novou společnost, kterou jste vytvořili.

V následujícím postupu jste zákazníkovi poskytli konfigurační balíček, který je nainstalován v počítači. Zákazník otevře novou společnost, která neobsahuje žádné zákaznické údaje. Vy nebo zákazník pak postupujete podle pokynů v Průvodci RapidStart Services, které jsou popsány v tomto postupu, abyste poskytli základní informace o společnosti. Průvodce importuje konfigurační balíček a poté tento balíček aplikuje na společnost.  

## <a name="to-configure-a-new-company"></a>Konfigurace nové společnosti  
1. V Centru rolí implementátoru služeb RapidStart Services vyberte akci **Průvodce RapidStart**.  
2. Rozbalte pevnou záložku **Krok 1**, která obsahuje obecné informace o nové společnosti. Do příslušných polí zadejte příslušné informace o nové společnosti. Pole **Název** je povinné. Ostatní pole jsou volitelná.  
3. Rozbalte pevnou záložku **Krok 2**, která obsahuje komunikační a kontaktní informace pro novou společnost. Do příslušných polí zadejte příslušné informace o nové společnosti.
4. Rozbalte pevnou záložku **Krok 3**, která obsahuje bankovní účet a platební údaje pro novou společnost. Do příslušných polí zadejte příslušné informace o nové společnosti.  
5. Rozbalte pevnou záložku **Krok 4**. Zvolte tlačítko **AssistEdit** a vyberte konfigurační balíček, který chcete použít. Zobrazí se název konfiguračního balíčku. Poté můžete provést následující akce v uvedeném pořadí:  

    1. Aplikujte konfiguraci výběrem akce **Použít balíček**. Tím se importuje konfigurační balíček a všechna data databáze balíků se aplikují současně.  

    2. Po použití zkontrolujte konfiguraci. Tato možnost umožňuje zkontrolovat podrobnosti konfigurace a dotazníky poskytnuté partnerem a importovat některá hlavní data, která jsou pro vaši společnost požadována. Zvolte akci **Konfigurační sešit**. Pro více informací navštivte sekci “Vyplnění konfiguračního dotazníku“ v [Shromáždění hodnot nastavení zákazníka](admin-gather-customer-setup-values.md).  

6. Rozbalte pevnou záložku **Krok 5**. Určete, které Centrum rolí má být výchozí pro novou společnost.  

    > [!IMPORTANT]  
    >  Změňte své Centrum rolí až po dokončení konfigurace společnosti. Pokud máte více podrobností o nastavení, které je třeba zvážit a upravit, pokračujte v práci nejprve pomocí konfiguračního sešitu. Poté se vraťte do průvodce a aktualizujte svůj profil Centra rolí nebo vyberte akci **Dokončit instalaci**.

7. Zvolte tlačítko **OK**.  
8. Chcete-li ověřit, zda byly informace o konfiguraci použity pro novou společnost, vyberte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Vyhledat stránku nebo sestavu"), zadejte **Informace o společnosti** a poté vyberte související odkaz.

Okno **Informace o společnosti** obsahuje informace, které jste zadali.   

Nyní jste nakonfigurovali společnost a aplikovali na ni data.  

## <a name="see-also"></a>Viz také  
[Aplikování konfigurace pro nové společnosti](admin-apply-configuration-to-new-companies.md)  
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Správa](admin-setup-and-administration.md)
