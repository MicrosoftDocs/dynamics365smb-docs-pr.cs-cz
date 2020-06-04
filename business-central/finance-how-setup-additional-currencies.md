---
title: Setting Up Additional Currencies| Microsoft Docs
description: Your general ledger is set up to use your local currency (LCY), and another currency is set up as an additional currency, with a current exchange rate assigned.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 01/13/2020
ms.author: sgroespe

---
# Nastavení přídavné měny pro hlášení
Vzhledem k tomu, že společnosti působí ve stále více zemích nebo oblastech, je důležitější, aby byly schopny kontrolovat a vykazovat finanční údaje ve více než jedné měně.

Finance jsou nastaveny tak, aby používaly lokální měnu (LM), ale můžete je nastavit tak, aby používaly i jinou měnu s přiřazeným aktuálním směnným kurzem. Označením druhé měny jako takzvané druhé měny pro vykazování v [!INCLUDE[d365fin](includes/d365fin_md.md) ] bude automaticky zaznamenávat částky v lokální měne i v této druhé měně pro vykazování na každou věcnou položku a další položky, například položky DPH.

> [!WARNING]
> Funkce doplňkové měny vykazování by neměla být použita jako základ pro účetní závěrky. Nejedná se o nástroj, který může provádět převody zahraničních dceřiných účetních závěrek v rámci konsolidace společnosti. Přídavnou měnu pro hlášení lze použít pouze k přípravě sestav v jiné měně, jako by tato měna byla lokální měnou společnosti.

## Zobrazení sestav a částek v přídavné měně
Použití přídavné měny pro hlášení může pomoci procesu vykazování pro společnost v následujících případech:

- Společnosti v zemích nebo oblastech mimo EU, které mají vysoký podíl transakcí se společnostmi  v EU. V takovém případě může společnost ze zemí mimo EU rovněž chtít podávat zprávy v eurech, aby její finanční zprávy byly pro obchodní partnery EU použitelnější.
- Společnosti, které také chtějí zobrazit přehledy v mezinárodně obchodovanější měně než ve své vlastní lokální měně.

Několik finančních výkazů je založeno na věcných položkách. Chcete-li zobrazit data sestavy v přídavné měně, jednoduše zaškrtněte pole **Zobrazi  částky v příd. měně pro hlášení** na záložce **Možnosti** na příslušné sestavě věcných položek.

## Úprava směnných kurzů
Vzhledem k tomu, že směnné kurzy neustále kolísají, musí být pravidelně upravovány další měnové ekvivalenty ve vašem systému. Pokud tyto úpravy nejsou provedeny, částky, které byly převedeny ze zahraničních (nebo dodatečných) měn a zaúčtovány do hlavní knihy v lokální měně, mohou být zavádějící. Kromě toho musí být denní položky zaúčtované před vstupem denního směnného kurzu do aplikace aktualizovány po zadání denních informací o směnném kurzu. Dávková úloha **Úprava směnných kurzů** se používá k úpravě směnných kurzů zaúčtovaných položek zákazníků, dodavatelů a bankovních účtů. Může také aktualizovat další částky měny vykazování u položek hlavní knihy. Pro víc informací navštivte [Aktualizace směnných kurzů](finance-how-update-currencies.md) .

## Nastavení přídavné měny pro hlášení
Chcete-li nastavit další měnu pro hlášení, je nutné postupovat takto:

- Určete účty hlavní knihy pro účtování úprav směnného kurzu.
- Určete metodu úpravy směnného kurzu pro všechny účty hlavní knihy.
- Zadejte způsob úpravy směnného kurzu pro položky DPH.
- Aktivujte další měnu pro hlášení.

### Určení účtů hlavní knihy pro účtování úprav směnného kurzu

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Měny** a vyberte související odkaz.
2. Na stránce **Měny** vyplňte následující pole pro dodatečnou měnu.

