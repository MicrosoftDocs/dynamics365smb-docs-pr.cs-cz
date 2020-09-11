---
title: Schedule jobs to run automatically | Microsoft Docs
description: Scheduled tasks are managed by the job queue. These jobs run reports and codeunits. You can set jobs to run one time, or on a recurring basis.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 04/01/2020
ms.author: edupont

---
# Použití fronty úloh k plánování úkolů
Fronta úloh v [!INCLUDE[d365fin](includes/d365fin_md.md)] možňuje uživatelům plánovat a spouštět konkrétní sestavy a codeunity. Můžete nastavit, aby se úlohy spouštěly jednorázově nebo opakovaně. Můžete například spustit sestavu **Prodejce - statistika prodeje** týdně, sledovat prodej podle prodejců každý týden, nebo můžete chtít spustit codeunitu **Zpracování e-mailů** denně, abyste se ujistili, že čekající e-mailové zprávy zákazníkům týkající se jejich servisních objednávek jsou odesílány včas.

Na stránce **Položky fronty úloh** jsou uvedeny všechny exitující úlohy. Pokud přidáte novou položku fronty úloh, kterou chcete naplánovat, musíte zadat informace o typu objektu, který chcete spustit, například sestava nebo codeunita, název a ID objektu. Můžete také přidat parametry k určení chování položky fronty úloh. Můžete například přidat parametr, který bude odesílat pouze zaúčtované prodejní objednávky. Musíte mít oprávnění ke spuštění konkrétní sestavy nebo procedury, jinak bude při spuštění položk fronty úloh vrácena chyba.

Fronta úloh může mít mnoho položek, což jsou úlohy, které fronta spravuje a spouští. Informace v položce určují, která codeunita nebo sestava se spouští, kdy a jak často se položka spouští, v jaké kategorii se úloha spouští a jak se spouští.

## Nastavení účtování na pozadí pomocí fronty úloh
Fronta úloh je účinným nástrojem pro plánování chodu obchodních procesů na pozadí, například když se více uživatelů pokouší zaúčtovat prodejní objednávky, ale současně lze zpracovat pouze jednu objednávku. Případně můžete naplánovat hodiny pro účtování, pokud je to pro vaši organizaci výhodné. Například ve vaší firmě může být smysluplné provádět určité rutiny, když většina procesů zadávání dat za daný den skončila.

