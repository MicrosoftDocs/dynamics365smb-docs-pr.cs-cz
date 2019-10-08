---
title: Používání rozšíření C5 Data Migration | Microsoft Docs
description: 'Toto rozšíření slouží k migraci zákazníků, dodavatelů, položek a účtů hlavní knihy z Microsoft Dynamics C5 2012 do Financials.'
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: 'extension, migrate, data, C5, import'
ms.date: 11/21/2017
ms.author: bholtorf
---

# <a name="the-c5-data-migration-extension-for-business-central"></a>Rozšíření Migrace dat C5 pro Business Central
Toto rozšíření usnadňuje migraci zákazníků, dodavatelů, položek a účtů hlavní knihy z Microsoft Dynamcis C5 2012 do [!INCLUDE[d365fin](includes/d365fin_md.md)]. Lze také migrovat historické položky pro účty hlavní knihy.

> [!Note]
> Společnost v [!INCLUDE [d365fin](includes/d365fin_md.md)] nesmí obsahovat žádná data. Zároveň po spuštění migrace nevytvářejte zákazníky, dodavatele, položky nebo účty, dokud migrace neskončí.

## <a name="what-data-is-migrated"></a>Jaká data jsou migrována ?
Pro každou entitu se migrují následující data:

**Zákazníci**
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
* Měrné jednotkay
* Kód sledování zboží
* Cenová skupina zákazníka

Pokud migrujete účty, migrují se také následující data:

* Nastavení účtování zásob
* Nastavení obecného účtování
* List deníku zboží
* Otevřené transakce (položky zboží)

> [!Note]
> Pokud existují otevřené transakce, které používají cizí měny, migrují se také směnné kurzy pro tyto měny. Ostatní směnné kurzy migrovány nejsou.

## <a name="to-migrate-data"></a>Migrace dat
Je třeba učinit jen pár kroků k exportu dat z C5 a jejich importu do [!INCLUDE [d365fin](includes/d365fin_md.md)]:  

1. V C5 exportujte data pomocí funkce **Export databáze**. Poté odešlete exportovanou složku do komprimované (zip) složky.  
2. V [!INCLUDE [d365fin](includes/d365fin_md.md)] zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Vyhledat stránku nebo sestavu"), zadejte **Migrace dat** a pak vyberte **Migrace dat**.  
3. Proveďte kroky v průvodci asistovanou instalaci. Ujistěte se, že jako zdroj dat jste zvolili **Import z Microsoft Dynamcis C5 2012**.  

> [!Note]
> Společnosti často přidávají pole pro přizpůsobení C5 pro jejich konkrétní obor podnikání, které  [!INCLUDE [d365fin](includes/d365fin_md.md)] nepřenáší data z vlastních polí. Migrace také selže, pokud máte více než 10 vlastních polí.

## <a name="viewing-the-status-of-the-migration"></a>Zobrazení stavu migrace
Na stránce **Přehled migrace dat** můžete sledovat úspěšnost migrace. Stránka zobrazuje informace, jako je počet entit, které bude migrace zahrnovat, stav migrace a počet položek, které byly migrovány, a zda byly jejich migrace úspěšné. Ukazuje také počet chyb, umožňuje vám zjistit, co se pokazilo, a pokud je to možné, usnadňuje přístup k entitě a řešení jejích problémů. Další informace naleznete v další části tohoto tématu.  

> [!Note]
> Zatímco čekáte na výsledky migrace, musíte stránku aktualizovat, aby se zobrazily výsledky.

## <a name="correcting-errors"></a>Opravy chyb
Pokud se něco pokazí a dojde k chybě, v poli **Stav** se zobrazí **Dokončeno s chybami** a v poli **Počet chyb** se zobrazí jejich počet. Chcete-li zobrazit seznam chyb, můžete otevřít stránku **Chyby dat migrace** výběrem:  

* Čísla v poli **Počet chyb** pro entitu.  
* Zvolením entity a potom akce **Zobrazit chyby**.  

Na stránce **Chyby dat migrace** můžete opravit chybu tak, že si vyberete chybovou zprávu, poté zvolíte **Upravit záznam**, čímž otevřete stránku zobrazující migrovaná data pro entitu. Po opravě jedné nebo více chyb můžete zvolit **Migrovat** a migrovat pouze entity, které jste opravili, aniž byste museli migraci úplně restartovat.  

> [!Tip]
> Pokud jste opravili více než jednu chybu, můžete pomocí funkce **Vybrat více** vybrat více řádků pro migraci. Alternativně, pokud existují chyby, u kterých oprava není důležitá, můžete je vybrat a poté zvolit **Přeskočit výběr**.

> [!Note]
> Pokud máte položky, které jsou součástí kusovníku, možná je budete muset migrovat více než jednou, pokud původní položka není vytvořena před variantami, které na ni odkazují. Pokud je varianta položky vytvořena jako první, může odkaz na původní položku způsobit chybovou zprávu.  

## <a name="verifying-data-after-migrating"></a>Ověření dat po migraci
Jedním ze způsobů, jak ověřit, zda vaše data byla správně migrována, je podívat se na následující stránky v C5 a [!INCLUDE [d365fin](includes/d365fin_md.md)].


| Microsoft Dynamcis C5 2012 | [!INCLUDE [d365fin](includes/d365fin_md.md)] |
|----------------------------|----------------------------------------------|
|      Položky zákazníka      |               Finanční deníky               |
|       Položky dodavatele       |               Finanční deníky               |
|        Položky zboží        |                Deníky zboží                 |

V [!INCLUDE [d365fin](includes/d365fin_md.md)] je dávka pro migrovaná data pojmenována **C5MIGRATE**.

## <a name="stopping-data-migration"></a>Zastavení migrace dat
Migraci dat můžete zastavit výběrem **Zastavit všechny migrace**. Pokud tak učiníte, zastaví se také všechny čekající migrace.

## <a name="see-also"></a>Viz také
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] pomocí rozšíření](ui-extensions.md)  
[Vítejte v [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  
