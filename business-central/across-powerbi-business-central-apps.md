---
title: Using Business Central Apps in Power BI| Microsoft Docs
description: Getting insight, business intelligence, and KPIs from your Business Central data is easy with the Business Central apps for Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
---
# Použití [!INCLUDE [prod_short](includes/prod_short.md)] Apps v Power BI

> **PLATÍ PRO:** [!INCLUDE [prod_long](includes/prod_long.md)] online

[!INCLUDE [prod_long](includes/prod_long.md)] publikuje následující aplikace Power BI, které poskytují podrobné řídicí panely pro prohlížení dat:

- [!INCLUDE [prod_long](includes/prod_long.md)] - CRM
- [!INCLUDE [prod_long](includes/prod_long.md)] - Finance
- [!INCLUDE [prod_long](includes/prod_long.md)] - Prodej

## Přehled

Každá aplikace obsahuje několik sestav, do kterých můžete přejít a zobrazit podrobnosti o datech, včetně následujících funkcí:

- Můžete vybrat jakýkoli vizuální prvek na řídícím panelu a nadnést jednu ze základních sestav
- Filtrovat sestavy nebo přidat pole, které chcete sledovat.
- Chcete-li pokračovat ve sledování, připněte na řídicí panel přizpůsobené zobrazení.   
   Data můžete aktualizovat ručně a můžete nastavit plán obnovy. Pro více informací navštivte [Konfigurace naplánované aktualizace](/power-bi/refresh-scheduled-refresh).

Aplikace jsou navrženy tak, aby pracovaly s daty od jakékoli společnosti v [!INCLUDE[prod_short](includes/prod_short.md)]. Když nainstalujete aplikaci Power BI, zadejte jeden nebo více parametrů pro připojení k [!INCLUDE [prod_short](includes/prod_short.md)].

> [!NOTE]
> Můžete si také vytvořit vlastní sestavy a řídicí panely v Power BI na základě vašich dat [!INCLUDE[prod_short](includes/prod_short.md)]. Pro více informací navštivte [Připojení obchodních dat k Power BI](across-how-use-financials-data-source-powerbi.md).

## Předpoklady

Aplikace Power BI vyžadují oprávnění k tabulkám, ze kterých se načítají data, a k webovým službám používaným k načítání dat. V následující tabulce jsou uvedeny webové služby požadované pro každou aplikaci Power BI:

| Aplikace | Webové služby |
|----|-------------|
| [!INCLUDE[prod_short](includes/prod_short.md)] – CRM | <ul><li>Prodejní příležitosti</li><li>Informace o společnosti v šabloně aplikace Excel</li><li>Popisky sestavy Power BI</li></ul> |
| [!INCLUDE[prod_short](includes/prod_short.md)] – Finance | <ul><li>PowerBIFinance</li><li>Informace o společnosti v šabloně aplikace Excel</li><li>Popisky sestavy Power BI</li></ul> |
| [!INCLUDE[prod_short](includes/prod_short.md)] – Prodej | <ul><li>Prodej zboží podle Zákazníka</li><li>Řídicí panel prodeje</li><li>Informace o společnosti v šabloně aplikace Excel</li><li>Popisky sestavy Power BI</li></ul> |

> [!TIP]
> Snadný způsob, jak najít webové služby, je vyhledat *Webové služby* v [!INCLUDE[prod_short](includes/prod_short.md)]. Na stránce **Webové služby** zkontrolujte, zda je pro výše uvedené webové služby vybráno pole **Publikovat**. Pro více informací navštivte [Publikování webové služby](across-how-publish-web-service.md).

## Připravit se

