---
title: Business Central a balíčky obsahu Power BI | Microsoft Docs
description: 'Získávání přehledu, business intelligence, a indikátorů KPI z vašich Business Central dat je snadné s Power BI a s balíčky obsahu Business Central.'
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 10/01/2018
ms.author: edupont
---
# <a name="enabling-your-business-data-for-power-bi"></a>Povolení obchodních dat pro Power BI
Získávání přehledů o vašich [!INCLUDE[d365fin](includes/d365fin_md.md)] datech je snadné díky Power BI a balíčkům obsahu [!INCLUDE[d365fin](includes/d365fin_md.md)]. Power BI načte vaše data a poté sestaví řídící panel a přehledy vycházející z těchto dat.  

Musíte mít platný účet v Dynamics 365 a ve službě Power BI. Pokud si chcete vytvořit vlastní sestavy Power BI, musíte si také stáhnout [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Balíčky obsahu Power BI vyžadují oprávnění k tabulkám, ze kterých se získávají data. Další podrobnosti o požadavcích jsou popsány níže.  

Microsoft publikoval následující balíčky obsahu:

| Aplikace | Popis |
| --- | --- |
| Microsoft Business Central | Poskytuje řídicí panel s klíčovými finančními údaji v průběhu času, jako jsou příjmy versus náklady, provozní marže a hotovostní cyklus.|
| Microsoft Business Central - CRM | Poskytuje řídicí panel s klíčovými údaji o prodejních příležitostech a kontaktech.  |
| Microsoft Business Central - Prodej | Poskytuje řídicí panel s klíčovými údaji o prodejích a zásobách. |

## <a name="using-the-dashboards"></a>Používání řídicích panelů
Každá sada obsahu obsahuje sestavy, které můžete procházet:

* Vyberte jakýkoli vizuální prvek na řídícím panelu a nadneste jednu ze základních sestav  
* Filtrování sestavy nebo přidání polí, které chcete sledovat.  
* Připojte toto přizpůsobené zobrazení k řídícímu panelu a pokračujte ve sledování.  
  Data můžete aktualizovat ručně, a můžete nastavit plán aktualizace. Pro více informací navštivte [Konfigurace naplánované aktualizace](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Balíčky obsahu jsou překonfigurovány pro práci s daty z demonstrační společnosti, které získáte když se zaregistrujete do [!INCLUDE[d365fin](includes/d365fin_md.md)]. Při instalaci aplikací v Power BI a připojení k vlastním datům nemusí některé sestavy fungovat, protože se spoléhají na data, která vaše společnost nemá. V těchto případech můžete tuto sestavu jednoduše odstranit z řídicího panelu.  

> [!NOTE]  
>   Na základě vašich [!INCLUDE[d365fin](includes/d365fin_md.md)] dat si také můžete v Power BI vytvořit vlastní sestavy a řídící panely. Pro více informací navštivte [Připojení obchodních dat k Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="how-to-connect"></a>Jak se připojit
1. V dolní části levého navigačního podokna vyberte možnost **Získat data**.  
![Navigace k získání dat](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Můžete také začít přímo z Dynamics 365 Business Edition. Z centra rolí přejděte do části **Výběr sestavy** v části Centrum rolí Power BI. Z pásu karet vyberte buď **Služba** nebo **Moje organizace**. Pokud je vybrána některá z těchto akcí, budete přesměrováni do Galerie organizace v Power BI nebo do knihovny služeb v Power BI, která bude také filtrována, aby zobrazovala pouze balíčky obsahu související s [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. V poli **Služby** vyberte **Získat**. Otevře se stránka s **AppSource** a **Aplikacemi pro Power BI**.  
![Vyberte si balíčky obsahu z online služeb](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Vyberte kartu **Aplikace** na kartě **Aplikace pro Power BI**, vyberte balíček obsahu **Microsoft Dynamics 365 Business Central**, který chcete použít, a poté vyberte **Získat nyní**.  
![Zvolte Dynamics 365 Business Central a vyberte Získat nyní.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Po zobrazení výzvy zadejte název *vaší společnosti* v [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Toto není zobrazovaný název. Název společnosti naleznete na stránce „Společnosti“ ve vaší instanci [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].  
![Zvolte Dynamics 365 Business Central a vyberte Získat nyní.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Po připojení se do pracovního prostoru Power BI automaticky načte řídicí panel, sestava a datová sada. Po dokončení se dlaždice aktualizují údaji z vaší [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)] společnosti.
![Zvolte Dynamics 365 Business Central a vyberte Získat nyní.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Co teď ?

- Zkuste [Zadání dotazu v poli Q&A](https://docs.microsoft.com/en-us/power-bi/service-q-and-a-tips) v horní části řídicího panelu.
- [Změna dlaždic](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) v řídicím panelu.  
- [Vyberte dlaždici](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) pro otevření zdrojové sestavy.  
- I když bude vaše datová sada denně aktualizována, můžete plán aktualizace aktualizovat nebo zkusit aktualizovat na požádání, pomocí funkce **Aktualizovat hned**.

## <a name="system-requirements"></a>Systémové požadavky
Chcete-li importovat svá [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data do Power BI, musíte mít oprávnění k webovým službám používaným pro získávání dat. Webové služby vyžadované pro každý balíček obsahu zahrnují:

## <a name="role-center-reports"></a>Sestavy Centra rolí

**Microsoft Dynamics 365 Business Central – CRM**
- Prodejní příležitosti
- Excel šablona Zobrazit společnost
- Popisky sestavy Power BI

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Excel šablona Zobrazit společnost
- Popisky sestavy Power BI

**Microsoft Dynamics 365 Business Central – Projekty**
- Přehled projektů
- Řádky plánování projektu
- Řádky úlohy projektu
- Popisky sestavy Power BI
- Excel šablona Zobrazit společnost

**Microsoft Dynamics 365 Business Central - Prodej**
- Řídicí panel prodeje
- Excel šablona Zobrazit společnost
- Popisky sestavy Power BI

## <a name="list-page-reports"></a>Sestavy Stránky seznamu

**Microsoft Dynamics 365 Business Central – Seznam zákazníků**
- Prodej zboží podle Zákazníka
- Seznam zboží nákupu Power BI
- Seznam prodávaného zboží Power BI
- Řídicí panel prodeje
- Seznam zákazníků Power BI
- ExcelŠablonaZobrazitSpolečnost
- Popisky sestavy Power BI

**Microsoft Dynamics 365 Business Central – Seznam věcných položek**
- Seznam částek Power BI
- Power BI částka finančního rozpočtu
- ExcelŠablonaZobrazitSpolečnost
- Popisky sestavy Power BI

**Microsoft Dynamics 365 Business Central – Seznam Zboží**
- Prodej zboží podle Zákazníka
- Seznam zboží nákupu Power BI
- Seznam prodávaného zboží Power BI
- Řídicí panel prodeje
- ExcelŠablonaZobrazitSpolečnost
- Popisky sestavy Power BI

**Microsoft Dynamics 365 Business Central - Seznam projektů**
- Seznam projektů Power BI
- ExcelŠablonaZobrazitSpolečnost
- Popisky sestavy Power BI

**Microsoft Dynamics 365 Business Central - Seznam nákupních fakturr**
- Nákupní seznam Power BI
- ExcelŠablonaZobrazitSpolečnost
- Popisky sestavy Power BI

**Microsoft Dynamics 365 Business Central - Seznam prodejních objednávek**
- Prodejní seznam Power BI
- ExcelŠablonaZobrazitSpolečnost
- Popisky sestavy Power BI


**Microsoft Dynamics 365 Business Central - Seznam dodavatelů**
- Seznam zboží nákupu Power BI
- Seznam prodávaného zboží Power BI
- Seznam dodavatelů Power BI
- ExcelŠablonaZobrazitSpolečnost
- Popisky sestavy Power BI

## <a name="web-services"></a>Webové služby
Snadným způsobem, jak najít webové služby, je vyhledávání webových služeb v [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. V seznamu zkontrolujte, zda je u výše uvedených webových služeb zaškrtnuto políčko Publikovat.

## <a name="troubleshooting"></a>Odstraňování problémů
Řídicí panel Power BI se spoléhá na publikované webové služby, které jsou uvedeny výše, a bude zobrazovat data z demonstrační společnosti nebo vaší vlastní firmy, pokud importujete data z vašeho aktuálního finančního řešení. Pokud se však něco pokazí, tato část poskytuje řešení pro nejtypičtějších problémy.

### <a name="incorrect-company-name"></a>Nesprávný název společnosti  
Častou chybou je, že místo názvu společnosti zadáte zobrazovaný název společnosti. Chcete-li najít název společnosti, hledejte **Společnosti**. Při zadávání názvu společnosti použijte pole **Název**.

### <a name="incorrect-user-name-and-password"></a>Nesprávné uživatelské jméno a heslo  
Uživatelské jméno a heslo použité pro připojení bude stejné jako to, které se používá pro připojení k vašemu účtu Microsoft Office 365.  

Balíčky obsahu také vyžadují, abyste měli účet Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Jakmile zadáte své přihlašovací údaje, automaticky zjistíme všechny klienty Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], ke kterým máte přístup. Pokud nemáte licencovaný nebo zkušební účet Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], zobrazí se chybová zpráva.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Klíč neodpovídal žádným řádkům v tabulce
Pokud během procesu připojení zadáte neplatný název společnosti, může se zobrazit chybová zpráva „Klíč neodpovídá žádným řádkům v tabulce“. Zadejte správný název společnosti a zkuste se znovu připojit.

## <a name="see-also"></a>Viz také
[Začínáme s Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Základní pojmy](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Business Intelligence](bi.md)  
[Začínáme](product-get-started.md)  
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Použití [!INCLUDE[d365fin](includes/d365fin_md.md)] jako zdroje dat Power BI](across-how-use-financials-data-source-powerbi.md)  
[Použití [!INCLUDE[d365fin](includes/d365fin_md.md)] jako zdroje dat PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Použití [!INCLUDE[d365fin](includes/d365fin_md.md)] v Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
