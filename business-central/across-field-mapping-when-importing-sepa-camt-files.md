---
    title: Field Mapping When Importing SEPA CAMT Files | Microsoft Docs
    description: In European markets, you can import bank statement files in the regional SEPA standards (Single Euro Payments Area).
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
# Mapování polí při importu souborů SEPA CAMT
[!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje regionální standardy SEPA (Single Euro Payments Area) pro import SEPA bankovních výpisů (formát CAMT). Pro více informací navštivte [Používání rozšíření AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).

Samotný Standard SEPA CAMT má lokální varianty. Proto bude možná nutné změnit obecnou definici výměny dat (představovanou **kódem SEPA CAMT** na stránce **Definice výměny účtovaných dat**), aby se přizpůsobila místní variaci standardu. Následující tabulky ukazují mapování element-k-poli pro tabulky 81, 273 a 274 v implementaci SEPA CAMT v [INCLUDE[d365fin](includes/d365fin_md.md)].

Informace o vytváření nebo úpravě definic výměny dat naleznete v [Nastavení definice výměny dat](across-how-to-set-up-data-exchange-definitions.md).

## CAMT mapování dat na pole v tabulce finančního deníku (81)

| Cesta prvku | Element zprávy | Datový typ | Popis | Identifikátor záporného znaménka | Číslo pole | Název pole |
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
| Stmt/Ntry/Amt | Amount | Decimal | Částka peněz v položce hotovost | 13 | Amount |
| Stmt/Ntry/CdtDbtInd | CreditDebitIndicator | Text | Označuje, zda je položka dal nebo položkou má dáti | DBIT | 13 | Amount |
| Stmt/Ntry/BookgDt/Dt | Date | Date | Datum zaúčtování položky na účet v knihách obsluhovatele účtu | 5 | Posting Date |
| Stmt/Ntry/BookgDt/DtTm | DateTime | DateTime | Datum a čas, kdy je položka zaúčtována na účet v knihách obsluhovatele účtu | 5 | Posting Date |
| Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm | Name | Text | Jméno strany, která dluží peněžní částku (konečnému) věřiteli | 1221 | Payer Information |
| Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd | Unstructured | Text | Informace poskytnuté k tomu, aby umožnily vyrovnání / odsouhlasení položky se zbožím, které má platba uhradit, jako jsou obchodní faktury v systému pohledávek, v nestrukturované podobě | 8 | Popis |
| Stmt/Ntry/AddtlNtryInf | AdditionalEntryInformation | Text | Další informace o položce | 1222 | Transaction Information |

## CAMT mapování dat na pole v tabulce vyrovnání (273)

| Cesta prvku | Element zprávy | Datový typ | Popis | Identifikátor záporného znaménka | Číslo pole | Název pole |
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
| Stmt/CreDtTm | CreationDateTime | Date | Datum a čas, kdy byla zpráva vytvořena | 3 | Statement Date |
| Stmt/Bal/Amt | Amount | Decimal | Částka vyplývající z částek, které mají být připsané pro všechny položky MD a dal | 4 | Statement Ending Balance |

## CAMT mapování dat na pole v tabulce řádků odsouhlasení bank. účtu(274)

| Cesta prvku | Element zprávy | Datový typ | Popis | Identifikátor záporného znaménka | Číslo pole | Název pole |
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
| Stmt/Ntry/Amt | Amount | Decimal | Částka peněz v položce hotovost | 7 | Statement Amount |
| Stmt/Ntry/CdtDbtInd | CreditDebitIndicator | Text | Označuje, zda je položka dal nebo položkou má dáti | DBIT | 7 | Statement Amount |
| Stmt/Ntry/BookgDt/Dt | Date | Date | Datum zaúčtování položky na účet v knihách obsluhovatele účtu | 5 | Transaction Date |
| Stmt/Ntry/BookgDt/DtTm | DateTime | DateTime | Datum a čas, kdy je položka zaúčtována na účet v knihách obsluhovatele účtu | 5 | Transaction Date |
| Stmt/Ntry/ValDt/Dt | Date | Date | Datum, kdy budou aktiva k dispozici vlastníkovi účtu v případě platební transakce, nebo přestane být k dispozici vlastníkovi účtu v případě zadání debetu | 12 | Value Date |
| Stmt/Ntry/ValDt/DtTm | DateTime | DateTime | Datum a čas, kdy se aktiva zpřístupní majiteli účtu v případě platební transakce, nebo přestanou být k dispozici majiteli účtu v případě zadání debetu. | 12 | Value Date |
| Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm | Name | Text | Jméno strany, která dluží peněžní částku (konečnému) věřiteli | 15 | Payer Information |
| Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd | Unstructured | Text | Informace poskytnuté k tomu, aby umožnily vyrovnání / odsouhlasení položky se zbožím, které má platba uhradit, jako jsou obchodní faktury v systému pohledávek, v nestrukturované podobě | 6 | Popis |
| Stmt/Ntry/AddtlNtryInf | AdditionalEntryInformation | Text | Další informace o položce | 16 | Transaction Information |

Prvky v uzlu **Ntry**, které jsou importovány do aplikace [!INCLUDE[d365fin](includes/d365fin_md.md)], ale nejsou namapovány na žádná pole, jsou uložena v **Účtování sloupce výměna dat**. Uživatelé si mohou tyto prvky zobrazit z **Deníku odsouhlasení plateb**, z **Vyrovnání platby** a ze stránky **Odsouhlasení bankovního účtu** zvolením akce **Detaily řádku bankovního výpisu**. Pro více informací navštivte [Automatické odsouhlasení plateb](receivables-how-reconcile-payments-auto-application.md).
## Viz také
[Nastavení výměny dat](across-set-up-data-exchange.md)  
[Elektronická výměna dat](across-data-exchange.md)  
[Používání rozšíření AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Použití schémat XML k přípravě definic datových výměn](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Odsouhlasení plateb pomocí automatického vyrovnání](receivables-how-reconcile-payments-auto-application.md)  
