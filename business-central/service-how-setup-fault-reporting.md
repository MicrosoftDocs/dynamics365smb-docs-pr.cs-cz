---
title: Nastavení Hlášení poruch ve Správě servisu | Microsoft Docs
description: 'Naučte se, jak nastavit procesy hlášení poruch.'
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

# <a name="set-up-fault-reporting"></a>Nastavení hlášení poruch
Hlášení poruch vám umožňuje stanovit standardy pro zaznamenávání informací o poruchách pro předměty servisu. Můžete například určit, o jaký problém jde, příznaky které se u vás vyskytnou, důvod problému a jak jej vyřešit.  

Kódy poruchy popisují typické chyby předmětů servisu nebo akce provedené na předmětech servisu. V závislosti na úrovni hlášení poruch ve vaší společnosti může být nutné nastavit kódy oblasti poruchy a kódy příznaku před nastavením kódů poruchy. Oblast poruchy popisuje oblasti poruch předmětů servisu. Kódy příčin poruch popisují příčinu poruch předmětů servisu a v případě potřeby, zda vylučují záruční a smluvní slevy. Například byste mohli chtít vyloučit záruční a smluvní slevy, pokud byl zákazník nějakým způsobem odpovědný za poruchu na předmětu servisu. K servisním zakázkám přiřadíte kódy důvodu poruchy. Pro více informací navštivte [Práce na servisních úkolech](service-how-to-work-on-service-tasks.md).  

## <a name="to-specify-the-overall-level-of-fault-reporting-to-use"></a>Určení celkové úrovně hlášení poruch, která se má použít
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení servisu** a poté vyberte související odkaz.
2. V poli **Úroveň hlášení poruchy** vyberte jednu z možností popsaných v následující tabulce.  

    |**Úroveň poruchy**|**Popis**|  
    |------------|-------------|  
    |Žádný | Nepoužívají se žádné kódy hlášení.|  
    |Porucha | Kódy jsou uvedeny v tabulce **Kódy poruchy**. Tyto kódy identifikují poruchy předmětů servisu, nebo akce, které mají být přijaty pro předměty servisu. Související kódy můžete seskupit do seskupení **kódu oblasti poruchy**.|  
    |Porucha + Příznak | Poskytujete kombinaci kódů v tabulkách **Kódy poruchy** a **Kódy příznaků**. Mezi typické kódy příznaků patří indikátory, které může zákazník použít k popisu problému, jako je hluk nebo kvalita.|  
    |Porucha + Příznak + Oblast | Kódy poruch, symptomů a oblastí poruch používáte jako implementaci systému IRIS (International Repair Coding System).|  

Chcete-li dokončit nastavení hlášení poruch, můžete také určit, jaké opravy nebo řešení jsou spojeny s chybou nebo vadou. To lze nastavit na stránce **Vztahy kódů chyba/vyřešení**, kde nastavíte kombinace kódů pro skupinu předmětů servisu u toho předmětu servisu, ze kterého jste vstoupili do okna, a počet výskytů pro každý z nich.

## <a name="to-create-fault-and-resolution-code-relationships"></a>Vytvoření vztahů kódů Chyba a Vyřešení
<!--this needs to go in a working with topic--> Abyste mohli při údržbě položek vidět nejběžnější způsoby opravy konkrétních poruch předmětů, musíte si vytvořit informace o vztazích kódů poruch/vyřešení. Použijte dávkovou úlohu 
**Vložit vztahy kódů porucha/vyřešení** pro nalezení všech kombinací kódů poruchy a vyřešení v zaúčtovaných  servisních zakázkách, a zaznamenejte je na stránku **Vztahy kódů porucha/řešení** .

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vztahy kódů porucha/řešení** a pak vyberte související odkaz.  
2. Zadejte datum pro definování období, které chcete zahrnout do dávkové úlohy.  
3. Chcete-li seskupit vztahy podle skupiny předmětů servisu, zaškrtněte políčko **Vztah založený na skupině předmětů servisu**.  
4. Chcete-li zachovat záznamy, které jste již ručně vložili na stránku **Vztahy kódů  porucha/řešení**, zaškrtněte políčko **Uchovat ručně vložené položky**.  

## <a name="see-also"></a>Viz také
[Nastavení Správy servisu](service-setup-service.md)  
[Správa servisu](service-service.md)  
