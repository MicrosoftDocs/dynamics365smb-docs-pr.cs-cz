---
title: Prohlížení a úpravy základních nastavení | Microsoft Docs
description: 'Naučte se, jak změnit některá základní nastavení, například Centrum rolí, společnost nebo pracovní datum.'
author: ZdenekBicek

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'change Role Center, notification, change company, change work date'
ms.date: 01/14/2020
ms.reviewer: v-zdbice
ms.author: sgroespe
---
# Změna základního nastavení

Na stránce **Má nastavení**, můžete zobrazit a změnit základní nastavení pro [!INCLUDE[d365fin](includes/d365fin_md.md)]. Změny, které provedete, ovlivní pouze vaše pracovní prostředí a ne pracovní prostředí ostatních uživatelů.  

## <a name="role-center"></a> Centrum rolí

Centrum rolí představuje domovskou stránku, úvodní obrazovku, která je navržena pro potřeby konkrétní role v organizaci. V závislosti na vaší roli vám Centrum rolí poskytuje přehled o firmě, vašem oddělení nebo vašich osobních úkolech. Pomáhá také navigovat k vašim každodenním úkolům a najít práci, která je vám přiřazena.

- Navigace v horní části umožňuje přepínat mezi zákazníky, dodavateli, zbožím a dalšími důležitými seznamy informací. Akce také umožňují iniciovat úlohy, například vytvořit novou prodejní fakturu, přímo z centra rolí.

- V centru rolí najdete **Aktivity**. Aktivity ukazují aktuální data a lze na ně kliknout nebo klepnout a zobrazit podrobnější informace. Klíčové ukazatele výkonu lze nastavit tak, aby zobrazovaly vybraný graf pro vizuální znázornění například peněžních toků nebo příjmů a výdajů. Na domovské stránce si také můžete vytvořit seznam oblíbených zákazníků, se kterými často obchodujete nebo kterým potřebujete věnovat zvláštní pozornost.

### <a name="to-change-role-center"></a>Chcete-li změnit Centrum rolí

Výchozí Centrum rolí je **Obchodní ředitel**, ale můžete si vybrat jiné Centrum rolí, které lépe vyhovuje vašim potřebám.

1. V pravém horním rohu vyberte ikonu **Nastavení** ![Settings](media/ui-experience/settings_icon_small.png "Ikona nastavení pro Centrum rolí"), a vyberte **Má nastavení**.
2. Na stránce **Má nastavení**, v poli **Role**, vyberte Centrum rolí, které chcete nastavit jako standardní. Například vyberte **Účtárna**.
3. Potvrďte výběr tlačítkem **OK**.

## <a name="company"></a>Společnost

Společnost funguje jako úložiště pro data v [!INCLUDE[d365fin](includes/d365fin_md.md)]. V databázi může být více společností, ale vždy lze vybrat pouze jednu.

Výchozí společnost se nazývá CRONUS a obsahuje pouze demonstrační data.

## <a name="to-change-the-company-name"></a>Změna názvu společnosti

Název společnosti je vždy zobrazen v levém horním rohu a funguje jako akce, kterou se můžete vrátit do centra rolí. Tento název můžete změnit na stránce **Informace o společnosti**.

1. Zvolte ikonu ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Informace o společnosti**, a vyberte odpovídající odkaz.
2. Do pole **Název** zadejte nový název společnosti.
3. Opusťte stránku. Systém se restartuje a zobrazí novou společnost v levém horním rohu.

## Zobrazení značky společnosti pro rychlý přístup k informacím o společnosti

V pravém horním rohu můžete přidat přizpůsobenou značku, při volbě které  se rychle zobrazí jméno společnosti a informace o tenantu v rozbalovacím poli.

1. Zvolte ikonu ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Informace o společnosti**, a vyberte odpovídající odkaz.
2. Na záložce **Značka společnosti** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Pokud je definován odznak společnosti, nemůžete změnit název společnosti, jak je popsáno v [Chcete-li změnit název společnosti](ui-change-basic-settings.md#to-change-the-company-name)

## <a name="work-date"></a>Pracovní datum

Výchozí pracovní datum je obvykle dnešní datum. Možná budete muset dočasně změnit pracovní datum, abyste mohli provádět úkoly, jako je dokončení transakcí k datu, které není aktuálním datem.

> [!TIP]  
> Do všech polí s daty zadejte **d** pro rychlé zadání dnešního data nebo zadejte **p** pro rychlé zadání pracovního data, což je hodnota pole **Pracovní datum** na stránce **Moje nastavení**.

> [!IMPORTANT]  
> Po změně pracovního data, pokud se odhlásíte nebo přepnete na jinou společnost, se pracovní datum vrátí na výchozí pracovní datum. Takže při příštím přihlášení nebo přepnutí zpět na původní společnost bude nutné znovu nastavit pracovní datum.

### Indikace pracovního data

Pokud není pracovní datum nastaveno na dnešní datum, objeví se na stránkách, které lze editovat, a kde je proto pracovní datum kritické, dva typy indikátorů:

- V horní části stránky se zobrazí upozornění, které vám řekne, jaké pracovní datum je nastaveno. Upozornění poskytuje přímý odkaz na nastavení pracovního data na stránce **Moje nastavení**, takže pokud chcete, můžete datum změnit. Z upozornění si můžete také zvolit zrušení upozornění pro zbytek vaší relace. Pokud pracovní datum nezměníte na "dnes", zobrazí se připomenutí při příštím přihlášení.

- Pokud upozornění zrušíte, v názvu stránky se zobrazí pracovní datum.  
-->
Pokud není pracovní datum nastaveno na aktuální den (dnes), pak se na všech stránkách, kde můžete upravovat datum, zobrazuje aktuální pracovní datum v levém horním rohu stránky.

## <a name="region"></a> Oblast

Nastavení **Oblast** určuje, jak jsou zobrazovány nebo formátovány data, časy, čísla a měny.

## <a name="language"></a> Jazyk

Mění jazyk zobrazení. Toto pole se zobrazí, pouze pokud je k dispozici více než jeden jazyk.

Počáteční jazyk je určen administrátorem nebo nastavením vašeho prohlížeče, když se registrujete pro [!INCLUDE[d365fin](includes/d365fin_md.md)]. Jazyk, který nastavíte, bude použit na všech zařízeních, ze kterých se přihlašujete, jako je telefon nebo tablet.

## <a name="changing-when-i-receive-notifications"></a>Změnit, kdy se zobrazí upozornění

Tento odkaz vyberte, chcete-li zobrazit nebo změnit upozornění o určitých událostech nebo změnách stavu, například když se chystáte fakturovat zákazníkovi, který má saldo po lhůtě splatnosti nebo dostupné zásoby jsou nižší než množství, které se chystáte prodat. Další informace naleznete v části [Správa upozornění](ui-smart-notifications.md).

## Viz také

[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
