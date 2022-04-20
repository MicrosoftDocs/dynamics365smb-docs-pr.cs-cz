---
title: Working with Power BI Reports in Business Central| Microsoft Docs
description: Get insight, business intelligence, and KPIs from your Business Central data with Power BI.
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
# Práce se sestavami Power BI v [!INCLUDE [prod_short](includes/prod_short.md)]

V tomto článku se dozvíte některé základy o zobrazení sestav Power BI v [!INCLUDE [prod_short](includes/prod_short.md)].

## Přehled

Sestavy Power BI vám poskytnou přehled ve vašem [!INCLUDE[prod_short](includes/prod_short.md)]. Různé stránky v [!INCLUDE [prod_short](includes/prod_short.md)] obsahují část sestav Power BI, která může zobrazovat sestavy Power BI. Centrum rolí je typická stránka, kde uvidíte část sestav Power BI. Některé stránky se seznamem, například **Zboží**, obsahují také část Power BI.

[!INCLUDE [prod_short](includes/prod_short.md)] funguje společně se službou Power BI. Sestavy pro zobrazení v [!INCLUDE [prod_short](includes/prod_short.md)] jsou uloženy ve službě Power BI. V [!INCLUDE [prod_short](includes/prod_short.md)] můžete přepnout sestavu zobrazenou v části Power BI na libovolnou sestavu Power BI dostupnou ve vaší službě Power BI. Po prvním přihlášení do [!INCLUDE [prod_short](includes/prod_short.md)] a dokud se nepřipojíte ke službě Power BI, části budou prázdné, jak je znázorněno zde:

![Power BI part in Business Central.](./media/power-bi-part.png)

## Začínáme

### Předpoklady

