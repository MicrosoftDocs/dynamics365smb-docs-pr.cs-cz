---
title: WIP Methods for Calculating and Recording Job Progress| Microsoft Docs
description: Describes the different work in process (WIP) methods you can use to post, monitor, and calculate financial information for ongoing jobs that are in progress.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 10/01/2019
ms.author: sgroespe

---
# Metody nedokončené výroby
[!INCLUDE[d365fin](includes/d365fin_md.md)]  podporuje následující metody výpočtu a zaznamenávání hodnoty nedokončené práce.

| Metoda nedokončené výroby | Vzorec výpočtu | Popis výpočtu |
| --- | --- | --- |
| Hodnota nákladů | Uznané výnosy = Fakturovatelné (fakturovaná cena)<br /><br /> Odhadované celkové náklady = Fakturovatelné (celková cena) x poměr rozpočtových nákladů<br /><br /> Náklady nedokončené výroby = (Procento dokončení - Fakturováno %) x Odhadované celkové náklady<br /><br /> Procento dokončení = Celkové náklady na využití / Celkové náklady rozpočtu<br /> Fakturováno % = Vyfakturovatelná fakturovaná cena<br /><br /> Vyfakturovatelná cena celkových uznaných nákladů = Použití (náklady celkem) - Nedokončená výroba | Výpočty hodnoty nákladů začínají výpočtem hodnoty toho, co bylo poskytnuto, tak, že se vezme část odhadovaných celkových nákladů na základě procenta dokončení. Fakturované náklady se odečtou tak, že se vezme část odhadovaných celkových nákladů na základě fakturovaného procenta.<br /><br /> Tento výpočet vyžaduje, aby byla pro celý projekt správně zadána fakturovatelná celková cena, celková cena rozpočtu a celkové náklady rozpočtu. |
| Náklady na prodej | Uznané výnosy = Fakturovatelné (fakturovaná cena)<br /><br /> Uznané náklady = Rozpočet (celkové náklady) x Fakturované procento<br /><br /> Fakturováno % = Fakturovatelné (fakturovaná cena) / Fakturovatelné (celková cena)<br /><br /> (Fakturováno % existuje jako sloupec na řádcích úloh projektu)<br /><br /> Náklady NV = Použití (náklady celkem) – Uznané náklady | Výpočty nákladů na prodej začínají výpočtem uznaných nákladů. Náklady jsou vykázány proporcionálně na základě celkových rozpočtových nákladů.<br /><br /> Tento výpočet vyžaduje, abyste fakturovatelné celkové ceny a celkové náklady rozpočtu zadali pro celý projekt správně. |
| Hodnota prodeje | Uznané náklady = Použití (náklady celkem)<br /><br /> Uznané výnosy = Použití (celková cena) x Očekáváný fakturační poměr<br /><br /> Úhrada nákladů % = Fakturovatelné (celková cena) / Celková cena rozpočtu<br /><br /> Výnosy NV = Uznaný prodej - Fakturovatelné (fakturovaná cena) | Výpočty hodnoty prodeje uznávají výnosy proporcionálně na základě celkových nákladů na využití a očekávaného poměru návratnosti nákladů.<br /><br /> Tato kalkulace vyžaduje, aby fakturovatelná celková cena a celková cena rozpočtu byly správně zadány pro celý projekt. |
| Procento dokončení | Uznané náklady = Použití (náklady celkem)<br /><br /> Uznané výnosy = Použití (celková cena) x Procento dokončení<br /><br /> Procento dokončení = Použití (náklady celkem) / Rozpočet (celkové náklady)<br /> (Označené jako "Dokončeno % nákladů" na řádku úlohy)<br /><br /> Výnosy NV = Deaktivované výnosy - Fakturovatelné (fakturovaná cena) | Výpočty procenta dokončení uznávají výnosy úměrně na základě procenta dokončení, tj. Použití (náklady celkem) vs. Rozpočtové náklady.<br /><br /> Tento výpočet vyžaduje, aby fakturovatelná celková cena a celkové náklady rozpočtu byly správně zadány do celý projekt. |
| Dokončená smlouva | Částka nedokončené výroby = Částka nákladů NV = Použití (náklady celkem)<br /><br /> Částka prodeje NV = Fakturovatelné (fakturovaná cena) | Uzavřená smlouva neuznává výnosy a náklady, dokud není práce dokončena. Toto možná budete chtít udělat, když bude vysoká nejistota kolem odhadů nákladů a příjmů pro projekt.<br /><br /> Veškerá spotřeba je účtována na účet nákladů NV (aktiva) a všechny fakturované prodeje jsou zaúčtovány na účet fakturovaného prodeje NV (pasiva), dokud není projekt dokončen. |

## Viz také
[Správa projektů](projects-manage-projects.md)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
