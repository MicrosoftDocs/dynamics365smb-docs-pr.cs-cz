---
title: Způsoby řešení problémů při samoobslužné registraci | Microsoft Docs
description: 'Naučte se o nejčastějších důvodech, proč nelze dokončit registraci do Business Central, a o způsobech, jakými tyto problémy vyřešit.'
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: edupont
---
# <a name="troubleshooting-self-service-sign-up"></a>Řešení problémů při samoobslužné registraci.
Registrace do [!INCLUDE[d365fin](includes/d365fin_md.md)] je jednoduchá a lze ji provést velmi rychle. Můžete si vytvořit účet zdarma, i když jste již existující organizací. Tento článek se zabývá problémy, které se mohou vyskytnout během registrace.

## <a name="what-email-address-can-i-use-with-business-central"></a>Jakou e-mailovou adresu mohu použít v Business Central?
[!INCLUDE[d365fin](includes/d365fin_md.md)] vyžaduje, abyste k registraci použili e-mailovou adresu práce nebo školy. [!INCLUDE[d365fin](includes/d365fin_md.md)] nepodporuje e-mailové adresy poskytované spotřebitelskými e-mailovými službami nebo poskytovateli telekomunikačních služeb. To zahrnuje outlook.com, hotmail.com, gmail.com a další.

Pokud se pokusíte zaregistrovat pomocí své osobní e-mailové adresy, zobrazí se zpráva, že bude třeba použít pracovní nebo školní e-mailovou adresu.

## <a name="troubleshooting"></a>Odstraňování problémů
V mnoha případech lze registraci do [!INCLUDE[d365fin](includes/d365fin_md.md)] provést řízením se dle následujícího procesu registrace. Existuje však několik důvodů, proč nemusí být možné samostatnou registraci dokončit. Níže uvedená tabulka shrnuje některé nejčastější důvody, proč není možné registraci dokončit, a způsoby, jakými tyto problémy vyřešit.

