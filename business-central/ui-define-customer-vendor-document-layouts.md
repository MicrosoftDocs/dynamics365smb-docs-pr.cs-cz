---
title: Assign Special Document Layouts to Customers or Vendors| Microsoft Docs
description: When custom report layouts are defined, you can select them from customer and vendor cards to specify that the selected layouts will be used for documents that you crate for the customer or vendor in question.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 04/01/2020
ms.author: sgroespe

---
# Definování rozložení sestav pro zákaníky a dodavatele
Po definování vlastních rozložení sestav je můžete vybrat z karet zákazníka a dodavatele a určit, která rozložení budou použita pro různé typy dokladů, a které budou použity pro dotyčného zákazníka nebo dodavatele. Hodnota v poli **Použití** definuje, pro který proces bude rozložení dokladu použito, například **Upomínka**, **Dodávka** a **Potvrzení**.

Kromě nastavení rozvržení, která se mají použít pro vybraný doklad, můžete ušetřit čas při odesílání dokladů různým zákazníkům nebo dodavatelům nastavením e-mailových adres konkrétních kontaktů pro použití s ​​konkrétními dokumenty. Například výkazy zákazníků budou odeslány kontaktům účetních, prodejní objednávky odběratelům a nákupní objednávky prodejcům nebo účetím.

ři definování rozložení dokladu pro zákazníka nebo dodavatele můžete také zadat e-mailovou adresu kontaktní osoby, která musí dokument obdržet. Můžete to rychle provést pomocí funkce **Vybrat e-mail z kontaktů** která automaticky filtruje kontaktní e-mailové adresy registrované pro dotyčného zákazníka nebo dodavatele.

Než budete moci definovat, které rozvržení dokumentu se použije pro které procesy a ke kterému kontaktu se má dokument odeslat, musíte načíst všechny dostupné doklady ze stránky **Výběry sestav**. To lze rychle provést pomocí funkce **Kopírovat z výběru sestav**.

Následující text popisuje, jak definovat rozložení prodejních dokladů z karty zákazníka. Postup je stejný pro rozložení nákupních dokladů z karty dodavatele.

## Povolení všech dostupných prodejních dokladů pro zákazníka
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Otevřete kartu zákazníka, pro kterou chcete definovat rozvržení dokladu v rámci jednoho obchodního procesu.
3. Na stránce **Karta zákazníka** zvolte stránnku **Rozvržení dokladu**.
4. Na stránce **Rozvržení dokladu** zvolte akci **Kopírovat z výběru sestavy**.

Na stránce **Rozvržení dokladu** dotyčného zákazníka je vyplněna všemi rozloženími sestav pro prodej, které existují v systému. Pro více informací jak se vytváření navštivte [Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md).

Nyní můžete pokračovat v úpravě seznamu pomocí vlastních rozložení sestav nebo e-mailových adres pro kontakty, kterým musí být doklady odeslány.

## Výběr vlastního rozvržení sestavy, které se použije pro prodejní doklad
Pokud jedno nebo více rozvržení sestav definovaných na stránce **Rozvržení dokladu** pro zákazníka, nemá definováno vlastní rozložení sestavy, můžete to rychle provést.

1. Na stránce **Rozvržení dokladu**zvolte na řádku rozložení sestavy, pro které chcete použít vlastní rozložení, vyberte pole **Popis vlastního rozvržení**. Toto pole je vyplněno, pokud je rozložení zákazníka již vybráno, nebo prázdné.
2. Na stránce **Rozvržení dokladu** vyberte speciální rozvržení dokladu, které chcete použít pro příslušný typ prodejního dokladu. Pro více informací navštivte [Vytvoření a úprava vlastní sestavy nebo rozvržení dokladu](ui-how-create-custom-report-layout.md).

## Nastavení, který kontakt obdrží rozložení dokladu pro zákazníka
Můžete ušetřit čas při odesílání dokladů různým zákazníkům nebo dodavatelům zadáním e-mailových adres kontaktu na různých řádcích na stránce **Rozvržení dokladu**. Například výkazy zákazníků budou odeslány kontaktům účetních, prodejní objednávky odběratelům a nákupní objednávky prodejcům nebo účetím.

1. Na stránce **Rozvržení dokladu** na řádku pro rozvržení sestavy, který chcete odeslat zákazníkovi, vyberte akci **Vybrat e-mail z kontaktů**.
2. Na stránce **Kontakty** vyberte řádek pro příslušný kontakt a poté vyberte tlačítko **OK**.

E-mailová adresa kontaktu je nyní vložena na řádku rozvržení dokladu, takže dotyčný prodejní doklad, například upomínka, je vždy zaslán tomuto kontaktu ve společnosti zákazníka.

## Viz také
[Aktualizace vlastního rozvržení sestav](ui-update-report-layouts.md)  
[Vytvoření a úpravy vlastního rozvržení sestav](ui-how-create-custom-report-layout.md)  
[Import a Export vlastního rozvržení sestav](ui-how-import-and-export-report-layout.md)  
[Odesílání dokladů pomocí e-mailu](ui-how-send-documents-email.md)  
[Správa rozložení sestav](ui-manage-report-layouts.md)  
[Práce se sestavami, dávkovými úlohami a XMLporty](ui-work-report.md)  
[Práce se sestavami, dávkovými úlohami a XMLporty](ui-work-report.md)
