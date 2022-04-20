---
title: Power BI FAQ
description: Get answers for some typical questions about working with Power BI and Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, reports, faq, errors
ms.date: 04/22/2021
ms.author: jswymer
---
# Nejčastější dotazy Power BI

Tento článek odpovídá na některé otázky, které můžete mít ohledně práce s Power BI a [!INCLUDE [prod_short](includes/prod_short.md)].

## [Obecné](#tab/general)
<!-- 26 -->
### Vybral jsem sestavu pro své centrum rolí v Business Central. Pokud později provádím změny vizuálů sestavy online, bude centrum rolí automaticky aktualizovat mé změny?

Ano, protože sestavy jsou vložené z Power BI.

<!-- 3 -->
### Jsou aplikace Business Central pro Power BI dostupné v jiných jazycích než v angličtině?

Ne.  Tyto aplikace jsou v současné době k dispozici pouze v angličtině.

<!-- 24 -->
### Jakmile je sestava publikována na mém powerbi.com pracovním prostoru, mohu si stáhnout její pbix?

Ano. Pro více informací navštivte [Stažení sestavy ze služby Power BI do Power BI Desktop](/power-bi/create-reports/service-export-to-pbix).

<!-- 27 -->
### Mohu si stáhnout aplikace jako soubory pbix?

Ne.  V současné době nenabízíme stahování souborů pbix pro oficiální aplikace Power BI, protože jsou publikovány v AppSource.

## [Licence](#tab/license)

