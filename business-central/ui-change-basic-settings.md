---
title: Viewing and Editing Basic Settings | Microsoft Docs
description: Learn how to change some basic settings, for example, the Role Center, company, or the work date.
author: SusanneWindfeldPedersen

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 04/01/2019
ms.author: solsen

---
# Změna základního nastavení
V okně [**Má nastavení**](https://businesscentral.dynamics.com?page=9176 " přejdete přímo na stránku uživatelského nastavení uživatele na stránce Business Central ") a můžete zobrazit a změnit základní nastavení aplikace [!INCLUDE[d365fin](includes/d365fin_md.md)]. Změny, které provedete, ovlivní pouze váš pracovní prostor; ne pracovní prostory ostatních uživatelů.

## <a name="role-center">Centrum rolí</a>
Centrum rolí představuje domovskou stránku, úvodní obrazovku, která je navržena pro potřeby určité role v organizaci. V závislosti na vaší roli vám Centrum rolí poskytuje přehled o firmě, vašem oddělení nebo vašich osobních úkolech. Pomáhá také při procházení každodenních úkolů a při hledání práce, která vám byla přidělena.

- Navigace v horní části umožňuje přepínat mezi zákazníky, prodejci, zbožím a dalšími důležitými seznamy informací. Podobně akce umožňují iniciovat úlohy, jako je například vytvoření nové prodejní faktury, přímo z centra rolí.

- Uprostřed najdete **Aktivity**. Činnosti ukazují aktuální data a lze na ně kliknout a zobrazit podrobnější informace. Klíčové ukazatele výkonu (KPI) lze nastavit tak, aby zobrazovaly vybraný graf pro vizuální znázornění například peněžních toků nebo příjmů a výdajů. Můžete také vytvořit seznam oblíbených zákazníků na domovské stránce pro obchodní vztahy, s nimiž obchodujete často nebo potřebujete věnovat zvláštní pozornost.

### Změna Centra rolí
Výchozí centrum rolí je **Obchodní ředitel**, ale můžete si zvoli jiné Centrum rolí, které bude více vyhovovat vašim potřebám.
1. V pravém horním rohu zvolte **Nastavení** ikonu nastavení ![ Nastavení ikon ](media/ui-experience/settings_icon_small.png " pro Centrum rolí ") a pak zvolte **Moje nastavení** .
2. Na stránce **Má nastavení**, v poli **Centrum rolí**, vyberte roli, kterou chcete jako standardní. Například vyberte **Účetní**.
3. Klikněte na tlačítko **OK**.

## <a name="company"></a>Společnost
Společnost funguje jako úložiště pro data v [!INCLUDE[d365fin](includes/d365fin_md.md)]. V databázi může existovat více společností, ale v jednom okamžiku lze vybrat pouze jednu.

Výchozí společnost se nazývá CRONUS a obsahuje pouze demonstrační data.

> [!TIP]
> Pokud chcete v aplikaci zobrazit jiné jméno vaší společnosti (například v Centru rolí), nastavte pole **Název** na stránce **Informace o společnosti** nebo pole **Zobrazovaný název** na stránce **Společnosti**.

## <a name="work-date"></a>Pracovní datum
Výchozí pracovní datum je obvykle dnešní datum. Možná budete muset dočasně změnit pracovní datum, abyste mohli provádět úkoly, jako je dokončení transakcí k datu, které není aktuálním datem.

> [!TIP]
> Napište **w** k rychlému zadání datumu v políčku s datumem. Napište **t** k rychlému zadání aktuálního data.

>  [!IMPORTANT]
> Pokud změníte pracovní datum a odhlásíte se nebo přepnete na jinou společnost, pracovní datum se vrátí na výchozí pracovní datum. Takže při příštím přihlášení nebo přepnutí zpět na původní společnost bude možná nutné znovu nastavit pracovní datum.

### Indikace pracovního data
<!--
Whenever the work date is not set to the current day (today), there are two indicators on pages that you open for editing:

- A reminder appears at the top of the page that tells you what the work date is set to. The reminder provides a direct link to the work date setting on the **My Settings** page so you change the date if you want. From the reminder, you can also choose to dismiss the reminder for the rest of your session. Unless you change the work date to "today", the reminder will appear the next time you sign in. 

- If you dismiss the reminder, the work date will appear in the title of the page.  
-->
Pokud pracovní datum není nastaveno na aktuální den (dnes), pak se na všech stránkách, kde můžete upravovat data, zobrazuje aktuální pracovní datum v levém horním rohu stránky.

## <a name="region"></a> Oblasti

**Oblasti** určují, jak jsou data, časy, čísla a měny zobrazeny nebo formátovány.


## <a name="language"></a> Jazyk
Změní zobrazovaný jazyk. Toto pole se zobrazí, pouze pokud je k dispozici více než jeden jazyk.

Počáteční jazyk je určen administrátorem nebo nastavením vašeho prohlížeče, když se zaregistrujete pro [! INCLUDE[d365fin](includes/d365fin_md.md)]. Jazyk, který nastavíte, bude použit na všech zařízeních, ze kterých se přihlašujete, jako je telefon nebo tablet.

## Změna příjmu oznámení
Tento odkaz slouží k zobrazení nebo změně oznámení týkajících se určitých událostí nebo změn stavu, například pokud se chystáte fakturovat zákazníkovi, který má splatné saldo, nebo jsou dostupné zásoby nižší než množství, které chcete prodat. Další informace naleznete v části [Chytrá oznámení](ui-smart-notifications.md).

## Viz také
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)
