---
title: "Inspecting Pages in Business Central"
description: Use the page inspection feature to zoom into details about the page design and data source. Page inspector is ideal for troubleshooting issues with your data.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.date: 10/01/2019
---

# Prohlížení stránek v Business Central

Funkce prohlížení stránky umožňuje získat podrobnosti o stránce a poskytnout tak přehled o návrhu stránky, různých prvcích, které stránku tvoří a zdroji na pozadí zobrazených dat. Funkce prohlížení stránky je speciálně navržena pro administrátory, uživatele napájení, podpůrné pracovníky a vývojáře. Je ideální pro určení datového modelu na pozadí stránky a řešení potíží. Pokud například narazíte na problém se stránkou, můžete pomocí inspekce stránky získat informace, které předáte správci systému nebo pracovníkům podpory.

## Práce s kontrolou stránky

Prohlížení stránky zahájíte ze stránky **Nápověda a podpora**. Vyberte otazník v pravém horním rohu a vyberte **Nápověda a podpora**, a poté zvolte **Prohlížet stránky a data**. Nebo stačí použít klávesovou zkratku **Ctrl+Alt+F1**.

Na stránce se otevře podokno **Prohlížet stránky a data**. Následující obrázek znázorňuje podokno panelu **Prohlížet stránky a data** na stránce **Prodejní objednávka**.

![Prohlížet stránky a data](media/page-inspection-example.png)

Když se panel **Prohlížet stránky a data** otevře poprvé, zobrazí informace, které se týkají objektu hlavní stránky.

Pomocí klávesnice, nebo polohovacího zařízení přesuňte zaostření na různé prvky na stránce. Když vyberete okno s fakty, nebo část na hlavní stránce, ohraničovací oblast se zvýrazní ohraničením a panel **Prohlížet stránky a data** zobrazí informace o vybraném prvku. Například předchozí obrázek zobrazuje informace o části seznamu na stránce **Prodejní objednávka**. Když přejdete na jiné stránky v aplikaci, panel **Prohlížet stránky a data** se automaticky aktualizuje informacemi o stránce, podle vašeho postupu.

Pro více informací o tom, co je na prohlížení stránek zobrazeno navštivte [Prohlížení a řešení problému stránek](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) v nápovědě Vývojář Business Central a IT Pro.

Pokud nevidíte podrobnosti, které očekáváte, že se zobrazí na panelu **Prohlížet stránky a data** tak pravděpodobně nemáte potřebná oprávnění, jak je popsáno v následující části.

## Řízení přístupu k podrobnostem prohlížení stránek a dat

Jako administrátor můžete řídit přístup k úplným podrobnostem, které jsou zobrazeny v podokně  **Prohlížet stránky a data** nakonfigurováním oprávnění, která uživatelé mají. Chcete-li uživateli udělit oprávnění k úplným podrobnostem, dejte uživateli oprávnění **Provést** na objektu **Systém** **5330**. Toto oprávnění můžete udělit pomocí sady oprávnění (jako například **D365 Troubleshoot**) nebo skupiny uživatelů (jako je **D365 Troubleshoot**). Pro více informací navštivte [Přiřazení oprávnění uživatelům a skupinám](ui-define-granular-permissions.md).

Uživatelé, kterým nejsou udělena oprávnění v **Systémovém objektu 5330**, mají stále přístup k panelu **Prohlížet stránky a data**, ale zobrazí se jim pouze pole **Stránka** a pole **Tabulka**, která zobrazují základní podrobnosti, které mohou předat svému týmu podpory.

## Viz také

[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
