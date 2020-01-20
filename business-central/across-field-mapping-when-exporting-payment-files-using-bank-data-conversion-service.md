---
    title: Field mapping for exporting bank payment files | Microsoft Docs
    description: When you export payment files using the AMC Banking 365 Fundamentals extension, the data that you export is exposed to the service provider.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Mapování polí při exportu platebních souborů pomocí rozšíření AMC Banking 365 Fundamentals
Když exportujete platební soubory pomocí rozšíření AMC Banking 365 Fundamentals, data, která exportujete, jsou vystavena poskytovateli služeb. Za ochranu osobních údajů je zodpovědný poskytovatel služeb. Další informace o rozšíření AMC Banking 365 Fundamentals naleznete v části [Používání rozšíření AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md).

> [!CAUTION]
> Při exportu platebních souborů pomocí rozšíření AMC Banking 365 Fundamentals, budou některá vaše obchodní data zpřístupněna poskytovateli služby. Za ochranu osobních údajů je zodpovědný poskytovatel služeb společnosti AMC Consult A/S. Pro více informací navštivte [Zásady ochrany osobních údajů AMC](https://go.microsoft.com/fwlink/?LinkId=510158).

Následující tabulka obsahuje pole v [!INCLUDE[d365fin](includes/d365fin_md.md)], ze kterých lze exportovat data.

| Připojené pole | Pole v tabulce | Tabulka | Popis |
|------------------|--------------------|-----------|---------------------------------------|  
| Číslo kreditora | Číslo kreditora | Bankovní účet | Identifikátor pro výběr plateb přiřazený vaší firmě bankou |
| Číslo bankovního účtu odesílatele | Č. bankovního účtu/IBAN | Bankovní účet | Číslo bankovního účtu vaší společnosti (IBAN nebo jiné), které je zadáno na kartě bankovního účtu |
| Odesílatelův clearingový standard | Clearingový standard | Bankovní účet | Registr názvů národních bank používaný pro bankovní účet odesílatele |
| Odesílatelův clearingový standard | Clearingový standard | Bankovní účet | Identifikátor banky odesílatele ve vztahu k použitému registru názvů banky |
| BIC banky odesílatele | SWIFT kód | Bankovní účet | Identifikátor SWIFT bankovního účtu odesílatele |
| Měna bankovního účtu odesílatele | Kód měny | Bankovní účet | Kód měny bankovního účtu odesílatele |
| Číslo dokladu | Číslo dokladu | Řádek finančního deníku | Číslo dokladu na řádku platby |
| Externí číslo vyrovnaného dokladu | Externí číslo vyrovnaného dokladu | Řádek finančního deníku | Číslo externího dokladu faktury nebo dobropisu, na který se platební řádek vztahuje |
| ID příjemce | Číslo účtu | Řádek finančního deníku | Číslo zákazníka nebo dodavatele, které je uvedeno na řádku platby |
| Způsob platby | Typ platby konver. bank. dat Typ | Způsob platby | Typ bankovního převodu, jako je tuzemský nebo mezinárodní |
| Platební reference | Platební reference | Řádek finančního deníku | Platební reference řádku platby |
| Adresa příjemce | Adresa | Zákazník/Dodavatel | Adresa příjemce uvedená na kartě zákazníka nebo dodavatele |
| Město příjemce | Město | Zákazník/Dodavatel | Město příjemce, které je uvedeno na kartě zákazníka nebo dodavatele |
| Jméno příjemce | Name | Zákazník/Dodavatel | Jméno příjemce, které je zadáno na kartě zákazníka nebo dodavatele |
| Kód země/oblasti příjemce | Kód země/oblasti | Zákazník/Dodavatel | Kód země/oblasti příjemce, který je zadán na kartě zákazníka nebo dodavatele |
| PSČ příjemce | PSČ | Zákazník/Dodavatel | Poštovní směrovací číslo příjemce, které je zadáno na kartě zákazníka nebo dodavatele |
| Bankovní účet příjemce dokladu | Č. bankovního účtu/IBAN | Bankovní účet zákazníka/bankovní účet dodavatele | Číslo bankovního účtu příjemce (IBAN nebo jiné), které je uvedeno na kartě bankovního účtu zákazníka nebo dodavatele |
| Clearingový kód banky příjemce | Clearingový standard | Bankovní účet zákazníka/bankovní účet dodavatele | Registr názvů národních bank použitý pro bankovní účet příjemce |
| Clearingový kód banky příjemce | Clearingový standard | Bankovní účet zákazníka/bankovní účet dodavatele | Identifikátor bankovního účtu příjemce ve vztahu k používanému registru názvů bankovních účtů |
| E-mailová adresa příjemce | E-mail | Zákazník/Dodavatel | E-mailová adresa příjemce |
| Zpráva příjemci 1 | Zpráva příjemci | Řádek finančního deníku | Zpráva adresáta, která je určena na řádku platby |
| Amount | Amount | Řádek finančního deníku | Částka na řádku platby |
| Kód měny | Kód měny | Řádek finančního deníku | Kód měny na platebním řádku |
| Datum převodu | Posting Date | Řádek finančního deníku | Zúčtovací datum řádku platby |
| Částka faktury | Původní částka | Položka zákazníka/dodavatele | Částka položky, na kterou je platba vyrovnána |
| Datum fakturace | Datum dokladu | Položka zákazníka/dodavatele | Datum faktury u položky, na kterou je platba vyrovnána |
| Adresa banky příjemce | Adresa | Bankovní účet zákazníka/bankovní účet dodavatele | Adresa bankovního účtu příjemce, která je uvedena na kartě bankovního účtu zákazníka nebo dodavatele |
| Adresa bankovního účtu příjemce, která je uvedena na kartě bankovního účtu zákazníka nebo dodavatele | Město | Bankovní účet zákazníka/bankovní účet dodavatele | Město bankovního účtu příjemce, které je uvedeno na kartě bankovního účtu zákazníka nebo dodavatele |
| Název banky příjemce | Name | Bankovní účet zákazníka/bankovní účet dodavatele | Název bankovního účtu příjemce, který je uveden na kartě bankovního účtu zákazníka nebo dodavatele |
| Země/oblast banky příjemce | Kód země/oblasti | Bankovní účet zákazníka/bankovní účet dodavatele | Země nebo oblast bankovního účtu příjemce, která je určena na kartě bankovního účtu zákazníka nebo dodavatele |
| Poštovní směrovací číslo banky příjemce | PSČ | Bankovní účet zákazníka/bankovní účet dodavatele | Poštovní směrovací číslo bankovního účtu příjemce, které je uvedeno na kartě bankovního účtu zákazníka nebo dodavatele |
| Adresa banky odesílatele | Adresa | Bankovní účet | Adresa bankovního účtu odesílatele, která je uvedena na kartě bankovního účtu |
| Město banky odesílatele | Město | Bankovní účet | Město bankovního účtu odesílatele, které je zadáno na kartě bankovního účtu |
| Název banky odesílatele | Name | Bankovní účet | Název bankovního účtu odesílatele, který je uveden na kartě bankovního účtu |
| Země/oblast banky odesílatele | Kód země/oblasti | Bankovní účet | Země/oblast bankovního účtu odesílatele, který je uveden na kartě bankovního účtu |
| PSČ banky odesílatele | PSČ | Bankovní účet | PSČ bankovního účtu odesílatele, které je zadáno na kartě bankovního účtu |
| Šablona finančního deníku | Název šablony deníku | Řádek finančního deníku | Šablona finančního deníku, která se používá pro platební řádek |
| Název listu finančního deníku | Název listu deníku | Řádek finančního deníku | Název listu finančního deníku, který se používá pro řádek platby |
| Název banky odesílatele - konv. dat | Název banky – konver. dat | Bankovní účet | Název bankovního účtu odesílatele, který je požadován rozšířením AMC Banking 365 Fundamentals a je uveden na kartě bankovního účtu |

## Viz také
[Nastavení výměny dat](across-set-up-data-exchange.md)
[Elektronická výměna dat](across-data-exchange.md)
[Používání rozšíření AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)
[Provádění plateb pomocí služby převodu bankovních dat nebo převodem na SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)
