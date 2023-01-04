---
title: Analyzing Report Data with Excel and XML
description: Learn how to use Excel and XML to analyze a report dataset. 
author: jswymer

ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 03/16/2022
ms.author: jswymer

---
# Analýza dat sestavy pomocí Excelu a XML

[!INCLUDE[d365fin](includes/2021_releasewave2.md)]

Jako vývojář nebo pokročilý uživatel můžete pomáhat kontrolovat data generovaná pro danou datovou sadu sestav při vytváření nových sestav nebo při stávajících úpravách.  Chcete-li tuto funkci podporovat, můžete exportovat datovou sadu sestavy jako nezpracovaná data do sešitu aplikace Excel nebo do souboru XML – přímo. Například v aplikaci Excel můžete provést ad-hoc analýzu dat a diagnostikovat problémy.

## Začínáme

Chcete-li exportovat datovou sadu sestavy do excelového sešitu nebo souboru XML, otevřete sestavu v klientovi a na stránce požadavku vyberte **Odeslat do** > **Dokument Microsoft Excel (pouze data)** nebo **dokument XML**. Soubor bude stažen do vašeho zařízení.

## Další informace o aplikaci Excel (pouze data)

**Dokument aplikace Microsoft Excel (pouze data)** exportuje výsledky sestavy a kritéria, která byla použita k jejich vygenerování, ale nezahrnuje rozložení sestavy. Soubor Excel bude obsahovat úplnou datovou sadu jako nezpracovaná data uspořádaná do řádků a sloupců. Zahrnuty jsou všechny sloupce dat datové sady sestavy bez ohledu na to, zda jsou použity v rozložení sestavy.

Jakmile máte soubor Excel, můžete začít analyzovat data. Můžete například filtrovat data a použít Power Pivot k jejich zobrazení.

Při každém exportu výsledků se vytvoří nový list. Pomocí **Dokument aplikace Microsoft Excel (pouze data)** můžete spustit stejnou sestavu a znovu použít změny formátování. Například pro Power Pivot můžete znovu spustit sestavu pro jiné časové období, zkopírovat výsledky do listu a pak list aktualizovat. Aplikaci pro vytváření sestav najdete také na [AppSource](https://appsource.microsoft.com/).

> [!NOTE]
> Nelze exportovat sestavu, která má více než 1 048 576 řádků nebo 16 384 sloupců. S místním Business Central může být maximální počet exportovaných řádků ještě nižší. Business Central Server obsahuje konfigurační nastavení s názvem **Maximální počet řádků dat povolených k odeslání do aplikace Excel** pro snížení limitu z maximální hodnoty. Další informace naleznete v [Konfigurace serveru Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) nebo se obraťte na správce.

## Pro administrátory

- **Dokument aplikace Microsoft Excel (pouze data)** byl zaveden jako volitelná funkce ve vlně 2021 vydání 1., aktualizace 18.3. Chcete-li uživatelům poskytnout přístup k této funkci při spuštění vlny 2021 vydání 1., povolte aktualizaci funkce **Uložit datovou sadu sestavy do dokumentu aplikace Microsoft Excel** v nástroji ** Správa funkcí**. Další informace naleznete v tématu [Povolení nadcházejících funkcí s předstihem](/dynamics365/business-central/dev-itpro/administration/feature-management). Ve vlně 2021 vydání 2. se tato funkce stala trvalou, takže ji nebudete muset povolit.

- Chcete-li používat **dokument aplikace Microsoft Excel (pouze data),** musí uživatelské účty **povolit akci Exportovat datovou sadu sestav do aplikace Excel**. Toto oprávnění můžete uživatelům udělit přiřazením sady oprávnění **Nástroje pro řešení potíží** nebo **Exportovat sestavu aplikace Excel**. Další informace naleznete v části [Přiřazení oprávnění uživatelům a skupinám](ui-define-granular-permissions.md)

## Pro vývojáře a pokročilé uživatele

Možnost **Dokument aplikace Microsoft Excel (pouze data)** exportuje všechny sloupce, včetně sloupců, které obsahují filtry a pokyny k formátování pro jiné hodnoty. Zde je několik zajímavých bodů:

- Binární data v poli, například v obrázku, se neexportují.

   Ve sloupcích, které obsahují binární data, budou pole obsahovat text **Binární data ({0} bajtů),** kde **{0}** označuje počet bajtů.
- Počínaje verzí Business Central 2021 2. vydání obsahuje soubor aplikace Excel také list **Metadata sestavy**.

   Tento list zobrazuje filtry použité na sestavu a obecné vlastnosti sestavy, jako je název, ID a podrobnosti o rozšíření. Filtry jsou zobrazeny ve sloupci **Filtr (DataItem::Table::FilterGroupNo::FieldName)**. Filtry v tomto sloupci zahrnují filtry nastavené na stránce požadavku sestavy. Zahrnuje také filtry definované v kódu AL, například [ Vlastností DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) a [ Vlastností DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Další informace o návrhu sestavy naleznete [v tématu Přehled sestavy](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

## Viz také

[Práce se sestavami](ui-work-report.md)    
[Správa rozvržení sestav a dokumentů](ui-manage-report-layouts.md)    
[Přiřazení oprávnění uživatelům a skupinám](ui-define-granular-permissions.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]