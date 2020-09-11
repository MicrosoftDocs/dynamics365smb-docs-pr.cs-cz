---
    title: Design Details - Item Tracking Posting Structure | Microsoft Docs
    description: Learn how to use item ledger entries as the primary carrier of item tracking numbers.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: design, item tracking, posting, inventory
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Detaily návrhu: Struktura účtování sledování zboží
Pro sladění s funkcemi kalkulace zásob a pro získání jednoduššího a robustnějšího řešení se jako hlavní nosič používají položky sledování zboží k přenášení informací o číslech sledování zboží.

Čísla sledování zboží na objednávkovém i ne-objednávkovém systému jsou uvedena v tabulce T337 **Položky rezervace**. Čísla sledování zboží, která souvisejí s historickými informacemi, jsou načtena přímo z položek zboží, které souvisejí s danou transakcí. To znamená, že položky zboží odrážejí specifikaci sledování zboží zaúčtovaného řádku objednávky.

Stránka **Řádky sledování zboží** načítá informace z T337 a položek zboží a společně je zobrazí přes tabulku T336 **Specifikace sledování**. T336 aké uchovává dočasná data na **stránce Řádky sledování zboží** pro množství sledování, které zbývý fakturovat.

## Vztah 1:M
Tabulka **Relace položky zboží** která se používá k propojení zaúčtovaného řádku dokladu se souvisejícími položkami zboží, se skládá ze dvou hlavních částí:

* Ukazatel na zaúčtovaný řádek dokladu, pole**Číslo řádku objednávky**
* Číslo položky odkazující na položku zboží, pole **Číslo položky zboží**.

Funkce existujícího pole **Číslo položky**, které spojuje položku zboží se zaúčtovacím řádkem dokladu, zpracovává typický vztah 1:1, pokud na zaúčtovaném řádku dokladu neexistují žádná čísla sledování zboží. Pokud existují čísla sledování zboží, poté pole **Číslo položky** zůstane prázdné, a vztah 1:M je zpracován tabulkou **Položky sledování zboží**. Pokud zaúčtované řádky dokladu přenáší sledovací čísla zboží, ale vztahuje se pouze k jedné položce zboží, pole **Číslo položky** zpracovává vztah, a nevytvoří žádný záznam v tabulce **Relace položky zboží**.

## Codeunity 80 a 90
Chcete-li rozdělit položky zboží během účtování, kód v codeunitě 80 a 90, obsahuje smyčky, které prochází globálními dočasnými proměnnými záznamu. Tento kód volá codeunitu 22 s řádkem deníku zboží. Tyto proměnné jsou inicializovány, pokud pro řádek dokladu existují čísla sledování zboží. Aby byl kód jednoduchý, vždy se používá tato struktura opakování. Pokud pro řádek dokladu neexistují žádná čísla sledování zboží, vloží se jeden záznam a smyčka se spustí pouze jednou.

## Účtování deníku zboží
Čísla sledování zboží jsou převedeny prostřednictvím položek rezervace, které se vztahují k položce zboží a opakování prostřednictvím čísel sledování zboží pomocí codeunity 22. Tento koncept funguje stejným způsobem, když se řádek deníku zboží používá nepřímo k zaúčtování prodejní nebo nákupní objednávky, jako když je řádek deníku zboží použit přímo. Při použití deníku zboží přímo se pole **ID zdrojové buňky** odkazuje na samotný řádek deníku zboží.

## Code unita 22
Codeunity 80 a 90 opakují volání procedury 22 během zaúčtování čísel sledování zboží faktry a při fakturaci existujicích dodávek nebo příjemek.

Během účtování množství čísel sledování zboží načte Codeunita 22 čísla sledování zboží z položek v T337, které se vztahují k účtování. Tyto položky jsou umístěny přímo na řádku deníku zboží.

Codeunit 22 prochází čísly sledování zboží a rozdělí účtování na příslušné položky zboží, které nesou čísla sledování zboží. Informace o tom, které položky zboží jsou vytvořeny, jsou vráceny do  tabulky T337 pomocí dočasného záznamu v tabulce T336, které jsou volány procedurou codeunitě 22. Tento postup se spustí, když codeunita 22 dokončí jeho spuštění, protože v tomto okamžiku codeunita 22 obsahuje informace. Po načtení dočasného záznamu v T336, codeunity 80 a 90 vytvoří záznam v tabulce **Relace položky zboží**, které propojí vytvořené položky zboží s vytvořeným řádkem dodávky nebo příjmu. Codeunita 80 nebo 90 pak převede dočasné záznamy v T336 na skutečné záznamy v T336, které souvisejí s daným řádkem. K tomuto převodu však dochází, pouze pokud není odstraněn řádek zaúčtovaného dokladu, protože je zaúčtován pouze částečně.

## Viz také
[Detaily návrhu: Sledování zboží](design-details-item-tracking.md)   
[Detaily návrhu: Design sledování zboží](design-details-item-tracking-design.md)