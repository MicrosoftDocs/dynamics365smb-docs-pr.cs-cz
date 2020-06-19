---
title: Manual Synchronization of Table Mappings | Microsoft Docs
description: The synchronization copies data between Dynamics 365 Sales entries and Business Central to keep both systems up-to-date.
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 10/01/2019
ms.author: bholtorf

---

# Ruční synchronizace mapování tabulek
Mapování integrační tabulky přiřadí tabulku [!INCLUDE[d365fin](includes/d365fin_md.md)] (typ záznamu), jako je zákazník, s entitou [!INCLUDE[crm_md](includes/crm_md.md)], jako je účet. Synchronizace mapování integrační tabulky umožňuje synchronizaci dat ve všech záznamech tabulky [!INCLUDE[d365fin](includes/d365fin_md.md)] a entity [!INCLUDE[crm_md](includes/crm_md.md)], které jsou ve spojení. Navíc v závislosti na konfiguraci mapování tabulek může synchronizace vytvořit a spojit nové záznamy v cílovém řešení pro neoddělené záznamy ve zdroji.

Ruční synchronizace mapování tabulek integrace může být užitečná během počátečního nastavení integrace a při diagnostice chyb synchronizace.

Tento článek popisuje tři metody pro ruční synchronizaci mapování integračních tabulek. Každá metoda poskytuje jinou úroveň synchronizace.

## Spuštění úplné synchronizace
Při úplné synchronizaci budou spuštěny všechny výchozí úlohy integrační synchronizace pro synchronizaci záznamů [!INCLUDE[d365fin](includes/d365fin_md.md)] a entit [!INCLUDE[crm_md](includes/crm_md.md)], jak je definováno na stránce **Mapování tabulky integrace**.

Úplná synchronizace provádí následující operace pro záznamy [!INCLUDE[d365fin](includes/d365fin_md.md)] nebo [!INCLUDE[crm_md](includes/crm_md.md)], které jsou:

* Není-li připojen, bude vytvořen nový porovnávací záznam a bude následně spojen do protichůdného řešení.
To, zda a kde bude záznam vytvořen, závisí na směru synchronizace. Například při synchronizaci dat od zákazníků  [!INCLUDE[d365fin](includes/d365fin_md.md)] na účty [!INCLUDE[crm_md](includes/crm_md.md)] pokud existuje zákazník, který není spojen s účtem, potom bude automaticky přidán nový účet v [!INCLUDE[crm_md](includes/crm_md.md)] a připojen k zákazníkovi v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Opak platí, když je směr synchronizace od [!INCLUDE[crm_md](includes/crm_md.md)] do [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro každý účet, který ještě není spojen se zákazníkem, bude vytvořen nový odpovídající zákazník v [!INCLUDE[d365fin](includes/d365fin_md.md)] a připojen k účtu v [!INCLUDE[crm_md](includes/crm_md.md)].

   > [!NOTE]
   > Aby toho bylo dosaženo, operace úplné synchronizace dočasně vymaže možnost **Synchronizovat  pouze spárované záznamy** v mapování integrační tabulky, která je používána úlohou synchronizace. Na konci procesu úplné synchronizace budete vyzváni, zda si přejete ponechat tuto možnost vymazanou pro všechny úlohy.

* Směr synchronizace (například z [!INCLUDE[d365fin](includes/d365fin_md.md)] do [!INCLUDE[crm_md](includes/crm_md.md)]  nebo z [!INCLUDE[crm_md](includes/crm_md.md)] do [!INCLUDE[d365fin](includes/d365fin_md.md)]) je předurčen mapováním integračních tabulek. Pro více informací navštivte [Standardní mapování entit prodeje pro synchronizaci](admin-synchronizing-business-central-and-sales.md).

Úlohy jsou spouštěny v následujícím pořadí, aby nedošlo k propojení závislostí mezi entitami.

1. Úloha synchronizace Měny transakce - Dynamics 365 Sales
2. Úloha synchronizace Prodejci - Dynamics 365 Sales
3. Úloha synchronizace Měrná jednotka - Dynamics 365 Sales
4. Úloha synchronizace Zákazník - Dynamics 365 Sales
5. Úloha synchronizace Kontakty - Dynamics 365 Sales
6. Úloha synchronizace Zdroj-produkt - Dynamics 365 Sales
7. Úloha synchronizace Zboží-Produkt - Dynamics 365 Sales

> [!IMPORTANT]
> Úplnou synchronizaci obvykle používáte, pouze pokud jste původně nastavili integraci mezi [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] a když pouze jedno řešení obsahuje data, která chcete zkopírovat do druhého řešení. Úplná synchronizace může být užitečná v demonstračním prostředí. Protože úplná synchronizace automaticky vytváří a spojuje záznamy mezi řešeními, je rychlejší začít pracovat se synchronizací dat mezi záznamy. Na druhou stranu byste měli spustit úplnou synchronizaci pouze v případě, že chcete záznam v [!INCLUDE[d365fin](includes/d365fin_md.md)] pro každý záznam v [!INCLUDE[crm_md](includes/crm_md.md)] pro daná mapování tabulek. V opačném případě můžete mít nežádoucí nebo duplicitní záznamy v [!INCLUDE[d365fin](includes/d365fin_md.md)] nebo [!INCLUDE[crm_md](includes/crm_md.md)].

### Podívejte se na postup pro úplnou synchronizaci
> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085502]

