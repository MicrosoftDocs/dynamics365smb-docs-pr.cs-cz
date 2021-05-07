---
    title: Design Details - Internal Warehouse Flows | Microsoft Docs
    description: The flow of items between bins at a company location centers on picking components and putting away end items for assembly or production orders and ad-hoc movements, such as bin replenishments, without a relation to source documents.
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
# Detaily návrhu: Interní skladové toky
Tok zboží mezi přihrádkami na skladě společnosti se soustředí na komponenty vychystávání a ukládání koncového zboží pro montážní nebo výrobní zakázky a adhoc přesuny. Jedný se například o doplnění přihrádky, bez vztahu ke zdrojovým dokladům. Rozsah a povaha zapojených činností se liší mezi základním a pokročilým skladováním.

Některé interní toky se překrývají s příchozími nebo odchozími toky. Některé z těchto kroků, které se překrávají jsou zobrazeny jako kroky 4 a 5 v diagramech pro pokročilé příchozí a odchozí toky. Pro více informací navštivte [Detaily návrhu: Vstupní procesy skladu](design-details-outbound-warehouse-flow.md).

## Vnitřní toky v základním nastavení skladu
V základní konfiguraci skladu se tok zboží mezi přihrádkami uvnitř společnosti soustředí na vyskladnění komponent a zaskladnění koncového zboží pro výrobní nebo montážní zakázky a adhoc přesuny. Jedná se o procesy jako je doplnění přihrádky, bez vztahu ke zdrojovým dokladům.

### Tok do a z Výroby
Hlavní integraci mezi výrobními zakázkami a základními aktivitami skladu představuje schopnost vyskladnit výrobní komponenty na stráních **Vyskladnění zásob** nebo **Pohyby zásob**.

> [!NOTE]  
> Na stránce **Vyskladnění zásob** je spotřeba komponenty zaúčtována společně s účtováním vyskladnění. Pomocí stránky **Přesun zásob** jsou zapsány pouze úpravy na přihrádce, nedojdeli k žádnému účtování do věcných položek.

Kromě zpracování komponent je integrace představena schopností zaskladnění vyrobeného zboží pomocí stránky **Zaskladnění zásob**.

Pole **Kód přihrádky do výroby**, **Kód přihrádky z výroby** a **Kód přihrádky dílny** na kartě lokace nebo strojním/pracovním centru definují výchozí toky do a z výrobních oblastí společnosti.

Další informace o tom, jak je spotřeba komponent vyskladněna a spotřebována z Do výroby nebo přihrádky dílky běžte na "Spotřeba komponent výroby ve skladu" v tomto článku.

### Tok z a do Montáže
Hlavní integrace mezi montážními zakázkami a základními aktivitami skladu je reprezentována schopností přesunout komponenty montáže do montáží.

I když pro zaskladování položek montáže neexistují žádné specifické funkce skladu, kód přihrádky v hlavičce objednávky montáže může být nastaven na výchozí přihrádku, který je nastavena pro vyskladnění. Zaúčtování montážní zakázky pak funguje jako účtování vyskladnění. Aktivitu skladu k přesunutí položek montáže do skladu lze spravovat na **Interní pohyby**bez vztahu k montážní zakázce.

Existují následující toky montáže.

| Tok | Popis |
|----------|---------------------------------------|  
| Montáž-na-sklad | Komponenty jsou potřebné v montážní zakázce, výstup je uložen ve skladu.<br /><br /> Tento skladový tok je řízen na stránce **Pohyby zásob**. Jeden řádek take určuje, odkud se budou brát komponenty. Další řádek určuje, kam se mají komponenty umístit. |
| Montáž-na-zakázku | Komponenty jsou potřebné na montážní zakázce, která je spojena s prodejní objednávkou, která je dodána a sestavena při zaúčtování objednávky. |

> [!NOTE]  
> Pokud je zboží sestaveno na objednávku, poté vyskladnění řádku propojených s prodejní objednávkou spustí pohyb zásob pro všechny komponenty montáže, nejen pro prodané zboží.

Pole **Kód přihrádky na montáž**, **kód přihrádky z montáže** a **Kód dod.  přihr.montáže-na-zák.** na kartě lokace definují toky z a do montáží.

> [!NOTE]  
> Pole **Kód dod. přihr.montáže-na-zák.** funguje jako přihrádka z montáže v montážích na zakázku.

### Ad-Hoc přesuny
V základním nastavení skladu se přesun zboží mezi přihrádkami bez vztahu ke zdrojovému dokladu se provádí na stránce **Interní pohyby**, která funguje společně s kartou **Pohyby zásob**.

Dalším způsobem, jak přesunout zboží mezi přihrádkami je ad-hoc přesun, kde se zadá do pole **Nový kód přihrádky** na stránce **Deník přeřazení zboží**.

## Interní skladové toky v rozšířeném nastavení skladu
V rozšířeném nastavení skladu je se tok mezi přihrádkami uvnitř společnosti soustředí na výdej komponent a vyskladnění koncového zboží pro výrobní zakázky a komponenty pro montážní zakázky. Kromě toho dochází k interním tokům jako jsou ad hoc přesuny, doplnění přihrádek, bez vztahu ke zdrojovým dokumentům.

### Toky z a do výroby
Hlavní integrace mezi výrobními zakázkami a pokročilými nastavením skladu je reprezentována schopností vyskladnění výrobních komponent na stránce **Vyskladnění** a **Sešity vyskladnění** a možnost zaskladnění vyrobené zbožá na stránce **Interní zaskladnění**.

