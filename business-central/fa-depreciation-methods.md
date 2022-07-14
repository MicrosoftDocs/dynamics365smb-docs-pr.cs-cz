---
title: Depreciation Methods for Fixed Assets
description: Learn about the different built-in methods to depreciate or write-down fixed assets in the default version of Business Central which includes eight methods.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 07/05/2021
ms.author: edupont

---
# Metody odpisů dlouhodobého majetku

Ve výchozí verzi [!INCLUDE [prod_short](includes/prod_short.md)] je k dispozici osm metod odpisování:

* Lineární
* Zrychlený 1
* Zrychlený 2
* ZR1/LI
* ZR2/LI
* Definováno uživatelem

   > [!NOTE]  
   > Určete vlastní metodu odpisu definováním tabulek odpisů. Pro informace o použití uživatelem definované metody odpisování navštivte [Nastavení uživatelem definované metody odpisů](fa-how-setup-user-defined-depreciation-method.md).
* Manuální

   > [!NOTE]  
   > Tuto metodu použijte pro aktiva, která nepodléhají odpisům, například pozemky. Do deníku dlouhodobého majetku je nutné zadat odpisy. Dávková úloha **Výpočet odpisů** vynechá dlouhodobá aktiva, která používají tuto metodu odpisování.
* Pololetní konvence

   > [!NOTE]  
   > Při použití této metody se dlouhodobý majetek odpisuje každý rok stejnou částkou.

## Lineární odpisy

When you use the straight-line method, you must specify one of the following options in the fixed asset depreciation book:

* Doba odpisování (roky nebo měsíce) nebo konečný termín odpisování
* Pevné roční procento
* Pevná roční částka
* Odpisové období

### Odpisové Období

Pokud zadáte dobu odpisování (počet odpisových let, počet odpisových měsíců nebo konečný termín odepisování), program použije pro výpočet odpisové částky následující vzorec:

*Odpisovaná částka = ((Účetní hodnota - Hodnota při vyřazení) x Počet dní odpisu) / zbývající dny odpisu*

Zbývající dny odpisu se počítají jako počet dnů odpisování minus počet dní mezi počátečním datem odpisu a posledním datem zadání dlouhodobého majetku.

Účetní hodnota může být snížena o zaúčtované zhodnocení, odpis, vlastní 1 nebo vlastní 2 částky v závislosti na tom, zda pole **Zahrnout do výpočtu  odpisů** je deaktivováno a je aktivováno pole **Část účetní hodnoty** na stránce **Nast.typu účtování DM**. Tento výpočet zajišťuje, že dlouhodobý majetek je plně odepsán v den ukončení odpisů.

### Pevná roční procentní sazba

Zadáte-li pevnou roční procentní sazbu, program vypočítá odpisovou část dle následujícího vzorce:

*Odpisovaná částka = (Lineární % x Odpisovatelný základ x Počet dní  odpis.) / (100 x 360)*

### Pevná roční částka

Pokud zadáte pevnou roční částku, program použije tento vzorec pro výpočet částky odpisů:

*Odpisovaná částka = (fixovaná odpisovaná částka x počet dní odpisu) / 360*

### Příklad - Lineární odpis

Dlouhodobý majetek má pořizovací cenu 100 000 LM. Odhadovaná doba života je osm let. Dávková úloha **Výpočet odpisůy** se spouští dvakrát ročně.

V tomto příkladu položka dlouhodobého majetku vypadá takto:

| Datum | Typ zaúčtování DM | Dny | Částka | Účetní hodnota |
| --- | --- | --- | --- | --- |
| 01.01.20 | Pořizovací cena | (Datum zahájení odpisování) | 100 000,00 | 100 000,00 |
| 30.06.20 | Odpisy | 180 | -6 250,00 | 93 750,00 |
| 31.12.20 | Odpisy | 180 | -6 250,00 | 87 500,00 |
| 30.06.21 | Odpisy | 180 | -6 250,00 | 81 250,00 |
| 31.12.21 | Odpisy | 180 | -6 250,00 | 75 000,00 |
| 30.06.27 | Odpisy | 180 | -6 250,00 | 6 250,00 |
| 31.12.27 | Odpisy | 180 | -6 250,00 | 0 |

## Zrychlený odpis 1

Jedná se o zrychlenou metodu odpisování, která přiděluje největší část nákladů na majetek v prvních letech své životnosti. Používáte-li tuto metodu, musíte zadat pevný roční procentní podíl.

Vzorec pro výpočet odpisových částek je:

*Odpisovaná částka = (Zrychlený % x Počet dní odpisu x Základ odpisu) / (100 x 360)*

Odpisovatelný základ se vypočítá jako účetní hodnota snížená o zaúčtované odpisy od počátku běžného fiskálního roku.

