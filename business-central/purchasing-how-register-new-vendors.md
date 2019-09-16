---
title: Vytvoření karty dodavatele k zaznamenání nového dodavatele | Microsoft Docs
description: 'Naučte se, jak vytvořit kartu dodavatele pro registraci nového dodavatele.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="register-new-vendors"></a>Zaevidujte nové dodavatele
Dodavatelé poskytují produkty, které prodáváte. Každý dodavatel, od kterého nakupujete, musí být evidován jako karta dodavatele.

Než budete moci zaregistrovat nové dodavatele, musíte nastavit různé kódy nákupu, ze kterých si můžete vybrat, když vyplňujete karty dodavatele. Po vytvoření všech požadovaných hlavních dat můžete provést další konfiguraci dodavatele, například upřednostnit dodavatele pro platební účely a položky seznamu, které může dodavatel a jiní dodavatelé dodávat. Další skupinou úkolů nastavení dodavatelů je zaznamenat vaše dohody týkající se slev, cen a způsobů platby. Pro více informací navštivte [Nastavení nákupu](purchasing-setup-purchasing.md).

Karty dodavatelů obsahují informace, které jsou potřebné k nákupu produktů od dodavatele. Pro více informací navštivte [Evidence nákupů](purchasing-how-record-purchases.md) a [Evidence nového zboží](inventory-how-register-new-items.md).

> [!NOTE]  
>   Pokud existují šablony dodavatele pro různé typy dodavatelů, objeví se při vytváření nové karty dodavatele stránka, ze které můžete vybrat vhodnou šablonu. Pokud existuje pouze jedna šablona dodavatele, pak nové karty dodavatele vždy používají tuto šablonu.

## <a name="to-create-a-new-vendor-card"></a>Vytvoření nové karty dodavatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Dodavatelé** a poté vyberte související odkaz.  
2. Na stránce **Dodavatelé** zvolte **Nový**.

    Pokud existuje více než jedna šablona dodavatele, otevře se stránka, ze kterého můžete zvolit šablonu dodavatele. V takovém případě postupujte podle následujících dvou kroků.
3. Na stránce **Vybrat šablonu pro dodavatele** vyberte šablonu, kterou chcete použít pro novou kartu dodavatele.
4. Zvolte tlačítko **OK**. Otevře se nová karta dodavatele, s některými poli vyplněnými informacemi ze šablony.
5. Podle potřeby pokračujte ve vyplňování nebo změně polí na kartě dodavatele. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Pokud neznáte fakturační adresu, která bude použita pro každou fakturu od dodavatele, nevyplňujte pole **Věřitel**. Místo toho vyberte číslo věřitele poté, co jste nastavili nákupní poptávku, objednávku nebo záhlaví faktury.

Dodavatel je nyní zaregistrován a karta dodavatele je připravena k použití v nákupních dokladech.

Pokud chcete tuto kartu dodavatele použít jako šablonu při vytváření nových karet dodavatele, můžete ji uložit jako šablonu dodavatele. Pro další informace se podívejte na následující sekci.

## <a name="to-save-the-vendor-card-as-a-template"></a>Pro uložení karty dodavatele jako šablonu
1. Na stránce **Karta dodavatele**, vyberte akci **Uložit jako šablonu**. Stránka **Šablona dodavatele** se otevře, zobrazující kartu dodavatele jako šablonu.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Chcete-li znovu použít dimenze v šablonách, zvolte akci **Dimenze**. Stránka **Šablony dimenzí** se otevře, zobrazující všechny kódy dimenzí, které jsou pro dodavatele nastaveny.
4. Upravte nebo zadejte kódy dimenzí, které se budou vztahovat na nové karty dodavatelů vytvořené pomocí šablony.
5. Po dokončení vytváření nové šablony dodavatele vyberte tlačítko **OK** .  
   Šablona dodavatele je přidána do seznamu šablon dodavatelů, takže ji můžete použít k vytváření nových karet dodavatelů.

## <a name="see-also"></a>Viz také
[Vytváření Číselné řady](ui-create-number-series.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Evidence nákupu](purchasing-how-record-purchases.md)   
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
