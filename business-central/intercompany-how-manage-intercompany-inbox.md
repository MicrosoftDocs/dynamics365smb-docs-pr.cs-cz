---
title: Process Incoming and Outgoing IC Transactions| Microsoft Docs
description: Intercompany transactions that you receive from your intercompany partners are listed in the intercompany inbox where you process them manually or automatically.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 10/01/2019
ms.author: sgroespe

---
# Správa vnitropodnikové doručené pošty a pošty k odeslání
Všechny vnitropodnikové transakce, které obdržíte elektronicky od svých vnitropodnikových partnerů, jsou uvedeny ve vnitropodnikové doručené poště.

## Organizace doručené pošty
Pomocí polí filtru v horní části stránky doručené pošty můžete určit, které transakce jsou na stránce zobrazeny. Například pokud se chcete podívat pouze na transakce vytvořené konkrétním partnerem, můžete zadat filtry do **Zdroje transakce** a **Kódu vnitropodnikového partnera**.

### Zdroj transakce
Co s transakcí můžete udělat, záleží na tom, zda to bylo:

- Vytvořeno vaším vnitropodnikovým partnerem
- Odmítnuto vaším vnitropodnikovým partnerem a vráceno vám

Pomocí pole **Zobrazit zdroj transakce** můžete filtrovat stránku **Transakce vnitropodnikové doručené pošty** tak, aby zobrazovala pouze jeden z těchto typů transakcí. (Můžete také filtrovat podle vnitropodnikového partnera nebo podle obsahu pole **Akce řádku**.)

#### Transakce vytvořená vnitropodnikovým partnerem
Když obdržíte novou transakci, kterou vytvořil váš partner, můžete si vybrat buď:

- Přijetí transakce
- Odmítnutí transakce (vrácení partnerovi)
- Zrušení transakce (odstraní transakci, ale nevrátí ji vašemu partnerovi)

#### Vrácení od vnitropodnikového partnera
Pokud transakce byla odmítnuta vaším vnitropodnikovým partnerem, jedinou možností je zrušení transakce v doručené poště. Poté musíte ve své společnosti vytvořit opravné řádky nebo stornovat deník nebo dokument.

## Opětovné vytvoření položek doručené pošty
Pokud jste transakci přijali ve složce doručená pošta, ale místo zaúčtování dokumentu jste deník odstranili, můžete položku doručené pošty znovu vytvořit a znovu ji přijmout.

## Získání přehledu vnitropodnikových transakcí za období
Můžete získat přehled o všech vnitropodnikových transakcích, které jste odeslali a přijali v období. Sestava **Vnitropodnikové transakce** uvádí všechny vnitropodnikové věcné položky, položky zákazníka a položky dodavatele.

> [!NOTE]
> Pokud jsou vnitropodnikoví partneři ve stejné databázi, pak se transakce přenášejí bez potřeby souboru nebo e-mailu. Podívejte se na pole **Typ přenosu** na stránce **Vnitropodnikový partner**. <br /><br />
V takovém případě můžete systém nastavit tak, aby obcházel doručenou poštu a poštu k odeslání výběrem zaškrtávacího políčka **Auto.  Přijmout transakce** na stránce **Vnitropodnikový partner** a výběrem zaškrtávacího políčka **Auto.  Odeslat transakce** na stránce **Nastavení vnitropodnikové společnosti**.

## Import vnitropodnikových transakcí ze souboru
Pokud máte vnitropodnikového partnera, který není ve stejné databázi jako vaše společnost, můžete od tohoto partnera přijímat vnitropodnikové transakce v souboru XML. Potom musíte importovat transakce do vaší doručené pošty.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Informace o společnosti** a poté vyberte související odkaz.
2. Uložte soubor na místo, které jste určili v poli **Detaily vnitropodnikové doručené pošty** na stránce **Informace o společnosti**.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Transakce vnitropodnikové doručené pošty** a poté vyberte související odkaz.
4. Na stránce **Transakce vnitropodnikové doručené pošty** vyberte akci **Import souboru transakcí**.
5. Na zobrazené stránce vyberte soubor .xml, který obsahuje transakce, a poté vyberte tlačítko **Otevřít**.

