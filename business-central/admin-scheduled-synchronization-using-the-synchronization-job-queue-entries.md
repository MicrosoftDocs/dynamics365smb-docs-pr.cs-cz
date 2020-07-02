---
title: Synchronizing Business Central and Dynamics 365 Sales | Microsoft Docs
description: Learn about synchronizing data between Business Central and Dynamics 365 Sales.
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

# Plánování synchronizace mezi Business Central a Dynamics 365 for Sales
Můžete synchronizovat [!INCLUDE[d365fin](includes/d365fin_md.md)] s [!INCLUDE[crm_md](includes/crm_md.md)] v naplánovaných intervalech nastavením úloh ve frontě úloh. Synchronizační úlohy synchronizují data v záznamech [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)], které byly dříve spojeny dohromady. Nebo u dosud nespojených záznamů, v závislosti na směru a pravidlech synchronizace mohou úlohy synchronizace vytvářet a spojovat nové záznamy v cílovém systému. Existuje hned několik synchronizačních úloh, které jsou k dispozici hned po spustení. Můžete je zobrazit na stránce **Položky fronty úloh**. Pro více informací navštivte [Použití fronty úloh na plánování úloh](admin-job-queues-schedule-tasks.md).
<!--
> [!Note]
> For the on-premeses version of [!INCLUDE[d365fin](includes/d365fin_md.md)], the synchronization jobs are run by codeunit **5339 Integration synch Job Runner**.-->

## Proces synchronizace
Každý záznam fronty synchronizační úlohy používá specifické mapování integrační tabulky, které určuje, která tabulka [!INCLUDE[d365fin](includes/d365fin_md.md)] a entita [!INCLUDE[crm_md](includes/crm_md.md)] se synchronizuje. Mapování tabulek také obsahuje některá nastavení, která řídí, které záznamy v tabulce [!INCLUDE[d365fin](includes/d365fin_md.md)] a entitě [!INCLUDE[crm_md](includes/crm_md.md)] se synchronizují.

Pro synchronizaci dat musí být záznamy entity [!INCLUDE[crm_md](includes/crm_md.md)] spojeny se záznamy [!INCLUDE[d365fin](includes/d365fin_md.md)]. Například zákazník [!INCLUDE[d365fin](includes/d365fin_md.md)] musí být spojen s účtem [!INCLUDE[crm_md](includes/crm_md.md)]. Spojky můžete nastavit ručně, před spuštěním synchronizačních úloh, nebo nechat synchronizační úlohy nastavit spojky automaticky. Následující seznam popisuje, jak jsou data synchronizována mezi [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)] , když používáte záznamy ve frontě synchronizačních úloh. Pro více informací navštivte [Manuální párování a synchronizace záznamů](admin-how-to-couple-and-synchronize-records-manually.md).

- Zaškrtávací políčko **Synchronizovat  pouze spárované záznamy** určuje, zda se při synchronizaci vytvoří nové záznamy. Ve výchozím nastavení je políčko zaškrtnuto, což znamená, že budou synchronizovány pouze propojené záznamy. V mapování integrační tabulky můžete změnit mapování tabulky mezi entitou [!INCLUDE[crm_md](includes/crm_md.md)] a tabulkou [!INCLUDE[d365fin](includes/d365fin_md.md)] tak, aby integrační synchronizační úlohy vytvořili nové záznamy v cílové databázi pro každý záznam ve zdrojové databázi, který není spojen. Pro více informací navštivte [Vytvoření nových záznamů](admin-how-to-modify-table-mappings-for-synchronization.md).

   **Příklad**
Pokud zrušíte zaškrtávací políčko **Synchronizovat  pouze spárované záznamy**, když synchronizujete zákazníky v [!INCLUDE[d365fin](includes/d365fin_md.md)] s účty v [!INCLUDE[crm_md](includes/crm_md.md)], vytvoří se nový účet pro každého zákazníka v [!INCLUDE[d365fin](includes/d365fin_md.md)] a je automaticky spojen. Navíc vzhledem k tomu, že synchronizace je v tomto případě obousměrná, je nový zákazník vytvořen a spojen pro každý účet [!INCLUDE[crm_md](includes/crm_md.md)], který ještě není spojen.

   > [!NOTE]
   > Existují pravidla a filtry, které určují, jaká data jsou synchronizována. Pro více informací navštivte [Synchronizační pravidla](admin-synchronizing-business-central-and-sales.md).

- Když jsou nové záznamy vytvořeny v [!INCLUDE[d365fin](includes/d365fin_md.md)], záznamy používají buď šablonu, která je definována pro mapování integrační tabulky, nebo výchozí šablonu, která je k dispozici pro typ záznamu. Pole jsou vyplněna údaji z [!INCLUDE[d365fin](includes/d365fin_md.md)] nebo [!INCLUDE[crm_md](includes/crm_md.md)] v závislosti na směru synchronizace. Pro více informací navštivte [Úprava mapování tabulek pro synchronizaci](admin-how-to-modify-table-mappings-for-synchronization.md).

