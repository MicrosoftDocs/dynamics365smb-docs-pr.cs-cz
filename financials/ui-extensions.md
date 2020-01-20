---
title: Instalace rozšíření pro přizpůsobení Business Central | Microsoft Docs
description: Zjistěte více o přidávání funkcí a přizpůsobení Business Central instalací rozšíření.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'app, add-in, manifest, customize'
ms.date: 07/07/2017
ms.author: edupont
---
# <a name="customizing-business-central-using-extensions"></a>Přizpůsobení Business Central pomocí rozšíření
Můžete změnit [!INCLUDE [d365fin](includes/d365fin_md.md)] instalací rozšíření, která například přidávají funkce, mění chování nebo umožňují přístup k novým online službám.
Při prvním spuštění [!INCLUDE [d365fin](includes/d365fin_md.md)], jsou pro vás již některá rozšíření nainstalována. Postupem času vám budou k dispozici další rozšíření a poté si můžete vybrat, zda chcete rozšíření použít nebo ne.

Společnost Microsoft například poskytuje rozšíření, které zajišťuje integraci s PayPal Payments Standard. Toto rozšíření je nainstalováno ve výchozím nastavení.
Pokud je však k dispozici další rozšíření, které nabízí integraci s jinou platební službou, můžete nainstalovat nové rozšíření a poté zvolit, kterou z těchto dvou služeb použít.  

Rozšíření spravujete v okně **Správa rozšíření**. Na tuto okno se dostanete z Domovské stránky. Případně vyberte ikonu **Hledat stránku nebo sestavu** ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), v pravém horním rohu zadejte **Rozšíření**, a poté vyberte související odkaz.  

> [!NOTE]  
>   Pokud si myslíte, že byste měli mít přístup k rozšíření, ale nemůžete ho najít, podívejte se na okno **Správa rozšíření** - pokud zde rozšíření není uvedeno, můžete jej nainstalovat podle popisu v následující části.  

## <a name="installing-an-extension"></a>Instalace Rozšíření
Nová rozšíření můžete získat z tržiště na adrese [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1). Zde si můžete prohlédnout všechna dostupná rozšíření pro [!INCLUDE [d365fin](includes/d365fin_md.md)] a získat aplikace, rozšíření a balíčky obsahu pro další produkty společnosti Microsoft. Nastavte příslušné filtry, podívejte se na informace o jednotlivých rozšířeních a získejte rozšíření pro své [!INCLUDE [d365fin](includes/d365fin_md.md)].  
> [!NOTE]
>   Přihlaste se na [AppSource.microsoft.com](https://appsource.microsoft.com/) pomocí e-mailového účtu, který používáte pro [!INCLUDE [d365fin](includes/d365fin_md.md)]. Použijte stejný e-mailový účet pro další služby a produkty pro bezproblémový provoz.  

Na marketplace se také můžete dostat z [!INCLUDE [d365fin](includes/d365fin_md.md)]. V okně **Správa rozšíření**  vidíte rozšíření, která jsou aktuálně nainstalována, a můžete otevřít stránku**Rozšíření Tržiště**, která zobrazuje [!INCLUDE [d365fin](includes/d365fin_md.md)] rozšíření, která jsou aktuálně dostupná v AppSource. Pokud zvolíte odkaz *Více aplikací*, budete přesměrováni na [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).  

Pokud zvolíte rozšíření, můžete si přečíst, co rozšíření dělá, a můžete získat další nápovědu k tomuto rozšíření. Pokud se rozhodnete pro rozšíření, musíte souhlasit s podmínkami použití. Pokud rozšíření získáte z webu AppSource, budete přihlášeni do [!INCLUDE [d365fin](includes/d365fin_md.md)] pro dokončení instalace.  

Když nainstalujete rozšíření, budete jej možná muset nastavit, například zadat účet pro použití s rozšířením **PayPal Payments standard pro [!INCLUDE [d365fin](includes/d365fin_md.md)]**.
Jiná rozšíření jednoduše přidají pole na existující stránku nebo například přidají novou stránku.   

Pokud rozšíření odinstalujete a poté změníte názor, můžete jej znovu nainstalovat. Když odinstalujete rozšíření, které jste používali, budou data zachována, takže pokud rozšíření znovu nainstalujete, budou vaše data stále k dispozici.  

Některá rozšíření jsou poskytována společností Microsoft a jiná rozšíření poskytována [jinými společnostmi](ui-extensions-other.md). Všechna rozšíření jsou testována před tím, než jsou dostupná, doporučujeme vám však přistoupit k odkazům, které jsou s každým rozšířením k dispozici, abyste se o rozšíření dozvěděli více, než se rozhodnete jej nainstalovat.  

Společnost Microsoft poskytuje následující rozšíření:  

* [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md)  
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)  
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)  
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)  
* [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md)  
* [Sales and Inventory Forecast](ui-extensions-sales-forecast.md)  
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)  
* [Quickbooks Payroll File Import](ui-extensions-quickbooks-payroll.md)  
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)  
* [GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)  
* [QuickBooks Online Data Migration](ui-extensions-quickbooks-online-data-migration.md)  
* [Accountant Portal](ui-extensions-accountant-portal.md)  
* [Image Analyzer](ui-extensions-image-analyzer.md)  
* [Payments and Reconciliations (DK)](ui-extensions-payments-reconciliation-formats-dk.md)  
* [C5 Data Migration](ui-extensions-c5-data-migration.md)  
* [Essential Business Insights](ui-extensions-essential-business-insights.md)  

> [!NOTE]  
>  Nová rozšíření nejsou v AppSource dostupná ihned po oznámení aktualizace. Rozšíření můžete sledovat na [AppSource.microsoft.com](https://appsource.microsoft.com/en-us/marketplace/apps?product=dynamics-365%3Bdynamics-365-for-financials&page=1).

## <a name="see-also"></a>Viz také
[Nastavení služby Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Povolení plateb zákazníkům prostřednictvím služby PayPal](sales-how-enable-payment-service-extensions.md)  
[Migrace obchodních dat z Jiných Finančních Systémů](across-import-data-configuration-packages.md)  
[Nastavení rozšíření GetAddress.io UK Postal Code](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Rozšíření od jiných poskytovatelů](ui-extensions-other.md)  
[Vítejte v [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

## [!INCLUDE [d365fin](includes/free_trial_md.md)]  
## [!INCLUDE [d365fin](includes/training_link_md.md)]
