---
    title: Business Central for Multi-Site and International Organizations | Microsoft Docs
    description: Business Central provides capabilities that support a hub-and-spoke business model.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: hub-and-spoke, multi-site, headquarter, sites
    ms.date: 10/01/2020
    ms.author: bholtorf

---

# Business Central pro organizace s více pracovišti a mezinárodní organizace
Organizace, které mají více poboček, často používají obchodní model "hub-and-spoke", kdy mateřská společnost nebo centrála řídí celkový provoz podniku, zatímco každá pobočka funguje jako samostatný subjekt. Jednotlivé pobočky jsou často geograficky rozmístěny a mají různé potřeby pro sdílení informací s ústředím společnosti. Kromě toho pobočky obvykle nepotřebují stejnou úroveň složitosti a často nemají prostředky na údržbu velkého systému.

[!INCLUDE[prod_short](includes/prod_short.md)] poskytuje malým a středním podnikům řešení pro řízení podniku, které se snadno používá a udržuje s nízkými náklady na vlastnictví.

Tento článek představuje některé způsoby, kterými [!INCLUDE[prod_short](includes/prod_short.md)] podporuje obchodní model hub-and-spoke.

## Integrace ústředí společnosti a poboček

[!INCLUDE[prod_short](includes/prod_short.md)] lze integrovat s účetním systémem ústředí společnosti a zároveň vyhovět různým potřebám různých pracovišť bez ohledu na jejich velikost, umístění nebo typ podnikání.

Následující schéma je příkladem různých lokalit integrovaných s ústředím společnosti.

![Diagram Description automatically generated](media/multisite-headquarter-sites.png)

## Splnění potřeb domácích a mezinárodních lokalit

Obchodní potřeby na pracovištích se často liší podle odvětví, obchodních metod nebo jejich vztahu k ústředí společnosti. [!INCLUDE[prod_short](includes/prod_short.md)] lze snadno přizpůsobit a rozšířit pro různé typy podniků a lokalit. Microsoft AppSource nabízí velké množství aplikací od společnosti Microsoft a našich partnerů a partneři mohou rychle nasadit [!INCLUDE[prod_short](includes/prod_short.md)] s minimálním narušením každodenního provozu.

U nadnárodních organizací podporuje [!INCLUDE[prod_short](includes/prod_short.md)] místní právní požadavky a obchodní postupy.

* Pro online verze existuje více než [40 lokalizovaných verzí pro jednotlivé země](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json), které si můžete nainstalovat jako rozšíření ze služby Microsoft AppSource.
* Pro on-premises verze jsou [verze pro jednotlivé země](/azure/architecture/solution-ideas/articles/business-central) k dispozici buď jako verze lokalizované společností Microsoft, nebo jako přídavné lokalizace od partnerů.

Síť více než 4 000 partnerů společnosti Microsoft po celém světě poskytuje místní odborné znalosti.

