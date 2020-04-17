---
title: Nastavení osvědčených postupů - parametry plánování | Microsoft Docs
description: Záložka Plánování s náhledem na kartě zboží je středem dodavatelského řetězce společnosti. Nastavení správných parametrů plánování je velmi důležité pro efektivní nákladové řízení zásob a vysoký zákaznický servis.
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
# <a name="setup-best-practices-planning-parameters"></a>Nastavení osvědčených postupů: Parametry plánování
Záložka s náhledem **Plánování** na kartě zboží je středem dodavatelského řetězce společnosti. Nastavení správných parametrů plánování je velmi důležité pro efektivní nákladové řízení zásob a vysokou kvalitu zákaznického servisu.  

 Následující tabulka obsahuje doporučené postupy, jak nastavit vybraná pole parametrů plánování. Další informace o poli získáte kliknutím na odkaz ve sloupci **Nastavení pole**.  

|Nastavení pole|Osvědčený postup|Komentář|  
|-----------------|-------------------|-------------|  
|Způsob přiobjednání||Pro další informace, viz [Nastavení osvědčených postupů  Způsob přiobjednání](setup-best-practices-reordering-policies.md)|  
|Rezervovat|Vyberte **Nikdy**, když je zboží naplánováno pomocí objednávacího bodu.<br /><br /> Při výrobě vyberte **Nikdy**, aby plánovací systém pokrýval všechny požadavky.<br /><br /> Vyberte **Volitelné** pro zboží, které můžete chtít rezervovat pro zákazníky s nejvyšší prioritou.<br /><br /> Vyberte **Vždy** pro nejedinečné zboží, například zboží typu různé, které jsou příchozí pro konkrétní požadavky.|Rezervy obecně působí proti účelu plánování, kterým je vyvážit poptávku a nabídku. Proto by položky, které jsou nastaveny pro plánování, by neměly být rezervovány.<br /><br /> Pokud si uživatel rezervuje množství zásob pro budoucí poptávku, bude plánovací základna narušena a bod přiobjednání nemusí fungovat správně. I když je plánovaná úroveň zásob přijatelná s ohledem na pořadí, množství nemusí být kvůli rezervaci k dispozici.|  
|Období prodlevy|Nastavte s ohledem na flexibilitu dodavatele.<br /><br /> Delší období vám umožní poskytovat lepší služby zákazníkům, ale také způsobí další změny plánu.|Pokud dodavatel přijme změny objednávek na poslední chvíli, použijte delší období, ale buďte připraveni na další změny plánu. Pokud dodavatel vyžaduje pevné plánování, zkraťte toto období co nejvíce.<br /><br /> Informace o poli **Období prodlevy** naleznete v [Podrobnosti návrhu: Parametry plánování](design-details-planning-parameters.md)|  
|Zahrnutí zásob|Vyberte vždy, když používáte přiobjednání Dávka pro dávku.|Nevybírejte pouze ve zvláštních situacích, například když skladové položky nelze prodat.|  
|Bezpečná průběžná doba|Nastavte mezi 1D a 6D.<br /><br /> Nastavte bezpečnou průběžnou dobu alespoň jednoho dne, abyste se ujistili, že spotřební materiál je k dispozici den před tím, než jsou potřeba.<br /><br /> Pokud používáte nového dodavatele, definujte delší dobu, než bude znám jejich výkon při dodání.<br /><br /> Při výrobě definujte pro kritické komponenty delší bezpečnostní průběžné doby.|Dodávka, která je plánována systémem, aby se zabránilo výdeji, dorazí ve stejný den, kdy dojde k výdeji. Avšak i rozestup několika hodin může být příliš pozdě, pokud je například poptávka ráno a nabídka dorazí až odpoledne. **Poznámka:**  Pole **bezpečná průběžná doba** používá základní kalendář. 14D tedy nemusí být nutně dva týdny|  
|Minimální zásoby|Použijte pro položky s velkými výkyvy poptávky.<br /><br /> Při výrobě použijte pro kritické komponenty.<br /><br /> Použijte pro položky, na které se vztahují servisní smlouvy.|Pokud pole **Bod přiobjednání** není vyplněno, pak množství minimálních zásob funguje také jako bod přiobjednání.|  
|Období shromáždění šarží|Pokud chcete jen několik velkých objednávek a souhlasíte s tím, že budete mít zásoby, stanovte dlouhé období shromáždění šarží.<br /><br /> Pokud chcete více velkých objednávek a minimální zásoby, stanovte krátké období shromáždění šarží.|Období shromáždění šarží je obecně nejdelší období,  které budete mít zásoby.|  
|Bod přiobjednání|Založte základní bod přiobjednání na profilu zboží.|Pokud historické údaje ukazují, že průměrná poptávka po zboží je 100 jednotek během dodací lhůty sedmi dnů, lze bod pro objednání nastavit minimálně na 100.<br /><br /> To znamená, že když úroveň zásob klesne pod 100 jednotek, pak plánovací systém navrhne doplnění, protože dodání této položky trvá sedm dní a během těchto sedmi dnů musí být dostatek na pokrytí poptávky.|  
|Časový interval|Ponechte prázdné, což znamená, že úroveň zásob se kontroluje každý den.|Každodenní kontrola úrovně zásob zajišťuje optimální plánování bodů přiobjednání. **Poznámka:**  Časový interval 1W znamená, že úroveň zásob může být pod bodem uspořádání po dobu jednoho týdne před navržením objednávky dodávky.|  
|Přesnost zaokrouhlování|Ve výdajově náročné výrobě nastavte na 0,00001.|Velké množství zaokrouhleného odpadu nebo spotřeby materiálu může představovat velmi vysoké náklady na zásoby. Proto může být důležité stanovit nejmenší přesnost zaokrouhlování, aby se minimalizovaly tyto potenciální náklady.|  

> [!NOTE]  
>  Nejlepší osvědčené postupy pro parametry plánování na kartách zboží se vztahují na stejná pole na kartách SKJ.  
>   
>  Pokud společnosti plánují poptávku na různá místa, důrazně se doporučuje definovat kartu SKJ pro každé místo a že veškerá poptávka je vytvořena pomocí hodnoty v poli **Kód místa**. Pro více informací navštivte [Podrobnosti o designu: Poptávka na prázdné lokaci](design-details-demand-at-blank-location.md)  

## <a name="see-also"></a>Viz také  
 [Nastavení osvědčených postupů: Plánovač dodávek](setup-best-practices-supply-planning.md)   
 [Podrobnosti návrhu: Plánovač dodávek](design-details-supply-planning.md)   
 [Osvědčené postupy při nastavení komplexních oblasti aplikace](set-up-complex-application-areas-using-best-practices.md)  
 [Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