Zaregistrujte se ke službě Power BI. IPokud jste se ještě nezaregistrovali, přejděte na [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Při přihlášení použijte pracovní e-mailovou adresu a heslo.

## Nainstalujte si aplikaci [!INCLUDE[prod_short](includes/prod_short.md)] v Power BI

1. Otevřete prohlížeč, přejděte na [https://powerbi.microsoft.com](https://powerbi.microsoft.com) a přihlaste se ke svému účtu.
2. V dolní části levého navigačního podokna vyberte možnost **Získat data**.

   ![Navigace k získání dat.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

   Můžete také začít od [!INCLUDE [prod_short](includes/prod_short.md)]. Na domovské stránce přejděte na **Výběr sestavy** v sekci Power BI. Z pásu karet vyberte buď **Služba** nebo **Moje organizace**. Otevře se galerie Organizace v Power BI nebo Microsoft AppSource, filtrovaná tak, aby zobrazovala jenom aplikace související s [!INCLUDE[prod_short](includes/prod_short.md)].

3. V poli **Služby** vyberte **Získat**.

   Tento krok otevře stránku **Aplikace Power BI**, která vám umožní procházet aplikaci Power BI dostupnou v **AppSource**.

4. Do pole **Hledat** zadejte **Dynamics 365 Business Central**.
5. Vyberte aplikaci, kterou chcete použít, vyberte **Získat teď** a poté **Instalovat**.

   Po dokončení bude aplikace dostupná z **Aplikace** v navigační nabídce v Power BI.

## Připojte ke svým datům aplikaci  [!INCLUDE[prod_short](includes/prod_short.md)]

1. V části **Aplikace** vyberte aplikaci Business Central a poté **Připojit**.
2. Po zobrazení výzvy vyplňte **Název společnosti** a **Prostředí** informacemi o instanci [!INCLUDE[prod_short](includes/prod_short.md)], ke které se chcete připojit.

   - Pro **Název společnosti** nezapomeňte použít celé jméno, nikoli zobrazované jméno. Název společnosti najdete na stránce **Společnosti** v [!INCLUDE[prod_short](includes/prod_short.md)].
   - Pokud jste pro **Prostředí** nevytvořili více prostředí, zadejte **Produkce**.

3. Vyberte **Další**.
4. Vyberte **Přihlásit se**.
5. Po zobrazení výzvy zadejte uživatelské jméno a heslo pro přihlášení do [!INCLUDE[prod_short](includes/prod_short.md)].
6. Po připojení se do vašeho pracovního prostoru, Power BI přidá řídicí panel a sestavy. Po dokončení se zobrazí data z vaší společnosti [!INCLUDE[prod_short](includes/prod_short.md)].

   ![Zvolte Dynamics 365 Business Central a vyberte Získat nyní.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## Řešení problémů

Řídicí panel Power BI závisí na publikovaných webových službách, které jsou uvedeny výše. Zobrazuje data z demonstrační společnosti nebo vaší vlastní společnosti, pokud importujete data z aktuálního finančního řešení. Pokud se však něco pokazí, tato část poskytuje řešení pro nejtypičtější problémy.

### Nemáte účet Power BI

Účet Power BI nebyl nastaven. Abyste získali platný účet Power BI, musíte mít licenci. Musíte mít dříve přihlášení k Power BI, abyste pak mohli vytvořit svůj pracovní prostor Power BI.

### Zpráva: Nejsou povoleny žádné sestavy. Zvolte Vybrat sestavu, chcete-li zobrazit seznam sestav, které můžete zobrazit.

Tato zpráva se zobrazí, pokud se výchozí sestavě nepodařilo nasadit do vašeho pracovního prostoru Power BI. Nebo se zpráva nasadila, ale nebyla úspěšně aktualizována. Pokud k tomuto problému dojde, přejděte do sestavy v pracovním prostoru Power BI, vyberte **Sada dat**, **Nastavení** a pak ručně aktualizujte přihlašovací údaje. Jakmile se datová sada úspěšně aktualizuje, přejděte zpět na [!INCLUDE[prod_short](includes/prod_short.md)] a ručně vyberte sestavu ze stránky **Vyberte sestavy**.

### K instalaci aplikace [!INCLUDE[prod_short](includes/prod_short.md)] v Power BI potřebujete licenci Power BI Pro

Ke sdílení vašeho obsahu potřebujete licenci [Power BI Pro](/power-bi/service-features-license-type) a lidé, se kterou tento obsah sdílíte, licenci potřebují také. Obsah musí být v pracovním prostoru s [kapacitou Premium](/power-bi/service-premium-what-is). Pro více informací navštivte [Způsoby sdílení práce v Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

### "Ověření parametrů se nezdařilo, zkontrolujte, zda jsou všechny parametry platné“

Tato chyba označuje, že jeden z parametrů není platný.

- Zadaný parametr prostředí neodpovídá žádnému existujícímu produkčnímu nebo sandboxovému prostředí [!INCLUDE[prod_short](includes/prod_short.md)].
- Zadaný parametr společnosti neodpovídá žádným existujícím společnostem [!INCLUDE[prod_short](includes/prod_short.md)]. Ověřte název společnosti na stránce **Společnosti** v [!INCLUDE[prod_short](includes/prod_short.md)].
- Pokud se připojujete k [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, zadali jste adresu URL, která není platná. Adresu URL můžete ověřit na stránce **Webové služby** v [!INCLUDE[prod_short](includes/prod_short.md)]
- Není otevřen port, který by umožňoval požadavek prostřednictvím brány firewall.

### Nelze se přihlásit

Pokud se po použití přihlašovacích údajů uživatele [!INCLUDE[prod_short](includes/prod_short.md)] zobrazí chyba „přihlášení se nezdařilo“, pravděpodobně dochází k jednomu z následujících problémů:

- Účet, který používáte, nemá oprávnění k načtení dat [!INCLUDE[prod_short](includes/prod_short.md)] z vašeho účtu. Ověřte, zda máte oprávnění k požadovaným datům v [!INCLUDE[prod_short](includes/prod_short.md)] a akci opakujte.
- Vybrali jste jiný typ ověřování než Základní, pokud se připojujete k [!INCLUDE[prod_short](includes/prod_short.md)] on-premises.
- Nezadali jste platné uživatelské jméno nebo heslo.

### Zpráva: Váš zdroj dat nelze aktualizovat, protože přihlašovací údaje jsou neplatné. Aktualizujte své přihlašovací údaje a zkuste to znovu

Pro [!INCLUDE[prod_short](includes/prod_short.md)] on-premises může být problém v tom, že adresa URL OData je vystavena pouze místní síti.

### Nesprávný název společnosti

Běžnou chybou je zadání zobrazovaného názvu společnosti namísto celého názvu společnosti. Chcete-li najít název společnosti, hledejte **Společnosti**. Při zadávání názvu společnosti použijte pole **Název**.

### Klíč neodpovídal žádným řádkům v tabulce

Pokud během procesu připojení zadáte neplatný název společnosti, může se zobrazit chybová zpráva „Klíč neodpovídá žádným řádkům v tabulce“. Zadejte správný název společnosti a zkuste se znovu připojit.

### Zdá se, že chybí historická data

Jakmile se aplikace Power BI nainstaluje a vaše data se zobrazí v Power BI, zjistíte, že se nezobrazí všechna vaše data. Datové sady jsou filtrovány tak, aby vracely pouze data z předchozích 365 dnů. Toto výchozí nastavení je zavedeno, aby bylo možné sestavy zrychlit.

### Vidím pouze data pro jednu společnost

Aplikace Power BI zobrazí pouze data od společnosti [!INCLUDE[prod_short](includes/prod_short.md)], která byla definována při instalaci aplikace Power BI. Data od dalších společností lze do sestav přidat přidáním nových dotazů, které používají jako zdroj dat různé společnosti.

### Co teď?

- Zkuste [Zadání dotazu v poli Q&A](/power-bi/service-q-and-a-tips) v horní části řídicího panelu.
- [Změna dlaždic](/power-bi/service-dashboard-edit-tile) v řídicím panelu.
- [Vyberte dlaždici](/power-bi/service-dashboard-tiles) pro otevření zdrojové sestavy.
- Ve výchozím nastavení není aktualizace datové sady naplánována. Plán aktualizace můžete změnit nebo jej můžete na vyžádání aktualizovat pomocí příkazu **Aktualizovat**. Pro více informací navštivte [Konfigurace naplánované aktualizace](/power-bi/refresh-scheduled-refresh).

## Zobrazit související školení na webu [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Viz také

[Business Central a Power BI](admin-powerbi.md)    
[Integrace komponent Power BI a přehledu architektur pro [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)    
[Práce s daty [!INCLUDE [prod_short](includes/prod_short.md)] v Power BI](across-working-with-business-central-in-powerbi.md)    
[Vytváranie zostáv Power BI na zobrazenie dát [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)    
[Power BI pro uživatelé](/power-bi/consumer/end-user-consumer)    
[„Nový vzhled“ služby Power BI](/power-bi/service-new-look)    
[Rychlý start: Připojení k datům v Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)    
[Dokumentace Power BI](/power-bi/)    
[Business Intelligence](bi.md)    
[Příprava na podnikání](ui-get-ready-business.md)    
[Import podnikových dat z jiných finančních systémů](across-import-data-configuration-packages.md)    
[Nastavení [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] jako zdroj dat Power BI](across-how-use-financials-data-source-powerbi.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] jako zdroj dat Power Apps](across-how-use-financials-data-source-powerapps.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] v Power Automate](across-how-use-financials-data-source-flow.md)




[!INCLUDE[footer-include](includes/footer-banner.md)]