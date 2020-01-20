---
title: Vytvoření karet zboží pro zboží a služby | Microsoft Docs
description: 'Vytvoření karty zboží pro služby, které prodáváte v hodinách a pro fyzické produkty, jako je zboží, hotové výrobky, komponenty nebo suroviny, které prodáváte ze svých zásob.'
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item, finished good, component, raw material, assembly item'
ms.date: 08/31/2017
ms.author: sgroespe
---
# <a name="register-new-items"></a>Evidence nového zboží
Zboží, mimo jiné, je základem vašeho podnikání, výrobků nebo služeb, se kterými obchodujete. Každé zboží musí být evidováno jako karta zboží.

Karty zboží obsahují informace, které jsou nutné k nákupu, skladování, prodeji, doručení a účtu zboží.

Karta zboží může být typu **Zásoby** nebo **Služby**, která určuje, zda je produkt fyzickou jednotkou nebo jednotkou času. Kromě některých polí, které se vztahují k fyzickým aspektům zboží, všechny políčka na kartě zboží fungují stejně jako skladové zboží a služby. Pro více informací o prodeji zboží navštivte [Prodej výrobků](sales-how-sell-products.md) nebo [Prodejní faktury](sales-how-invoice-sales.md).

Zboží lze strukturovat jako nadřazené s podřízeným zbožím v kusovníku. V [!INCLUDE [d365fin](includes/d365fin_md.md)], může být kusovník buď kusovníkem montáže nebo výrobním kusovníkem v závislosti na jeho použití. Pro více informací navštivte [Práce s kusovníkem](inventory-how-work-BOMs.md).

> [!NOTE]  
>   Pokud existují šablony zboží pro různé typy zboží, objeví se okno při vytváření nové karty zboží, odkud můžete vybrat vhodnou šablonu. Pokud existuje pouze jedna šablona zboží, pak nové karty zboží používají vždy tuto šablonu.

Pokud zakoupíte stejné zboží od více než jednoho dodavatele, můžete ho připojit k dané kartě zboží. Dodavatelé se poté zobrazí v okně **Katalog dodavatele zboží**, takže můžete snadno vybrat alternativního dodavatele.

## <a name="to-create-a-new-item-card"></a>Vytvoření nové karty zboží
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Zboží** a pak vyberte související odkaz.  
2. V okně **Zboží** vyberte akci **Nový**.

    Pokud existuje pouze jedna šablona zboží, otevře se nová karta zboží s několika poli vyplněnými informacemi ze šablony.
3. V okně **Vybrat šablonu pro nové zboží** vyberte šablonu, kterou chcete použít pro novou kartu zboží.
4. Zvolte tlačítko **OK**. Otevře se nová karta zboží s některými poli vyplněnými informacemi ze šablony.
5. Postupujte podle potřeby tak, že vyplníte nebo změníte pole na kartě zboží. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> V poli **Metoda ocenění** stanovíte, jak se vypočítají jednotkové náklady zboží, a to tak, že budete předpokládat tok fyzického zboží vaší společností. V závislosti na type zboží je k dispozici pět metod ocenění. Pro více informací navštivte [Podrobnosti o designu: Metody ocenění](design-details-costing-methods.md).
>
> Pokud vyberete **Průměr**, pak se jednotková cena zboží vypočítá jako průměrná jednotková cena v každém okamžiku po nákupu. Zásoby se oceňují s předpokladem, že všechny zásoby se prodávají současně. S tímto nastavením můžete vybrat pole **Pořizovací cena** pro zobrazení historie transakcí, z nichž se vypočítávají průměrné náklady, v okně **Přehled výpočtu průměrné  pořizovací ceny**.

Na záložce **Cena a účtování** můžete zobrazit zvláštní ceny nebo slevy, které udělujete za dané zboží, pokud jsou splněna určitá kritéria, jako je zákazník, minimální objednávkové množství nebo datum ukončení. Každý řádek představuje zvláštní cenu nebo řádkovou slevu. Každý sloupec představuje kritérium, které musí platit, aby se zaručila zvláštní cena, kterou zadáte do pole **Jednotková cena**, nebo řádková sleva, kterou zadáte do pole **Řádková sleva %**. Pro více informací navštivte [Zaznamenat prodejní cenu, slevu a platební smlouvy](sales-how-record-sales-price-discount-payment-agreements.md).

Položka je nyní evidovaná a karta zboží je připravena k použití v nákupních a prodejních dokladech.

Chcete-li tuto kartu zboží použít jako šablonu při vytváření nových karet zboží, můžete ji uložit jako šablonu. Pro další informace se podívejte na následující sekci.

## <a name="to-save-the-item-card-as-a-template"></a>Uložení karty zboží jako šablony
1. V okně **Karta zboží**, vyberte akci **Uložit jako šablonu**. Okno **Šablona zboží** otevírá kartu zboží jako šablonu.
2. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Chcete-li znovu použít dimenze v šablonách, zvolte akci **Dimenze**. Okno **Šablony dimenzí** otevírá jakékoli kódy dimenzí, které jsou pro dané zboží nastaveny.
4. Upravte nebo zadejte kódy dimenzí, které se budou vztahovat na nové karty zboží vytvořené pomocí šablony.
5. Po dokončení nové šablony zboží vyberte tlačítko **OK** .

Šablona zboží je přidána do seznamu šablon zboží, takže ji můžete použít k vytvoření nových karet zboží.

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Nastavení více dodavatelů pro zboží  
Pokud zakoupíte stejné zboží od více než jednoho dodavatele, musíte zadat informace o každém dodavateli zboží, jako jsou ceny, dodací lhůta, slevy atd.  

1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Zboží** a pak vyberte související odkaz.  
2.  Vyberte příslušné zboží a pak zvolte akci **Upravit**.  
3.  Zvolte akci **Dodavatelé**.  
4.  Vyberte pole **Číslo dodavatele** a poté vyberte dodavatele, kterého chcete pro zboží nastavit.  
5.  Volitelně vyplňte zbývající pole.  
6.  Opakujte kroky 2 až 5 pro každého dodavatele, od kterého chcete zboží koupit.

Dodavatelé se nyní objeví v okně **Katalog zboží dodavatele**, které otevřete z karty zboží, abyste si mohli snadno vybrat alternativního dodavatele.

## <a name="see-also"></a>Viz také
  [Zásoby](inventory-manage-inventory.md)  
  [Nákup](purchasing-manage-purchasing.md)  
  [Prodej](sales-manage-sales.md)  
  [Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
