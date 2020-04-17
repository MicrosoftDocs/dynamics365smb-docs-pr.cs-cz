---
title: Record expenses or income directly in G/L| Microsoft Docs
description: For business activities that are not represented by a document in, such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the General Journal page.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 10/01/2019
ms.author: sgroespe

---
# Zaúčtování transakcí přímo do hlavní knihy

Finanční deníky se používají k zaúčtování finančních transakcí přímo na účty hlavní knihy a na jiné účty, například na bankovní účty, účty zákazníků, dodavatelů a zaměstnanců.

Typickým využitím finančního deníku je zaúčtování výdajů zaměstnanců z vlastních peněz během podnikatelské činnosti za účelem pozdější úhrady.  Pro více informací navštivte [Zaznamenávání a uhrazování výdajů zaměstnanců](finance-how-record-reimburse-employee-expenses.md).

Finanční deníky zaúčtují finanční transakce přímo na účty hlavní knihy a další účty, například bankovní účty, účty zákazníků, dodavatelů a zaměstnanců. Účtování pomocí finančního deníku vždy vytváří položky na účtech hlavní knihy. To platí i v případě, že například zaúčtujete řádek deníku na účet zákazníka, protože položka je zaúčtována k finančímu účtu pohledávek prostřednictvím účto skupiny. Svou verzi finančního deníku si můžete přizpůsobit nastavením listu nebo šablony deníku. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).

Na rozdíl od položek, které jsou zaúčtovány s doklady, které vyžadují zpracování dobropisů, můžete správně obrátit položky, které jsou zaúčtovány ve finančním deníku. Pro více informací navštivte [Účtování deníku storna a vrácení příjemky/dodávky](finance-how-reverse-journal-posting.md).

## Zaúčtování transakce přímo na účet hlavní knihy

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky** a poté vyberte související odkaz.
2. Otevřete příslušný list finančního deníku. Pro více informací navštivte [Práce s finančními deníky](ui-work-general-journals.md).
3. V novém řádku deníku vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Opakujte krok 3 pro všechny samostatné transakce, které chcete zaúčtovat.

   > [!TIP]
   > Pokud chcete zadat více řádků transakcí nad jedním řádkem zůstatkového účtu, například pro jeden bankovní účet, zaškrtněte políčko **Navrhnout vyrovnávací částku** na řádku pro vaši dávku na stránce **Listy finančního deníku**. Poté je pole **Částka** na řádku rozvahového účtu automaticky předvyplněno hodnotou, která je nutná k vyrovnání transakcí.
5. Vyberte akci **Účtovat** a zaznamenejte transakce na určené finanční účty.

## Viz také

[Práce s finančními deníky](ui-work-general-journals.md)  
[Evidence a uhrazení výdajů zaměstnance](finance-how-record-reimburse-employee-expenses.md)  
[Účtování deníku storna a vrácení příjemky/dodávky](finance-how-reverse-journal-posting.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
