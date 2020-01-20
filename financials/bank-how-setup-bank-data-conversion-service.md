---
title: Nastavení převodu Bankovních dat | Microsoft Docs
description: 'Můžete nastavit bankovní účty, abyste mohli sledovat transakce a importovat nebo exportovat bankovní zdroje, jako je například Yodlee.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer'
ms.date: 06/02/2017
ms.author: sgroespe
---
# <a name="set-up-the-bank-data-conversion-service"></a>Nastavení služby převodu bankovních dat
Globální poskytovatel služeb, který převádí informace o platbách do libovolného formátu dat, který banka vyžaduje, je připojen a připraven k zapnutí v [!INCLUDE [d365fin](includes/d365fin_md.md)]. Tento postup se označuje v [!INCLUDE [d365fin](includes/d365fin_md.md)] jako služba pro převod bankovních dat.

Můžete exportovat platební řádky z okna **Deník plateb** do datového toku, který pak nahrajete do své banky pro automatické zpracování, takže nemusíte provádět elektronické platby individuálně. Další informace naleznete v části [Export plateb do Bankovních dokladů](payables-how-export-payments-bank-file.md).

Do okna **Deník odsouhlasení plateb** můžete importovat soubory bankovních výkazů pomocí služby pro převod bankovních dat a převést soubor, který obdržíte z banky, do datového proudu, který v [!INCLUDE [d365fin](includes/d365fin_md.md)] lze importovat. Další informace naleznete v části [Automatické vyrovnání plateb a odsouhlasení bankovních účtů](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Jako alternativu k importu bankovních výpisů pomocí služby převodu bankovních údajů můžete použít službu Envestnet Yodlee Bank Feeds. Pro více informací běžte na [Nastavení Envestnet  yodlee Bank služby](bank-how-setup-bank-statement-service.md).

Chcete-li importovat nebo exportovat bankovní soubory, musíte si nastavit vlastní bankovní účet a bankovní účty svých dodavatelů. Další informace naleznete v části N [astavení bankovních účtů](bank-how-setup-bank-accounts.md).

> [!NOTE]  
>   Služba převodu bankovních dat může omezit počet řádků, které lze exportovat do jednoho souboru. Při překročení limitu se zobrazí chybová zpráva. Doporučuje se, aby soubory bankovních výpisů nepřekročily 1000 řádků, jelikož doba zpracování v bankovní službě převodu dat se může výrazně zvýšit.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Zaregistrování vaší společnosti na službu převodu bankovních dat
1. Zvolte pravém horním rohu zvolte ![Vyhledat stránku nebo sestavu ](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte <x2/> Nastavení bank. dat** a pak vyberte související odkaz.**  
2. **Převod konv. bankovních **Otevře se okno se třemi poli předvyplněnými odpovídajícími adresami URL poskytovatele služby pro převod bankovních dat.

    > [!NOTE]  
   >   V demonstrační databázi jsou pole Uživatelské jméno a Heslo předem vyplněny přihlašovacími informacemi, které nahradíte skutečnými informacemi vaší společnosti při přihlášení k službě převod bankovní dat.
3. V poli **Registrační adresa** vyberte tlačítko prohlížeče a otevřete přihlašovací stránku poskytovatele služeb.  
4. Na přihlašovací stránce poskytovatele služby bankovních dat zadejte uživatelské jméno a heslo pro předplatné vaší společnosti a dokončete přihlašovací proces podle pokynů poskytovatele služby.

    Vaše společnost je nyní zaregistrována pro službu převodu bankovních dat. Pokračujte v zadání uživatelského jména a hesla, které jste zadali do příslušných polí v nastavení v [!INCLUDE [d365fin](includes/d365fin_md.md)].
5. V **Nastavení služby konver. bank. dat** v poli **Uživatel Jméno** zadejte stejnou hodnotu, kterou jste zadali jako přihlašovací jméno na stránce poskytovatele služby v kroku 4.
6. V poli **Heslo** zadejte stejnou hodnotu, kterou jste zadali v poli **Heslo** na stránce poskytovatele služby v kroku 4.

## <a name="to-encrypt-your-login-information"></a>Šifrování přihlašovacích údajů
Doporučuje se chránit přihlašovací informace, které zadáváte v **Převod bankovních dat ** okně. Můžete šifrovat data na [!INCLUDE [d365fin](includes/d365fin_md.md)] serveru generováním nového nebo importováním existujícího šifrovacího klíče, který povolíte na instanci serveru [!INCLUDE [d365fin](includes/d365fin_md.md)]/>, který je připojen k databázi.

1. V **Nastavení služby konver. bank. dat** zvolte akci **Správa šifrování**.
2. V okně **Správa šifrování dat** povolte šifrování dat.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Zobrazení nebo aktualizace seznamu aktuálně podporovaných formátů bankovních dat
1. Zvolte pravém horním rohu zvolte ![Vyhledat stránku nebo sestavu ](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte <x2/> Nastavení služby konver. bank. dat** a pak vyberte související odkaz.**
2. V **Nastavení služby služby konver. bank. dat** zvolte akci Název banky - Seznam převodu dat k otevření seznamu názvů bank představujících formáty bankovních dat podporovaných službou převodu.****
3. Na stránce **Název banky - seznam převodu dat** vyberte akci **Aktualizovat seznam bankovních názvů**.

Seznam formátů bankovních dat, které jsou podporovány službou převodu bankovních dat je nyní aktualizován. Toto je seznam bankovních názvů filtrovaný podle země nebo oblasti, ze kterého můžete vybírat v poli **název banky-převod dat** v okně **karta bankovního účtu** .

> [!NOTE]  
>   Aktualizace podporovaných formátů bankovních dat nastane také, když vyberete nebo zadáte hodnotu do pole **Název banky - převod dat** na bankovním účtu.

Nyní jste se zaregistrovali na službu převodu bankovních dat. Postupujte podle přihlašovacích informací na každém bankovním účtu, který služba použije.

## <a name="see-also"></a>Viz také
[Nastavení bankovnictví](bank-setup-banking.md)  
[Správa bankovních účtů](bank-manage-bank-accounts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
