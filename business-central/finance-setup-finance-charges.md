---
title: Set Up Finance Charge Terms
description: Learn how to set up Business Central so that you can inform customers of added charges by sending finance charge memos.
author: edupont04


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.search.form: 6, 494
ms.date: 04/01/2021
ms.author: edupont

---
# Nastavení podmínek penále

Když zákazník nezaplatí do data splatnosti, můžete si nechat automaticky vypočítat penále a přidat je k částkám po splatnosti na účtu zákazníka. Zákazníky můžete informovat o přidaných penále zasláním oznámení o penále. Nejprve však musíte nastavit kód, který představuje každý výpočet penále. Poté můžete tento kód zadat do pole Kód podmínky penále na kartách zákazníků.

## Podmínky penále

Musíte nastavit podmínky penále pro každý výpočet penále a poté přiřadit podmínky zákazníkovi v poli **Kód podmínky penále** na stránce **Zákazník**.

Penále lze vypočítat pomocí metod průměrného denního zůstatku nebo splatného salda.

* Průměrný denní zůstatek

   Zohledňuje se počet dní, po které je platba po splatnosti:  
   *Metoda průměrného denního zůstatku* – *Penále* = *Částka po splatnosti* x *(Dny po splatnosti / Úrokové období)* x *(Úroková sazba/100)*

* Splatný zůstatek

   Penále je procentem z dlužné částky:  
   *Metoda splatného salda* – *Penále* = *Částka po splatnosti* x *(úroková sazba / 100)*

Kromě toho je každý termín v tabulce Podmínky Penále propojen s podtabulkou, tabulkou Text Penále. Pro každou sadu podmínek penále můžete definovat počáteční a/nebo koncový text, který se má zahrnout do poznámky o penále.

### Nastavte Podmínky Penále

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Podmínky penále** a vyberte související odkaz.
2. Vyplňte pole podle potřeby.
3. Chcete-li použít více než jednu kombinaci podmínek penále, nastavte kód pro každou z nich.

   Pro každé období penále můžete zadat jednotlivé podmínky, které mohou zahrnovat další poplatky v LM i v cizí měně. Můžete definovat další poplatky v cizích měnách pro každý termín na stránce **Podmínky penále**.
4. Vyberte akci **Měny**.
5. Na stránce **Měny pro Podmínky penále**, definujte pro každý termín kód měny a dodatečný poplatek.

   > [!NOTE]  
   > Když vytvoříte penále v cizí měně, podmínky v cizí měně, které zde nastavíte, se použijí k vytvoření oznámení o penále. Pokud nejsou nastaveny žádné podmínky penále v cizí měně, použijí se podmínky penále LM uvedené na stránce **Podmínky penále** a poté se převedou na příslušnou měnu.

   Pro každou podmínku penále můžete zadat text, který bude vytištěn před (**Počáteční text**) nebo za (**Konečný text**) na záznamech ve zprávě o penále.
6. Vyberte akce **Počáteční text** nebo **Koncový text** a vyplňte na stránce **Text penále**.
7. Chcete-li automaticky vložit související hodnoty do výsledného textu penále, zadejte do pole **Text** následující zástupné symboly.

| Zástupný symbol | Hodnota |
|-----------------|-----------|  
| %1 | Obsah pole **Datum dokladu** v záhlaví poznámky o penále |
| %2 | Obsah pole **Datum splatnosti** v záhlaví oznámení o penále |
| %3 | Obsah pole **Úroková sazba** v souvisejících podmínkách penále |
| %4 | Obsah pole **Zbývající částka** v záhlaví poznámky o penále |
| %5 | Obsah pole **Částka úroku** v záhlaví zprávy o penále |
| %6 | Obsah pole **Dodatečný poplatek** v záhlaví poznámky o penále |
| %7 | Celková částka upomínky |
| %8 | Obsah pole **Kód měny** v záhlaví poznámky o penále |
| %9 | Obsah pole **Datum zaúčtování** v záhlaví poznámky o penále |

## Viz také

[Inkaso nevyrovnaných zůstatků](receivables-collect-outstanding-balances.md)    
[Nastavit podmínky a úrovně připomenutí](finance-setup-reminders.md)    
[Nastavení financí](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]