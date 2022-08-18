---
title: Get Started Creating Layouts
description: Learn how to create layouts to personalize the appearance of a report when viewed, printed, or saved.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/23/2022
ms.author: jswymer

---
# Začínáme s vytvářením rozvržení sestav

Business Central přichází s mnoha vestavěnými rozvrženími, která můžete použít ve svých sestavách. Další rozvržení mohouo být přidána jako součást jiných rozšíření. Je však také možné vytvářet vlastní sestavy, a to buď od začátku, nebo na základě existujícího rozvržení.

> [!IMPORTANT]
> Rozvržení sestav můžete také použít k přidání obsahu do e-mailových zpráv. Rozvržení sestav může například ušetřit čas a pomoci zajistit konzistenci tím, že při komunikaci se zákazníky znovu použije stejný obsah. Chcete-li použít vlastní rozvržení sestavy pro e-mail, typ souboru pro rozvržení musí být Word. Nelze použít typ souboru RDLC. Pro více informací navštivte [ Nastavení opakovaně použitelných e-mailových textů a rozvržení](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## Přehled

Při práci s rozvrženími sestav pomáhá představit si rozvržení jako soubor, který je importován a přiřazen k sestavě. Bez ohledu na typ rozvržení je způsob správy rozvržení v Business Central v podstatě stejný. Obvykle budete pracovat se stránkou **Rozvržení sestav**. Hlavní rozdíl spočívá v tom, jak navrhujete rozvržení, což se provádí pomocí softwaru, na kterém je rozvržení postaveno, jako je Word, Excel nebo SQL Server Report Builder.

S ohledem na tento koncept. Při vytváření rozvržení sestav jsou v zásadě tři nebo čtyři úkoly:

1. Rozhodněte se o typu rozvržení.
2. Exportujte kopii existujícího rozvržení a použijte ji jako výchozí bod.
3. Proveďte změny v souboru rozvržení v příslušné aplikaci.
4. Přidejte nový soubor rozvržení k sestavě.

> [!IMPORTANT]
> Rozvržení, které pochází z rozšíření, nelze upravit ani nahradit. Můžete upravovat nebo nahrazovat pouze uživatelem definovaná rozvržení. Na stránce **Rozvržení sestav**  můžete zjistit, zda je rozvržení z rozšíření nebo uživatelem definované, když se podíváte na sloupec **Rozšíření**. Rozvržení z rozšíření zobrazí ve sloupci informace o zdrojovém rozšíření. Sloupec **Rozšíření** bude prázdný pro uživatelem definované rozvržení.
>
> Další informace o rozdílech mezi rozvrženími z rozšíření a uživatelem definovanými najdete v [Layout source](ui-manage-report-layouts.md#layout-sources).

## Začínáme

Konkrétní úkoly se budou lišit v závislosti na vaší situaci. Následující tabulka vám pomůže začít.

| Co chcete udělat? | Viz... |
|-----------------------|------|
| Zjistěte, jaký typ rozvržení je nejlepší pro mou situaci | [Rozhodněte se, jaký typ rozvržení chcete](#decide) |
| Vytvořte nové rozvržení pro sestavu, které je založeno na existujícím rozvržení, přičemž stávající rozvržení zachováte tak, jak je. | [Vytvoření nového rozvržení](#create) |
| Provedení změn existujícího rozvržení použitého v sestavě | [Úprava rozvržení](#modify) |
| Mám novou verzi souboru rozvržení pro sestavu. Chci nahradit existující soubor rozvržení. | [Nahrazení rozvržení](#replace) |
| Přepnutí aktuálního rozvržení používané sestavou na jiné rozvržení | [Nastavení rozvržení používaného sestavout](ui-set-report-layout.md) |
| Změna názvu a popisu rozvržení | [Přejmenování rozvržení](#rename) |

## <a name="decide"></a>Rozhodněte se, jaký typ rozvržení chcete

První věcí při vytváření rozvržení je rozhodnout, který [typ rozvržení](ui-manage-report-layouts.md#layout-types) chcete. Můžete zvolit Word, Excel nebo RDLC. Typ rozvržení bude záviset na tom, jak má vygenerovaná sestava vypadat. Navíc záleží na vašich znalostech aplikačního softwaru pro vytváření rozvržení, jako je Word, Excel a SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Rozvržení aplikace Excel se obecně nejsnáze vytváří a upravuje, protože funkce pro sumarizaci dat, přidávání grafiky a styly jsou běžné funkce aplikace Excel.

* Ne všechny sestavy a dokumenty mají datovou sadu, která je optimalizovaná pro použití s rozložením aplikace Excel. Například agregace a složité výpočty fungují nejlépe s rozloženími RDLC nebo Word. Totéž platí pro doklady.

* Pokud provádíte pouze změny stylu, jako je typ písma, velikost a barvy, je dobrou volbou také rozložení aplikace Word.

* Přidání datových polí nebo změna uspořádání datových polí v aplikaci Word nebo RDLC je pokročilejší než v aplikaci Excel.

* Rozvržení Word a RDLC je dobré použít pro sestavy, které budou vytištěny.

* Obecné koncepty návrhu pro rozvržení Word a RDLC jsou podobné. Každý typ má však určité konstrukční prvky, které ovlivňují vzhled generované sestavy v [!INCLUDE[prod_short](includes/prod_short.md)]. Stejná sestava může při použití rozvržení Wordu vypadat jinak než rozložení RDLC.

## <a name="create"></a>Vytvoření nového rozvržení

Existují dva způsoby, jak vytvořit nové rozvržení z existujícího rozvržení. Jedním ze způsobů je uložení existujícího rozvržení do kopie. Druhým způsobem je export existujícího rozvržení.

## [Kopírování](#tab/copy)

Kopírování je rychlý způsob, jak vytvořit nové rozvržení, které je stejné již vytvořené. Jakmile budete mít kopii, provedete úpravy exportem rozvržení.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vyberte rozvržení, které chcete pro nové rozvržení zkopírovat, a pak vyberte akci **Upravit**.

    Pokud jste vybrali rozvržení rozšíření, budete dotázáni, zda chcete upravit kopii. Chcete-li pokračovat, vyberte **Ano**.
    
    > [!TIP]
    > Při hledání rozvržení vám pomůže pole **Vyhledávání**, panel **Filtr** a třídění sloupců.
3. Změňte **Název rozvržení**.
4. Přepněte přepínač **Uložit změny do kopie** do polohy **Zapnuto**a poté vyberte **OK**

   Nové rozvržení se zobrazí na stránce **Rozvržení sestav**.
5. Chcete-li provést změny v novém rozvržení navštivte [Úprava existujícího rozvržení](#modify).

### [Exportování/Importování](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vyberte rozvržení, které chcete pro nové rozvržení zkopírovat, a pak vyberte akci **Exportovat rozvržení**.

Soubor rozvržení se stáhne do vašeho zařízení

    > [!TIP]
    > Při hledání rozvržení vám pomůže pole **Vyhledávání**, panel **Filtr** a třídění sloupců.

3. Otevřete soubor rozložení v příslušné aplikaci, například Word (pro soubor .docx) nebo Excel (pro soubor .xlsx).

   Pro více informací navštivte:

   * [Práce s rozvrženími aplikace Excel](ui-how-add-fields-word-report-layout.md)
   * [Práce s rozvrženími aplikace Excel](ui-excel-report-layouts.md)
   * [Práce s RDLC rozvrženími](ui-rdlc-report-layouts.md)

   Proveďte změny v souboru a uložte jej.

4. Zpět na **Rozvržení sestav** a vyberte akci **Nové rozvržení**.
5. Vyplňte následující pole:

   | Pole | Popis | Povinný |
   |-----|-----------|---------|
   | ID Sestavy | Nastavte na ID přiřazené k sestavě | ano |
   | Název rozvržení | Zadejte stručný popis rozložení, který vám pomůže snadno ho identifikovat. | ano |
   | Popis | Zadejte podrobnější informace o rozvržení. | ne |
   | Možnosti formátování | Nastavte toto pole tak, aby odpovídalo typu rozložení, například Word, Excel nebo RDLC. | ano |

6. Výběrem **OK** > **Vybrat** otevřete na svém zařízení průzkumníka souborů.
7. Najděte a vyberte soubor Excel a poté vyberte **Otevřít**.

   Vybraný soubor se nahraje do rozvržení a vrátíte se na stránku **Rozvržení Sestav**.

Pokud chcete vidět, jak sestava vypadá s novým rozvržením, vyberte rozvržení v seznamu a pak vyberte **Spustit sestavu**.

---

## <a name="modify"></a>Úprava rozvržení

Chcete-li upravit existující rozvržení definované uživatelem, postupujte takto.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vyberte rozvržení, které chcete upravit, a pak vyberte akci **Exportovat rozvržení**.

Soubor rozvržení se stáhne do vašeho zařízení

> [!TIP]
> Při hledání rozvržení vám pomůže pole **Vyhledávání**, Filtr **Filtr** a třídění sloupců.

3. Otevřete soubor rozložení v příslušné aplikaci, například Word (pro soubor .docx) nebo Excel (pro soubor .xlsx).

   Pro více informací navštivte:

   * [Práce s rozvrženími aplikace Excel](ui-how-add-fields-word-report-layout.md)
   * [Práce s rozvrženími aplikace Excel](ui-excel-report-layouts.md)
   * [Práce s RDLC rozvrženími](ui-rdlc-report-layouts.md)

   Proveďte změny v souboru a uložte jej.

4. Zpět na stránce **Rozvržení sestav** vyberte existující rozložení a pak vyberte akci **Nahradit rozložení**
5. Výběrem **OK** > **Vybrat** otevřete na svém zařízení průzkumníka souborů.
6. Najděte a vyberte soubor Excel a poté vyberte **Otevřít**.

   Vybraný soubor se nahraje do rozvržení a vrátíte se na stránku **Rozvržení Sestav**.
7. Pokud chcete vidět, jak sestava vypadá s novým rozvržením, vyberte rozvržení v seznamu a pak vyberte **Spustit sestavu**.

## <a name="replace"></a>Nahrazení rozvržení

Pomocí těchto kroků nahraďte existující uživatelem definovaný soubor rozložení novým souborem.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vyberte existující rozvržení a poté vyberte akci **Nahradit rozvržení**.
3. Vyberte **OK** > **zvolte**, zda chcete v zařízení otevřít Průzkumníka souborů.
4. Najděte a vyberte excelový soubor a pak vyberte **Otevřít**.

Vybraný soubor se nahraje do rozvržení a vrátíte se na stránku **Rozvržení Sestav**.
5. Pokud chcete vidět, jak sestava vypadá s novým rozvržením, vyberte rozvržení v seznamu a pak vyberte **Spustit sestavu**.

## <a name="rename"></a>Přejmenování rozvržení

Chcete-li změnit název a popis uživatelsky definovaného rozvržení, postupujte podle těchto kroků..

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Vyberte rozložení, které chcete přejmenovat, a pak vyberte akci **Úprava informací**.

    > [!TIP]
    > Při hledání rozvržení vám pomůže pole **Vyhledávání**, panel **Filtr** a třídění sloupců.
3. Změňte **Název rozvržení**, pak vyberte **OK**.

## Viz související školení na webu [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## Viz také

[Správa rozvržení sestav](ui-manage-report-layouts.md)
[Práce s rozvržením aplikace Word](ui-how-add-fields-word-report-layout.md)  
[Práce s rozvržením aplikace Excel](ui-excel-report-layouts.md)  
[Práce s sestavy, dávkovými úlohami, a XMLporty](ui-work-report.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]