Zaúčtovaná částka odpisu může obsahovat položky s různými typy zaúčtování (odpis, vlastní1 a vlastní2) zaúčtované od počátečního data aktuálního fiskálního roku. Tyto typy zaúčtování jsou zahrnuty v částce zaúčtovaného odpisu, pokud jsou zaškrtnuta pole **Typ odpisu** a **Část účetní hodnoty** na stránce **Nast.typu účtování DM**.

### Příklad - Zrychlený odpis 1

Dlouhodobý majetek má pořizovací cenu 100 000 LM. Pole **Zrychlený %** je 25. Dávková dávková úloha **Výpočet odpisůy** se spouští dvakrát ročně.

Následující tabulka ukazuje, jak vypadají položky dlouhodobého majetku.

| Datum | Typ zaúčtování DM | Dny | Částka | Účetní hodnota |
| --- | --- | --- | --- | --- |
| 01.01.20 | Pořizovací cena | (Datum zahájení odpisování) | 100 000,00 | 100 000,00 |
| 30.06.20 | Odpisy | 180 | -12 500,00 | 87 500,00 |
| 31.12.20 | Odpisy | 180 | -12 500,00 | 75 000,00 |
| 30.06.21 | Odpisy | 180 | -9 375,00 | 65 625,00 |
| 31.12.21 | Odpisy | 180 | -9 375,00 | 56 250,00 |
| 30.06.22 | Odpisy | 180 | -7 031,25 | 49 218,75 |
| 31.12.22 | Odpisy | 180 | -7 031,25 | 42 187,50 |
| 30.06.23 | Odpisy | 180 | -5 273,44 | 36 914,06 |
| 31,12.23 | Odpisy | 180 | -5 273,44 | 31 640,62 |
| 30.06.24 | Odpisy | 180 | -3 955,08 | 27 685,54 |
| 31.12.24 | Odpisy | 180 | -3 955,08 | 23 730,46 |

Metoda výpočtu:

* Rok 1: *25 % ze 100 000 = 25 000 = 12 500 + 12,500*

* Rok 2: *25 % ze 75 000 = 18 750 = 9 375 + 9,375*

* Rok 3: *25 % z 56 250 = 14 062,50 = 7 031,25 + 7 031,25*

Výpočet pokračuje, dokud účetní hodnota neodpovídá konečnému počtu zaokrouhlení částky nebo hodnotě, kterou zadáte.

## Zrychlený odpis 2

Metody Zrychlený odpis 1 a Zrychlený odpis 2 vypočítají stejnou celkovou částku odpisů pro každý rok. Pokud však spustíte dávkovou úlohu **Výpočet odpisů** více než jednou ročně, metoda Zrychlený odpis 1 bude mít za následek stejné částky odpisů pro každé odpisové období. Metoda Zrychlený odpis 2 na druhé straně bude mít za následek odpisové částky, které klesají pro každé období.

### Příklad - Zrychlený odpis 2

Dlouhodobý majetek má pořizovací cenu 100 000 LM. Pole **Zrychlený %** je 25. Dávková dávková úloha **Výpočet odpisůy** se spouští dvakrát ročně. Položky knihy dlouhodobého majetku vypadají takto:

| Datum | Typ zaúčtování DM | Dny | Částka | Účetní hodnota |
| --- | --- | --- | --- | --- |
| 01.01.20 | Pořizovací cena | (Datum zahájení odpisování) | 100 000,00 | 100 000,00 |
| 30.06.20 | Odpisy | 180 | -13 397,46 | 86 602,54 |
| 31.12.20 | Odpisy | 180 | -11 602,54 | 75 000,00 |
| 30.06.21 | Odpisy | 180 | -10 048,09 | 64 951,91 |
| 31.12.21 | Odpisy | 180 | -8 701,91 | 56 250,00 |

Metoda výpočtu:

* *BV* = Účetní hodnota
* *ND* = Počet dní odpisu
* *DBP* = Zrychlený %
* *P* = *DBP*/100
* *D* = *ND*/360

Vzorec pro výpočet odpisových částek je:

*DA* = *BV* x (1 – (1 – P)<sup>D</sup>)

Hodnoty odpisování jsou:

| Datum | Výpočet |
| --- | --- |
| 30.06.20 | DA = 100 000,00 x (1 -(1 - 0,25)<sup>0,5</sup>) = 13 397,46 |
| 31.12.20 | DA = 86 602,54 x (1 - (1 - 0,25)<sup>0,5</sup>) = 11 602,54 |
| 30.06.21 | DA = 75 000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 10 048,09 |
| 31.12.21 | DA = 64 951,91 x (1 - (1 - 0,25)<sup>0,5</sup>) = 8 701,91 |

## Odpisy DB1/SL

DB1/SL is an abbreviated combination of Declining-Balance 1 and Straight-Line. Výpočet pokračuje, dokud účetní hodnota neodpovídá konečnému počtu zaokrouhlení částky nebo hodnotě, kterou zadáte.