Toho lze dosáhnout nastavením fronty úloh tak, aby spouštěla různé sestavy dávkového účtování, například  **Dávkové účtování prod. objednávek**, **Dávkové účtování prod. faktur**, **Dávkové účtování prod. obj. vratky** a **Dávkové účtování prod. dobropisů**. Pro více informací navštivte [Vytvoření položky fronty úloh pro zaúčtování prodejní objednávky na pozadí](admin-job-queues-schedule-tasks.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

[!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje účtování na pozadí pro všechny doklady prodeje, nákupu a servisu.

> [!NOTE]
> Některé úlohy mění stejná data a neměly by se spouštět současně, protože to může způsobit konflikty. Například úlohy na pozadí pro prodejní doklady se pokusí upravit stejná data současně. Kategorie fronty úloh pomáhají předcházet těmto konfliktům tím, že zajišťují, že při spuštění jedné úlohy se další úloha, která patří do stejné kategorie front úloh nespustí, dokud nedokončí. Například úloha, která patří do kategorie fronty prodejních úloh, bude čekat, dokud nebudou provedeny všechny ostatní úlohy související s prodejem. Kategorii fronty úloh určíte v záložce **Účtování na pozadí** na stránce **Nastavení prodeje a pohledávek**.
>
> [!INCLUDE[d365fin](includes/d365fin_md.md)]  obsahuje kategorie fronty úloh pro prodej, nákup a účtování hlavní knihy. Doporučujeme, abyste vždy určili jeden z nich nebo ten, který vytvoříte. Pokud dojde k selhání v důsledku konfliktů, zvažte nastavení kategorie pro všechno účtování prodeje, nákupu a hlavní knihy na pozadí.

Následující postup vysvětluje, jak nastavit účtování prodejních objednávek na pozadí. Kroky jsou podobné pro nákup a servis.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení prodeje a poheldávek** související odkaz.
2. Na stránce **Nastavení prodeje a pohledávek** vyberte políčko **Účtovat frontou úloh**.
3. Chcete-li filtrovat položky fronty úloh pro účtování prodejních objednávek, vyberte pole **Kód Kategorie fronty úloh** a vyberte kategorii **SalesPost**.

   Vytvoří se objekt fronty úlohy, codeunit 88 **Sales Post via Job Queue** je vytvořena Pokračujte povolením na stránce **Položky fronty úloh**.
4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky fronty úloh** a poté vyberte související odkaz.
5. Na stránce **Položky fronty úloh** vyberte tlačítko **Nový**.
6. V poli **Typ spoušteného objektu** vyberte **Procedura**.
7. V poli  **ID spouštěného objektu** vyberte  **88**. Titulek spouštěného objektu a popis zobrazí Sales Post via Job Queue.

   Pro tento scénář nejsou relevantní žádná další pole.
8. Vyberte talčítko **Nastavit stav na Připraveno**.
9. Chcete-li ověřit, zda fronta úloh funguje podle očekávání, zaúčtujte prodejní objednávku. Pro více informací navštivte [Prodej zboží](sales-how-sell-products.md).
10. Zkontrolujte na stránce **Položky protokolu fronty úloh** pokud byla prodejní objednávka úspěšně zaúčtována. Pro více informací navštivte [Zobrazení stavů nebo chyb ve frontě úloh ](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Pokud chcete, aby se při zaúčtování vytiskly prodejní doklady, zaškrtněte **Účto a tisk frontou úloh** na stránce **Nastavení prodeje a pohledávek**.

> [!IMPORTANT]  
> Pokud nastavíte úlohu, která bude účtovat a tisknout dokumenty a tiskárna zobrazí dialogové okno, například žádost o přihlašovací údaje nebo upozornění na nedostatek inkoustu v tiskárně, bude váš dokument zaúčtován, ale nevytisknut. Odpovídající záznam fronty úloh nakonec vyprší a pole **Status** se nastaví na **Chyba**. Proto doporučujeme nepoužívat nastavení tiskárny, které vyžaduje interakci se zobrazením dialogových oken tiskárny ve spojení s odesíláním na pozadí.

## Vytvoření položky fronty úlohy pro dávkové účtování prodejních objednávek
Následující postup ukazuje, jak nastavit sestavu **Dávkové účto prod.objednávek** na automatické zaúčtování vydaných prodejních objednávek v 16:00 hod v pracovních dnech týdne.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky fronty úloh** a poté vyberte související odkaz.
2. Zvolte tlačítko **Nový**.
3. V poli **Typ spoušteného objektu** vyberte **Procedura**.
4. V poli **ID spouštěného objektu** vyberte 296, **Dávkové účto prod.objednávek**.
5. Zaškrtněte políčko **Dialog sestavy**.
6. Na stránce **Dávkové účto prod.objednávek**, definujte, co je zahrnuto během automatického účtování prodejních objednávek, a pak zvolte tlačítko **OK**.
7. Zaškrtněte všechna políčka od **Spustit v pondělí** až **Spustit v pátek**.
8. Do pole **Počáteční čas** vložte 16:00.
9. Vyberte talčítko **Nastavit stav na Připraveno**.

Prodejní objednávky, které jsou připraveny k zaúčtování, budou nyní zaúčtovány každý den v týdnu v 16:00.

> [!NOTE]
> Pokud fronta úloh nemůže zaúčtovat prodejní objednávku, stav se změní na  **Chyba** prodejní objednávka se přidá do seznamu prodejních objednávek, které musí uživatel zpracovat ručně. Pro více informací navštivte [Zobrazení stavů nebo chyb ve frontě úloh](admin-job-queues-schedule-tasks.md#to-view-status-or-errors-in-the-job-queue).

Po nastavení a spuštění front úloh se stav může v každém opakujícím se období změnit takto:

* **Vyčkávat**
* **Připraveno**
* **Probíhá**
* **Chyba**
* **Dokončeno**

Po úspěšném dokončení je úloha odebrána ze seznamu položek fronty úloh, pokud se nejedná o opakovanou úlohu. Pokud se jedná o opakovanou úlohu, pole **Datum a čas prvního spuštění** se upraví tak, aby ukazovalo příští očekávané spuštění úlohy.

## Zobrazení stavu nebo chyb ve frontě úloh
Data, která jsou generována při spuštění fronty úloh, jsou uložena v databázi, takže můžete řešit chyby fronty úloh.

### Zobrazení stavu jakékoli úlohy
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky fronty úloh** a poté vyberte související odkaz.
2. Na stránce **Položky fronty úloh** vyberte položku ve frontě úloh a poté vyberte akci **Podrobnosti**.

### Zobrazení stavu z prodejního nebo nákupního dokladu
1. V dokladu, který jste se pokusili zaúčtovat pomocí fronty úloh, pole **Stav fronty úloh** bude obsahovat **Chybu**.
2. Zkontrolujte chybovou zprávu a problém vyřešte.

## Moje fronta úloh
Část **Moje fronta úloh** v Centru rolí zobrazuje položky front úloh, které jste zahájili, ale které ještě nejsou dokončeny. Ve výchozím nastavení není tato část viditelná, takže ji musíte přidat do Centra rolí. Pro více informací navštivte [Změna základního nastavení](ui-change-basic-settings.md).

Tato část zobrazuje, které doklady s vaším ID v poli **Přiřazené ID uživatele** jsou zpracovávány nebo zařazovány do fronty, včetně dokladů souvisejících s účtováním na pozadí. Část vám může na první pohled sdělit, zda došlo k chybě při zaúčtování dokladu nebo zda došlo k chybám v položce fronty úloh. Část také umožňuje zrušit zaúčtování dokladu, pokud není spuštěno.

### Zobrazení chyby z části Moje fronta úloh
1. U položky se stavem **Chyba** zvolte tlačítko **Zobrazit chybu**.
2. Zkontrolujte chybovou zprávu a problém vyřešte.

## Zabezpečení
Položky fronty úloh se spouští na základě oprávnění. Tato oprávnění musí umožnit spuštění sestavy nebo procedury.

Pokud je fronta úloh aktivována ručně, spustí se s pověřeními uživatele. Když je fronta úloh aktivována jako naplánovaná úloha, je spuštěna s pověřeními instance serveru. Při spuštění úlohy se spustí s pověřeními fronty úloh, která ji aktivuje. Uživatel, který vytvořil tuto položku fronty úloh, však musí mít také oprávnění. Pokud je úloha „spuštěna v relaci uživatele“ (například během účtování na pozadí), je spuštěna s přihlašovacími údaji uživatele, který ji vytvořil.

> [!IMPORTANT]  
> Pokud použijete sadu oprávnění SUPER, která je dodávána s [!INCLUDE[d365fin](includes/d365fin_md.md)], máte vy a vaši uživatelé oprávnění ke spuštění všech objektů. V tomto případě je přístup pro každého uživatele omezen pouze oprávněními k datům.

## Efektivní používání fronty úloh
Záznam položky fronty úloh má mnoho polí, jejichž účelem je přenášet parametry do procedury, kterou jste zadali ke spuštění s frontou úloh. To také znamená, že procedury, které mají být spuštěny prostřednictvím fronty úloh, musí být specifikovány se záznamem záznamu fronty úloh jako parametr ve triggeru **OnRun**. To pomáhá zajistit další úroveň zabezpečení, protože to zabrání uživatelům ve spuštění náhodných procedur prostřednictvím fronty úloh. Pokud uživatel musí předat parametry do sestavy, jediným způsobem, jak toho dosáhnout, je zabalení provádění sestavy do procerury, která pak analyzuje vstupní parametry a vloží je do sestavy před provedením.

## Plánování synchronizace mezi  [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)]
Pokud máte integrovaný [!INCLUDE[d365fin](includes/d365fin_md.md)] s [!INCLUDE[d365fin](includes/cds_long_md.md)], můžete pomocí fronty úloh naplánovat, kdy chcete synchronizovat data pro záznamy které jste spojili ve dvou obchodních aplikacích. V závislosti na směru a pravidlech, která jste definovali pro integraci, mohou úlohy synchronizace také vytvářet nové záznamy v cílové aplikaci tak, aby odpovídaly záznamům ve zdroji. Pokud například prodejce vytvoří nový kontakt v [!INCLUDE[crm_md](includes/crm_md.md)], může synchronizační úloha vytvořit tento kontakt pro sdruženého prodejce v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro více infrmací navštivte [Plánování synchronizace mezi Business Central a Dynamics 365 for Sales](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md).

## Viz také
[Administrace](admin-setup-and-administration.md)  
[Nastavení Business Central](setup.md)  
[Změna základního nastavení](ui-change-basic-settings.md)
