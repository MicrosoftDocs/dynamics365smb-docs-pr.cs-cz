---
title: Použití rozšíření QuickBooks Migration | Microsoft Docs
description: 'Popisuje, jak používat rozšíření k migraci zákazníků, dodavatelů, zboží a účtů z QuickBooks Online do Business Central.'
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'extension, migrate, data, QuickBooks, import'
ms.date: 05/24/2017
ms.author: bholtorf
---

# <a name="the-quickbooks-online-data-migration-extension-for-business-central"></a>Rozšíření Quickbooks Online Data Migration pro Business Central
Toto rozšíření je zahrnuto v Průvodci asistovaného nastavení **migrace dat**, který vám pomůže při migraci důležitých obchodních dat z QuickBooks Online do [!INCLUDE [d365fin](includes/d365fin_md.md)]. To je užitečné například v době, kdy vaše firma roste, a tak jste se rozhodli upgradovat aplikaci pro správu firmy a začali jste používat [!INCLUDE [d365fin](includes/d365fin_md.md)].

## <a name="what-data-can-i-import-from-quickbooks-online"></a>Jaké data mohu importovat z QuickBooks Online?
Z QuickBooks Online můžete do [!INCLUDE [d365fin](includes/d365fin_md.md)]importovat následující data:  

* Zákazníci
* Dodavatelé
* Zboží
* Účetní osnova
* Počáteční zůstatky v hlavní knize
* Dostupné množství skladových položek
* Otevřené dokumenty pro zákazníky a dodavatele, jako faktury, dobropisy a platby

Migrujeme pouze plnou částku v prodejních a nákupních fakturách. Neaktualizujeme částečně zaplacené částky. Například, jestliže zákazník zaplatil 300, z celkových 500 korun na prodejní faktuře, migrujeme celých 500. Jestli jste obdrželi částečnou platbu, tak ji musíte aktualizovat manuálně, buď před, nebo po migraci dat. Doporučujeme abyste před migrací použili neuhrazené transakce, aby bylo možné později věci zjednodušit.

> [!NOTE]  
>   Nemigrujeme nákupní a prodejní objednávky.

## <a name="before-you-start"></a>Než začnete
Důležitá část migračního procesu je specifikovat účty, do kterých budou transakce migrovat. Je dobrý nápad si toto mapování naplánovat před migrací dat. Například, účty, ve kterých zúčtujete transakce pro:  

* Prodej zboží a služeb odběratelům
* Nákup zboží a služeb od dodavatelů  
* Opravné položky v hlavní knize  

[!INCLUDE [d365fin](includes/d365fin_md.md)] vyžaduje, aby měly účty v hlavní knize přiřazené čísla účtů. Ujistěte se, že čísla účtů jsou přiřazená k vašemu účtu v QuickBooks.

Pokud mají transakce v aplikaci QuickBooks Online daňové částky, musíte před zaúčtováním transakcí vytvořit daňový účet pro vaše daňové kompetence v aplikaci [!INCLUDE [d365fin](includes/d365fin_md.md)].

## <a name="how-do-i-start-using-the-extension"></a>Jak začnu používat rozšíření?
Začít je snadné. Stačí spustit Průvodce asistovaného nastavení **migrace dat**. Zde je návod:

1. Zvolte ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo ikonu sestavy"), zadejte ** Asistovaná nastavení ** a pak vyberte **Migrovat obchodní data**.
2. Postupujte podle instrukcí k jednotlivým krokům v asistovaném průvodci nastavením.

## <a name="what-do-i-do-after-i-migrate-data"></a>Co mám dělat po migraci dat?
Po migraci dat mají transakce stav **Nezveřejněno**, takže je můžete zkontrolovat a provést úpravy. Pokud chcete transakce zkontrolovat, přejděte na stránku, kde je obvykle najdete. Chcete-li například zkontrolovat nezveřejněné prodejní faktury, přejděte na stránku **Prodejní faktury**. Jestli chcete zkontrolovat deníky plateb, přejděte na stránku **Deníky plateb**.   

Je zde několik věcí, které by jste měli zejména udělat:

* Pokud transakce v aplikaci QuickBooks Online měly přirážku, nebo slevu, musíte je před zaúčtováním manuálně přidat do souvisejících transakcí v [!INCLUDE [d365fin](includes/d365fin_md.md)].
* Pokud jste plátci DPH, budete možná muset do nastavení účtování přidat Obchodní účetní skupinu a Účetní skupinu zboží, abyste mohli účtovat DPH.
* Ověřte počáteční stavy pro účty v hlavní knize. QuickBooks Online neukládá aktuální stavy všech účtů, takže budete pravděpodobně muset opravit počáteční stavy.

## <a name="see-also"></a>Viz také
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] Pomocí rozšíření](ui-extensions.md)  
