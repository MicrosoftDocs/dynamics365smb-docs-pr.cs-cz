---
title: "Handling Missing Option Values"
description: Learn how to prevent full synchronization from failing because the options differ in mapped fields.
author: bholtorf

ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 02/03/2020
---

# Zpracování chybějících hodnot možností
[!INCLUDE[d365fin](includes/cds_long_md.md)] obsahuje pouze tři pole sady možností, která obsahují hodnoty možností, které můžete mapovat na [!INCLUDE[d365fin](includes/d365fin_md.md)] typu Option<!-- Option type, not enum? @Onat can you vertify this? --> pro automatickou synchronizaci. Během synchronizace jsou nemapované možnosti ignorovány a chybějící možnosti jsou připojeny k související tabulce [!INCLUDE[d365fin](includes/d365fin_md.md)] a přidány do systémové tabulky **Volba mapování CDS**, kterou můžete zpracovat ručně později. Například přidáním chybějících možností v obou produktech a aktualizací mapování. Tato část popisuje, jak to funguje.

Stránka **Mapování tabulky integrace** obsahuje tři mapy pro pole, která obsahují jednu nebo více mapovaných hodnot možností. Po úplné synchronizaci obsahuje stránka  **Volba mapování CDS** obsahuje nemapované možnosti ve třech polích.

| Záznam | Hodnota možnosti | Titulek hodnoty možnosti |
|----------------------------|--------------|----------------------|
| Platební podmínky: NET30 | 1 | Netto 30 |
| Platební podmínky: 2%10NET30 | 2 | 2% 10; Netto 30 |
| Platební podmínky: NET45 | 3 | Netto 45 |
| Payment Terms: NET60 | 4 | Netto 60 |
| Způsob dodávky: FOB | 1 | FOB |
| Způsoby dodávky: BEZPOPLATKU | 2 | Bez poplatku |
| Přepravce: VZDUCEHM | 1 | VZDUCHEM |
| Přepravce: DHL | 2 | DHL |
| Přepravce: FEDEX | 3 | FedEx |
| Přepravce: UPS | 4 | UPS |
| Přepravce: POŠTA | 5 | Poštovní zásilky |
| Přepravce: FULLLOAD | 6 | Plně naložen |
| Přepravce: BUDEVOLAT | 7 | Bude telefonovat |

Obsah stránky **Volba mapování CDS**  je založen na hodnotách výčtu v tabulce **Účet CDS**. V [!INCLUDE[d365fin](includes/cds_long_md.md)], jsou následující pole na entitě účtu mapována do polí v záznamech zákazníků a dodavatelů:

- **Adresa 1: Přepravní podmínky** datového typu Enum, kde jsou hodnoty definovány následovně:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Adresa 1: Způsob dopravy** datového typu Enum, kde jsou hodnoty definovány následovně:

```
enum 5336 "CDS Shipping Agent Code"
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Platební podmínky** datového typu Enum, kde jsou hodnoty definovány následovně:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Všechny výčty [!INCLUDE[d365fin](includes/d365fin_md.md)] jsou mapovány na sady voleb v [!INCLUDE[d365fin](includes/cds_long_md.md)].

### Rozšíření sady možností v [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Vytvořte nové AL rozšíření.

2. Přidejte rozšíření Enum pro možnosti, které chcete rozšířit. Ujistěte se, že používáte stejnou hodnotu.

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Při rozšíření výčtu [!INCLUDE[d365fin](includes/cds_long_md.md)]musíte použít stejné hodnoty ID možnosti z [!INCLUDE[d365fin](includes/d365fin_md.md)]. V opačném případě se synchronizace nezdaří.

> Prvních deset znaků nových názvů hodnot a titulků musí být jedinečné. Například dvě možnosti s názvem "Převod 20 pracovních dnů" a "Převod 20 kalendářních dnů" způsobí chybu, protože obě mají stejné první 10 znaků, "Transfer 2". Pojmenujte je například "TRF20 WD" a "TRF20 CD."

### Aktualizace Možnosti mapování [!INCLUDE[d365fin](includes/cds_long_md.md)]
Nyní můžete znovu vytvořit mapování voleb mezi [!INCLUDE[d365fin](includes/cds_long_md.md)] a zánamy [!INCLUDE[d365fin](includes/d365fin_md.md)].

Na stránce **Mapování tabulky integrace**vyberte řádek mapování **Platební podmínky** a poté zvolte **Synchronizovat upravené záznamy**. Stránka **Volba mapování CDS** je aktualizována s přidanými záznamy níže.

| Záznam | Hodnota možnosti | Titulek hodnoty možnosti |
|--------------------------------|----------------|----------------------|
| Platební podmínky: NET30 | 1 | Netto 30 |
| Platební podmínky: 2%10NET30 | 2 | 2% 10; Netto 30 |
| Platební podmínky: NET45 | 3 | Netto 45 |
| Payment Terms: NET60 | 4 | Netto 60 |
| **Platební podmínky: CASH PAYME** | **779800001** | **Platba v hotovosti** |
| **Platební podmínky: PREVOD** | **779800002** | **Převod** |

Tabulka **Platební podmínky** [!INCLUDE[d365fin](includes/d365fin_md.md)] bude mít nové záznamy pro volby v [!INCLUDE[d365fin](includes/cds_long_md.md)]. V následující tabulce jsou nové možnosti tučným písmem . Řádky kurzívou představují všechny možnosti, které lze nyní synchronizovat. Zbývající řádky představují možnosti, nejsou používány a budou ignorovány během synchronizace. Můžete je odebrat nebo rozšířit možnosti CDS stejnými jmény.

| Kód | Výpočet splatnosti | Výpočet skonto data | Sleva % | Výp.  Platba skonta v dobropisu | Popis |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 DNY | 10D |                           | 0. | NEPRAVDA | Čistých 10 dní |
| 14 DNY | 14D |                           | 0. | NEPRAVDA | Čistých 14 dní |
| 15 DNY | 15D |                           | 0. | NEPRAVDA | Čistých 15 dní |
| 1M(8D) | 1M | 8D | 2. | NEPRAVDA | 1 Měsíc/2% 8 dnů |
| 2 DNY | 2D |                           | 0. | NEPRAVDA | Čisté 2 dny |
| *2%10NET30* |                      |                           | 0. | NEPRAVDA |                   |
| 21 DNY | 21D |                           | 0. | NEPRAVDA | Čistý 21 dní |
| 30 DNY | 30D |                           | 0. | NEPRAVDA | Čistých 30 dní |
| 60 DNY | 60D |                           | 0. | NEPRAVDA | Čistých 60 dní |
| 7 DNU | 7D |                           | 0. | NEPRAVDA | Čistých 7 dní |
| ***CASH PAYME*** |                      |                           | 0. | NEPRAVDA |                   |
| CM | CM |                           | 0. | NEPRAVDA | Aktuální měsíc |
| COD | 0D |                           | 0. | NEPRAVDA | Dobírka |
| *NET30* |                      |                           | 0. | NEPRAVDA |                   |
| *NET45* |                      |                           | 0. | NEPRAVDA |                   |
| *NET60* |                      |                           | 0. | NEPRAVDA |                   |
| ***PREVOD*** |                      |                           | 0. | NEPRAVDA |                   |

## Viz také
