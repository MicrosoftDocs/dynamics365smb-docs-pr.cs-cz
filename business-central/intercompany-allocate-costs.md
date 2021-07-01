---
title: Allocate Costs to Intercompany Partners| Microsoft Docs
description: Learn how VAT settings for customers and vendors control whether, and how, VAT is calculated.
services: project-madeira
documentationcenter: ''
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: bholtorf

---
# Přidělení nákladů mezipodnikových partnerům
Při použití vnitropodnikového účtování pro přenos dokladů mezi partnerskými společnostmi ovlivňují nastavení týkající se DPH (především DPH účto skupina) přiřazená k účtům zákazníka nebo dodavatele (souvisejícím s vnitropodnikovým partnerem), zda a jak DPH registrováno a vypočítáno.
Můžete také provádět distribuci nákladů přímo z objednávky partnerským společnostem. Pokud například zaevidujete nákupní fakturu od externího dodavatele a chcete distribuovat některé nebo všechny náklady jednomu nebo více mezipodnikových partnerům.

Náklady můžete přidělit jednomu nebo více mezipodnikových partnerů pomocí následujících možností:

* **Vnitropodnikové finanční deníky** - tyto deníky jsou užitečné při nákupu služby. Například když si mateřská společnost najme službu pro nastavení počítačových systémů ve dvou dceřiných společnostech. Faktura je odeslána mateřské společnosti, ale náklady jsou přiděleny mezipodnikovým partnerům. Další informace naleznete v tématu [Práce s mezipodnikovým doklady a deníky](intercompany-how-work-documents-journals.md).
* Nákupní objednávky a faktury - Použití nákupních dokladů je užitečné, pokud jsou nákupní funkce například provozních nákladů centralizovány v jedné společnosti a poté přiděleny mezipodnikových partnerům.

## Přidělení nákladů pomocí vnitropodnikových finančních deníků
To enter a  line in an intercompany general journal, follow these steps.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vnitropodnikové finanční deníky** a poté vyberte související odkaz.
2. V případě potřeby zadejte do pole **Číslo externího dokladu** číslo dokladu faktury od dodavatele.
3. V poli **Typ dokladu** vyberte **Faktura**.
4. V poli **Typ účtu** vyberte **Dodavatel**.
5. V poli **Číslo účtu** vyberte dodavatele.
6. V poli **Částka** zadejte zápornou částku rovnající se částce na faktuře.
7. V poli **Číslo protiúčtu** a vyberte **Účet**.
8. V poli **Číslo protiúčtu** vyberte vyrovnávací účet, který chcete použít.
9. Chcete-li přidělit náklady vnitropodnikovým partnerům, postupujte takto:
   1. Vytvořte nový řádek.
   2. V poli **Typ dokladu** zvolte možnost, která ponechá pole prázdné.
   3. V poli **Číslo dokladu**  zadejte číslo, které se liší od čísla v poli **Číslo externího dokladu**. Alokace nákladů je považována za jinou transakci.
   4. V poli **Typ účtu** zvolte **Vnitropodnik. partner**.
   5. V poli **Číslo účtu** vyberte vnitropodnikového partnera, ke kterému chcete přiřadit náklady.
   6. V poli **Typ protiúčtu** vyberte **Účet**.
   7. V poli **Číslo protiúčtu** vyberte účet, na který chcete zaúčtovat částku, kterou obdržíte od vnitropodnikového partnera.
   1. V poli **Částka** zadejte částku faktury, která má být přidělena vnitropodnikovému partnerovi.
   1. V poli **Číslo finančního účtu vnitropodnikového partnera** vyberte účet, na který chcete zaúčtovat částku pro vnitropodnikového partnera.
   1. Podle potřeby vyplňte zbývající pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Opakujte tyto kroky pro každého vnitropodnikového partnera, který by se měl podílet na nákladech.
1. Chcete-li dokument zaúčtovat a přidělit náklady, zvolte **Účtovat**.

## Rozdělení nákladů pomocí nákupního dokladu
Následující postup popisuje, jak přidělit náklady pomocí nákupní faktury. Kroky jsou stejné i pro nákupní objednávky.

> [!NOTE]
> Chcete-li tyto kroky provést, musíte personalizovat stránku **Nákupní faktura** přidáním polí **Kód vnitropodnikového partnera**, **Typ odkazu na vnitropod. partnera** a **Vnitropodnikový partner**. Další informace naleznete v tématu [Přizpůsobení stránky pomocí pásu Přizpůsobení](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

1. Vyberte ![Žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete delat"), zadejte **Nákupní faktury**a pak zvolte související odkaz.
2. V poli **Typ** vyberte **Účet**.

   Finanční účet je jediná možnost, kterou můžete použít k přidělení nákladů.
1. V poli **Číslo** vyberte účet, na který chcete účtovat.
1. Do pole **Kód vnitropodnikového partnera**vyberte vnitropodnikového partnera, ke kterému chcete přiřadit náklady.
1. Do pole **Typ odkazu na vnitropod. partnera** vyberte účet, který chcete použít pro přidělení. This account will map the expense to an account in the intercomany partner's chart of accounts.
1. In the **Quantity** field, specify the number of units to charge to the intercompany partner.
1. In the **Direct Unit Cost Excl. VAT (or Incl. VAT)** field, enter the cost per item to charge to the intercompany partner.
1. Podle potřeby vyplňte zbývající pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. To post the purchase order, choose **Post**.

## To send the allocated costs to intercompany partners
1. Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **IC Outbox Transactions**, and then choose the related link.
2. Choose lines to send, and then choose the **Send to IC Partner** action.
3. To allocate the costs, choose the **Complete Line Actions** action.

## Calculating VAT for Cost Distributions
When you use a document to distribute costs to intercompany partners, there are two VAT settings to be aware of:
* The settings on the G/L account for expenses:
   * If the general business or VAT business posting groups are set up on the G/L account, then the calculation depends on the groups and the product groups from the document line.
   * If the general business or VAT business posting groups are not specified on the G/L account, the calculation depends on the following:
* The posting group settings on the intercompany partner
   * Whether the intercompany partner is assigned to a customer number that does not have a general business or VAT business posting groups specified.
   * There is no customer number associated with the intercompany partner. Then the general business or VAT business posting groups are blank, and the line in the VAT posting setup is used, which is usually a group where 0% VAT is specified.

> [!NOTE]
> It is important to validate both the intercompany partner setup and the G/L account setup (for the expense account used for the cost distribution) before you allocate costs to intercompany partners.

## Viz také
[Set Up Intercompany](intercompany-how-setup.md)  
[Managing Intercompany Transactions](intercompany-manage.md)  
[Finance](finance.md)  
[Setting Up Finance](finance-setup-finance.md)  
[Working with General Journals](ui-work-general-journals.md)  
[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]