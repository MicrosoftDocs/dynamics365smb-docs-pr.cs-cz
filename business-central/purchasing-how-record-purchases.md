---
title: Create a Purchase Invoice and Record Purchases | Microsoft Docs
description: Describes how to purchase inventory, non-inventory items, or resources by creating and posting purchase invoices or orders.
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 04/01/2020
ms.author: sgroespe

---
# Záznam nákupu
Můžete vytvořit nákupní fakturu nebo objednávku, abyste zaznamenali náklady na nákup a sledovali závazky. Pokud potřebujete kontrolovat zásoby, nákupní faktury a objednávky, můžete použít také dynamickou aktualizaci úrovní zásob, abyste mohli minimalizovat náklady na zásoby a poskytovat lepší služby zákazníkům. Nákupní náklady, včetně nákladů na služby a hodnoty zásob, které vyplývají z účtování nákupních faktur nebo objednávek, přispívají k údajům o zisku a dalším finančním KPI ve vašem centru rolí.

Kromě nákupu fyzického zboží  (typ zboží **Zásoby**), které ovlivňují oceňování zásob, můžete nakupovat služby reprezentované časovými jednotkami. To lze provést buď s typem zboží **Služba** nebo s typem řádku **Zdroj**.

> [!NOTE]
> Musíte použít nákupní objednávky, pokud váš nákupní proces vyžaduje, abyste zaznamenali částečné příjmy z množství objednávky, například protože celé množství nebylo u dodavatele k dispozici. Pokud prodáváte zboží doručováním přímo od vašeho dodavatele k zákazníkovi, jako zásilku, musíte použít také nákupní objednávky. Pro více informací navštivte [Provedení přímé dodávky](sales-how-drop-shipment.md). Ve všech ostatních aspektech fungují objednávky stejně jako nákupní faktury. Následující postup je založen na nákupní faktuře. Kroky jsou podobné pro objednávku.

Když obdržíte skladové položky nebo po dokončení nakoupené služby, zaúčtujte nákupní fakturu nebo objednávku za účelem aktualizace zásob, finančních záznamů a aktivace platby dodavateli podle platebních podmínek. Pro více informací navštivte [Účtování nákupu](ui-post-purchases.md) a [Provádění plateb](payables-make-payments.md).

> [!CAUTION]
> Neúčtujte fyzické zboží nákupní faktury, dokud toto zboží neobdržíte a neznáte konečné náklady na nákup, včetně jakýchkoli dalších poplatků. V opačném případě může dojít ke zkreslení hodnoty zásob a zisku.

Před zaplacením dodavateli můžete snadno opravit nebo zrušit zaúčtovanou nákupní fakturu. To je užitečné, pokud chcete opravit chybu při psaní nebo pokud chcete změnit nákup v rané fázi procesu objednávky. Pro více informací navštivte [Opravit nebo zrušit neuhrazené faktury za nákup](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Pokud jste již za zboží nebo služby na zaúčtované nákupní faktuře zaplatili, musíte ke zrušení nákupu vytvořit nákupní dobropis. Pro více informací navštivte [Zpracování nebo zrušení nákupní vratky](purchasing-how-process-purchase-returns-cancellations.md).

Karta zboží může být typu **Zásoby**, **Služba** a **Neskladované**, který určuje, zda se jedná o fyzické zásoby, jednotku pracovní doby nebo fyzickou jednotku, která není vedena na skladě. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md). Proces nákupní faktury je stejný pro všechny tři typy zboží.

> [!NOTE]
> S typem nákupního řádku **Zdroj** můžete také zakoupit externí zdroje, například za účelem fakturace dodavatele za dodanou práci. Pro více informací navštivte [Nastavení zdrojů](projects-how-setup-resources.md).<br /><br />
> Chcete-li použít zakoupený zdroj, možná budete muset nastavit kapacitu zdroje a ručně ji přiřadit k úloze. Zakoupením zdroje vytvoříte položku zdroje ale tyto položky nejsou sledovány z hlediska množství a hodnoty, jako je například zboží. Pokud je vyžadováno sledování množství a hodnot, zvažte použití jiných typů zboží na řádku.

Políčka dodavatele na nákupní faktuře můžete vyplnit dvěma způsoby, podle toho, zda je dodavatel již zaregistrován.
<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## Vytvoření nákupní faktury
Následující text popisuje, jak vytvořit nákupní fakturu. Kroky jsou podobné pro objednávku. Hlavní rozdíl spočívá v tom, že objednávky mají další pole a akce pro fyzickou manipulaci se zbožím.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktury** a poté vyberte související odkaz.
2. Do pole **Dodavatel** zadejte název existujícího dodavatele.

   Ostatní pole na stránce **Nákupní faktury** jsou nyní vyplněna standardními informacemi vybraného dodavatele. Pokud dodavatel není registrován, postupujte takto:
