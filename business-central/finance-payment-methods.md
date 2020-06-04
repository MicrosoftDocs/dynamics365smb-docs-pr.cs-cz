---
title: Nastavení způsobu platby | Microsoft Docs
description: 'Můžete použít různé metody způsobu platby, například šek, bankovní převod, hotovost nebo PayPal, k určení, jak byly prodejní a nákupní faktury zaplacené.'
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'check, bank transfer, cash, PayPal'
ms.date: 11/22/2018
ms.author: bholtorf
---
# <a name="defining-payment-methods"></a>Nastavení způsobu platby
Způsoby platby definují, jaký způsob platby od zákazníků preferujete a jak chcete platit svým dodavatelům. Metody se mohou u každého zákazníka a dodavatele lišit. Mezi typické způsoby platby patří **banka**, **hotovost**, **šek**, nebo **účet**. 

Zákazníkům a dodavatelům můžete přiřadit způsob platby, tak, aby se stejný způsob vždy použil u prodejních a nákupních faktur, které pro ně vytvoříte. V případě potřeby můžete způsob změnit přímo na prodejní nebo nákupní faktuře. Například, pokud chcete platit konkrétní nákupní fakturu v hotovosti, a nikoli šekem. Tímto se nezmění výchozí způsob platby přiřazený dodavateli.

Stejné způsoby platby se používají pro prodejní a nákupní faktury. Například, způsob platby v _hotovosti_ se používá jak při provádění plateb, tak při jejich přijímání. [!INCLUDE[d365fin](includes/d365fin_md.md)] předpokládá, že když vytváříte prodejní fakturu, očekáváte platbu, a opak zase u nákupních faktur. 

Vratky z dobropisu jsou však výjimkami, protože peníze tečou opačným směrem, od vás k vašemu zákazníkovi a od vašeho dodavatele k vám. Výchozí způsob platby proto není k dobropisům přiřazen. Pokud jste však určili platební podmínky pro zákazníka nebo dodavatele, tak zde existuje řešení. Avšak pole **Výpočet skonta   na   dobropisech** není k tomuto určeno. Pokud na stránce **Platební podmínky** zaškrtnete toto políčko, při vytváření dobropisu se přidá i výchozí způsob platby.

## <a name="to-set-up-a-payment-method"></a>Nastavení způsobu platby
[!INCLUDE[d365fin](includes/d365fin_md.md)] poskytuje několik platebních metod, které podniky často používají. Můžete jich však přidat tolik, kolik potřebujete.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Způsob platby** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>K přiřazení platební metody zákazníkovi nebo prodejci
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazník**, nebo **Dodavatel** a poté vyberte související odkaz.
2. V poli **Způsob platby** vyberte metodu, která se použije jako výchozí pro zákazníka, nebo dodavatele.

## <a name="see-also"></a>Viz také
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