<!-- 14 -->
### Potřebuji k publikování sestav licenci Power BI Pro?

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Ne.  K publikování sestav není potřeba licence Pro. Stačí standardní (bezplatná) licence Power BI. Pro více informací navštivte [Licencování Power BI](admin-powerbi-setup.md#license).

<!-- 15 -->
### Je něco, co nemůžu udělat s licencí zdarma?

Nemůžete sdílet sestavy ani instalovat aplikace Business Central pro Power BI. Kromě toho vám bezplatná licence umožňuje vytvářet téměř všechny varianty grafů a sestav.

<!-- 16 -->
### Pokud někdo sdílí sestavu s jinou osobou, pak tato osoba potřebuje licenci Pro, aby ji viděla. Existují plány, jak tuto možnost umožnit pomocí bezplatné licence?

Nad tímto požadavkem nemáme kontrolu. Tento požadavek je nastaven pomocí Power BI. Pro více informací navštivte [Sdílení řídicích panelů a sestav Power BI se spolupracovníky a dalšími](/power-bi/collaborate-share/service-share-dashboards).

## [Návrhář](#tab/designer)

<!-- 7 -->
### Funguje konektor se stránkami rozhraní API?

Ano. Od června 2021 však bude nový konektor Power BI podporovat webové služby Business Central i stránky rozhraní API. Pro více informací navštivte [Povolení práce s rozhraními API Business Central pomocí konektoru Power BI, nikoli pouze s webovými službami](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### Můžu sestavu Power BI vytvořit pomocí Řádků prodejní faktury nebo rozhraní API řádků deníku?

Nejčastěji používané řádkové záznamy jsou k dispozici v [Business Central API v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/)). Můžete je tedy použít k vytváření sestav v Power BI tak, že je vyberete v konektoru **Dynamics 365 Business Central**. Rozhraní **Lines** API jsou však navržena pro použití pouze s některými velmi specifickými filtry a ve vašem scénáři nemusí fungovat. Může se zobrazit chyba podobná chybě "Chcete-li získat řádky, musíte zadat ID nebo ID dokumentu". Pokud chcete tento problém vyřešit, proveďte následující kroky při získávání dat z Business Central pro sestavu v Power BI Desktopu:

1. Místo zahrnutí zdroje dat pro entitu řádků přidejte nadřazený zdroj dat. Například přidejte **Prodejní fakturu** namísto **Řádků prodejní faktury**.
2. Na panelu akcí Power BI Desktopu vyberte **Transformovat data**.
3. Vyberte dotaz, který jste právě přidali, například **Prodejní faktury**.
4. Použijte na záznamy jakékoli potřebné filtrování, abyste snížili množství záznamů načtených ve vaší sestavě.
5. Posouvejte se doprava, dokud nenajdete sloupec pojmenovaný jako řádky, například **Řádky prodejní faktury**.
6. Vyberte tlačítko Rozbalit v záhlaví sloupce vedle názvu sloupce.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Zobrazuje sloupec Řádky prodejní faktury v Power BI Desktopu.":::
<!-- 11 -->
### Je možné zvolit, ze kterého prostředí Business Central chcete získat data pro Power BI, například sandbox nebo produkční prostředí?

Ano. Lze jej snadno vybrat. Když se připojíte k Business Central pomocí konektoru, musíte zvolit prostředí a název společnosti.

<!-- 6 -->
### Mohu sloučit data z několika produkčních prostředí stejného tenanta?

Ano. V Power BI spusťte znovu operaci získat data a vyberte prostředí, které chcete.

<!-- 25 -->
### Which pages in Business Central have the Power BI Report part?

V současné době existuje několik vybraných stránek, které mají panel s fakty s částí **Sestavy Power BI** pro zobrazení sestavy.

Na stránkách se seznamy je část **Sestavy Power BI** filtrována tak, aby zobrazovala sestavy, které se týkají dat v seznamu. Tady jsou stránky typu seznam, které obsahují část **Sestavy Power BI**:

| ID stránky | Jméno |
|-------|----|
| 22 | Přehled zákazníků |
| 27 | Přehled dodavatelů |
| 31 | Přehled zboží |
| 9305 | Seznam prodejních objednávek |
| 9308 | Nákupní faktury |

Tady jsou další stránky, které obsahují větší část **Sestav Power BI**:

| ID stránky | Jméno |
|-------|----|
| 1156 | Podrobnosti o společnosti |
| 4013 | Intelligent Cloud Insights |
| 9006 | Centrum rolí Zpracovatel objednávek |
| 9008 | Deník rolí Skladník |
| 9010 | Centrum rolí Výrobní plánovač |
| 9015 | Centrum rolí Vedoucí projektuC |
| 9016 | Centrum rolí Správce servisu |
| 9022 | Centrum rolí Obchodní ředitel |
| 9024 | Centrum rolí Správce zabezpečení |
| 9026 | Centrum rolí Manažer prodeje a vztahů   |
| 9027 | Centrum rolí Účtárna |

> [!TIP]
> V tuto chvíli nemáme v plánu přidat jej na všechny stránky seznamu. Můžete však vytvořit jednoduchou extension stránky, která přidá část **Sestavy Power BI** do okna s fakty. Pro více informací navštivte [Přidání částí sestav Power BI na stránky](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) v nápovědě vývojáře a IT Pro.

<!-- 5 -->
### Existuje nějaký způsob, jak filtrovat datovou sadu z Business Central *dříve* než ji vytáhnu do Power BI, místo toho, abych potom použil filtry přímo v Power BI?

Chcete-li filtrovat větší datové sady, nejjednodušším způsobem je nastavit filtr v sestavě Power BI přímo úpravou vzorce Power Query. Většina filtrů, které nastavíte tímto způsobem, bude předána do Business Central prostřednictvím skládání dotazů. Viz [Inkrementální aktualizace pro datové sady](/power-bi/admin/service-premium-incremental-refresh).

V současné době neexistuje žádný způsob, jak nastavit filtr pro data webové služby z Business Central. Pokud vaše aplikace potřebuje nastavit filtr z Business Central, budete si pro tento účel muset vytvořit vlastní aplikaci Business Central.

<!-- 10 -->
### Existuje z Power BI kromě použití dotazu i jiný způsob, jak získat data z tabulek Business Central, které nemají přidruženou stránku? Například jako tabulka *Atributy zboží mapování hodnot*.

Ne.  V tuhle chvíli ne.

<!-- 12 -->
### Jsou publikované dotazy rychlejší než publikované stránky?

Pokud jde o webové služby, publikované dotazy jsou obvykle rychlejší než ekvivalentní publikované stránky. Důvodem je, že dotazy jsou optimalizovány pro čtení dat a neobsahují triggery, jako je OnAfterGetRecord.

Až bude nový konektor k dispozici v červnu 2021, doporučujeme používat stránky rozhraní API na dotazy publikované jako webové služby.

<!-- 13 -->
### Existuje způsob, jak může koncový uživatel vytvořit webovou službu se sloupcem, který je v tabulce Business Central, ale ne na stránce? Nebo bude muset vývojář vytvořit vlastní dotaz?

Ano. S vydáním nového konektoru v červnu 2021 může vývojář vytvořit novou stránku rozhraní API, která tento požadavek splní.

<!-- 28 -->
### Můžu Power BI připojit k databázi Business Central online jen pro čtení?

Ne.  Ale tuto funkci máme v našem dlouhodobém plánu.

### <a name="perms"></a>Jak změním nebo vymažu uživatelský účet, který aktuálně používám pro připojení k Business Central z Power BI Desktopu?

V Power BI Desktopu proveďte následující kroky:

1. V nabídce Soubor vyberte **Možnosti a nastavení** > **Nastavení zdroje dat**.
2. Ze seznamu vyberte **Dynamics Business Central** a poté vyberte **Vymazat oprávnění** > **Odstranit**.

Až se příště připojíte k Business Central, abyste získali data, budete vyzváni k přihlášení.

## [Výkon](#tab/performance)

<!-- 17 -->

### Je rychlejší získat data pomocí stránek ROZHRANÍ API než pomocí webových služeb?

Ano. Naše testy ukazují, že stránky API jsou až o 25 % výkonnější než webové služby.

<!-- 18 -->
### Existují plány na zrcadlení instance Azure SQL Database, ke které se mohu připojit přímo?

Ne.  V tuhle chvíli ne. S Business Central můžu komunikovat pouze prostřednictvím rozhraní API.

<!-- 19 -->
### Načítání dat z webových služeb Business Central se zdá být pomalé. Existuje nějaký způsob, jak získat data přímo z databázové tabulky SQL?

Ne.  Přímý přístup k databázi není možný, ale přechod na stránky rozhraní API (když je k dispozici nový konektor) výrazně pomůže.

## [Pokročilé](#tab/advanced)
<!-- 1 -->

### Existují plány pro konektor Power BI, který podporuje přírůstkové funkce aktualizace ve službě Power BI?

Ano. Je to v našem plánu.

<!-- 2 -->
### Pokud řešení Business Central on-premises nemá přístup k internetu, můžu pořád používat Power BI?
<!-- todo: please explain this one-->

Ano. V takovém případě používáte Power BI Desktop lokálně a připojujete se k Business Central on-premises. Po připojení můžete vytvářet a prohlížet si sestavy, ale nemůžete je publikovat do služby Power BI.
<!-- 20 -->
### Existují nějaké plány, které by umožnily replikaci online databází Business Central, aby byly přístupné pro dotazy SQL jen pro čtení? Tato funkce by podporovala přírůstkovou aktualizaci a byla by mnohem rychlejší než rozhraní API nebo webové služby.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Ano. Tuto funkci máme v našem dlouhodobém plánu.

<!-- 21 -->
### Když použiju Azure Data Factory k získání dat z Business Central a jejich využití v Power BI, pomůže to zvýšit výkon?

Ano. Tento pokročilý scénář pomůže Business Central zůstat výkonným, protože přístup k datům se bude provádět prostřednictvím Azure Data Factory.

<!-- 22 -->
### Existují nějaké plány na podporu kanálů nasazení Power BI nebo způsob, jak vytvořit kanály nasazení pro sestavy PBI, podobně jako rozšíření? Nebo možná i jednoduché rozhraní API v Centru pro správu?

Prověřujeme tuto funkci. Power BI nabízí bohatá rozhraní API pro řízení nasazení sestav. Pro více informací navštivte [Úvod do nasazení kanálů](/power-bi/create-reports/deployment-pipelines-overview).

### Vyzkoušel jsem náhled nového konektoru, který bude v červnu 2021. Při připojování k rozhraní API v2.0 se zobrazí některé hodnoty jako "_x0020_". Co znamenají tyto hodnoty?

Nadcházející verze konektoru Power BI umožňuje připojení k stránkám rozhraní Business Central API, včetně rozhraní API v2.0. Tyto stránky obsahují několik polí založených na objektech [AL Enum](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Pole založená na objektech AL Enum musí mít názvy, které jsou konzistentní a vždy stejné, aby filtry v sestavě vždy fungovaly bez ohledu na jazyk nebo operační systém, který používáte. Z tohoto důvodu nejsou pole založená na AL Enums přeložena a jsou kódována, aby se zabránilo jakémukoli speciálnímu znaku, včetně mezery. Zejména vždy, když je v objektu AL Enum prázdná možnost, je zakódována na "_x0020_". Transformaci dat v Power BI můžete použít vždy, pokud chcete pro tato pole zobrazit jinou hodnotu, například "Prázdná".


---

## Viz také

[Licence Power BI](admin-powerbi-setup.md#license)  
[Úvod Business Central a Power BI](admin-powerbi.md)    
[Přehled integrace Power BI](admin-powerbi-overview.md)    
[Povolení Power BI v Business Central](admin-powerbi-setup.md)    
[Práce se sestavami Power BI v Business Central](across-working-with-powerbi.md)    
[Práce s daty Business Central v Power BI](across-working-with-business-central-in-powerbi.md)    
[Vytvážení sestav Power BI pro zobrazení dat Business Central](across-how-use-financials-data-source-powerbi.md)      
[Dokumentace Power BI](/power-bi/)


[!INCLUDE[footer-include](includes/footer-banner.md)]
