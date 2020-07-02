---
title: Using Business Central with Outlook| Microsoft Docs
description: This service has deep integration with Office 365 enabling you to manage all your business interactions and mail with customers and vendors directly in Outlook.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 08/14/2019
ms.author: edupont

---
# Použití aplikace Business Central jako schránka v aplikaci Outlook
[!INCLUDE[d365fin](includes/d365fin_md.md)] zavádí možnost spravovat obchodní interakce se zákazníky a dodavateli přímo v aplikaci Microsoft Outlook. S [!INCLUDE[d365fin](includes/d365fin_md.md)] doplňky aplikace Outlook můžete zobrazit finanční údaje týkající se zákazníků a dodavatelů a také vytvářet a odesílat finanční doklady, jako jsou nabídky a faktury.

## Získání doplňku
Je snadné začít s doplňkem [!INCLUDE[d365fin](includes/d365fin_md.md)] pro Outlook. V asistovaném nastavení **Nastavit vaši schránku v aplikaci Outlook**, můžete nastavit připojení pro sebe nebo pro vaši organizaci, pokud vaše organizace používá Office 365. Pokud budete vyzváni, jednoduše zadejte své uživatelské jméno a heslo pro Office 365 a sdělte nám, zda chcete obdržet ukázkovou e-mailovou zprávu. Doplněk [!INCLUDE[d365fin](includes/d365fin_md.md)] je automaticky přidán do aplikace Outlook. Pro více informací navštivte [Minimální požadavky pro aplikaci Outlook](product-requirements.md#outlook).

Po spuštění aplikace Outlook se pak zobrazí e-mailová zpráva od *Administrátor Dynamics 365 Business Central*. Nové doplňky jsou přidány do pásu karet aplikace Outlook a v prohlížeči můžete vidět doplňky [!INCLUDE[prodshort](includes/prodshort.md)] přímo nad nebo pod tělem e-mailové zprávy. Doplňky jsou pravidelně aktualizovány a budete upozorněni, že v aplikaci Outlook je pro vás připravena nová verze.

> [!TIP]
> Použíávate-li nový Outlook v prohlížeči, pak doplňky [!INCLUDE [prodshort](includes/prodshort.md)] budou skryty pod **Další akce**.

Některé společnosti používající Office 365 omezují oprávnění uživatelů k nasazení doplňků. Musíte se proto ujistit, že máte předplatné sady Office 365, které zahrnuje e-mail, a které vám umožní nasadit doplňky. Chcete-li přesto doplněk vyzkoušet, můžete [Vyzkoušet zdarma sadu Office 365](https://products.office.com/try).

## Použití doplňku Contact Insights
Řekněme, že dostanete e-mail od zákazníka, který chce získat nabídku na některé zboží. Přímo v aplikaci Outlook můžete otevřít doplněk [!INCLUDE[d365fin](includes/d365fin_md.md)], který rozpozná odesílatele jako zákazníka a otevírá zákaznickou kartu pro jeho společnost. Na tomto ovládacím panelu můžete vidět přehledné informace o zákazníkovi a podrobnější informace o konkrétních dokladech. Můžete také nahlédnout do historie prodeje pro zákazníka. Pokud se jedná o nový kontakt, můžete jej vytvořit jako nového zákazníka v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)] bez opuštění aplikace Outlook.

V doplňku můžete vytvořit prodejní nabídku a odeslat ji zpět tomuto zákazníkovi, aniž byste opustili aplikaci Outlook. Všechny informace, které potřebujete k odeslání nabídky, jsou k dispozici ve vaší schránce v aplikaci Outlook.
Po zadání dat můžete nabídku zaúčtovat. Potom ji můžete odeslat e-mailem. [!INCLUDE[d365fin](includes/d365fin_md.md)] vygeneruje  .PDF soubor s prodejní nabídkou a připojí jej k e-mailové zprávě, kterou v návrhu doplníte.

Podobně, pokud dostanete e-mail od dodavatele, můžete tento doplněk použít pro práci s dodavateli a nákupními fakturami.

Někdy chcete zobrazit více polí, než je v doplňku možné zobrazit, například když chcete vyplnit řádky faktury. Chcete-li mít více místa pro práci, můžete tento doplněk vložit na samostatnou stránku. Stále je součástí aplikace Outlook, ale máte více místa. Při zadávání dat ve vyskakovacím okně se změny automaticky ukládají. Po dokončení zadávání dat do dokladu můžete zvolit tlačítko **OK**. Výběrem rámce doplňku v aplikaci Outlook se automaticky obnoví dokument se změnami provedenými ve vyskakovacím zobrazení.

