---
title: Udržování rozložení sestavy k aktuálnímu stavu | Microsoft Docs
description: 'Možná budete muset aktualizovat vlastní rozvržení sestavy, které se používá v sestavách. Je to vyžadováno v případě, že došlo ke změně návrhu sady dat sestavy, například pole použité v rozvržení bylo ze sady dat sestavy odstraněno.'
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/01/2017
ms.author: jswymer
---
# <a name="updating-report-or-document-layouts"></a>Aktualizace rozvržení sestav a dokumentů
Možná bude nutné aktualizovat vlastní rozvržení sestavy, které se používá v sestavě. Je to vyžadováno v případě, že došlo ke změně návrhu sady dat sestavy, například pole použité v rozvržení bylo ze sady dat sestavy odstraněno. Pokud rozvržení sestavy vyžaduje aktualizaci, zobrazí se chybová zpráva při pokusu o zobrazení náhledu, tisk nebo uložení sestavy.  
  
Rozvržení sestavy můžete automaticky aktualizovat z chybové zprávy, která se zobrazí při spuštění sestavy, výběrem tlačítka **Ano** v chybové zprávě. Nebo před spuštěním sestav můžete aktualizovat konkrétní rozvržení sestav nebo všechna vlastní rozvržení sestav, které mohou být ovlivněny změnou setu dat.  
  
Máte také možnost testovat aktualizace bez použití požadovaných změn ve vlastních rozvržení sestav. To vám umožní zjistit, jaké změny budou použity v rozvržení sestavy a identifikovat možné problémy v procesu. Z výsledků testů můžete otevřít vlastní rozvržení sestav přímo pro úpravy a opravit případné problémy. Doporučujeme otestovat aktualizaci rozvržení sestavy před použitím aktualizací.  
  
Ne všechny změny sady dat sestavy mohou být automaticky aktualizovány v rozvržení sestavy. Některé změny vyžadují ruční úpravu rozvržení sestavy. Pro další informace navštivte [Omezení aktualizace rozvržení vlastní sestavy](ui-update-report-layouts.md#UpdateLimitations)  
  
## <a name="to-update-one-or-more-custom-report-layouts"></a>Aktualizace jedné nebo více vlastních rozvržení sestav  
  
1.  Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Rozvržení sestav** a pak vyberte související odkaz.  
  
2.  V okně **Rozvržení Sestav** chcete-li aktualizovat konkrétní sestavu, vyberte rozvržení v seznamu a poté zvolte akci **Aktualizovat rozvržení**. Nebo pokud chcete aktualizovat všechna vlastní rozvržení sestav pro společnost, vyberte akci **Aktualizovat všechna rozvržení**.  

Pokud nenastanou žádné chyby, budou aktualizace použity na rozvržení sestavy. Pokud se vyskytnou chyby, objeví se zpráva obsahující chyby. Poté musíte ručně upravit vlastní rozvržení sestavy, abyste chybu opravili. Pro další informace navštivte [Oprava chyb](ui-update-report-layouts.md#FixErrors).  

## <a name="to-test-custom-report-layout-updates"></a>Testování aktualizací vlastního rozvržení sestavy  
  
1. Zvolte ikonu ![Vyhledat Stránku nebo Sestavu](media/ui-search/search_small.png "Ikona Vyhledat Stránku nebo Sestavu"), zadejte **Výběr Rozvržení Sestav** a pak vyberte související odkaz.  
  
2. V okně **Výběr Rozvržení Sestav**, vyberte akci **Testovat aktualizace rozvržení**.  
  
   Změny rozvržení sestavy se testují, ale nepoužijí se na skutečné rozvržení sestavy. Objeví se okno **Protokol aktualizace rozložení sestavy**, které poskytuje stavu potenciální aktualizace pro každé rozvržení sestavy. Pokud existují chyby v rozvržení sestavy, můžete přistupovat k rozvržení sestavy přímo za účelem úpravy ze zprávy k vyřešení problémů. Pro další informace navštivte [Oprava chyb](ui-update-report-layouts.md#FixErrors).  
  
##  <a name="UpdateLimitations"></a> Omezení aktualizace vlastního rozvržení sestav  
 Existuje několik typů změn, které může automatická aktualizace použít pro vlastní rozvržení sestav, například pole použité v rozvržení bylo ze sady dat sestavy odstraněno. Automatická aktualizace však nemůže zpracovat následující změny sady dat sestav.  
  
1. Odstraněná pole, popisky nebo datové položky.  
  
2. Po přejmenování pole v sadě dat jsou duplikované názvy polí v rozvržení sestavy. To by mělo být považováno za chybu návrhu.  
  
3. Upgradujte scénáře, kde existuje více iterací rozvržení sestavy, které způsobují více přejmenování akcí na stejných polích, štítcích nebo datových položkách.  
  
   Pokud proces aktualizace zjistí některý z těchto problémů, nelze aktualizaci použít. Problémy budete muset vyřešit ručně, například úpravou rozvržení sestavy v aplikaci Word nebo programově pomocí upgradovacích kódových jednotek.  
  
##  <a name="FixErrors"></a> Opravy chyb  
 Pokud se při aktualizaci nebo testování aktualizací rozvržení sestavy zobrazí chybová zpráva, budete pravděpodobně muset upravit rozvržení sestavy, abyste problém vyřešili. Přečtěte si chybovou zprávu, která vám pomůže určit příčinu problému.  
  
 Nejtypičtější problém nastane, když pole použité v rozvržení bylo odstraněno ze sady dat sestav. V takovém případě se v chybové zprávě zobrazí řádek, který uvádí, že položka byla odstraněna. Chcete-li tento problém vyřešit, budete muset upravit rozložení a odstranit příslušné pole.  
  
 Pro další informace navštivte [Vytvoření a úprava vlastního rozvržení sestavy](ui-how-create-custom-report-layout.md#ModifyCustomLayout)  
  
 Po úpravě rozvržení zkuste rozvržení znovu aktualizovat.  
  
## <a name="see-also"></a>Viz také  
 [Správa rozvržení sestav](ui-manage-report-layouts.md)  
 [Práce se sestavami](ui-work-report.md)  