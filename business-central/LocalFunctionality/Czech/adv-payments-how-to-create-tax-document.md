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

# Vytvoření daňového dokladu k zálohové faktuře

## Automatické účtování DPH ze zálohové faktury 

Pokud je v hlavičce prodejní zálohy pole **Automaticky účtovat doklad DPH** hodnotu **ANO**, při zaúčtování úhrady prodejní zálohy se automaticky vytvoří i zálohový daňový doklad a položka DPH.

Do historie zálohy je zapsána položka **Platba DPH**, ve které je vyplněn základ a částka DPH.

### Tisk DPH dokladu k zálohové faktuře
Pro tisk DPH dokladu k zálohové faktuře postupujte následujícím způsobem:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní zálohové faktury** a poté vyberte související odkaz. 
2. Na přehledu prodejních zálohových faktur označte řádek s požadovanou zálohou.
3. Zvolte funkci **Položky zálohy** v sekci **Historie**. Kurzorem označte řádek s typem položky **Platba DPH**. Dále použijte v sekci Sestavy funkci **Daňový doklad**, pomocí které můžete vytisknout zálohový daňový doklad s rozpisem DPH.

- Pokud je na záloze použito více sazeb DPH, vznikne pro každou sazbu samostatná položka **Platba DPH**. Pokud byla u takto nastavené zálohy uhrazena pouze její část, položky **Platba DPH** vzniknou v poměrné výši.
- Při úhradě zálohy v plném rozsahu se pole **Stav zálohy** změní na hodnotu **K použití**. Při částečné úhradě zůstává hodnota v poli stav zálohy **K úhradě**. Zálohu je možné čerpat do faktury do výše uhrazené částky, tedy i v případě, že ještě nebyla celá doplacena.
- Daňový doklad k záloze je proúčtován s číslem dokladu podle číselné řady nastavené v šabloně záloh v poli pro číselnou řadu zálohového daňového dokladu.

## Ruční zaúčtování DPH dokladu 
Pokud je v hlavičce prodejní zálohy pole **Automaticky účtovat doklad DPH** hodnotu **NE**, při účtování úhrady prodejní zálohy se automaticky zálohový daňový doklad nevytvoří. Záloha může být i takto použita v konečné prodejní faktuře. 

Pokud ale chcete DPH doklad k úhradě dodatečně zaúčtovat, je možné spustit vytvoření a proúčtování zálohového daňového dokladu z historie z **Položek zálohy**. 

### Ruční vytvoření DPH dokladu
Pro ruční vytvoření DPH dokladu postupujte následujícím způsobem:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní zálohové faktury** a poté vyberte související odkaz. 
2. Na přehledu prodejních zálohových faktur označte řádek s požadovanou zálohou.
3. Zvolte funkci **Položky zálohy** v sekci **Historie**. Kurzorem označte řádek s typem položky **Platba DPH**.
4. Z pásu akcí spusťe akci **Účtovat daňový doklad**. Položka zálohy **Platba DPH** (a související položka DPH a věcné položky) se vytvoří se stejným zúčtovacím datem jako proúčtovaná platba.

- Pokud je zálohové faktuře hodnota v poli **Automaticky účtovat doklad DPH** hodnota **NE** i při účtování faktury spojené s touto zálohou, nedojde k automatickému oddanění zálohy a bude třeba provést oddanění dodatečně ručně. Hodnotu v poli je možné před účtováním faktury dodatečně upravit - pokud nastavíte **Automaticky účtovat doklad DPH** na hodnotu **ANO**, při účtování faktury dojde i k oddanění zálohy.
- Pokud při účtování konečné faktury byla záloha použita, ale nedošlo k jejímu oddanění, je možné provést oddanění dodatečně ručně. 

### Ruční odpočet DPH ze zálohy 
Pro ruční odpočet DPH ze zálohy postupujte následujícím způsobem:
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní zálohové faktury** a poté vyberte související odkaz. 
2. Na přehledu prodejních zálohových faktur označte řádek s požadovanou zálohou.
3. Zvolte funkci **Položky zálohy** v sekci **Historie**. Kurzor umístěte na položku typu **Použití** a zvolte z akci **Účtovat použití DPH**. Tímto dojde k oddanění zálohy s datem a číslem dokladu zaúčtované faktury. 


## Viz také

[Zálohové platby pro Česko (rozšíření)](ui-extensions-advance-payments-localization-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
[Finance](../../finance.md)
