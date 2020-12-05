---
    title: Allocation Status and Repair Status | Microsoft Docs
    description: Learn about the relationship between the repair status of service items and the allocation status of the allocation entries for them.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: resources, allocation, status, repairs
    ms.date: 10/01/2020
    ms.author: bholtorf

---
# Stav přidělení a stav opravy předmětů servisu
Stav opravy předmětů servisu a stav přidělení položek přidělení pro předměty servisu mají určitý vztah ve Správě servisu. Stav přidělení se změní, když změníte stav opravy předmětu servisu na **Dokončeno** nebo **Částečný Servis** a když převedete nabídku servisu na servisní objednávku. Stav opravy předmětu sevisu se změní, když zrušíte přidělení předmětu servisu nebo znovu přidělíte předmět servisu jinému zdroji. Stav opravy předmětu servisu můžete zobrazit na stránce **Servisní úlohy** a stav opravy můžete aktualizovat v poli **Kód stavu opravy** na stránce **Sešit předmětu sevisu< / g5>. Stav přidělení můžete zobrazit v poli **Stav** na stránce **Přidělení zdrojů**.

## Změna stavu opravy
Když změníte stav opravy předmětu servisu na řádku předmětu servisu, bude vyhledána odpovídající položka přidělení pro tento předmět servisu, který má stav **Aktivní**. Pokud je taková položka přidělení nalezena, stav se aktualizuje jedním z následujících způsobů:

* Pokud změníte stav opravy na **Dokončeno**, stav přidělení se změní z **Aktivní** na **Dokončeno**.
* Pokud změníte stav opravy na **Částečný sevis**, tedy že servis byl částečně dokončen, nebo **Odesláno**, tedy že nebyl proveden žádný servis, stav přidělení se změní z **Aktivní** na **Nutné přerozdělení**.
* Když je vytvořen záznam o přidělení servisní zakázky, který označuje, že nebyl přidělen žádný zdroj, je pole **Stav** na stránce **Přidělení zdrojů** nastaveno na **Neaktivní**.
* Stav položky přidělení je nastaven na **Zrušeno**, když znovu přidělíte odkazovaný předmět servisu v položce přidělení servisní zakázky, což naznačuje, že přidělený zdroj nebo skupina zdrojů se o servisní úlohu nepokusil.

Stav přidělení odráží, kdy je proces servisu dokončen, nebo když je pro dokončení servisu předmětu servisu nutný jiný zdroj.

## Převod nabídek servisu na objednávky servisu
Při převodu nabídky servisu na servisní zakázku se servisní zakázka, předměty servisu v zakázce a jejich položky přidělení aktualizují následujícími způsoby:

* Stav opravy předmětů servisu se změní na **Počáteční**.
* Stav servisní zakázky se změní na **Servis probíhá**.
* Existuje hledání položek přidělení pro všechny předměty servisu v servisní zakázce, které mají stav **Aktivní**. Pokud jsou takové položky přidělení nalezeny, změní se jejich stav přidělení z **Aktivní** na **Nutné přerozdělení**.

## Zrušení přidělení
Když zrušíte přidělení pro předmět servisu, [! INCLUDE[d365fin](includes/d365fin_md.md)] aktualizuje stav přidělení odpovídající položky přidělení z **Aktivní** na **Nutné přerozdělení**.

Stav opravy předmětu servisu v položce přidělení se aktualizuje následujícími způsoby:

* Pokud je stav opravy **Počáteční**, stav opravy se změní na **Odesláno** (nebyl zahájen žádný servis).
* Pokud je stav opravy **Zpracovává se**, stav opravy se změní na **Částečný servis** (určitý servis byl dokončen).

## Přerozdělení Aktivní položky přidělení
Když znovu přidělíte předmět servisu v položce přidělení, která je **Aktivní**, položka přidělení se aktualizuje následujícími způsoby:

* Pokud byl servis zahájen, když bylo přidělení **Aktivní** (tj. Pokud byl stav opravy předmětu servisu v položce změněn na **Zpracovává se**), změní se stav přidělení z **Aktivní** na **Dokončeno**.
* Pokud servis nebyl zahájen, když bylo přidělení **Aktivní**, změní se stav přidělení z **Aktivní** na **Zrušeno**.

Stav opravy předmětu servisu v položce přidělení se aktualizuje stejným způsobem, jako kdybyste zrušili přidělení:

* Pokud je stav opravy **Počáteční**, stav opravy se změní na **Odesláno** (nebyl zahájen žádný servis).
* Pokud je stav opravy **Zpracovává se**, stav opravy se změní na **Částečný servis** (určitý servis byl dokončen).

Je vytvořena nová položka přidělení, která obsahuje nový zdroj, který má stav **Aktivní**.

## Přerozdělení předmětu servisu
Když znovu přidělíte předmět servisu v položce přidělení, která má stav **Nutné přerozdělění**, položka přidělení se aktualizuje následujícími způsoby:

* Pokud byl servis zahájen, když bylo přidělení **Aktivní** (tj. Pokud byl stav opravy předmětu servisu v položce změněn na **Zpracovává se**), změní se stav přidělení z **Nutné přerozdělení** na **Dokončeno**.
* Pokud servis nebyl zahájen, když bylo přidělení **Aktivní**, změní se stav přidělení z **Nutné přerozdělení** na **Zrušeno**.

Je vytvořena nová položka přidělení, která obsahuje nový zdroj, který má stav **Aktivní**.

## Viz také
[Nastavení přidělení zdrojů](service-how-setup-resource-allocation.md)<x2/>
[Přidělování zdrojů](service-how-to-allocate-resources.md)

