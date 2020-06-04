---
title: Create a Job Sales Invoice to Invoice a Job| Microsoft Docs
description: Describes how to invoice customers for job expenses as a project progresses.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2019
ms.author: sgroespe

---
# Fakturace projektů
Během projektu se mohou hromadit náklady na projekt z využití zdrojů, materiálů a nákupů souvisejících s projektem. V průběhu projektu se tyto transakce zaúčtují do deníku projektů. Je důležité, aby byly všechny náklady zaznamenány do deníku projektů před fakturací odběratele.

Celý projekt můžete fakturovat ze stránky **Řádky úlohy projektu** nebo pouze fakturovat vybrané fakturovatelné řádky ze stránky **Řádky plánování**. Fakturace může být provedena po dokončení úlohy nebo v určitých intervalech během postupu úlohy na základě harmonogramu fakturace.

> [!NOTE]
> Pokud vyberete **Fakturovatelné** na poli **Typ řádku projektu** na nákupních dokladech pro nákupy související s projektem, pak jsou vytvořeny řádky plánování projektu, které jsou připraveny k fakturaci zákazníkovi. Pro více informací navštivte [Správa dodávek projektu](projects-how-manage-project-supplies.md).

## Vytvoření a zaúčtování prodejní faktury projektu
Můžete vytvořit fakturu pro projekt, nebo pro jednu a více úloh projektu pro zákazníka, a to když je dokončena buď práce, která má být fakturována, nebo bylo dosaženo data fakturace podle fakturačního plánu.

Ze stránky **Úlohy**, můžete fakturovat zákazníka výběrem úlohy a následným výběrem akce **Vytvořit prodejní fakturu projektu**. Následující postup ukazuje, jak pomocí dávkové úlohy fakturovat více projektů.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vytvořit prodejní fakturu projektu** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Nastavte filtry, pokud chcete omezit projekty, které bude dávková úloha zpracovávat.
4. Zvolte tlačítko **OK** a začněte vytvářet faktury.

## Vytvoření více prodejních faktur projektu z řádků plánování projektu
Můžete vytvořit fakturu z řádků plánování projektu a zároveň označit množství zboží, zdroje nebo finančního účtu, které chcete fakturovat.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Otevřete příslušný projekt.
3. Vyberte úlohu projektu, pro kterou pole **Typ úlohy projektu** obsahuje **Účtování**, a poté vyberte akci **Řádky plánování projektu**.
4. Na řádku plánování projektu, v poli **Množství k transf. k fakturaci** zadejte množství zboží, zdroje, typu účtu hlavní knihy, které chcete fakturovat.
5. Zvolte akci **Vytvořit prodejní fakturu**.
6. Na stránce **Vytvořit prodejní fakturu projektu**, zadejte datum zúčtování a zda chcete vytvořit novou fakturu nebo připojit tuto fakturu k existující.
7. Zvolte tlačítko **OK**.

   Na řádku plánování projektu, v poli **Množství k transf. k fakturaci**, můžete vidět množství.
8. Na stránce **Řádky plánování projektu**, vyberte akci **Prodejní faktury/Dobropisy**.

   Stránka **Prodejní faktura** při otevření, udává množství, které jste převedli na fakturu.
9. Proveďte další změny a pak zvolte akci **Účtovat**.

> [!NOTE]
> Výše uvedený postup je podobný pro vytvoření, kontrolu a zaúčtování dobropisu z prodeje související s projektem.

## Výpočet a zaúčtování položek dokončení projektu
Po dokončení všech činností projektu, včetně účtování za použití a fakturace, musíte aktualizovat projekt tak, aby měl **Stav** **Dokončeno**. Potom je nutné stornovat všechny nedokončené výroby, které byly zaúčtovány do hlavní knihy.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Vyberte otevřený projekt a poté vyberte akci **Upravit**.
3. V poli **Stav**, vyberte **Dokončeno**.
4. Podle pomocných kroků můžete vypočítat a odeslat nedokončenou výrobu. Alternativně, postupujte podle kroků 5 a 6, abyste tak učinili ručně.
5. Vyberte akci **Kalkulovat NV**.
6. Na stránce **Vypočítat NV projektu**, vyplňte pole podle potřeby.

   Položky nedokončené výroby projektu vytvořené spuštěním dávkové úlohy budou mít zaškrtnuté políčko **Dokončený projekt** což znamená, že se jedná o položky dokončení.
7. Vyberte akci **Zaúčtovat NV projektu**.
8. Na stránce **Zaúčtovat NV projektu**, vyplňte pole podle potřeby.

   Položky nedokončené výroby projektu vytvořené spuštěním dávkové úlohy budou mít zaškrtnuté políčko **Dokončený projekt** což znamená, že se jedná o položky dokončení.

## Viz také
[Správa projektů](projects-manage-projects.md)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