- S následnou synchronizací budou aktualizovány pouze záznamy, které byly změněny nebo přidány po poslední úspěšné synchronizační úloze pro entitu.

   Nové záznamy v [!INCLUDE[crm_md](includes/crm_md.md)] se přidají do [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pokud se data v polích v záznamech [!INCLUDE[crm_md](includes/crm_md.md)] změnila, data se zkopírují do odpovídajícího pole v [!INCLUDE[d365fin](includes/d365fin_md.md)].

- Při obousměrné synchronizaci se úloha synchronizuje z [!INCLUDE[d365fin](includes/d365fin_md.md)] na [!INCLUDE[crm_md](includes/crm_md.md)] a poté z [!INCLUDE[crm_md](includes/crm_md.md)] na [!INCLUDE[d365fin](includes/d365fin_md.md)].

## Výchozí položky fronty synchronizace úloh
Následující tabulka popisuje výchozí synchronizační úlohy.

| Položka fronty úloh | Popis | Směr | Mapování tabulky integrace | Výchozí synchronizační frekvence (min) | Výchozí doba nečinnosti (min) |
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
| Úloha synchronizace Kontakt - Dynamics 365 for Sales | Synchronizuje kontakty [!INCLUDE[crm_md](includes/crm_md.md)] s kontakty [!INCLUDE[d365fin](includes/d365fin_md.md)]. | Obousměrný | Kontakt | 30 | 720 <br>(12 hodin) |
| Úloha synchronizace Měny transakce - Dynamics 365 for Sales | Synchronizuje měny transakcí [!INCLUDE[crm_md](includes/crm_md.md)] s něnami [!INCLUDE[d365fin](includes/d365fin_md.md)]. | Z [!INCLUDE[d365fin](includes/d365fin_md.md)] do [!INCLUDE[crm_md](includes/crm_md.md)] | Měna | 30 | 720 <br> (12 hodin) |
| Úloha synchronizace Zákazník - Dynamics 365 for Sales | Synchronizuje účty [!INCLUDE[crm_md](includes/crm_md.md)] se zákazníky [!INCLUDE[d365fin](includes/d365fin_md.md)]. | Obousměrný | Zákazník | 30 | 720<br> (12 hodin) |
| Úloha synchronizace Cenové skupiny zákazníka - Dynamics 365 for Sales | Synchronizuje prodejní ceníky [!INCLUDE[crm_md](includes/crm_md.md)] s cenovými skupinami zákazníka [!INCLUDE[d365fin](includes/d365fin_md.md)]. |  | Cenové skupiny zákazníka-Prodejní ceníky | 30 | 1440<br> (24 hod.) |
| Úloha synchronizace Zboží - Produkt - Dynamics 365 for Sales | Synchronizuje produkty [!INCLUDE[crm_md](includes/crm_md.md)] se zbožím [!INCLUDE[d365fin](includes/d365fin_md.md)]. | Z [!INCLUDE[d365fin](includes/d365fin_md.md)] do [!INCLUDE[crm_md](includes/crm_md.md)] | Zboží-Produkt | 30 | 1440<br> (24 hod.) |
| Úloha synchronizace Účtované prodejní faktury-Faktury - Dynamics 365 for Sales | Synchronizuje faktury [!INCLUDE[crm_md](includes/crm_md.md)] s účtovanými prodejními fakturami [!INCLUDE[d365fin](includes/d365fin_md.md)]. | Z [!INCLUDE[d365fin](includes/d365fin_md.md)] do [!INCLUDE[crm_md](includes/crm_md.md)] | Faktury-Účtované prodejní faktury | 30 | 1440<br> (24 hod.) |
| Úloha synchronizace Zdroj-produkt - Dynamics 365 for Sales | Synchronizuje produkty [!INCLUDE[crm_md](includes/crm_md.md)] se zdroji [!INCLUDE[d365fin](includes/d365fin_md.md)]. | Z [!INCLUDE[d365fin](includes/d365fin_md.md)] do [!INCLUDE[crm_md](includes/crm_md.md)] | Zdroj-Produkt | 30 | 720<br> (12 hodin) |
| Úloha synchronizace Prodejci - Dynamics 365 for Sales | Synchronizuje prodejce [!INCLUDE[d365fin](includes/d365fin_md.md)] s uživateli [!INCLUDE[crm_md](includes/crm_md.md)]. | Z [!INCLUDE[crm_md](includes/crm_md.md)] do [!INCLUDE[d365fin](includes/d365fin_md.md)] | Prodejci | 30 | 1440<br> (24 hod.) |
| Úloha synchronizace Prodejní cena-Ceny produktu - Dynamics 365 for Sales | Synchronizuje ceny produktů [!INCLUDE[crm_md](includes/crm_md.md)] s prodejními cenami [!INCLUDE[d365fin](includes/d365fin_md.md)]. | Ceny produktu-Prodejní cena | 30 | 1440<br> (24 hod.) |
| Úloha synchronizace Měrná jednotka - Dynamics 365 for Sales | Synchronizuje skupiny jednotek [!INCLUDE[crm_md](includes/crm_md.md)] s měrnými jednotkami [!INCLUDE[d365fin](includes/d365fin_md.md)]. | Z [!INCLUDE[d365fin](includes/d365fin_md.md)] do [!INCLUDE[crm_md](includes/crm_md.md)] | Měrná jednotka | 30 | 720<br> (12 hodin) |
| Úloha synchronizace Statistika zákazníka - Dynamics 365 for Sales | Aktualizuje účty [!INCLUDE[crm_md](includes/crm_md.md)] s nejnovějšími [!INCLUDE[d365fin](includes/d365fin_md.md)] zákaznickými daty. V [!INCLUDE[crm_md](includes/crm_md.md)] se tato informace objeví ve **Statistice účtu Business Central** ve formě rychlého zobrazení účtů, které jsou propojeny se zákazníky [!INCLUDE[d365fin](includes/d365fin_md.md)].<br /><br /> Tato data lze také ručně aktualizovat z každého záznamu zákazníka. Pro více informací navštivte [Manuální párování a synchronizace záznamů](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Note:**  Tato položka fronty úloh je relevantní pouze v případě, že [!INCLUDE[d365fin](includes/d365fin_md.md)] integrační řešení je nainstalováno v [!INCLUDE[crm_md](includes/crm_md.md)]. Pro více informací, navštivte [Integrační řešení Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md). | Nelze použít | Nelze použít | 30 | Nelze použít |

## Časový limit nečinnosti
Některé položky ve frontě úloh, například ty, které plánují synchronizaci mezi [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)], používají pole **Časový limit nečinnosti** na kartě Položka fronty úloh, aby zabránili zbytečnému spuštění fronty úloh.
<br><br>

> ![Vývojový diagram pro uložení položek fronty úloh v důsledku nečinnosti](media/on-hold-with-inactivity-timeout.png)

Pokud hodnota v tomto poli není nula a fronta úloh nenalezla během posledního spuštění žádné změny, [!INCLUDE[d365fin](includes/d365fin_md.md)] pozastaví zadání fronty úloh. Když k tomu dojde, pole **Stav fronty úloh** zobrazí **Blokování z důvodu nečinnosti** a [!INCLUDE[d365fin](includes/d365fin_md.md)] bude čekat po dobu zadanou v poli **Časový limit nečinnosti** před tím, než znovu spustí záznam fronty úloh.

Například ve výchozím nastavení bude položka fronty úloh Měna, která synchronizuje měny v [!INCLUDE[crm_md](includes/crm_md.md)] s směnnými kurzy v [!INCLUDE[d365fin](includes/d365fin_md.md)], hledat změny směnných kurzů každých 30 minut. Pokud nejsou nalezeny žádné změny, [!INCLUDE[d365fin](includes/d365fin_md.md)] pozastaví zadání fronty úloh Měna na 720 minut (šest hodin). Pokud se změní kurz v [!INCLUDE[d365fin](includes/d365fin_md.md)] zatímco je položka fronty úloh pozastavena, [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky znovu aktivuje zadání fronty úloh a fronta úloh se restartujte.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky aktivuje položky fronty úloh, které jsou pozastaveny, pouze pokud dojde ke změnám v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Změny v [!INCLUDE[crm_md](includes/crm_md.md)] nebudou aktivovat položky fronty úloh.

## Zobrazení protokolu synchronizační úlohy
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Integrace synchronizační úlohy** a poté vyberte související odkaz.
2. Pokud pro synchronizační úlohu došlo k jedné nebo více chybám, objeví se ve sloupci  **Chyba** počet chyb. Chcete-li zobrazit chyby úlohy, zvolte číslo.

   > [!TIP]
   > Všechny chyby synchronizační úlohy můžete zobrazit přímým otevřením protokolu chyb synchronizační úlohy.

## Zobrazení protokolu synchronizace úloh z mapování tabulky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Mapování tabulky integrace** a poté vyberte související odkaz.
2. Na stránce **Mapování tabulky integrace** vyberte položku a pak zvolte **Protokol synchronizační  úlohy integrace**.

## Zobrazení protokolu chyb synchronizace
* Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Chyby synchronizace integrace** a poté vyberte související odkaz.

## Viz také
[Synchronizace dat v Business Central a Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)  
[Ruční synchronizace mapování tabulek](admin-manual-synchronization-of-table-mappings.md)  
[Plánování synchronizace mezi  Business Central a Dynamics 365 for Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
[Integrace Dynamics 365 Business Central s Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
