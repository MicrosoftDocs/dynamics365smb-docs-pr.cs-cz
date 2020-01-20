---
title: Integrace Poradce při potížích v Microsoft Flow | Microsoft Docs
description: Pomocí poradce při potížích můžete dát svá Business Central data k dispozici jako zdroj dat a zadat OData URL svých webových služeb a vytvořit tak automatizovaný pracovní postup.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'workflow, Odata, Power App, SOAP'
ms.date: 10/01/2018
ms.author: solsen
---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Integrace Poradce při potížích v Microsoft Flow - URL požadavku je příliš dlouhé
Svá data [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete použít jako součást pracovního postupu v aplikaci Microsoft Flow.  

> [!NOTE]  
>   Musíte mít platný účet v [!INCLUDE[d365fin](includes/d365fin_md.md)] a ve službě Flow.  

Pokud vytváříte Microsoft Flow pomocí [!INCLUDE[d365fin](includes/d365fin_md.md)] konektoru, může se zobrazit chybová zpráva oznamující, že požadovaná adresa URL je po vytvoření toku příliš dlouhá, například následující: **URL adresa požadavku je příliš dlouhá**.

## <a name="cause"></a>Příčina
Aby se tok spustil, hledá změny ve vašich údajích. Při určování, zda se vaše data změnila, konektory porovnávají data v mezipaměti s novými daty požadovanými od zdroje.  

Pokud požadavek na data vytvoří adresu URL, která je příliš dlouhá, selže. Běžné příčiny mohou zahrnovat:
- Obecně jakákoli zdrojová tabulka s více než 250 řádky
- Zdrojové tabulky obsahující několik tisíc záznamů

## <a name="workaround"></a>Alternativní řešení
Postupujte podle těchto kroků pro alternativní řešení.
1. Zvolte úpravu toku, který selhává.
2. Rozbalte možnost **Zobrazit pokročilé možnosti** ve spouštěči toku.
3. Do pole **Přeskočit počet** zadejte počet záznamů, které chcete přeskočit.  
Pokud například tabulka, kterou používáte jako zdroj dat, má 4 000 záznamů, zadejte 4 000 jako počet záznamů, které chcete přeskočit.
4. Aktualizujte svůj tok.

> [!NOTE]  
> Konektor je aktuálně v beta verzi. Aktualizace způsobu změny dat jsou zamýšleny pro budoucí vydání.


## <a name="see-also"></a>Viz také
[Používání [!INCLUDE[d365fin](includes/d365fin_md.md)] v automatizovaném pracovním postupu.](across-how-use-financials-data-source-flow.md)  
[Začínáme](product-get-started.md)  
[Import obchodních dat z jiných finančních systémů.](across-import-data-configuration-packages.md)  
[Správa uživatelů a práv](ui-how-users-permissions.md)    
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finance](finance.md)  
