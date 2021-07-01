---
title: Add companies to your company hub
description: Learn how to add companies from other Business Central environments to your company hub so you can manage work across environments.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: accountant, accounting, company hub
ms.date: 04/01/2021
ms.author: edupont

---
# Přidání společnosti do Company Hub (Centra společností)

S centrem společnosti můžete přistupovat ke své práci z více společností z různých prostředí [!INCLUDE [prod_short](includes/prod_short.md)]. Prostředí a společnosti můžete přidat ručně, pokud se vaše společnosti nezobrazí automaticky v centru společnosti.

Přímo na vstupní stránce centra společnosti najdete nabídku **Nastavneí** odkud máte přístup ke stránce **Odkazy na prostředí**. Jednoduše vyberte **Nový** a poté vyplňte pole. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Centra společnosti můžete připojit k tolika společnostem, kolik jich potřebujete. Centrum společnosti však můžete připojit pouze ke společnostem, které jsou hostovány v [!INCLUDE [prod_short](includes/prod_short.md)] online.

## Propojení prostředí

Odkaz na prostředí je karta, na které určíte prostředí [!INCLUDE [prod_short](includes/prod_short.md)], které hostí jednu nebo více společností, ve které pracujete. Data na kartě pro každé prostředí zadáváte vy a můžete je podle potřeby změnit. Pole **Odkaz na prostředí** je však zásadní - takto můžete přistupovat ke každé společnosti v [!INCLUDE [prod_short](includes/prod_short.md)]. Pomocí akce **Test spojení** na pásu karet otestujte, že jste zadali správný odkaz. Odkaz, který musíte zadat, je v prostředí, které hostí společnost, kterou přidáváte, a musí obsahovat ID Azure Active Directory (Azure AD) nebo název domény organizace. Pokud například zadali doménu, jako je MyBusiness.com, pak odkaz na jejich [!INCLUDE[prod_short](includes/prod_short.md)] je ```https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1```. Jinak to bude vypadat asi takto: ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```

Odkaz se používá, když zvolíte společnost v centru společnosti.

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Akce pro společnost, která je uvedena v centru společnosti":::

> [!TIP]
> Pokud pracujete ve zkušební verzi [!INCLUDE [prod_short](includes/prod_short.md)], je snadné přidat společnosti k vašemu tenantu. Odkaz na prostředí můžete najít zkopírováním ID Azure Active Directory z části **Řešení problémů** na stránce nápovědy a podpory. Název prostředí je pravděpodobně ve výchozí hodnotě PRODUCTION. Přidejte tyto informace do pole **Odkaz na prostředí**, jako je ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1``` a poté zkuste **Test spojení**. Hodnotící společnost bude přidána na seznam.
>
> Pokud jste se přesunuli do třicetidenní zkušební společnosti , Má Společnost, můžete ji přidat do seznamu výběrem **Znovu načíst / Znovu načíst všechny společnosti**.

## Načtení společnosti

Když jste přidali svá prostředí, vaše společnosti se zobrazí automaticky. Pokud však víte, že do prostředí byla přidána nová společnost, můžete výběrem tlačítka **Načíst všechny společnosti** aktualizovat seznam. Stejnou akci použijte k aktualizaci dat z různých společností.

> [!TIP]
> Aby bylo možné aktualizovat data ve Centru společností, musíte mít přístup k datům ve společnostech, ze kterých data pocházejí.

## Viz také

[Spravujte práci napříč více společnostmi v centru společnosti](company-hub.md)  
[Zdroje nápovědy a podpory](product-help-and-support.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]