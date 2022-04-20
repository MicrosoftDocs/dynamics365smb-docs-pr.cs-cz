---
title: Troubleshooting and Correcting Dimensions
description: Learn how to troubleshoot typical dimension errors, and how to correct dimensions after they are used on posted transactions.
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension, correction, correct, business intelligence
ms.search.form: 116, 540, 2588
ms.date: 09/27/2021
ms.author: bholtorf

---

# Odstraňování problémů a oprava dimenzí

Pohledy finančního výkaznictví a analýzy často spoléhají na data z dimenzí. I přes dostupná ochranná opatření se někdy stane chyba, která může vést k nepřesnostem. Toto téma popisuje některé typické chyby a vysvětluje, jak opravit přiřazení dimenzí u zaúčtovaných transakcí, aby byly finanční výkazy přesné.

## Řešení problémů s chybami dimenzí

Při zaúčtování dokladů nebo řádků deníku, které obsahují dimenze, se mohou vyskytnout různé chyby, které však obvykle souvisejí s nesprávným nastavením nebo přiřazením dimenzí.

> [!NOTE]
> V následujícím seznamu možných chybových hlášení jsou kódy *%X* zástupnými znaky pro datové proměnné, které bude skutečné hlášení obsahovat v uživatelském rozhraní v závislosti na kontextu. Například, *%1 %2 je blokobáno.* Může se zobrazit v uživatelském rozhraní jako "Kód dimenze OBLAST je blokováno.".

| Vydání | Chybová zpráva | Možné řešení |
|-----|-------------|-----------------|
| Blokovaná dimenze | %1 %2 je blokováno. | -Najít nezaúčtované doklady obsahující sadu dimenzí s blokovanou dimenzí a odblokovat ji.<br />-Odstranit řádek dimenzí pro blokovanou dimenzi. |
| Odstraněná dimenze | %1 %2 nelze nalézt. | -Obnovte chybějící dimenzi.<br /> -Najděte nezaúčtované doklady obsahující sadu dimenzí s chybějící dimenzí a přidejte ji.<br />-Odstraňte řádek dimenzí pro blokovanou dimenzi. |
| Blokovaná hodnota dimenze | %1 %2 - %3 je blokováno. | -Najděte nezaúčtované doklady obsahující sadu dimenzí s blokovanou hodnotou dimenze a odblokujte ji.<br />-Odstraňte řádek dimenzí pro blokovanou dimenzi. |
| Odstraněná hodnota dimenze | %1 pro %2 chybí. | -Obnovte chybějící hodnotu dimenze.<br />-Najděte nezaúčtované doklady obsahující sadu dimenzí s chybějící hodnotou dimenze a přidejte ji.<br />-Odstraňte řádek dimenzí pro chybějící dimenzi.. |
| Nepovolená hodnota dimenze | Typ hodnoty dimenze pro %1 %2 - %3 nesmí být %4. | -Změňte pole **Typ hodnoty dimenze**na stránce **Hodnoty dimenze** na **Standardní** nebo **Od-součet**.<br />-Odstraňte řádek dimenzí pro blokovanou dimenzi. |
| Blokovaná kombinace dimenzí | Dimenze %1 a %2 nelze použít současně. | -Najděte nezaúčtované doklady obsahující sadu dimenzí s blokovanou kombinací dimenze a odblokujte ji.<br />-Změňte jeden z konfliktích řádků sady opravnění pro kombinanci dimenzí. |
| Blokovaná kombinace hodnot dimenzí | Dimension combinations %1 - %2 and %3 - %4 can't be used concurrently. | -Najděte nezaúčtované doklady obsahující sadu dimenzí s blokovanou kombinací dimenze a odblokujte ji..<br />-Změňte jeden z konfliktích řádků sady opravnění pro kombinanci dimenzí. |
| Prázdný kód hodnoty dimenze pro výchozí dimenzi, kde pole **Účtování hodnoty** obsahuje **Kód nutný** | -Vyberte %1 pro %2 %3.<br />-Vyberte %1 pro %2 %3 pro %4 %5. | -Změňte pole **Účtování hodnoty** na stránce **Výchozí dimenze**.<br />-Zadejte neprázdnou hodnotu dimenze pro konfliktní dimenzi v sadě dimenzí. |
| Nesprávný kód hodnoty dimenze pro výchozí dimenzi, kde pole **Účtování hodnoty** osahuje **Stený kód** | -Vyberte %1 %2 pro %3 %4.<br />-Vyberte %1 %2 pro %3 %4 pro %5 %6. | -Změňte pole **Účtování hodnoty** na stránce **Výchozí dimenze**.<br />-Zadejte požadovanou hodnotu dimenze pro konfliktní dimenzi v sadě dimenzí. |
| Neprázdný kód hodnoty dimenze pro výchozí dimenzi, kde pole **Účtování hodnoty** osahuje **Stený kód** | -%1 %2 musí být prázný.<br />-%1 %2 musí být prázdné pro %3 %4. | -Změňte pole **Účtování hodnoty** na stránce **Výchozí dimenze**.<br />-Zadejte prázdný kód hodnoty dimenze pro konfliktní dimenzi v sadě dimenzí. |
| Neočekávaná hodnota dimenze pro výchozí dimenzi, kde pole **Účtování hodnoty** neobsahuje **Ždáný kód** | -%1 %2 musí být uvedeno.<br />-%1 %2 musí být uvedeno pro %3 %4 | -Změňte pole **Hodnotu účtování** na stránce **Výchozí dimenze**.<br />-Odstraňte konflitkní řádek ze sady dimenzí. |
| Oprava dimenzí neproběhne správně. | -Vyberte **Obnovit** chcete-li vrátit opravu do stavu konceptu. Tím se změny resetují a opravu můžete spustit znovu. |

