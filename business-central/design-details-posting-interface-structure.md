---
    title: Design Details - Posting Interface Structure | Microsoft Docs
    description: This topic provides an overview of the global procedures in the posting interface structure.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: posting, interface, design
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Struktura účtovacího rozhraní
V [!INCLUDE[prod_short](includes/prod_short.md)] struktura účtovacího rozhraní, existuje několik globálních procedur, které používají stejnou strukturu:

* Volání kódu procedur RunWithCheck a RunWithoutCheck – obecné rozhraní pro účtování pro Řádek finančního deníku.
* CustPostApplyCustLedgEntry – Účtování vyrovnaných položek zákazníka, spuštěné z codeunity 226 CustEntry-Apply Posted Entries.
* VendPostApplyVendLedgEntry – Účtování vyrovnaných položek dodavatele, spuštěné z codeunity 227 VendEntry-Apply Posted Entries.
* UnapplyCustLedgEntry – Účtování zrušených vyrovnaných položek zákazníka, spuštěné z codeunity 226 CustEntry-Apply Posted Entries
* UnapplyVendLedgEntry – Účtování zrušených vyrovnaných položek dodavatele, spuštěné z codeunity 227 VendEntry-Apply Posted Entries

## Viz také
[Detaily návrhu: Struktura enginu účtování](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]