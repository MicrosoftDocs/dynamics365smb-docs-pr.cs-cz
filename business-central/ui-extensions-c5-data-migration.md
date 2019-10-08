---
title: Používání rozšíření C5 Data Migration | Microsoft Docs
description: 'Toto rozšíření slouží k migraci zákazníků, dodavatelů, položek a účtů hlavní knihy z Microsoft Dynamics C5 2012 do Business Central.'
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'extension, migrate, data, C5, import'
ms.date: 10/01/2018
ms.author: bholtorf
---

# <a name="the-c5-data-migration-extension"></a>Rozšíření C5 Data Migration
Toto rozšíření usnadňuje migraci zákazníků, dodavatelů, položek a účtů hlavní knihy z Microsoft Dynamcis C5 2012 do [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lze také migrovat historické položky pro účty hlavní knihy.

> [!Note]
> Společnost v [!INCLUDE[d365fin](includes/d365fin_md.md)] nesmí obsahovat žádná data. Zároveň po spuštění migrace nevytvářejte zákazníky, dodavatele, položky nebo účty, dokud migrace neskončí.

## <a name="what-data-is-migrated"></a>Jaká data jsou migrována ?
Pro každou entitu se migrují následující data:

**Zákazníci**
* Kontakty  
* Lokace
* Země
* Dimenze zákazníka (oddělení, středisko, účel)
* Způsob dodávky
* Prodejce
* Platební podmínky
* Způsob platby
* Cenová skupina zákazníka
* Fakturační sleva zákazníka

Pokud migrujete účty, migrují se také následující data:

* Nastavení účto skupiny zákazníka
* List finančního deníku
* Otevřené transakce (položky zákazníka)

**Dodavatelé**
* Kontakty
* Lokace
* Země
* Dimenze dodavatele (oddělení, středisko, účel)
* Fakturační sleva
* Způsob dodávky
* Nákupčí
* Platební podmínky
* Způsob platby
* Fakturační sleva dodavatele

Pokud migrujete účty, migrují se také následující data:

* Nastavení účto skupiny dodavatele
* List finančního deníku
* Otevřené transakce (položky dodavatele)

**Položky**
* Lokace
* Země
* Dimenze položky (oddělení, středisko, účel)
* Prodejní řádkové slevy
* Skupina slev zákazníka
* Skupina slev zboží
* Prodejní cena
* Číslo tarifu
* Měrné jednotky
* Kód sledování zboží
* Cenová skupina zákazníka
* Kusovníky montáže

Pokud migrujete účty, migrují se také následující data:

* Nastavení účtování zásob
* Nastavení obecného účtování
* List deníku zboží
* Otevřené transakce (položky zboží)

> [!Note]
> Pokud existují otevřené transakce, které používají cizí měny, migrují se také směnné kurzy pro tyto měny. Ostatní směnné kurzy migrovány nejsou.

**Účetní osnova**  
* Standardní dimenze: Středisko, Nákladové středisko, Účel  
* Historické finanční transakce  

> [!Note]
> S historickými finančními transakcemi se zachází trochu jinak. Při migraci dat nastavíte parametr **Aktuální období**. Tento parametr určuje, jak zpracovat finanční transakce. Transakce po tomto datu se migrují jednotlivě. Transakce před tímto datem jsou agregovány na jeden účet a migrovány jako jedna částka. Řekněme například, že existují transakce v letech 2015, 2016, 2017, 2018 a do pole Aktuální období zadáte 01.01.2017. Pro každý finanční účet budou částky za transakce k 31. prosinci 2106 nebo dříve sloučeny do jediného řádku finančního deníku. Všechny transakce po tomto datu budou migrovány jednotlivě.

## <a name="file-size-requirements"></a>Požadavky na velikost souboru
Největší velikost souboru, který můžete nahrát do [!INCLUDE[d365fin](includes/d365fin_md.md)], je 150 MB. Pokud je soubor exportovaný z C5 větší, zvažte migraci dat pomocí více souborů. Například exportujte jeden nebo dva typy entit z C5, jako jsou například zákazníci a dodavatelé, do jednoho souboru, a poté exportujte zboží do jiného souboru atd. Soubory můžete v [!INCLUDE[d365fin](includes/d365fin_md.md)] importovat jednotlivě.

## <a name="to-migrate-data"></a>Migrace dat
Je třeba učinit jen pár kroků k exportu dat z C5 a jejich importu do [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

1. V C5 exportujte data pomocí funkce **Export databáze**. Poté odešlete exportovanou složku do komprimované (zip) složky.  
2. V [!INCLUDE[d365fin](includes/d365fin_md.md)] vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Migrace Dat** a poté zvolte **Migrace Dat**.  
3. Proveďte kroky v průvodci asistovanou instalaci. Ujistěte se, že jako zdroj dat jste zvolili **Import z Microsoft Dynamcis C5 2012**.  

## <a name="viewing-the-status-of-the-migration"></a>Zobrazení stavu migrace
Na stránce **Přehled migrace dat** můžete sledovat úspěšnost migrace. Stránka zobrazuje informace, jako je počet entit, které bude migrace zahrnovat, stav migrace a počet položek, které byly migrovány, a zda byly jejich migrace úspěšné. Ukazuje také počet chyb, umožňuje vám zjistit, co se pokazilo, a pokud je to možné, usnadňuje přístup k entitě a řešení jejích problémů. Další informace naleznete v další části tohoto tématu.  

> [!Note]
> Zatímco čekáte na výsledky migrace, musíte stránku aktualizovat, aby se zobrazily výsledky.

## <a name="how-to-avoid-double-posting"></a>Jak se vyhnout dvojímu účtování
Abychom se vyhnuli dvojímu účtování do hlavní knihy, pro otevřené transakce se používají následující rozvahové účty:  

* Pro dodavatele používáme A/P  účet z účto skupiny dodavatelů.  
* Pro zákazníky používáme A/R  účet z účto skupiny zákazníků.  
* U položek vytváříme nastavení obecného účtování tam, kde účet adjustace je účet určený jako účet inventáře v nastavení účtování zásob.  

## <a name="correcting-errors"></a>Opravy chyb
Pokud se něco pokazí a dojde k chybě, v poli **Stav** se zobrazí **Dokončeno s chybami** a v poli **Počet chyb** se zobrazí jejich počet. Chcete-li zobrazit seznam chyb, můžete otevřít stránku **Chyby dat migrace** výběrem:  

* Čísla v poli **Počet chyb** pro entitu.  
* Zvolením entity a potom akce **Zobrazit chyby**.  

Na stránce **Chyby dat migrace** můžete opravit chybu tak, že si vyberete chybovou zprávu a poté zvolíte **Upravit záznam**, čímž se zobrazí migrovaná data pro entitu. Pokud máte několik chyb k opravě, můžete použít možnost **Hromadné opravy chyb** a upravit entity v seznamu. Stále však musíte otevírat jednotlivé záznamy, pokud byla chyba způsobena související položkou. Například dodavatel nebude migrován, pokud má e-mailová adresa jednoho z jeho kontaktů neplatný formát.

Po opravě jedné nebo více chyb můžete zvolit **Migrovat** a migrovat pouze entity, které jste opravili, aniž byste museli migraci úplně restartovat.  

> [!Tip]
> Pokud jste opravili více než jednu chybu, můžete pomocí funkce **Vybrat více** vybrat více řádků pro migraci. Alternativně, pokud existují chyby, u kterých oprava není důležitá, můžete je vybrat a poté zvolit **Přeskočit výběr**.

> [!Note]
> Pokud máte položky, které jsou součástí kusovníku, možná je budete muset migrovat více než jednou, pokud původní položka není vytvořena před variantami, které na ni odkazují. Pokud je varianta položky vytvořena jako první, může odkaz na původní položku způsobit chybovou zprávu.  

## <a name="verifying-data-after-migrating"></a>Ověření dat po migraci
Jedním ze způsobů, jak ověřit, zda vaše data byla správně migrována, je podívat se na následující stránky v C5 a [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamcis C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]| Dávkové úlohy k použití |
|-----|-----|-----|
|Položky zákazníka| Finanční deníky| CUSTMIGR |
|Položky dodavatele| Finanční deníky| VENDMIGR|
|Položky zboží| Deníky zboží| ITEMMIGR |
|Věcné položky| Finanční deníky| GLACMIGR |

## <a name="stopping-data-migration"></a>Zastavení migrace dat
Migraci dat můžete zastavit výběrem **Zastavit všechny migrace**. Pokud tak učiníte, zastaví se také všechny čekající migrace.

## <a name="see-also"></a>Viz také
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] pomocí rozšíření](ui-extensions.md)  
[Začínáme](product-get-started.md)
