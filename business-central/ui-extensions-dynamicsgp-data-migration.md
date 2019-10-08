---
title: Migrace dat z Dynamics GP pomocí rozšíření Data Migration | Dokumenty Microsoft
description: 'Pomocí rozšíření Dynamics GP Data Migration můžete migrovat zákazníky, dodavatele, skladové položky, účty hlavní knihy, otevřené závazky a otevřené transakce pohledávek z Dynamics GP do Business Central.'
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'app, add-in, manifest, customize, import, implement'
ms.date: 10/01/2018
ms.author: edupont
---
# <a name="the-dynamics-gp-data-migration-extension"></a>Rozšíření Dynamics GP Data Migration 
Toto rozšíření usnadňuje migraci zákazníků, dodavatelů, skladových položek, účtů hlavní knihy, otevřených závazků a transakcí otevřených pohledávek z Dynamics GP do [!INCLUDE[prodshort](includes/prodshort.md)]. Pokud vaše firma nyní používá aplikaci Dynamics GP, můžete exportovat příslušné záznamy a poté otevřít průvodce asistovaným nastavením pro přidání dat do [!INCLUDE[prodshort](includes/prodshort.md)]. Migrační rozšíření funguje pro všechny podporované verze Microsoft Dynamics GP. Pro více informací navštivte [Importování obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)

## <a name="exporting-data-from-dynamics-gp"></a>Exportování dat z Dynamics GP
Musíte exportovat některé nebo všechny své stávající zákazníky, dodavatele, skladové položky a účty hlavní knihy pomocí funkce exportu dat v Dynamics GP. Při výběru dat pro export lze vybrat následující typy:

* Účet  
* Zákazník  
* Zboží  
* Dodavatel  

Po vytvoření exportního souboru budete mít soubor ZIP, který obsahuje několik souborů txt, které budou určeny tím, co jste vybrali během procesu exportu dat.  Budou také vytvořeny další soubory txt, které obsahují podpůrné informace, potřebné pro nastavení ve vaší nové [!INCLUDE[prodshort](includes/prodshort.md)] společnosti.

Rozšíření Dynamics GP Data Migration automaticky mapuje exportovaná data tak, že vaše data jsou rychle k dispozici ve vaší nové [!INCLUDE[prodshort](includes/prodshort.md)] společnosti.

## <a name="whats-new-in-the-october-2018-release"></a>Co je nového ve vydání Říjen 2018

V této verzi jsme rozšířili množství dat, které přenášíme do [!INCLUDE[prodshort](includes/prodshort.md)] z Dynamics GP.

V průvodci migrací si nyní můžete vybrat, jak chcete migrovat účetní osnovu Dynamics GP. Můžete migrovat existující účetní osnovu nebo můžete vytvořit novou účetní osnovu na základě existující účetní osnovy.  

Pokud se rozhodnete použít stávající účetní osnovu, budou účty nastaveny jako hlavní segment účtu z Dynamics GP a další segmenty budou nastaveny jako dimenze uvnitř [!INCLUDE[prodshort](includes/prodshort.md)].  

Pokud se rozhodnete vytvořit novou účetní osnovu, získáte v průvodci další stránku s informacemi o účtu, která vám umožní stáhnout sešit, provést příslušné změny a poté znovu importovat sešit a změnit své účty.  

Budete si muset stáhnout sešit aplikace Excel a namapovat nové číslo účtu pro každé číslo účtu v tabulce Excel. Každý účet bude muset mít své vlastní číslo, jinak dojde k chybě migrace. Po dokončení mapování můžete pokračovat v průvodci migrací importem sešitu aplikace Excel, který jste právě aktualizovali. Průvodce ověří, že každý řádek má jedinečné číslo účtu a že v žádném řádku není prázdné číslo nového účtu.  

Při změně mapování možností účetní osnovy si také všimněte změny typu dat, která se vyskytují ve finančním deníku pro čísla účtů.  

- Pokud se rozhodnete použít existující čísla účtů, převedeme počáteční zůstatek hlavního segmentu (nové číslo účtu) jako součet čísla hlavního účtu v době migrace.  
- Pokud se rozhodnete vytvořit nová čísla účtů, přeneseme souhrnné informace za dva fiskální roky , na základě fiskálních období, která jste nastavili v Dynamics GP.

V dřívějších verzích [!INCLUDE[prodshort](includes/prodshort.md)] průvodce migroval souhrnnou transakci zůstatku zákazníka/dodavatele v aplikaci Dynamics GP. Nyní přeneseme podrobné otevřené transakce pro zákazníky a dodavatele v době migrace. Co to znamená ? Pokud má váš zákazník v modulu Pohledávky zaregistrovány 3 neuhrazené transakce, přenese průvodce tyto transakce do [!INCLUDE[prodshort](includes/prodshort.md)] se zbývající částkou jako částku dokladu. Totéž platí pro modul Závazky dodavatele.  

Skladové položky se importují pomocí metody oceňování nákladů, která byla vybrána při spuštění průvodce nastavením společnosti. Servisním položkám se automaticky přiřadí metoda oceňování FIFO. V současné době přenášíme Množství na skladě pro položky v době migrace.  Toto množství se přenese na prázdné místo.  

Poslední možností, kterou vidíte v Průvodci migrací dat pro aplikaci Dynamics GP, je možnost zadat možnost účtování. Toto nastavení určuje, zda chcete automaticky zaúčtovat všechny transakce ve finančních denících jakmile migrace přesune data do [!INCLUDE[prodshort](includes/prodshort.md)], nebo zda chcete transakce zaúčtovat ručně tak, aby všechny transakce seděly v dávkách uvnitř stránky finančního deníku a vy jste si mohli ověřit informace před jejich zveřejněním. Tato možnost je viditelná na stránce Možnosti účetní osnovy.


## <a name="see-also"></a>Viz také
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Přizpůsobení [!INCLUDE[prodshort](includes/prodshort.md)] pomocí rozšíření ](ui-extensions.md)  
