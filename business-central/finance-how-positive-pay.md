---
title: Export Positive Pay Files| Microsoft Docs
description: You can ensure your bank only clears validated checks and amounts by exporting a Positive Pay file that contains vendor and payment information.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 10/01/2019
ms.author: sgroespe

---
# Export souboru kladných plateb
Chcete-li se ujistit, že vaše banka smaže pouze ověřené šeky a částky, můžete exportovat soubor kladných plateb, který obsahuje informace o dodavateli, číslo šeku a částku platby, kterou pošlete do banky pro účely zpracování plateb.

[!INCLUDE[d365fin](includes/d365fin_md.md)] je předkonfigurován pro podporu souborů kladných plateb pro Bank of America a City Bank.

## Nastavení bankovního účtu pro kladné platby
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Otevřete kartu banky, pro kterou chcete použít kladnou platbu.
3. V poli **Kód exportu kladné platby** zadejte POSPAYBANK.
4. Zavřete stránku.

## Export souboru kladných plateb
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Vyberte bankovní účet, pro který chcete exportovat soubor pozitivní platby.
3. Vyberte akci **Export kladných plateb**.

   Otevře se stránka **Export kladné platby**, která zobrazuje platby provedeny na bankovní účet od posledního data nahrání, jak je uvedeno v polích **Datum posledního nahrání** a **Čas posledního nahrání**.
4. V poli **Datum přerušení nahrávání** zadejte datum, před kterým platby nebudou zahrnuty do exportovaného souboru.
5. Vyberte akci **Export**.
6. Na stránce **Export souboru** vyberte tlačítko **Uložit** a uložte soubor na vhodné místo.
7. Nahrajte soubor na stránky vaší elektronické banky.
8. Zapište nebo zkopírujte číslo potvrzení zobrazené při úspěšném odeslání souboru.

Zobrazení exportovaných záznamů kladných plateb

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Vyberte bankovní účet, pro který chcete zobrazit záznamy exportovaných kladných plateb.
3. Vyberte akci **Položky kladné platby**.

   Na stránce **Položky kladné platby** jsou zobrazeny všechny exportované záznamy kladných plateb pro bankovní účet.
4. V poli **Číslo potvrzení** zadejte pro každý exportovaný záznam číslo potvrzení, které obdržíte, když je nahrání souboru do banky úspěšné.
5. Chcete-li zobrazit související platební řádky, vyberte akci **Detaily položky kladné platby**.

Opětovné exportování souborů kladných plateb

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Vyberte bankovní účet, pro který chcete znovu exportovat soubory kladných plateb.
3. Vyberte akci **Položky kladné platby**.
4. Vyberte řádek pro exportování souboru kladné platby, který chcete znovu exportovat.
5. Na stránce **Položky kladné platby** vyberte akci **Opětovné exportování kladných plateb do souboru**.

## Viz také
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Práce s finančními deníky](ui-work-general-journals.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
