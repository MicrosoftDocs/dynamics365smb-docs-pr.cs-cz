---
title: Update Custom Report Layouts
description: Learn how to update a custom report layout used on a report when there are design changes to the report's data set, for example.
author: jswymer


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9652, 9650
ms.date: 06/24/2021
ms.author: edupont

---
# (Zastaralé) Aktualizace vlastních rozvržení sestav

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

V některých případech může být nutné aktualizovat vlastní rozvržení sestavy, které se používá v sestavách. To je nutné, pokud došlo ke změně dat sestavy, například pole použité v rozbržení bylo odebráno ze sady dat sestavy. Pokud rozložení sestavy vyžaduje aktualizaci, zobrazí se chybová zpráva při pokusu o zobrazení náhledu, tisk nebo uložení sestavy.

Rozložení sestavy můžete automaticky aktualizovat z chybové zprávy, která se zobrazí při spuštění sestavy, výběrem tlačítka **Ano** v chybové zprávě. Nebo před spuštěním sestav můžete aktualizovat konkrétní rozvržení sestav nebo všechna vlastní rozvržení sestav, které mohou být ovlivněny změnou setu dat.

Máte také možnost testovat aktualizace bez použití požadovaných změn ve vlastních rozloženích sestav. To vám umožní zjistit, jaké změny budou použity v rozvržení sestavy a identifikovat možné problémy v procesu. Z výsledků testů můžete otevřít vlastní rozvržení sestav pro úpravy a opravit případné problémy. Před instalací aktualizací doporučujeme otestovat rozvržení sestavy.

Ne všechny změny sady dat sestavy mohou být automaticky aktualizovány v rozložení sestavy. Některé změny vyžadují ruční úpravu rozvržení sestav. Pro více informací navštivte [Omezení aktualizace vlastního rozvržení sestavy](ui-update-report-layouts.md#UpdateLimitations).

## Aktualizace jedné nebo více vlastních rozvržení sestav

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výběr rozvržení sestav** a poté vyberte související odkaz.

2. Chcete-li na stránce **Výběr rozvržení sestav** aktualizovat konkrétní sestavu, vyberte rozvržení ze seznamu a poté zvolte akci **Aktualizovat rozložení**. Nebo pokud chcete aktualizovat všechna vlastní rozložení sestav pro vybranou společnost, vyberte akci **Aktualizovat všechna rozložení**.

Pokud nenastanou žádné chyby, bude aktualizace použita na rozvržení sestav. Pokud se vyskytnou chyby, objeví se zpráva obsahující chyby. Poté budete muset ručně upravit vlastní rozvržení sestav, abyste chybu opravili. Pro více informací navštivte [Oprava chyb](ui-update-report-layouts.md#FixErrors).

## Testování aktualizací vlastního rozvržení sestav

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výběr rozvržení sestav** a poté vyberte související odkaz.

2. Na stránce **Výběr rozvržení sestav**, vyberte akci **Testovat aktualizace rozvržení**.

Změny rozvržení sestavy se testují, ale nepoužijí se na skutečné rozvržení sestavy. Objeví se stránka **Protokol aktualizace rozložení sestavy** s informacemi o stavu a případných aktualizacích pro každé rozložení sestavy. Pokud se v rozvržení sestavy vyskytnou chyby, můžete k rozvržení sestavy přistupovat přímo ze sestavy, upravovat a opravit tak případné problémy. Pro více informací navštivte [Oprava chyb](ui-update-report-layouts.md#FixErrors).

## <a name="UpdateLimitations"></a> Omezení aktualizace vlastního rozvržení sestav
Existuje několik typů změn, které může automatická aktualizace použít u vlastních rozvržení sestavy, například pole použité v rozvržení bylo odebráno ze sady dat sestavy. Automatická aktualizace však nemůže zpracovat následující změny datové sady sestavy.

1. Mazání polí, popisů nebo datových položek

2. Duplicitní názvy polí v rozvržení sestavy po přejmenování pole v datové sadě. To je třeba považovat za chybu návrhu.

3. Scénáře aktualizace, kdy existuje více iterací rozvržení sestavy, které způsobí více akcí přejmenování stejných polí, popisů nebo datových položek.

Pokud proces aktualizace zjistí některý z těchto problémů, nelze aktualizaci použít. Problémy budete muset odstranit ručně, například úpravou rozvržení sestavy ve Wordu, nebo programově pomocí codeunit.

## <a name="FixErrors"></a> Opravy chyb
Pokud se při aktualizaci nebo testování aktualizací rozvržení sestavy zobrazí chybová zpráva, je pravděpodobné, že budete muset rozvržení sestavy upravit, abyste problém odstranili. Přečtěte si chybové hlášení, které vám pomůže určit příčinu problému.

Nejtypičtější problém nastane, když je pole, které se používá v rozvržení, odstraněno z datové sady sestavy. V takovém případě se v chybové zprávě zobrazí řádek s informací, že položka byla odstraněna. Chcete-li tento problém vyřešit, musíte upravit rozvržení a odstranit příslušné pole.

Pro více informací navštivte [Vytvoření a úprava vlastního rozvržení sestavy](ui-how-create-custom-report-layout.md#ModifyCustomLayout).

Po úpravě rozvržení zkuste rozvržení znovu aktualizovat.

## Podívejte se na související školení na webu [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## Viz také
[Správa rovržení sestav](ui-manage-report-layouts.md)  
[Práce se sestavami, dávkovými úlohami a XMLporty](ui-work-report.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]