3. Do pole **Dodavatel** zadejte název nového dodavatele.
4. V dialogovém okně o registraci nového dodavatele vyberte tlačítko **Ano**.
5. Na stránce **Vybrat šablonu pro nového dodavatele** vyberte šablonu, na které bude založena nová karta dodavatele, a poté zvolte tlačítko **OK**.
6. Otevře se nová karta dodavatele, která je předem vyplněna informacemi o vybrané šabloně dodavatele. Do pole **Název** je předvyplněno jméno nového dodavatele, které jste zadali na nákupní faktuře.
7. Pokračujte ve vyplňování zbývajících polí na kartě dodavatele. Pro více informací navštivte [Evidence nových dodavatelů](purchasing-how-register-new-vendors.md).
8. Po dokončení karty dodavatele zvolte tlačítko **OK** a vraťte se na stránku **Nákupní faktura**.

   Několik polí na stránce **Nákupní faktura** je vyplněno informacemi, které jste zadali na nové kartě dodavatele.
9. Podle potřeby vyplňte zbývající pole na stránce **Nákupní faktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   Nyní jste připraveni vyplnit řádky nákupní faktury zbožím nebo zdroji, které jste zakoupili od dodavatele.

   > [!NOTE]
   > Pokud jste pro dodavatele nastavili opakující se nákupní řádky, například měsíční objednávku doplnění, můžete tyto řádky vložit do faktury výběrem akce **Získat periodické nákupní řádky**.
10. Na záložce **Řádky** v poli **Číslo zboží** zadejte číslo skladového zboží nebo servisu.
11. Do pole **Množství** zadejte množství zboží, které chcete zakoupit.

   > [!NOTE]
   > Pro zboží typu **Služby** a pro řádky typu **Zdroj** je množství časovou jednotkou, například hodinami, jak je uvedeno na řádku v poli **Kód měrné jednotky**.

   Pole **Částka na řádku** se aktualizuje tak, aby se v poli **Nákupní cena** zobrazovala hodnota vynásobená hodnotou v poli **Množství**.

   Cena a částka na řádku se zobrazí s nebo bez daně z obratu v závislosti na tom, co jste vybrali v poli **Ceny včetně daně** na kartě dodavatele.

   Pole součtů pod řádky jsou automaticky aktualizována při vytváření nebo úpravě řádků tak, aby zobrazovali částky, které budou zaúčtovány do účetních knih.

   > [!NOTE]
   > Ve vzácných případech se zaúčtované částky mohou lišit od toho, co je zobrazeno v polích součtů. To je obvykle způsobeno výpočty zaokrouhlování ve vztahu k DPH nebo dani z příjmu.<br /><br />Ke kontrole částek, které budou skutečně zaúčtovány, můžete použít stránku **Statistika** která obsahuje výpočty zaokrouhlování. Pokud také zvolíte akci **Vydat**, budou součty aktualizovány tak, aby zahrnovaly výpočty zaokrouhlování.

12. Do pole **Částka fakturační slevy** zadejte částku, která by měla být odečtena z hodnoty uvedené v poli **Celkem včetně  DPH** ve spodní části faktury.

   > [!NOTE]
   > Pokud jste pro dodavatele nastavili slevy na faktuře, zadaná procentuální hodnota, pokud jsou kritéria splněna, se automaticky vloží do pole **Sleva faktury dodavatele %** a příslušná částka se vloží do pole **Částka fakturační slevy**.
13. Když obdržíte zakoupené zboží nebo služby, vyberte **Účtovat**.

Nákup se nyní projeví v zásobách, položkách zdrojů a finančních záznamech a aktivuje se platba dodavatele. Nákupní faktura je odstraněna ze seznamu nákupních faktur a nahrazena novým dokladem v seznamu zaúčtovaných faktur.

## Viz související školení na [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## Viz také
[Nákup](purchasing-manage-purchasing.md)  
[Nastavení nákupu](purchasing-setup-purchasing.md)  
[Nastavení zdrojů](projects-how-setup-resources.md)  
[Účtování nákupu](ui-post-purchases.md)  
[Požadavky nabádky](purchasing-how-request-quotes.md)  
[Nákup zboží pro prodej](purchasing-how-purchase-products-sale.md)  
[Evidence nových dodavatelů](purchasing-how-register-new-vendors.md)  
[Vytvoření přímé dodávky](sales-how-drop-shipment.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
