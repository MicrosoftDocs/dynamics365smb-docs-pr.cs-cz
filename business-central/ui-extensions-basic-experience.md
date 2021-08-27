---
    title: Basic Experience Extension | Microsoft Docs
    description: This extension is a modernized alternative to Microsoft Dynamics C5.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: C5, financials, extension
    ms.date: 04/01/2021
    ms.author: bholtorf


---
# Rozšíření Basic Experience
Pokud používáte Microsoft Dynamics C5, mohou vám partneři společnosti Microsoft s přechodem na modernější řešení založené na [!INCLUDE[prod_short](includes/prod_short.md)], takže si můžete i nadále užívat stejné zjednodušené funkce jako Dynamics C5 .

Toto rozšíření je určeno pro malé firmy a může podporovat až tři uživatele. Pokud potřebujete více uživatelů, musíte upgradovat na [!INCLUDE[prod_short](includes/prod_short.md)] a odinstalujte toto rozšíření.

> [!NOTE]
> Od této chvíle je toto rozšíření k dispozici pouze pro zákazníky v Dánsku a na Islandu.

## Co je k dispozici
Následující tabulka popisuje možnosti, které jsou k dispozici při instalaci rozšíření Basic Experience.

| Oblasti | Funkcionalita |
|---------|---------|
| **Hlavní kniha** | Základní finance, Účetní schémata, Dlouhodobý majetek, Správa banky, Vyrovnávání banky, Platby, Inkaso, Dimenze, Více měn, Rozpočty, Workflow, Správa dokladů/OCR, Konsolidace, Neomezené společnosti |
| **Pohledávky/Prodej** | Základní pohledávky, fakturace prodeje, prodejní slevy, ceny, DPH, správa kontaktů |
| **Závazky/Nakup** | Základní závazky, Fakturace nákupu |
| **Správa projektů** | Projekty, Ocenění projektu, Pracovní výkazy, Přiřazení, Úkoly, Zdroje |
| **Zásoby** | Základní zásoby, náhrady zboží, křížové odkazy zboží |

## Začínáme
Toto rozšíření se trochu liší od většiny a při jeho instalaci a nastavení budete potřebovat pomoc od partnera společnosti Microsoft. Jen abyste věděli, co můžete očekávat, zde je pohled na vysokou úroveň toho, co partner Microsoftu udělá.

1. Vytvoří nového [!INCLUDE[prod_short](includes/prod_short.md)] tenanta. Může to být buď zkušební verze, nebo verze CSP.
2. Přidání alespoň jednoho uživatele do účtu Azure Active Directory, který je přiřazen k licenci Basic Experience.
3. Odebere všechny společnosti, včetně ukázkové společnosti Cronus.
4. Vytvoří novou společnost, která neobsahuje žádná ukázková data ani nastavení.
5. Přidá balíček **Demo RapidStart**. <!--what does the pockage contain?-->
6. Stáhněte si a nainstalujte rozšíření Basic Experience ze služby AppSource.

## Migrace dat
Převeďte svá data Dynamics C5. Po instalaci rozšíření Basic Experience bude mít partner společnosti Microsoft prázdnou společnost. Snadný způsob, jak přesunout data z Dynamics C5 do Basic Experience, je použít rozšíření Migrace dat C5, které je součástí [!INCLUDE[prod_short](includes/prod_short.md)]. Rozšíření migruje zákazníky, dodavatele, zboží a vaše hlavní účty a jejich položky.

## Viz také
[Rozšíření C5 Data Migration

[!INCLUDE[footer-include](includes/footer-banner.md)]