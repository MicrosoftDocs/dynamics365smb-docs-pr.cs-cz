---
title: Bookmark a link to a page or report on your Role Center | Microsoft Docs
description: Learn how to add a link to your Role Center.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 02/12/2020
ms.author: sgroespe
---

# Záložka stránky nebo sestavy v Centru rolí
Pomocí ikony záložky můžete přidat akci, která otevře stránku nebo sestavu z navigační nabídky Centra rolí. To vám umožní rychle dosáhnout vašeho oblíbeného obsahu nebo obchodních úkolů. Záložku přidáte z cílové stránky nebo sestavy, což znamená obrazovku, která se má otevřít z odkazu v Centru rolí.

Ikona záložky se zobrazí v pravém horním rohu stránky a také v okně **Řekněte mi**, kde můžete efektivně přidat do záložek více stránek nebo sestav. Pokud záložka již pro stránku existuje, ikona je tmavá a popis s nápisem "Uloženo jako záložka".

## Uložení cílové stránky jako záložky
1. Otevřete jakoukoli stránku, na kterou chcete odkaz ve svém Centru rolí.
2. Zvolte ikonu ![Záložky](media/ui_bookmark_icon.png "Přidat záložku do svého centra rolí") .

Akce pojmenovaná po stránce je nyní přidána do navigační nabídky v Centru rolí.

## Uložení vybrané sestavy jako záložky
1. Otevřete libovolnou stránku před spuštěním sestavy, kterou chcete v Centru rolí odkazovat.
2. Zvolte ikonu ![Záložky](media/ui_bookmark_icon.png "Přidat záložku do svého centra rolí") .

Akce pojmenovaná po sestavě je nyní přidána do navigační nabídky v Centru rolí.

## Vytvoření záložky stránky nebo sestavy z okna Řekněte mi
1. Otevřete okno **Řekněte mi** a vložte například **Prodejní objednávky**.
2. Najeďte myší na výsledek vyhledávání pro stránku nebo sestavu **Prodejní objednávky** a poté zvolte ikonu ![Záložky](media/ui_bookmark_icon.png "Přidat záložku do svého centra rolí") icon.

Akce pojmenovaná po stránce nebo sestavě je nyní přidána do navigační nabídky v Centru rolí.


## Často kladené otázky

- **Můžu přeskládávat svoje záložky?**  
   Ano. Můžete přizpůsobit své Centrum rolí a přesunout akce do optimálnější sekce nebo je přesunout do stávajících skupin nebo podskupin.  
   Naučte se jak [Úprava Vašeho pracovního prostředí](ui-personalization-user.md).

- **Jak odstraním záložku?**  
   Na cílové stránce nebo přehledu znovu vyberte ikonu záložky a odeberte příslušnou akci z Centra rolí. Centrum rolí můžete také přizpůsobit a dočasně skrýt akce, aniž byste je zcela odstranili.

- **Kde najdu svoje záložky?**  
   Při přidávání záložky na stránku nebo sestavu se nová akce přidá do horní navigační nabídky na aktuální domovské obrazovce (Centrum rolí). Pokud máte mnoho akcí, možná budete muset zmáčknout tlačítko **Více**, abyste je zobrazili, protože nová akce je vždy přidána na konci těchto akcí.
<!-- Should we add a screenshot here? -->

- **Nemám ikonu záložky. Je něco špatně?**  
   Možnost označit stránku nebo sestavu záložkou je jednou z mnoha funkcí personalizace uživatelů v Business Central. Pokud není ikona záložky zobrazena je pravděpodobné, že správce zakázal přizpůsobení.

- **Proč nemůžu záložkovat vybranou stránku nebo sestavu?**  
   Ne všechny stránky a sestavy mohou být záložkovány. Pokud je stránka nebo sestava spuštěna v nějakém zvláštním kontextu, která se řídí obchodní aplikací, ikona záložky se nezobrazí. Například stránky, které nelze nalézt v okně **Řekněte mi**, ale jsou spuštěny odjinud, nezobrazí ikonu záložky. Podobně stránky návrhu sestavy, které se používají pouze ke shromažďování filtrů bez spuštění sestavy, nezobrazí ikonu záložky.

Viz technické podrobnosti o [RunRequestPage](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) a [FilterPageBuilder](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **Budou vymazány moje záložky při mazání perzonalizace?**  
   Ano. Záložky jsou umístěny v navigační nabídce. Pokud odstraníte změny v navigační nabídce na jakékoli stránce nebo zrušíte veškerou personalizaci v Centru rolí, budou všechny vaše záložky trvale odstraněny.

- **Proč ikona záložky stále označuje, že stále není označena záložkou?**  
   Když přidáte záložku, nová akce bude přidána do navigační nabídky v Centru rolí a při následné návštěvě stránky nebo přehledu bude ikona záložky tmavá. Pokud centrum rolí přizpůsobíte a změníte uspořádání akcí přesunutím do skupin, ikona záložky už nebude tmavá a na stejnou stránku nebo sestavu můžete přidat další záložku. To umožňuje přidat více akcí na stejnou stránku nebo sestavu a kategorizovat je do různých skupin.

- **Proč se v mém odkazu na sestava zobrazuje jiná sestava?**  
   Po použití rozšíření na Business Central mohou být některé sestavy nahrazeny jinými. Dojde-li k nahrazení, text nové akce není aktualizován a bude nadále zobrazovat název původní sestavy, ale přejde do novější sestavy. Chcete-li opravit text nové akce, můžete novou akci odebrat a přidat ji znovu.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **Je záložka dostupná pro XMLporty?**  
   Ne. V současné době není z uživatelského rozhraní možné přidávat akce k otevření XMLportů.

- **Budou mé záložky přeloženy, když změním jazyk v Business Central?**  
   Když přidáte novou akci, použije se při vytváření záložek jakýkoli přeložený text, který byl v té době k dispozici. Pokud je později přidán nový přeložený text, nová akce nebude obsahovat novější překlady.


## Viz také
[Úprava Vašeho pracovního prostředí](ui-personalization-user.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Změna záklandího nastavení](ui-change-basic-settings.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)
