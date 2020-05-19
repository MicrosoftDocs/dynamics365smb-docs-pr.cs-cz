---
title: Jak vytvořit obsah přihrádek | Microsoft Docs
description: 'Poté co založíte přihrádky můžete začít vytvářet jejich obsah. Jinými slovy, můžete založit zboží, které chcete uložit do libovolné dané přihrádky, a nastavit pravidla, kterými se řídí plnění přihrádek konkrétním zbožím..'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="create-bin-contents"></a>Vytvoření obsahu přihrádky
Poté co založíte přihrádky můžete začít vytvářet jejich obsah. Jinými slovy, můžete založit zboží, které chcete uložit do libovolné dané přihrádky, a nastavit pravidla, kterými se řídí plnění přihrádek konkrétním zbožím.. Můžete to udělat manuálně na stránce **Obsah přihrádky** nebo automatizovaně na stránce **Sešit vytvoření obsahu přihrádky**.

## <a name="to-create-bin-content-manually"></a>Vytvření obsahu přihrádky manuálně  
1.  Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.  
2.  Vyberte lokaci, kde budete chtít založit obsah přihrádky a vyberte tlačítko **Přihrádka**.  
3.  Vyberte přihrádku, kde budete chtít založit obsah a vyberte tlačítko **Obsah přihrádky**.  
4.  Pro každé zboží, které chcete uskladnit do přihrádky, vyplňte řádek na stránce  **Obsah přihrádky** patřičnou informací. Některá políčka jsou již vyplněna s informacemi o dané přihrádce.  
5.  Nejdříve vyplňte pole **Číslo zboží** poté, pokud používate řízené vyskladnění a zaskladnění vyplňte pole jako jsou **Kód měrné jednotky**, **Maximální množství** a **Minimální množství**.  

Pokud je nutné vyplňte i pole **Pevné**. Pokud je přihrádka nastavena jako výchozí pro dané zboží, nastavte pole **Výchozí přihrádka**.  

Pokud používáte řízené vyskladnění a zaskladnění a pokud jste již zadali správné rozměrové informace o každé měrné jednotce zboží, maximální množství, které zadáte na stránce **Obsah přihrádky** je ověřováno na základně fyzikcé možnosti dané přihrádky. Minimální a maximální množství se používá při výpočtu doplňování přihrádky a navrhovaných zaskladňovacích míst.  

Pokud vyberete políčko **Pevné**, zafixujete dané zboží do přihrádky, to v [!INCLUDE[d365fin](includes/d365fin_md.md)] znamená, že se pokusí umístit zboží do přihrádky a pokusí se zachovat zboží pro danou přihrádku, i když množství v přihrádce bude 0. Ostatní zboží může být uloženo do přihrádky, dokonce i když bylo zboží částečně fixováno k přihrádce.  

> [!NOTE]  
>  Můžete založit několik přihrádek současně, přes **Sešit vytvoření obsahu přihrádky**.  

## <a name="to-create-bin-content-with-a-worksheet"></a>Vytvoření obsahu přihrádky pomocí sešitu  
Po vytvoření přihrádek můžete vytvořit obsah přihrádek, který chcete pro každou přihrádku pomocí sešitu vytvoření obsahu přihrádky.

1.  Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Sešit vytvoření obsahu přihrádky** a poté vyberte související odkaz.  
2.  V hlavičce sešitu, v poli **Název** vyberte sešit pro lokaci, kde chcete vytvořit obsah přihrádky.  
3.  V poli **Kód přihrádky** vyberte kód přihrádky, pro kterou chcete definovat obsah.   

    Pokud používáte přímé zaskladnění a vyskladnění na této lokaci, budou políčka **Typ přihrádky**, **Kód třídy skladu** a **Pořadí přihrádky** vyplněna automaticky. Toto je informace, kterou je třeba vzít v úvahu při definování obsahu přihrádky.  
4.  Vyberte zboží, které chcete přiřadit k přihrádce a vyplňte pole související s obsahem přihrádky. Pokud používáte přímé zaskladnění a vyskladnění a chcete použít funkci **Vypočítat doplnění přihrádky**, vyplňte políčka **Max. množství** a **Min. množství**.  

    Pro nastavení přihrádky jako preferované přihrádky pro dané zboží ikdyž je množství v přihrádce **0** a všechna ostatní kritéria zaskladnění jsou stejná, vyberte políčko **Pevné**.  
5.  Opakujte kroky 3 až 4 pro každé zboží pro přiřazení přihrádky.  
6.  Chcete-li zobrazit náhled a vytisknout obsah přihrádky, který jste zadali v sešitu, vyberte tlačítko **Tisk**. Pokračujte v revizi obsahu přihrádky, dokud nebudete spokojeni.  
7.  Až budete připraveni, vyberte akci **Vytvořit obsah přihrádky**  

V tomto sešitu můžete pracovat s řadou řádků obsahu přihrádky pro několik přihrádek a získat tak dobrý přehled o tom, co vkládáte do různých přihrádek v dané zóně, uličce nebo přihrádce.  

## <a name="see-also"></a>Viz také
[Výpočet doplnění přihrádky](warehouse-how-to-calculate-bin-replenishment.md)    
[Správa skladů](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)     
[Správa montáže](assembly-assemble-items.md)    
[Podrobnosti návrhu: Správa skladů](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
