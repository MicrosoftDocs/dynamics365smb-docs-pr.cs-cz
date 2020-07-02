---
title: Work with Incoming Documents| Microsoft Docs
description: You can manage incoming external business documents, such as payment receipts or PDFs, manage OCR tasks, and convert files to electronic documents and records.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: sgroespe

---
# Došlé doklady
Některé obchodní transakce nejsou od počátku používání zaznamenány v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Místo toho se do vaší společnosti dostane externí obchodní doklad jako příloha e-mailu nebo papírová kopie, kterou naskenujete. To je typické pro nákupy, kde takové soubory příchozích dokladů představují potvrzení o platbách za výdaje nebo malé nákupy.

Z PDF nebo obrazových souborů představujících příchozí doklady můžete nechat externí službu OCR (Optické rozpoznávání znaků) generovat elektronické doklady, které pak mohou být převedeny záznam v evidenci dokladů v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Na stránce **Došlé doklady** můžete pomocí různých funkcí prohlížet účtenky, spravovat úlohy OCR a ručně nebo automaticky převádět soubory příchozích dokladů na příslušné doklady nebo řádky deníku. Externí soubory lze připojit v libovolné fázi procesu, včetně zaúčtovaných dokladů a výsledných položek dodavatele, zákazníka a financí.

Proces došlých dokladů se může skládat z následujících hlavních činností:

* Evidence externích dokladů v [!INCLUDE[d365fin](includes/d365fin_md.md)] vytvořením řádků na stránce **Došlé doklady** jedním z následujících způsobů:
   * Ručně pomocí jednoduchých funkcí, buď z počítače nebo z mobilního zařízení, jedním z následujících způsobů:
      * Použitím tlačítka **Vytvořit ze souboru** a vyplněním patřičných polí na stránce **Došlý doklad**. Soubor se automaticky připojí.
      * Použitím tlačítka **Nový**, vyplněním patřičných polí na stránce **Došlý doklad** a manuální připojení dokladu.
      * Z tabletu nebo telefonu použitím tlačítka **Vytvořit z fotoaparátu** k vytvoření nového záznamu příchozího dokladu a potom odesláním obrázku například službě OCR.
   * Automaticky přijetím dokladu ze služby OCR jako elektronického dokladu poté, co jste odeslali e-mailem související soubor PDF nebo obrázek službě OCR. Záložka **Finanční Informace** je automaticky vyplněna na stránce **Došlý doklad**.
* Pomocí služby OCR můžete mít PDF nebo obrazové soubory převedené na elektronické doklady, které lze převést na záznamy dokladů v [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Vytvořte nové doklady nebo řádky finančního deníku pro záznamy příchozích dokladů zadáním informací při jejich čtení z příchozích souborů.
* Připojte příchozí soubory k nákupním a prodejním dokladům v jakémkoli stavu, včetně položek dodavatele, zákazníka a financí, které vyplývají z účtování.
* Zobrazení záznamů příchozích dokladů a jejich příloh z libovolného nákupního a prodejního dokladu, položek nebo vyhledání všech finančních položek bez příchozích záznamů dokladů na stránce **Účetní osnova**.

| Viz | Také |
| --- | --- |
| Nastavení funkce Došlých dokladů a nastavení služby OCR | [Nastavení došlých dokladů](across-how-setup-income-documents.md) |
| Vytváření záznamů došlých dokladů, připojování souborů, použití služby OCR k přeměně PDF souborů na elektronické doklady, převedení elektronických dokladů na evidenci dokladů, kontrola záznamů došlých dokladů z zaúčtovaných prodejních a nákupních dokladů. | [Zpracování došlých dokladů](across-process-income-documents.md) |

## Viz související školení v programu [Microsoft Learn](/learn/modules/incoming-documents-dynamics-365-business-central/index)

## Viz také
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
