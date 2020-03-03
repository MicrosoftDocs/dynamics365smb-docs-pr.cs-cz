---
    title: Exchange Data | Microsoft Docs
    description: You can exchange data between Business Central and external files or streams in connection with common business tasks, such as sending and receiving electronic documents and importing and exporting bank files.
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
# Výměna dat
Můžete vyměňovat data mezi [!INCLUDE[d365fin](includes/d365fin_md.md)]  a externími soubory nebo datovými toky v souvislosti s běžnými obchodními úkoly, jako je odesílání a přijímání elektronických dokladů nebo import a export bankovních souborů.

Než budete moci odesílat a přijímat elektronické doklady nebo importovat a exportovat bankovní soubory, musíte nastavit rámec pro výměnu dat pro zpracování datových souborů nebo datových toků. Kromě toho je nutné nastavit související oblasti, jako například zákazníky, kterým odesíláte elektronické faktury a rozšíření AMC Banking 365 Fundamentals, pokud rozesíláte převody bankovních souborů externímu poskytovateli služeb. Pro více informaci navštivte [Nastavení výměny dat](across-set-up-data-exchange.md).

Následující tabulka popisuje sekvenci úloh s odkazy na témata, které je popisují.

| **Viz** | **Také** |
|------------|-------------|  
| Převedení záznamů prodejních dokladů v [!INCLUDE[d365fin](includes/d365fin_md.md)] do standardizovaného formátu a jejich odeslání jako elektronické doklady, které mohou zákazníci nahrát do svého systému. | [Posílání elektronických dokumentů](sales-how-to-send-electronic-documents.md) |
| Odesílání obrázkových a PDF souborů poskytovateli služeb OCR a jejich přijímání zpět jako elektronické doklady, které v [!INCLUDE[d365fin](includes/d365fin_md.md)] lze převést na záznamy dokladů. | [Použití funkce OCR k převedení souborů PDF a obrázkových souborů do elektronických dokumentů](across-how-use-ocr-pdf-images-files.md) |
| Příjem elektronických dokumentů, buď od služby OCR, nebo od služby výměny dokumentů ve standardizovaném formátu, který převedete v [!INCLUDE[d365fin](includes/d365fin_md.md)] na příslušné záznamy dokumentů. | [Příjem a převod elektronických dokumentů](purchasing-how-to-receive-and-convert-electronic-documents.md) |
| Připravení na import souboru s výpisem z účtu na stránku **Deník odsouhlasení plateb**, jako první krok při vyrovnávání plateb, nebo na stránku **Odsouhlasení bankovního účtu**, jako první krok při vyrovnávání bankovních účtů. | [Nastavení služby Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md) |
| Export plateb z **Deníku plateb** do bankovních souborů, které můžete nahrát do vaší banky pro zpracování. | [Export plateb do bankovního souboru](payables-how-export-payments-bank-file.md) |
| Vytváření elektronických plateb podle standardu EU nebo SEPA Převedení kreditu. | [Provádění plateb pomocí služby převodu bankovních dat nebo převodem na SEPA Převedení kreditu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md) |
| Podle nastavení přímý debet SEPA pověřte svou banku, aby převáděla částky plateb z bankovních účtů vašich zákazníků na firemní účet. | [Vytvoření přímého inkasa SEPA a jeho exportace do bankovního souboru](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md) |
| Aktualizaci stránky **Měny** pomocí poskytovatele směnných kurzů. | [Aktualizace směnných kurzů](finance-how-update-currencies.md) |
| Zobrazení prvků souborů, které jsou mapovány do polí v [!INCLUDE[d365fin](includes/d365fin_md.md)] při importu souborů výpisů SEPA CAMT. | [Mapování polí při importu souborů SEPA CAMT](across-field-mapping-when-importing-sepa-camt-files.md) |
| Zobrazení polí v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)], která jsou mapovány na prvky souboru při exportu platebních souborů pomocí rozšíření AMC Banking 365 Fundamentals. | [Mapování polí při exportu platebních souborů pomocí rozšíření AMC Banking 365 Fundamentals ](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md) |

## Viz také
[Nastavení výměny dat](across-set-up-data-exchange.md)  
[Elektronická výměna dat](across-data-exchange.md)  
[Fakturace prodeje](sales-how-invoice-sales.md)  
[Záznam nákupu](purchasing-how-record-purchases.md)  
[Došlé doklady](across-income-documents.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)
