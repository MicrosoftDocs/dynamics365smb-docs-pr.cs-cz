---
    title: Design Details - Availability in the Warehouse | Microsoft Docs
    description: The system must keep a constant control of item availability in the warehouse, so that outbound orders can flow efficiently and provide optimal deliveries.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Skladová dostupnost
Systém musí udržovat stálou kontrolu nad dostupností zboží ve skladu, aby mohli odchozí objednávky efektivně proudit a poskytovat optimální dodávky.

Dostupnost se liší v závislosti na rozdělení na úrovni přihrádek, když dochází k činnostem skladu, jako jsou vyskladnění a přesuny, když systém rezervace ukládá omezení, která je třeba dodržovat. Poměrně složitý algoritmus ověřuje, že jsou splněny všechny podmínky před přidělením množství vyskladnění pro odchozí dodávky.

Pokud není splněna jedna nebo více podmínek, mohou se zobrazit různé chybové zprávy, včetně obecné zprávy "Není co zpracovat". Zpráva "Není co zpracovat" může nastat z mnoha různých důvodů, a to jak v odchozích, tak v příchozích tocích, kde je přímo nebo nepřímo zapojený řádek dokladu, který obsahuje pole **Množství ke zpracování**.

> [!NOTE]
> Brzy zde budou zveřejněny informace o možných důvodech hlášky „Není co zpracovat“.

## Obsah přihrádky a rezervace
V každé instalaci správy skladu existuje množství zboží jako položky skladu, v oblasti aplikace Sklad, tak jako položky zboží v oblasti zásob. Tyto dva typy položek obsahují různé informace o tom, kde položky existují a zda jsou k dispozici. Položky skladu definují dostupnost zboží podle přihrádky a typu přihrádky, který se nazývá obsah přihrádky. Položky zboží definují dostupnost zboží podle jeho rezervace k odchozím dokladům.

V algoritmu vyskladnění existují zvláštní funkce pro výpočet množství, které je k dispozici k vyskladnění, když je obsah přihrádky spojen s rezervacemi.

## Dostupné množství k vyskladnění
Pokud například algoritmus vyskladnění nezváží množství zboží, které je rezervováné pro čekající dodávku prodejní objednávky, může být toto zboží vyskladněno pro jinou prodejní objednávku, která je dodána dříve, což brání splnění prvního prodeje. Aby se zabránilo této situaci, algoritmus vyskladnění odečte množství, která jsou vyhrazena pro jiné výstupní doklady, množství v existujících dokladech vyskladnění a množství, která jsou vyskladněna, ale ještě nebyla dodána nebo spotřebována.

Výsledek se zobrazí v poli **Dostupné množ.k vyskladnění** na stránce **Sešity vyskladnění** kde je toto pole vypočítáno dynamicky. Hodnota se také vypočítá, když uživatelé vytvoří vyskladnění přímo pro výstupní doklady. Tyto výstupní doklady mohou být prodejní objednávky, spotřeba výroby nebo výstupní transfery, kde se výsledek projeví v souvisejících polích množství například **Množství ke zpracování**.

> [!NOTE]  
> Pokud jde o prioritu rezervací, množství k rezervaci se odečte od množství, které je k dispozici k výběru. Pokud je například množství dostupné v přihrádce vyskladnění 5 jednotek, ale 100 jednotek je v přihrádce zaskladnění, pak při pokusu o rezervaci více než 5 jednotek pro jinou objednávku se zobrazí chybová zpráva, protože dodatečné množství musí být k dispozici v přihrádce vyskladnění.

### Výpočet množství, které je k dispozici k vyskladnění
Množství, které je k dispozici k vyskladnění se vypočítá takto:

množství dostupné k vyskladnění = množství v přihrádkách pro vyskladnění - množství na vyskladnění a přesun – (rezervované množství v přihrádkách pro vyskladnění + rezervované množství na vyskladnění a přesun)

Následující diagram ukazuje různé prvky výpočtu.

![Dostupné množství s překrýváním rezervací](media/design_details_warehouse_management_availability_2.png "Dostupné množství s překrýváním rezervací")

## Množství dostupné k rezervaci
Vzhledem k tomu, že koncept obsahu přihrádky a rezervace existují společně, musí být množství zboží, které je k dispozici k rezervaci, přiřazeno ve výstupních dokladech skladu.

Mělo by být možné rezervovat všechny položky ve skladu s výjimkou těch, u které byla zahájena expedice. Proto je množství, které je k dispozici k rezervaci, definováno jako množství ve všech dokladech a ve všech typech přihrádek, s výjimkou následujících výstupních množství:

- Množství na nezapsaných dokladech vyskladnění
- Množství v dodacích přihrádkách
- Množství v přihrádkách pro výrobu
- Množství v přihrádkách dílny
- Množství v přihrádkách montáže
- Množství v adjustačních přihrádkách

Výsledek se zobrazí v poli **Celkové množství k dispozici** na stránce **Rezervace**.

Na řádku rezervace je množství, které nelze rezervovat, protože je přiděleno ve skladu, zobrazeno v poli **Množství přidělené ve skladu** na stránce **Rezervace**.

### Výpočet dostupného množství k rezervaci
Množství dostupné k rezervaci se vypočítá takto:

dostupné množství k rezervaci = celkové množství zásob - množství na vyskladnění a přesun ze zdrojových dokladů - rezervované množství - množství ve výchozích přihrádkách

Následující diagram ukazuje různé prvky výpočtu.

![Dostupnost rezervací přes alokaci sklad](media/design_details_warehouse_management_availability_3.png "Dostupnost rezervací přes alokaci skladu")

## Viz také
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Zobrazení dostupnosti ve skladu](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]