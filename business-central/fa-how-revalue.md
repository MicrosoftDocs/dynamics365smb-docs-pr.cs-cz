---
title: Revalue Fixed Assets| Microsoft Docs
description: Learn how to adjust the value of fixed assets, recording new amounts as a write-down or appreciation, and post additional acquisition costs.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: sgroespe

---
# Přecenění dlouhodobého majetku
Přecenění dlouhodobého majetku se může skládat ze zhodnocení, snížení hodnoty nebo obecných úprav hodnot.

Když se hodnota dlouhodobého majetku zvýší, zaúčtujte do knihy odpisů řádek deníku s vyšší částkou, zhodnocením. Nová částka se zaznamená jako zhodnocení podle nastavení účtování dlouhodobého majetku.

Pokud se hodnota dlouhodobého majetku snížila, zaúčtujte do knihy odpisů řádek deníku s nižší částkou, znehodnocením. Nová částka se zaznamená jako znehodnocení podle nastavení účtování dlouhodobého majetku.

Indexace se používá k úpravě více hodnot dlouhodobého majetku, například podle obecných změn cen. Dávkovou úlohu **Indexace dlouhodobého majetku** lze použít ke změně různých částek, například částek znehodnocení a zhodnocení.

## Zaúčtování zhodnocení z finančního deníku dlouhodobého majetku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky dlouhodobého majetku** a poté vyberte související odkaz.
2. Vytvořte počáteční řádek deníku a vyplňte pole podle potřeby.
3. V poli **Typ účtování DM** vyberte **Přecenění**.
4. Vyberte akci **Vložit protiúčet  DM**. Druhý řádek deníku je vytvořen pro protiúčet, který je nastaven pro účtování zhodnocení.

   > [!NOTE]
   > Krok 4 funguje pouze v případě, že jste nastavili následující: Na stránce **Karta účto skupiny DM** je potřeba pro účto skupinu dlouhodobého majetku nastavit pole **Účet zhodnocení**, které musí obsahovat MD účet věcných položek a pole **Protiúčet  zhodnocení** musí obsahovat účet hlavní knihy, na který chcete zaúčtovat vyrovnávací položky. Pro více informací navštivte [Nastavení účto skupin dlouhodobého majetku](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Vyberte akci **Účtovat**.

## Učtování znehodnocení z finančního deníku dlouhodobého majetku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky dlouhodobého majetku** a poté vyberte související odkaz.
2. Vytvořte počáteční řádek deníku a podle potřeby vyplňte pole.
3. V poli **Typ účtování DM** vyberte **Znehodnocení**.
4. Vyberte akci **Vložit protiúčet  DM**. Druhý řádek deníku je vytvořen pro protiúčet, který je nastaven pro zaúčtování znehodnocení.

   > [!NOTE]
   > Krok 4 funguje pouze v případě, že jste nastavili následující: Na stránce **Karta účto skupiny DM** je potřeba pro účto skupinu dlouhodobého majetku nastavit pole **Účet znehodnocení**, které musí obsahovat Dal účet věcných položek a pole **Účet nákladů znehodnocení** musí obsahovat MD účet věcných položek, na který chcete zaúčtovat vyrovnávací položky. Pro více informací navštivte [Nastavení účto skupin dlouhodobého majetku](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Vyberte akci **Účtovat**.

## Provádění všeobecného přecenění dlouhodobého majetku
Indexace se používá k úpravě více hodnot dlouhodobého majetku, například podle obecných změn cen. Dávkovou úlohu **Indexace dlouhodobého majetku** lze použít ke změně různých částek, například částek znehodnocení a zhodnocení. Na stránce **Kniha odpisů** musí být zaškrtnuto políčko **Povolit indexaci**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Indexace dlouhodobého majetku** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole.
3. Vyberte tlačítko **OK**.

   Řádky přecenění jsou vytvořeny podle nastavení v kroku 2. Řádky jsou vytvořeny v deníku dlouhodobého majetku nebo v deníku dlouhodobého majetku v závislosti na šabloně a v dávkovém nastavení na stránce **Nastavení deníku DM**. Pro více informací navštivte [Nastavení obecných informací o dlouhodobém majetku](fa-how-setup-general.md).
4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Finanční deníky dlouhodobého majetku** a poté vyberte související odkaz.
5. Vyberte deník s dlouhodobým majetkem, který chcete přecenit, a pak zvolte akci **Položky**.
6. Zaškrtněte vytvořené položky a pak zvolte akci **Účtovat** pro zaúčtování deníku.

   > [!TIP]
   > Pokud jsou hodnoty indexu pouze pro účely simulace, můžete vytvořit speciální knihu odpisů pro jejich uložení. Tyto položky pak nebudou mít žádný vliv na ostatní odpisy.

## Zaúčtování dodatečných pořizovacích nákladů
Dodatečné pořizovací náklady na dlouhodobý majetek zaúčtujete stejným způsobem jako původní pořizovací cenu: z nákupní faktury nebo z deníku dlouhodobého majetku. Pro více informací navštivte [Pořízení dlouhodobého majetku](fa-how-acquire.md).

Pokud již byl odpis pro dlouhodobý majetek vypočten, zaškrtněte políčko **Odpis  nákladů pořízení**, které umožňuje, aby se dodatečné pořizovací náklady snížené o zůstatkovou hodnotu odpisovaly v poměru k částce, o kterou již byl dříve pořízený dlouhodobý majetek odepsán. Tím je zajištěno, že doba odpisu se nezmění.

Procento odpisů se vypočítá takto:

*P = (Odpisovaná částka celkem x 100) / Odpisovatelný základ*

*Odpisovaná částka = (P/100) x (Extra náklady na pořízení - Hodnota při vyřazení)*

Nezapomeňte zaškrtnout políčko **Odpisy  od zúčt.data DM** na faktuře, ve finančním deníku dlouhodobého majetku nebo v řádcích deníku dlouhodého majetku, aby se zajistilo, že se odpisy počítají od posledního data účtování dlouhodobého majetku do data účtování dodatečných pořizovacích nákladů.

### Příklad - účtování dodatečných nákladů na pořízení
Stroj je zakoupen 1. srpna 2000. Pořizovací cena je 4 800. Metoda odpisování je rovnoměrná po dobu čtyř let.

31. srpna 2000 je spuštěna dávková úloha **Výpočet odpisů**. Odpisy se počítají takto:

*Účetní hodnota x počet dní odpisu / celkový počet dnů odpisu = 4800 x 30 / 1440 = 100*

15. září 2000 je zaúčtována faktura za malování stroje. Částka faktury je 480.

Pokud jste vybrali zašrtávací políčko **Odpis  od zúčt.data DM** na faktuře před účtováním se provede následující výpočet:

15 dnů odpisů (od 01.09.2000 do 15.9.2000) se počítá takto:

*Účetní hodnota x počet dní odpisu / zbývající počet dnů odpisu = (4800 - 100) x 15 / 1410 = 50*

Pokud jste vybrali zašrtávací políčko **Odpis  nákladů pořízení** na faktuře před zaúčtováním, je proveden následující výpočet:

*Dodatečné pořizovací náklady jsou odepisovány ((150 x 100) / 4800) / 100 x 480 = 15*

Odpisovatelný základ je nyní *5280 = (4800 + 480)* a kumulovaný odpis je *165 = (100 + 50 + 15)*, což odpovídá 45 dnům odpisu celkových pořizovacích nákladů. To znamená, že aktivum bude zcela odepsáno během odhadované životnosti čtyř let.

Při spuštění dávkové úlohy **Výpočet odpisů** se 30.09.2000 provádí následující výpočet:

*Zbývající životnost, kterou lze odpisovat, jsou 3 roky, 10 měsíců a 15 dní = 1395 dní*

*Účetní hodnota je  (5280 - 165) = 5115*

*Odpisy za září 2000: 5115 x 15 / 1395 = 55.00*

*Celkový odpis = 165 + 55 = 220*

Pokud jste nevybrali zaškrtávací políčko **Odpisy  od zúčt.data DM** majetek by  ztratil 15 dní odpisů, protože dávková úloha **Výpočet odpisů** spuštěná 30.09.2000 by vypočítala odpisy od 15.09.2000 do 30.09.2000. To znamená, že při spuštění dávkové úlohy **Výpočet odpisů** 30.09.2000 je výpočet následující:

*Zbývající životnost je 3 roky, 10 měsíců a 15 dní = 1395 dní*

*Účetní hodnota je (4800 + 480 - 100 - 15) = 5165*

*Částka odpisu za září 2000: 5165 x 15 / 1395 = 55.54*

*Celkový odpis = 100 + 15 + 55.54 = 170.54*

## Viz také
[Dlouhodobý majetek](fa-manage.md)  
[Nastavení dlouhodobého majetku](fa-setup.md)  
[Finance](finance.md)  
[Začínáme](product-get-started.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