## Vytváření faktur z vašich schůzek
Některé firmy zaznamenávají všechny fakturovatelné schůzky v kalendáři aplikace Outlook. S [!INCLUDE[d365fin](includes/d365fin_md.md)] můžete vytvořit fakturu zákazníkovi přímo z položky kalendáře: Otevřete událost a pak můžete otevřít aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)], vyhledejte stávající informace nebo vytvořte fakturu nebo jiný prodejní doklad přímo na jedom místě.

## Rychlé vyhledání dokumentu
Doplněk [!INCLUDE[d365fin](includes/d365fin_md.md)] umožňuje rychlý přístup k dokumentům a dokladů uvedeným v e-mailových zprávách. Doplněk je k dispozici pro e-mailovou zprávu, pokud je v těle zprávy rozpoznáno číslo dokladu. Otevřením doplňku získáte rychlý přístup k dokladu.

Obdržíte-li například e-mailovou zprávu, která zmiňuje text *S-QUO100* , [!INCLUDE[d365fin](includes/d365fin_md.md)] ji označuje jako prodejní nabídku, takže můžete tento doklad otevřít v aplikaci Outlook. V aplikaci Outlook vyberte tlačítko **Odkazy na doklady** bezprostředně nad tělem e-mailové zprávy. V aplikaci Outlook Web App zvolte text *S-QUO1001* v těle e-mailové zprávy.

V doplňku Document Links můžete upravovat a provádět akce s dokladem, stejně jako v [!INCLUDE[d365fin](includes/d365fin_md.md)].

## Ruční přidání doplňků
V některých případech se doplňky do aplikace Outlook nepřidávají automaticky. I když jste vy nebo kolega spustili asistované průvodce instalací jménem společnosti, [!INCLUDE[d365fin](includes/d365fin_md.md)] nemusí být v aplikaci Outlook zobrazena. Pokud k tomuto problému dojde, můžete přidat doplňky [!INCLUDE[d365fin](includes/d365fin_md.md)] ručně.

Nejprve musíte ověřit, zda máte přístup k doplňkům ve svém účtu Office 365. Stačí jednoduše otevřít aplikaci Outlook v prohlížeči, otevřít zprávu, vybrat **Další akce** (...) v horní části zprávy a pak v dolní části seznamu zvolit možnost **Získat doplňky** . Otevře se stránka **Doplňky pro aplikaci Outlook**, kde můžete pro aplikaci Outlook povolit [!INCLUDE[prodshort](includes/prodshort.md)]. Poté, co přejdete zpět do aplikace Outlook, [!INCLUDE[prodshort](includes/prodshort.md)] by mělo být k dispozici.

Podobně v klientovi aplikace Outlook desktop můžete ověřit, zda [!INCLUDE[d365fin](includes/d365fin_md.md)] je uveden na stráce **Získat doplňky** .

V obou případech, pokud [!INCLUDE[d365fin](includes/d365fin_md.md)] stále není k dispozici, je nutné získat soubory manifestu doplňku. Další informace získáte od administrátora sady Office 365.

## Použití jiných e-mailových účtů

Doplňky jsou navrženy pro použití s ​​Office 365. Pokud používáte [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, váš správce bude vědět, zda můžete v aplikaci Outlook použít doplňky [!INCLUDE [prodshort](includes/prodshort.md)]. Pro více informací běžte na [Jakou e-mailovou adresu mohu použít v [!INCLUDE[prodshort](includes/prodshort.md)]?](across-faq.md#what-email-address-can-i-use-with-) a [Funkce, které vyžadují specifické okolnosti](/dynamics365/business-central/dev-itpro/features-not-implemented-on-premises#features-that-require-specific-circumstances).

## Viz také

[Začínáme](product-get-started.md)  
[Získání Business Cental na mobilní zařízení](install-mobile-app.md)  
[Odesílání dokladů e-mailem](ui-how-send-documents-email.md)  
[Finance](finance.md)  
[Prodej](sales-manage-sales.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Minimální požadavky pro aplikaci Outlook](product-requirements.md#outlook)  
[používání doplňků ve webové aplikaci Outlook](https://support.office.com/en-us/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)
