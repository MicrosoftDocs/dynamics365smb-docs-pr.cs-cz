---
title: Czech Local Functionality - Payables and Receivables | Microsoft Docs
description: This section describes local functionality - Payables and Receivables
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Receivables, Payables, Finance, CZ, Cash
ms.date: 12/30/2019
ms.reviewer: v-pejano
ms.author: v-makune
---

# Závazky a pohledávky

## Zápočty

Zákazníci společnosti jsou také často jejími dodavateli. V takových případech je běžné, že společnosti vyrovnají své pohledávky a závazky.

Seznam hlavních funkcionalit Zápočtů:  

- Pole **Saldo jako dodavatel / Saldo jako zákazník** na kartě zákazníka/ dodavatele – chcete-li zobrazit saldo jako dodavatel na kartě zákazníka a saldo jako zákazník na kartě dodavatele, musí uživatel nastavit obchodní vztah zákazníka a dodavatele s kontaktem, aby systému ukázal, že daná společnost je v aplikaci evidována jako dodavatel i jako zákazník, a že se jedná o jednu a tutéž společnost.
- **Nastavení zápočtů** – Číselná řada, Protiúčet zápočtu, atd.,
- **Karta zápočtu** – řádky k započtení,  
- Funkce – **Navrhni řádky zápočtu**, Vydání,
- **Dohoda o vzájemném zápočtu pohledávek a závazků**,
- **Účtování zápočtu** – je vytvořen Účtovaný zápočet a provedeno vyrovnání položek.

Položky k započítání lze vkládat ručně nebo automaticky z Karty zápočtu funkcí Navrhni řádky zápočtu.  Dále jsou k dispozici funkce pro označení položek k započítání a přepočtení salda.

K dispozici je pak i tisk Dohody o vzájemném zápočtu pohledávek a závazků dle České legislativy.

## Přepočet pohledávek a závazků (Úprava směnných kurzů)

Většina firem v České republice požaduje následující vylepšení, která mají být realizována v oblasti úpravy směnných kurzů při přepočtu pohledávek a závazků:

- Možnost řídit úpravu směnných kurzů samostatně pro bank. účty, zákazníky a dodavatele
- Možnost účtovat úpravu směnného kurzu v detailu nebo souhrnně dle měny
- Možnost spustit úpravu směnných kurzů jako simulaci (bez účtování) v testovacím režimu

Ve standardní sestavě Úprava směnných kurzů je nyní možné:

- Nastavit bankovní účet, zákazníka nebo dodavatele jako filtr
- Vybrat úpravu jen pro zákazníky nebo dodavatele nebo bankovní účty
- Zvolit testovací režim
- Vybrat sumarizaci položek
- Vybrat způsob přenosu dimenzí

Úprava směnných kurzů rovněž obsahuje změněný princip výpočtu pro realizované zisky a ztráty na základě Zákona o daních z příjmů. Tato funkce vypočítá realizovaný zisk nebo ztrátu proti naposledy upraveným částkám.
Tato funkce ve standardní verzi Microsoft[!INCLUDE[d365fin](../../includes/d365fin_md.md)] nejdříve odúčtuje nerealizovaný zisk nebo ztrátu a pak vypočítá realizovaný zisk nebo ztrátu. Výpočet je proveden proti částce v původním kurzu při zpracování platby a faktury.
Nový princip výpočtu zpracovává odchylky oproti aktuálně upravenému směnnému kurzu.
Úprava směnných kurzů byla rozšířena i o český modul zálohy.

## Více účtů pohledávek a závazků

Uživatelé často účtují operace jako nedobytné pohledávky či jiné typy operací pohledávek/závazků, které mají být zaznamenány v položkách zákazníků/dodavatelů, ale zároveň zaúčtovány na jiné účty pohledávek/závazků než jsou specifikovány v účto skupinách zákazníků a dodavatelů. Nejjednodušší způsob, jak umožnit takovou funkčnost, je povolit uživateli změnu účto skupiny zákazníka/dodavatele při účtování dílčí operace.

## Odsouhlasení pohledávek a závazků

Na konci každého fiskálního roku (nebo jiného období je-li požadováno) společnosti zasílají hlášení o stavu pohledávek zákazníkům a závazků dodavatelům, aby si navzájem sladili svoje záznamy. Zákazníci a dodavatelé buď hlášení potvrdí, nebo ho pošlou na základě svých vlastních informací s opravami zpět. Tato funkcionalita umožňuje uživatelům vytvořit sestavy odsouhlasení pohledávek a závazků v [!INCLUDE[d365fin](../../includes/d365fin_long_md.md)].

## Opravné prodejní doklady

Podle novelizace Zákona o DPH je nutné rozlišovat typy prodejních dobropisů. Tato funkce umožňuje uživatelům nastavit následující typy dobropisů:

- Opravný daňový doklad
- Interní oprava
- Daňový doklad insolvence

## Aktualizace kontaktů z ARES

ARES je zkratka pro Access to Register of Economic Subjects. ARES je informační systém umožňující získávání informací o ekonomických subjektech registrovaných v České republice.
Uživatel může http adresu služby ARES vyplnit v Nastavení služby ověření IČ.  
Aktualizaci z ARES můžete spustit z karty kontaktu, dodavatele nebo zákazníka na tlačítku v poli IČ. Můžete vyhledávat společnosti a rozhodnout, která pole v [!INCLUDE[d365fin](../../includes/d365fin_long_md.md)] zaktualizujete (název, adresa, město, PSČ).

## Nový design výstupních dokladů

Byla vytvořena nová sada tiskových sestav pro externí doklady společnosti.
Všechny doklady mají stejný vzhled (záhlaví, zápatí, typ a velikost písma, atd.)  

Kromě toho byly výstupní doklady rozšířeny o všechny náležitosti vyžadované českou legislativou:  

- IČ, DIČ
- Odpočet záloh s informacemi o faktuře a datu přijaté platby
- Tisk Specifikace DPH seskupené podle DPH identifikátoru
- Pojmenování opravných daňových dokladů na základě typu dobropisu
- Tisk dokladů vztahujících se k zálohám

### Seznam CZ sestav dokladů  

- Prodej - zálohová faktura CZ
- Prodejní záloha - faktura CZ
- Prodejní záloha - dobropis CZ
- Nákup - zálohová faktura CZ
- Nákupní záloha - faktura CZ
- Nákupní záloha - dobropis CZ
- Nákup - poptávka CZ
- Objednávka CZ
- Potvrzení objednávky vratky CZ
- Prodej - nabídka CZ
- Potvrzení objednávky CZ
- Prodej - faktura CZ
- Prodej - dobropis CZ
- Prodej - dodávka CZ
- Prodej - příjemka vratky CZ
- Upomínka CZ
- Penále CZ
- Servisní nabídka CZ
- Servisní zakázka CZ
- Nabídka servisní smlouvy CZ
- Servisní smlouva CZ
- Servis - faktura CZ
- Servis - dodávka CZ
- Servis - dobropis CZ

## Viz také  

[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](finance.md)