## Změna přiřazení dimenzí po zaúčtování

Pokud zjistíte, že u zaúčtovaných položek hlavní knihy byla použita nesprávná dimenze, můžete opravit hodnoty dimenzí a aktualizovat zobrazení analýzy. To vám pomůže udržet vaše finanční sestavy a analýzy přesné.

> [!IMPORTANT]
> Funkce pro opravu dimenzí má pouze pomoci zpřesnit finanční výkaznictví. Opravy dimenzí se vztahují pouze na věcné položky. Nemění dimenze přiřazené záznamům v jiných účetních knihách pro stejnou transakci. Dojde k nesouladu mezi dimenzemi přiřazenými v hlavní knize a dílčích knihách.

### Nastavení opravy dimenze

Při nastavování korekcí dimenzí je třeba vzít v úvahu dvě věci:

* Existují dimenze, které nechcete lidem dovolit změnit? Na stránce **Nastavení opravy dimenze** zadejte dimenze, které chcete zablokovat pro změny.
* Komu chcete umožnit změnu dimenzí? Chcete-li uživatelům povolit provádění změn, přiřaďte uživatelům oprávnění **D365 DIM CORRECTION**. Oprávnění jim umožňují vytvářet opravy dimenzí, spouštět je a v případě potřeby je vrátit zpět. Budou také moci určit blokované dimenze. Další informace o oprávněních naleznete v tématu [Přiřazení práv uživatelům a uživatelským skupinám](ui-define-granular-permissions.md).

### Opravy dimenzí

Můžete ručně vybrat jednu nebo více položek hlavní knihy nebo použít filtry k výběru sad položek. V případě potřeby můžete také přidat nebo odstranit dimenze.

1. Chcete-li zahájit opravu dimenzí, použijte jednu z následujících stránek:

   * Na stánce **Finanční žurnály** vyberte žurnál a poté vyberte **Opravy dimenzí**. Tím se spustí oprava položek ve vybraném žurnálu.
   * Na stránce **Věcné položky** vyberte tlačítko **Opravy dimenzí**.

2. V poli **Popis** vložte informace, které chcete změnit. Ostatní lidé si mohou tyto informace později přečíst, aby pochopili, co bylo provedeno.
3. V záložce **Vyberané položky zboží** vyberte příslušné položky.

   > [!IMPORTANT]
   > Při změně výběru se hodnoty na kartě **Změny opravy dimenze** vynulují. Proto vždy vyberte položky před zadáním změn hodnoty dimenze.

   Následující tabulka popisuje možnosti.

   | Možnost | Popis |
   |---------|---------|
   | Přidat související položky | Přidat položky hlavní knihy, které jsou ve stejném finančním žurnálu. |
   | Přidat podle filtru | Při přidávání položek hlavní knihy použije kritéria filtru. |
   | Ruční výběr | Vyberte konkrétní položky hlavní knihy. |
   | Přidat podle dimenzí | Filtrovat položky hlavní knihy podle rozměrů. |
   | Odstranit položky | Zrušte výběr položek zboží. |
   | Správa kritérií výběru | Sledujte proces výběru a v případě potřeby výběr zrušte. |

