---
title: Setting Up Your Browser
description: Describes how to set up browsers to work with Business Central and products that integrate with it.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 04/01/2021
ms.author: jswymer
---
# Nastavení a řešení potíží s prohlížečem pro práci s webovým klientem Business Central

Tento článek vysvětluje, jak nastavit prohlížeč tak, aby [!INCLUDE[web_client](includes/web_client.md)] a všechny jeho funkce fungovaly správně. Přečtěte si tento článek, pokud máte potíže s otevřením [!INCLUDE[web_client](includes/web_client.md)], protože některé problémy mohou být způsobeny nastavením prohlížeče.

Článek obsahuje podrobnosti o nastavení Microsoft Edge, ale s požadavky na JavaScript, Cookies a vyskakovací okna, které jsou všechny prohlížeče stejné. Pro další prohlížeče naleznete v instrukcích od výrobce.

## Použití podporovaného prohlížeče

Ujistěte se, že používáte jeden z podporovaných prohlížečů. Pro ověření běžte na [Minimální požadavky na používání Business Central](product-requirements.md#browsers).

## Povolení JavaScript z Business Central

*Problém:*

Pokud prohlížeč nepodporuje JavaScript, uvidíte **Nepodporovaný/VypnutýJavaScript** v adresním poli a **HTTP Error 404.0 - Not Found** hlášku, když zkusíte otevřít [!INCLUDE[prod_short](includes/prod_short.md)].

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Oprava:*

1. V Microsoft Endge, běžte do **Nastavení** > **Cookies a opránění stránek** > **JavaScript**.
2. Udělejte jeden z následujích kroků. Zvolte krok doporučený vaší organizací:

   - Posuňte přepínač **Povoleno** doleva (Vypnuto). Poté, vyberte **Přidat** a zadejte adresu (URL) pro [!INCLUDE[prod_short](includes/prod_short.md)] v poli **webu**. Vyberte **Přidat** jakmile to bude hotové.
   - Posuňte posuvník **Povoleno** doprava (Zapnuto).

## Povolte soubory cookies z Business Central

*Problém:*

If the browser doesn't allow cookies, you'll get the following error:

**Sorry, the page could not be found. Please check the address and try again.**

*Oprava:*

1. In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.
2. Move the **Allow sites to save and read cookie data** toggle to the right (On).

## <a name="popup"></a>Allow pop-ups from Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] integrates with several products. In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product. This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].

*Problém:*

If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:

**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Oprava:*

1. In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.
2. Move the **Blocked** toggle to the right (On).
3. Vyberte **Přidat**. In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.

## Viz také

[Troubleshooting Teams](admin-teams-troubleshooting.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]