---
    title: How to Create Prepayment Invoices | Microsoft Docs
    description: Learn how to handle situations where you require prepayment, or your vendor does.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Vytvoření zálohové faktury
Pokud požadujete, aby vaši zákazníci před odesláním objednávky odeslali platbu, nebo pokud váš prodejce požaduje, abyste odeslali platbu před odesláním objednávky, můžete použít funkci zálohy.

Po vytvoření prodejní nebo nákupní objednávky můžete vytvořit zálohovou fakturu. Pro každý prodejní nebo nákupní řádek můžete použít výchozí procenta nebo můžete podle potřeby upravit částku. Můžete například zadat celkovou částku pro celou objednávku.

Následující postup popisuje, jak fakturovat zálohu z prodejní objednávky. Kroky jsou podobné pro nákupní objednávky.

## Vytvoření zálohové faktury
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté vyberte související odkaz.
2. Vytvořte novou prodejní objednávku. Pro více informací navštivte [Prodej produktů](sales-how-sell-products.md).

   Na záložce **Záloha** se pole **Záloha (%)** vyplní automaticky, pokud je na kartě zákazníka výchozí procento zálohy. Můžete změnit obsah pole. Procento zálohy je zkopírováno z hlavičky pouze na řádky, které nekopírují výchozí procento zálohy z položky.

   Pokud je vybráno pole **Slučovat zálohy**, budou řádky na faktuře sloučeny, pokud:
   - Mají stejný účet hlavní knihy pro zálohy, jak je stanoveno v obecném nastavení účtování.
   - Mají stejné dimenze.
   Pole ponechejte prázdné, pokud chcete zadat zálohovou fakturu s jedním řádkem pro každý řádek prodejní objednávky, který má procento zálohy.

3. Vyplňte prodejní řádky.

   Pokud byly pro vaše položky nastaveny výchozí procenta záloh, budou automaticky zkopírovány do pole **Záloha (%)** na řádku. V opačném případě je procentuální částka zálohy zkopírována z hlavičky. Na řádku můžete změnit obsah pole **Záloha (%)**.
4. Pokud chcete použít jedno procento zálohy na celou objednávku, změňte pole **Záloha (%)** v záhlaví po vyplnění řádků.
5. Chcete-li zobrazit celkovou částku zálohy, vyberte akci **Statistika**.

   Pokud chcete upravit celkovou částku zálohy pro objednávku, můžete změnit obsah pole **Částka zálohy** na stránce **Statistika prodejní objednávky**.

   Pokud je vybráno pole **Ceny včetně DPH** můžete pole **Částka zálohy včetně  DPH** upravovat.

   Pokud změníte obsah pole **Částka zálohy**, bude částka rozdělena proporcionálně mezi všechny řádky, s výjimkou těch, které mají **0** v poli **Záloha (%)**.
6. Chcete-li vytisknout zkušební zprávu před zaúčtováním zálohové faktury, vyberte akci **Záloha** a poté vyberte akci **Testovací sestava zálohy**.
7. Chcete-li zaúčtovat zálohovou fakturu, vyberte akci **Záloha** a poté vyberte akci **Zaúčtovat zálohovou fakturu**.

   Chcete-li zaúčtovat a vytisknout zálohovou fakturu, vyberte akci **Zaúčtovat a vytisknout zálohovou  fakturu**.

Pro objednávku můžete vystavit další zálohovou faktury. Chcete-li to provést, zvyšte částku zálohy na jednom nebo více řádcích, v případě potřeby upravte datum dokladu a zaúčtujte zálohovou fakturu. Pro rozdíl mezi dosud fakturovanými částkami zálohy a novou částkou zálohy bude vytvořena nová faktura.

> [!NOTE]
> Pokud se nacházíte v Severní Americe, nemůžete po zaúčtování faktury změnit procentní sazbu zálohy. Tomu je zabráněno v severoamerické verzi [!INCLUDE[d365fin](includes/d365fin_md.md)], protože výpočet daně z prodeje bude jinak nesprávný.

Pokud jste připraveni zaúčtovat zbývající částku faktury, zaúčtujte ji stejně jako jakoukoli jinou fakturu a částka zálohy bude automaticky odečtena z dlužné částky.

## Viz také
[Fakturace záloh](finance-invoice-prepayments.md)  
[Návod: Nastavení a fakturace prodejních záloh](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finance](finance.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
