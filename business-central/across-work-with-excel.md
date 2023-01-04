---
title: Viewing and Editing in Excel From Business Central (contains video)
description: Learn about how you can open the pages in Microsoft Excel from Business Central for better data analysis.
author: jswymer

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer

---
# Zobrazení a úpravy v aplikaci Excel

Se stránkami, které zobrazují seznam záznamů v řádcích a sloupcích, jako je seznam zákazníků, prodejních objednávek nebo faktur, můžete seznam exportovat do aplikace Microsoft Excel a zobrazit jej tam. V závislosti na stránce máte dvě možnosti zobrazení v aplikaci Excel. Obě možnosti jsou k dispozici z ikony **Sdílet** ![Stránku sdílet v jiné aplikaci](media/share-icon.png) V horní části stránky. Na stránce můžete vybrat akci **Otevřít v Excelu** nebo **Upravit v Excelu**. Tento článek vysvětluje rozdíly mezi těmito dvěma akcemi.

## Otevřít v aplikaci Excel

Pomocí akce **Otevřít v aplikaci Excel** můžete provádět změny záznamů v aplikaci Excel, ale nemůžete publikovat změny zpět do [!INCLUDE[prod_short](includes/prod_short.md)]. Změny můžete uložit pouze do souboru aplikace Excel, aniž by to ovlivnilo data v [!INCLUDE[prod_short](includes/prod_short.md)].

- Pomocí této akce aplikace Excel respektuje všechny filtry na stránce, které omezují zobrazené záznamy. Sešit aplikace Excel bude obsahovat stejné řádky a sloupce, které se zobrazí na stránce v [!INCLUDE[prod_short](includes/prod_short.md)].

- Tato akce funguje na Windows i MacOS.

- Počínaje aktualizací 18.3 můžete také zobrazit seznamy, které jsou zobrazeny v částech stránky, jako jsou řádky v prodejní objednávce.

> [!NOTE]
> Pro místní [!INCLUDE[prod_short](includes/prod_short.md)] je ve výchozím nastavení k dispozici akce **Otevřít v Excelu**. Pokud však nastavíte [!INCLUDE[prod_short](includes/prod_short.md)] místně pro úpravy dat v Excelu, pak se akce **Otevřít v Excelu** nahradí akcí **Upravit v Excelu**.

[!INCLUDE [send-report-excel](includes/send-report-excel.md)]

## Úprava v aplikaci Excel

Akce **Upravit v Excelu** je dostupná u většiny seznamů, ale ne u všech. Pomocí akce **Upravit v aplikaci Excel** provedete změny záznamů v aplikaci Excel a poté publikujete změny zpět do [!INCLUDE[prod_short](includes/prod_short.md)]. Po otevření Excelu se na pravé straně zobrazí podokno **Doplněk Excelu**.

- Díky této akci Excel respektuje většinu filtrů na stránce, které omezují zobrazené záznamy, takže sešit aplikace Excel bude obsahovat téměř stejné záznamy a sloupce.

- Chcete-li získat nejnovější data z [!INCLUDE[prod_short](includes/prod_short.md)], zvolte **Aktualizovat** v podokně Doplněk aplikace Excel.

- Můžete přepnout společnost, se kterou pracujete. Chcete-li přepnout společnost, vyberte ikonu **Možnosti** ![možnosti doplňku aplikace Excel.](media/cogwheel.png " Možnosti doplňku aplikace Excel") v podokně Doplněk aplikace Excel a potom vyberte společnost z pole **Společnost**.

   > [!IMPORTANT]
   > Při změně společnosti se ujistěte, že pole **Prostředí** není prázdné. Pokud ano, nastavte ji na jednu z dostupných možností; v opačném případě nebude doplněk fungovat správně.

Pokud v doplňku provedete změny, je nutné jej znovu načíst, aby se aktualizovalo připojení. Chcete-li znovu načíst, použijte ![nabídku doplňku aplikace Excel](media/excel-addin-menu.png "nabídku doplňku aplikace Excel") nabídka v pravém horním rohu doplňku. Pokud se vám nedaří načíst doplněk, obraťte se na svého správce. Pokud jste správcem, přečtěte si téma [Získání doplňku Business Central pro Excel](admin-deploy-excel-addin.md).

> [!NOTE]
> Doplněk funguje s Excelem pro web (online) z jakéhokoli zařízení, pokud používáte podporovaný prohlížeč. Funguje také s aplikací Excel pro Windows (PC); ale ne pro macOS.
>
> Pro místní [!INCLUDE[prod_short](includes/prod_short.md)] je akce **Upravit v Excelu** k dispozici pouze v případě, že doplněk aplikace Excel nakonfiguroval váš správce, a je k dispozici pouze pro Webový klient. Pro správce, pokud se chcete dozvědět, jak nainstalovat doplněk aplikace Excel, přečtěte si téma [Nastavení doplňku aplikace Excel pro úpravu dat Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).


<!-- Note for later: here we're immediately jumping to pretty advanced topics like changing company or reloading the addin. Fine to keep them for now. In the future, we will first need to explain in more detail the actual functionality of the addin, primarily these sub-sections:

Refreshing record data in Excel
Editing and publishing back to Business Central
Creating new records from Excel
Crafting your own editable Excel.
Point (4) is where it gets interesting for changing/specifying company, environment and other connection settings-->

### První přihlášení

Akce **Upravit v aplikaci Excel** vyžaduje, aby byl doplněk Business Central nainstalován v aplikaci Excel. V některých případech může váš správce nastavit, aby se doplněk automaticky nainstaloval za vás. V tomto případě se stačí přihlásit k Business Central v podokně **doplňku aplikace Excel** pomocí vašeho uživatelského jména a hesla. Jinak se otevře podokno **Nový doplněk Office**. Pokud chcete doplněk nainstalovat, zvolte **Důvěřovat tomuto doplňku**, který nainstaluje doplněk přímo z Office Store.

Pokud se doplněk z nějakého důvodu nenainstaluje, kontaktujte svého správce nebo jej zkuste nainstalovat ručně. Další informace naleznete v části [Ruční instalace doplňku pro vlastní použití](admin-deploy-excel-addin.md#install).

## Podívejte se na rozdíly mezi možnostmi
<br><br>

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## Podívejte se na související školení na webu [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Viz také

[Analýza účetní uzávěrky v aplikaci Microsoft Excel](finance-analyze-excel.md)    
[Práce s Business Central](ui-work-product.md)    
[Vylepšení integrace Excelu ve druhé vlně vydání 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]