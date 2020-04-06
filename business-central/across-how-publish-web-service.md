---
title: Expose objects as web services | Microsoft Docs
description: Publish objects as web services to make them immediately available for your Business Central solution.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 02/04/2020
ms.author: edupont

---
# Publikování webových služeb

Webové služby jsou lehký způsob, jak zpřístupnit funkce aplikace různým externím systémům a uživatelům. [!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje řadu objektů, které jsou ve výchozím nastavení vystaveny jako webové služby z důvodu integrace s jinými službami společnosti Microsoft, můžete ale také sami přidat další webové služby.

Webovou službu můžete nastavit v klientu [!INCLUDE[d365fin](includes/d365fin_md.md)]. Poté musíte webovou službu publikovat, aby byla přes síť dostupná. Uživatelé mohou webové služby najít nasměrováním prohlížeče na umístění serveru a vyžádáním seznamu dostupných služeb. Když publikujete webovou službu, je okamžitě k dispozici v síti pro ověřené uživatele. Všichni oprávnění uživatelé mají přístup k metadatům webových služeb, ale pouze uživatelé, kteří mají dostatečná oprávnění, mají přístup ke skutečným datům.

## Vytvoření a publikování webové služby
Následující kroky vysvětlují, jak vytvořit a publikovat webovou službu.

### Pro vytvoření a publikování webové služby

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Webové služby**, a poté vyberte související odkaz.
2. Na stránce **Webové služby** vyberte **Nový**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > **Codeunit** a **Stránka**  jsou platné typy webových služeb SOAP. **Stránka** a **Dotaz** jsou platné typy webových služeb OData.
> Pokud databáze obsahuje více společností, můžete také zvolit ID objektu, které je specifické pro jednu ze společností.
> Nakonec, je název služby viditelný pro spotřebitele webové služby a je základem pro identifikaci a rozlišování webových služeb, takže byste měli učinit tento název smysluplným.

3. Zaškrtněte políčko ve sloupci **Publikováno**.

Při publikování webové služby v polích **OData URL** a **SOAP URL**, zobrazí se adresy URL, které jsou generovány pro webovou službu. Webovou službu můžete okamžitě vyzkoušet výběrem odkazů v polích **OData URL** a **SOAP URL**. Volitelně můžete zkopírovat hodnotu pole a uložit jej pro pozdější použití.

> [!IMPORTANT]
> U codeunit, které jsou publikovány jako webová služba SOAP, musí být metody vystavěné v codeunitě v kódu označeny jako `[External]`.

Po publikování webové služby je tato služba k dispozici externím stranám. Dostupnost této webové služby můžete ověřit pomocí prohlížeče, nebo můžete vybrat odkaz na polích **OData URL** a **SOAP URL** na stránce **Webové služby**. Následující postup ukazuje, jak můžete ověřit dostupnost webové služby pro pozdější použití.

### Ověření dostupnosti webové služby.

1. Do prohlížeče zadejte příslušnou adresu URL. Následující tabulka znázorňuje typy adres URL, které můžete zadat pro různé typy webových služeb.

   > [!div class="mx-tdBreakAll"]
   > |Type|Syntax|Example|
> |----------------|------|-------|
> |SOAP|https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/ |https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument|
> |OData V4|https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*|https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument<br/>    The company name is case-sensitive.|

2. Zkontrolujte informace, které se zobrazí v prohlížeči. Ověřte, zda vidíte název webové služby, kterou jste vytvořili.

Při přístupu k webové službě a chcete zapisovat data zpět do [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte zadat název společnosti. Společnost můžete určit jako součást URI, jak je uvedeno v příkladech, nebo můžete určit společnost jako součást parametrů dotazu. Například následující URI odkazují na stejnou webovou službu OData a jsou obě platné URI.

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## Viz také

[Správa](admin-setup-and-administration.md)  
[Webové služby Business Central pro vývojáře](/dynamics365/business-central/dev-itpro/webservices/web-services)