Dávková úloha **Výpočet odpisů** vypočítá přímou částku a klesající částku zůstatku, ale pouze část větší z obou částek je převedena do deníku.

K výpočtu klesajícího zůstatku můžete použít různá procenta.

Pokud použijete tuto metodu, musíte zadat odhadovanou životnost a procento klesajícího zůstatku na stránce **Knihy odpisů DM**.

### Příklad - Odpisy DB1-SL

Dlouhodobý majetek má pořizovací cenu 100 000 LM. Na stránce **Knihy odpisů DM** obsahuje pole **Zrychlený %** hodnotu 25 a pole **Počet roků odpisování** obsahuje hodnotu 8. Dávková dávková úloha **Výpočet odpisůy** se spouští dvakrát ročně.

Položky knihy dlouhodobého majetku vypadají takto:

| Datum | Typ zaúčtování DM | Dny | Částka | Účetní hodnota |
| --- | --- | --- | --- | --- |
| 01.01.20 | Pořizovací cena | (Datum zahájení odpisování) | 100 000,00 | 100 000,00 |
| 30.06.20 | Odpisy | 180 | -12 500,00 | 87 500,00 |
| 31.12.20 | Odpisy | 180 | -12 500,00 | 75 000,00 |
| 30.06.21 | Odpisy | 180 | -9 375,00 | 65 625,00 |
| 31.12.21 | Odpisy | 180 | -9 375,00 | 56 250,00 |
| 30.06.22 | Odpisy | 180 | -7 031,25 | 49 218,75 |
| 31.12.22 | Odpisy | 180 | -7 031,25 | 42 187,50 |
| 30.06.23 | Odpisy | 180 | -5 273,44 | 36 914,06 |
| 31,12.23 | Odpisy | 180 | -5 273,44 | 31 640,62 |
| 30.06.24 | Odpisy | 180 | -3 955,08 | 27 685,54 |
| 31.12.24 | Odpisy | 180 | -3 955,08 | 23 730,46 |
| 30.06.25 | Odpisy | 180 | -3 955,08 | 19 775,38 SL |
| 31.12.25 | Odpisy | 180 | -3 955,08 | 15 820,30 SL |
| 30.06.26 | Odpisy | 180 | -3 955,08 | 11 865,22 SL |
| 31.12.26 | Odpisy | 180 | -3 955,07 | 7 910,15 SL |
| 30.06.27 | Odpisy | 180 | -3 955,08 | 3 955,07 SL |
| 31.12.27 | Odpisy | 180 | -3 955,07 | 0,00 SL |

`SL` za účetní hodnotou znamená, že byla použita lineární metoda.

Způsob výpočtu:

* Rok 1 (2020):

   *Částka zrychleného odpisu: 25 % ze 100 000 = 25 000 = 12 500 + 12 500*

   *Částka lineárního odpisu = 100 000 / 8 = 12 500 = 6 250 + 6 250*

   Klesající částka se používá, protože je to větší částka.

* Rok 5 (2025):

   *Částka zrychleného odpisu: 25 % z 23 730,46 = 4 943,85 = 2 471,92 + 2 471,92*

   *Částka lineárního odpisu = 23 730,46/3 = 7 910,15 = 3 995,07 + 3 995,08*

   Částka lineárního odpisu se používá, protože je to částka větší.

## Odpisy podle půlroční konvence

Metoda půlroční konvence se použije pouze v případě, že jste zaškrtli pole **Použít pololetní konvenci** na stránce **Kniha odpisů DM**.

Tuto metodu odpisování lze použít v souvislosti s následujícími metodami odpisování v programu:

* Lineární
* Zrychlený 1
* ZR1/LI

Při použití pololetní konvence má dlouhodobý majetek šest měsíců odpisů v prvním fiskálním roce bez ohledu na obsah pole **Počáteční datum odpisování**.

> [!NOTE]  
> Odhadovaná doba životnosti dlouhodobého majetku, která zbývá po prvním fiskálním roce, bude vždy obsahovat pololetí při použití metody pololetní konvence. Aby tedy byla metoda půlroční konvence správně aplikována, musí pole **Poslední datum odpisování** na stránce **Kniha odpisů DM** vždy obsahovat datum, které je přesně šest měsíců před konečným datem fiskálního roku, ve kterém bude dlouhodobý majetek plně odepsán.

### Příklad - Odpisy pololetní konvence

Dlouhodobý majetek má pořizovací cenu 100 000 LM. **Počáteční datum odpisování** je 01.03.20. Odhadovaná životnost je pět let, takže **Poslední datum odpisování** musí být 30.06.25. Dávková úloha **Výpočet odpisů** se spouští každoročně. Tento příklad je založen na kalendářním fiskálním roce.

