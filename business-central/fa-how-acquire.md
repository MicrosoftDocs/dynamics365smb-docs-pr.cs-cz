---
title: Acquire Fixed Assets| Microsoft Docs
description: You can set up a fixed asset, assign a depreciation book, and record the fixed asset’s acquisition cost.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 04/01/2020
ms.author: sgroespe

---
# Pořízení dlouhodobého majetku
Pro každý dlouhodobý majetek je nutné nastavit kartu obsahující informace o majetku. Budovy nebo výrobní zařízení můžete nastavit jako hlavní aktivum se seznamem součástí a můžete je seskupit různými způsoby, například podle třídy, oddělení nebo umístění. Před získáním musí být kniha odpisů nastavena a přiřazena ke každému dlouhodobému majetku.

Při nastavení dlouhodobého majetku a přiřazení knihy odpisů musíte dlouhodobý majetek získat. Chcete-li získat dlouhodobý majetek, zaznamenáte jeho pořizovací cenu na příslušný finanční účet, bankovní účet nebo dodavatele zaúčtováním pořizovací transakce ze stránky **Finanční deník DM**. Na stránce **Asistované pořízení dlouhodobého majetku** můžete automaticky vytvořit a zaúčtovat požadované řádky finančního deníku.

Hodnota při vyřazení je zbytková hodnota dlouhodobého majetku, pokud jej již nelze použít. Zůstatkovou hodnotu můžete zaúčtovat současně s účtováním pořizovací ceny. Pro více informací navštivte [Odpis nebo amortizace dlouhodobého majetku](fa-how-depreciate-amortize.md).

Indexace se používá k úpravě hodnot pro obecné změny cenové hladiny. Dávkovou úlohu **Indexace dlouhodobého majetku** lze použít k výpočtu nákladů na pořízení při reprodukčních nákladech.

