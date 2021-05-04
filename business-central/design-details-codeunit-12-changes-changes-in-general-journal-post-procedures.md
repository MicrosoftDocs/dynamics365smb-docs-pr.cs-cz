---
    title: Changes in General Journal Posting Procedures in Codeunit 12
    description: In earlier versions, codeunit 12 was changed to help improve performance in posting from the general journal. Learn about the changes to the posting procedures in this article.
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
# Historické změny v Codeunitě 12: Změny prodecur účtování ve Finančním deníku

Následující změny byly implementovány ve verzích [!INCLUDE [navnow_md](includes/navnow_md.md)].

| **Microsoft Dynamics NAV 2009 R2** | **Microsoft Dynamics NAV 2013 R2** | **Komentář** |
|----------------------------------------|----------------------------------------|-----------------|  
| GetGLReg | GetGLReg | Aktualizováno |
| RunWithCheck | RunWithCheck | Aktualizováno |
| RunWithoutCheck | RunWithoutCheck | Aktualizováno |
| Kód | Kód | Aktualizováno |
|  | PostGenJnlLine | Přidáno |
|  | InitAmounts | Přidáno |
|  | InitLastDocDate | Přidáno |
| InitVAT | InitVAT | Aktualizováno |
| PostVAT | PostVAT | Aktualizováno |
| InsertVAT | InsertVAT | Aktualizováno |
| SummarizeVAT | SummarizeVAT | Aktualizováno |
| InsertSummarizedVAT | InsertSummarizedVAT | Aktualizováno |
| PostGLAcc | PostGLAcc | Aktualizováno |
| PostCust | PostCust | Aktualizováno |
| PostVend | PostVend | Aktualizováno |
| PostBankAcc | PostBankAcc | Aktualizováno |
| PostFixedAsset | PostFixedAsset | Aktualizováno |
| PostICPartner | PostICPartner | Aktualizováno |
| InitCodeUnit | StartPosting | Aktualizováno |
|  | ContinuePosting | Přidáno |
| FinishCodeunit | FinishPosting | Aktualizováno |
|  | PostUnrealizedVAT | Přidáno |
|  | CheckPostUnrealizedVAT | Přidáno |
|  | ExchangeAccounts | Přidáno |
| InitGLEntry | InitGLEntry | Aktualizováno |
|  | InitGLEntryVAT | Přidáno |
|  | InitGLEntryVATCopy | Přidáno |
| InsertGLEntry | InsertGLEntry | Aktualizováno |
|  | CreateGLEntry | Přidáno |
|  | CreateGLEntryBalAcc | Přidáno |
|  | CreateGLEntryVAT | Přidáno |
|  | CreateGLEntryVATCollectAdj | Přidáno |
|  | CreateGLEntryFromVATEntry | Přidáno |
|  | UpdateCheckAmounts | Přidáno |
| ApplyCustLedgEntry | ApplyCustLedgEntry | Aktualizováno |
|  | CalcPmtDiscPossible | Přidáno |
|  | CalcPmtTolerancePossible | Přidáno |
| CalcPmtTolerance | CalcPmtTolerance | Aktualizováno |
| CalcPmtDisc | CalcPmtDisc | Aktualizováno |
| CalcPmtDiscIfAdjVAT | CalcPmtDiscIfAdjVAT | Aktualizováno |
| CalcPmtDiscTolerance | CalcPmtDiscTolerance | Aktualizováno |
|  | CalcPmtDiscVATBases | Přidáno |
|  | CalcPmtDiscVATAmounts | Přidáno |
|  | InsertPmtDiscVATForVATEntry | Přidáno |
|  | InsertPmtDiscVATForGLEntry | Přidáno |
| CalcCurrencyApplnRounding | CalcCurrencyApplnRounding | Aktualizováno |
| FindAmtForAppln | FindAmtForAppln | Aktualizováno |
| CalcCurrencyUnrealizedGainLoss | CalcCurrencyUnrealizedGainLoss | Aktualizováno |
| CalcCurrencyRealizedGainLoss | CalcCurrencyRealizedGainLoss | Aktualizováno |
| CalcApplication | CalcApplication | Aktualizováno |
| CalcRemainingPmtDisc | CalcRemainingPmtDisc | Přesunuto do Codeunity 426 Payment Tolerance Management |
| CalcAmtLCYAdjustment | CalcAmtLCYAdjustment | Přidáno |
| InitNewCVLedgEntry | InitFromGenJnlLine | Přesunuto do tabulky 383 Zásobník detailní položky zák./dodav. |
| InitOldCVLedgEntry | CopyFromCVLedgEntryBuf | Přesunuto do tabulky 383 Zásobník detailní položky zák./dodav. |
| InsertDtldCVLedgEntry | InsertDtldCVLedgEntry | Přesunuto do tabulky 383 Zásobník detailní položky zák./dodav. |
|  | InitBankAccLedgEntry | Přidáno |
|  | InitCheckLedgEntry | Přidáno |
|  | InitCustLedgEntry | Přidáno |
|  | InitVendLedgEntry | Přidáno |
|  | InsertDtldCustLedgEntry | Přidáno |
|  | InsertDtldVendLedgEntry | Přidáno |
| CustUnrealizedVAT | CustUnrealizedVAT | Aktualizováno |
| CustPostApplyCustLedgEntry | CustPostApplyCustLedgEntry | Aktualizováno |
|  | PrepareTempCustLedgEntry | Přidáno |
| UnapplyCustLedgEntry | UnapplyCustLedgEntry | Aktualizováno |
| TransferCustLedgEntry | CopyFromGenJnlLine | Přesunuto do tabulky 21  Položka zákazníka |
| PostDtldCustLedgEntries | PostDtldCustLedgEntries | Aktualizováno |
|  | PostDtldCustLedgEntry | Přidáno |
|  | PostDtldCustLedgEntryUnapply | Přidáno |
|  | GetDtldCustLedgEntryAccNo | Přidáno |
| ZeroTransNoDtldCustLedgEntries | SetZeroTransNo | Přesunuto do tabulky 379 Detailní položka zákazníka |
| AutoEntrForDtldCustLedgEntries | Refactored to PostDtldCustLedgEntryUnapply |
| CustUpdateDebitCredit | UpdateDebitCredit | Přesunuto do tabulky 379 Detailní položka zákazníka |
| ApplyVendLedgEntry | ApplyVendLedgEntry | Aktualizováno |
|  | PrepareTempVendLedgEntry | Přidáno |
| VendPostApplyVendLedgEntry | VendPostApplyVendLedgEntry | Aktualizováno |
| UnapplyVendLedgEntry | UnapplyVendLedgEntry | Aktualizováno |
| TransferVendLedgEntry | CopyFromGenJnlLine | Přesunuto do tabulky 25 Položky dodavatele |
| PostDtldVendLedgEntries | PostDtldVendLedgEntries | Aktualizováno |
|  | PostDtldVendLedgEntry | Přidáno |
|  | PostDtldVendLedgEntryUnapply | Přidáno |
|  | GetDtldVendLedgEntryAccNo | Přidáno |
|  | PostDtldCVLedgEntry | Přidáno |
|  | PostDtldCustVATAdjustment | Přidáno |
|  | PostDtldVendVATAdjustment | Přidáno |
| ZeroTransNoDtldVendLedgEntries | SetZeroTransNo | Přesunuto do tabulky 380 Detailní položka dodavatele |
| AutoEntrForDtldVendLedgEntries | Refactored to PostDtldVendLedgEntryUnapply |
| VendUpdateDebitCredit | UpdateDebitCredit | Přesunuto do tabulky 380 Detailní položka dodavatele |
| VendUnrealizedVAT | VendUnrealizedVAT | Aktualizováno |
|  | PostUnrealVATEntry | Přidáno |
|  | PostApply | Přidáno |
| PostUnrealVATByUnapply | PostUnrealVATByUnapply | Aktualizováno |
|  | PostUnapply | Přidáno |
|  | InsertDtldCustLedgEntryUnapply | Přidáno |
|  | InsertDtldVendLedgEntryUnapply | Přidáno |
|  | InsertTempVATEntry | Přidáno |
|  | ProcessTempVATEntry | Přidáno |
|  | UpdateCustLedgEntry | Přidáno |
|  | UpdateVendLedgEntry | Přidáno |
| UpdateCalcInterest | UpdateCalcInterest | Aktualizováno |
| UpdateCalcInterest2 | UpdateCalcInterest2 | Aktualizováno |
| GLCalcAddCurrency | GLCalcAddCurrency | Aktualizováno |
| HandleAddCurrResidualGLEntry | HandleAddCurrResidualGLEntry | Aktualizováno |
| CalcLCYToAddCurr | CalcLCYToAddCurr | Aktualizováno |
| CalcAddCurrFactor | Deleted |
| GetCurrencyExchRate | GetCurrencyExchRate | Aktualizováno |
| ExchAmount | ExchangeAmount | Přesunuto do tabulky 330 Směnný kurz |
| ExchangeAmtLCYToFCY2 | ExchangeAmtLCYToFCY2 | Aktualizováno |
| CalcAddCurrForUnapplication | CalcAddCurrForUnapplication | Aktualizováno |
| CheckNonAddCurrCodeOccurred | CheckNonAddCurrCodeOccurred | Aktualizováno |
| CheckCalcPmtDisc | Přesunuto do Codeunity 426 Payment Tolerance Management |
| CheckCalcPmtDiscCVCust | Přesunuto do Codeunity 426 Payment Tolerance Management |
| CheckCalcPmtDiscCust | Přesunuto do Codeunity 426 Payment Tolerance Management |
| CheckCalcPmtDiscGenJnlCust | Přesunuto do Codeunity 426 Payment Tolerance Management |
| CheckCalcPmtDiscCVVend | Přesunuto do Codeunity 426 Payment Tolerance Management |
| CheckCalcPmtDiscVend | Přesunuto do Codeunity 426 Payment Tolerance Management |
| CheckCalcPmtDiscGenJnlVend | Přesunuto do Codeunity 426 Payment Tolerance Management |
| Reverse | Reverse | Přesunuto do Codeunity 17 Gen. Jnl.-Post Reverse |
| ReverseCustLedgEntry | ReverseCustLedgEntry | Přesunuto do Codeunity 17 Gen. Jnl.-Post Reverse |
| ReverseVendLedgEntry | ReverseVendLedgEntry | Přesunuto do Codeunity 17 Gen. Jnl.-Post Reverse |
| ReverseBankAccLedgEntry | ReverseBankAccLedgEntry | Přesunuto do Codeunity 17 Gen. Jnl.-Post Reverse |
| ReverseVAT | ReverseVAT | Přesunuto do Codeunity 17 Gen. Jnl.-Post Reverse |
| SetReversalDescription | SetReversalDescription | Přesunuto do Codeunity 17 Gen. Jnl.-Post Reverse |
| ApplyCustLedgEntryByReversal | ApplyCustLedgEntryByReversal | Přesunuto do Codeunity 17 Gen. Jnl.-Post Reverse |
| ApplyVendLedgEntryByReversal | ApplyVendLedgEntryByReversal | Přesunuto do Codeunity 17 Gen. Jnl.-Post Reverse |
| PostPmtDiscountVATByUnapply | PostPmtDiscountVATByUnapply | Přesunuto do Codeunity 17 Gen. Jnl.-Post Reverse |
|  | CheckDimComb | Přidáno do Codeunity 17 Gen. Jnl.-Post Reverse |
|  | CopyCustLedgEntry | Přidáno do Codeunity 17 Gen. Jnl.-Post Reverse |
|  | CopyVendLedgEntry | Přidáno do Codeunity 17 Gen. Jnl.-Post Reverse |
|  | CopyBankAccLedgEntry | Přidáno do Codeunity 17 Gen. Jnl.-Post Reverse |
| HandlDtlAddjustment | HandleDtldAdjustment | Aktualizováno |
| CollectAddjustment | CollectAdjustment | Aktualizováno |
| SetOverDimErr | SetOverDimErr | Aktualizováno |
| PostJob | PostJob | Aktualizováno |
| InsertVATEntriesFromTemp | InsertVATEntriesFromTemp | Aktualizováno |
| CaptureOrRefundCreditCardPmnt | CaptureOrRefundCreditCardPmnt | Aktualizováno |
| UpdateDOPaymentTransactEntry | UpdateDOPaymentTransactEntry | Aktualizováno |
| ABSMin | ABSMin | Aktualizováno |
| GetApplnRoundPrecision | GetApplnRoundPrecision | Aktualizováno |
| CheckDimValueForDisposal | CheckDimValueForDisposal | Aktualizováno |
| CalculateCurrentBalance | CalculateCurrentBalance | Aktualizováno |
| IncludeVATAmount | Přesunuto do tabulky 81 Gen. finančího deníku |
| CalcVATAmountFromVATEntry | CalcVATAmountFromVATEntry | Aktualizováno |
|  | TotalVATAmountOnJnlLines | Přidáno |
|  | SetGLRegReverse | Přidáno |
|  | GetGLSetup | Přidáno |
|  | ReadGLSetup | Přidáno |
|  | CheckSalesExtDocNo | Přidáno |
|  | CheckPurchExtDocNo | Přidáno |
|  | CheckGLAccDimError | Přidáno |
|  | GetCurrency | Přidáno |
|  | PostDtldAdjustment | Přidáno |
|  | GetNextEntryNo | Přidáno |
|  | GetNextTransactionNo | Přidáno |
|  | GetNextVATEntryNo | Přidáno |
|  | IncrNextVATEntryNo | Přidáno |
|  | IsNotPayment | Přidáno |
|  | IsTempGLEntryBufEmpty | Přidáno |
|  | IsVATAdjustment | Přidáno |
|  | IsVATExcluded | Přidáno |
|  | UpdateDimensions | Přidáno |
|  | UpdateDimensionsFromCustLedgEntry | Přidáno |
|  | UpdateDimensionsFromVendLedgEntry | Přidáno |
|  | UpdateTotalAmounts | Přidáno |
|  | CreateGLEntriesForTotalAmounts | Přidáno |

## Viz také
[Detaily návrhu: Změny v Codeunitě 12: Mapování globálních proměnných pro řádek finančího deníku](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]