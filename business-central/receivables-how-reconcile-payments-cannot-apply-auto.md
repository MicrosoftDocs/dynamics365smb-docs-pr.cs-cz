---
title: Using the Transfer Difference to Account Feature to Reconcile Payments
description: Describes how to process payments that cannot be applied to a document, for example, when an exchange rate causes amounts to differ.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 10/01/2020
ms.author: edupont

---
# Odsouhlasení plateb, které nelze vyrovnat automaticky
Někdy budete možná muset zpracovat platby na váš bankovní účet, které nemohou být vyrovány se související položkou zákazníka, dodavatele nebo bankovního účtu. Důvodem může být, že v [!INCLUDE[prod_short](includes/prod_short.md)] není doklad, na který by se platba vyrovnala, nebo související doklad v  [!INCLUDE[prod_short](includes/prod_short.md)] má rozdílnou částku, než transakce. Může se jednat například o důvod způsobený směnou měny. Na stránce **Deník odsouhlasení plateb** se všechny částky transakcí pro dosud nevyrovnané platby zobrazí v poli **Rozdíl** včetně částek, které nelze vyrovnat z výše uvedených důvodů.

Metody řešení těchto typů nevyrovnaných plateb:
* Ruční vyrovnání
* Použítí textového mapování účtů
* Převod nadbytečné částky na řádek deníku a pomocí účtování vytvoření požadované položky, jako je například vrácení přeplatku

Platby, které nelze vyrovnat se mohou na řádcích deníku odsouhlasení zobrazít následujícími způsoby:

* Hodnota v poli **Rozdíl** je rovná hodnotě v poli **Částka transakce**, což znamená, že žádnou část platby nelze vyrovnat se související otevřenou položkou zákazníka, dodavatele nebo bankovního účtu.
* Hodnota v poli **Rozdíl** je menší než hodnota v poli **Částka transakce** což znamená, že část platby může být vyrovnaná se související otevřenou položkou zákazníka, dodavatele nebo bankovního účtu. Zbývající část platby nelze vyrovnat a musí být odsouhlasena ručně pomocí přímého účtování na účet.

Chcete-li tyto platby odsouhlasit, zvolte akci **Převést rozdíl na účet** a poté určete na jaký účet bude částka v poli **Rozdíl** zaúčtována při účtování deníku odsouhlasení plateb. Můžete to udělat buď na stránce **Deník odsouhlasení plateb** nebo ze stránky **Přehled vyrovnání plateb** kterou otevřete výběrem hodnoty v poli **Spolehlivost párování** nebo v poli **Rozdíl**.

> [!TIP]  
> Podobné funkce existují pro nastavení automatického odsouhlasení opakujících se plateb, které nelze vyrovnat na související otevřené položky zákazníka, dodavatele nebo bankovního účtu. Další informace naleznete na stránce [Textové mapování opakovaných plateb pro automatické odsouhlasení](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

## Odsouhlasení plateb, které nelze vyrovnat automaticky
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Deníky odsouhlasení plateb** a poté vyberte související odkaz.
2. Otevřete deník odsouhlasení plateb. Pro více informací navštivte [Automatické odsouhlasení plateb](receivables-how-reconcile-payments-auto-application.md).
3. Zvolte funkci **Převést rozdíl na účet**. Stránka **Převést rozdíl na účet** se otevře.
4. Do pole **Typ účtu** vyberte na jaký typ účtu bude platba účtována.
5. Do pole **Číslo účtu** vyberte účet, na který bude platba účtována.
6. V poli **Popis** zadejte text, který popisuje toto přímé účtování platby. Ve výchozím nastavení je vložen text do pole **Text transkace** v řádku deníku odsouhlasení plateb.
7. Vyberte tlačítko **OK**.

Hodnota v poli **Rozdíl** je rovna hodnotě v poli **Částka transakce**, při účtování deníku odsouhlasení plateb, tak poté celá platba na řádku deníku bude přímo zaúčtována do zadaného protiúčtu.

Pokud hodnota v poli **Rozdíl** je nižší než hodnota v poli **Částka transakce** bude vytvořen další řádek deníku se stejným textem, datem a s rozdílem vloženým do pole **Částka transakce**. Na původním řádku deníku bude rozdíl odečten od hodnoty v poli **Částka transakce** a platba zůstane vyrovnaná na související položku zákazníka, dodavatele nebo bankovního účtu. Při účtování deníku odsouhlasení plateb bude částka platby zaúčtovaná jako vyrovnání. Druhá část platby bude zaúčtována přímo na zadaný účet.

## Viz také
[Správa pohledávek](receivables-manage-receivables.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]