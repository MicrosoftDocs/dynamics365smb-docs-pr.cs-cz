---
title: Work with Time Sheets for Jobs| Microsoft Docs
description: Describes how to create a time sheet for a job, copy planning lines to it, define work types, fill in the time sheet, and submit it for approval.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2019
ms.author: sgroespe

---
# Použití pracovních výkazů pro projekty
Pomocí dávkové úlohy **Vytvořit pracovní výkazy** můžete vytvořit pracovní výkazy pro určený počet časových období nebo týdnů. Abyste mohli vytvářet pracovní výkazy, musíte mít oprávnění.

Řádky pro plánování úloh můžete kopírovat a používat v pracovním výkazů. Tímto způsobem musíte zadat pouze informace na jedno místo a informace v řádku jsou vždy správné.

Po schválení položek pracovního výkazu je můžete zaúčtovat do příslušného deníku projektů, nebo deníku zdrojů.

Před použitím pracovních výkazů je nutné nastavit obecné informace a zadat správce a jednoho nebo více schvalovatelů pracovních výkazů. Pro více informací navštivte [Nastavení pracovních výkazů](projects-how-setup-time-sheets.md).

## Vytvoření pracovního výkazu
Pomocí dávkové úlohy **Vytvořit pracovní výkazy** můžete vytvořit pracovní výkazy pro určený počet časových období nebo týdnů. Poté jej může vlastník pracovního výkazu znovu otevřít a zaznamenat čas strávený na úkolu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pracovní výkazy**, a poté vyberte související odkaz.
2. Na stránce **Přehled pracovních výkazů**, vyberte akci **Vytvořit pracovní výkazy**.
3. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Pole **Použij pracovní výkaz** a **ID vlastníka pracovního výkazu** musí být na kartě vyplněna jako zdroj pracovního výkazu.

1. Zvolte tlačítko **OK**.

Pracovní výkazy, které jste vytvořili, můžete zobrazit na stránce **Přehled pracovních výkazů**.

## Kopírování řádků plánování projektu do pracovního výkazu
Následující postup popisuje, jak rychle přidat řádky plánování projektu do pracovního výkazu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pracovní výkazy**, a poté vyberte související odkaz.
2. Na stránce **Přehled pracovních výkazů** vyberte pracovní výkaz pro příslušné časové období a pak zvolte akci **Upravit pracovní výkaz**.
3. Vyberte akci **Vytvořit řádky z plánování projektu**. Všechny řádky plánování projektu v období pracovního výkazu se zkopírují do pracovního výkazu pro osobu nebo stroj v poli **Číslo zdroje** na pracovním výkazu.

## Definování typů práce a přidání do pracovního rozvrhu
Můžete definovat typ práce pro všechny řádky pracovního výkazu pro úlohy. Tímto způsobem můžete přidat informace, které potřebujete zákazníkovi vyúčtovat za různé druhy práce.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pracovní výkazy**, a poté vyberte související odkaz.
2. Otevřete příslušný pracovní výkaz
3. Vyberte pole **Popis**.
4. Na stránce **Detaily řádku projektu prac.výkazu**, vyberte pole **Kód typu práce**, a vyberte ze seznamu typ práce, jako například **Míle**.
5. Pokud neexistují žádné typy práce, vyberte akci **Nový**.
6. Na stránce **Typy práce**, vyplňte pole podle potřeby.
7. Opakujte krok 4 a přiřaďte nový typ práce k pracovnímu výkazu.

## Opětovné použití řádků pracovního výkazu v jiných pracovních výkazech
Pokud informace o pracovním výkazu zůstávají stejné v průběhu časového období, můžete ušetřit čas zkopírováním řádků z předchozího pracovního výkazu. Poté stačí zadat své časové využití pro nové období.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pracovní výkazy**, a poté vyberte související odkaz.
2. Otevřete pracovní výkaz pro období, které je pozdější než období existujícího pracovního výkazu s řádky.
3. Vyberte akci **Kopírovat řádky z předchozího pracovního výkazu**.

Řádky jsou zkopírovány, včetně podrobností, jako je typ a popis. Pokud například řádek souvisí s projektem, je zkopírováno **Číslo projektu**. Všechny zkopírované řádky mají stav **Otevřeno**. Nyní můžete upravit řádky podle potřeby.

## Vyplnění řádků pracovního rozvrhu a odeslání ke schválení
Registrace pracovního výkazu je sledována v hodinách, což je standardní základní měrná jednotka zdrojů. Ve výchozím nastavení jsou v pracovním výkazu uvedeny běžné pracovní dny od pondělí do pátku.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Pracovní výkazy**, a poté vyberte související odkaz.
2. Vyberte pracovní výkaz pro příslušné časové období a pak zvolte akci **Upravit pracovní výkaz**.
3. Vyplňte pole na řádku podle potřeby. Zadejte počet hodin, které zdroj používá každý den v týdnu.

   > [!TIP]
   > Můžete zkontrolovat součet hodin pracovního výkazu, který jste zadali v okně s náhledem **Souhrn skutečnost/rozpočet**.
4. Opakujte krok 3 pro jiné typy práce, které zdroj provádí.
5. Zvolte akci **Odeslat**, a poté zvolte akci **Všechny otevřené řádky** chcete-li odeslat všechny řádky, nebo akci **Pouze vybrané řádky** chcete-li odeslat pouze řádky vybrané na stránce **Pracovní výkaz**.

   > [!NOTE]
   > Můžete zadat pouze řádky výkazů, pro které jste zadali čas.
