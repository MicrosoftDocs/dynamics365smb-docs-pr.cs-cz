---
title: Finance - Czech Local Functionality | Microsoft Docs
description: This section describes Czech local functionality for Finance.
author: v-pejano

ms-service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: CZ, Czech, Finance, Posting
ms.date: 05/15/2019
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Finance

V České republice existují specifické funkce [!INCLUDE[prodshort](../../includes/prodshort.md)], které můžete využít pro sledování a spravování svých financí.

## Opravné účtování (červené storno)

Podle požadavků legislativy jsou náklady a výnosy obvykle účtovány pouze buď na stranu Má-dáti nebo Dal finančního účtu. Společnosti ve východní Evropě obvykle dodržují účetní zásady, podle kterých některé skladové a finanční transakce v hlavní knize musí být účtovány jako oprava. Důvodem je, že auditoři a finanční úřady provádějí účetní kontroly v souladu s tímto pravidlem. 

Cíl této funkcionality je:
- Umožnit hlavnímu účetnímu vynutit opravné účtování na požadovaných účtech hlavní knihy
- Umožnit hlavnímu účetnímu vynutit opravné účtování zásob (záporné položky transferů, účtování očekávaných nákladů)
- Umožnit hlavnímu účetnímu vynutit opravné účtování storna v dlouhodobém majetku
- Umožnit uživatelům opravné účtovaní pouze jedním kliknutím (finance, zásoby a účtování projektů)

## Statutární informace o společnosti

V současné době, kolují mnohé doklady vně i uvnitř společnosti. Místní právní předpisy stanovují minimální požadavky na takové doklady. Tyto požadavky můžeme zhruba rozdělit do tří skupin:
- Jména zástupců společnosti musí být uvedena na některých interních či externích dokladech
- Zápatí dokumentů – většina externích dokumentů musí obsahovat základní informace o společnosti v zápatích dokumentů, obvykle v jazyce partnerské společnosti
- Registrační čísla společnosti musí být viditelně uvedena v interních a externích dokumentech 

Tato funkce umožňuje uživatelům definovat zástupce společnosti a nastavit je jako generálního ředitele, hlavní účetní a finančního manažera pro použití v interních a externích dokladech. 
Uživatelé mohou definovat zápatí dokumentu v různých jazycích. Tato zápatí lze použít v různých sestavách a dokumentech.

Další registrační čísla společnosti a další registrační informace mohou být uloženy v Informacích o společnosti a používány v dokladech.

## Interní účetní doklady

Uživatelé provádějí účetní operace a musí mít možnost tisknout takové dokumenty s účetními operacemi, které vzhledem i obsahem vyhovují požadavkům legislativy. 
Uživatelé také chtějí tisknout dokumenty pro již zaúčtované účetní operace.
Z výše uvedených důvodů tato funkce poskytuje následující sestavy: 
- Finanční deník – test – sestava se používá pro tisk dokumentů z finančního deníku
- Obecný účetní doklad – sestava – se používá k tisku zaúčtovaných účetních operací

## Účetní výstupní doklady

Pro splnění nároků na výstupy odpovídající legislativním požadavkům a místním zvyklostem poskytuje tato funkcionalita následující sestavy: 
- Finanční deník
- Hlavní účetní kniha
- Kontační lístky
- Obratová předvaha dle glob. dimenze
- Otevřené věcné položky do data
- Inventura účtu do data
- Vyrovnání bankovního účtu
- Vyrovnání spojovacího konta
- Odsouhlasení DPH – finance
- Pozdržené platby
- Otevřené položky zákazníka k datu
- Otevřené položky dodavatelů k datu
- Saldo fiskálního roku – upravená standardní sestava 
- Předvaha podle období - upravená standardní sestava

## Účetní schémata - rozšíření 

