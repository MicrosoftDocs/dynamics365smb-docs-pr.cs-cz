---
title: Czech Local Functionality - Automatic Creation and Update of Dimensions
description: This section describes local functionality - Automatic creation and update of dimensions in the Czech version of Business Central.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Finance, Localization, CZ
ms.date: 06/17/2021
ms.reviewer: v-pejano
ms.author: v-makune
---

# Automatické vytváření a aktualizace dimenzí

Umožňuje nastavit automatické vytváření výchozích hodnot dimenzí dle předem stanovených parametrů.

## Nastavení vytváření a aktualizace dimenzí

Nastavení vytváření a akualizace dimnezí se nastavuje dle následujících kroků:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dimenze** a poté vyberte související odkaz.
1. Založte novou dimenzi.
1. Vyberte řádek s novou dimenzí klikněte na tlačítko **Výchozí dimenze typu účtu**.
1. Do pole **ID tabulky** zadejte číslo tabulky.
1. V poli **Účtování hodnoty** vyberte **Kód nutný**. Tímto krokem se nastaví nutnost vyplnění dimenze při účtování záznamu tabulky.
1. Dále vyberte pole **Automaticky vytvořit**. Po tomto nastavení se po založení nového záznamu založí i nová dimenze.
1. Pro nastavení popisu dimenze, aby se neevidovali pouze čísla nebo kódy, slouží pole **ID pole popisu dimenze**. Zde vyberte pole, například číslo **3 - Popis**.
1. Další krokem nastavení je **Aktualizace popisu dimenze** s možností ***Aktualizovat nebo Vytvořit***. V prvním případě se bude automaticky měnit popis dimenze podle popisu záznamu. V druhém případě se název nebude měnit, pokud se ručně přepíše název dimenze.
1. V tento okamžik při založení záznamu, se do popisu dimenze přenese popis záznamu.
1. Pokud chcete nastavit šablonu popisu dimenze, použijte pole **Formát popisu dimenze**, kde například můžete použít ***"Záznam - %1"***.
1. Pokud chcete účtovat v rámci záznamu vždy s nově založenou dimenzí, nastavte v poli **Účtování hodnoty pro automatické vytváření** možnost **Stejný kód**.
1. Pokud chcete doplnit dimenze k  již existujícím projektům, dle nového nastavní, použijte funkci  **Aktualizovat aut. výchozí dimenze** na přehledu **Výchozí dimenze typu účtu**.

## Použití, vytváření a aktualizace dimenzí

Jako příklad si nastavení a použití ukážeme na projektech.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dimenze** a poté vyberte související odkaz.
1. **Založte novou dimenzi** například s názvem *"Projekt"*.
1. Vyberte řádek s dimenzí **Projekt** klikněte na tlačítko **Výchozí dimenze typu účtu**.
1. Do pole **ID tabulky** zadejte číslo **167** (Projekty).
1. V poli **Účtování hodnoty** vyberte **Kód nutný**. Tímto krokem se nastaví nutnost vyplnění dimenze při účtování na projektu.
1. Dále vyberte pole **Automaticky vytvořit**. Po tomto nastavení se po založení nového projektu založí i nová dimenze.
1. Pro nastavení popisu dimenze, aby se neevidovali pouze čísla nebo kódy, slouží pole **ID pole popisu dimenze**. Zde vyberte pole číslo **3 - Popis**.
1. Další krokem nastavení je **Aktualizace popisu dimenze** s možností ***Aktualizovat nebo Vytvořit***. V prvním případě se bude automaticky měnit popis dimenze podle popisu projektu. V druhém případě se název nebude měnit, pokud se ručně přepíše název dimenze.
1. V tento okamžik při založení projektu, se do popisu dimenze přenese popis projektu.
1. Pokud chcete nastavit šablonu popisu dimenze, použijte pole **Formát popisu dimenze**, kde například můžete použít ***"Projekt - %1"***. Nyní při založení projektu "Výrobní linka" bude název dimenze *"Projekt - Výrobní linka"* 
1. Pokud chcete účtovat v rámci projektu vždy s nově založenou dimenzí, nastavte v poli **Účtování hodnoty pro automatické vytváření** možnost **Stejný kód**.
1. Pokud chcete doplnit dimenze k  již existujícím projektům, dle nového nastavní, použijte funkci  **Aktualizovat aut. výchozí dimenze** na přehledu **Výchozí dimenze typu účtu**.
1. Po nastavení přehledy zavřete.

## Viz Také

[Rozšířený lokalizační balíček pro Česko](ui-extensions-advanced-localization-pack-cz.md)  
[Česká lokální funkcionalita](czech-local-functionality.md)
