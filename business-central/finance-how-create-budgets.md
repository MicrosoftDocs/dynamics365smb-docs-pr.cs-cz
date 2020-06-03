---
title: Creating G/L Budgets| Microsoft Docs
description: Describes hos to create G/L budgets to forecast different financial activities and assign dimensions for business intelligence purposes.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/13/2020
ms.author: sgroespe

---
# Vytváření nákladových rozpočtů
Vytvořením rozpočtů se samostatnými názvy můžete mít více rozpočtů pro identická časová období. Nejprve nastavte název rozpočtu a zadejte čísla rozpočtu. Název rozpočtu je pak zahrnut ve všech položkách rozpočtu, které vytvoříte.

Při vytváření rozpočtu můžete pro každý rozpočet definovat čtyři dimenze. Tyto dimenze specifické pro rozpočet se nazývají dimenze rozpočtu. Dimenze rozpočtu pro každý rozpočet vyberete z dimenzí, které jste již nastavili. Dimenze rozpočtu lze použít k nastavení filtrů rozpočtu a přidání informací o dimenzích do položek rozpočtu. Pro více informací navštivte [Práce s dimenzemi](finance-dimensions.md).

Rozpočty hrají důležitou roli v obchodních informacích, například ve finančním výkazu založeném na účetních schématech, které zahrnují položky rozpočtu nebo při analýze rozpočtu oproti skutečným částkám v účetní osnově. Pro více informací navštivte [Business Intelligence](bi.md).

V nákladovém účetnictví pracujete s nákladovými rozpočty podobným způsobem. Pro více informací navštivte [Vytvoření rozpočtů nákladů](finance-create-cost-budgets.md).

## Vytvoření nového finančního rozpočtu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční rozpočty** a poté vyberte související odkaz.
2. Vyberte akci **Upravit seznam** a podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vyberte akci **Upravit rozpočet**.
4. V horní části stránky **Rozpočet** vyplňte pole podle potřeby, abyste určili, co se má zobrazit.

   Zobrazeny jsou pouze položky, které obsahují název rozpočtu, který jste zadali do pole **Název rozpočtu**. Vzhledem k tomu, že název rozpočtu byl právě vytvořen, neexistují žádné položky, které odpovídají filtru. Stránka je proto prázdná.
5. Chcete-li zadat částku, vyberte příslušnou buňku v matici. Otevře se stránka **Položky finančního rozpočtu**.
6. Vytvořte nový řádek a vyplňte pole **Částka**. Zavřete stránku **Položky finančního rozpočtu**.
7. Opakujte kroky 5 a 6, dokud nezadáte všechny částky rozpočtu.

> [!NOTE]
> Na záložce **Filtry** můžete filtrovat informace o rozpočtu podle dimenzí rozpočtu, které jste nastavili pod názvem rozpočtu.

## Export a import finančních rozpočtů s aplikací Excel
Pokud jde o prakticky všechny ostatní stránky, můžete exportovat data na rozpočtových stránkách do aplikace Excel pro další zpracování nebo analýzu. Pro více informací navštivte [Export firemních dat do Excelu](about-export-data.md).

> [!NOTE]
> Účetní osnovy, na nichž jsou založeny rozpočty hlavní knihy, mají řádky s typem účtů Nadpis, které obsahují součet řádků pod ním. Při exportu rozpočtu se data na všech řádcích exportují bez ohledu na typ účtu. Avšak zpět lze importovat pouze data na řádcích s typem účtu Účtování. Podle toho:<br /><br /> **Při importu finančního rozpočtu budou odstraněny všechny hodnoty nacházející se na řádcích s typem Nadpis.** <br /><br />Tím se zabrání nesprávným součtem po importu dat, která byla vytvořena nebo upravena v aplikaci Excel.<br /><br /> **Scénář**: Víte, že náklady na nové platy v rozpočtu budou 1 200 000 LM. Vy chcete vytvořit rozpočet pro oddělení mezd pro tři konkrétní řádky (typu účtu Účtování) pro zaměstnance na plný úvazek, zaměstnance na částečný úvazek a dočasnou pomoc. Tyto tři řádky jsou seskupeny pod záhlavím Mzdy.<br /><br />Do řádku záhlaví zadáte 1,200 000, exportujete rozpočet do Excelu a poté jej odešlete na oddělení mezd a řeknete jim, aby distribuovali 1.200.000. LM.<br /><br /> Oddělení mezd rozdělí částku na tři účtovací účty. Při importu zpět do finančního rozpočtu jsou tři účty vyplněny novými daty aplikace Excel, které se sčítají na 1.200 000 LM a řádek Nadpis je prázdný.

## Viz související školení na webu [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)

## Viz také
[Export vašich obchodních dat do Excelu](about-export-data.md)  
[Finance](finance.md)  
[Business Intelligence](bi.md)  
[Nastavení financí](finance-setup-finance.md)  
[Hlavní hniha a účetní osnova](finance-general-ledger.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