| Pole | Popis |
|---------------------------------|---------------------------------------|  
| **Účet realizovaných zisků** | Účet hlavní knihy, na který budou zaúčtovány kurzové zisky pro měnové úpravy mezi LM a přídavnou měnou vykazování. |
| **Účet realizovaných ztrát** | Účet hlavní knihy, na který budou zaúčtovány kurzové ztráty pro měnové úpravy mezi LM a přídavnou měnou vykazování. |
| **Reziduální účet zisků** | Účet hlavní knihy, na který jsou zaúčtovány zbývající částky, které jsou zisky, pokud účtujete v oblasti aplikace hlavní knihy v LM i v přídavné měně pro hlášení. |
| **Reziduální účet ztrát** | Účet hlavní knihy, na který jsou zaúčtovány zbývající částky, které jsou ztrátami, pokud účtujete v oblasti aplikace hlavní knihy v LM i v přídavné měně pro hlášení. |

> [!NOTE]  
> Zbytkové částky mohou nastat, když [!INCLUDE[d365fin](includes/d365fin_md.md)] zaokrouhlí debetní a kreditní částky, které byly převedeny z LM na přídavnou měnu vykazování.

Pro každý účet hlavní knihy je nutné určit, jak budou částky hlavní knihy pro tento účet upraveny o kolísání směnného kurzu mezi LM a přídavnou měnou pro hlášení.

### Určení metody úpravy směnného kurzu pro všechny účty hlavní knihy
1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Účetní osnova** a vyberte související odkaz.
2. Na stránce **Účetní osnova** vyberte příslušný účet a pak zvolte tlačítko **Upravit**.
3. Na stránce **Karta finančního účtu** vyberte příslušnou metodu v poli **Úprava sm. kurzu**.

   Pokud účtujete v přídavné měně pro hlášení, zadejte v poli **Úprava směnného kurzu**, jak bude tento účet hlavní knihy upraven o kolísání směnného kurzu mezi LM a přídavnou měnou. V následující tabulce jsou uvedeny možnosti výběru.

   | Pole | Popis |
   |----------------------------------|---------------------------------------|  
   | **Bez úpravy** | Na účtu hlavní knihy se neprovede žádná úprava směnného kurzu. Toto je výchozí možnost.<br /><br /> **NOTE:** Tato možnost by měla být vybrána, pokud je vždy pevný směnný kurz mezi LM a přídavnou měnou. |
   | **Úprava částky** | Částka LM je upravena o kurzové zisky nebo ztráty. Kurzové zisky nebo ztráty jsou zaúčtovány na účet hlavní knihy v poli **Částka** a na účty, které jste zadali pro zisky nebo ztráty v polích **Účet realizovaných finančních zisků** a **Účet realizovaných finančních ztrát** na stránce **Měny**. |
   | **Úprava částy v přídavné měně** | Přídavná měna vykazování je upravena o kurzové zisky nebo ztráty. Kurzové zisky nebo ztráty jsou zaúčtovány na účet hlavní knihy v poli **Částka v přídavné měně** a na účty, které jste zadali pro zisky nebo ztráty v polích **Účet realizovaných finančních zisků** a **Účet realizovaných finančních ztrát** na stránce **Měny**. |

   Kurzové zisky a ztráty jsou zaúčtovány při spuštění dávkové úlohy **Úprava směnných kurzů**. V této dávkové úloze je směnný kurz úpravy identifikován na stránce **Směnné kurzy** a potom se porovnají částky v polích **Částka** a **Částka v přídavné měně** v položce hlavní knihy, aby se zjistilo, zda existuje kurzový zisk nebo ztráta. Dávková úloha používá možnost, kterou vyberete v poli **Úprava směnného kurzu** k určení, jak vypočítat a účtovat zisky nebo ztráty směnného kurzu pro účty hlavní knihy.

4. Zavřete stránku **Karty finančního účtu**.

