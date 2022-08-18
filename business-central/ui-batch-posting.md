---
title: Post Multiple Documents at the Same Time
description: Learn how to select multiple non-posted documents in a list for immediate or scheduled batch posting in Business Central.
author: SorenGP


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 
ms.reviewer: edupont
ms.date: 06/25/2021
ms.author: edupont

---
# Dávkové účtování dokladů

Namísto účtování jednotlivých dokladů jeden po druhém můžete vybrat více nezaúčtovaných dokladů v seznamu pro okamžité zaúčtování nebo pro dávkové zaúčtování podle plánu, například na konci dne. To může být užitečné, pokud může pouze nadřízený zaúčtovat doklady vytvořené jinými uživateli nebo, aby se zabránilo problémům s výkonem systému z účtování během pracovní doby.

## Okamžité hmoradné zaúčtování nákupních objednávek

Následující postup vysvětluje, jak okamžitě zaúčtovat více nákupních objednávek. Postup je podobný pro všechny nákupní a prodejní doklady.

1. Vyberte ![Žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete delat"), zadejte **Nákupní objednávky**a pak zvolte související odkaz.
2. Na stránce **Nákupní objednávky** pokračujte výběrem všech objednávek, které mají být zaúčtovány:
3. V poli **Číslo** zvolte tři tečky pro otevření kontextové nabídky a pak zvolte akci **Vybrat další**.
4. Zaškrtněte políčko u všech řádků představujících objednávky, které chcete zaúčtovat současně.
5. Zvolte akci **Účtovaní** a poté **Účtovat**.
6. V potvrzovací zprávě klikněte na tlačítko **Ano**.

## Dávkově zaúčtování více nákupních objednávek

Následující postup vysvětluje, jak dávkově zaúčtovat nákupní objednávky. Kroky jsou podobné pro všechny nákupní a prodejní doklady, kde je k dispozici akce **Dávkové účtování**.

1. Vyberte ![Žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete delat"), zadejte **Nákupní objednávky**a pak zvolte související odkaz.
2. Na stránce **Nákupní objednávky** pokračujte výběrem všech objednávek, které mají být zaúčtovány:
3. V poli **Číslo** zvolte tři tečky pro otevření kontextové nabídky a pak zvolte akci **Vybrat další**.
4. Zaškrtněte políčko u všech řádků představujících objednávky, které chcete zaúčtovat současně.
5. Zvolte akci  **Účtování** a poté **Dávkové účtování**.
6. Na stránce **Dávkové účto nák.objednávek** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Zvolte tlačítko **OK**.
8. Chcete-li zobrazit potenciální problémy, ke kterým došlo během hromadného účtování dokladů, otevřete stránku **Registr chybových zpráv**.

> [!NOTE]
> Účtování více dokladů může chvíli trvat a blokovat ostatní uživatele. Zvažte možnost povolení účtování na pozadí. Pro více informací navštivte [Použití fronty úloh na plánování úloh](admin-job-queues-schedule-tasks.md)

## Nastavení účtování na pozadí pomocí fronty úloh
Fronta úloh je účinným nástrojem pro plánování chodu obchodních procesů na pozadí, například když se více uživatelů pokouší zaúčtovat prodejní objednávky, ale současně lze zpracovat pouze jednu objednávku.

Následující postup vysvětluje, jak nastavit účtování prodejních objednávek na pozadí. Kroky pro nákup jsou podobné.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení prodeje a pohledávek** a poté vyberte související odkaz.
2. Na stránce **Nastavení prodeje a pohledávek** zaškrtněte políčko **Účtovat frontou úloh**.
3. Zvolte pole **Kód kategorie fronty úloh** a zadejte kód **SALESPOST**.

   > [!NOTE]
   > Některé úlohy mění stejná data a neměly by být spuštěny současně, protože to může způsobit konflikty. Například úlohy na pozadí pro prodejní doklady se pokusí upravit stejná data současně. Kategorie fronty úloh pomáhají předcházet těmto konfliktům tím, že zajišťují, že při spuštění jedné úlohy se další úloha, která patří do stejné kategorie front úloh nespustí, dokud nedokončí. Například úloha, která patří do kategorie fronty prodejních úloh, bude čekat, dokud nebudou provedeny všechny ostatní úlohy související s prodejem. Kategorii fronty úloh určíte na záložce **Účtování na pozadí** na stránce **Nastavení prodeje a pohledávek**.
   >
   > [!INCLUDE[prod_short](includes/prod_short.md)] poskytuje kategorie fronty úloh pro prodej, nákup a účtování hlavní knihy. posting. Doporučujeme, abyste vždy určili jeden z nich nebo ten, který vytvoříte. Pokud dojde k selhání v důsledku konfliktů, zvažte nastavení kategorie pro všechno účtování prodeje, nákupu a hlavní knihy na pozadí.

   Chcete-li, aby se prodejní doklady vytiskly i při jejich zaúčtování, zaškrtněte políčko **Účto a tisk frountou úloh** na stránce **Nastavení prodeje a pohledávek**.  
   Pokud v poli **Typ výstupu sestavy** vyberete **PDF**, úspěšně zaúčtované nákupní objednávky budou k dispozici v části **Schránka sestav** ve vašem Centru rolí.

   > [!IMPORTANT]  
   > Pokud nastavíte úlohu, která bude účtovat a tisknout dokumenty a tiskárna zobrazí dialogové okno, například žádost o přihlašovací údaje nebo upozornění na nedostatek inkoustu v tiskárně, bude váš dokument zaúčtován, ale nevytisknut. Odpovídající záznam fronty úloh nakonec vyprší a pole **Stav** se nastaví na **Chyba**. Proto doporučujeme nepoužívat nastavení tiskárny, které vyžaduje interakci se zobrazením dialogových oken tiskárny ve spojení s odesíláním na pozadí.

   Při příštím účtování prodejních dokladů , [!INCLUDE [prod_short](includes/prod_short.md)]automaticky vytvoří položku fronty úloh pro každý doklad a spustí úlohy na pozadí jednu po druhé.

4. Chcete-li ověřit, zda fronta úloh funguje podle očekávání, zaúčtujte prodejní objednávku. Více informací viz [Prodávání produktů](sales-how-sell-products.md).
   Prodejní objednávka bude nyní přidána do vyhrazené položky fronty úloh, která definuje, kdy jsou doklady zaúčtovány.

### Zobrazení stavu z prodejního nebo nákupního dokladu
Pokud fronta úloh nemůže prodejní objednávku zaúčtovat, změní se stav na  **Chyba** a prodejní objednávka se přidá do seznamu prodejních objednávek, které musí uživatel zpracovat ručně.
1. V dokladu, který jste se pokusili účtovat pomocí odeslání na frontu úloh, vyberte pole **Stav fronty úloh**, které bude obsahovat **Chybu**.
2. Zkontrolujte chybovou zprávu a problém vyřešte.

Případně můžete na stránce **Položky protokolu fronty úloh** zkontrolovat, zda byla prodejní objednávka úspěšně zaúčtována. Další informace naleznete v části [Monitorování fronty úloh](#monitor-the-job-queue).

## Vytvoření položky fronty úlohy pro dávkové účtování prodejních objednávek

Případně můžete odložit účtování na dobu, kdy je to pro vaši organizaci výhodné. Například ve vaší firmě může mít smysl spouštět určité úlohy, když většina zadávání dat pro daný den skončila. Můžete toho dosáhnout nastavením fronty úloh tak, aby spouštěly různé sestavy dávkového účtování, jako jsou **Dávkové účto prod.faktur**, **Dávkové účto prod.objednávek** a podobné sestavy. [!INCLUDE[prod_short](includes/prod_short.md)] podporuje účtování na pozadí pro všechny prodejní, nákupní a servisní doklady.

Následující postup ukazuje, jak nastavit sestavu **Dávkové účto prod.objednávek** tak, aby automaticky účtovaly prodejní objednávky v 16:00 hod. ve všední dny.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky fronty úloh** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. V poli **Typ spouštěného objektu** vyberte možnost ** Sestava**.
4. V poli **ID spouštěného objektu** vyberte možnost 296, **Dávkové účto prod.objednávek**.

   Můžete také použít následující sestavy:

   * 900 **Dávkové účtování montážních zakázek**
   * 497 **Dávkové účto nák.faktur**
   * 496 **Dávkové účto nák.objednávek**
   * 498 **Dávkové účto nák. dobropisů
   * 6665 **Dávkové účto nák. obj. vratky**
   * 298 **Dávkové účto prod.dobropisů**
   * 297 **Dávkové účto prod.faktur**
   * 296 **Dávkové účto prod.objednávek**
   * 6655 **Dávkové účto prod.obj.vratky**
   * 6005 **Dávkové účtování dobropisů servisu**
   * 6004 **Dávkové účtování faktur servisu**
   * 6001 **Dávkové účto serv.zakázek**

5. Zaškrtněte políčko **Dialog sestavy**
6. Na stránce **Dávkové účto prod.objednávek** definujte, co je zahrnuto během automatického zaúčtování prodejních objednávek, a poté klikněte na tlačítko **OK**.

   > [!IMPORTANT]
   > Nezapomeňte nastavit striktní filtry; jinak [!INCLUDE [prod_short](includes/prod_short.md)] zaúčtuje všechny doklady, i když nejsou připravené. Zvažte nastavení filtru v poli **Stav** na hodnotu *Vydáno* a filtr v poli **Zúčtovací datum** na *..dnes*. Pro více infortmací navštivte [Řazení, Vyhledávání a Seznam filtrování](ui-enter-criteria-filters.md).
7. Zaškrtněte všechna políčka od **Spustit v pondělí** až po **Spustit v pátek**
8. Do pole **Počáteční čas** zadejte 16:00.
9. Zvolte akci **Nastavit stav na Připraveno**.

Prodejní objednávky, které jsou v rámci definovaných filtrů, budou nyní zaúčtovány každý pracovní den v 16 hodin.

## Monitorování fronty úloh

Pokud nastavíte účtování na pozadí pomocí fronty úloh, nastavte jako běžný úkol sledovat frontu úloh, abyste zachytili případné problémy. Stav můžete sledovat na stránce **Položky fronty úloh**. Pro více informací navštivte [Použití fronty úloh na plánování úloh](admin-job-queues-schedule-tasks.md)

Jako správce můžete použít [Application Insights](/azure/azure-monitor/app/app-insights-overview) ke shromažďování a analýze telemetrie, kterou můžete použít k identifikaci problémů. Pro více informací navštivte [Monitorování a analýza telemetrie](/dynamics365/business-central/dev-itpro/administration/telemetry-overview) v obsahu pro vývojáře a správu.

## Viz také

[Účtování dokladů a deníků](ui-post-documents-journals.md)  
[Použití fronty úloh k pravidelným úkolům](admin-job-queues-schedule-tasks.md)  
[Úprava účtovaných dokladů](across-edit-posted-document.md)  
[Oprava nebo zrušení nezaplacených účtovaných faktur](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Vyhledávání stránek a inforamcí pomocí Řekněte mi](ui-search.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]