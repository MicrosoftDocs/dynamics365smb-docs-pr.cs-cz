---
title: Set up email in Business Central | Microsoft Docs
description: Describes how to use the company's SMTP server to send and receive email messages within Business Central, or alternatively how to use the email server settings created with the Office 365 subscription.
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 12/17/2019
ms.author: sgroespe

---
# Nastavení e-mailu
Chcete-li odesílat a přijímat e-maily z [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte vyplnit pole na stránce Nastavení poštovního protokolu SMTP.

Místo ručního zadávání podrobností o serveru SMTP můžete použít funkci **Použít nastavení serveru pro Office 365** k získání informací z předplatného Office 365.

Můžete buď nastavit e-mail ručně, jak je popsáno níže, nebo můžete získat pomoc přes průvodce asistovaného nastavení **Nastavit e-mail.** Pro více infomací běžte na [Příprava na podnikání](ui-get-ready-business.md).

## Nastavení e-mailu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení poštovního protokolu SMTP** a vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Pokud používáte účet, který vyžaduje dvoufaktorové ověření, ak heslo, které zadáte do pole **Heslo** musí být stejné jako pro předplatné sady Office 365 a musí být typu **Heslo aplikace**. Pro více informací navštivte [Správa hesel aplikací pro dvoustupňové ověření](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Můžete také vybrat akci **Použít nastavení serveru pro Office 365** a vložit jakékoli informace, které jsou již definovány pro vaše předplatné sady Office 365.
4. Po správném vyplnění všech polí zvolte funkci **Test nastavení e-mailu**.
5. Po úspěšném testu zavřete stránku.

## Použití náhradní adresy odesílatele odchozích e-mailových zpráv
Všechny odchozí e-mailové zprávy z [!INCLUDE[d365fin](includes/d365fin_md.md)] použijí výchozí adresu pro účet, který jste zadali na stránce Nastavení poštovního protokolu SMTP, jak je popsáno výše. Můžete však použít možnosti **Odeslat jako** nebo **Odeslat jménem** na serveru Exchange ke změně adresy odesílatele u odchozích zpráv. [!INCLUDE[d365fin](includes/d365fin_md.md)] použije výchozí účet k ověření na serveru Exchange, ale buď nahradí adresu odesílatele adresou, kterou určíte, nebo ji změní jménem „jménem“.

Následuje příklad použití funkce Odeslat jako a Odeslat jménem: [!INCLUDE[d365fin](includes/d365fin_md.md)].:

* Při odesílání dokladů, jako jsou nákupní nebo prodejní objednávky dodavatelům a zákazníkům, můžete chtít, aby vypadaly, že pocházejí z adresy _noreply@yourcompanyname.com_.
* Když vaše workflow odešle žádost o schválení e-mailem pomocí e-mailové adresy žadatele.

> [!Note]
> Adresy odesílatelů můžete nahradit pouze jedním účtem. To znamená, že nemůžete mít jednu náhradní adresu pro nákupní procesy a jinou pro prodejní procesy.

### Nastavení náhradní adresy odesílatele pro všechny odchozí e-mailové zprávy
1. V **Centru pro správu Exchange** pro váš účet Office 365 najděte poštovní schránku, kterou chcete použít jako náhradní adresu a poté si adresu zkopírujte nebo poznamenejte. Pokud potřebujete novou adresu, přejděte do Centra pro správu Microsoftu 365 a vytvořte nového uživatele a nastavte jeho poštovní schránku.
2. V [!INCLUDE[d365fin](includes/d365fin_md.md)] vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení poštovního protokolu SMTP**, a vyberte související odkaz.
3. V polie **Odeslat jako** vložte náhradní adresu.
4. Zkopírujte nebo poznamenejte adresu do pole **ID uživatele**.
5. V **Centru pro správu Exchange** najděte poštovní schránku, kterou chcete použít jako náhradní adresu, a zadejte adresu z pole **ID uživatele** do pole **Odeslat  jako**. Pro více informací navštivte [Použití EAC pro přiřazení práv k individuálním poštovním chránkám](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### Použití náhradní adresy v schvalovacím workflow
1. V [!INCLUDE[d365fin](includes/d365fin_md.md)] vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení poštovního protokolu SMTP**, a vyberte související odkaz.
2. Zkopírujte nebo poznamenejte adresu do pole **ID uživatele**.
3. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Nastavení uživatelů schvalování** a poté vyberte související odkaz.
4. V **Centru pro správu Exchange**, vyhledejte poštovní schránky pro každého uživatele uvedeného na stránce **Nastavení uživatelů schvalování** a v poli **Odeslat jako** vložte emalovou adresu z pole **ID uživatele** z **Nastavení poštovního protokolu SMTP** v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro více informací navštivte [Správa práv pro příjemce](/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. V [!INCLUDE[d365fin](includes/d365fin_md.md)] vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení poštovního protokolu SMTP**, a vyberte související odkaz.
6. Chcete-li povolit nahrazení, zapněte políčko **Povolit nahrazení odesílatele**.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] určí, která adresa se má zobrazit v následujícím pořadí: <br><br> 1. Adresa určená v poli  **E-Mail** na stránce **Nastavení uživatelů schvalování** pro zprávy z workflow. <br> 2. Adresa určená v poli  **Odeslat jako** na stránce **Nastavení poštovního protokolu SMTP** . <br> 3. Adresa určená v poli  **ID uživatele** na stránce **Nastavení poštovního protokolu SMTP**.


## Viz také

[Sdílené poštovní schránky ve službě Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Nastavení [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Odesílání dokladů](ui-how-send-documents-email.md)  
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] pomocí rozšíření](ui-extensions.md)  
[Použití [!INCLUDE[d365fin](includes/d365fin_md.md)] jako vaší obchodní schránky v outlooku](admin-outlook.md)  
[Získání [!INCLUDE[d365fin](includes/d365fin_md.md)] aplikace pro moje chytré zařízení](install-mobile-app.md)
