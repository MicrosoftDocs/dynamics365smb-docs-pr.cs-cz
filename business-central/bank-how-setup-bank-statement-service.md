---
title: Nastavení Yodlee Bank Feeds | Microsoft Docs'
description: 'Můžete převést platební údaje do jakéhokoli formátu dat, který vaše banka vyžaduje a povolit export nebo import bankovních souborů.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, payment process'
ms.date: 02/26/2019
ms.author: sgroespe
---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Nastavení služby Envestnet Yodlee Bank Feeds
Můžete importovat elektronické bankovní výpisy z vaší banky pro rychlé naplnění na stránce **Deník odsouhlasení plateb**, abyste mohli zaplatit a odsouhlasit bankovní účet. Další informace naleznete v části [Automatické vyrovnání plateb a odsouhlasení bankovních účtů](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Rozšíření služba Envestnet Yodlee Bank Feeds do [!INCLUDE[d365fin](includes/d365fin_md.md)] je připravena k použití. Pro další informace se podívejte na [Přizpůsobení[!INCLUDE[d365fin](includes/d365fin_md.md)] pomocí Extensions](ui-extensions.md).

> [!NOTE]
> Služba Envestnet Yodlee Bank Feeds je podporovaná pouze  v US, Kanadě a UK.<br /><br />
> Funkce je podporována pouze v online verzi Business Central. Chcete-li tuto funkci používat on-premise, musíte získat cobrand účet od Envestnet Yodlee.

Poté, co aktivujete službu bankovního informačního kanálu, musíte propojit bankovní účet s online bankovním účtem, ze kterého zdroj pochází. Bankovní účty propojíte s online bankovními účty pomocí různých scénářů:

* Bankovní účet v [!INCLUDE[d365fin](includes/d365fin_md.md)] pro váš online bankovní účet neexistuje. Proto vytvoříte bankovní účet tím, že ho propojíte s online bankovním účtem.
* Bankovní účet, který chcete propojit s online bankovním účtem, existuje v [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Propojený bankovní účet musí být odpojen, protože chcete přestat používat bankovní službu pro daný účet.
* Online bankovní účty se změnily a vy chcete aktualizovat informace o bankovních účtech v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Když je bankovní služba aktivována, můžete nastavit bankovní účet, aby automaticky importoval nové bankovní výpisy do **Deníku odsouhlasení plateb** každé dvě hodiny. Transakce plateb, které již byly zveřejněny jako zaúčtované a/nebo odsouhlasené v **Deníku odsouhlasení plateb** nebudou importovány. Další informace naleznete v části “Povolit automatický import bankovních výpisů.“

> [!NOTE]  
> Používáte-li asistované nastavení Nastavení společností, některé kroky v následujících postupech budou realizovány automaticky, když se dostanete k nastavení firemního bankovního účtu. Další informace naleznete v [Začínáme](product-get-started.md).

## <a name="to-enable-the-bank-feed-service"></a>Povolení bankovní služby
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Otevřete bankovní účet, který použijete pro bankovní službu.
3. Na stránce **Bankovní účty** v poli **Formát importu bankovního výpisu** vyberte YODLEEBANKFEED.  

Bankovní služba bude aktivována, když propojíte bankovní účet s jeho souvisejícím online bankovním účtem. Viz další postup.  

> [!NOTE]
> Pokud používáte průvodce **nastavením společnosti** pro nastavení společnosti, povolíte službu zaškrtnutím políčka Použít **Služba bankovního informačního kanálu**. Více informací naleznete na [vytvíření nových společností v Business Cental](about-new-company.md)

## <a name="to-create-a-new-linked-bank-account"></a>Vytvoření nového propojeného bankovního účtu
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Vyberte relevantní bankovní účet a pak zvolte **Vytvořit nový propojený bankovní účet**. Po několika okamžicích se otevře stránka **Propojení bankovního účtu**.

    > [!NOTE]  
    > Toto stránka zobrazuje skutečnou webovou stránku služby Envestnet Yodlee Bank Feeds. Terminologie a funkčnost na stránce nemusí odpovídat instrukcím uvedeným v tomto tématu.  
3. Na stránce **Propojení online bankovního účtu** v podokně **Propojit účet** použijte funkci Hledat a vyhledejte banku, kde máte jeden nebo více online bankovních účtů.
4. Vyberte název banky. Otevře se podokno **Přihlášení**.
5. Zadejte uživatelské jméno a heslo, které používáte pro přihlášení do online banky a poté zvolte tlačítko **Další**.  
6. Služba bankovního informačního kanálu se připravuje na propojení prvního bankovního účtu v určené bance s novým bankovním účtem v [!INCLUDE[d365fin](includes/d365fin_md.md)].

    > [!NOTE]  
    > Máte-li v bance více online bankovních účtů, musíte pro tyto další online bankovní účty vytvořit bankovní účty v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Viz kroky 8 až 10.  

    Po dokončení procesu se název banky zobrazí v podokně **Mé účty** v záložce **Propojené**. Číslo v závorce udává, kolik online bankovních účtů bylo spojeno.  
7. Zvolte tlačítko **OK**.

    Pokud propojujete pouze jeden bankovní účet online, otevře se stránka **Bankovní účet** a zobrazí se název bankovního účtu online. V tomto případě je dokončena úloha propojení bankovního účtu. Zbývá jen nastavení bankovního účtu. Další informace naleznete v části [Nastavení bankovních účtů](bank-how-setup-bank-accounts.md).

    Pokud propojujete více online bankovních účtů, otevře se stránka **Propojení bankovníhch účtů** s uvedenými online bankovními účty, které nejsou ještě propojeny s bankovními účty v [!INCLUDE[d365fin](includes/d365fin_md.md)]. V tomto případě, následujte další krok.  
8. Na stránce **Propojení bankovního účtu** vyberte řádek pro online bankovní účet a poté zvolte akci **Odkaz na nový bankovní účet**.  

    Na stránce **Karta bankovního účtu** se otevře nový bankovní účet, který je předem vyplněn názvem online bankovního účtu.

    Pokud v [!INCLUDE[d365fin](includes/d365fin_md.md)] již existuje bankovní účet, ke kterému chcete připojit další bankovní účet, postupujte podle následujícího kroku.  
9. Na stránce **Propojení bankovního účtu** vyberte řádek pro online bankovní účet a poté zvolte akci **Odkaz na existující bankovní účet**.
10. Na stránce **Seznam bankovních účtů** vyberte bankovní účet, ke kterému ho chcete propojit a potom klepněte na tlačítko **OK**.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Propojení bankovního účtu s bankovním účtem online
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Vyberte řádek pro bankovní účet, který není propojen s bankovním účtem online, a poté vyberte akci **Propojit s bankovním účtem online**. Otevře se stránka **Propojení online bankovního účtu** s názvem banky, která je vyplněna v podokně **Propojení účtu**.
3. Vyberte název banky. Otevře se podokno **Přihlášení**.
4. Zadejte uživatelské jméno a heslo, které používáte pro přihlášení do online banky a poté zvolte tlačítko **Další**.  

    Bankovní služba se připravuje na propojení vašeho bankovního účtu v [!INCLUDE[d365fin](includes/d365fin_md.md)] s příslušným online bankovním účtem.  

    Po úspěšném dokončení procesu se název banky zobrazí v podokně **Mé účty** na kartě **Propojené**. Pokud má banka více než jeden bankovní účet, je propojen pouze bankovní účet, který jste vybrali v kroku 2.  
5. Zvolte tlačítko **OK**.

Na stránce **Seznam bankovních účtů** je zaškrtnuto políčko **Propojené**.

## <a name="to-unlink-a-bank-account"></a>Zrušení propojení bankovního účtu
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.  
2. Vyberte řádek pro propojený bankovní účet, který chcete odpojit od souvisejícího online bankovního účtu a vyberte akci **Odpojit online bankovní účet**.

> [!NOTE]  
> Pokud v dialogovém okně pro potvrzení zvolíte možnost **Ano**, odstraní se odkaz na online bankovní účet a údaje o přihlašování se vymažou. Chcete-li bankovní účet znovu propojit s bankovním účtem online, musíte se znovu přihlásit. Další informace naleznete v části "Propojení bankovního účtu s online bankovním účtem."

## <a name="to-update-bank-account-linking"></a>Aktualizace propojení bankovního účtu
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Vyberte příslušný bankovní účet a poté vyberte akci **Aktualizovat propojení bankovního účtu**.

Pokud existují problémy pro kterýkoliv z propojených bankovních účtů v okně **Seznam bankovních účtů** otevře se okno **Propojení bankovního účtu**, které specifikuje bankovní účty s problémy. Problémy lze nejlépe vyřešit zrušením propojení online bankovního účtu a následným znovu vytvořením odkazu. Další informace naleznete v části "Propojení bankovního účtu s online bankovním účtem."

## <a name="to-enable-automatic-import-of-bank-statements"></a>Povolení automatického importu bankovních výpisů
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Vyberte řádek propojeného bankovního účtu a poté zvolte akci **Automatický import výpisu z bankovního účtu**.
3. Na stránce **Nastavení automatického importu bankovního výpisu** v poli **Počet dní k započítání** nastavíte kolik dní zpětně se mají získat translakce.

    > [!NOTE]  
    > Doporučujeme nastavit tuto hodnotu na 7 nebo více dní.  
4. Zaškrtněte políčko **Povolit**.  

Každou hodinu bude nyní **Deník odsouhlasení plateb** naplněno novými platbami provedenými na online bankovním účtu.

> [!NOTE]  
> Transakce plateb, které již byly zveřejněny jako zaúčtované a/nebo odsouhlasené v **Deníku odsouhlasení plateb** nebudou importovány.

## <a name="see-also"></a>Viz také
[Nastavení bankovnictví](bank-setup-banking.md)  
[Správa bankovních účtů](bank-manage-bank-accounts.md)  
[Automatické aplikování plateb a odsouhlasení bankovních účtů](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] Pomocí rozšíření ](ui-extensions.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
