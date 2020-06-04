---
title: Approve or Reject Documents in Workflows| Microsoft Docs
description: Request, reject, or delegate an approval of, for example, a purchase or sales document, as part of a workflow.
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 10/01/2019
ms.author: sgroespe

---
# Použití schvalování workflow
Pokud musí být záznam, například nákupní doklad nebo karta zákazníka, schválen někým ve vaší organizaci, odešlete požadavek na schválení jako součást workflow. Na základě nastavení workflow je příslušná schvalující osoba informována o tom, že záznam vyžaduje schválení.

Schvalování workflow se nastavuje na stránce **Workflow**. Pro více informací navštivte [Nastavení workflow](across-set-up-workflows.md).

Kromě schvalování workflow popsaného v tomto tématu můžete provádět různé další úkoly souvisejíci s workflow. Pro více informací navštivte [Použití workflow](across-use-workflows.md).

Základní workflow schvalování nákupních a prodejních dokladů, deníků plateb, karet odběratele a karet zboží jsou připraveny ke spuštění jako průvodce. Pro více informací navštivte [Přehled](product-get-started.md).

## Požadavek na schválení záznamu
Následující úloha je prováděna uživatelem schvalování.

1. Na stránce, která představuje záznam, vyberte akci **Odeslat požadavek ke schvalování**.
2. Chcete-li zobrazit všechny vaše žádosti o schválení, vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Položky požadavku ke schvalování** a poté vyberte související odkaz.

Stav položky schvalování se aktualizuje z hodnoty **Vytvořené** na **Otevřeno**. Stav záznamu, například nákupní faktura, je aktualizována z **Otevřeno** na **Čeká na schválení** a zůstává uzamčena pro zpracování až do doby, než všichni schvalovatelé schválí záznam.

Když schvalovatel schválil záznam, stav se změní na **Vydáno**. Poté můžete pokračovat v práci se záznamem.

## Zrušení žádosti o schválení
Následující úloha je prováděna uživatelem schvalovaní s právy schvalovatele.

Zákazník může chtít po odeslání ke schválení změnit objednávku. V takovém případě můžete zrušit proces schvalování a provést potřebné změny objednávky, než požádáte o opětovné schválení.

- Na stránce, která představuje záznam, vyberte akci **Zrušit požadavek ke schvalování**.

Pokud byla žádost o schválení zrušena, změní se stav příslušné položky schválení na **Zrušeno**. Stav záznamu je aktualizován z **Čeká na schválení** na **Otevřeno**. Schvalovací proces pak může začít znovu.

## Schválení nebo zamítnutí žádosti o schválení
Následující úloha je prováděna uživatelem schvalovaní s právy schvalovatele.

Žádosti o schválení můžete zpravovat na stránce **Žádosti o schválení**, například za účelem schválení více žádostí najednou. Alternativně můžete zpracovat každý požadavek na souvisejícím záznamu stejně jako stránka **Nákupní faktura**, výběrem odkazu v obdržené notifikaci.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Požadavky na schválení** a poté vyberte související odkaz.
2. Vyberte jeden nebo více řádků pro záznam nebo záznamy, které chcete schválit nebo odmítnout.
3. Vyberte akci **Schválit**, **Zamítnout** nebo **Delegovat**.

Po schválení nebo odmítnutí záznamu se stav schválení v poli **Status** změní na **Schváleno** nebo **Zamítnuto**.

Je-li nastavena hierarchie schvalovatele, bude stav záznamu **Čeká na schválení** dokud záznam neschválí všichni schvalovatelé. Poté se stav záznamu změní na **Vydáno**.

Současně se stav schválení změní z **Vytvořeno** na **Otevřeno**, jakmile bude vytvořena žádost o schválení pro záznam. Pokud je žádost zamítnuta, stav schválení se změní na **Zamítnuto**. Stav zůstane nastaven na **Otevřený** nebo **Zamítnuto** dokud žádost neschválí všichni schvalovatelé.

## Delegovat žádosti o schválení
Následující úloha je prováděna uživatelem schvalovaní s právy schvalovatele.

Chcete-li zabránit tomu, aby se dokumenty shromažďovaly nebo jinak zablokovaly workflow, schvalovatel a správce schvalování mohou přenést žádost o schválení na náhradního schvalovatele. Náhradník může být buď určeným náhradníkem, přímým schvalovatelem nebo schvalovacím správcem v uvedeném pořadí priority. Tuto funkci obvykle používáte, pokud je schvalovatel mimo kancelář a není schopen schválit žádosti před datem splatnosti.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Požadavky na schválení** a poté vyberte související odkaz.
2. Vyberte jeden nebo více řádků pro žádosti o schválení, které chcete přenést na náhradního schvalovatele a potom vyberte akci **Delegovat**.

Oznámení o schválení žádosti je odesláno schvalujícímu náhradníkovi.

## Správa žádostí o schválení po splatnosti
Následující úloha je prováděna uživatelem schvalovaní s právy schvalovatele.

V pravidelných intervalech musíte připomenout uživatelům schvalovacího workflow žádosti o schválení po splatnosti, na které musí reagovat. Na to použijete funkci **Odeslat upozornění na zpožděné pol.schvalování**.

Funkce **Odeslat upozornění na zpožděné pol.schvalování** kontroluje všechny otevřené žádosti o schválení, které jsou v současné době opožděné. Každý schvalovatel, který má alespoň jeden záznam o schválení po uplynutí doby platnosti, obdrží oznámení se seznamem všech žádostí o schválení po splatnosti. Oznámení se také zašle jejich schvalovatelům a všem žadatelům o schválení po splatnosti. Toto pomáhá, pokud musí být položka schválení po splatnosti delegována na náhradníka.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Odeslat upozornění na zpožděné pol.schvalování** a poté vyberte související odkaz.
2. Na stránce **Upozornění na zpožděné pol.schvalování**, vyberte akci **Odeslat upozornění na zpožděné pol.schvalování**.

## Viz také
[Prodej](sales-manage-sales.md)  
[Došlé doklady](across-income-documents.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