Transakce se importují do složky Doručená pošta a nyní je můžete zpracovat.

## Zpracování příchozích vnitropodnikových transakcí
Když vám vaši vnitropodnikoví partneři pošlou vnitropodnikové transakce, transakce skončí ve vaší vnitropodnikové doručené poště. Každou transakci v doručené poště musíte vyhodnotit a jednat podle potřeby.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Transakce vnitropodnikové doručené pošty** a poté vyberte související odkaz.
2. Na stránce **Transakce vnitropodnikové doručené pošty** vyberte řádek a poté vyberte akci, například **Přijmout**, aby se řádek zpracoval.
3. Na stránce **Dokončit akci vnitrop.dor.pošty** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vyberte tlačítko **OK**.

Pro řádky, které jste zpracovali pomocí akce **Přijmout**, budou ve vaší společnosti vytvořeny řádky dokumentů nebo deníků. Otevřete každý dokument nebo deník, proveďte potřebné změny a poté je odešlete.

Řádky, které jste zpracovali pomocí akce **Vrátit vnitropodnikovému partnerovi**, budou přesunuty do pošty k odeslání, odkud je pak můžete odeslat partnerovi.

U řádků, které jste zpracovali akcí **Vrátit vnitropodnikovému partnerovi**, musíte nyní zaúčtovat opravu původní transakce, kterou jste zaúčtovali ve vaší společnosti.

## Zpracování odchozích vnitropodnikových transakcí
Když zaúčtujete vnitropodnikový deník nebo dokument nebo odešlete potvrzení vnitropodnikové objednávky, transakce se odešlou do vaší vnitropodnikové pošty. Abyste je mohli zaslat svým vnitropodnikovým partnerům, musíte otevřít složku k odeslání a zpracovat je.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Transakce vnitropodnikové pošty k odeslání** a poté vyberte související odkaz.
2. Na stránce **Transakce vnitropodnikové pošty k odeslání** vyberte řádek a poté vyberte akci, například **Vrátit do doručené pošty**, aby se řádek zpracoval.

Řádky, které jste zpracovali pomocí akce **Poslat vnitropodnikovému partnerovi**, budou odeslány do složky Doručená pošta příslušného partnera.

Řádky, které jste zpracovali pomocí akce **Vrátit do doručené pošty**, budou přesunuty do složky Doručená pošta, kde je můžete přijmout a vytvořit dokumenty nebo řádky deníku ve vaší společnosti.

U řádků, které jste zpracovali pomocí akce **Storno**, musíte nyní zaúčtovat opravu původní transakce, kterou jste zaúčtovali ve vaší společnosti.

## Opětovné vytvoření vnitropodnikových transakcí doručené pošty
V některých případech můžete chtít znovu vytvořit transakci v doručené poště nebo v poště k odeslání. Pokud jste například přijali transakci ve složce Doručená pošta, ale místo zaúčtování dokument nebo deník odstranili, můžete položku doručené pošty znovu vytvořit a znovu ji přijmout.

Následující postup popisuje opětovné vytvoření transakcí doručené pošty, ale stejné kroky platí také pro poštu k odeslání.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zpracované transakce vnitropodnikové doručené pošty** a poté vyberte související odkaz.

2. Na stránce **Zpracované transakce vnitropodnikové doručené pošty** vyberte řádek s transakcí, kterou chcete znovu vytvořit ve složce Doručená pošta, a pak vyberte akci **Znovu vytvořit transakce doručené pošty**.

## Viz také
[Správa vnitropodnikových transakcí](intercompany-manage.md)  
[Finance](finance.md)  
[Nastavení financí](finance-setup-finance.md)  
[Práce s finančními deníky](ui-work-general-journals.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
