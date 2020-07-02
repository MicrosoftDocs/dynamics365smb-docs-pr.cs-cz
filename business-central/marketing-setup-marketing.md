---
title: Set Up Marketing and Contact Management Information| Microsoft Docs
description: You can set up marketing and contact management in Business Central to optimize relationships with prospects or customers, and improve campaigns and promotions.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 04/01/2020
ms.author: sgroespe

---
# Nastavení správy vztahů
Než začnete pracovat se svými kontakty a zájmy marketingu, měli byste provést několik rozhodnutí a kroků, abyste nastavili, jak marketingová oblast spravuje určité aspekty vašich kontaktů. Můžete se například rozhodnout, zda chcete synchronizovat kartu kontaktu s kartou zákazníka, kartou dodavatele a kartou bankovního účtu, jak jsou definovány číselné řady nebo jaké by mělo být standardní oslovení při zápisu do kontaktů.

Správa kontaktů a strategie pro identifikaci, přilákání a udržení zákazníků pomůže optimalizovat vaše podnikání a zvýšit spokojenost zákazníků. Použití dobrého systému správy kontaktů vám také pomůže vytvořit a udržovat vztahy se zákazníky. Komunikace je klíčem k těmto vztahům. Schopnost přizpůsobit komunikaci s potenciálními i stávajícími zákazníky, prodejci a obchodními partnery podle jejich potřeb je nezbytná pro úspěch společností. Vytvoření strategie a definování způsobu, jakým vaše společnost používá kontaktní informace, je primárním krokem. Tyto informace si bude prohlížet mnoho různých skupin ve vaší společnosti, takže mít správně zavedený systém pomůže všem k vyšší produktivitě.

Nastavení marketingu a kontaktů nastavíte na stránce **Nastavení marketingu**. Chcete-li otevřít stránku **Nastavení marketingu**, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení marketingu** a poté vyberte související odkaz.

## Automatické kopírování konkrétních informací z kontaktů typu společnost kontaktům typu osoba
Některé informace o kontaktech typu společnost jsou totožné s informacemi o kontaktech typu osoba, které v těchto společnostech pracují, například informace o adrese. V části **Dědičnost** na stránce **Nastavení marketingu** můžete nastavit, aby aplikace automaticky kopírovala určitá pole z karty kontaktu pro společnost na kartu kontaktu por osoby při každém vytvoření kontaktní osoby pro kontaktní společnost. Můžete například vybrat, zda chcete zkopírovat kód prodejce, adresu (adresa, adresa 2, město, poštovní směrovací číslo a kraj), podrobnosti komunikace (faxové číslo, zpětná odpověď na telex a telefonní číslo) a další.

Pokud změníte jedno z těchto polí na kartě kontaktu pro společnost, aplikace automaticky upraví pole na kartě kontaktu pro osoby (pokud jste pole na kartě kontaktu pro osoby ručně nezměnili).

Pro více informací navštivte [Vytvoření kontaktů](marketing-create-contact-companies.md).

## Použití předdefinovaných výchozích hodnot u nových kontaktů
Můžete se rozhodnout, že aplikace automaticky přiřadí konkrétní kód jazyka, kód oblasti, kód prodejce a kód země nebo oblasti jako výchozí pro každý nový kontakt, který vytvoříte. Můžete také zadat výchozí kód prodejního cyklu, který aplikace automaticky přiřadí každé nové příležitosti, kterou vytvoříte.

Dědičnost polí přepíše výchozí hodnoty, které jste nastavili. Pokud jste například nastavili angličtinu jako výchozí jazyk, ale jazykem kontaktní společnosti je němčina, aplikace automaticky přiřadí němčinu jako kód jazyka kontaktních osob zaznamenaných pro tuto společnost.

<!--You can also setup a default salutation that application automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, application will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## Automatické zaznamenávání interakcí
[!INCLUDE[d365fin](includes/d365fin_md.md)] může automaticky zaznamenávat prodejní a nákupní doklady jako interakce (například objednávky, faktury, příjemky atd.), stejně jako e-maily, telefonní hovory a průvodní stránky.

Pro více informací navštivte [Automatické zaznamenávání interakcí s kontakty](marketing-auto-record-interactions.md).

## Synchronizace kontaktů se zákazníky a další
Chcete-li synchronizovat kartu kontaktu s kartou zákazníka, kartou dodavatele a kartou bankovního účtu, musíte vybrat kód obchodního vztahu pro zákazníky, dodavatele a bankovní účty. Kontakt můžete například propojit s existujícím zákazníkem pouze v případě, že jste na stránce **Nastavení marketingu** vybrali kód obchodního vztahu pro zákazníky.

Pro více informací navštivte [Synchronizace kontaktů se zákazníky, dodavateli a bankovními účty].

## Přiřazení číselné řady kontaktům a příležitostem
Můžete nastavit číselnou řadu pro kontakty a příležitosti. Pokud jste pro kontakty nastavili číselnou řadu, při vytváření kontaktu a stisknutí klávesy Enter, aplikace automaticky zadá další dostupné číslo kontaktu v poli Číslo na kartě daného kontaktu.

Pro další informace o číselných řadách navštivte [Vytváření číselných řad](ui-create-number-series.md).

## Hledání duplicitních kontaktů při vytváření kontaktů
Můžete zvolit automatické vyhledávání duplicit aplikace při každém vytvoření kontaktu pro společnost, nebo můžete zvolit ruční vyhledávání po vytvoření kontaktů. Můžete si také zvolit, aby aplikace aktualizovala vyhledávací řetězce automaticky pokaždé, když změníte kontaktní informace nebo vytvoříte kontakt. Můžete zvolit procento zásahů vyhledávání, to znamená procento identických řetězců, které musí mít dva kontakty, aby je aplikace mohla považovat za duplikáty.

## Viz také
[Správa kontaktů](marketing-contacts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
