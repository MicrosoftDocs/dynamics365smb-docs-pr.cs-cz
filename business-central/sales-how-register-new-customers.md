---
title: Vytvoření zákaznické karty pro záznam nových zákazníků | Microsoft Docs
description: 'Popisuje, jak vytvořit zákaznickou kartu pro registraci informací o každém novém zákazníkovi nebo klientovi, kterému prodáváte.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="register-new-customers"></a>Registrace nového zákazníka
Zákazníci jsou zdrojem vašich příjmů. Každého zákazníka, kterému prodáváte musíte registrovat, jako kartu zákazníka. Karty zákazníka obsahují informace, které jsou potřebné k prodeji produktů zákazníkovi. Pro více informací navštivte [Prodej faktur](sales-how-invoice-sales.md) a [Evidence nového zboží](inventory-how-register-new-items.md).  

Než budete moci evidovat nové zákazníky, musíte nastavit různé prodejní kódy, ze kterých si můžete vybrat při vyplňování zákaznických karet. Další informace naleznete v části [Nastavení prodeje](sales-setup-sales.md).

> [!NOTE]  
>   Pokud existují šablony zákazníka pro různé typy zákazníků, tak se při vytváření nové karty zákazníka objeví stránka, odkud můžete vybrat vhodnou šablonu. Pokud existuje pouze jedna šablona zákazníka, pak nové karty zákazníka používají vždy tuto šablonu.

## <a name="to-create-a-new-customer-card"></a>Vytvoření nové karty zákazníka
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci**, a poté vyberte související odkaz.  
2. Na stránce **Zákazníci** vyberte akci **Nový**.

    Pokud existuje pouze jedna šablona zákazníka, otevře se nová karta zboží s několika poli s předvyplněnými informacemi ze šablony.

    Pokud existuje více než jedna šablona zákazníka, otevře se stránka, ze které můžete vybrat požadovanou šablonu zákazníka. V takovém případě postupujte podle následujících dvou kroků.
3. Na stránce **Vybrat šablonu pro nového zákazníka** vyberte šablonu, kterou chcete použít pro novou kartu zákazníka.
4. Zvolte tlačítko **OK**. Otevře se nová karta zákazníka s některými předvyplněnými poli podle informací ze šablony.  
5. Postupujte podle potřeby tak, že vyplníte nebo změníte pole na kartě zákazníka. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Na záložce **Prodejní ceny** můžete zobrazit zvláštní ceny nebo slevy, které udělujete zadaným zákazníkům, pokud jsou splněna určitá kritéria, jako jsou položky, minimální objednávkové množství nebo datum ukončení. Každý řádek představuje zvláštní cenu nebo řádkovou slevu. Každý sloupec představuje kritérium, které musí platit, aby se zaručila zvláštní cena, kterou zadáte do pole **Jednotková cena**, nebo řádková sleva, kterou zadáte do pole **Řádková sleva %**. Pro více informací navštivte [Zaznamenat prodejní cenu, slevu a platební smlouvy](sales-how-record-sales-price-discount-payment-agreements.md).

Zákazník je nyní zaregistrován a karta zákazníka je připravena k použití v prodejních fakturách.

Chcete-li tuto zákaznickou kartu použít jako šablonu při vytváření nových karet zboží, můžete ji uložit jako šablonu. Pro další informace se podívejte na následující sekci.

## <a name="to-save-the-customer-card-as-a-template"></a>K uložení karty zákazníka jako šablony
1. Na stránce **Karta zákazníka**, vyberte akci **Uložit jako šablonu**. Stránka **Šablona zákazníka** otevírá kartu zákazníka jako šablonu.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Chcete-li znovu použít dimenze v šablonách, zvolte akci **Dimenze**. Stránka **Šablony dimenzí** otevírá jakékoli kódy dimenzí, které jsou pro daného zákazníka nastaveny.
4. Upravte nebo zadejte kódy dimenzí, které se budou vztahovat na nové karty zákazníka vytvořeného pomocí šablony.  
5. Po dokončení nové šablony zákazníka vyberte tlačítko **OK** .

Šablona zákazníka je přidána do seznamu šablon zákazníků, takže ji můžete použít k vytvoření nových karet zákazníků.

## <a name="see-also"></a>Viz také
[Vytváření Číselné řady](ui-create-number-series.md)  
[Prodej](sales-manage-sales.md)    
[Nastavení Prodeje](sales-setup-sales.md)    
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
