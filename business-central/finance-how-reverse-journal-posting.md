---
title: Undo a Posting by Posting a Reversing Entry| Microsoft Docs
description: If you have made an erroneous posting in the general journal, then you can use the Reverse Transaction function to undo the posting with a correct audit trail.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 01/27/2020
ms.author: sgroespe

---
# Stornování účtování
Chcete-li zrušit chybné účtování, vyberte záznam a vytvořte záznam storna (položky identické s původním záznamem, ale s opačným znaménkem v poli částky) se stejným číslem dokladu a datem účtování jako původní položka. Po stornování záznamu musíte provést správné položky.

Stornovat lze pouze položky, které jsou zaúčtovány z řádku finančního deníku. Položku lze zrušit pouze jednou.

Chcete-li zrušit příjemku nebo účtování dodání, dříve než budou zaúčtovány jako faktura, můžete v zaúčtovaném dokladu použít funkci **Zpět**. Můžete vrátit množství typu **Zboží** a **Zdroj**.

Pokud jste provedli nesprávné zaúčtování záporného množství, například nákupní objednávku s nesprávným množstvím zboží, a zaúčtovali jste ji jako přijatou, ale nefakturovanou, můžete účtování vrátit zpět.

Pokud jste odeslali nesprávné kladné množství, například prodejní dodávku nebo dodávku nákupní vratky, se špatným počtem zboží a zaúčtovali jste ji jako dodávku, ale nebyla vyfakturována, můžete účtování zrušit.

## Stornování účtování položek hlavní knihy
Položky můžete stornovat ze všech stránek **Položek**. Následující postup je založen na stránce **Věcné položky**.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Věcné položky** a poté vyberte související odkaz.
2. Vyberte položku, kterou chcete stornovat, a pak zvolte akci **Storno transakce**. Upozorňujeme, že musí pocházet z účtování v deníku.
3. Na stránce **Stornovat položky transakce** vyberte akci **Stornovat**.
4. V potvrzovací zprávě vyberte tlačítko **Ano**.

> [!NOTE]
> Nemůžete vrátit zpět položky, které byly zaúčtovány s informacemi z úlohy nebo které realizovaly zisky a ztráty v rámci stejné transakce.

## Zaúčtování záporné položky
Pole **Oprava** můžete použít k zaúčtování záporného MD namísto Dal nebo zaúčtování záporného Dal namísto MD na účtu. Pro splnění zákonných požadavků je toto pole ve výchozím nastavení viditelné ve všech denících. Pole **Částka MD** a **Částka Dal** zahrnují jak původní položku, tak opravenou položku. Tato pole nemají žádný vliv na zůstatek na účtu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky** a poté vyberte související odkaz.
2. V poli **Název listu** vyberte požadovaný název listu.
3. Zadejte informace do příslušných polí.
4. V řádku deníku, který chcete aktivovat pro záporné položky, zaškrtněte políčko **Oprava**.
5. Chcete-li zaúčtovat deník, vyberte akci **Účtovat** a poté zvolte tlačítko **Ano**.

## Zrušení účtování množství na zaúčtované nákupní příjemce
Následující text popisuje, jak zrušit vrácení zaúčtovaného zboží nebo zdrojů. Kroky jsou podobné i pro účtované dodávky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované nákupní příjemky** a poté vyberte související odkaz.
2. Otevřete zaúčtovanou příjemku, kterou chcete vrátit.
3. Vyberte řádek nebo řádky, které chcete vrátit zpět.
4. Vyberte akci **Vrátit příjemku**.

Korekční řádek je vložen pod vybraný řádek příjmu. Pokud bylo množství přijato v příjemce skladu, je na zaúčtovou příjemku skladu vložen opravný řádek.

Pole **Přijaté množství** a **Přijato,  nefakt.  (množ.)** na související objednávce jsou nastaveny na nulu.

## Vrácení a následné opětovné zaúčtování množství u zaúčtované dodávky vratky
Následující text popisuje, jak zrušit zaúčtovanou dodávku vratky pro zboží nebo zdroj a poté znovu zaúčtovat nákupní vratku s novým množstvím. Kroky jsou podobné i pro zaúčtované příjemky vratky.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účtované dodávky vratek** a poté vyberte související odkaz.
2. Otevřete zaúčtovanou dodávku vratky, kterou chcete vrátit.
3. Vyberte řádek nebo řádky, které chcete vrátit.

4. Vyberte akci **Vrátit dodávku vratky**.

   Do zaúčtovaného dokladu se vloží korekční řádek a pole **Množství vratky  dodané** a **Částka vratky dodaná,  nefakt.** na vratce jsou nastaveny na nulu.

   Nyní se vraťte zpět k objednávce nákupní vratky a zopakujte účtování.

5. Na stránce **Účtovaná dodávka vratky** si poznamenejte číslo do pole **Č.objednávky vratky**.
6. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Objednávky nákupní vratky** a poté vyberte související odkaz.
7. Otevřete příslušnou objednávku vratky a poté vyberte akci **Znovu otevřít**.
8. Opravte položku v poli **Množství** a znovu zaúčtujte objednávku nákupní vratky.

## Viz také
[Zrušení účtování montáže](assembly-how-to-undo-assembly-posting.md)  
[Zaúčtování transakcí přímo do hlavní knihy](finance-how-post-transactions-directly.md)  
[Práce s finančními deníky](ui-work-general-journals.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
