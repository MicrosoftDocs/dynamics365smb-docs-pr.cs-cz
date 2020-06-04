---
title: Setting Up Suggested Field Values | Microsoft Docs
description: To avoid manual calculations and complete tasks quickly and accurately, you can set up automatic data entry so that Business Central fills in selected fields.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2019
ms.author: sgroespe

---
# Umožnění [!INCLUDE[d365fin](includes/d365fin_md.md)] navrhovat hodnoty
[!INCLUDE[d365fin](includes/d365fin_md.md)] může pomoci při provádění úloh rychleji a lépe, pokud předvyplňujete pole nebo dokončuje řádky, která byste jinak museli vypočítat a zadávat sami. Ačkoli je automatické zadávání dat vždy správné, můžete je později v případě potřeby změnit.

Funkce, které zadávají hodnoty polí, jsou obvykle nabízeny pro úkoly, do kterých zadáváte velké objemy transakčních dat a chcete předejít chybám a ušetřit čas. Toto téma obsahuje výběr takových funkcí. Další sekce budou přidány v příštích aktualizacích aplikace [!INCLUDE[d365fin](includes/d365fin_md.md)].

## Zaškrtávací políčko **Navrhnout vyrovnávací částku** na stránce **Listy finančního deníku**
Pokud například zadáváte řádky finančního deníku pro více výdajů, které musí být zaúčtovány na stejný bankovní účet, pak při každém zadání nového řádku deníku pro výdaj můžete mít pole **Částka** na řádku bankovního účtu automaticky aktualizováno na částku, která vyrovnává náklady. Další informace o práci s obecnými deníky naleznete v tématu [Práce s finančními deníky](ui-work-general-journals.md) .

### Automatické vyplnění pole **Částka** pro vyrovnávání řádků finančího deníku
1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Finanční deníky** související odkaz.
2. V řádku pro požadovaný list finančního deníku zvolte zaškrtávací pole **Navrhnout částku vyrovnání**.
3. Otevřete finanční deník a pokračujte v evidenci a zaúčtování transakcí pomocí popsané funkce pro automatické zadávání hodnoty pole.

Informace o nastavení dávky osobního finančního deníku, například pro zpracování výdajů, naleznete v tématu [Práce s finančními deníky](ui-work-general-journals.md) .

## Pole **Automaticky vyplnit datum přijetí** na stránce **Platební registrace**
Stránka **Registrace plateb** zobrazuje neuhrazené příchozí platby jako řádky, které představují prodejní doklady, kde je částka splatná k platbě. Další informace o vyrovnánvíní plateb zákazníků naleznete v části [Odsouhlasení plateb zákazníků ze seznamu nezaplacených prodejních dokladů](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

Mezi hlavní akce na stránce patří vyplnění políčka **Platba** a pole **Datum přijetí**. Můžete nastavit [!INCLUDE[d365fin](includes/d365fin_md.md)] k automatickému zadávání pracovního data do pole **Datum přijetí** když vyberete zaškrtávací políčko **Platba**.

### Automatické vyplnění pole **Datum přijetí** na stránce **Registrace plateb**
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení registrace plateb** související odkaz.
2. Zaškrtněte políčko **Automaticky doplnit datum přijetí**.
3. Otevřete stránku **Registrace plateb** a pokračujte ve zpracování příchozích plateb zákazníků pomocí popsané funkce pro automatické zadávání hodnot pole.

## Viz také
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Finance](finance.md)
