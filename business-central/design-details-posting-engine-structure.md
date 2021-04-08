---
    title: Design Details - Posting Engine Structure | Microsoft Docs
    description: Posting interface and some other functions in codeunit 12 use posting engine functions to prepare and insert general ledger entry and VAT entry records. The posting engine is also responsible for general ledger register creation.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Struktura enginu účtování
Zúčtovací rozhraní a některé další funkce v codeunitě 12 používají funkce účtovacího modulu k přípravě a vložení záznamů o položkách hlavní knihy a položkách DPH. Zúčtovací modul je také zodpovědný za vytvoření žurnálu hlavní knihy.

Funkce v následující tabulce poskytují standardní rámec pro navrhování postupů účtování (such as Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry, and Reverse) a výhradní přístup ke tabulce 17 Věcné položky.

| Rutina | Popis |
|-------------|---------------------------------------|  
| StartPosting | Inicializuje vyrovnávací paměť pro účtování TempGLEntryBuf, uzamkne tabulky Věcné položky a Položky DPH a inicializuje Účetní období, Žurnál DPH a Směnný kurz. Mělo by být voláno pouze jednou, pak je NextEntryNo roven 0. |
| ContinuePosting | Zkontroluje a zaúčtuje nerealizovanou DPH pro předchozí zvýšení transakce NextTransactionNo a připraví účtování dalšího řádku. |
| FinishPosting | Dokončí účtování vložením Věcných položek z dočasné vyrovnávací paměti do tabulky databáze. Vždy se používá společně se StartPosting. Kontroluje nesrovnalosti. |
| InitGLEntry | Používá se k inicializaci nové Věcné položky do finančního deníku. Vrací se GLEntry jako parametr. |
| InitGLEntryVAT | Stejné jako InitGLEntry, také přiřazuje číslo protiúčtu a SummarizeVAT. |
| InitGLEntryVATCopy | Podobně jako InitGLEntryVAT, ale také navíc kopíruje data účto skupin z Položek DPH před SummarizeVAT. |
| InsertGLEntry | Jediná funkce, která vloží věcné položky do globální tabulky TempGLEntryBuf. Tuto funkci vždy používejte pro vložení. |
| CreateGLEntry | Provede InitGLEntry, přiřadí další částku měny a pak provede InsertGLEntry. Nahradí několik řádků kódu jedním voláním funkce. |
| CreateGLEntryBalAcc | Stejné jako CreateGLEntry, ale také přiřazuje Typ protiúčtu |
| CreateGLEntryVAT | Stejné jako CreateGLEntry, ale s dodatečným zpracováním pro účto skupiny a uložením do dočasné tabulky DPH:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);` |
| CreateGLEntryVATCollectAdj | Stejné jako CreateGLEntry, ale s dodatečným úpravou a uložením do dočasné tabulky DPH:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);` |
| CreateGLEntryFromVATEntry | Stejné jako CreateGLEntry, ale také kopíruje účtoskupiny z položek DPH |

## Viz také
[Detaily návrhu: Struktura rozhraní účtování](design-details-posting-interface-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]