Pro jednu z nejvíce používaných oblastí aplikace pro analýzu a reporting vyžadují východoevropské země následující vylepšení funkcionality standardních účetních schémat:
- Společný seznam výrazů – společný seznam výrazů obsahuje pojmenované řádky, které lze použít jako vzorce pro všechna účetní schémata. Toho je docíleno definováním jednoho účetního schématu jako společného seznamu výrazů s názvem Sdílené účetní schéma.
- Ukládání výsledků (současný stav) analýzy - toto vylepšení umožňuje uživateli ukládat výsledky analýzy provedené pomocí účetních schémat.
- Analýza vzorců – toto rozšíření umožňuje uživateli analyzovat výsledky vzorců. Analýza je nyní dostupná i pro Typ součtu - Vzorec. Analýza výsledku vzorce zobrazí uživateli nový formulář obsahující seznam prvků použitých pro výpočet a jejich popis.
- Další zdroje dat - kromě toho, že uživatelé mohou provádět analýzu na základě položek v hlavní knize, mohou nyní provádět i analýzy na základě položek DPH, položek zákazníků, položek dodavatelů a položek ocenění.

## Statutární výkazy

Společnosti musí vytvořit účetní závěrku v souladu se zákonem o účetnictví č. 563/1991.  Musí vytvořit rozvahu a výkaz zisků a ztrát.
Tato funkce poskytuje následující výkazy:

- Rozvaha
- Výkaz zisku a ztráty

Tyto výkazy používají účetní schémata s definovanou strukturou statutárních výkazů.

V názvu účetních schémat je v české verzi přidáno nové pole:
- Typ účetního schématu – Rozvaha nebo Výkaz zisku a ztráty

V řádku účetních schémat jsou v české verzi přidána nová pole:
- Korekce řady – odkaz na jiný řádek pro sestavení Rozvahy
- Typ Aktivní/Pasivní – Aktiva nebo pasiva pro sestavení Rozvahy
- Vypočti – Vždy, Nikdy, Při kladné, Při záporné

Rozvaha a Výkaz zisků a ztrát jsou často připravovány v šablonách souborů aplikace Excel s potřebným vzhledem pro vytištění výkazu. Uživatelé chtějí mít možnost mapovat definované účetní schémata do připravených šablon aplikace Excel.

Z výše uvedených důvodů tato funkce poskytuje nové nastavení šablon aplikace Excel a mapování položek výkazů. Na základě tohoto nastavení mohou uživatelé exportovat data účetních schémat do souboru aplikace Excel.

## Rozšířené účtování nedokončené výroby 

Česká legislativa používá při účtování nedokončené výroby následující nové finanční účty:
- Účet spotřeby
- Změna stavu nedokončené výroby
- Změna stavu výrobků

Tato funkce umožňuje správně provádět účtování nedokončené výroby a výroby dle českých účetních postupů. Díky ní je možno nastavit pro kombinace skladové lokace a účto skupiny zboží finanční účty pro spotřebu, změnu stavu nedokončené výroby i změnu stavu polotovarů a výrobků.
Nový systém účtování je používán u následujících transakcí:
- Účtování spotřeby v denících spotřeby 
- Účtování nákladů výrobních operací ve výstupních denících
- Dokončování výrobních zakázek

## Dodatečné finanční funkce

Následující tabulka obsahuje další informace o dodatečných finančních funkcích, které jsou k dispozici pro Českou republiku.


| Téma | Popis |
| :-------------------------------------------------------- | :----------------------------------------------------------- |
| [Uzávěrkové operace ](year-close-operations.md) | Aby bylo možné dodržet účetní předpisy na konci fiskálního roku, musí být některé účetní knihy uzavřeny nebo otevřeny. |
| [Vyrovnání věcných položek](general-ledger-entries-application.md) | Kromě použití položek zákazníka a dodavatele byla zavedena nová funkčnost aplikace věcných položek. Vyrovnání věcných položek se obvykle používá s cílem umožnit společnostem práci s dočasnými a převodovými účty ve financích. |
| [Aktualizace směnného kurzu](exchange-rate-update.md) | Možnost automatické aktualizace směnných kurzů z externí služby poskytované ČNB (Česká národní banka). |

## Viz také
[Česká lokální funkcionalita](czech-local-functionality.md)