| **Obchodní požadavek** | **Jak to Business Central podporuje** | **Další informace** |
|-------------------------|-------------------------|-------------------------|
| Přizpůsobte systém na míru danému podniku. | Využijte systém, který byl od počátku navržen pro středně velké podniky. | [Přehled](https://dynamics.microsoft.com/business-central/overview/) |
| Řešení regulačních a místních postupů. | Dodržování místních právních požadavků a obchodních postupů. | [Místní funkcionality](about-localization.md) |
| Přístup k více společnostem z jedné stránky. | Získejte rychlý přístup ke kterékoli společnosti Business Central ve vaší organizaci. | [Company Hub](ui-extensions-company-hub.md) |
| Práce s více jazyky a měnami. | Podpora více jazyků a měn pomáhá uspokojit místní potřeby. | [Mnohojazyčné funkce](about-locale-language.md)<br></br>[Více měnové funkce](finance-how-setup-additional-currencies.md) |


## Konsolidace finančních údajů

Základním aspektem obchodního modelu hub-and-spoke je schopnost ústřední společnosti a poboček vyměňovat si finanční údaje, i když ústřední společnost a pobočky používají různé systémy, účetní struktury, jazyky a měny.

| **Obchodní požadavek** | **Jak to Business Central podporuje** | **Další informace** |
|-------------------------|-------------------------|-------------------------|
| Konsolidace finančních údajů z poboček | Konsolidace finančních výkazů pro pobočky bez ohledu na to, zda na nich běží aplikace Business Central nebo jiná aplikace, do jediného obchodního subjektu (společnosti). | [Konsolidování finančních dat z několika společností](finance-consolidated-company-reporting.md) |
| Integrace účetních struktur. | Přenos konsolidačních dat z různých účetních struktur do vlastní. Vestavěný formát souborů pro F&O (k dispozici ve Wave 2, 2020) | [Import podnikových dat z jiných finančních systémů](across-import-data-configuration-packages.md)<br></br>[Příprava účtů hlavní knihy pro konsolidaci](finance-consolidated-company-reporting-setup.md#glacc). |
| Transakce ve více měnách. | Pomáhají zajistit, aby finanční výkazy v různých měnách byly přesné a používaly správné směnné kurzy. | [Aktualizace směnných kurzů](finance-how-update-currencies.md) |

## Sdílení obchodních informací pomocí integrované analýzy

Sladění organizace s vašimi obchodními cíli díky společnému chápání současné reality. Integrovaná analytika může lidem pomoci zakládat svá rozhodnutí na stejném souboru faktů.

| **Obchodní požadavek** | **Jak to Business Central podporuje** | **Další informace** |
|-------------------------|-------------------------|-------------------------|
| Sdílejte poznatky s pracovišti bez rozsáhlé podpory IT. | Vytvářejte klíčové ukazatele výkonnosti a panely Business Intelligence v aplikaci Power BI na základě svých dat.
 | [Práce s daty Business Central v Power BI](across-working-with-business-central-in-powerbi.md) |
| Vytváření vlastních finančních výkazů. | Generování finančních výkazů na základě parametrů. | [Business Intelligence](bi.md) |
| Srovnání s fakty. | Vytvářet, zobrazovat a sdílet sestavy s interními a externími zúčastněnými stranami. | [Finanční sestavy](finance-reports.md) |
| Analýza dat v Excelu | Zjišťování faktů, řešení problémů a provádění ad hoc analýz v aplikaci Microsoft Excel. | [Analýza finančních výkazů v aplikaci Excel](finance-analyze-excel.md) |


## Výměna dat pomocí rozhraní API a portů XML

Rozhraní API a XML porty zjednodušují proces připojování instancí [!INCLUDE[prod_short](includes/prod_short.md)], včetně těch, které byly přizpůsobeny pro jednotlivé weby.

| **Obchodní požadavek** | **Jak to Business Central podporuje** | **Další informace** |
|-------------------------|-------------------------|-------------------------|
| Propojení přizpůsobených verzí mezi pobočkami a ústředím společnosti. | API stránky mohou zobrazovat libovolnou reprezentaci entity, včetně jejích přizpůsobení. | [Povolení rozhraní API pro Business Central](/dynamics-nav/enabling-apis-for-dynamics-nav) |
| Verzování a zabezpečení. | Rozhraní API používají ODataV4, která zajišťují verzování, webové háčky a sledování změn. | [Bezpečnost a ochrana](/dynamics365/business-central/dev-itpro/security/security-and-protection) |
| Účotávní a import XML dokumentů .
 | Jednotky kódu lze vystavit jako nevázané akce pro podporu odesílání a přijímání dokumentů XML. Pro zpracování dokumentů XML lze použít XMLports. Nesvázané akce jsou také schopny generovat dokument XML nebo JSON. | [Objekty XMLport](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-object) |
| Usnadnění údržby prostřednictvím elektronické výměny dat. | Jako integrační vrstva mezi centrálou a pobočkami může být přidáno řešení pro elektronickou výměnu dat. | [Framework pro výměnu dat](across-about-the-data-exchange-framework.md) |
| Výměna dat mezi různými systémy. | Pomocí XMLportů můžete vytvářet dokumenty, které si pak mohou vyměňovat ústředí společnosti, jež používá jeden systém, a pracoviště, která používají Business Central. | [Přehled XMLport](/dynamics365/business-central/dev-itpro/developer/devenv-xmlport-overview) |
| Organizace složitých výměn dat. | Pro splnění jedinečných potřeb na vašich pracovištích použijte kombinaci XMLportů s Business Central a Microsoft BizTalk Server.</br> Pro komplexní potřeby použijte řešení elektronické výměny dat založené na BizTalk Server a Commerce Gateway v Business Central v kombinaci s XMLports. | [Práce se sestavami, dávkovými úlohami a XMLporty](ui-work-report.md) |
| Připojení k řešením a službám třetích stran. | API rozhraní vytvářejí spojení mezi Business Central a řešeními a službami třítách stran. | [API v2.0](/dynamics-nav/api-reference/v2.0/) |


## Podpora efektivního mezipodnikového dodavatelského řetězce

Pobočky často potřebují přístup k dodavatelskému řetězci a schopnost řídit určité jeho aspekty. Například pobočky mohou používat stejného dodavatele, ale spravovat svá aktiva a fyzická umístění odděleně.

| **Obchodní požadavek** | **Jak to Business Central podporuje** | **Další informace** |
|-------------------------|-------------------------|-------------------------|
| K transakcím mezi divizemi přistupujte jako k běžným prodejním a nákupním transakcím. | Pomocí mezipodnikových zaúčtování můžete vytvářet prodejní a nákupní doklady a záznamy v hlavní knize pro celé workflow a pro více společností najednou, abyste eliminovali duplicitní zadávání dat. | [Správa vnitropodnikových transakcí](intercompany-manage.md) |
| Používejte bezpapírové procesy. | Vyhnete se nákladům na odesílání, přijímání a tisk dokladů. | [Došlé doklady](across-income-documents.md)<br><br> [Správa příloh, odkazů a poznámek na kartách a v dokumentech](ui-how-add-link-to-record.md) |

## Rychlá reakce na nové obchodní podmínky

Ústředí společnosti musí být schopno rychle reagovat na obchodní změny v jednotlivých lokalitách. V kombinaci s nástrojem Power Automate může [!INCLUDE[prod_short](includes/prod_short.md)] sloužit jako mechanismus včasného varování.

![Snímek obrazovky příspěvku na sociální síti](media/multisite-apps.png)

| **Obchodní požadavek** | **Jak to Business Central podporuje** | **Další informace** |
|-------------------------|-------------------------|-------------------------|
| Automatické generování e-mailových upozornění. | V aplikaci Power Automate můžete nastavit upozornění, která budou generovat e-maily informující o kritických obchodních podmínkách na pracovištích nebo u partnerů v dodavatelském řetězci. | [Business Central a Power BI](admin-powerbi.md) |
| Použijte standardní nebo vlastní upozornění. | Použijte 12 různých šablon, které jsou součástí aplikace Business Central, nebo si nastavte vlastní upozornění, která budou vyhovovat vašemu podnikání. | [Použití nástroje Business Central s automatizovaným workflow ](across-how-use-financials-data-source-flow.md) |

## Viz také
[Administrace Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
