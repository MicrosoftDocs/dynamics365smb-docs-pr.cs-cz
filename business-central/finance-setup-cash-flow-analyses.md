---
title: Setting up Cash Flow Analysis| Microsoft Docs
description: Set up the charts on the Accounts Role Center to help analyze the flow of money in your business, including expenses and income, liquidity, and cash receipts minus cash payments.
services: project-madeira
documentationcenter: ''
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: money flow, expense and income, liquidity, cash receipts minus cash payments, Cartera, funds
ms.date: 01/13/2020
ms.author: bholtorf

---
# Nastavení analýzy cashflow
Pokud chcete pomoci s rozhodnutím o tom, co dělat s vaší hotovostí, podívejte se na grafy v Centru rolí -  Účetní:

* **Hotovostní cyklus**
* **Výnosy a Náklady**
* **Cash Flow**
* **Předpověď Cash Flow**

Toto téma popisuje, odkud pocházejí data v grafech a také to, co dělat, když chcete začít používat grafy.  
<br><br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mJhc]

## Grafy peněžních cyklů, příjmů a výdajů
Grafy **Hotovostní cyklus** a **Výnosy a Náklady** jsou připraveny k použití, založeny na účetní osnově a účetních schématech. Účty účetní osnovy jsou zdrojem dat a účetní schémata vypočítávají vztah mezi prodejem a pohledávkami. K dispozici jsou některé účty a účetní schémata. Můžete je použít tak, jak jsou nebo je změnit a případně přidat nové. Pokud přidáte účty účetní osnovy do grafů, například jejich importem z QuickBooks, budete muset namapovat na účty na stránce **Účetní schémata** pro následující názvy účetních schémat:

| Účetní schémata | Kde se používají |
| --- | --- |
| **I_CACYCLE** | Data pro graf Hotovostní Cyklus |
| **I_CASHFLOW** | Data pro graf Cash Flow |
| **I_INCEXP** | Data pro graf Náklady a Výnosy |
| **I_MINTRIAL** | Info část dat pro redukovanou zkušební bilanci |

**Note** Je vhodné zachovat výpočty, které jsou k dispozici pro účetní schéma.

Zadejte účty do políčka **Součet** pro **Celkové tržby**, **Celkové příjmy**, **Celkové náklady** a **Celkové zásoby**. Chcete-li mapovat na rozsah účtů nebo na více než jeden konkrétní účet, zadejte čísla účtů oddělená znaky ".." nebo svislým pruhem. Například, **1111..4444** nebo **2222|3333|5555**.

**Tip** Pro ověření mapování použijte funkci **Náhled**.

## Nastavení grafu Cash Flow
Graf Cash Flow je založen na následujích:

* Graf účtů peněžních toků.
* Jedno nebo více nastavení peněžních toků. Ty určují účty, které mají být použity pro hlavní knihu, nákup, prodej, služby a dlouhodobý majetek.

Abychom vám pomohli začít, jsou k dispozici některé účty a nastavení cashflow. Můžete je přidat, změnit nebo odebrat.

Chcete-li je nastavit vyhledejte **Účetní osnova cash flow**, vyberte odkaz a doplňte do polí. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Opakujte tyto kroky **Nastavení cash flow**.

## Seznam plánů cash flow
Graf **Plán cash flow** používá účty cashflow, nastavení cashflow a plán cash flow. Některé jsou k dispozici, ale můžete nastavit pomocí průvodce asistovaného nastavení. Průvodce vám pomůže určit věci, jako jsou: jak často aktualizovat plán, účty, na kterých jsou založeny, kdy platit daně a zda chcete zapnout [Azure AI](https://azure.microsoft.com/overview/ai-platform/) .

Seznam plánů cash flow může použít Azure AI k zahrnutí dokladů s datem splatnosti. Výsledkem je komplexnější předpověď. Připojení k Azure AI je již přednastaveno. Stačí jej pouze zapnout. Když se přihlásíte do [!INCLUDE[d365fin](includes/d365fin_md.md)], zobrazí se v modrém pruhu oznámení a poskytne odkaz na výchozí nastavení cash flow. Oznámení se zobrazí pouze jednou. Pokud ho zavřete, ale rozhodnete se zapnout Azure AI, můžete použít průvodce asistovaným nastavením nebo ručně.

> [!NOTE]  
> Případně můžete použít vlastní prediktivní webovou službu. Pro více informací navštivte [tématu Vytvoření a použití vlastní prediktivní webové služby pro prognózy cashflow](#AnchorText).

Použití průvodce asistovaným nastavením:

1. V centru rolí účetní, pod grafem **Plán Cash Flow**, vyberte tlačítko **Otevřít asistované nastavení**.
2. Vyplňte pole v každém kroku průvodce.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Seznam plánů cash flow** a vyberte související odkaz.
4. Na stránce **Seznam plánů cash flow**, vyberte tlačítko **Přepočítat plán**.

Použití ručního procesu:

1. V centru rolí účetní vyhledejte **Nastavení cash flow** a poté vyberte související odkaz.
2. Rozbalte záložku **Azure AI**, a vyberte šakrtávací tlačítko **Azure AI povoleno**.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Seznam plánů cash flow** a vyberte související odkaz.
4. Na stránce **Seznam plánů cash flow**, vyberte tlačítko **Přepočítat plán**.

> [!TIP]  
> Zvažte délku období, které služba použije při svých výpočtech. Čím více dat poskytnete, tím přesnější budou předpovědi. Také pozor na velké rozdíly v obdobích. Budou mít také vliv na předpovědi. Pokud Azure AI nenajde dostatek dat nebo se data budou velice lišit, služba neprovede předpověď.

## <a name="AnchorText"> </a>Vytvoření a použití vlastní prediktivní webové služby pro prognózy cashflow
Můžete také vytvořit vlastní prediktivní webovou službu založenou na veřejném modelu s názvem **Forecasting model for Microsoft Business Central** . Tento prediktivní model je k dispozici online v AI Azure Gallery. Chcete-li model použít, postupujte takto:

1. Otevřete prohlížeč a přejděte do [Azure AI Gallery](https://go.microsoft.com/fwlink/?linkid=828352) .
2. Vyhledejte **Forecasting Model for Microsoft Business Central**, a otevřete model v Azure Machine Learning Studio.
3. Použijte svůj účet Microsoft k registraci pracovního prostoru a potom zkopírujte model.
4. Spusťte model a publikujte jej jako webovou službu.
5. Poznamenejte si API URL a API klíč. Tyto přihlašovací údaje použijete pro nastavení cash flow.
6. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení Cash Flow** a vyberte související odkaz.
7. Rozbalte záložku **Azure AI** a vyplňte pole.

## Viz související školení v programu [Microsoft Learn](/learn/modules/forecast-cash-flow-dynamics-365-business-central/index)

## Viz také
[Analýza Cash Flow ve Vaši společnosti](finance-analyze-cash-flow.md)  
[Nastavení financí](finance-setup-finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
