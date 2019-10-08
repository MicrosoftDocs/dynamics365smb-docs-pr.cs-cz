---
title: Doporučené postupy pro nastavení globálního plánování | Microsoft Docs
description: '**Plánovací** Záložka v okně **Nastavení výroby** obsahuje několik polí, která definují globální pravidla pro plánovače dodávek.'
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2017
ms.author: sgroespe
---
# <a name="setup-best-practices-global-planning-setup"></a>Nastavení osvědčených postupů: Globalní plánování instalace
**Plánovací** Záložka v okně **Nastavení výroby** obsahuje několik polí, která definují globální pravidla pro plánovače dodávek.  

 Následující tabulka obsahuje doporučené postupy, jak nastavit vybraná pole parametrů globálního plánování. Další informace o poli získáte kliknutím na odkaz ve sloupci **Nastavení pole**.  


|        Nastavení pole        |                                                          Osvědčený postup                                                           |                                                                     Komentář                                                                     |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Použití prognózy na místech |                                       Vyberte, pokud máte prognózy pro konkrétní lokace.                                       |                                                                                                                                                 |
|  Komponenty na lokaci   |                        Pokud zboží není definováno jako SKJ, vyberte kód místa vašeho hlavního skladu.                        |                                          To platí také v případě, že používáte pouze sešity požadavků.                                           |
|   Prázdná úroveň přetečení    |              Pokud migrujete z Microsoft Dynamics NAV 5.0 nebo starší, vyberte **Povolit výchozí kalkulaci**.               |                             Používejte pouze v případě, že chcete všem nebo některým zbožím povolit overflow bodu přiobjednání.                              |
|  Výchozí doba prodlevy  | Nastavte mezi 1D a 5D.<br /><br /> Pokud teprve s [!INCLUDE [d365fin](includes/d365fin_md.md)] začínáme, tak nastavte delší období. | Když jsou uživatelé více sblížení s různými důvody pro hlášení akcí, tak začínají zkracovat dobu utlumení, aby povolili více doporučených změn. |
| Výchozí doba utlumení |                                       Nastavte mezi 5 a 20 procenty velikosti dávky zboží.                                       |                                                                                                                                                 |

## <a name="see-also"></a>Viz také  
 [Nastavení osvědčených postupů: Plánovač dodávek](setup-best-practices-supply-planning.md)   
 [Podrobnosti návrhu: Plánovač dodávek](design-details-supply-planning.md)   
 [Osvědčené postupy při nastavení komplexních oblasti aplikace](set-up-complex-application-areas-using-best-practices.md)  
 [Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