Pokud používáte [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, musí být povolena pro integraci Power BI. Tuto úlohu obvykle provádí správce. Pro více informací navštivte [Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] online je již nastaven na integraci s Power BI.

### Registrace Power BI

Než budete moci používat Power BI s [!INCLUDE[prod_short](includes/prod_short.md)], budete se muset zaregistrovat ke službě Power BI. Pokud jste se ještě nezaregistrovali, přejděte na [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Při přihlášení použijte pracovní e-mailovou adresu a heslo.

## <a name="connect"></a>Připojení k Power BI - pouze jednou

Když se poprvé přihlásíte do [!INCLUDE [prod_short](includes/prod_short.md)], pravděpodobně se vám na různých stránkách zobrazí prázdná část Power BI (jak je znázorněno na předchozím obrázku). První věcí, kterou musíte udělat, je připojit se k vašemu účtu Power BI. Po připojení se zobrazí sestavy. Tento krok musíte provést pouze jednou.

1. Vyberte odkaz **Začínáme s Power BI** v části **Sestavy Power BI**.
2. Spustí se asistované nastavení **Nastavení sestav Power BI v Business Central**. Chcete-li pokračovat, vyberte **Další**.
3. Na stránce **Zkontrolujte svou licenci Power BI**. Udělejte jeden z následujích kroků.

   - Pokud jste se do Power BI ještě nepřihlásili, vyberte [Přejít na domovskou stránku Power BI](https://powerbi.microsoft.com). Zaregistrujte si účet a poté se vraťte na stránku [!INCLUDE[prod_short](includes/prod_short.md)] a dokončete nastavení.

   - Pokud již licenci máte, vyberte **Další**.
4. Na další stránce, [!INCLUDE[prod_short](includes/prod_short.md)] teď nahraje demo sestavu do Power BI. Bude to trvat několik minut, takže se to dělá v pozadí. Chcete-li dokončit nastavení, vyberte **Další** a poté **Dokončit**.

Spustí se proces připojení. Během procesu, [!INCLUDE [prod_short](includes/prod_short.md)] komunikuje se službou Power BI a určuje, jestli máte platný účet a licenci Power BI. Jakmile je vaše licence ověřena, zobrazí se na stránce výchozí sestava Power BI. Pokud se sestava nezobrazí, můžete ji vybrat z dané části.

> [!TIP]
> S [!INCLUDE [prod_short](includes/prod_short.md)] tento krok automaticky nahraje výchozí sestavy Power BI použité v [!INCLUDE [prod_short](includes/prod_short.md)] do vašeho pracovního prostoru Power BI.

#### Z [!INCLUDE [prod_short](includes/prod_short.md)] on-premises

Připojení k Power BI z [!INCLUDE [prod_short](includes/prod_short.md)] je podobné jako online. Na stránce **OPRÁVNĚNÍ K AZURE ACTIVE DIRECTORY SERVICE** však můžete být vyzváni k udělení přístupu ke službám Power BI. Chcete-li udělit přístup, vyberte **Služby autorizace Azure** a poté **Přijmout**.

Po připojení můžete vybrat sestavu z části Power BI na stránkách.

## Práce se sestavou Power BI

### Zobrazení sestavy na stránkách seznamu

[!INCLUDE[prod_long](includes/prod_long.md)] obsahuje na několika stránkách se seznamami záložku Power BI. Tato záložka poskytuje další pohled na data v seznamu. Při přechodu mezi řádky v seznamu se sestava aktualizuje a filtruje pro vybranou položku. Pokud tuto část nevidíte, vyberte na panelu akcí možnost **Akce** > **Zobrazit** > **Zobrazit/Skrýt sestavy Power BI**.

Informace o vytváření sestav pro stránky seznamů najdete v tématu [Vytváření sestav Power BI pro zobrazení dat seznamu v [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

### Přepínání sestav

Součást Power BI na stránce může zobrazovat všechny sestavy Power BI, které máte k dispozici. Chcete-li přepnout a zobrazit jinou sestavu, zvolte akci **Vybrat sestavu** z rozevíracího seznamu příkazů v horní části.

Stránka **Výběr sestav Power BI** zobrazuje seznam všech sestav Power BI, ke kterým máte přístup. This list is retrieved from any of your own workspaces or workspaces that have been shared with you in the Power BI service. Zaškrtněte políčko **Povolit** pro každou sestavu, kterou chcete zobrazit na stránce, a pak zvolte **OK**. Když se vrátíte na stránku, zobrazí se poslední povolená sestava. Pomocí rozevírací nabídky použijte příkazy **Předchozí** a **Další** k navigaci mezi sestavami.

### Získání dalších sestav

Pokud na stránce **Výběr sestav Power BI** nevidíte žádné sestavy nebo nevidíte sestavu, kterou chcete, zvolte **Získat sestavy**. Tato akce umožňuje hledat sestavy ze dvou míst: z *Mojí organizace* nebo ze *Služeb*.

- Zvolte **Moje organizace**, chcete-li přejít na služby Power BI. Zde si můžete prohlédnout sestavy v rámci vaší organizace, ke kterým jste dostali práva. Poté je můžete přidat do pracovního prostoru.
- Zvolte **Služby** abyste se dostali do Microsoft AppSource, kde můžete nainstalovat aplikaci Power BI.

> [!TIP]
> Pokud máte Power BI Desktop, můžete také vytvářet nové sestavy Power BI. Po publikování těchto sestav do pracovního prostoru Power BI se pak zobrazí na stránce **Výběr sestav Power BI**.

### Správa a úpravy sestav

V sestavě v části Power BI můžete provádět změny. Provedené změny pak budou publikovány ve službě Power BI. Pokud je sestava sdílena s ostatními uživateli, změny se jim také zobrazí, pokud je neuložíte do nové sestavy.

Chcete-li sestavu upravit, zvolte akci **Spravovat sestavu** z rozevírací nabídky v části Power BI. Pak začnite dělat změny. Po dokončení změn vyberte možnost **Soubor** > **Uložit**. Pokud se jedná o sdílenou sestavu a nechcete tuto změnu provést pro všechny uživatele, vyberte **Uložit jako**, abyste se vyhnuli provedení této změny pro všechny uživatele.

Po návratu do centra rolí se zobrazí aktualizovaná sestava. Pokud jste použili možnost **Uložit jako**, budete muset zvolit **Vybrat sestavu** a potom povolit, aby se nová sestava zobrazila.

> [!NOTE]
> Tato funkce není povolena pro [!INCLUDE [prod_short](includes/prod_short.md)] on-premises.

### <a name="upload"></a>Nahrání sestav

Sestavy Power BI lze mezi uživatele distribuovat jako soubory PBIX. Pokud máte nějaké .pbix soubory, můžete je nahrát a sdílet se všemi uživateli [!INCLUDE [prod_short](includes/prod_short.md)]. Sestavy jsou sdíleny v rámci každé společnosti v [!INCLUDE [prod_short](includes/prod_short.md)].

Pokud chcete sestavu odeslat, vyberte akci **Odeslat sestavu** z rozevíracího seznamu příkazů v části **Sestavy Power BI**. Potom vyhledejte soubor .pbix, který definuje sestavy, které chcete sdílet. Můžete změnit výchozí název souboru.

Po nahrání sestavy do pracovního prostoru Power BI se tato sestava automaticky nahraje do pracovních prostorů Power BI jiných uživatelů.

> [!NOTE]
> Nahrání sestavy vyžaduje, abyste měli uživatelská oprávnění SUPER v [!INCLUDE[prod_short](includes/prod_short.md)]. Nahrávat sestavy nemůžete také pomocí [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. V on-premises prostředí nahráváte sestavy přímo do pracovního prostoru Power BI. Pro další informace navštivte [Práce s [!INCLUDE [prod_short](includes/prod_short.md)] Data In Power BI](across-working-with-business-central-in-powerbi.md).

## Řešení problémů

Pokud se však něco pokazí, tato část poskytuje řešení pro nejtypičtější problémy.

### Nemáte účet Power BI

Účet Power BI nebyl nastaven. Chcete-li získat platný účet Power BI, musíte mít licenci a abyste vytvořili pracovní prostor Power BI, musíte se do Power BI předem registrovat.

### Zpráva: Nejsou povoleny žádné sestavy. Zvolte Vybrat sestavu, chcete-li zobrazit seznam sestav, které můžete zobrazit.

Tato zpráva se zobrazí, pokud se výchozí sestavě nepodařilo nasadit do vašeho pracovního prostoru Power BI. Nebo se nasadilo, ale neproběhlo úspešné obnovení. Přejděte do sestavy v pracovním prostoru Power BI, vyberte **Sada dat**, **Nastavení** a pak ručně aktualizujte přihlašovací údaje. Jakmile se datová sada úspěšně aktualizuje, přejděte zpět na [!INCLUDE[prod_short](includes/prod_short.md)] a ručně vyberte sestavu ze stránky **Vyberte sestavy**.

#### Na stránce seznamu „Vybrat sestavu“ není vidět sestava.

Je to pravděpodobně proto, že název sestavy neobsahuje název stránky seznamu. Vymažte filtr a získejte úplný seznam dostupných sestav Power BI.

## Zobrazit související školení na webu [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Viz také

[Business Central a Power BI](admin-powerbi.md)    
[Vytváření sestav Power BI k zobrazení dat [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)    
[Integrace komponent Power BI a přehledu architektur pro [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)    
[Práce s daty [!INCLUDE [prod_short](includes/prod_short.md)] v Power BI](across-working-with-business-central-in-powerbi.md)    
[Power BI pro uživatelé](/power-bi/consumer/end-user-consumer)    
[„Nový vzhled“ služby Power BI](/power-bi/service-new-look)    
[Rychlý start: Připojení k datům v Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)    
[Dokumentace Power BI](/power-bi/)    
[Business Intelligence](bi.md)    
[Připravte se na podnikání](ui-get-ready-business.md)    
[Import obchodních dat z jiných finančních systémů](across-import-data-configuration-packages.md)    
[Nastavení [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] jako zdroje dat Power BI](across-how-use-financials-data-source-powerbi.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] jako zdroje dat Power Apps](across-how-use-financials-data-source-powerapps.md)    
[Použití [!INCLUDE[prod_short](includes/prod_short.md)] v Power Automate](across-how-use-financials-data-source-flow.md)




[!INCLUDE[footer-include](includes/footer-banner.md)]