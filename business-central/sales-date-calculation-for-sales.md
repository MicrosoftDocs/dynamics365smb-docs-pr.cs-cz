---
    title: Date Calculation for Sales | Microsoft Docs
    description: The application automatically calculates the date on which you must order an item to have it in inventory on a certain date. This is the date on which you can expect items ordered on a particular date to be available for picking.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Výpočet data pro prodej
[!FUNKCE INCLUDE[d365fin](includes/d365fin_md.md)] automaticky vypočítá nejbližší možné datum dodávky zboží na řádku prodejní objednávky.

Pokud zákazník požádal o konkrétní datum dodání, vypočítá se datum, kdy musí být zboží k dispozici pro vyskladnění, aby splnilo dané datum dodání.

Pokud zákazník nepožaduje konkrétní datum dodání, vypočítá se datum, kdy lze zboží doručit, počínaje dnem, kdy jsou položky k dispozici k vyskladnění.

## Výpočet požadovaného data dodání
Pokud zadáte požadované datum dodání na řádku prodejní objednávky, stane se toto datum výchozím bodem pro následující výpočty.

- požadované datum dodání - čas dodávky = plánované datum dodávky
- plánované datum dodávky -  výstupní sklad doba zpracování = datum dodávky

Pokud je zboží dostupné k vyskladnění k datu dodávky, může proces prodeje pokračovat. Jinak se zobrazí varování o vyprodání zásob.

> <x1/>!Note<x2/>
> Pokud je váš proces založen na zpětném výpočtu, například pokud k získání plánovaného data dodávky použijete požadované datum dodání, doporučujeme vám použít datové vzorce s pevnou dobou trvání, například „5D“ pro dobu pěti dnů nebo „1W“ pro jeden týden. Datové vzorce bez pevné doby trvání, například „CW“ pro aktuální týden nebo CM pro aktuální měsíc, mohou mít za následek nesprávné výpočty data. Více informací o datových vzorcích viz [Práce s daty a časy kalendáře](ui-enter-date-ranges.md).

## Výpočet nejbližšího možného data dodání
Pokud na řádku prodejní objednávky nezadáte požadované datum dodání nebo pokud požadované datum dodání nelze splnit, vypočítá se nejbližší možné datum, kdy bude zboží k dispozici. Toto datum se poté zadá do pole Datum dodávky na řádku a datum, kdy plánujete zboží odeslat, stejně jako datum, kdy budou zákazníkovi dodány, se vypočítá podle následujících vzorců.

- datum dodávky + výstupní sklad doba zpracování = plánované datum dodávky
- plánované datum dodávky + doba dodávky = plánované datum dodání


## Viz také
[Výpočet data pro nákupy](purchasing-date-calculation-for-purchases.md)<x2/>
[Vypočet slibovaných dat objednávky](sales-how-to-calculate-order-promising-dates.md)<x4/>
[Práce s [! INCLUDE[d365fin](includes/d365fin_md.md)]] (ui-work-product.md)