Další integrační bod ve výrobě je poskytován na stránce **Skladové přesuny** společně se stránkou Sešity přesunu, která umožňuje umístit komponenty a převzít vyrobené zboží pro vydané výrobní zakázky.

Pole **Kód přihrádky do výroby**, **Kód přihrádky z výroby** a **Kód přihrádky dílny** na kartě lokace nebo strojním/pracovním centru definují výchozí toky do a z výrobních oblastí společnosti.

Další informace o tom, jak je spotřeba komponent provedena z přihrádek do výroby nebo otevřené přihrádek dílny, naleznete v části Spotřeba výrobních komponent ve skladu v tomto článku.

### Tok z a do Montáže
Hlavní integrace mezi montážními zakázkami a pokročilými aktivitami skladu je reprezentována schopností vyskladnit komponenty montáže pomocí stránek **Vyskladnění** a **Sešitu vyskladnění**. Tato funkce funguje stejně jako při vyskladnění komponent pro výrobní zakázky.

I když pro zaskladování položek montáže neexistují žádné specifické funkce skladu, kód přihrádky v hlavičce objednávky montáže může být nastaven na výchozí přihrádku, který je nastavena pro vyskladnění. Zaúčtování montážní zakázky pak funguje jako účtování vyskladnění. Aktivitu skladu pro přesunutí položek montáže do skladu lze dělat pomocí stránek **Sešitů přesunu** nebo **Interní vyskladnění** bez vvztahu k pořadí na montážní zakázce.

> [!NOTE]  
> Pokud je zboží smontováno na zakázku, potom skladová dodávka propojené prodejní objednávky aktivuje výběr vyskladnění pro všechny komponenty montáže, nejen pro prodanou položku, jako při klasické expedici zboží.

Pole **Kód přihrádky na montáž** a **Kód přihrádky z montáže** na kartě lokace definuje tok z a do montáže.

### Ad-Hoc přesuny
V pokročilém nastavení skladu je přesun zboží z přihrádky do přihrádky bez vztahu ke zdrojovým dokladům spravován na stránce **Sešity přesunu** a je evidován na stránce Skladové přesuny.

## Spotřeba výrobních komponent ve skladu
Pokud jsou komponenty vyskladněné pomocí vyskladnění jsou účtované jako spotřeba montáže, když se vyskladnění zapíše. Použitím metody spotřeby **Vyskladnění + předem** a **Vyskladnění + zpětné** vyskladnění spustí související účtování spotřeby při spuštění první operace nebo při dokončení poslední.

Zvažte následující scénář založený na demo databázi [!INCLUDE[prod_short](includes/prod_short.md)].

Existuje výrobní zakázka na 15 Ks zboží LS-100. Některé ze seznamu komponent musí být spotřebovány ručně v deníku spotřeby a ostatní zboží na seznamu může být vyskladněné a spotřeovaná pomocí metody **Vyskladnění + Zpětně**.

> [!NOTE]  
> **Vyskladnění + Zpětné** funguje pouze v případě, když řádek TNG postupu používá kód řádku TNG. Vydání plánované výrobní zakázky inicializuje spotřebu komponent nastavenou na **Vyskladnění + předem**. Spotřeba však nemůže probíhat, dokud není zapsáno vyskladnění komponent, což se opět může uskutečnit pouze po vydání objednávky.

Následující kroky popisují související akce různých uživatelů a odpovídající odpověď:

1. Vedoucí dílny uvolní výrobní zakázku. Zboží se spotřebou **Předem** a bez řádku TNG postupu se odečítají z přihrádek dílny.
2. Vedoucí dílny zvolí funkci **Vytvořit vyskladnění** na výrobní zakázce. Doklad vyskladnění je vytvořen pro vyskladnění s následující metodou spotřeby **Ruční**, **Vyskladnění + Zpětné** a **Vyskladnění + předem**. Tyto položky jsou umístěny do přihrádky výroby.
3. Správce skladu přiřadí vyskladnění skladníkovi.
4. Pracovník skladu vyskladní zboží z příslušných přihrádek a umístí je do přihrádky výroby nebo do přihrádky určené ve vyskladnění, což může být přihrádka pracovního nebo strojního centra.
5. Pracovník skladu zapíše vyskladnění. Množství se odečte z přihrádek pro vyskladnění a přidá se do přihrádky spotřeby. Pole **Vyskladněné množství** na přehledu komponent je pro všechno zboží aktualizováno.

   > [!NOTE]  
   > Spotřebovat lze pouze vyskladněné množství.

6. Obsluha stroje informuje vedoucího výroby, že koncové zboží je hotovo.
7. Vedoucí dílny používá deník spotřeby nebo deník výroby k zaúčtování spotřeby položek komponent, které používají metodu **Ruční** nebo **Předem** nebo **Vyskladnění + Předem** společně s kódem řádku TNG postupu.
8. Vedoucí výroby zaúčtuje výstup výrobní zakázky a změní stav na **Dokončeno**. Množství položek komponent, které používají metodu **Zpětné** spořeby se odečte z přihrádky dílny a množství položek komponent, které používají metodu **Vyskladnění + Zpětné** je odečte z přihrádly výroby.

Následující obrázek ukazuje, když je pole **Kód přihrádky** v seznamu komponent vyplněno podle umístění nebo nastavení strojního/pracovního centra.

![Přehled, kdy a jak je vyplněno pole Kód přihrádky](media/binflow.png "Přehled, kdy a jak je vyplněno pole Kód přihrádky")

## Viz také
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]