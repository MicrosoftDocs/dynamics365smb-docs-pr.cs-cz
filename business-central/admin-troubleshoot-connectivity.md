---
title: Troubleshoot Connectivity
description: Describes how to use the Troubleshoot Connectivity page to identify and fix problems connecting to Business Central online.
author: jswymer

ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: connectivity, troubleshooting, connection problems
ms.date: 06/17/2021
ms.author: jswymer
ROBOTS: NOINDEX
---
# Řešení potíží s připojením pro Business Central

> **APPLIES TO:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Tato funkce je aktuálně ve verzi Preview. Funkce a dokumentace se může v pozdějších verzích změnit. Pokud byste chtěli přispět do dokumentace na základě vlastních zjištění a zkušeností, vyberte ![upravit článek na GitHubu.](media/github-edit-pencil.png) **Upravit** a navrhnout změny. Pak se na to podíváme!

[!INCLUDE[prod_short](includes/prod_short.md)] Online obsahuje stránku **Odstraňování problémů s připojením**, kterou můžete použít k identifikaci problémů s připojením ke službě online. Existuje několik věcí, které ovlivňují připojení k Business Central, jako je nastavení brány firewall vaší konfigurace sítě nebo služby domény. Stránka vám umožňuje spustit seznam kontrol, které diagnostikují běžné problémy s připojením Business Central. Tyto informace můžete použít k tomu, abyste se pokusili problémy vyřešit sami, nebo je předat zástupci podpory.

> [!NOTE]
> Stránka **Odstraňování problémů s připojením** netestuje výkon nebo spolehlivost sítě, jako je rychlost vašeho připojení. Ověřuje pouze připojení k různým prostředkům.

## Spuštění kontroly připojení

1. Otevřete internetový prohlížeč.
2. V adrese zadejte adresu URL, kterou používáte k otevření Business Central a přidání `/connectivity` na konci.

   Pokud například použijete `https://businesscentral.dynamics.com`, zadejte:

   ```http
   https://businesscentral.dynamics.com/connectivity
   ```

   Nebo pokud adresa URL obsahuje ID tenanta, například `https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB`, zadejte:

   ```http
   https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB/connectivity
   ```

3. Na stránce **Poradce při potížích s připojením** zvolte **Spustit kontrolu**.

   Spustí se řada kontrol a zobrazí se výsledek každé kontroly:

   - ![Konektivita byla úspěšná.](media/connectivity-check.png) označuje úspěšnou kontrolu.
   - ![Kontrola připojení se nezdařila.](media/connectivity-failed.png) označuje, že se kontrola nezdařila. Další podrobnosti najdete ve zprávě pod kontrolou.
   - ![Kontrola připojení nebyla spuštěna.](media/connectivity-blocked.png) označuje, že kontrola nebyla spuštěna, obvykle z důvodu selhání předchozí kontroly. Další podrobnosti najdete ve zprávě pod kontrolou.

4. Chcete-li znovu spustit kontrolu, zvolte **Restartovat kontrolu**.

Následující části vysvětlují kontroly, které jsou spouštěny, a poskytují několik tipů pro řešení případných problémů.

## Základní připojení k internetu

Zkontroluje, zda máte připojení k internetu, ověřením, že máte přístup ke známé veřejné doméně, jako je www.bing.com.

| Problém | Co můžete vyzkoušet |
|-------|-------------|
| Váš prohlížeč tuto kontrolu nepodporuje | Otevřete stránku v podporovaném prohlížeči a zkuste to znovu. Seznam podporovaných prohlížečů naleznete v tématu [Minimální požadavky pro používání Business Central - Prohlížeče](product-requirements.md#browsers) |
| Příkazem ping se nepodařilo otestovat server na následující adrese URL: {url} | Zkontrolujte nastavení brány firewall. |

## Načítání zdrojů CDN (Content Delivery Network)

[!INCLUDE[prod_short](includes/prod_short.md)] používá Azure Content Delivery Network (CDN) k poskytování prostředků, které jsou nutné ke spuštění webového klienta Business Central. Tato kontrola ověřuje, že požadované prostředky jsou dostupné a přístupné pomocí příkazu ping na instanci Business Central v CDN.

| Problém | Co můžete vyzkoušet |
|-------|-------------|
| Váš prohlížeč tuto kontrolu nepodporuje | Viz **Základní kontrola připojení k Internetu**. |
| Příkazem ping se nepodařilo otestovat server na následující adrese URL: {url} | Zkontrolujte nastavení brány firewall. |

## Ověřování uživatelů

Zkontroluje, zda se aktuální uživatel přihlásil pomocí platného účtu Business Central.

| Problém | Co můžete vyzkoušet |
|-------|-------------|
| Momentálně není ověřen žádný uživatel | Přihlaste se do Business Central pomocí platného uživatelského jména a hesla. |

## Zjišťování prostředí Business Central

Zkontroluje prostředí Business Central, která jsou k dispozici ověřenému uživateli, a poté ověří, zda lze uživatele ověřit v prostředí.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

| Problém | Co můžete vyzkoušet |
|-------|-------------|
| Žádný ověřený uživatel, který by tuto kontrolu provedl | Viz **Kontrola ověření uživatele**. |
| Nepodařilo se načíst dostupná prostředí pro váš účet. | Zkontrolujte seznam dostupných prostředí v Centru pro správu Business Central. |
| Vaše uživatelské jméno nebo heslo je nesprávné nebo nemáte platný účet. | Ověřte, zda jste se přihlásili pomocí správného uživatelského jména a hesla. |

## Připojení aplikační služby

Zkontroluje, zda se ověřený uživatel může připojit ke zjištěnému prostředí, obvykle počínaje produkčním prostředím.

| Problém | Co můžete vyzkoušet |
|-------|-------------|
| Žádný ověřený uživatel, který by tuto kontrolu provedl | Viz **Kontrola ověření uživatele**. |
| Nepodařilo se načíst dostupná prostředí pro váš účet. | Viz **Zjišťování prostředí Business Central**. |
| Žádná adresa clusteru, pro kterou by bylo možné provést tuto kontrolu | Zkontrolujte seznam dostupných prostředí v Centru pro správu Business Central. |
| Koncový bod verze neexistuje | Zkontrolujte seznam dostupných prostředí v Centru pro správu Business Central. |

## Viz také

[Zdroje nápovědy a podpory](product-help-and-support.md)  
[Přehled úkolů pro nastavení Business Central](setup.md)  
[Často kladené otázky k používání Business Central](across-faq.yml)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Středisko správy Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
