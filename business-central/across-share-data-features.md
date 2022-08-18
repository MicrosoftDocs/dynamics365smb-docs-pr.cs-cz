---
title: Sharing Data
description: Learn about the different ways to share business data from Business Central. 
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords:
ms.date: 04/01/2022
ms.author: jswymer
---
# Sdílení obchodních dat z Business Central

Spolupráce mezi lidmi uvnitř i mimo organizaci je nedílnou součástí většiny podniků. [!INCLUDE[prod_short](includes/prod_short.md)] nabízí několik funkcí pro sdílení obchodních dat, jako je evidence záznamů, konkrétních záznamů nebo dokladů. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Se všemi těmito funkcemi je přístup k datům chráněn licencí a oprávněními Business Central.

## Kopírování odkazu

![Podporováno](media/check.png) Business Central Online ![Podporováno](media/check.png) Business Central On-premises

Z libovolné stránky můžete zkopírovat adresu URL stránky a pak ji vložit a distribuovat v jiných formách médií, jako jsou e-maily, chaty v Teams nebo textové zprávy. Nejjednodušší způsob, jak zkopírovat odkaz, je vybrat **Sdílet** > **Kopírovat odkaz** v horní části stránky. Dalším způsobem je zkopírovat URL přímo z adresního pole prohlížeče.

### Úprava odkazu na stránku

Po zkopírování odkazu můžete před jeho odesláním upravit adresu URL a ovlivnit tak, co se zobrazí při otevření stránky. Můžete například přidat filtry nebo určit jinou společnost.

Pro více informací navštivte  [Web Client URL](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### Filtrované seznamy

Pomocí podokna filtrů na stránkách seznamu můžete použít filtry k zúžení záznamů zobrazených v seznamu. Pokud použijete akci **Kopírovat odkaz** nebo zkopírujete adresu URL z prohlížeče, odkaz na stránku nebude obsahovat změny filtru. Uživatelé, kteří odkaz otevřou, uvidí všechny záznamy. Způsob, jak zachovat filtrování na odkazu na stránku kolekce, je nejprve uložit filtrovanou stránku jako **Přehled**. Poté otevřete zobrazení a zkopírujte odkaz odtud.

Pro více infortmací navštivte [Řazení, Vyhledávání a Seznam filtrování](ui-enter-criteria-filters.md).

## Sdílení s Teams

![Podporováno](media/check.png) Business Central Online ![Není Podporováno](media/x-icon.png) Business Central On-premises

Přímo z většiny stránek sbírky a stránek s podrobnostmi můžete poslat odkaz na stránku lidem, do skupinových chatů nebo kanálů. Můžete například sdílet odkaz na filtrované zobrazení záznamů. Příjemci pak vyberou odkaz a otevřou stránku v Business Central.

Pro více informací navštivte [Sdílení záznamů a odkazů na stránky pomocí Teams](across-working-with-teams.md).

## Sdílení přes OneDrive

![Podporováno](media/check.png) Business Central Online ![Podporováno](media/check.png) Business Central On-premises

Business Central usnadňuje ukládání, správu a sdílení souborů s ostatními lidmi prostřednictvím OneDrivu pro firmy. Na většině stránek, kde jsou dostupné soubory, jako je Schránka sestav nebo soubory připojené k záznamům, najdete akce **Otevřít na OneDrivu** a **Sdílet**. Obě akce uloží kopii souboru na OneDrive. Jakmile budete na OneDrive, můžete u souboru používat jeho funkce sdílení a příspěvků Rozdíl v akcích spočívá v tom, že **Otevřít ve službě OneDrive** otevře soubor ve službě OneDrive. Funkce **Sdílet** otevře stránku, na které vyberete, který soubor chcete sdílet. Příjemci obdrží e-mail s oznámením o přístupu k souboru z vašeho OneDrivu.

Pro více informací navštivte [Sdílení souborů na OneDrivu](across-share-onedrive.md).

## Otevření v aplikaci Excel

![Podporováno](media/check.png) Business Central Online ![Podporováno](media/check.png) Business Central On-premises

Pro stránky seznamů a seznamy vložené do stránky můžete použít akci **Otevřít v aplikaci Excel**. Tato akce exportuje seznam záznamů do sešitu aplikace Excel (.xlsx souboru), který můžete sdílet s ostatními. V sešitu můžete také použít funkci sdílení, která je součástí Excelu.

Pro více informací navštivte [Zobrazení a úpravy v aplikaci Excel](across-work-with-excel.md).

## Sdílení řádků nebo tabulek

![Podporováno](media/check.png) Business Central Online ![Podporováno](media/check.png) Business Central On-premises

V seznamu můžete sdílet jeden nebo více záznamů. Pro zkopírování do schránky stačí stisknout klávesovou zkratku Ctrl+C. Poté vložte to, co jste zkopírovali, do jiné aplikace stisknutím Ctrl+V. Například zkopírováním tří prodejních objednávek a jejich vložením do e-mailu se objednávky zobrazí v pěkně formátované tabulce.

Pro více informací navštivte [Nejčastější dotazy ke kopírování a vkládání](faq-copy-paste.yml).

## Viz také

[Integrace Business Central a OneDrive](across-onedrive-overview.md)  
[Správa integrace OneDrive s Business Central](admin-onedrive-integration.md)  
[Nejčastější dotazy k OneDrive](admin-onedrive-faq.md)