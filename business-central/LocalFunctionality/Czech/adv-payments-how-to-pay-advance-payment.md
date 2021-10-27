---
title: Advance Payments activation and upgrade
description: This section describes Advance Payments Localization for Czech extension functionality.
author: v-pejano

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Advance Payments, Localization
ms.date: 10/01/2021
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Úhrada zálohové faktury 

Pokud je zálohová faktura ve stavu K úhradě, je možné ji zaplatit, a to pomocí finančního deníku nebo pokladního dokladu.  

## Úhrada zálohové faktury finančním deníkem

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky** a poté vyberte související odkaz.
2. Vyberte šablonu finančního deníku.
2. Pro úhradu zálohové faktury ve finančním deníku vyplňte pole **Typ dokladu = platba**. 
3. Zadejte příslušné **Číslo zákazníka/dodavatele** (podle typu zálohové faktury: nákup/prodej). 
4. V poli **Číslo zálohy** na řádku finančního deníku je dostupný seznam všech neuhrazených nebo částečně neuhrazených záloh. Seznam záloh je filtrován podle kódu měny zvoleném na řádku finančního deníku.   
Vyberte zálohovou fakturu, kterou chcete uhradit, a volbu potvrďte v řádku deníku. Navrženou částku je možné snížit, pokud má být záloha hrazena jen částečně.   
K jednomu řádku finančního deníku je možné připojit pouze jednu zálohu. Platbu více záloh současně je třeba rozdělit na více řádků. 
5. Po zaúčtováním finančního deníku vznikne v položkách zálohy položka s **Typem položky = Platba.**

## Úhrada zálohové faktury pokladním dokladem 
Při úhradě zálohové faktury pokladnou postupuje uživatel obdobným způsobem jako ve finančním deníku. 
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pokladní doklad** a poté vyberte související odkaz.
2. Vytvořte nový pokladní doklad.
3. Zadejte příslušné **Číslo zákazníka/dodavatele** (podle typu zálohové faktury: nákup/prodej). 
4. V poli **Číslo zálohy** na řádku pokladního dokladu je dostupný seznam všech neuhrazených nebo částečně neuhrazených záloh, filtrovaný podle kódu měny pokladny.
Vyberte zálohovou fakturu, kterou chcete uhradit, výběr potvrďte v řádku pokladního dokladu. Navrženou částku je možné snížit, pokud má být záloha hrazena částečně. K jednomu řádku pokladního dokladu je možné připojit pouze jednu zálohu. Platbu více záloh současně je třeba rozdělit na více řádků. 
5. Po zaúčtování pokladního dokladu vznikne v položkách zálohy položka s **Typem položky = Platba**.




## Viz také

[Zálohové platby pro Česko (rozšíření)](ui-extensions-advance-payments-localization-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
[Finance](../../finance.md)