### Spuštění úplné synchronizace
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení připojení k Microsoft Dynamics 365 for Sales** a poté vyberte související odkaz.
2. Vyberte akci **Spustit úplnou synchronizaci** a poté vyberte tlačítko **Ano**.
3. Po dokončení úplné synchronizace můžete určit, zda chcete naplánovaným synchronizačním úlohám vytvářet nové záznamy.

   Pokud chcete, aby všechny synchronizační úlohy vytvořily nové cíle v cílovém adresáři pro neoddělené záznamy ve zdroji, zvolte **Ano**. Tím nastavíte pole **Synchronizovat  pouze spárované záznamy** v mapovacích tabulkách, která jsou používána synchronizačními úlohami.

   Pokud chcete, aby se synchronizační úlohy spouštěly stejně jako před úplnou synchronizací s ohledem na vytváření nových záznamů, zvolte **Ne**. Tím nastavíte pole **Synchronizovat  pouze spárované záznamy** na nastavení, které mělo před úplnou synchronizací.

Výsledky úplné synchronizace si můžete prohlédnout na stránce **Úlohy synchronizace integrace**. Pro více informací navštivte [Zobrazení stavu synchronizace](admin-how-to-view-synchronization-status.md).

## Synchronizace všech upravených záznamů
Na stránce **Nastavení připojení Microsoft Dynamics 365 for Sales** můžete synchronizovat změny dat ve všech mapovaných tabulkách integrace. Je to podobné jako při plné synchronizaci. Bude synchronizovat data ve všech spojených záznamech v tabulkách [!INCLUDE[d365fin](includes/d365fin_md.md)] a entitách [!INCLUDE[crm_md](includes/crm_md.md)], které jsou definovány v mapování tabulek. Ve výchozím nastavení budou synchronizovány pouze záznamy, které byly změněny od poslední synchronizace. Mapování tabulek je synchronizováno v následujícím pořadí, aby nedošlo k propojení závislostí mezi entitami:

1. Úloha synchronizace Měny transakce - Dynamics 365 Sales
2. Úloha synchronizace Prodejci - Dynamics 365 Sales
3. Úloha synchronizace Měrná jednotka - Dynamics 365 Sales
4. Úloha synchronizace Zákazník - Dynamics 365 Sales
5. Úloha synchronizace Kontakty - Dynamics 365 Sales
6. Úloha synchronizace Zdroj-Produkt\- Dynamics 365 Salesb
7. Úloha synchronizace Zboží-Produkt - Dynamics 365 Sales

Výsledky synchronizace můžete zobrazit na stránce **Úlohy synchronizace integrace**. Pro více informací navštivte [Zobrazení stavu synchronizace](admin-how-to-view-synchronization-status.md).

> [!TIP]
> Úpravou mapování integrační tabulky předem můžete nakonfigurovat synchronizaci s filtry, abyste určili, které záznamy jsou synchronizovány, nebo je nakonfigurujte tak, aby vytvářely nové záznamy v cílovém řešení pro neoddělené záznamy ve zdroji. Pro více informací navštivte [Úprava mapování tabulek pro synchronizaci](admin-how-to-modify-table-mappings-for-synchronization.md).

### Synchronizace záznamů pro všechny tabulky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení připojení k Microsoft Dynamics 365 for Sales** a poté vyberte související odkaz.
2. Vyberte akci **Synchronizovat upravené záznamy** a poté vyberte **Ano**.

## Synchronizace mapování jednotlivých tabulek
Na stránce **Mapování integračních tabulek** můžete použít mapování tabulek specifických pro synchronizační úlohu. To bude synchronizovat data ve všech propojených záznamech v tabulce [!INCLUDE[d365fin](includes/d365fin_md.md)] a entitě [!INCLUDE[crm_md](includes/crm_md.md)], která je definována mapováním tabulky. Ve výchozím nastavení budou synchronizovány pouze záznamy, které byly změněny od poslední synchronizace.

Úpravou mapování integrační tabulky předem můžete nakonfigurovat synchronizační úlohu tak, aby v cílovém řešení vytvořila nové záznamy pro neoddělené záznamy ve zdroji.

### Synchronizace záznamů mapování integrační tabulky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Mapování tabulky integrace** a poté vyberte související odkaz.
2. Vyberte akci **Synchronizovat upravené záznamy** a poté vyberte **Ano**.

## Viz také
[Synchronizace Business Central a Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)  
[Nastavení uživatelských účtů pro integraci s Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)