6. Chcete-li upravit informace na řádku, který byl nastaven na **Odesláno**, vyberte řádek a pak zvolte akci **Znovu otevřít**.

   > [!NOTE]
   > Manažer může odmítnout řádek pracovního výkazu, který je předložen ke schválení. Pokud má řádek stav **Odmítnuto**, můžete na něm provést změny a poté znovu vybrat **Odeslat**.
7. Zvolte tlačítko **OK**.

## Schválení nebo odmítnutí pracovního výkazu
Před použitím musí být ke schválení předložen ke schválení pracovní výkaz. Jednotlivé řádky na pracovním výkazu můžete schválit a odmítnout nebo je odeslat zpět zadavateli k další akci. Pracovní výkaz lze schválit dvěma způsoby:

* Správce pracovního výkazu může schválit libovolný pracovní výkaz
* Osoba, která je zadána v poli **ID schvalovatele pracovního výkazu** na kartě zdroje, může schválit časové rozvrhy zdroje. Pro více informací navštivte [Nastavení pracovních výkazů](projects-how-setup-time-sheets.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Správce pracovních výkazů**, a poté vyberte související odkaz.
2. Vyberte ze seznamu pracovní výkaz.
3. Na stránce **Pracovní výkazy** vyberte akci **Schválit** a poté vyberte akci **Všechny odeslané řádky**, abyste schválili všechny řádky, nebo akci **Vybraný řádek pouze** ke schválení pouze řádků vybraných na stránce **Pracovní výkaz**.
4. Zvolte tlačítko **OK**.
5. Případně vyberte akci **Odmítnout** a postupujte podle kroků 4 až 5.

> [!TIP]
> Použijte informační okna**Stav pracovního výkazu** a **Souhrn skutečnost/rozpočet** k získání přehledu informací o pracovním výkazu.

Poté, co jste schválili nebo odmítli pracovní výkaz, nelze jej změnit, pokud není poprvé znovu otevřen. Následující postup vysvětluje, jak znovu otevřít schválený nebo odmítnutý výkaz.

## Opětovné otevření pracovního výkazu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Správce pracovních výkazů**, nebo **Pracovní výkazy** a poté vyberte související odkaz.
2. Otevřete ze seznamu pracovní výkaz.

   > [!NOTE]
   > Znovu otevřít lze pouze řádky se stavem **Schváleno**. Nelze znovu otevřít řádky se stavem **Odmítnuto**. Nemůžete znovu otevřít pracovní výkaz, pokud byl zveřejněn.
3. Na stránce **Pracovní výkazy**, zvolte akci **Znovu otevřít**, a poté vyberte akci **Všechny odeslané řádky** abyste otevřeli všechny řádky, nebo akci **Vybraný řádek pouze** ke schválení pouze řádků vybraných na stránce **Pracovní výkaz**.
4. Zvolte tlačítko **OK**. Stav řádku nebo řádků pracovních výkazů se změní na **Odesláno**.

## Zaúčtování řádků pracovního výkazu v deníku zdrojů
Po schválení položek pracovní výkazu můžete zdroje zaúčtovat do příslušného deníku zdrojů.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deník zdrojů** a poté vyberte související odkaz.
2. Vyberte akci **Navrhni řádky z pracovního výkazu**.
3. Vyplňte pole podle potřeby.
4. Zvolte tlačítko **OK**. Položky pro použití jsou vytvořeny v deníku zdrojů, kde můžete podle potřeby upravit informace.
5. Vyberte akci **Účtovat**.
6. Chcete-li účtování ověřit, zvolte **Položky hlavní knihy**. Stránka **Položky zdrojů** zobrazuje výsledek zaúčtování deníku zdrojů.

## Zaúčtování řádků pracovního výkazu do deníku projektů
Poté, co jste pro úlohu schválili položky pracovního výkazu, můžete je zveřejnit v příslušném deníku úloh.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky projektů** a poté vyberte související odkaz.
2. Vyberte akci **Navrhni řádky z pracovního výkazu**.
3. Vyplňte pole podle potřeby.
4. Zvolte tlačítko **OK**. Položky pro použití jsou vytvářeny v deníku úloh, kde můžete informace podle potřeby upravovat.

   > [!NOTE]
   > Informace o typu práce a o tom, zda je práce fakturovatelná, jsou zkopírovány z řádku pracovního výkazu. V případě potřeby můžete snížit počet hodin a provést částečné zaúčtování. Pokud snížíte množství, při příštím zvolení akce **Navrhni řádky z pracovního výkazu**, bude vytvořený řádek obsahovat zbývající počet hodin.
5. Vyberte akci **Účtovat**.
6. Chcete-li účtování ověřit, zvolte **Položky hlavní knihy**. Stránka **Položky projektu** se otevře, zobrazující výsledek zaúčtování deníku zdrojů.

## Archivace pracovních výkazů
Po zaúčtování pracovních výkazů je můžete archivovat pro budoucí použití. Před archivací pracovních výkazů musí být zaúčtovány všechny řádky pracovních výkazů.

> [!NOTE]
>  Když archivujete pracovní výkaz, bude odstraněn ze seznamů na stránce **Pracovní výkazy** a stránce **Správce pracovních výkazů**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Správce pracovních výkazů**, a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole a poté zvolte tlačítko **OK**.
3. Chcete-li zkontrolovat archivované pracovní výkazy, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Archivy pracovních výkazů**, nebo **Správce pracovních výkazů** a poté vyberte související odkaz.

## Viz také
[Správa projektů](projects-manage-projects.md)  
[Nastavení správy projektu](projects-setup-projects.md)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
