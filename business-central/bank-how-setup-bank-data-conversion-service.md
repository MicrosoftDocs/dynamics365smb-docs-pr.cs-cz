---
title: Nastavení převodu Bankovních dat | Microsoft Docs
description: 'Můžete nastavit bankovní účty, abyste mohli sledovat transakce a importovat nebo exportovat bankovní zdroje, jako je například Yodlee.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Yodlee, feed, stream, data exchange, AMC, bank file import, bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer'
ms.date: 10/02/2018
ms.author: sgroespe
---
# <a name="set-up-the-bank-data-conversion-service"></a>Nastavení služby převodu bankovních dat
Globální poskytovatel služeb, který převádí informace o platbách do libovolného formátu dat, který banka vyžaduje, je připojen a připraven k zapnutí v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tento postup se označuje v [!INCLUDE[d365fin](includes/d365fin_md.md)] jako služba pro převod bankovních dat.

Platební řádky můžete exportovat ze stránky **Platební deník** do souboru nebo datového toku, který pak nahrajete do své banky pro automatické zpracování, takže nemusíte provádět elektronické platby jednotlivě. Další informace naleznete v části [Export plateb do Bankovních dokladů](payables-how-export-payments-bank-file.md).

Soubory bankovních výpisů můžete importovat na stránku **deník odsouhlasení plateb** pomocí služby pro převod bankovních dat a převést soubor, který obdržíte z banky, do datového formátu, který je [!INCLUDE[d365fin](includes/d365fin_md.md)] schopen importovat. Další informace naleznete v části [Automatické vyrovnání plateb a odsouhlasení bankovních účtů](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Jako alternativu k importu bankovních výpisů pomocí služby převodu bankovních údajů můžete použít službu Envestnet Yodlee Bank Feeds. Pro více informací běžte na [Nastavení Envestnet  yodlee Bank služby](bank-how-setup-bank-statement-service.md).

Chcete-li importovat nebo exportovat bankovní soubory, musíte si nastavit vlastní bankovní účet a bankovní účty svých dodavatelů. Další informace naleznete v části [Nastavení bankovních účtů](bank-how-setup-bank-accounts.md).

> [!NOTE]  
> Služba převodu bankovních dat může omezit počet řádků, které lze exportovat do jednoho souboru. Při překročení limitu se zobrazí chybová zpráva. Doporučuje se, aby soubory bankovních výpisů nepřekročily 1000 řádků, jelikož doba zpracování v bankovní službě převodu dat se může výrazně zvýšit.

## <a name="to-sign-your-company-up-for-the-bank-data-conversion-service"></a>Zaregistrování vaší společnosti na službu převodu bankovních dat
1. Zvolte ![,žárovku, která otevře funkci Tell Me](media/ui-search/search_small.png "co chcete udělat"), zadejte **Služba konv.bank. dat** a pak vyberte související odkaz.  
2. **Převod konv. bankovních dat** se třemi políčky předem vyplněnými příslušnými adresami URL poskytovatele služby převodu bankovních dat.

    > [!NOTE]  
    >   V demonstrační databázi jsou pole Uživatelské jméno a Heslo předem vyplněny přihlašovacími informacemi, které nahradíte skutečnými informacemi vaší společnosti při přihlášení k službě převod bankovní dat.
3. V poli **Registrační adresa** vyberte tlačítko prohlížeče a otevřete přihlašovací stránku poskytovatele služeb.  
4. Na přihlašovací stránce poskytovatele služby bankovních dat zadejte uživatelské jméno a heslo pro předplatné vaší společnosti a dokončete přihlašovací proces podle pokynů poskytovatele služby.

    Vaše společnost je nyní zaregistrována pro službu převodu bankovních dat. Pokračujte v zadání uživatelského jména a hesla, které jste zadali do příslušných polí v nastavení v [!INCLUDE[d365fin](includes/d365fin_md.md)].

5. Na stránce **Nastavení Konverze bankovních dat** v poli **Uživatel** Jméno zadejte stejnou hodnotu, kterou jste zadali jako přihlašovací jméno na stránce poskytovatele služby v kroku 4.
6. V poli **Heslo** zadejte stejnou hodnotu, kterou jste zadali v poli **Heslo** na stránce poskytovatele služby v kroku 4.

> [!NOTE]  
> Vaše přihlašovací údaje jsou automaticky šifrovány.

## <a name="to-view-or-update-the-list-of-currently-supported-bank-data-formats"></a>Zobrazení nebo aktualizace seznamu aktuálně podporovaných formátů bankovních dat
1. Zvolte ![,žárovku, která otevře funkci Tell Me](media/ui-search/search_small.png "co chcete udělat"), zadejte **Služba konv. služby konver. bank. dat** a pak vyberte související odkaz.
2. Na stránce **Nastavení Konverze bankovních dat** , zvolte akci **Název banky - Přehled převodu dat** a otevřete seznam názvů bank představujících formáty bankovních dat podporované službou převodu.
3. Na stránce **Název banky - seznam převodu dat** vyberte akci **Aktualizovat seznam bankovních názvů**.

Seznam formátů bankovních dat, které jsou podporovány službou převodu bankovních dat je nyní aktualizován. Toto je seznam bankovních názvů filtrovaný podle země nebo oblasti, ze kterého můžete vybírat v poli **název banky-převod dat** na stránce **Karta bankovního účtu** .

> [!NOTE]  
>   Aktualizace podporovaných formátů bankovních dat nastane také, když vyberete nebo zadáte hodnotu do pole **Název banky - převod dat** na bankovním účtu.

Nyní jste se zaregistrovali na službu převodu bankovních dat. Postupujte podle přihlašovacích informací na každém bankovním účtu, který služba použije.

## <a name="see-also"></a>Viz také
[Nastavení bankovnictví](bank-setup-banking.md)  
[Správa bankovních účtů](bank-manage-bank-accounts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