### Určení metody úpravy směnného kurzu pro položky DPH
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení financí** a vyberte související odkaz.
2. Stránce **Nastavení financí** vyberte odpovídající metodu v poli **Úprava směnného kurzu DPH**.
3. Pokud účtujete v přídavné měně pro vykazování, můžete v poli **Úprava směnného kurzu DPH** určit, jak budou účty nastavené pro účtování DPH na stránce **Nastavení účtování DPH** upraveny o kolísání směnného kurzu mezi LM a přídavnou měnou vykazování.

   Při spuštění dávkové úlohy **Úprava směnných kurzů** je směnný kurz identifikován na stránce **Směnný kurz** a poté jsou částky na polích **Částka** a **Částka v přídavné měně** na vstupu DPH jsou porovnána, aby se určilo, zda existuje kurzový zisk nebo ztráta. Dávková úloha používá možnost, kterou vyberete v tomto poli, k určení, jak zaúčtovat zisky nebo ztráty směnného kurzu pro účty DPH.

   Máte stejné možnosti jako u položek hlavní knihy, ale v tomto případě budou upraveny položky DPH. V následující tabulce jsou uvedeny možnosti výběru.

   | Pole | Popis |
   |----------------------------------|---------------------------------------|  
   | **Bez úpravy** | Na účtu hlavní knihy se neprovede žádná úprava směnného kurzu. Tato možnost je výchozí. |
   | **Úprava částky** | Částka LM je upravena o kurzové zisky nebo ztráty. Kurzové zisky nebo ztráty jsou zaúčtovány na účet hlavní knihy v poli **Částka** a na účty, které jste zadali pro zisky nebo ztráty v polích **Účet realizovaných finančních zisků** a **Účet realizovaných finančních ztrát** na stránce **Měny**. |
   | **Úprava částy v přídavné měně** | Přídavná měna vykazování je upravena o kurzové zisky nebo ztráty. Kurzové zisky nebo ztráty jsou zaúčtovány na účet hlavní knihy v poli **Částka v přídavné měně** a na účty, které jste zadali pro zisky nebo ztráty v polích **Účet realizovaných finančních zisků** a **Účet realizovaných finančních ztrát** na stránce **Měny**. |

### Aktivace přídavné měny pro hlášení
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení financí** a vyberte související odkaz.
2. Na stránce **Nastavení financí** vyberte pole **Přídavná měna pro hlášení** a vyberte měnu, ve které chcete vykazovat.
3. Když opustíte pole, [!INCLUDE[d365fin](includes/d365fin_md.md)] zobrazí potvrzující zprávu popisující účinky aktivace další měny vykazování.
4. Stisknutím tlačítka **Ano** potvrdíte, že chcete aktivovat měnu.
5. Otevře se okno dávkové úlohy **Adjustace  přídavné měny pro hlášení**

   Tato dávková úloha převádí částky LM u existujících položek na přídavnou měnu pro hlášení. Dávková úloha používá výchozí směnný kurz zkopírovaný z směnného kurzu platného v pracovní den na stránce **Směnné kurzy**. Zbytkové částky, ke kterým dochází při převodu LM na přídavnou měnu vykazování, jsou zaúčtovány na účty zbytkových zisků a ztrát uvedené na stránce **Měny**. Datum zaúčtování a číslo dokumentu pro tyto položky jsou stejné jako pro původní položku hlavní knihy. Po zaúčtování všech těchto zbývajících položek dávková úloha zaúčtuje položku zaokrouhlení k datu uzávěrky každého uzavřeného roku na účet nerozděleného zisku. Tím zajistíte, že konečný zůstatek účtů příjmů za každý uzavřený rok je 0 v LM i v přídavné měně pro vykazování.
6. Podle potřeby vyplňte pole. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Stisknutím tlačítka **OK** spustíte dávkovou úlohu.

Po spuštění dávkové úlohy budou částky na následujících existujících položkách v LM i v přídavné měně pro hlášení:

- Položky hlavní knihy
- Položky vyrovnání zboží
- Položky DPH
- Položky ocenění
- Řádky výrobní zakázky
- Položky objednávky výrobní zakázky

Kromě toho budou mít všechny budoucí položky stejného typu částky zaznamenané jak v LM, tak v přídavné měně pro hlášení.

> [!NOTE]  
> Pole **Přídavné měny pro hlášení** bude aktivováno až poté, co vyberete tlačítko **OK** v dávkové úloze **Adjustace přídavné měny pro hlášení**.

## Viz související školení v programu [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## Viz také
[Aktualizace směnných kurzů](finance-how-update-currencies.md)  
[Uzavírání roků a období](year-close-years-periods.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
