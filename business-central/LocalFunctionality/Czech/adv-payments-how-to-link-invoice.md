---
title: Advance Payments activation and upgrade
description: This section describes Advance Payments Localization for Czech extension functionality.
author: v-pejano

ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: Czech, Advance Payments, Localization
ms.date: 10/01/2021
ms.reviewer: v-pejano
ms.author: v-pejano
---

# Propojení zálohové faktury s konečným dokladem 

## Použití zálohové faktury v konečné faktuře

Pro použití zálohové faktury v konečné faktuře postupujte následujícím způsobem:

1. Fakturu zadejte do systému obvyklým způsobem. Pokud chcete k faktuře připojit jednu či více záloh, proveďte tak z hlavičky faktury z pomocí akce **Propojit zálohovou fakturu**. 
2. Do zobrazené stránky **Vyrovnání zálohy** pomocí funkce **Nový** a rozkliknutím pole **Číslo zálohy** zobrazte seznam záloh dostupných pro přiřazení do faktury. Zobrazují se jen zálohy se stejným kódem měny a v takových částkách, které byly uhrazeny nejpozději k zúčtovacímu datu prodejní faktury. Potvrďte výběr zálohy a záloha přenese na stránku **Vyrovnání zálohy** pro propojení faktury a zálohy. 
Takto lze pokračovat dále ve výběru záloh. Kliknutím na další řádek stránky lze znovu prostřednictvím pole Číslo zálohy přidat do propojení další zálohy. 
3. V poli **Částka** můžete zadat, jaká částka a ze které zálohy má být fakturou čerpána. Je možné tak do faktury čerpat více záloh v částečných hodnotách.
4. Pokud je přiřazení záloh nastaveno tak, jak chce uživatel využít zálohy ve faktuře, potvrdí stránku tlačítkem **OK**.

Poznámka: 
- Záloha bude vždy čerpána do maximální možné hodnoty faktury, tzn. i když uživatel nesníží hodnotu čerpané zálohy a záloha bude hodnotu faktury převyšovat, záloha bude odečtena maximálně do hodnoty faktury.
- Pokud uživatel zvolí částečné čerpání zálohy, bude ze zálohy odpočtena jen příslušná nastavená část.
- Pokud uživatel zvolí částečné čerpání z více záloh a hodnota záloh k použití bude vyšší než hodnota faktury, systém automaticky odpočítá částky ze záloh podle data úhrady záloh.
- Pokud je přiřazení záloh nastaveno tak, jak chce uživatel využít zálohy ve faktuře, potvrdí stránku tlačítkem OK. 

## Informace o použití zálohové faktury v konečném dokladu

- V novém **FactBoxu** prodejní faktury v části **Použití prodejní zálohy** je zobrazen počet využitých záloh, jejich čísla, odkazy na DPH položky, a je zde vidět celková částka faktury po odpočtu záloh.
- Standardní statistika dokladu zálohy nezahrnuje. Je možné ale spustit náhled účtování, který zobrazí všechny položky, včetně položek záloh, které budou při účtování vznikat.

## Odpojení zálohové faktury z konečného dokladu

Pokud nemá být záloha využita na faktuře, je možné ji z propojení odebrat:

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](../../media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní zálohové faktury** a poté vyberte související odkaz.
2. Otevřete vybranou zálohovu fakturu, použijte akci **Propojit zálohovou fakturu**, která otevře stránku s propojenými zálohami. 
4. Na stránce můžete upravovat částky, příp. odebrat celý řádek se zálohou. Vždy je třeba zkontrolovat, zda je stránka v editovatelném módu a úprava řádků se zaznamená. 
5. Přes tlačítko výběru (tři tečky) zvolte **Odstranit** a potvrďte smazání řádky s přiřazenou zálohovou fakturou.

Po zaúčtování faktury se zálohou vzniká na záloze položka s Typem položky **Použití** v částce odečítané z faktury, a pokud byl k platbě proúčtován i zálohový daňový doklad, vzniká automaticky i položka **DPH použití** s odpočtem DPH. 

Daňový dobropis je možné vytisknout z Historie zálohy z položky typu **DPH použití**. 
Položka **DPH použití** vzniká se stejným datem a číslem dokladu jako prodejní faktura.


## Použití zálohové faktury vytvořené z objednávky

- Pokud je záloha vytvořena z objednávky, není pro využití zálohy z objednávky potřeba žádná úprava nastavení. 
- Pokud je k záloze vytvořen zálohový daňový doklad, při účtování faktury dojde automaticky i k oddanění zálohy a vzniku zálohového daňového dobropisu. 
- Stejně jako u faktury je ve **FactBoxu** objednávky **Použití prodejní zálohy** uveden počet propojených záloh, odkazy na DPH a celková částka faktury po odpočtu zálohy.
- Objednávku je možné dodat i fakturovat i v okamžiku, kdy záloha není k zúčtovacímu datu objednávky zaplacená. Uživatel je na tuto skutečnost upozorněn a může se rozhodnout, zda doklad zaúčtovat či ne.
- Pokud záloha vytvořená z objednávky není zaplacená a objednávka bude zaúčtována a vyfakturována, automaticky bude zrušeno propojení mezi objednávkou a zálohou a zálohu tak bude možné (po zaplacení) využít pro jinou konečnou fakturu.


## Viz také

[Zálohové platby pro Česko (rozšíření)](ui-extensions-advance-payments-localization-cz.md)  
[České lokální funkcionality](czech-local-functionality.md)  
[Finance](../../finance.md)
