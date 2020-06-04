---
title: Jak vytvořit přihrádky | Microsoft Docs
description: 'Nejúčinnějším způsobem vytvoření přihrádek ve vašem skladu je vygenerování skupin podobných přihrádek v sešitu pro vytvoření přihrádky, ale také je můžete vytvořit individuálně.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 01/22/2019
ms.author: sgroespe
---
# <a name="create-bins"></a>Vytváření přihrádky
Nejúčinnějším způsobem vytvoření přihrádek ve vašem skladu je vygenerování skupin podobných přihrádek v sešitu pro vytvoření přihrádky, ale také je můžete vytvořit individuálně z karty lokace. Můžete také použít funkci na stránce **Sešit vytvoření přihrádky** k vytváření přihrádek automaticky.  

## <a name="to-create-a-bin-from-the-location-card"></a>Vytvoření přihrádek z karty lokace  
1.  Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.  
2.  Vyberte lokaci, ze které budete chtít založit přihrádku a vyberte tlačítko **Přihrádky**.  
3. Zvolte akci **Nový**.
4. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="the-dedicated-field"></a>Políčko Přiřazený
Políčko **Přiřazený** na stránce **Přihrádky** určuje, že množství v přihrádce je chráněno před vyskladněním z jiných požadavků. Množství ve vyhrazených přihrádkách však lze stále rezervovat. V souladu s tím jsou množství ve vyhrazených přihrádkách zahrnuta do pole **Celkové množství k dispozici** na stránce **Rezervace**.

Vytvoření vyhrazené přihrádky má za následek podobnou funkčnost v základním skladu jako použití typů přihrádek, což je k dispozici pouze ve velkém (rozšířeném) skladu. Pro více informací navštivte [Založení typů přihrádky](warehouse-how-to-set-up-bin-types.md).

**Příklad:** Pracovní centrum je založeno s kódem přihrádky v poli **Kód přihrádky na výrobu**. Řádky komponent výrobní zakázky s tímto kódem přihrádky vyžadují, aby zde byly umístěny dopředu propláchnuté komponenty. Dokud však nebudou komponenty spotřebovány z této přihrádky, mohou z této přihrádky vybírat nebo spotřebovávat další požadavky na komponenty, protože jsou stále považovány za dostupný obsah přihrádky. Chcete-li se ujistit, že obsah přihrádky je k dispozici pouze pro požadavek na komponentu, který používá tuto výrobní přihrádku, musíte vybrat pole **Přiřazený** na řádku pro tento kód přihrádky.

> [!Caution]
> Zboží ve vyhrazených přihrádkách není chráněno, pokud jsou vybrány a spotřebovány jako součásti výroby nebo sestavy na stránce **Vyskladnění zásob**. Pro více informací navštivte [Vyskladnění pro výrobu nebo montáž v základním skladu](warehouse-how-to-pick-for-production.md).

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Vytvoření přihrádek individuálně v sešitu vytváření přihrádky  
1.  Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Sešit vytvoření přihrádky** a poté vyberte související odkaz.  
2.  Na každém řádku vyplňte pole, která jsou nezbytná pro pojmenování a charakterizaci přihrádek, které vytváříte.  
3.  Vyberte tlačítko **vytvořit přihrádky**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Vytvořte přihrádky automatizovaně pomocí sešitu vytvoření přihrádek.  
Než začnete automaticky vytvářet přihrádky, měli byste určit druh přihrádek, které jsou nezbytné pro vaši činnost, jakož i nejpraktičtější tok zboží prostřednictvím fyzické struktury vašeho skladu.  

> [!NOTE]  
>  Jakmile přihrádku použijete, nemůžete ji odstranit, pokud není prázdná. Pokud však chcete použít jiný systém pojmenování přihrádek, můžete pomocí deníku přeřazení přesunout své zboží do nového systému přihrádek. Tento proces je ruční a vyžaduje čas, proto je nejlepší správně nastavit své přihrádky od začátku.  

Chcete-li pracovat se stránkou **Sešit vytvoření přihrádky**, musíte být nastaveni jako zaměstnanec skladu v místě, kde se nachází přihrádky. Pro více informací navštivte [Založení zaměstnanců skladu](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Sešit vytvoření přihrádky** a poté vyberte související odkaz.  
2.  Vyberte tlačítko **Výpočet přihrádek**.
3. Na stránce **Výpočet přihrádek** v poli **Kód šablony přihrádky** vyberte šablonu přihrádky, kterou chcete použít jako model pro přihrádky, které vytváříte.
4.  Vyplňte popis přihrádek, které právě vytváříte.  
5.  Chcete-li vytvořit kódy přihrádky, vyplňte políčka **Od čísla** a **Do čísla** ve třech kategoriích zobrazených na stránce: **Regál**, **Sekce,** a **Úroveň**. Kód přihrádky může mít až 20 znaků.  

    > [!NOTE]  
    >  Počet znaků, které jste zadali do tří kategorií pro každé pole, například znaky, které jste zadali do tří polí **Od čísla** plus oddělovače pole, pokud existují, musí být 20 nebo méně.  

     Písmena v kódu můžete použít jako identifikační kombinaci, ale písmeno, které používáte, musí být stejné v poli **Od čísla** a **Do čísla** . Můžete například definovat část kódu Regál **Od čísla A01** a **do čísla A10**. Program není nastaven tak, aby generoval kódy se sekvencemi písmen, například od A01 do F05.  

6.  Pokud chcete, aby znak, například spojovací čárka, oddělila pole kategorií, která jste definovali jako součást kódu přihrádky, vyplňte tento znak do  pole **Oddělovač pole**.  
7.  Pokud chcete, aby program nevytvořil řádek pro přihrádku, pokud již existuje, vyberte pole **Zkontrolovat existující přihrádky**.  
8. Po vyplnění polí zvolte tlačítko **OK**.

    Program vytvoří řádek pro každou přihrádku v sešitu. Nyní můžete odstranit některé přihrádky, například pokud máte regál s průchodem přes první dvě úrovně několika sekcí.  

9. Po odstranění všech nepotřebných přihrádek, vyberte akci **Vytvořit přihrádky** a program vytvoří přihrádky pro každý řádek v sešitu.  

Opakujte postup pro další sadu přihrádek, dokud nevytvoříte všechny přihrádky ve skladu.  

## <a name="see-also"></a>Viz také  
[Správa skladů](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)     
[Správa montáže](assembly-assemble-items.md)    
[Podrobnosti návrhu: Správa skladů](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