## Vytvoření dlouhodobého majetku a jeho automatického získání
Následující postup popisuje, jak vytvořit dlouhodobý majetek a poté jej získat pomocí stránky **Asistované pořízení dlouhodobého majetku** k vytvoření a zaúčtování požadovaných řádků finančního deníku dlouhodobého majetku. Řádky deníku můžete také vytvořit a zaúčtovat ručně. Pro více informací navštivte [Ruční zaúčtování pořízení dlouhodobého majetku pomocí finančního deníku dlouhodobého majetku](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dlouhodobý majetek** a poté vyberte související odkaz.
2. Vyberte akci **Nový** a podle potřeby vyplňte pole na záložce **Obecné**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Na záložce **Kniha odpisů** vyplňte pole podle potřeby. Tento krok přiřadí knihu odpisů dlouhodobému majetku.
4. Pokud potřebujete dlouhodobému majetku přiřadit více než jednu knihu odpisů, vyberte akci **Přidat více knih odpisů**. Pro více informací navštivte [Přiřazení knihy odpisů k dlouhodobému majetku](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

   Když jsou vyplněna všechna pole potřebná k pořízení dlouhodobého majetku, tak **Jste připraven k pořízení dlouhodobého majetku. Oznámení o pořízení** se zobrazí v horní části stránky.
5. V oznámení vyberte akci **Získat**.
6. Postupujte podle pokynů na stránce **Asistované pořízení dlouhodobého majetku** a dokončete automatické pořízení dlouhodobého majetku.

> [!NOTE]
> Můžete také účtovat pořizovací náklady na stranu Dal. V takovém případě nezapomeňte, že hodnota v poli **Pořizovací náklady včetně  DPH** musí být se znaménkem mínus, které označuje stranu Dal.

Když zvolíte **Dokončit**, vyplní se pole **Účetní hodnota** na stránce **Karta DM**, což znamená, že dlouhodobý majetek byl získán za zadané náklady na pořízení.

## Nastavení seznamu komponent pro hlavní majetek
Svůj dlouhodobý majetek můžete seskupit do hlavních aktiv a jejich součástí. Můžete mít například výrobní stroj, který se skládá z mnoha částí, které chcete tímto způsobem seskupit.

Hlavní aktivum i všechny jeho komponenty musí být nastaveny jako jednotlivé karty dlouhodobého majetku. Po nastavení seznamu komponent [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky vyplní pole **Hlavní aktiva/komponenta** a **Komponenty hlavního majetku** na kartách dlouhodobého majetku.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dlouhodobý majetek** a poté vyberte související odkaz.
2. Vyberte dlouhodobý majetek, který je hlavním aktivem, a poté vyberte akci **Komponenty hlavního majetku**.
3. Na stránce **Komponenty hlavního majetku** vyberte pole **Číslo DM**. a vyberte dlouhodobý majetek, který chcete přidat jako součást hlavního majetku.
4. Zavřete stránku.
5. Opakujte kroky 3 a 4 pro každou komponentu, kterou chcete přidat.
6. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení DM** a poté vyberte související odkaz.
7. Zaškrtněte políčko **Povolit účto na hlavní majetek**.

## Ruční zaúčtování pořízení dlouhodobého majetku s finančním deníkem dlouhodobého majetku
Následující postup popisuje, jak získat dlouhodobý majetek ručním vytvořením a zaúčtováním řádků na stránce **Finanční deník DM**. Dlouhodobý majetek můžete také získat automaticky pomocí stránky **Asistované pořízení dlouhodobého majetku**. Pro více informací navštivte krok 5 v [Vytvoření dlouhodobého majetku a jeho automatické získání](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically).

> [!NOTE]
> Můžete také účtovat pořizovací náklady na stranu Dal. V takovém případě mějte na paměti, že hodnota v poli **Částka** musí být se znaménkem mínus pro označení strany Dal.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky DM** a poté vyberte související odkaz.
2. Na stránce **Finanční deník DM** v poli **Typ účtování DM** vyberte **Náklady na pořízení**.
3. Podle potřeby vyplňte zbývající pole.
4. Vyberte akci **Účtovat**.

> [!TIP]
> Pokud vyplníte pole **Číslo pojištění** ve finančním deníku DM při účtování pořizovací ceny, pak [!INCLUDE[d365fin](includes/d365fin_md.md)] také zaúčtuje pořizovací cenu dlouhodobého majetku do knihy pojistného krytí. Pro více informací navštivte [Pojištění dlouhodobého majetku](fa-how-insure.md).

## Zrušení účtování pořizovacích nákladů pro jeden dlouhodobý majetek
Pokud při účtování nákladů na pořízení uděláte chybu, můžete položku odebrat pomocí dávkové úlohy **Storno položek DM** a poté zaúčtovat správnou položku pořízení. Chybné položky se přenesou na stránku **Chybné položky DM**.

Pokud například zaúčtujete pořízení s nesprávným datem, musíte ji co nejdříve opravit, protože se používá zúčtovací datum dlouhodobého majetku, což je mnoho kritických výpočtů.

> [!IMPORTANT]
> Pro položky dlouhodobého majetku nelze použít funkci **Stornovat transakce**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Storno položek DM** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Stisknutím tlačítka **OK** spusťte dávkovou úlohu.
4. Po zrušení nesprávné položky nebo položek pokračujte v účtování správných nákladů na pořízení.

Chcete-li zrušit více položek pro dlouhodobý majetek najednou, použijte dávkovou úlohu **Storno položek DM**.

## Zaúčtování hodnoty při vyřazení spolu s pořizovacími náklady
Hodnotu při vyřazení můžete zaúčtovat společně s náklady na pořízení z deníku dlouhodobého majetku.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky DM** a poté vyberte související odkaz.
2. Na stránce **Deníky dlouhodobého majetku** vytvořte řádek pořízení. Pro více informací navštivte [Ruční zaúčtování pořízení dlouhodobého majetku pomocí finančního deníku dlouhodobého majetku](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. Do pole **Hodnota při vyřazení** na řádku deníku zadejte částku hodnoty při vyřazení jako kredit (se znaménkem mínus).
4. Vyberte akci **Účtovat**.

> [!NOTE]
> Pokud pro dlouhodobý majetek existuje záchranná hodnota, bude tato hodnota použita v účtování o odpisech namísto hodnoty v poli **Konečná účetní hodnota** na stránce **Knihy odpisů DM**. Pro více informací navštivte [Správa koncové účetní hodnoty](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## Viz také
[Dlouhodobý majetek](fa-manage.md)  
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
