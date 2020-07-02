---
title: Use the Suggest Vendor Payments Batch Job| Microsoft Docs
description: You can specify vendor payment settings to get suggestions or proposals for payments that are due soon or where a discount is available.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: sgroespe

---
# Návrh platby dodavateli
Na stránce **Deník plateb** můžete k navrhování platebních řádků použít dávkovou úlohu **Navrhnout platby dodavateli**. Řádky pro platby, které jsou brzy splatné nebo platby, kde je k dispozici platební skonto, jsou navrhovány na základě vašeho nastavení.

Chcete-li plně využít výhod návrhů plateb, musíte nejprve prioritizovat vaše dodavatele. Pro více informací navštivte [Prioritizace dodavatelů](purchasing-how-prioritize-vendors.md).

> [!NOTE]
> Položky dodavatele, které jsou **přidrženy**, nejsou zahrnuty do dávkové úlohy.

> [!IMPORTANT]
> Pokud chcete využít platebních slev a zadali jste dostupnou částku, bude částka použita pro:
* Prioritizované položky dodavatele po lhůtě splatnosti první v pořadí podle priority.
* Položky dodavatele po lhůtě splatnosti, které nejsou upřednostňovány.
* Otevřené položky dodavatele, které splňují podmínky pro poskytnutí slev na platby, uspořádané podle čísla dodavatele.

## Použití funkce Navrhnout platby dodavatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Deníky plateb** a poté vyberte související odkaz.
2. Otevřete příslušný deník a poté vyberte akci **Navrhnout platby dodavateli**.
3. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vyberte tlačítko **OK**.

## Vložení data splatnosti jako data účtování na řádky platebních deníků
Při použití dávkové úlohy **Navrhnout platby dodavateli** k vytvoření platebních řádků pro vaše dodavatele můžete vyplnit dvě zvláštní pole a ujistit se, že vygenerované řádky používají datum splatnosti pro výpočet data zaúčtování. Tato pole jsou **Výpočet data zaúčtování z Data splatnosti vyrovnání dokladu** a **Posun data splatnosti vyrovnání dokladu**.

> [!IMPORTANT]
> Nelze použít pole **Výpočet data zaúčtování z data splatnosti vyrovnání dokladu** společně s polem **Vyhledat skonto** nebo **Dodavatel na jeden řádek**. Pokud je zúčtovací datum založen na datu splatnosti, nemusí být některá skonta správně vypočtena, protože zúčtovací datum je po datu skonta.

Pokud je vypočtené datum zaúčtování v minulosti, pak se datum zaúčtování přesune na pracovní datum a zobrazí se varování.

Případně můžete manuálně vytvořit platební řádky pomocí data splatnosti pro výpočet data účtování. Poté, co použijete položky dodavatele, můžete pomocí akce **Vypočíst zúčtovací datum** aktualizovat datum zaúčtování na řádku deníku s datem splatnosti příslušné nákupní faktury. Pro více informací navštivte [Ruční vyrovnání nákupních transakcí](payables-how-apply-purchase-transactions-manually.md).

> [!NOTE]
> Je-li nákupní faktura zpožděna, je datum zaúčtování nastaven na pracovní datum a písmo na řádku bude červené.

## Viz také
[Správa závazků](payables-manage-payables.md)  
[Provádění plateb](payables-make-payments.md)  
[Práce s finančním deníkem](ui-work-general-journals.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