4. Na záložce **Změny opravy dimenze** vyberte dimenzi, kterou chcete změnit v poli **Kód dimenze** a novou hodnotu v poli **Nový kód dimenze**.
5. Chcete-li ověřit, zda je oprava provedena, zvolte **Ověřit změny dimenzí**. Pro více informací navštivte [Ověřování změn dimenzí](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Zvolte **Spustit**.

### Ověření změn dimenze

Než spustíte opravu, je vhodné ji nejprve ověřit. Ověření kontroluje omezení týkající se účtování hodnot pro účty hlavní knihy, omezení dimenzí a zda jsou hodnoty dimenzí blokovány. Během ověřování je stav opravy nastaven na  **Probíhá ověřování**. Po ověření opravy se výsledek zobrazí v poli **Stav ověření** field. Pokud byly nalezeny chyby, můžete je prozkoumat pomocí akce **Zobrzit chyby**. Po opravě chyby je nutné použít akci **Znovu otevřít** ke spuštění opravy nebo nového ověření.

Opravu můžete buď spustit okamžitě, nebo naplánovat její spuštění na pozdější dobu. Pokud provádíte opravy u velké sady dat, doporučujeme naplánovat její spuštění mimo pracovní dobu. Pro více informací navštivte [Změny dimenzí u velkých datových sad](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### Vracení změn

Pokud se vám po opravě dimenze nelíbí, co vidíte, můžete pomocí akce **Vrátit změnu** obnovit předchozí hodnotu. Vrátit zpět však můžete pouze poslední změnu. Než změnu vrátíte zpět, můžete potvrdit změny, které vrácení provede. To je užitečné například v případě, že se po provedení změny změnila omezení dimenzí.

Pokud akce Vrátit změnu není k dispozici, například proto, že jste provedli mnoho oprav, můžete použít akci **Kopírovat do konceptu** k zahájení nové opravy pro stejné položky.

### Změny dimenzí u velkých datových sad

Buďte opatrní při opravách velkých sad položek, například sad, které obsahují více než 10 000 položek Pokud je to možné, doporučujeme použít filtry ke spuštění oprav na menších sadách dat. Je také vhodné provádět opravy mimo běžnou pracovní dobu

### Použití zobrazení analýzy s opravami dimenzí

Pokud je **Aktualizace při účtování** je povoleno pro zobrazení analýzy, [!INCLUDE[prod_short](includes/prod_short.md)] může zobrazit při zaúčtování dokladů a deníků. Pohledy můžete také aktualizovat s tímto nastavením povoleným výsledky oprav dimenzí. Chcete-li tak učinit, zapněte **Aktualizace pohledů analýzy**. Aktualizace analytických pohledů může mít vliv na výkon, zejména u velkých datových sad, proto doporučujeme aktualizovat analytické pohledy pouze u malých datových sad.

### Zobrazení historických změn dimenzí

Pokud byla položka hlavní knihy opravena, můžete prozkoumat změnu pomocí akce **Historie změn dimenzí**.

### Zpracování neúplných oprav

Pokud se oprava nedokončí, zobrazí se na kartě změny varování. Pokud k tomu dojde, můžete pomocí akce **Obnovit** vrátit opravu do stavu konceptu a vrátit změny zpět. Změnu pak můžete spustit znovu.

> [!NOTE]
> Resetování neúplné opravy neovlivní aktualizace zobrazení pohledů, protože k nim dochází na konci procesu opravy.

### Použití nákladového účetnictví s opravenými položkami hlavní knihy

 opravě dimenzí nebudou data pro nákladové účetnictví synchronizována. Nákladové účetnictví používá dimenze k agregaci částek pro nákladová střediska a objekty nákladů a ke spuštění přidělení nákladů. Změna dimenzí pro položky hlavní knihy bude pravděpodobně znamenat, že znovu spustíte modely nákladového účetnictví. To, jestli potřebujete odstranit jen několik žurnálů nákladů a znovu spustit přidělení, nebo potřebujete odstranit všechno a znovu spustit všechny modely, závisí na datech, která byla aktualizována, a na tom, jak jsou nastaveny možnosti nákladového účetnictví. Musíte ručně určit, kde budou mít opravy dimenzí vliv na nákladové účetnictví a kde jsou potřebné aktualizace. [!INCLUDE[prod_short](includes/prod_short.md)] does not currently provide an automated way to do that.

## Viz také

[Práce s dimenzemi](finance-dimensions.md)
[Analýza dat pomocí Dimenzí](bi-how-analyze-data-dimension.md)
