---
title: Set Up Payment Terms
description: In the base version of Business Central, use payment terms to manage due dates and payment discounts. 
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords:
ms.date: 04/01/2021
ms.author: edupont
---
# Nastavení platebních podmínek

Platební podmínky určují, jak spravujete splatnost a platební slevy. Můžete nastavit libovolný počet kódů platebních podmínek a definovat platební podmínky pomocí vzorců data. Když se poprvé zaregistrujete do [!INCLUDE [prod_short](includes/prod_short.md)], demonstrační společnost poskytuje několik platebních metod, které firmy často používají. Můžete si však přidat tolik, kolik jich potřebujete.

Zákazníkům a prodejcům můžete přiřadit platební podmínky, aby se na prodejních a nákupních dokumentech, které pro ně vytvoříte, vždy používaly stejné podmínky. V případě potřeby můžete změnit podmínky na prodejním nebo nákupním dokladu, například pokud chcete, aby vám konkrétní zákazník zaplatil do 7 dnů, nikoli do 14 dnů. Tím se nezmění výchozí platební doba přiřazená zákazníkovi. Stejné platební podmínky jsou k dispozici pro prodejní a nákupní doklady.

Když poté zaúčtujete fakturu, [!INCLUDE [prod_short](includes/prod_short.md)] vypočítá platební slevy na základě platebních podmínek. V té době se také vypočítá datum slevy na platbu, tj. poslední datum, kdy může zákazník zaplatit a získat slevu na platbu.

Podobně, když zaúčtujete dobropis, [!INCLUDE [prod_short](includes/prod_short.md)] vypočítá možné skonto na základě platebních podmínek. Sleva z dobropisu se počítá podle stejných zásad jako slevy na platbách na fakturách. Pokud je na fakturu použit dobropis, bude případná částka slevy na platbě na faktuře snížena o částku slevy na platbě na dobropis.

Chcete-li svým zákazníkům zasílat upomínky na platby po splatnosti, musíte nastavit úrovně připomenutí a podmínky. Další informace naleznete v tématu [Nastavení podmínek upomínek a úrovní upomínky](finance-setup-reminders.md).

## Nastavení platebních podmínek

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Platební podmínky<x5/> a vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Po nastavení platebních podmínek je přiřadíte zákazníkům a dodavatelům. Volitelně můžete svým platebním metodám přiřadit platební podmínky.

> [!TIP]
> V základní verzi [!INCLUDE [prod_short](includes/prod_short.md)] nejsou platební podmínky s částečnými platbami podporovány. Místo toho je nutné použít funkci záloh. Další informace naleznete v tématu [Nastavení záloh](finance-set-up-prepayments.md).
>
> V některých zemích *můžete* nastavit platební podmínky s částečnými platbami. Chcete-li zjistit, zda je tato funkce ve vaší zemi podporována, přečtěte si část **Lokální funkcionality** v navigačním podokně na levé straně webu [Docs.microsoft.com](about-localization.md).

## Viz také

[Nastavení platebních metod](finance-payment-methods.md)  
[Nastavení záloh](finance-set-up-prepayments.md)  
[Nastavení Financí](finance-setup-finance.md)  
[Evidence nového zákazníka](sales-how-register-new-customers.md)  
[Evidence nového dodavatele](purchasing-how-register-new-vendors.md)  
[Prodej](sales-manage-sales.md)  
[Nakupování](purchasing-manage-purchasing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]