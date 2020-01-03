---
title: Použití rozšíření QuickBooks Migration | Microsoft Docs
description: 'Popisuje jak používat rozšíření k importaci zákazníků, dodavatelů, zboží a účtů z QuickBooks Desktop do Business Central.'
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'app, add-in, manifest, customize, import, implement'
ms.date: 10/01/2018
ms.author: edupont
---

# <a name="the-quickbooks-data-migration-extension"></a>Rozšíření QuickBooks Data Migration
Toto rozšíření usnadňuje migraci zákazníků, dodavatelů, zboží a účtů z QuickBooks na [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pokud vaše firma používá QuickBooks, můžete exportovat příslušné informace skrz průvodce asistovaného nastavení a poté data uložit do [!INCLUDE[d365fin](includes/d365fin_md.md)].  
Pro více informací navštivte [Import obchodních dat z jiných finančních systémů](across-import-data-configuration-packages.md).

## <a name="data-from-quickbooks-desktop"></a>Data z QuickBooks Desktop
 
Z QuickBooks Online můžete do Business Central importovat následující data:

- Zákazníci  
- Dodavatelé  
- Zboží  
- Účetní osnova  
- Počáteční zůstatky v hlavní knize  
- Dostupné množství skladových položek  
- Otevřené dokumenty pro zákazníky a dodavatele, jako faktury, dobropisy a platby  

Migrujeme pouze plnou částku v prodejních a nákupních fakturách. Neaktualizujeme částečně zaplacené částky. Například, jestliže zákazník zaplatil 300, z celkových 500 korun na prodejní faktuře, migrujeme celých 500. Jestli jste obdrželi částečnou platbu, tak ji musíte aktualizovat manuálně, buď před, nebo po migraci dat. Doporučujeme abyste před migrací použili neuhrazené transakce, aby bylo možné později věci zjednodušit.

> [!NOTE]
> Nemigrujeme nákupní a prodejní objednávky.

## <a name="before-you-start"></a>Než začnete
Důležitá část migračního procesu je specifikovat účty, do kterých budou transakce migrovat. Je dobrý nápad si toto mapování naplánovat před migrací dat. Například, účty, ve kterých zúčtujete transakce pro:

- Prodej zboží a služeb odběratelům  
- Nákup zboží a služeb od dodavatelů  
- Opravné položky v hlavní knize  

Business Central vyžaduje, aby měly účty v hlavní knize přiřazené čísla účtů. Ujistěte se, že čísla účtů jsou přiřazená k vašemu účtu v QuickBooks.
Pokud mají transakce v aplikaci QuickBooks částky daně, musíte před zaúčtováním transakcí vytvořit daňový účet pro vaše daňové kompetence v aplikaci Business Central.

Chcete-li získat data z desktopové aplikace QuickBooks, bude nutné stáhnout nástroj Microsoft Data Exporter Tool.  Pokyny pro nástroj jsou v Průvodci migrací dat v [!INCLUDE[d365fin](includes/d365fin_md.md)] Nástroj se připojí k vaší aplikaci QuickBooks a exportuje příslušná data do souboru .zip.  

> [!NOTE]
> Nástroj pro export dat funguje v současné době pouze s QuickBooks 2017 a 2018.

## <a name="finding-the-quickbooks-data-migration-extension"></a>Vyhledání rozšíření QuickBooks Data Migration
Rozšíření QuickBooks Data Migration je nainstalováno a připraveno k použítí jako integrovaná část asistovaného průvodce nastavením Data Migration. Pokud jste připraveni začít hned teď a exportovali jste svá data z QuickBooks, vyberte ikonu ![ Žárovka, která otevře Řekněte mi funkci](media/ui-search/search_small.png "Řekněte mi co chcete udělat"), zadejte **Asistované nastavení** a poté vyberte související odkaz. Vyberte možnost **Migrovat obchodní data** a poté postupujte podle pokynů v průvodci.  

## <a name="what-do-i-do-after-i-migrate-data"></a>Co mám dělat po migraci dat?
Po migraci dat mají transakce stav Nezveřejněno, takže je můžete zkontrolovat a provést úpravy. Pokud chcete transakce zkontrolovat, přejděte na stránku, kde je obvykle najdete. Chcete-li například zkontrolovat nezveřejněné prodejní faktury, přejděte na stránku Prodejní faktury. Jestli chcete zkontrolovat deník plateb, přejděte na stránku Deník plateb.
Je zde několik věcí, které by jste měli zejména udělat: Pokud transakce v aplikaci QuickBooks měly přirážku nebo slevu, je nutné je před zaúčtováním manuálně přidat do souvisejících transakcí v aplikaci Business Central.
Pokud jste plátci DPH, budete možná muset do nastavení účtování přidat Obchodní účetní skupinu a Účetní skupinu zboží, abyste mohli účtovat DPH.
Ověřte počáteční stavy pro účty v hlavní knize. QuickBooks neukládá aktuální stavy všech účtů, takže budete pravděpodobně muset opravit počáteční stavy.

## <a name="see-also"></a>Viz také
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] Pomocí rozšíření ](ui-extensions.md)  
