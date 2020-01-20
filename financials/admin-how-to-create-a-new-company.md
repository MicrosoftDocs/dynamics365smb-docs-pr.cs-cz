---
title: Jak vytvořit novou společnost | Microsoft Docs
description: 'Pro použití služeb RapidStart jsou vytvořeny tabulky a stránky, ale v nich nejsou žádná data.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 03/06/2018
ms.author: sgroespe
---
# <a name="create-a-new-company"></a>Vytvoření nové společnosti
Chcete-li používat služby RapidStart pro [!INCLUDE [d365fin](includes/d365fin_md.md)], musíte nejprve vytvořit novou společnost, pro kterou chcete provést implementaci zákazníka. Když vytvoříte novou společnost, vytvoří se standardní tabulky a stránky [!INCLUDE [d365fin](includes/d365fin_md.md)], ale v nich nejsou žádná data.

Kromě toho můžete po inicializaci použít ve vaší společnosti konkrétní instalační data. Informace jsou poskytovány v konfiguračním balíčku, souboru .rapidstart, který dodává obsah v komprimovaném formátu.  

Příklady konfiguračních balíčků, včetně souborů specifických pro zemi nebo oblast, jsou součástí demonstrační společnosti CRONUS. Použijte následující postupy pro použití vzorového konfiguračního balíčku s novou společností.  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a>Použití ukázkového konfiguračního balíčku BASICCONIG  
1. Otevřete společnost CRONUS International Ltd. Pro více informací navštivte [Změna základního nastavení](ui-change-basic-settings.md).
2. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), klikněte na **Konfigurační balíčky** a poté zvolte související odkaz.  
3. Vyberte balíček BASICCINFOG ze seznamu a poté vyberte akci **Exportovat balíček**.  

Následující postup použijte k vytvoření nové společnosti a jako součást procesu použijte balíček BASICCONFIG.  

## <a name="to-create-a-new-company"></a>Vytvoření nové společnosti  
1. Vytvořte novou společnost. Pro více informací navštivte [Vytváření nových společností v [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md).
2. Z role Implementátor služeb RapidStart můžete nyní importovat konfigurační balíček, který jste exportovali od společnosti CRONUS International Ltd.

Po vytvoření nové společnosti jsou některé tabulky automaticky vyplněny, i když není použita žádná firemní šablona. V okně **Zdrojový kód** si můžete například prohlédnout standardní kódy pro účtování a dávkové transakce. Pokud poskytujete místní verzi [!INCLUDE [d365fin](includes/d365fin_md.md)], měli byste si přečíst tuto tabulku a zvážit případné problémy s místním jazykem.

## <a name="about-data-tables"></a>O datových tabulkách
[!INCLUDE [d365fin](includes/d365fin_md.md)], data přicházejí ve dvou základních typech: hlavní a data nastavení. Při nastavování firemní konfigurace můžete pomocí těchto typů zaměřit svou konfigurační strategii.  

### <a name="master-data-tables"></a>Tabulky hlavních dat  
V následující tabulce jsou uvedeny některé tabulky hlavních dat. Při inicializaci nové společnosti jsou tyto tabulky prázdné.  

|Číslo tabulky|Název tabulky|  
|-------------------|--------------------|  
|15|Finanční účet|  
|18|Zákazník|  
|23|Dodavatel|  
|27|Zboží|  
|5050|Kontakt|  

### <a name="setup-data-tables"></a>Tabulky dat nastavení  
V následující tabulce jsou uvedeny některé tabulky dat nastavení, ve kterých zaznamenáváte informace o nastavení do konfiguračního dotazníku. Tyto tabulky obsahují základní informace o založení společnosti.  

|Číslo tabulky|Název tabulky|  
|-------------------|--------------------|  
|98|Nastavení financí|  
|311|Nastavení prodeje a pohledávek|  
|312|Nastavení nákupu a závazků|  
|313|Nastavení zásob|  

Kromě datových tabulek nastavení má [!INCLUDE [d365fin](includes/d365fin_md.md)] také datové tabulky typu nastavení, které specifikují základní informace o společnosti a jejích obchodních procesech. Následující tabulka uvádí některé z nich.  

|Číslo tabulky|Název tabulky|  
|-------------------|--------------------|  
|3|Platební podmínky|  
|4|Měna|  
|6|Cenové skupiny odběratele|  
|5700|Skladová jednotka|

  

## <a name="see-also"></a>Viz také  
[Aplikování konfigurace pro nové společnosti](admin-apply-configuration-to-new-companies.md)  
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Správa](admin-setup-and-administration.md)
