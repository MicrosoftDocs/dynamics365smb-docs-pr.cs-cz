---
title: Create a Job Card for a Job and Specify Tasks| Microsoft Docs'
description: For a new project, you create a job card that contains job tasks and planning lines, to help you manage progress and budgets.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: project management, task
ms.date: 10/01/2019
ms.author: sgroespe
---
# Vytváření projektů

Při spuštění nového projektu je nutné vytvořit kartu projektu s integrovanými úkoly projektu a řádky plánování projektu, strukturované do dvou vrstev.

První vrstvu tvoří úlohy projektu. Musíte vytvořit alespoň jednu úlohu projektu na projekt, protože všechna účtování odkazují na úlohu projektu. Pokud ve svém projektu máte alespoň jednu úlohu projektu, můžete založit řádky plánování projektu a zaúčtovat spotřebu do projektu.

Druhá vrstva se skládá z řádků plánování projektu, které specifikují podrobné použití zdrojů, zboží a různých výdajů do hlavní knihy.

Struktura vrstvy umožňuje rozdělit projekt na menší úkoly, a proto umožňuje použít konkrétnější podrobnosti při sestavování rozpočtu, nabídek a evidencí. Kromě toho vám umožní nahlédnout do toho, jak projekt postupuje. Můžete například sledovat, zda dodržujete stanovené milníky nebo zda míříte k cíli, abyste splnili očekávání rozpočtu.

> [!TIP]
> Vyberte akci **Nový projekt** v centru rolí **Projektový Manažer** ke spuštění asistovaného nastavení, který vás provede kroky vytvoření projektu s integrovanými úlohami a řádky plánování projektu. Následující postup popisuje, jak provést kroky ručně. Pro příklad ručního vytváření úlohy navštivte [video: How to create a job in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw).

## Vytvoření karty projektu
Vytvořte kartu projektu a poté pro ni vytvořte úlohy projektu a řádky plánování projektu.


1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Vyberte akci **Nový** a vyplňte pole dle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Chcete-li určit projekt s informacemi o dalších projektech, vyberte akci **Kopírovat projekt**, vyplňte pole podle potřeby a poté vyberte tlačítko **OK**.

> [!NOTE]
> Pokud ve svých projektech používáte pracovní výkazy, musíte také určit odpovědnou osobu. Tato osoba může schválit pracovní výkazy pro úkoly zaměstnance přidružené k projektu. Pro více informací navštivte [Pracovní výkazy](projects-how-setup-time-sheets.md).

## Vytvoření úlohy projektu
Klíčovou součástí vytvoření projektu je určení různých úkolů, které se v projektu vyskytují. To uděláte přidáním nových řádků v záložce s náhledem **Úlohy** na stránce ** Karta projektu**, pokaždé jeden projekt na řádek. Každý projekt musí mít alespoň jednu úlohu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Otevřete kartu projektu pro příslušný projekt.
3. Na záložce **Úlohy** vyplňte pole dle potřeby na novém řádku.
4. Chcete-li odsadit úkoly a vytvořit hierarchii, zvolte akci**Úlohy**, a pak zvolte akci **Odsadit úlohy projektu**.
5. Opakujte kroky 3 a 4 pro všechny úlohy, které pro projekt potřebujete.
6. Chcete-li určit projektové úlohy s informacemi o dalších úlohách projektu, vyberte tlačítko **Kopírovat úlohy projektu**, vyplňte pole podle potřeby a poté zvolte tlačítko **OK**.

## Vytvoření Řádků plánování projektu
Nové úlohy projektu můžete upřesnit na řádcích plánování projektu. Řádek plánování lze použít k zachycení všech informací, které chcete na projektu sledovat. Řádky plánování můžete použít k přidání informací, například jaké zdroje jsou požadovány, nebo k zachycení zboží potřebných k provedení projektu. Pokud například máte za úkol získat zakázku ze strany zákazníka, můžete ji přiřadit k plánovacím řádkům pro položky, jako je schůzka se zákazníkem a přiřazení zdroje.

Řádek plánování projektu může mít jeden z následujících typů.

| Typ | Popis |
| --- | --- |
| **Plán** | Poskytuje odhad spotřeby a nákladů na projekt, obvykle v projektu typu čas a materiál. Řádky plánování tohoto typu nelze fakturovat. |
| **Fakturovatelné** | Poskytuje odhadovanou fakturaci zákazníkovi, obvykle v projektu s pevnou cenou. |
| **Plán i Fakturovatelné** | Poskytuje odhad spotřeby a nákladů na projekt, který se zároveň bude fakturovat. |

**Poznámka**. Při zadávání informací do řádků plánování projektu se automaticky vyplňují informace o nákladech. Například náklady, cena a sleva na zdroje a položky jsou původně založeny na informacích, které jsou definovány na kartách zdrojů a položek.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. Otevřete příslušnou kartu projektu.
3. Vyberte úlohu projektu, pro kterou pole**Typ úlohy projektu** obsahuje **Účtování**, a poté vyberte akci **Řádky plánování projektu**.
4. Na stránce **Řádky plánování projektu**, vyplňte pole podle potřeby.
5. Opakujte kroky 3 a 4 pro všechny řádky plánování, které potřebujete pro úlohu projektu.

## Viz také


[Správa projektů](projects-manage-projects.md)  
[Video: How to create a job in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
