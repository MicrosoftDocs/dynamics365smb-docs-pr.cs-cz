---
title: Troubleshooting your company hub
description: Learn how to work around any issues when you the company hub in Dynamics 365 Business Central to manage work across multiple companies.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 04/01/2021
ms.author: edupont

---
# Odstraňování problémů s Company Hub (Centrem společností)

Přidání společností na řídicí panel centra společnosti je dostatečně snadné, ale tento článek řeší problémy, které mohou nastat při nastavení.

## Kontrola chyb

Použijte akci **Zkontrolovat chyby** pro zobrazení posledních chyb. Můžete zobrazit další podrobnosti o každé chybě a protokol můžete vyčistit odstraněním starších položek.

## Připojení se nezdařilo.

Existuje několik důvodů, proč se nemůžete připojit ke společnosti, včetně následujících důvodů:

- URL adresa v poli **Odkaz na prostředí** je neplatná

   Přejděte na stránku **Odkaz na prostředí** otevřete prostředí, ke kterému se nemůžete připojit, a poté vyberte akci **Test spojení**.
- Společnost klienta je aktuálně offline, například pokud je upgradována.

   Na řídicím panelu zvolte položku menu **Nástroje** a poté vyberte **Zkontrolovat chyby**. Tím se otevře seznam s technickými podrobnostmi, takže pokud se vám zobrazí chyby, možná budete chtít kontaktovat svého správce. Například chybová zpráva "*Server odmítl pověření klienta*" čím se například naznačuje, že nemáte přístup.
- V prostředí, ke kterému se pokoušíte připojit, nemáte přístup ke všem společnostem.

   V [!INCLUDE [prod_short](includes/prod_short.md)] může mít organizace více obchodních jednotek zvaných společnosti a vy nemusíte mít přístup ke všem společnostem. Spolupracujte se svým správcem nebo klientem a ujistěte se, že máte přístup ke společnostem, ve kterých musíte pracovat.

## Data se neaktualizují

Když přidáte společnost nebo požádáte o aktualizaci dat, [!INCLUDE [prod_short](includes/prod_short.md)] načte data.. Musíte si ale stránku obnovit sami, například zvolit akci **Načíst všechny společnosti** obnovit stránku prohlížeče, odejít z řídicího panelu a pak zase zpět nebo podobně.

Pokud jste přidali společnost, ale ta se v seznamu nezobrazuje, můžete také aktualizovat seznam pomocí akce **Načíst všechny společnosti** k aktualizaci seznamu.

## Viz také

[Spravujte práci napříč více společnostmi v centru společnosti](company-hub.md)  
[Přidání společností do Company hubu](company-hub-add-company.md)  
[Účetní zkušenosti v Business Central](finance-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]