---
title: Czech Local Functionality - Fixed Assets | Microsoft Docs
description: This section describes Czech local functionality - Fixed Assets
author: ACMartinKunes

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: Czech, finance, CZ, Fixed Assets
ms.date: 12/30/2019
ms.reviewer: v-pejano
ms.author: v-makune
---

# Dlouhodobý majetek

## Daňové odpisy dlouhodobého majetku
Funkcionalita daňového odepisování dlouhodobého majetku počítá a účtuje daňové odpisy v souladu se Zákonem o dani z příjmu (Zákon č. 586/1992 §26 - §33). Obsahuje zvláštní nastavení pro daňové odpisové skupiny, kde lze zadávat dobu a metodu odepisování, odpisové sazby a koeficienty pro nové odpisové metody daňových odpisů dlouhodobého majetku. 

Každý dlouhodobý hmotný majetek náleží do odpisové skupiny. Tyto skupiny určují minimální dobu odpisu a parametry používané pro výpočet odpisů.
K dispozici jsou následující metody odpisování dlouhodobého hmotného majetku (DM) pro daňové účely:

- Lineární – Tato metoda je založena na pořizovací hodnotě a procentu (přímka).
- Zrychlené – Tato metoda je založena na účetní hodnotě a koeficientu (klesající zůstatek).
- Lineární založené na pořizovací hodnotě a procentu (Lineární pro nehmotný majetek).

Každý dlouhodobý majetek je zařazen do určité odpisové skupiny. Tyto skupiny určují minimální dobu odepisování a parametry, které jsou využívány k výpočtu odpisů.  

## Výpočet odpisů v Dlouhodobém majetku

Vzhledem k českým právním předpisům je nutné vypočítávat daňové odpisy z odpisovatelného základu, který se mohou lišit od pořizovací ceny. Podle požadavků by měla být odpisová základna, podle české metody odpisování s klesajícím zůstatkem pro druhý a následující rok životnosti dlouhodobého majetku, vypočtena podle nového vzorce definovaného zákonem o dani z příjmu.
Byly provedeny změny ve výpočtu odpisované částky pomocí metody zrychleného odpisování pro druhé a následující roky životnosti dlouhodobého majetku podle výše uvedeného vzorce. Daňové odpisy se počítají ročně a volba počet dní  platnosti se doporučuje pro výpočet správné částky odpisu.

## Přerušení odepisování 

Funkcionalita Přerušení odepisování (na základě zákona o dani z příjmu Zákon č. 586/1992 §26 část 8) umožňuje přerušit odepisování pro vybraný dlouhodobý majetek a zadané období.  Systém stanoví odpisový plán po skončení doby přerušení.
K dispozici jsou následující metody odpisování dlouhodobého hmotného majetku pro daňové účely: 

- Lineární
- Pravidelné
- Zrychlené
- Lineární pro nehmotný majetek
- Vylepšené metody odpisování a metody rovnoměrného způsobu odpisování k vyskladnění podprocesů z plánu odpisů končí po skončení odpisového období.

Uživatel může otevřít knihu odpisů DM a vyplnit pole Přerušit odpisování a Přerušit odepisování do. Zachovat poslední  datum odpisu určuje, zda chcete udržovat Plán odpisů.

## Dvou krokové pořízení dlouhodobého majetku

Při získávání dlouhodobého majetku je nutno v českém účetnictví provést dva kroky. Pokud společnost obdrží fakturu za pořízení dlouhodobého majetku, musí být zaúčtována. Použití dlouhodobého majetku se účtuje už od okamžiku jeho prvního použití. Jak pořízení, tak i vydání k používání je vyžadováno a spojeno s věcmi položkami. Dlouhodobý majetek není odpisován, dokud není vydán k používání.

Pro tento způsob použijte typ účtování Vlastní 2 pro první krok (Pořízení) a typ účtování Pořízení dlouhodobého majetku pro krok druhý (Vydání k použití). Chcete-li začít používat tuto funkci, zaškrtněte políčko Pořízení dlouhodobého majetku, zahrnuté v Nastavení DM, jako Vlastní 2.
Hodnota Custom 2 je v Češtině přejmenovaná z "Vlastní 2" na "Pořízení" pro správnou identifikaci a intuitivnější porozumění.

## Účtování o vyřazení majetku

České účetní standardy vyžadují specifické účtování, když je hmotný majetek vyřazován nebo prodán.  Po prodeji nebo zaúčtování dlouhodobého majetku (DM), účtování o vyřazení majetku zajistí, že hodnota dlouhodobého majetku zůstane stejná jako hodnota získaná po odpisu.