| Příznak / Chybová zpráva | Příčina a Řešení |
| --- | --- |
| U e-mailových adres Office 365, které nejsou registrovány v podporované zemi, se během registrace zobrazí následující zpráva:<br /><br />**To nefungovalo, zatím nepodporujeme vaši zemi nebo region.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] v současné době podporuje pouze e-mailové účty Office 365, které jsou registrovány na omezeném počtu trhů. Pro více informací navštivte [Oblastní dostupnost](#regional-availability) |
| Osobní e-mailové adresy, jako například nancy@gmail.com, nejsou podporovány. Během registrace se zobrazí následující zpráva:<br /><br />**Zadali jste osobní e-mailovou adresu: Zadejte prosím svou pracovní e-mailovou adresu, abychom mohli bezpečně ukládat data vaší společnosti.**<br> nebo <br> **To vypadá jako osobní e-mailová adresa. Zadejte svou pracovní adresu, abychom vás mohli spojit s ostatními ve vaší společnosti. A nebojte se. S nikým vaši adresu sdílet nebudeme.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] nepodporuje e-mailové adresy poskytované spotřebitelskými e-mailovými službami nebo poskytovateli telekomunikačních služeb. Pro dokončení registrace zkuste použít e-mailovou adresu přiřazenou vaší prací nebo školou. Pokud se stále nemůžete zaregistrovat a jste ochotni dokončit pokročilejší proces nastavení, můžete si zaregistrovat nové zkušební předplatné sady Office 365 a pomocí této e-mailové adresy se zaregistrovat. |
| E-mailové adresy .gov nebo .mil Během registrace se zobrazí následující zpráva:<br /><br />**[!INCLUDE[d365fin](includes/d365fin_md.md)] nedostupné: [!INCLUDE[d365fin](includes/d365fin_md.md)] není v současné době k dispozici uživatelům s e-mailovými adresami .gov nebo .mil. Použijte jinou pracovní e-mailovou adresu nebo to zkuste později.** <br>nebo <br>**Nemůžeme dokončit vaši registraci. Vypadá to, že [!INCLUDE[d365fin](includes/d365fin_md.md)] pro vaši práci nebo školu momentálně není k dispozici.** |[!INCLUDE[d365fin](includes/d365fin_md.md)] v současné době nepodporuje adresy .gov nebo .mil. |
| Samostatná registrace není povolena. Během registrace se zobrazí následující zpráva:<br /><br />**Nemůžeme dokončit vaši registraci. Vaše IT oddělení vypnulo registraci do [!INCLUDE[d365fin](includes/d365fin_md.md)]. Chcete-li dokončit registraci, kontaktujte je.** <br>nebo <br> **To vypadá jako osobní e-mailová adresa. Zadejte svou pracovní adresu, abychom vás mohli spojit s ostatními ve vaší společnosti. A nebojte se. S nikým vaši adresu sdílet nebudeme.** |IT správce vaší organizace zakázal samostatnou registraci pro [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro dokončení registrace se obraťte na správce IT a požádejte jej, aby postupoval podle pokynů na níže uvedené stránce a umožnil stávajícím uživatelům registrovat se do [!INCLUDE[d365fin](includes/d365fin_md.md)] a umožnil novým uživatelům připojit se ke stávajícímu klientovi. Tento problém může také nastat, pokud jste se zaregistrovali do Office 365 prostřednictvím partnera. |
| E-mailová adresa není ID Office 365. Během registrace se zobrazí následující zpráva:<br /><br />**Nemůžeme vás najít na contoso.com. Používáte v práci nebo ve škole jinou ID ? Zkuste se přihlásit pomocí ní a pokud to nepomůže, obraťte se na IT oddělení.** |ID používané vaší organizací k přihlášení do Office 365 a dalších služeb společnosti Microsoft se liší od vaší e-mailové adresy. Například vaše e-mailová adresa může být Nancy.Smith@contoso.com, ale vaše ID je nancys@contoso.com. Chcete-li dokončit registraci, použijte ID, kterou vaše organizace přiřadila k přihlášení do Office 365 nebo jiných služeb společnosti Microsoft. Pokud neznáte svou ID, obraťte se na svého IT správce. Pokud se stále nemůžete zaregistrovat a jste ochotni dokončit pokročilejší proces nastavení, můžete si zaregistrovat nové zkušební předplatné sady Office 365 a pomocí této e-mailové adresy se zaregistrovat. |
| Pokud je váš účet Office 365 registrován v podporované zemi a vy se přihlašujete do [!INCLUDE[d365fin](includes/d365fin_md.md)], zatímco jste v jiné zemi, obdržíte při registraci následující zprávu:<br /><br />**To nefungovalo, zatím nepodporujeme vaši zemi nebo region.**| Předplatné sady Office 365 vaší organizace je zaregistrováno v konkrétní zemi na administrativním portálu Office 365. Registrace do [!INCLUDE[d365fin](includes/d365fin_md.md)] používá jazyk a národní prostředí, které používá váš aktuální prohlížeč, a výsledkem je, že se vám může zobrazit chybová zpráva, i když se nacházíte v podporované zemi. Požádejte svého IT správce o ověření země, která je uvedena v profilu organizace na [Administrativním portálu Office 365](https://portal.office.com/adminportal/home#/companyprofile). Možná budete muset použít jiný účet pro [!INCLUDE[d365fin](includes/d365fin_md.md)].|

## <a name="regional-availability"></a>Oblastní dostupnost
Pro seznam aktuálně podporovaných trhů navštivte [Mezinárodní dostupnost balíčku Microsoft Dynamics](https://docs.microsoft.com/en-us/dynamics365/get-started/availability) a vstupní stránku sekce [Místní funkcionalita](about-localization.md).

<!-- [!INCLUDE[d365fin](includes/d365fin_md.md)] is currently available in the following markets:

| Europe | North America |
| --- | --- |
| Australia | Canada |
| Austria | |
| Belgium | United States |
| Denmark | |
| Germany | |
| Finland | |
| France | |
| Italy | |
| Netherlands | |
| New Zealand | |
| Spain | |
| Sweden | |
| Switzerland | |
| United Kingdom | |
-->

## <a name="see-also"></a>Viz také
[Vítejte v [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](index.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Místní funkcionality](about-localization.md)  
