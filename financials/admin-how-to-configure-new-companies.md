---
title: Jak nakonfigurovat nové společnosti | Microsoft Docs
description: 'Můžete nakonfigurovat a přizpůsobit novou společnost, kterou jste vytvořili. Chcete-li doladit implementaci, dokončete konfiguraci ve třech fázích.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 03/01/2019
ms.author: sgroespe
---
# <a name="configure-new-companies"></a>Konfigurace nových společností
Pro konfiguraci nové společnosti při vaší implementaci řešení obvykle postupujete podle tří fází. V první fázi importujete konfigurační balíček, soubor .rapidstart s konfiguračními informacemi. Ve druhé fázi změníte konfigurační informace a poté je použijete pro vaši novou společnost. V závěrečné fázi zkontrolujete a opravíte chyby.  

Následující postupy předpokládají, že jste vytvořili a uložili konfigurační balíček. Pro více informací navštivte [Připravení konfiguračního balíčku](admin-how-to-prepare-a-configuration-package.md).  

Následující postupy předpokládají, že jste inicializovali a otevřeli novou společnost a že používáte roli Implementátor služeb RapidStart v Centru rolí.

## <a name="to-import-a-configuration-package"></a>Pro import konfiguračního balíčku  
1. Otevřete novou společnost v databázi [!INCLUDE [d365fin](includes/d365fin_md.md)].  
2. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), klikněte na **Konfigurační balíčky** a poté vyberte související odkaz.  
3. Zvolte akci **Importovat balíček**.  
4. Přejděte do umístění, kam jste uložili soubor konfiguračního balíčku .rapidstart, a poté zvolte tlačítko **Otevřít**.  
5. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), klikněte na **Informace o společnosti** a poté zvolte související odkaz. Na kartě firemních údajů zadejte informace o společnosti. Uveďte informace, jako jsou bankovní údaje. Můžete také poskytnout logo společnosti.  

Importují se všechny tabulky, které jste určili pro zařazení do nové společnosti. V tomto okamžiku můžete aplikovat data balíčku do databáze nebo přizpůsobit a upravit data tabulky tak, aby vyhovovala vašim požadavkům zákazníka.  

## <a name="to-apply-package-data"></a>Pro aplikaci dat balíčku  
1. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), klikněte na **Konfigurační list** a poté vyberte související odkaz.  
2. Vyberte tabulku, pro kterou chcete upravit data, a poté vyberte akci **Použít data**. Stisknutím tlačítka **Ano** potvrďte aplikaci.
3. Pro potvrzení, že data jsou nyní v databázi a že aplikace byla úspěšná, vraťte se na stránku **Konfigurační sešit** a zvolte akci **Data databáze**.  

> [!NOTE]  
>  Po aplikování dat je můžete vidět pouze v databázi. Již nadále nejsou v balíčku.  

## <a name="to-modify-and-apply-package-data"></a>Pro upravení a aplikaci dat balíčku  
1. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), klikněte na **Konfigurační list** a poté vyberte související odkaz.  
2. Vyberte tabulku, pro kterou chcete upravit data, a poté vyberte akci **Data balíčku**.  
3. V okně **Záznamy konfiguračního balíčku** proveďte úpravy. Můžete například odstranit možnosti, které se neaplikují.  
4. Zvolte akci **Použít data** a poté klepněte na tlačítko **OK**.  
5. Pro potvrzení, že data jsou nyní v databázi a že aplikace byla úspěšná, vraťte se do okna **Konfigurační sešit** a zvolte akci **Data databáze**.  

## <a name="to-locate-and-identify-a-configuration-error"></a>Pro vyhledání a identifikaci chyby konfigurace  
Při aplikaci dat do databáze se mohou vyskytnout určité typy chyb. Nejčastější chybou je, že požadované související tabulky nebyly zahrnuty. Tyto chyby opravíte v konfiguračním sešitu.

1. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), klikněte na **Konfigurační balíčky** a poté vyberte související odkaz.  
2. Vyberte balíček, který chcete zkontrolovat, a poté vyberte akci **Upravit**.  

    Tabulky, které obsahují chyby, jsou zvýrazněny. Počet chyb balíčku je zobrazen v poli **Počet chyb balíčku**.  

3. Zvolte pole **Počet chyb balíčku** a otevřete okno **Záznamy konfiguračního balíčku**, kde jsou uvedeny záznamy s chybami.  

### <a name="to-fix-an-error"></a>Pro opravení chyby  
1. Otevřete společnost, která je založena na vašem konfiguračním balíčku.  
2. Zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), klikněte na **Konfigurační list** a poté vyberte související odkaz.  
3. Opravte chyby, jako je například přidání chybějících souvisejících tabulek do sešitu.  
4. Přidejte tabulky do existujícího konfiguračního balíčku nebo vytvořte nový balíček, který obsahuje pouze nové tabulky. Pro více informací navštivte [Připravení konfiguračního balíčku](admin-how-to-prepare-a-configuration-package.md).  
5. Znovu otevřete novou společnost, pro kterou implementujete konfiguraci.  
6. Importujte konfigurační balíček.  

    > [!NOTE]  
    >  Pokud znovu importujete stejný balíček, můžete přepsat všechny již provedené úpravy dat. Z tohoto důvodu můžete chtít přidat některé nové tabulky do nového balíčku a importovat je.  

7. Aplikujte data do databáze, jak je popsáno v části [Pro upravení a aplikaci dat balíčku](admin-how-to-configure-new-companies.md#to-modify-and-apply-package-data).

## <a name="see-also"></a>Viz také  
[Aplikování konfigurace pro nové společnosti](admin-apply-configuration-to-new-companies.md)  
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Správa](admin-setup-and-administration.md)
