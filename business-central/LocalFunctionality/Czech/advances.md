---
title: Czech Local Functionality - Advance payments and invoices | Microsoft Docs
description: This section describes Czech local functionality - Advance payments and invoices
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Advance payment, Advance invoices, Payables, Finance, CZ, Cash
ms.date: 12/30/2019
ms.reviewer: v-pejano
ms.author: v-makune
---

# Zálohové platby a faktury

Funkce zálohové faktury a platby se používá pro generování faktur a provádění plateb před dodáním zboží nebo před zahájením výroby. Funkce zálohové faktury a platby zahrnuje zálohové faktury, zálohové platby, zálohové platby podléhající DPH a daňové doklady. Typy dokumentů a požadavky na dokumenty pro tuto funkci jsou uvedeny níže:

## Zálohové faktury

- Používají se k vyžádání peněz předem.
- Doklad není účtován a nemá daňový doklad.
- Doklady se vytvářejí před šablonami faktur (skupiny dokladů) s předdefinovaným účetnictvím a číselnou řadou souvisejících dokladů. Šablony zálohových faktur definují, zda jste, nebo nejste, povinni účtovat DPH.
- Zálohové faktury lze vytvořit z objednávek, faktur nebo jako samostatný doklad bez vazby na doklady.
- Volné zálohy lze dodatečně spojit s dokladem před zaúčtováním konečné faktury. 

## Životní cyklus zálohové faktury

Zálohová faktura má svůj vlastní životní cyklus, který je definován stavy:
- **Otevřeno** - zálohovou fakturu lze editovat.
- **Příprava platby** - je očekávána platba zálohové faktury.
- **Příprava faktury** - je očekáváno vytvoření daňového dokladu k přijaté/vydané platbě.
- **Příprava** konečné faktury - zálohová faktura je připravena k čerpání.
- **Uzavřeno** - konečný stav po vyčerpání zálohové faktury.

## Zálohové platby

- Platba provedená na vrub zálohové faktury.
- Částečné zálohové platby, týkající se zaúčtování a fakturaci, v denících a pokladně.
- Přijaté zálohové platby nejsou pohledávky, ale závazky.
- Vydané zálohové platby nejsou závazky, pohledávky.
- Zálohové platby mohou podléhat DPH. Legislativa CZ stanovuje pravidla, zda záloha podléhá nebo nepodléhá DPH.
- Přijaté zálohové platby jsou účtovány na základě data přijetí platby. 
- Vydané zálohové platby jsou účtovány na základě data příjmu daňových dokladů. 
- Lze vrátit nevyčerpanou část zálohové faktury.
- Zaúčtování platby jako platbu lze provést na základě zálohové faktury.
- Zaúčtovanou zálohovou platbu propojenou se zálohovou fakturou lze odpojit. 
- Zálohová faktura může být uhrazena více platbami.
- Přijaté zálohové platby se účtují jako závazky.
- Zálohové platby v cizí měně závisí na dohodnutých datech.

## Daňové doklady (daňový dobropis)

- Doklady specifikují zaplacené DPH z přijatých zálohových plateb. 
- Není možné nárokovat DPH ze zálohových plateb, bez přijetí daňových dokladů, vydaných pro zálohové platby.
- Vylepšení kalkulace DPH splňují legislativu České republiky.
- Doklady deklarují zaplacené DPH z přijatých/vydaných zálohových plateb. 
- Daňové doklady/daňové dobropisy jsou vytvářeny s vazbou na zálohovou fakturu, ke které byla platba provedena.
- Modul obsahuje funkce pro automatické generování daňových dokladů při účtování zálohové platby. 
- K vydaným zálohovým platbám je možná korekce daňových dokladů před jejich zaúčtováním z důvodu jejich účtování na základě obdrženého dokladu od věřitele. 
- Režim zálohové faktury bez daňového dokladu umožňuje uplatnění DPH až na konečné faktuře, pokud její plnění splňuje podmínky § 28 Zákona o dani z přidané hodnoty.
- Daňový doklad k vydané platbě lze účtovat pouze na základě obdrženého dokladu od věřitele, proto nákupní zálohová faktura umožňuje změnu režimu s/bez DPH i v průběhu jejího zpracování.
- Výpočet DPH zálohových faktur opírající se o Zákon o dani z přidané hodnoty (§ 37a, § 92).
- Nový modul pracuje s DPH také v režimu registrace plátce v jiné zemi EU.

## Čerpání zálohy

- Čerpání zálohové platby a už zaplacené nebo nárokované DPH z konečné faktury.
- Odpočet se provádí při poměrném zaúčtování konečné faktury.
- Modul nabízí nástroj pro provázání zálohových faktur s konečným dokladem.
- Lze provést změnu/doplnění/zrušení provázání zálohové faktury s konečným dokladem před jeho zaúčtováním. 
- Je možné provázat více zálohových faktur ke konečnému dokladu v jednom kroku.
- Parametry nástroje lze ovlivnit způsob propojení konečného odkladu se zálohovými fakturami.
- Pro lepší kontrolu/korekci daňového plnění konečné faktury byla rozšířena statistika objednávky a faktury o záložky informující o čerpání platby a zaplacené/nárokované DPH. 
- Provedené čerpání zálohové faktury z konečné faktury lze stornovat se všemi účetními zápisy, kterými bylo čerpání účtováno. 
- Při čerpání zálohové faktury v cizí měně dochází k vyčíslení kurzových rozdílů. 

## Nástroj pro provázání zálohové faktury a konečného dokladu 

Nástroj poskytuje možnost volby různých způsobů provázání řádků konečného dokladu s řádky zálohových plateb: 

- režim provázání zálohových faktur zaplacených/nezaplacených
- provázání dle částek zbývajících nebo k fakturaci konečného dokladu
- provázání na základě sazeb DPH 

## Informační okna – statistika zákazníka/dodavatele 

Statistické informační okna karty zákazníka a dodavatele doplněny o informace o zálohách: 
- Fakturovaná částka zálohy
- Zálohy - otevřené
- Zálohy - příprava platby
- Zálohy - příprava faktury
- Zálohy - příprava koneč. faktury

## Interní a výstupní doklady 

Byla vytvořena sada dokladů, které zohledňují národní legislativu a zvyklosti.

Výstupní doklady:
- Zálohová faktura
- Daňový doklad k přijaté platbě
- Daňový dobropis k přijaté platbě 
- Prodejní faktura

Interní doklady:
- Seznam prodejních záloh
- Seznam nákupních záloh
- Přehled DPH na  nákupních  zálohách
- Přehled DPH na prodejních  zálohách

## Viz také
[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](finance.md)