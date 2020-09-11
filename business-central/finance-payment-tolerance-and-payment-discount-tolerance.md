---
    title: Payment Tolerance and Payment Discount Tolerance | Microsoft Docs
    description: You can set up payment tolerance to close an invoice when the payment does not fully cover the amount on the invoice.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Práce s odchylkami platby a tolerancemi platebních slev
Můžete nastavit odchylku platby pro uzavření faktury, pokud platba plně nepokrývá částku na faktuře. Například platební tolerance jsou obvykle pro malé částky, které by stálo více opravit než jen přijmout. Můžete nastavit toleranci platební slevy a poskytnout tak platební slevu po uplynutí data platební slevy.

Můžete použít platební tolerance tak, aby každá nesplacená částka měla nastavenou maximální povolenou platební toleranci. Pokud je splněna odchylka platby, je částka platby analyzována. Pokud je částka platby nedoplatek, pak je nesplacená částka zcela uzavřena nedoplatkem. Podrobná položka je zaúčtována do položky platby, takže na vyúčtované položce faktury nezůstane žádná zbývající částka. Pokud je částka platby přeplatek, je do položky platby zaúčtována nová podrobná položka, takže na položce platby nezůstane žádná zbývající částka.

Můžete použít toleranci platební slevy, takže pokud přijmete platební slevu po datu skonta, pak je vždy zaúčtována buď na účet skonta nebo na účet odchylky skonta.

## Použití platební odchylky na více dokladech
Jeden doklad má stejnou platební toleranci bez ohledu na to, zda je použit samostatně nebo s jinými doklady. Přijetí pozdního skonta při použití odchylky platby na více dokladů se automaticky vyskytuje pro každý doklad, kde platí následující pravidlo:

*datum skonta < datum platby na vybranou položku <= datum odchylky platby*

