---
title: Maintain Fixed Assets| Microsoft Docs
description: You keep a maintenance record of any repairs and service on a fixed asset.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 04/01/2020
ms.author: sgroespe

---
# Údržba dlouhodobého majetku
Náklady na údržbu jsou běžné pravidelné náklady vynaložené na zachování hodnoty dlouhodobého majetku. Na rozdíl od kapitálových zisků nezvyšují hodnotu.

Můžete zaznamenávat a udržovat aktuální soubor o údržbě a servisu dlouhodobého majetku, abyste měli snadno přístupné úplné záznamy o údržbě dlouhodobého majetku. Při každém používání dlouhodobého majetku zaznamenáte všechny relevantní informace, například datum služby, číslo dodavatele a telefonní číslo servisního agenta. Registrace údržby se zaznamenává pro každý dlouhodobý majetek z příslušné karty dlouhodobého majetku.

Indexace se používá k úpravě hodnot pro obecné změny cenové hladiny. Dávkovou úlohu **Indexace dlouhodobého majetku** lze použít k přepočtu nákladů na údržbu.

## Záznam údržby dlouhodobého majetku
Pokaždé, když byla provedena údržba, například servisní návštěva, můžete ji zaznamenat pro příslušný dlouhodobý majetek na stránce **Evidence údržby**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dlouhodobý majetek** a poté vyberte související odkaz.
2. Vyberte dlouhodobý majetek, pro který chcete zaznamenat údržbu, a pak zvolte akci **Evidence údržby**.
3. Na stránce **Evidence údržby** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Účtování nákladů na údržbu z finančního deníku DM
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Přehled knihy odpisů** a poté vyberte související odkaz.
2. Vyberte knihu odpisů, která je přiřazena k dlouhodobému majetku, a poté vyberte akci **Upravit**.
3. Na stránce **Karta knihy odpisů** zkontrolujte, zda není zaškrtnuto políčko **Údržba**. Tím je zajištěno, že náklady na údržbu nejsou účtovány do věcných položek.
4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky DM** a poté vyberte související odkaz.
5. Vytvořte počáteční řádek deníku a vyplňte pole podle potřeby.
6. V poli **Typ účtování DM** vyberte **Údržba**.
7. Vyberte akci **Vložit protiúčet  DM**. Druhý řádek deníku je vytvořen pro protiúčet, který je nastaven pro účtování údržby.

   > [!NOTE]
   > Krok 7 funguje pouze v případě, že jste nastavili následující: Na stránce **Karta účto skupiny DM** pro účto skupinu dlouhodobého majetku třeba nastavit pole **Účet údržby** tak, aby obsahoval MD účet hlavní knihy a pole **Protiúčet  údržby** musí obsahovat účet hlavní knihy, na který chcete zaúčtovat vyrovnávací položky. Pro více informací navštivte [Nastavení účto skupin dlouhodobého majetku](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Vyberte akci **Účtovat**.

## Sledování servisních návštěv dlouhodobého majetku
Můžete si vytisknout sestavu **Údržba – příští servis** a zjistit, pro které položky jste naplánovali servisní návštěvu. Tuto sestavu můžete také použít při aktualizaci pole **Datum další údržby** na kartách dlouhodobého majetku.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Údržba – příští servis** a poté vyberte související odkaz.
2. Vyplňte pole **Počáteční datum** a **Datum dokončení**.
3. Vyberte tlačítko **Tisk** nebo **Náhled**.

## Sledování nákladů na údržbu
Náklady na údržbu můžete zobrazit při pohledu na statistiky dlouhodobého majetku.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dlouhodobý majetek** a poté vyberte související odkaz.
2. Vyberte dlouhodobý majetek, pro který chcete zobrazit náklady na údržbu, a pak zvolte akci **Knihy odpisů**.
3. Na stránce **Knihy odpisů DM** vyberte příslušnou knihu odpisů dlouhodobého majetku a pak zvolte akci **Statistika**.
4. Na stránce **Statistika DM** vyberte pole **Údržba**.

Otevře se stránka **Položky údržby** zobrazující položky, které tvoří částku v poli **Údržba**.

## Zobrazení nebo tisk nákladů na údržbu pro více dlouhodobých aktiv
V sestavě **Údržba - analýza** můžete zvolit zobrazení údržby na základě jednoho, dvou nebo tří kódů údržby pro zadané datum nebo období. Můžete zobrazit součet všech vybraných majetků nebo součet pro každý majetek.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Analýza údržby** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole.
3. Vyberte tlačítko **Tisk** nebo **Náhled**.

## Zobrazení položek údržby
Náklady na údržbu můžete také studovat zobrazením položek údržby.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dlouhodobý majetek** a poté vyberte související odkaz.
2. Vyberte dlouhodobý majetek, pro který chcete zobrazit položky, a pak zvolte akci **Knihy odpisů**.
3. Na stránce **Knihy odpisů DM** vyberte příslušnou knihu odpisů dlouhodobého majetku a pak zvolte akci **Položky údržby**.

## Zobrazení nebo tisk položek údržby pro více dlouhodobých aktiv
V sestavě **Detaily údržby** můžete zobrazit nebo vytisknout položky údržby pro jeden nebo více dlouhodobých majetků.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Detaily údržby** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole.
3. Vyberte tlačítko **Tisk** nebo **Náhled**.

## Viz také
[Dlouhodobý majetek](fa-manage.md)  
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
