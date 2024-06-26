---
title: Advance Payments Localization for Czech (Extension) 
description: This section describes Advance Payments Localization for Czech extension functionality.
author: v-pejano

ms.service: dynamics-365-business-central
ms.topic: article
ms.search.keywords: Czech, Finance, Localization
ms.date: 06/01/2024
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Zálohové platby pro Česko (rozšíření)

Rozšíření **Zálohové platby** se v [!INCLUDE[prodshort](../../includes/prodshort.md)] používá pro vytváření faktur a provádění plateb před dodáním zboží nebo služby. Řešení Zálohové platby pomáhá společnostem plnit zákonné požadavky na evidenci a účtování záloh, včetně požadavků na DPH v České republice.  

Funkcionalita Zálohové platby umožňuje přijímat zálohové faktury od dodavatelů, vystavovat zálohové faktury zákazníkům, realizovat zálohové platby včetně plateb podléhajících DPH a čerpat uhrazené zálohy na dokladech. Dále poskytuje legislativou požadované daňové doklady, výstupy pro finanční výkazy a výkazy DPH.  

**Součástí modulu jsou:**  

- Prodejní a nákupní zálohové faktury
- Zálohové platby přijaté i vydané
- Daňové doklady a daňový dobropisy k přijatým či vydaným zálohovým platbám  

**Hlavní funkce modulu:**  

- Vytváření prodejních či nákupních zálohových faktur dle nastavení šablon záloh
- Vytváření záloh z prodejních objednávek na základě procenta nebo zadané částky
- Návrh záloh do platebního příkazu a na druhé straně úhrada záloh bankou
- Propojení s modulem Pokladna pro možnost úhrady záloh pokladní hotovostí
- Vystavení a tisk zálohových daňových dokladů k úhradám záloh a to automaticky nebo ručně
- Správa čerpání uhrazených záloh konečnou fakturou
- Možnost uzavření nevyčerpané zálohy, včetně daňového vypořádání
- Práce s cizí měnou, kurzovými rozdíly mezi zálohovou platbou a fakturou
- Možnost zrušení přiřazení platby zálohové faktury nebo dodatečné propojení
- Možnost zrušení propojení konečné faktury se zálohou nebo dodatečné propojení
- Podpora Center odpovědnosti k dokladům záloh tak, aby se zobrazovaly pouze doklady relevantní pro konkrétního uživatele
- Reporty pro rekapitulaci úhrad a čerpání záloh, reporty pro rekapitulaci DPH ze záloh  

**Omezení aplikace:**  

- Použití jedné měny v rámci jednoho obchodního případu
- Vytváření zálohových faktur z dokladů ani dodatečné přiřazení volných zálohových faktur k dokladu nezohledňuje fakturační nebo skonto slevy
- Zálohy nelze použít na dobropisech a objednávkách vratky (řeší se odpojením zálohy od zaúčtované faktury a dobropisováním faktury bez záloh)
- Se zálohami nespolupracuje modul servis
- V zálohách není řešena přídavná měna
- Aplikace nezahrnuje podporu pro změnu sazeb DPH  

Následující tabulka popisuje seznam úloh s odkazy na témata, které je popisují.

| Funkce | Odkaz |
| --- | --- |
|Aktivace funkcionality Zálohové platby a upgrade stávajících dat.|[Aktivace a upgrade zálohových plateb](adv-payments-how-to-activate-advance-payments.md)|
|Porozumění základním principům aplikace Zálohových plateb, životní cyklus zálohy. |[Základní principy účtování a použití zálohových plateb](adv-payments-principles.md)|
|Nastavení šablon záloh, účtování DPH a výkazu DPH.|[Nastavení zálohových plateb](adv-payments-how-to-setup-advance-payments.md)|
|Založení zálohové faktury a tisk.|[Vytvoření zálohové faktury](adv-payments-how-to-create-advance-invoice.md)|
|Vytvoření zálohy z objednávky.|[Vytvoření zálohy z objednávky](adv-payments-how-to-create-advance-invoice-from-order.md)|
|Úhrada zálohy finančním deníkem nebo pokladnou.|[Úhrada zálohy](adv-payments-how-to-pay-advance-payment.md)|
|Vytvoření daňového dokladu k záloze, korekce DPH u nákupní zálohy, tisk dokladu.|[Vytvoření daňového dokladu k záloze](adv-payments-how-to-create-tax-document.md)|
|Vytvoření konečné faktury, její propojení se zálohou a zaúčtování.|[Propojení zálohy s konečnou fakturou](adv-payments-how-to-link-invoice.md)|
|Uzavření nevyčerpané zálohy.|[Uzavření zálohy](adv-payments-how-to-close-advance-payment.md)|
|Cizí měny a zálohové faktury.|[Zálohy v cizí měně](adv-payments-foreign-currency.md)|
|Storno zálohového daňového dokladu, odpojení chybné platby od zálohy, dodatečné připojení platby k záloze, připojení zálohy do již zaúčtované faktury, odpojení zálohy od zaúčtované faktury.|[Doplňkové funkce](adv-payments-additional-functions.md)|
|Přehled zálohových faktur, DPH ze zálohových faktur, rekapitulace zálohových faktur.|[Kontrolní sestavy záloh](adv-payments-check-reports.md)|

## Viz také

[České lokální funkcionality](czech-local-functionality.md)  
[Finance](../../finance.md)
