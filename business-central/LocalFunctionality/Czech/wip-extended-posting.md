---
title: Czech Local Functionality - WIP Extended Posting 
description: This section describes local functionality - WIP Extended Posting.
author: v-makune

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, WIP, Finance, Extended Posting, Localization, CZ
ms.date: 12/01/2020
ms.reviewer: v-pejano
ms.author: v-pejano
---


# Rozšířené účtování nedokončené výroby
 Tato funkce umožňuje správně provádět účtování výrobní spotřeby, aktivace/deaktivace nedokončené výroby a změny stavu výrobků/polotovarů dle českých účetních postupů. Díky ní je možno nastavit pro kombinace skladové lokace a účto skupiny zboží finanční účty pro spotřebu, změnu stavu nedokončené výroby i změnu stavu polotovarů a výrobků. 

Nový systém účtování je používán u následujících transakcí: 

- Účtování spotřeby v denících spotřeby.
- Účtování nákladů výrobních operací a příjmu výrobků ve výstupních denících. 
- Dokončování výrobních zakázek. 

Účet zaokrouhlení v **Nastavení obecného účtování** umožňuje zaúčtovat všechny náklady ze zaokrouhlení skladových pohybů (položky ocenění s Typ položky=Zaokrouhlení) na jiný finanční účet než je účet adjustace zásob. Pomocí pole **Datum zaokrouhlení** v **Nastavení financí** umožňuje řídit datum zaúčtování položky zaokrouhlení. 


Česká legislativa používá při účtování výrobní operací následující finanční účty: 

- Účet spotřeby.
- Změna stavu nedokončené výroby.
- Změna stavu výrobků. 

## Viz také

[Česká lokální funkcionalita](czech-local-functionality.md)  
