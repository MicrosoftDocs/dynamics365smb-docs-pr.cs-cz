---
    title: General Journal Post Line Overview | Microsoft Docs
    description: This topic introduces changes to Codeunit 12, **Gen. Jnl.-Post Line**, which is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: design, general ledger, post
    ms.date: 10/01/2020
    ms.author: edupont

---
# Přehled účtování řádku finančního deníku
Codeunit 12, **Gen. Jnl.-Post Line**, je hlavní objekt aplikace pro účtování finančího deníku a je jediným místem pro vložení věcných položek, položek DPH, zákazníka a dodavatele. Codeunita se také používá pro vyrovnávání, zrušení vyrovnání a rezervace.

I když byla Codeunita vylepšena v každém vydání za posledních deset let, její architektura zůstala v podstatě nezměněna. Codeunita byla velmi velká a měla přibližně 7600 řádků kódu. S vydáním [!INCLUDE[prod_short](includes/prod_short.md)], se architektura změnila a procedura byla zjednodušena a více udržovatelnější. Tato dokumentace představuje změny a poskytuje informace, které budete potřebovat pro upgrade.

## Stará architektura
Stará architektura měla následující vlastnosti:

* Existovalo rozsáhlé využití globálních proměnných, což zvýšilo možnost skrytých chyb v důsledku použití proměnných se špatným rozsahem.
* Existovalo mnoho dlouhých procedur (s více než 100 řádky kódu) tkteré měly také vysokou cyklomatickou složitost (tj. Mnoho vnořených příkazů CASE, REPEAT a IF), což velmi ztěžuje čtení a údržbu kódu
* Několik procedur, které byly použity pouze lokálně a byly určeny pouze k lokálnímu použití, nebylo označeno jako lokální.
* Většina procedur neměla žádné parametry a používala globální proměnné. Některé použité parametry a přetížené globální proměnné s lokálními.
* Vzory kódu pro vyhledávání ve věcných položkách, vytváření položek a položek DPH nebyly standardizovány a lišily se od místa k místu. Kromě toho došlo k mnoha duplikacím kódu a přerušení symetrii mezi kódem zákazníka a dodavatele.
* Velká část kódu v Codeunitě 12, přibližně 30 procent, souvisela s výpočty slevy a tolerancí plateb, i když tyto funkce nejsou v mnoha zemích nebo oblastech potřebné.
* Účtování, Vyrovnání, Zrušení vyrovnání, Stornování, Skonto, Odchylky a Úprava směnných kurzů byly společně v Codeunitě 12 pomocí dlouhého seznamu globálních proměnných.

### Nová Architektura
V [!INCLUDE[prod_short](includes/prod_short.md)], codeunit 12 prošla následující úpravou:

* Codeunita 12 byla přepracována do menších procedur (všechny méně jak 100 řádků kódu).
* Standardizované vzory pro vyhledávání účtů hlavní knihy byly implementovány pomocí pomocových funkcí z tabulek účto skupin.
* Architektura účtovacího modulu byla implementována pro správu zahájení a dokončení transakcí a pro izolaci vytváření do položek hlavní knihy a položek DPH, inkasa úpravy DPH a výpočtu dalších částek měny.
* Duplikace kódu byla odstraněna.
* Mnoho pomocných funkcí bylo převedeno do odpovídajících tabulek položek zboží, zákazníka a dodavatele.
* Použití globálních proměnných bylo minimalizováno, takže každá procedura používá parametry a zapouzdřuje vlastní aplikační logiku.

## Viz také
[Detaily návrhu: Struktura rozhraní účtování](design-details-posting-interface-structure.md)   
[Detaily návrhu: Struktura enginu účtování](design-details-posting-engine-structure.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]