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

# Uzavření zálohové faktury  

Pokud nebude zaplacená zálohová faktura čerpána nebo dočerpána, je možné ji uzavřít. Funkce pro uzavření zálohy je dostupná na kartě Prodejní/Náupní zálohové faktury (tedy nikoli z položek historie zálohy), jedná se o funkci **Uzavři zálohu**. 

Pro uzavření zálohy postupujte následujícím způsobem:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní zálohové faktury** a poté vyberte související odkaz. V případě nákupu hledejte **Nákupní zálohové faktury**.
2. Otevřete požadovanou kartu zálohy.
3. V pásu akcí zvolte **Uzavřít zálohu**.
4. Při uzavření můžete v Dialogového okně uzavření zálohy zvolit datum, se kterým bude záloha uzavřena. Při uzavření dojde k vypořádání DPH, pro zálohový daňový dobropis vzniká položka **Uzavření DPH**. Z položky **Uzavření DPH** je možné daňový dobropis vytisknout. Pro položku **Uzavření** i **Uzavření DPH** je použita číselná řada nastavená v šablonách záloh v poli pro číselnou řadu zálohových daňových dobropisů.

Nedočerpaná částka zálohy bude převedena do salda zákazníka ve formě otevřené položky zákazníka.  
Při uzavření zálohy vzniká automaticky záporná Původní položka tak, aby částka zálohy k úhradě byla nulová (počáteční Původní položka mínus platby plus částka uzavření).


## Viz také

[Zálohové platby pro Česko (rozšíření)](ui-extensions-advance-payments-localization-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
[Finance](../../finance.md)
