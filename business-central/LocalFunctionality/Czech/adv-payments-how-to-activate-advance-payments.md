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

# Aktivace funkcionality Zálohové platby a upgrade stávajících dat  

Aktivace funkcionality Zálohové platby pro Česko se spouští pomocí **Správy funkcí**. Aktivace probíhá ve 2 krocích - povolení pro uživatele a aktualizace dat. Aktualizací dat dojde k upgrade stávajících položek záloh a související agendy do nových tabulek.  

> [!NOTE]
> Proces aktualizace dat je **nevratný**. Po dokončení aktualizace již nebude k dispozici předchozí verze záloh a nebude možné se k původní verzi záloh vrátit.

Podle toho, zda budou nebo nebudou převedena data, budou v databázi dostupné buď objekty ve verzi "zastaralé" - např. Prodejní zálohy (zastaralé), nebo "nové" - např. Prodejní zálohy.  

![Správa funkcí](Media/AdvP-Activate.png "Správa funkcí")

Pro aktivaci funkcionality Zálohové platby pro Česko použijte následující postup:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Správa funkcí** a poté vyberte související odkaz.
2. Otevře se Vám okno **Správa funkcí**
3. Vyberete řádek pro funkci **Lokalizace zálohových plateb pro českou verzi** a v poli **Povoleno pro** zvolíte Všichni uživatelé.
4. Poté projdete průvodcem aktivace a nastavení aktualizace dat.
5. Jakmile dojde k upgrade dat z předchozí verze záloh, bude hodnota pole **Aktuální stav společnosti** nastavena na Dokončená aktualizace dat. Od tohoto okamžiku můžete používat novou verzi funkcionality Zálohové platby.  

## Viz také

[Zálohové platby pro Česko (rozšíření)](ui-extensions-advance-payments-localization-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
[Finance](../../finance.md)