Toto pravidlo platí také pro určení, zda se mají zobrazit upozornění při použití odchylky platby na více dokladů. Upozornění tolerance skonta se zobrazí pro každou položku, která splňuje kritéria data. Pro více informací navštivte [Příklad 2 – Výpočty tolerancí pro více dokladů](finance-payment-tolerance-and-payment-discount-tolerance.md#example-2---tolerance-calculations-for-multiple-documents).

Můžete zvolit zobrazení upozornění, které je založeno na různých situacích tolerance.

- První upozornění je pro toleranci skonta. Jste informováni, že můžete přijmout pozdní skonto. Poté můžete zvolit, zda chcete přijmout toleranci k datu slevy.
- Druhé upozornění je pro odchylku platby. Budete informováni, že všechny položky mohou být uzavřeny, protože rozdíl je v součtu maximální tolerance platby pro vyrovnané položky. Poté můžete zvolit, zda chcete přijmout toleranci k částce platby.

> [!NOTE]
> Aktivace varovné zprávy umožní zvolit způsob zpracování plateb, které jsou v rámci tolerance. Pokud zprávu nepovolíte a je zadána úroveň tolerance, budou faktury s částkami, které jsou v rámci tolerance, automaticky uzavřeny a zbývající částku nelze ponechat.

Pro další informace navštivte [Povolení nebo zakázání upozornění na toleranci platby](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).

## Nastavení odchylek
Tolerance ve dnech a částkách vám umožňuje uzavřít fakturu, i když platba zcela nepokrývá částku na faktuře, ať už je to z důvodu překročení data splatnosti platební slevy, odečtení zboží nebo z důvodu malé chyby . To platí i pro refundace a dobropisy.

Chcete-li nastavit odchlyku, musíte nastavit různé účty odchylek, zadejte jak odchylku skonta, tak metody účtování odchylky platby a spusťte dávkovou úlohu **Změna platební odchylky**.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení obecného účtování** a poté vyberte související odkaz.
2. Na stránce **Nastavení obecného účtování**, nastavte účet odchylky platby Má dáti a kreditní prodejní platby, dále účet tolerance platby nákupu na stranu Dal.
3. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Účto skupiny zákazníků** a vyberte související odkaz.
4. Na stránce **Účto skupiny zákazníků**, nastavte účet MD účet skonta a DAL účet skonta. Pro další informace navštivte [Nastavení skupin účtování](finance-posting-groups.md).
5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Účto skupiny dodavatele** a poté vyberte související odkaz.
6. Na stránce **Účto skupiny dodavatele** nastavte účet MD účet skonta a DAL účet skonta
7. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení financí** a vyberte související odkaz.
8. Otevřete stránku **Nastavení financí** page.
9. V záložce **Vyrovnání** vyplňte, políčka **Účtování skonta skonta**, **Lhůta odkladu skonta** a **Účtování platební odchylky**.
10. Zvolte akci **Změna platební odchylky**.
11. Na stránce **Změna platební odchylky**, vyplňte pole **Odchylka platby %** a **Max. částka platební odchylky**a poté zvolte tlačítko **OK**

> [!IMPORTANT]  
> Nyní jste nastavili toleranci pouze pro místní měnu. Pokud chcete, aby [!INCLUDE[d365fin](includes/d365fin_md.md)] zpracoval odchylku k platbám, dobropisům a refundacím v cizí měně, musíte spustit dávkovou úlohu **Změna platební odchylky** pomocí pole **Kód měny**.

> [!NOTE]  
> Pokud chcete, aby se upozornění o odchylce platby dostalo pokaždé, když zaúčtujete vyrovnání do ochylky, musíte aktivovat varování o odchylce plateb. Pro další informace navštivte sekci [Povolení nebo zakázání upozornění na toleranci platby](finance-payment-tolerance-and-payment-discount-tolerance.md#to-enable-or-disable-payment-tolerance-warnings).
>
> Chcete-li deaktivovat odchylku pro odběratele nebo dodavatele, musíte zablokovat odchylky na příslušné kartě zákazníka nebo dodavatele. Pro další informace navštivte  [Blokování platebních odchylek pro zákazníky](finance-payment-tolerance-and-payment-discount-tolerance.md#to-block-payment-tolerance-for-customers).
>
> Když nastavíte toleranci, [!INCLUDE[d365fin](includes/d365fin_md.md)] také zkontroluje, zda existují nějaké otevřené položky a vypočítá odchlyky pro tyto položky.

## Povolení nebo zakázání upozornění na odchylky plateb
Upozornění odchylky platby se zobrazí při zaúčtování vyrovnání, které má zůstatek v povolené odchylce. Poté si můžete vybrat, jak chcete zůstatek zaúčtovat a dokumentovat.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení financí** a vyberte související odkaz.
2. Na stránce **Nastavení financí** v záložce **Vyrovnání**, vyberte zašrtávací tlačítko **Varování platební odchylky** k aktivaci upozornění. Chcete-li varování deaktivovat, vypněte zašrtávací políčko.

> [!NOTE]  
> Výchozí volba stránky **Varování platební odchylky** je **Ponechat saldo jako zůstatek**. Výchozí možnost pro stránku **Varování skonta odchylky** je **Nepřijmout opožděné skonto**.

## Blokování platební odchylky pro zákazníky
Výchozí nastavení pro odchylku platby je povoleno. Chcete-li zakázat platební odchylku určitého zákazníka nebo dodavatele, musíte blokovat toleranci na příslušné kartě zákazníka nebo dodavatele. Následující text popisuje, jak to nastavit pro zákazníka. Kroky jsou podobné pro dodavatele.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zákazníci** nebo **Dodavatelé** a vyberte související odkaz.
2. V záložce **platby** vybrte zašrtávací políčko **Nepoužívat platební odchylku**.

> [!NOTE]  
> Pokud má zákazník nebo prodejce otevřené položky, musíte nejprve odstranit odchlyky plateb z položek, které jsou aktuálně otevřené.

## Příklad 1 - Výpočty odchylek pro jeden doklad
Následuje několik příkladů scénářů zobrazujících očekávané výpočty odchylky a účtování, ke kterým dochází v různých situacích.

Stránka **Nastavení financí** obsahuje následující nastavení
- Lhůta odkladu skonta: 5D
- Maximální odchylka platby: 5

Scénáře s alternativou A nebo B představují následující:

- **A** V tomto případě bylo upozornění odchlyky skonta vypnuto nebo má uživatel upozornění zapnuto a zvolil možnost povolit pozdní skonto (Zaúčtovat zůstatek jako odchylku platby).
- **B** V tomto případě má uživatel upozornění a vybral nepovolit pozdní skonto (Ponechat zůstatek jako zbývající částka).

| — | Zásoby | Platba skonta | Max. plat. zálohy | Platba skonta   | Platba skonta zálohy   | Datum platby | Platba | Typ odchylky | Všechny položky uzavřeny | Platba skonta zálohy hl. kn/CL | Platba zálohy hl. kn. |
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
| 1 | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | <=01/15/03 | 985 | Odchylka platby | Ano | 0 | -5 |
| 2 | **1,000** | **20** | **5** | **01/15/03** | **01/20/03** | **<=01/15/03** | **980** | **Žádné** | **Ano** | **0** | **0** |
| 3 | 1,000 | 20 | 5 | 01/15/03 | c | <=01/15/03 | 975 | Odchylka platby | Ano | 0 | 5 |
| 4A | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | 01/16/03 01/20/03 | 1005 | Odchlylka skonta. | Ne, 25 na platbě. | 20/-20 | 0 |
| 5A | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | 01/16/03 01/20/03 | 1000 | Odchlylka skonta. | Ne, 20 na platbě. | 20/-20 | 0 |
| 6A | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | 01/16/03 01/20/03 | 995 | Odchlylka skonta. | Ne, 15 na platbě. | 20/-20 | 0 |
| 4B | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | 01/16/03 01/20/03 | 1005 | Odchylka platby | Ano | 0 | -5 |
| **5B** | **1,000** | **20** | **5** | **01/15/03** | **01/20/03** | **01/16/03 01/20/03** | **1000** | **Žádné** | **Ano** | **0** | **0** |
| 6B | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | 01/16/03 01/20/03 | 995 | Odchylka platby | Ano | 0 | 5 |
| 7 | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | 01/16/03 01/20/03 | 985 | Odchlylka skonta. a platby. | Ano | 20/-20 | -5 |
| 8 | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | 01/16/03 01/20/03 | 980 | Odchlylka skonta. | Ano | 20/-20 | 0 |
| 9 | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | 01/16/03 01/20/03 | 975 | Odchlylka skonta. a platby. | Ano | 20/-20 | 5 |
| 10 | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | >01/20/03 | 1005 | Odchylka platby | Ano | 0 | -5 |
| **11** | **1,000** | **20** | **5** | **01/15/03** | **01/20/03** | **>01/20/03** | **1000** | **Žádné** | **Ano** | **0** | **0** |
| 12 | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | >01/20/03 | 995 | Odchylka platby | Ano | 0 | 5 |
| 13 | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | >01/20/03 | 985 | Žádné | Ne, 15 na faktuře | 0 | 0 |
| 14 | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | >01/20/03 | 980 | Žádné | Ne, 20 na faktuře | 0 | 0 |
| 15 | 1,000 | 20 | 5 | 01/15/03 | 01/20/03 | >01/20/03 | 975 | Žádné | Ne, 25 na faktuře | 0 | 0 |

### Schémata rozsahu plateb
Ve vztahu k výše uvedenému scénáři jsou diagramy rozsahů plateb následující:

#### (1) Datum platby <=01/15/03 (Scénář 1-3)
Zbývající částka na

Běžná pravidla vyrovnání

![Pravdlo 1 odchylky pro jednotnou platbu](media/singlePmtTolRules(Pre1503).gif "Pravdlo 1 odchylky pro jednotnou platbu")

(1) Pokud platba spadá do těchto rozsahů, mohou být všechny položky vyrovnání uzavřeny s tolerancí nebo bez ní..

(2) Pokud platba spadá do těchto rozsahů, nelze všechny položky vyrovnání uzavřít ani s tolerancí.

#### (2) Datum platby je mezi 01/16/03 a 01/20/03 (scénáře 4-9)
Zbývající částka na

Běžná pravidla vyrovnání

![Pravdlo 2 odchylky pro jednotnou platbu](media/singlePmtTolRules(GracePeriod).gif "Pravdlo 2 odchylky pro jednotnou platbu")

(1) Pokud platba spadá do těchto rozsahů, mohou být všechny položky vyrovnání uzavřeny s tolerancí nebo bez ní..

(2) Pokud platba spadá do těchto rozsahů, nelze všechny položky vyrovnání uzavřít ani s tolerancí.

#### (3) Datum platby je po 01/20/03 (scénáře 10-15)
Zbývající částka na

Běžná pravidla vyrovnání

![Pravdlo 3 odchylky pro jednotnou platbu](media/singlePmtTolRules(Post0120).gif "Pravdlo 3 odchylky pro jednotnou platbu")

(1) Pokud platba spadá do těchto rozsahů, mohou být všechny položky vyrovnání uzavřeny s tolerancí nebo bez ní..

(2) Pokud platba spadá do těchto rozsahů, nelze všechny položky vyrovnání uzavřít ani s tolerancí.

## Příklad 2 – Výpočty odchylek pro více dokladů
Následuje několik příkladů scénářů zobrazujících očekávané výpočty odchylky a účtování, ke kterým dochází v různých situacích. Příklady jsou omezeny pouze na scénáře, které vedou k uzavření všech položek ve vyrovnání.

Stránka **Nastavení financí** obsahuje následující nastavení
- Lhůta odkladu skonta: 5D
- Maximální odchylka platby: 5

Scénáře s alternativou A, B, C, nebo D představují následující:

- **A** V tomto případě bylo upozornění odchlyky skonta vypnuto, nebo má uživatel upozornění zapnuto a zvolil možnost povolit pozdní skonto (Zaúčtovat jako odchylka) na libovolné faktuře.
- **B** V tomto případě má uživatel upozornění zapnuto a zvolil nepovolit opožděné skonto na žádné faktuře.
- **C** - V tomto případě má uživatel upozornění zapnuté a zvolil, aby povolil opožděné skonto na první faktuře, ale ne na druhé.
- **D** - V tomto případě má uživatel zapnuté upozornění a zvolil nepřijmou opožděné skonto na první faktuře, ale povolil ji na druhé.

| — | Zásoby | Plat. sleva | Max. plat. zálohy | Platba skonta   | Platba skonta zálohy   | Datum platby | Platba | Typ odchylky | Všechny položky uzavřeny | Platba skonta zálohy hl. kn/CL | Platba zálohy hl. kn. |
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
| 1 | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | <=01/15/03 | 1920 | Odchylka platby | Ano | 0<br /><br /> 0 | -5 <br />-5 |
| **2** | **1,000** <br />**1,000** | **60** <br />**30** | **5** <br />**5** | **01/15/03** <br />**01/17/03** | **01/20/03** <br />**01/22/03** | **<=01/15/03** | **1910** | **Žádné** | **Ano** | **0**<br /><br /> **0** | 0 <br />0 |
| 3 | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | <=01/15/03 | 1900 | Odchylka platby | Ano | 0<br /><br /> 0 | 5 <br />5 |
| 4B | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/16/03 01/17/03 | 1980 | Odchylka platby | Ano | 0<br /><br /> 0 | -5<br /><br /> -5 |
| **5B** | **1,000** <br />**1,000** | **60** <br />**30** | **5** <br />**5** | **01/15/03** <br />**01/17/03** | **01/20/03** <br />**01/22/03** | **01/16/03 01/17/03** | **1970** | **Žádné** | **Ano** | **0**<br /><br /> **0** | **0**<br /><br /> **0** |
| 6B | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/16/03 01/17/03 | 1960 | Odchylka platby | Ano | 0<br /><br /> 0 | 5<br /><br /> 5 |
| 7A | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/16/03 01/17/03 | 1920 | Odchlylka skonta. a platby. | Ano | 60/60<br /><br /> 0/0 | -5 <br />-5 |
| 8A | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/16/03 01/17/03 | 1910 | Odchlylka skonta. | Ano | 60/60<br /><br /> 0/0 | 0 <br />0 |
| 9A | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/16/03 01/17/03 | 1900 | Odchlylka skonta. a platby. | Ano | 60/60 | 5 <br />5 |
| 10B | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 2010 | Odchylka platby | Ano | 0<br /><br /> 0 | -5<br /><br /> -5 |
| **11B** | **1,000** <br />**1,000** | **60** <br />**30** | **5** <br />**5** | **01/15/03** <br />**01/17/03** | **01/20/03** <br />**01/22/03** | **01/18/03 01/20/03** | **2000** | **Žádné** | **Ano** | **0**<br /><br /> **0** | **0**<br /><br /> **0** |
| 12B | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1990 | Odchylka platby | Ano | 0<br /><br /> 0 | 5<br /><br /> 5 |
| 13D | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1980 | Odchlylka skonta. a platby. | Ano | 0/0<br /><br /> 30/-30 | -5 <br />-5 |
| 14D | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1970 | Odchlylka skonta. | Ano | 0/0<br /><br /> 30/-30 | 0 <br />0 |
| 15D | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1960 | Odchlylka skonta. a platby. | Ano | 0/0<br /><br /> 30/-30 | 5 <br />5 |
| 16D | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1950 | Odchlylka skonta. a platby. | Ano | 60/-60<br /><br /> 0/0 | -5 <br />-5 |
| 17D | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1940 | Odchlylka skonta. | Ano | 60/-60<br /><br /> 0/0 | 0 <br />0 |
| 18D | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1930 | Odchlylka skonta. a platby. | Ano | 60/-60<br /><br /> 0/0 | 5 <br />5 |
| 19A | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1920 | Odchlylka skonta. a platby. | Ano | 60/-60<br /><br /> 30/-30 | -5 <br />-5 |
| 20A | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1910 | Odchlylka skonta. | Ano | 60/-60<br /><br /> 30/-30 | 0 <br />0 |
| 21A | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/18/03 01/20/03 | 1900 | Odchlylka skonta. a platby. | Ano | 60/-60<br /><br /> 30/-30 | 5 <br />5 |
| 22B | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/21/03 01/22/03 | 2010 | Odchylka platby | Ano | 0<br /><br /> 0 | -5<br /><br /> -5 |
| **23B** | **1,000** <br />**1,000** | **60** <br />**30** | **5** <br />**5** | **01/15/03** <br />**01/17/03** | **01/20/03** <br />**01/22/03** | **01/21/03 01/22/03** | **2000** | **Žádné** | **Ano** | **0**<br /><br /> **0** | **0**<br /><br /> **0** |
| 24B | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/21/03 01/22/03 | 1990 | Odchylka platby | Ano | 0<br /><br /> 0 | 5<br /><br /> 5 |
| 25A | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/21/03 01/22/03 | 1980 | Odchlylka skonta. a platby. | Ano | 0/0<br /><br /> 30/30 | -5 <br />-5 |
| 26A | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/21/03 01/22/03 | 1970 | Odchlylka skonta. | Ano | 0/0<br /><br /> 30/30 | 0 <br />0 |
| 27A | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | 01/21/03 01/22/03 | 1960 | Odchlylka skonta. a platby. | Ano | 0/0<br /><br /> 30/30 | 5 <br />5 |
| 28 | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | >01/22/03 | 2010 | Odchylka platby | Ano | 0 | -5 |
| **29** | **1,000** <br />**1,000** | **60** <br />**30** | **5** <br />**5** | **01/15/03** <br />**01/17/03** | **01/20/03** <br />**01/22/03** | **>01/22/03** | **2000** | **Žádné** | **Ano** | **0** | **0** |
| 30 | 1,000 <br />1,000 | 60 <br />30 | 5 <br />5 | 01/15/03 <br />01/17/03 | 01/20/03 <br />01/22/03 | >01/22/03 | 1990 | Odchylka platby | Ano | 0 | 5 |

### Schémata rozsahu plateb
Ve vztahu k výše uvedenému scénáři jsou diagramy rozsahů plateb následující:

#### (1) Datum platby <=01/15/03 (Scénář 1-3)
Zbývající částka na

Běžná pravidla vyrovnání

![Pravdlo 1 odchylky pro více plateb](media/multiplePmtTolRules(Pre1503).gif "Pravdlo 1 odchylky pro více plateb")

(1) Pokud platba spadá do těchto rozsahů, mohou být všechny položky vyrovnání uzavřeny s tolerancí nebo bez ní..

(2) Pokud platba spadá do těchto rozsahů, nelze všechny položky vyrovnání uzavřít ani s tolerancí.

#### (2) Datum platby se pohybuje mezi 01/16/03 a 01/17/03 (Scénář 4-9)
Zbývající částka na

Běžná pravidla vyrovnání

![Pravdlo 2 odchylky pro více plateb](media/multiplePmtTolRules(GracePeriodInv1-2).gif "Pravdlo 2 odchylky pro více plateb")

(1) Pokud platba spadá do těchto rozsahů, mohou být všechny položky vyrovnání uzavřeny s tolerancí nebo bez ní..

(2) Pokud platba spadá do těchto rozsahů, nelze všechny položky vyrovnání uzavřít ani s tolerancí.

#### (3) Datum platby se pohybuje mezi 01/18/03 a 01/20/03 (Scénář 10-21)
Zbývající částka na

Běžná pravidla vyrovnání

![Pravdlo 3 odchylky pro více plateb](media/multiplePmtTolRules(GracePeriodInv1).gif "Pravdlo 3 odchylky pro více plateb")

(1) Pokud platba spadá do těchto rozsahů, mohou být všechny položky vyrovnání uzavřeny s tolerancí nebo bez ní..

(2) Pokud platba spadá do těchto rozsahů, nelze všechny položky vyrovnání uzavřít ani s tolerancí.

#### (4) Datum platby se pohybuje mezi 01/21/03 and 01/22/03 (Scénář 22-27)
Zbývající částka na

Běžná pravidla vyrovnání

![Pravdlo 4 odchylky pro více plateb](media/multiplePmtTolRules(GracePeriodInv2).gif "Pravdlo 4 odchylky pro více plateb")Pravdlo 1 odchylky pro více plateb

(1) Pokud platba spadá do těchto rozsahů, mohou být všechny položky vyrovnání uzavřeny s tolerancí nebo bez ní..

(2) Pokud platba spadá do těchto rozsahů, nelze všechny položky vyrovnání uzavřít ani s tolerancí.

#### (5) Datum platby je po 01/22/03 (Scénář 28-30)
Zbývající částka na

Běžná pravidla vyrovnání

![Pravdlo 4 odchylky pro více plateb](media/multiplePmtTolRules(Post0122).gif "Pravdlo 4 odchylky pro více plateb")

(1) Pokud platba spadá do těchto rozsahů, mohou být všechny položky vyrovnání uzavřeny s tolerancí nebo bez ní..

(2) Pokud platba spadá do těchto rozsahů, nelze všechny položky vyrovnání uzavřít ani s tolerancí.

## Viz také
[Finance](finance.md)  
[Setting Up Finance](finance-setup-finance.md)  
[Managing Receivables](receivables-manage-receivables.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
