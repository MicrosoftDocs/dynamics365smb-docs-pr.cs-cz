---
title: Set Up Prepayments
description: Learn how to configure Business Central so that you can use prepayments to invoice and collect deposits from customers and remit deposits to vendors.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keyword: prepayment
ms.search.form: 314, 459, 460, 664
ms.date: 10/27/2021
ms.author: edupont

---
# Nastavení záloh

Pokud požadujete, aby vaši zákazníci odeslali platbu před odesláním objednávky, nebo pokud váš dodavatel vyžaduje, abyste platbu odešleli před odesláním objednávky, můžete použít funkci Záloha. Funkce záloh umožňuje fakturovat a vybírat vklady požadované od zákazníků nebo převádět vklady dodavatelům, aby bylo zajištěno, že všechny dílčí platby budou zaúčtovány na fakturu. Pro více informací navštivte [Vytvoření zálohové faktury](finance-how-to-create-prepayment-invoices.md).

Před zaúčtováním zálohových faktur musíte nastavit účty v hlavní knize a nastavit číselné řady pro zálohové doklady. Je nutné zadat účet pro zálohy související s prodejem a účet pro zálohy související s nákupem. Můžete určit stejné účtovací účty, které se použijí pro všechny platby spojené se všemi obecnými obchodními účto skupinami nebo obecnými skupinami účtování produktů, nebo můžete určit konkrétní účty pro konkrétní účto skupiny pro prodej a nákup. To závisí na požadavcích vaší společnosti na sledování záloh.

Můžete definovat procento částky řádku, která bude fakturována za zálohu pro zákazníka nebo dodavatele, pro všechno zboží nebo vybrané zboží. Po dokončení nastavení můžete vygenerovat zálohové faktury z prodejních a nákupních objednávek. Můžete použít výchozí procenta pro každý prodejní nebo nákupní řádek nebo můžete podle potřeby změnit částky na faktuře. Můžete například určit celkovou částku za celou objednávku.

> [!NOTE]
> Doporučujeme nepoužívat procento zálohy ve výši 100 % v následujících případech:
>
> * Pokud se nacházíte v Severní Americe. Vzhledem k tomu, jak se daně počítají, může procento zálohy ve výši 100 % vést k problémům s fakturami za platbu předem.
> * Ve všech oblastech, pokud ručně odečtete skonto z faktury. Procento zálohy ve výši 100 % automaticky nezanechá částku, ze které lze slevu odečíst.

Vzhledem k tomu, že předplacená částka patří kupujícímu, dokud neobdržel zboží nebo služby, je nutné nastavit účty hlavní knihy, aby se částky zálohy zadržovaly, dokud nebude zaúčtována konečná faktura. Platby za prodej musí být zaznamenány na účtu závazků, dokud nebudou položky odeslány. Zálohy na nákup musí být zaznamenány na účtu majetku, dokud není zboží přijato. Kromě toho je nutné pro každý identifikátor DPH nastavit samostatný účet hlavní knihy.

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## Přidání účtů záloh k obecnému nastavení účtování

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení obecného účtování** a poté vyberte související odkaz.
2. Na stránce **Nastavení obecného účtování** vyplňte pro příslušné řádky následující pole:

   * **Účet záloh výnosů**
   * **Nákupní  účet záloh**

> [!TIP]
> Pokud pole na stránce **General Posting Setup** page, then use the horizontal scroll bar at the bottom of the page to scroll to the right.

Pokud jste ještě nenastavili účty hlavní knihy pro platby záloh, můžete v příslušném poli účtu otevřít stránku **Přehled účtů**.

## Nastavení číselných řad pro doklady záloh

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení prodeje a pohledávek** a poté vyberte související odkaz.
2. Na stránce **Nastavení prodeje a pohledávek** na záložce **Číselné řady** vyplňte následující pole:

   * **Čísla účtovaných  zál.  faktur**
   * **Čísla účtovaných  zál.  dobropisů**

3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení nákupu a závazků** a vyberte související odkaz.
4. Na stránce **Nastavení nákupu a závazků** na záložce **Číselné řady** vyplňte následující pole:

   * **Čísla účtovaných  zál.  faktur**
   * **Čísla účtovaných  zál.  dobropisů**

> [!NOTE]  
> Stejnou číselnou řadu můžete použít pro zálohové faktury a běžné faktury, nebo můžete použít různé číselné řady. Pokud používáte různé řady, nesmí se překrývat, protože v obou řadách nesmí existovat stejná čísla.

## Nastavení procent záloh pro zboží, zákazníky a dodavatele

Pro zboží můžete nastavit výchozí procento zálohy pro všechny zákazníky, konkrétního zákazníka nebo cenovou skupinu zákazníka. Pokud nechcete použít stejné procento zálohy na všechny zákazníky, musíte určit, na které zákazníky nebo které cenové skupiny zákazníků se procento zálohy vztahuje.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte zboží a pak zvolte akci **Procentní části zálohy**.
3. Na stránce **Procentní části prodejní zálohy** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Pro zákazníka nebo dodavatele můžete nastavit jedno výchozí procento zálohy pro všechny zboží a všechny typy prodejních řádků. Toto zadáte na kartě zákazníka nebo dodavatele. Následující postup ukazuje, jak určit procento zálohy pro zákazníka, ale podobné kroky platí i pro dodavatele.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Otevřete kartu pro zákazníka.
3. Vyplňte pole **Záloha v %**.
4. Opakujte kroky pro ostatní zákazníky nebo pro dodavatele.

> [!TIP]
> Na stránku **Procentní části prodejní zálohy** se můžete dostat také z karty zákazníka nebo dodavatele.

### Určení, které procento zálohy má první prioritu

Objednávka může mít procento zálohy v prodejní hlavičce a jiné procento pro zboží na řádcích. Chcete-li určit, které procento zálohy se vztahuje na každý řádek prodeje, systém vyhledá procento zálohy v následujícím pořadí a použije první výchozí hodnotu, kterou najde:

1. Procento zálohy za zboží na řádku a na kartě zákazníka, pro kterého je objednávka určena.
2. Procento zálohy pro zboží na řádku a cenovou skupinu zákazníka, do které zákazník patří.
3. Procento zálohy pro zboží na řádku pro všechny zákazníky.
4. Procento zálohy v prodejní nebo nákupní hlavičce.

Jinými slovy, procento zálohy na kartě zákazníka se použije pouze v případě, že pro zboží není nastaveno procento zálohy. Pokud však po vytvoření řádků změníte obsah pole **Procento zálohy** v prodejní nebo nákupní hlavičce, bude procento zálohy na všech řádcích aktualizováno. To usnadňuje vytvoření objednávky s pevným procentem zálohy bez ohledu na procento nastavené na kartě zboží.

## Viz také

[Fakturace záloh](finance-invoice-prepayments.md)    
[Návod: Nastavení a fakturace prodejních záloh](walkthrough-setting-up-and-invoicing-sales-prepayments.md)    
[Výpočet daně ze zboží a služeb při platbách záloh](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)    
[Znalost o hlavní knize a certifikátu pravosti](finance-general-ledger.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
