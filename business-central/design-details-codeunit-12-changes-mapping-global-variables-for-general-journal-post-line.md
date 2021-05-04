---
    title: Changes in Mapping Global Variables for Posting in Codeunit 12
    description: In earlier versions, codeunit 12 was changed to help improve performance in posting from the general journal. Learn about the changes to the global variables.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/28/2020
    ms.author: edupont

---
# Historické změny v Codeunitě 12: Mapování globálních proměnných pro řádek finančího deníku

Následující změny byly implementovány ve verzích [!INCLUDE [navnow_md](includes/navnow_md.md)].

| **Microsoft Dynamics NAV 2009 R2** | **Microsoft Dynamics NAV 2013 R2** | **Komentář** |
|----------------------------------------|----------------------------------------|-----------------|  
| GLSetup@1009 : Record 98; | GLSetup@1009 : Record 98; | Beze změny |
| SalesSetup@1010 : Record 311; | Změněno na místní |
| PurchSetup@1011 : Record 312; | Změněno na místní |
| AccountingPeriod@1012 : Record 50; | Změněno na místní |
| GLAcc@1013 : Record 15; | Změněno na místní |
| GLEntry@1014 : Record 17; | GlobalGLEntry@1014 : Record 17; | Přejmenováno |
| GLEntryTmp@1015 : TEMPORARY Record 17; | TempGLEntryBuf@1010 : TEMPORARY Record 17; | Přejmenováno |
| TempGLEntryVAT@1016 : TEMPORARY Record 17; | TempGLEntryVAT@1016 : TEMPORARY Record 17; | Beze změny |
| OrigGLEntry@1017 : Record 17; | Smazáno |
| VATPostingSetup@1019 : Record 325; | Změněno na místní |
| Cust@1020 : Record 18; | Změněno na místní |
| Vend@1021 : Record 23; | Změněno na místní |
| GenJnlLine@1022 : Record 81; | Změněno na místní |
| GLReg@1029 : Record 45; | GLReg@1029 : Record 45; | Beze změny |
| CustPostingGr@1030 : Record 92; | Změněno na místní |
| VendPostingGr@1031 : Record 93; | Změněno na místní |
| Currency@1032 : Record 4; | Změněno na místní |
| AddCurrency@1033 : Record 4; | AddCurrency@1033 : Record 4; | Beze změny |
| ApplnCurrency@1034 : Record 4; | Změněno na místní |
| CurrExchRate@1035 : Record 330; | CurrExchRate@1035 : Record 330; | Beze změny |
| VATEntry@1038 : Record 254; | VATEntry@1038 : Record 254; | Beze změny |
| BankAcc@1039 : Record 270; | Změněno na místní |
| BankAccLedgEntry@1040 : Record 271; | Změněno na místní |
| CheckLedgEntry@1041 : Record 272; | Změněno na místní |
| CheckLedgEntry2@1042 : Record 272; | Změněno na místní |
| BankAccPostingGr@1043 : Record 277; | Změněno na místní |
| GenJnlTemplate@1044 : Record 80; | Změněno na místní |
| TaxJurisdiction@1045 : Record 320; | Změněno na místní |
| TaxDetail@1046 : Record 322; | TaxDetail@1046 : Record 322; | Beze změny |
| FAGLPostBuf@1047 : TEMPORARY Record 5637; | Změněno na místní |
| UnrealizedCustLedgEntry@1084 : Record 21; | UnrealizedCustLedgEntry@1084 : Record 21; | Beze změny |
| UnrealizedVendLedgEntry@1085 : Record 25; | UnrealizedVendLedgEntry@1085 : Record 25; | Beze změny |
| GLEntryVATEntryLink@1087 : Record 253; | GLEntryVATEntryLink@1087 : Record 253; | Beze změny |
| TempVATEntry@1088 : TEMPORARY Record 254; | TempVATEntry@1088 : TEMPORARY Record 254; | Beze změny |
| ReversedGLEntryTemp@1089 : TEMPORARY Record 17; | Přesunuto do Codeunit17 |
| CostAccSetup@1092 : Record 1108; | Změněno na místní |
| GenJnlCheckLine@1048 : Codeunit 11; | GenJnlCheckLine@1001 : Codeunit 11; | Beze změny |
| ExchAccGLJnlLine@1049 : Codeunit 366; | Změněno na místní |
| FAJnlPostLine@1050 : Codeunit 5632; | Změněno na místní |
| SalesTaxCalculate@1051 : Codeunit 398; | Změněno na místní |
| GenJnlApply@1052 : Codeunit 225; | Změněno na místní |
| DimMgt@1053 : Codeunit 408; | Změněno na místní |
| JobPostLine@1028 : Codeunit 1001; | Změněno na místní |
| TransferGlEntriesToCA@1091 : Codeunit 1105; | Změněno na místní |
|  | PaymentToleranceMgt@1002 : Codeunit 426; | Přidáno |
|  | AddCurrencyCode@1117 : Code[10]; | Přidáno |
| FiscalYearStartDate@1054 : Date; | FiscalYearStartDate@1011 : Date; | Beze změny |
| NextEntryNo@1055 : Integer; | NextEntryNo@1022 : Integer; | Beze změny |
| BalanceCheckAmount@1056 : Decimal; | BalanceCheckAmount@1056 : Decimal; | Beze změny |
| BalanceCheckAmount2@1057 : Decimal; | BalanceCheckAmount2@1057 : Decimal; | Beze změny |
| BalanceCheckAddCurrAmount@1058 : Decimal; | BalanceCheckAddCurrAmount@1058 : Decimal; | Beze změny |
| BalanceCheckAddCurrAmount2@1059 : Decimal; | BalanceCheckAddCurrAmount2@1059 : Decimal; | Beze změny |
| CurrentBalance@1060 : Decimal; | CurrentBalance@1060 : Decimal; | Beze změny |
| SalesTaxBaseAmount@1061 : Decimal; | Změněno na místní |
| TotalAddCurrAmount@1062 : Decimal; | TotalAddCurrAmount@1062 : Decimal; | Beze změny |
| TotalAmount@1063 : Decimal; | TotalAmount@1063 : Decimal; | Beze změny |
| UnrealizedRemainingAmountCust@1086 : Decimal; | UnrealizedRemainingAmountCust@1086 : Decimal; | Beze změny |
| UnrealizedRemainingAmountVend@1074 : Decimal; | UnrealizedRemainingAmountVend@1074 : Decimal; | Beze změny |
| NextVATEntryNo@1064 : Integer; | NextVATEntryNo@1064 : Integer; | Beze změny |
| FirstNewVATEntryNo@1065 : Integer; | FirstNewVATEntryNo@1065 : Integer; | Beze změny |
| NextTransactionNo@1066 : Integer; | NextTransactionNo@1066 : Integer; | Beze změny |
| NextConnectionNo@1067 : Integer; | NextConnectionNo@1067 : Integer; | Beze změny |
| InsertedTempGLEntryVAT@1068 : Integer; | InsertedTempGLEntryVAT@1027 : Integer; | Beze změny |
| LastDocNo@1069 : Code[20]; | LastDocNo@1023 : Code[20]; | Beze změny |
| LastLineNo@1070 : Integer; | Smazáno |
| LastDate@1071 : Date; | LastDate@1021 : Date; | Beze změny |
| LastDocType@1072 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder'; | LastDocType@1025 : ' ,Payment,Invoice,Credit Memo,Finance Charge Memo,Reminder'; | Beze změny |
| NextCheckEntryNo@1073 : Integer; | NextCheckEntryNo@1028 : Integer; | Beze změny |
| AddCurrGLEntryVATAmt@1075 : Decimal; | AddCurrGLEntryVATAmt@1017 : Decimal; | Beze změny |
| CurrencyDate@1076 : Date; | CurrencyDate@1020 : Date; | Beze změny |
| CurrencyFactor@1077 : Decimal; | CurrencyFactor@1019 : Decimal; | Beze změny |
| UseCurrFactorOnly@1078 : Boolean; | UseCurrFactorOnly@1078 : Boolean; | Beze změny |
| NonAddCurrCodeOccured@1079 : Boolean; | NonAddCurrCodeOccured@1079 : Boolean; | Beze změny |
| FADimAlreadyChecked@1080 : Boolean; | FADimAlreadyChecked@1080 : Boolean; | Beze změny |
| AllApplied@1081 : Boolean; | Změněno na místní |
| OverrideDimErr@1018 : Boolean; | OverrideDimErr@1018 : Boolean; | Beze změny |
| JobLine@1036 : Boolean; | JobLine@1036 : Boolean; | Beze změny |
| Prepayment@1037 : Boolean; | Smazáno |
| CheckUnrealizedCust@1082 : Boolean; | CheckUnrealizedCust@1082 : Boolean; | Beze změny |
| CheckUnrealizedVend@1083 : Boolean; | CheckUnrealizedVend@1083 : Boolean; | Beze změny |
| GLEntryNo@1090 : Integer; | GLEntryNo@1026 : Integer; | Beze změny |
|  | GLSetupRead@1015 : Boolean; | Přidáno |
|  | AmountRoundingPrecision@1012 : Decimal; | Přidáno |
|  | CrCardTransactionEntryNo@1013 : Integer; | Přidáno |

## Viz také
[Detaily návrhu: Změny v Codeunitě 12: Změny prodecur účtování ve Finančním deníku](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]