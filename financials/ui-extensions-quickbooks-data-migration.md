---
title: Použití rozšíření QuickBooks Migration | Microsoft Docs
description: 'Popisuje jak používat rozšíření k importaci zákazníků, dodavatelů, zboží a účtů z QuickBooks Desktop do Business Central.'
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'app, add-in, manifest, customize, import, implement'
ms.date: 03/29/2017
ms.author: edupont
---
# <a name="the-quickbooks-data-migration-extension-for-business-central"></a>Rozšíření Quickbooks Data Migration pro Business Central
Toto rozšíření usnadňuje migraci zákazníků, dodavatelů, zboží a účtů z QuickBooks na [!INCLUDE [d365fin](includes/d365fin_md.md)]. Pokud vaše firma používá QuickBooks, můžete exportovat příslušné informace skrz průvodce asistovaného nastavení a poté data uložit do [!INCLUDE [d365fin](includes/d365fin_md.md)].  
Pro více informací navštivte [Import obchodních dat z jiných finančních systémů](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-quickbooks-desktop"></a>Exportování dat z QuickBooks Desktop
Musíte exportovat některé nebo všechny vaše stávající zákazníky, dodavatele, skladové položky a účty do souboru Intuit Interchange Format (IIF). Rozšíření migrace dat QuickBooks obsahuje výchozí mapování dat QuickBooks, takže můžete použít vaše stávající data k testování vaší nové [!INCLUDE [d365fin](includes/d365fin_md.md)]společnosti. Ve většině případů bude výchozí mapování dostatečné, ale mapování můžete změnit v průvodci asistovaného nastavení.  
V QuickBooks, nabídka Soubor obsahuje nástroj pro export seznamů. Pro účely [!INCLUDE [d365fin](includes/d365fin_md.md)] můžete exportovat následující seznamy:

* Seznam zákazníků  
* Seznam dodavatelů  
* Seznam zboží  
* Seznam účtů  

Exportovaná data jsou uložena jako IIF soubor a poté nahrána do [!INCLUDE [d365fin](includes/d365fin_md.md)].

## <a name="finding-the-quickbooks-data-migration-extension"></a>Vyhledání rozšíření QuickBooks Data Migration
Rozšíření QuickBooks Data Migration je nainstalováno a připraveno k použítí jako integrovaná část asistovaného průvodce nastavením Data Migration. Pokud jste připraveni začít hned teď a exportovali jste svá data z QuickBooks, zvolte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "Hledat stránku nebo ikonu sestavy"), zadejte **Asistované nastaven**í a poté vyberte související odkaz. Vyberte možnost **Migrovat obchodní data** a poté postupujte podle pokynů v průvodci.  

## <a name="see-also"></a>Viz také
[Import obchodních dat z jiných finančních systémů.](upload-data.md)  
[Přizpůsobení [!INCLUDE [d365fin](includes/d365fin_md.md)] Pomocí rozšíření ](ui-extensions.md)  