Dlouhodobý majetek zůstává nezměněn i po vydání k použití. Pokud je dlouhodobý majetek pravidelně odepisován, odečte se příslušná částka z pořizovacích nákladů v okamžiku vyřazení. Částka slada je aktuální hodnota dlouhodobého majetku.

V knize odpisů zaškrtněte políčko Odpovídající věcné položky při vyřazení, aby byla tato funkce funkční. Vyberte zaškrtávací políčko Odpovídající věcné položky při vyřazení, pro zachování souladu mezi věcnými položkami a položkami DM.

## Různé typy účtování vyřazení a údržby 

V českém účetnictví je ale nutné účtovat různé druhy vyřazení a údržby DM na různé finanční účty. Standardní funkcionalita nabízí pouze jeden způsob účtování likvidace a údržby.

Pro tyto účely je nově doplněna tabulka – Rozšířená účto skupina DM. Tato tabulka umožňuje pro každou Účto skupinu DM nastavit: 

- Účtování vyřazení na různé účty v kombinaci s kódem příčiny použitým při vyřazení
- Účtování údržby na různé účty v kombinaci s kódem údržby použitým při účtování

## Klasifikace dlouhodobého majetku

### Kódy klasifikace: 

Zákon o dani z příjmu 586/1992 Dlouhdobého majetku podle klasifikace produkce CZ-CPA a podle klasifikace stavebních činností CZ-CC. Byla přidána nová tabulka Kód klasifikace a pole Kód klasifikace na kartě dlouhodobého majetku. Toto pole se používá pro klasifikaci DM do daňové skupiny.

## Sestavy umístění dlouhodobého majetku a Historie majetku

Tato funkce umožňuje rozšířené sledování změn v umístění dlouhodobého majetku včetně odpovědných osob.
Přidáním této funkce mohou uživatelé ovládat historii polohy dlouhodobého majetku a historii odpovědných osob za dlouhodobý majetek.
Tato funkce také poskytuje sestavy pro ověření společnosti, kde se nachází konkrétní DM / se nacházel nebo komu je / byla přiřazen.
Aby bylo možné povolit sledování Umístění DM a Odpovědný zaměstnanec (dále jako Historie DM), musí uživatel nejprve povolit tuto funkci v okně Nastavení DM zaškrtnutím políčka Historie dlouhodobého majetku. Po povolení Historie DM v Nastavení DM může uživatel začít sledovat změny v Umístění DM a v Odpovědných zaměstnancích - tyto změny jsou uloženy v tabulce Položka historie DM.

Položky historie DM: 
- Ukládají změny v evidenci DM
- Obsahují časové a uživatelské razítko změny

Byly přidány nové sestavy pro dokumentaci transakcí a historie:
- Přiřazení/uvolnění DM
- Historie DM

## Sestavy dlouhodobého majetku

Pro splnění nároků na výstupy odpovídající legislativním požadavkům a místním zvyklostem poskytuje tato funkce následující sestavy:

- **Karta DM** – sestava kombinuje data ze standardního seznamu DM a sestavy podrobností DM, seskupuje podrobnosti pro knihu odpisů DM. DM
- **Sestava pořízení DM** – sestava se vytiskne,  jakmile je přijat konkrétní dlouhodobý majetek k použití. Tyto dokument musí být podepsané zástupci společnosti.
- **Sestava vyřazení DM** – sestava se vytiskne, pokud je určitý dlouhodobý majetek vyřazen nebo poškozen.
- **Dlouhodobý majetek – analýza fin. účtu** – uživatel může tuto sestavu použít k porovnání s finančním účtem.
- **Dlouhodobý majetek – analýza  2** – uživatel může definovat 3 sloupce pro datum, 4 sloupce pro pole množství a pole skupina celkem a zvolit export do Excelu.
- **Dlouhodobý majetek – porovnání   odpisových knih** – uživatel může zvolit 2 knihy odpisů pro srovnání.
- **Seznam fyzické inventury DM** – společnosti jsou povinny odsouhlasit fyzický stav dlouhodobého majetku a jeho účetní hodnoty za účelem přípravy finančního výkazu.
- **Inventurní seznam DM** – vytiskne inventurní seznam DM pro odpovědného zaměstnance, nebo pro kód umístění DM.

Pro Českou republiku byly upraveny následující standardní sestavy (celkem skupina celkem, atd.):
- Analýza dlouhodobého majetku
- Dlouhodobý majetek – úč.hodn.01
- Dlouhodobý majetek – úč.hodn.02
- Dlouhod. majetek – oček. hodnota
- Finanční analýza dlouhodobého majetku
- Analýza údržby dlouhodobého majetku

## Viz také
[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](finance.md)
