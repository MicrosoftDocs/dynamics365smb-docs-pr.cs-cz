---
title: Insure Fixed Assets| Microsoft Docs
Description: You can assign a fixed asset to an insurance policy, which is represented by an insurance card.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 04/01/2020
ms.author: sgroespe

---
# Pojištění dlouhodobého majetku
Pojistná smlouva pro dlouhodobý majetek je reprezentována kartou pojištění. K jedné pojistné smlouvě můžete přiřadit jednu nebo více položek dlouhodobého majetku.

Dlouhodobý majetek přiřadíte k pojistné smlouvě zaúčtováním do položek pojistného krytí ze strínky **Deník pojištění**.

Kromě toho můžete přiřadit dlouhodobý majetek k pojistné smlouvě a vytvořit položky krytí při zaúčtování jeho nákladů na pořízení. To uděláte tak, že zaúčtujete náklady na pořízení z deníku dlouhodobého majetku s vyplněným polem **Číslo pojištění**. Na stránce **Nastavení DM** musí být zaškrtnuto políčko **Automatické účtování pojištění**. Pro více informací navštivte [Ruční zaúčtování pořízení dlouhodobého majetku pomocí finančního deníku dlouhodobého majetku](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

Pokud není zaškrtnuto políčko **Automatické účtování pojištění** na stránce **Nastavení DM** vytvoří funkce účtování pořízení z deníku dlouhodobého majetku řádky na stránce **Deník pojištění**, které musíte zaúčtovat ručně.

> [!WARNING]
> Pokud nezvolíte zaškrtávací políčko **Automatické účtování pojištění** na stránce **Nastavení DM**, pak by měl být váš deník pojištění založen na šabloně deníku bez číselné řady. Je to proto, že vložená čísla dokladů z řádku deníku dlouhodobého majetku budou jinak v konfliktu s číselnou řadou deníku pojištění. Pro více informací o šablonách deníku a listech, navštivnte [Nastavení obecných informací o dlouhodobém majetku](fa-how-setup-general.md).

Po přiřazení dlouhodobého majetku k pojistné smlouvě je na kartě dlouhodobého majetku zaškrtnuto políčko **Pojištěno**. Když prodáte dlouhodobý majetek, zaškrtávací políčko se automaticky zruší.

## Vytvoření nebo úprava karty pojištění
Pojistná smlouva pro dlouhodobý majetek musí být reprezentována kartou pojištění.

Pokud obdržíte informace o změnách ve výši krytí, musíte zadat nové informace na stránce **Karta pojištění** abyste zajistili správnou analýzu pojistného krytí.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pojištění** a poté vyberte související odkaz.
2. Vyberte akci **Nový** a vytvořte novou kartu pro pojistnou smlouvu. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Případně vyberte pojistku, kterou chcete změnit, a pak zvolte akci **Upravit**.

## Přiřazení dlouhodobého majetku k pojistné smlouvě zaúčtováním z deníku pojištění
Dlouhodobý majetek přiřadíte k pojistné smlouvě zaúčtováním do položek pojistného krytí.

Následující postup vysvětluje, jak ručně vytvořit řádek deníku pojištění. Pokud je na stránce **Nastavení DM** zaškrtnuto políčko **Automatické účtování pojištění**, pak se po zaúčtování pořizovacích nákladů automaticky vytvoří řádky deníku pojištění. V takovém případě stačí deník zaúčtovat.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky pojištění** a poté vyberte související odkaz.
2. Otevřete příslušný deník a podle potřeby vyplňte řádky deníku.
3. Chcete-li přiřadit více dlouhodobého majetku k jedné pojistce, vytvořte řádky deníku se stejnou hodnotou v poli **Číslo pojištění** a různou hodnotou v poli **Číslo DM**.
4. Vyberte akci **Účtovat**.

   > [!NOTE]
   > Položky z deníku pojištění jsou zaúčtovány pouze do položek pojistného krytí.

## Aktualizace hodnoty pojištění dlouhodobého majetku
Pomocí dávkové úlohy **Indexace pojištění** můžete aktualizovat hodnotu krytého dlouhodobého majetku.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Indexace pojištění** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole.

   > [!NOTE]
   > Do pole **Hodnota indexu** můžete zadat pokles o 5%, například jako 95 nebo zvýšení o 2% jako 102.
3. Vyberte tlačítko **OK**.

   Dávková úloha vypočítá novou částku jako procento z celkové pojištěné částky, jak je uvedeno na stránce **Statistika pojištění** a poté vytvoří řádek v deníku pojištění.
4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky pojištění** a poté vyberte související odkaz.
5. Otevřete příslušný deník pojištění, zkontrolujte vytvořené částky a poté je zaúčtujte do položek pojistného krytí.

## Sledování pojistného krytí
[!INCLUDE[d365fin](includes/d365fin_md.md)] poskytuje vyhrazené sestavy a statistické stránky pro použití při analýze pojistných smluv a zda je váš dlouhodobý majetek nadměrně nebo nedostatečně pojištěný.

### Přehled pojistných smluv
Chcete-li získat přehled o svých pojistných smlouvách, prohlédněte si náhled nebo vytiskněte sestavu **Přehled pojištění**. Sestava zobrazuje všechny pojistky a nejdůležitější pole z karet pojištění.

### Pojistné krytí
Chcete-li zjistit, které pojistné smlouvy pokrývají jednotlivé aktivum a o jakou částku, můžete zobrazit náhled nebo vytisknout sestavu **Pojištění-celk. hodnota poj**.

### Nadměrné/nedostatečné pokrytí
Můžete zkontrolovat, zda je dlouhodobý majetek nadměrně nebo nedostatečně pojištěný, a to následujícími způsoby:

* Pomocí stránky **Statistika pojištění**. Kladná částka v poli **Předimenzované nebo poddimenzované pojištění** znamená, že dlouhodobý majetek je nadměrně pojištěn. Záporná částka znamená, že je nedostatečně pojištěn.
* Pomocí stránky **Statistika DM**. Výběrem pole **Celková pojištěná částka** zobrazíte stránku **Položky  pojistného krytí**.
* Pomocí sestavy **Nadměrné/nedostatečné pokrytí**.
* Pomocí sestavy **Analýza pojištění**.

### Nepojištěný dlouhodobý majetek
Chcete-li zkontrolovat, zda jste nezapomněli přiřadit dlouhodobý majetek k pojistné smlouvě, můžete vytisknout nebo zobrazit náhled **Pojištění - nepojištěný DM**. Tato sestava zobrazuje dlouhodobý majetek, pro který nebyly částky zaúčtovány do položek pojistného krytí.

## Zobrazení položek pojistného krytí
Můžete zobrazit položky, které jste vytvořili v položkách pojistného krytí.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pojištění** a poté vyberte související odkaz.
2. Vyberte příslušnou pojistnou smlouvu a pak zvolte akci **Položky krytí**.

## Zobrazení celkové hodnoty dlouhodobého majetku
Vyhrazená stránka matice zobrazuje hodnoty pojištění, které jsou registrovány pro každou pojistnou smlouvu pro každý dlouhodobý majetek v důsledku částek souvisejících s pojištěním, které jste zaúčtovali.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pojištění** a poté vyberte související odkaz.
2. Vyberte příslušnou pojistnou smlouvu a pak zvolte akci **Celková částka pojištění na DM**.
3. Podle potřeby vyplňte pole.
4. Vyberte akci **Zobrazit matici**.
5. Chcete-li zobrazit základní položky pojistného krytí, vyberte hodnotu v matici.

## Oprava položek pojistného krytí
Pokud byl dlouhodobý majetek připojen k nesprávné pojistné smlouve, můžete jej opravit vytvořením dvou položek přeřazení z deníku pojištění.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky pojištění** a poté vyberte související odkaz.
2. Vytvořte jeden řádek deníku pro dlouhodobý majetek a správnou pojistnou smlouvu, kde je hodnota v poli **Částka** kladná.
3. Vytvořte další řádek deníku pro dlouhodobý majetek a nesprávnou pojistnou smlouvu, kde je hodnota v poli **Částka** záporná.
4. Vyberte akci **Účtovat**.

Dlouhodobý majetek bude odpojen od nesprávné pojistky na druhém řádku a připojen ke správné pojistce na prvním řádku.

## Viz také
[Dlouhodobý majetek](fa-manage.md)  
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
