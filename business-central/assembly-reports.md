---
title: Assembly Reports and Analytics in Business Central
description: See which assembly reports and analytics are available in the standard version of Business Central so that you can keep track of your business.
author: AndreiPanko

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa

---
# Sestavy a analýzy montáží v aplikaci Business Central

Reporting montáží v [!INCLUDE [prod_short](includes/prod_short.md)] umožňuje výrobním a obchodním pracovníkům získat přehled a statistiky o aktuálních a minulých montážních činnostech.

## Sestavy

Následující tabulka popisuje některé z klíčových sestav v oblasti montáží.

| Sestava | ID Objektu | Popis |
|---------|---------|---------|
| **Kusovníky** | 801 | Zobrazí seznam kusovníků: název, číslo kusovníku, součásti kusovníku a všechny další kusovníky, které jsou součástí kusovníku. Komponenty kusovníku jsou definovány v tabulce Komponenty kusovníku. Zde se také zobrazí měrná jednotka a potřebné množství každého komponentu na základní měrnou jednotku. |
| **Zboží - schopen provést (časová osa)** | 5871 | Zobrazuje, jak se v průběhu času mění pět různých klíčových údajů o dostupnosti položky kusovníku. Tyto údaje se mění v závislosti na očekávaných událostech týkajících se nabídky a poptávky a na nabídce, která vychází z dostupných komponent, které lze smontovat nebo vyrobit.<br>Pomocí sestavy můžete zjistit, zda můžete splnit prodejní objednávku na zboží k určitému datu, a to tak, že se podíváte na její aktuální dostupnost v kombinaci s potenciálním množstvím, které mohou dodat její komponenty, pokud by byla zahájena montážní zakázka. Sestava vám ukáže, kdy a kolik jednotek montážní a výrobní položky můžete vyrobit na základě dostupnosti komponent a aktuální dostupnosti položky. To se zobrazuje jako celkové množství.<br>Informace jsou zobrazeny v grafu, kde každý údaj o dostupnosti představuje čáru, která postupuje po časové ose a pohybuje se nahoru a dolů podle toho, jak se mění množství. Údaje o množství pocházejí ze stejného nástroje, který poskytuje informace v okně **Dostupnost zásob za úroveň kusovníku**. |
| **Distribuce náklad.podílu kusovníku** | 5872 | Zobrazuje graficky, jak jsou náklady na montované nebo vyrobené zboží rozloženy v kusovníku.<br>Takové informace mohou být užitečné například při rozhodování, zda změnit dodavatele komponent, nahradit využití interních kapacit externí pracovní silou nebo naopak, nebo při revizi a úpravě kusovníku.<br>První graf v sestavě zobrazuje celkové jednotkové náklady na komponenty a pracovní zdroje nadřazené položky rozdělené až do pěti různých podílů nákladů a graficky znázorněné různými barvami.<br>Koláčový graf s popiskem *Podle materiálu/mzdových nákladů* zobrazuje poměrné rozdělení mezi materiálové a mzdové náklady nadřazené položky a její vlastní výrobní režii. Podíl materiálových nákladů zahrnuje materiálové náklady zboží. Podíl mzdových nákladů zahrnuje náklady na kapacitu, režijní náklady na kapacitu a náklady na subdodávky. Podíly nákladů se zobrazují různě v závislosti na volbě v poli  **Pouze zobrazit**.<br>Koláčový graf s popiskem *Podle přímých/nepřímých* obrazuje poměrné rozdělení mezi přímé a nepřímé náklady nadřazené položky. Podíl přímých nákladů zahrnuje náklady na materiál, kapacitu a subdodávky. Podíl nepřímých nákladů zahrnuje kapacitní a výrobní režii.<br>Tabulka v dolní části sestavy je zahrnuta, pokud zaškrtnete políčko Zahrnout podrobnosti. Zobrazuje vybrané hodnoty z okna Podíly na nákladech kusovníku podle jednotlivých úrovní nebo srolované, v závislosti na možnosti zvolené v poli Zobrazit podíly na nákladech jako. |
| **Seznam použití** | 809 | Zobrazí seznam kusovníků, jejichž součástí je vybrané zboží. Užitečný přehled pro případ, že musíte změnit komponentu v kusovníku, která je vložena do položky sestavy. Například pokud váš dodavatel již nemůže dodat určitou položku, kterou jste použili pro montáž/výrobu. V takových scénářích vám tato sestava poskytuje snadný přehled o tom, do kterých kusovníků je komponenta zahrnuta. Můžete nastavit filtr pro číslo komponenty. |
| **Kusovník - suroviny** | 810 | Tato sestava vám poskytnoutne přehled o potřebných komponentech, a to jak pro montáž, tak pro výrobu. Uvidíte zásoby, základní měrnou jednotku, hlavního dodavatele, tedy pokud je číslo dodavatele napsáno na kartě zboží a také výpočet dodací lhůty. |
| **Kusovník - polotovary** | 811 | Pokud vyrábíte a/nebo sestavujete podsestavy, využijte tuto sestavu k získání přehledu o tomto typu komponent. Tato sestava zobrazuje základní měrnou jednotku, zásoby, jednotkové náklady a alternativní číslo zboží. |
| **Kusovník montáže - konc. zboží** | 812 | Zobrazí seznam položek nebo kusovníků, které nejsou součástmi kusovníků. **Poznámka**: Tato sestava není omezena pouze na kusovníky, takže nezapomeňte nastavit filtr v poli **Montážní kusovník** nebo na poli  **Systém doplnění**. |
| **Montáž na zakázku - Prodej** | 915 | Zobrazuje klíčové údaje o prodeji zboží montážních komponent, které lze prodávat jako součást montáže při prodeji na objednávku i jako samostatné zboží přímo ze skladu.<br>Tuto sestavu využijete k analýze množství, nákladů, prodejů a zisku montážních komponent, abyste podpořili svá rozhodnutí, například zda montáž ocenit jinak nebo zda určité zboží přestat nebo začít používat v montážích.<br> **V řádku montáže** se zobrazují údaje o prodeji celkového množství, které se prodává jako součást položky montáže. Pokud vyberete pole **Zobrazit podrobnosti montáže**, zobrazí se konkrétní prodeje položek montáže, které se sčítají v tomto součtu.<br>Důraz je kladen na součásti montáže, ale čísla jsou vypočítána ze ziskové marže jejich nadřazené položky montáže. V souladu s tím se částka prodeje každé komponenty vypočítá z jejích vlastních nákladů a ziskového rozpětí její nadřazené komponenty podle následujícího vzorce.<br>V přehledu se zobrazují informace o položkách, které splňují jedno nebo obě následující kritéria:<br>- Existuje v kusovníku montáže zboží, které používá zásady montáže na zakázku.<br>- Byl prodán jako součást prodeje na zakázku. |

## Úlohy

Následující články popisují některé klíčové úlohy pro analýzu stavu vaší firmy:

* [Zobrazit dostupnost zboží](inventory-how-availability-overview.md)

## Viz také

[Správa montáží](assembly-assemble-items.md)  
[Práce s kusovníkem](inventory-how-work-boms.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
