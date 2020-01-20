---
title: Zobrazení vlastních sestav Power BI | Microsoft Docs
description: Pomocí sestav Power BI můžete získat další přehled o datech v seznamech.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 10/01/2018
ms.author: edupont
---
# <a name="viewing-list-data-in-power-bi-reports-in-business-central"></a>Zobrazení dat seznamu v Power BI Reports v Business Central 
[!INCLUDE[d365fin](includes/d365fin_md.md)] zahrnuje ovládací prvek Informačního okna na řadě klíčových stránek seznamu, který poskytuje další pohled do dat v seznamu. Při přechodu mezi řádky v seznamu se sestava aktualizuje a filtruje pro vybranou položku. Můžete vytvořit vlastní sestavy pro zobrazení v tomto ovládacím prvku, ale při vytváření sestav je třeba dodržovat několik pravidel, která zajistí požadované chování.  

> [!NOTE]  
>   Musíte mít platný účet v [!INCLUDE[d365fin](includes/d365fin_md.md)] a ve službě Power BI. Také si musíte stáhnout [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Pro více informací navštivte [Použití [!INCLUDE[d365fin](includes/d365fin_md.md)] jako zdroje dat Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Datová sada sestavy
Když vytváříte sestavu v Power BI Desktop, zadejte zdroj dat nebo webovou službu, která obsahuje data související se seznamem, ke kterému chcete sestavu přidružit. Pokud například chcete vytvořit sestavu pro Přehled prodeje, ujistěte se, že sada dat obsahuje informace týkající se prodeje.  

Chcete-li filtrovat data v sestavách na základě záznamu vybraného ze seznamu, musí být primární klíč použit jako filtr sestav. Aby bylo možné sestavy správně filtrovat, bude nutné, aby primární klíče byly součástí vaší sady dat. Ve většině případů je primárním klíčem seznamu pole **Číslo**.  

## <a name="defining-the-report-filter"></a>Definice filtru sestavy
Aby bylo možné správně filtrovat v  informačním panelu Power BI, musí mít sestava základní filtr sestavy (nikoli filtr stránky nebo vizuální filtr, a také ne pokročilý filtr). Filtr, který je předán do sestavy Power BI z každé stránky seznamu, bude založen na primárním klíči, jak je popsáno v předchozí části.  

Chcete-li definovat filtr pro sestavu, vyberte primární klíč ze seznamu dostupných polí a poté toto pole přetáhněte do sekce **Filtr sestav**.  

![Nastavení filtru sestavy pro přehled aktivity prodejní faktury](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Velikost a barva sestavy
Velikost sestavy musí být nastavena na 325 pixelů na 310 pixelů. To je nutné pro správné škálování sestavy v dostupném prostoru povoleném v informačním okně Power BI. Chcete-li definovat velikost sestavy, umístěte zaměření mimo oblast rozložení sestavy a poté vyberte ikonu malířského válečku.

![Nastavení šířky a výšky sestavy pro sestavu aktivity prodejní faktury](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Šířku a výšku sestavy můžete změnit výběrem možnosti **Vlastní** v poli **Typ**.

Podobně, pokud chcete aby se pozadí sestavy mísilo s barvou pozadí informačního okna Power BI, definujte barvu pozadí vlastní sestavy jako *E5E5E5*. Toto je volitelné.  

## <a name="reports-with-multiple-pages"></a>Sestavy s více stránkami
S Power BI můžete vytvořit jednu sestavu s více stránkami. Vizuální prvky, které chcete vidět na [!INCLUDE[d365fin](includes/d365fin_md.md)] stránkách seznamu, musí být na první stránce sestavy v Power BI.  

> [!NOTE]  
>  Power BI Fact Box může zobrazovat pouze první stránku sestavy; Pokud chcete vidět další sestavy, musíte rozbalit sestavu a pomocí karet ve spodní části přehledu přejít na jiné stránky.  

## <a name="saving-your-report"></a>Uložení vaší sestavy

Při uložení sestavy je doporučeno, aby název sestavy obsahoval název stránky seznamu, ve které chcete sestavu zobrazit. Například slovo *Dodavatel* musí být někde v názvu sestavy u těch sestav, které chcete zpřístupnit v Seznamu dodavatelů.  

Toto není požadavek; urychlí to však proces výběru sestav. Když je stránka výběru sestavy otevřena ze stránky seznamu, předáme filtr na základě názvu stránky, abychom omezili zobrazené sestavy.  Filtr můžete odebrat a získat tak úplný seznam sestav, které máte k dispozici v Power BI.  

## <a name="troubleshooting"></a>Odstraňování problémů
Tato část poskytuje řešení pro nejčastější problémy, které mohou nastat při vytváření sestavy Power BI.  

**Uživatel nevidí na stránce výběru sestavy tu sestavu, kterou chce vybrat**  
Pokud nemůžete vybrat sestavu, možným řešením je ověření názvu sestavy, aby se zajistilo, že obsahuje název stránky seznamu. Můžete také vymazat filtr a získat tak úplný seznam dostupných sestav Power BI.  

**Sestava je načtena, ale prázdná, nefiltrovaná nebo nesprávně filtrovaná**  
Ověřte, zda filtr sestavy obsahuje správný primární klíč. Ve většině případů se jedná o pole **Číslo**, ale například v tabulce **Věcných položek** musíte použít pole **Číslo položky**.

**Sestava je načtena, ale zobrazuje stránku, kterou jste neočekávali**  
Ověřte, že stránka, kterou chcete zobrazit, je první stránkou ve vaší sestavě.  

**Sestava se zobrazuje s nežádoucími šedými okraji, je příliš malá nebo příliš velká.**  
Ověřte, že velikost sestavy je nastavena na 325 pixelů x 310 pixelů. Uložte sestavu a poté obnovte stránku seznamu.  

## <a name="see-also"></a>Viz také
[Použití [!INCLUDE[d365fin](includes/d365fin_md.md)] jako zdroje dat Power BI](across-how-use-financials-data-source-powerbi.md)  
[Začínáme](product-get-started.md)    
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)    
[Finance](finance.md)  
