---
title: Migrace dat z Dynamics GP pomocí rozšíření Data Migration | Dokumenty Microsoft
description: 'Pomocí rozšíření Dynamics GP Migration můžete migrovat zákazníky, dodavatele, skladové položky a účty z Dynamics GP do Business Central.'
documentationcenter: ''
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'app, add-in, manifest, customize, import, implement'
ms.date: 03/29/2017
ms.author: edupont
---
# <a name="the-dynamics-gp-data-migration-extension-for-finance-and-operations-business-edition"></a>Rozšíření Dynamics GP Data Migration pro Finance and Operations, Business edition
Toto rozšíření usnadňuje migraci zákazníků, dodavatelů, skladových položek a účtů z aplikace Dynamics GP do [!INCLUDE [d365fin](includes/d365fin_md.md)]. Pokud vaše firma nyní používá aplikaci Dynamics GP, můžete exportovat příslušné hlavní záznamy a poté otevřít průvodce asistovaným nastavením pro přidání dat do [!INCLUDE [d365fin](includes/d365fin_md.md)]. Pro více informací navštivte [Importování obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)

## <a name="exporting-data-from-dynamics-gp"></a>Exportování dat z Dynamics GP
Musíte exportovat některé nebo všechny své stávající zákazníky, dodavatele, skladové položky a účty do souboru pomocí funkce Dynamics GP pro export dat. Pro účely [!INCLUDE [d365fin](includes/d365fin_md.md)] můžete exportovat následující typy dat:

* Účet  
* Zákazník  
* Zboží  
* Dodavatel  

Rozšíření Dynamics GP Data Migration automaticky mapuje exportovaná data tak, že vaše data jsou rychle k dispozici ve vaší nové [!INCLUDE [d365fin](includes/d365fin_md.md)] společnosti. Během procesu se vytvoří podpůrné informace o nastavení, například účto skupiny. Skladové položky budou do systému převedeny pomocí metody FIFO jakožto metody oceňování nákladů. Účty budou nastaveny jako hlavní segment účtu z Dynamics GP s dimenzemi, protože [!INCLUDE [d365fin](includes/d365fin_long_md.md)] nemá segmenty účtu.

## <a name="see-also"></a>Viz také
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] pomocí rozšíření ](ui-extensions.md)  