Položky knihy dlouhodobého majetku vypadají takto:

| Datum | Typ zaúčtování DM | Dny | Částka | Účetní hodnota |
| --- | --- | --- | --- | --- |
| 01.03.20 | Pořizovací cena | (Datum zahájení odpisování) | 100 000,00 | 100 000,00 |
| 31.12.20 | Odpisy | 270 | -10 000,00 | 90 000,00 |
| 31.12.21 | Odpisy | 360 | -20 000,00 | 70 000,00 |
| 31.12.22 | Odpisy | 360 | -20 000,00 | 50 000,00 |
| 31,12.23 | Odpisy | 360 | -20 000,00 | 30 000,00 |
| 31.12.24 | Odpisy | 360 | -20 000,00 | 10 000,00 |
| 31.12.25 | Odpisy | 180 | -10 000,00 | 0,00 |

## Příklad - Odpisy DB1/SL s použitím půlroční konvence

Dlouhodobý majetek má pořizovací cenu 100 000 LM. **Počáteční datum odpisování** je 01.11.20. Odhadovaná životnost je pět let, takže **Poslední datum odpisování** musí být 30.06.25. Na stránce **Knihy odpisů DM** obsahuje pole **Zrychlený %** hodnotu 40. Dávková úloha **Výpočet odpisů** se spouští ročně. Tento příklad je založen na kalendářním fiskálním roce.

Položky knihy dlouhodobého majetku vypadají takto:

| Datum | Typ zaúčtování DM | Dny | Částka | Účetní hodnota |
| --- | --- | --- | --- | --- |
| 01.11.20 | Pořizovací cena | (Datum zahájení odpisování) | 100 000,00 | 100 000,00 |
| 31.12.20 | Odpisy | 60 | -20 000,00 | 80 000,00 |
| 31.12.21 | Odpisy | 360 | -32 000,00 | 48 000,00 |
| 31.12.22 | Odpisy | 360 | -19 200,00 | 28 800,00 |
| 31,12.23 | Odpisy | 360 | -11 520,00 | 17 280,00 |
| 31.12.24 | Odpisy | 360 | -11 520,00 | 5 760,00 SL |
| 31.12.25 | Odpisy | 180 | -5 760,00 | 0,00 SL |

`SL` za účetní hodnotou znamená, že byla použita lineární metoda.

Způsob výpočtu:

* Rok 1:

   *Částka zrychleného odpisu = Částka za celý rok = 40 % ze 100 000 = 40 000.* Tedy za půl roku 40 000 / 2 = 20 000

   *Lineární částka odpisu = Částka za celý rok = 100 000 / 5 = 20 000.* Tedy za půl roku = 20 000 / 2 = 10 000

   Klesající částka se používá, protože je to větší částka.

* Rok 5 (2024):

   *Částka zrychleného odpisu = 40 % z 17 280,00 = 6 912,00*

   *Částka lineárního odpisu = 28 800 / 1,5 = 11 520,00*

   Částka lineárního odpisu se používá, protože je to částka větší.

## Kopírování položek do dalších odpisových knih

Pokud máte tři odpisové knihy, B1, B2 a B3, a chcete duplikovat položky z B1 na B2 a B3, můžete zaškrtnout políčko **Část seznamu duplikací** na kartách odpisové knihy pro B2 a B3. To může být užitečné, pokud je odpisová kniha B1 integrována s hlavní knihou a používá finanční deník dlouhodobého majetku a odpisové knihy B2 a B3, které nejsou integrovány do hlavní knihy a používají deník dlouhodobého majetku.

Při zadání položky v B1 ve finančním deníku dlouhodobého majetku a zaškrtnutí do pole  **Použít seznam duplikátů** program duplikuje záznam v knize B2 a B3 v deníku dlouhodobého majetku, když je záznam zaúčtován.

> [!NOTE]  
> Nemůžete duplikovat ve stejném deníku a listu deníku, ze kterých duplikujete. Pokud zaúčtujete položky dlouhodobého majetku ve finančním deníku, můžete je duplikovat v deníku dlouhodobého majetku nebo ve finančním deníku dlouhodobého majetku pomocí jiné dávky.

> [!NOTE]  
> V finančním deníku DM a deníku dlouhodobého majetku nelze použít stejnou číselnou řadu. Při zaúčtování položek do finančního deníku dlouhodobého majetku musíte nechat pole **Číslo dokladu** prázdné Pokud do pole zadáte číslo, bude číslo duplikováno v deníku dlouhodobého majetku. Před zaúčtováním deníku budete muset ručně změnit číslo dokladu.

## Viz také

[Dlouhodobý majetek](fa-manage.md)    
[Nastavení dlouhodobého majetku](fa-setup.md)    
[Finance](finance.md)    
[Příprava na podnikání](ui-get-ready-business.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
