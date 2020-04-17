---
    title: SEPA Direct Debit in Business Central | Microsoft Docs
    description: You can collect payments directly from the customer’s bank account according to the SEPA format.
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
# Sběr plateb pomocí SEPA – příkaz k inkasu
Se souhlasem zákazníka můžete vybírat platby přímo z bankovního účtu zákazníka podle formátu SEPA.

Nejprve nastavte formát exportu bankovního souboru, který dá bance pokyn k provedení inkasa. Poté nastavte způsob platby zákazníka. Nakonec nastavte zmocnění k přímému debetu, který odráží váš souhlas se zákazníkem vybírat platby v určitém období trvání smlouvy.

Chcete-li dát pokyn bance, aby převedla částku platby z bankovního účtu zákazníka na účet vaší společnosti, vytvořte Položku přímého inkasa, která obsahuje informace o bankovních účtech, ovlivněných prodejních fakturách a mandátu k inkasu. Potom exportujte soubor XML, který je založen na položce inkasa, kterou odešlete bance ke zpracování. Všechny platby, které nemohly být zpracovány, vám sdělí vaše banka a musíte poté ručně odmítnout Položky přímého inkasa

Můžete nastavit Kódy std.prodeje zákazníka pomocí způsobu platby inkasem a informací o pověření. Potom můžete použít dávkovou úlohu **Vytvořit standardní faktury odběratele** pro generování několika prodejních faktur s předvyplněnými informacemi o přímém debetu. To lze provést ručně nebo automaticky podle data splatnosti platby.

Pokud jsou platby úspěšně zpracovány, jak je sdělí vaše banka, můžete účtovat přijaté platby buď přímo ze stránky **Položky přímého inkasa** nebo přesunutím platebních řádků do deníku, kde zaúčtujete potvrzení o platbě, například na stránku **Deník přijaté hotovosti**. Případně, v závislosti na procesu řízení hotovosti, můžete počkat a použít platby jako součást odsouhlasení banky.

> [!NOTE]
> Pro inkaso plateb pomocí příkaz k inkasu SEPA, musí být měna na prodejní faktuře EURO.

## Nastavení SEPA – příkaz k inkasu
Ze stránky **Přímá inkasa** můžete exportovat pokyny do své elektronické banky a provést inkaso z účtu zákazníka na váš bankovní účet. [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje formát inkasa SEPA, ale ve vaší zemi/oblasti mohou být k dispozici jiné formáty pro elektronické platby.

Chcete-li povolit export formátů bankovních souborů, které nejsou v [!INCLUDE[d365fin](includes/d365fin_md.md)] předdefinované, můžete nastavit definici výměny dat pomocí rámce pro výměnu dat. Více informací viz [Nastavení definic výměny dat](across-how-to-set-up-data-exchange-definitions.md).

Před zpracováním plateb odběratele elektronicky exportem inkasa ve formátu přímého debetu SEPA je nutné provést následující kroky nastavení:

* Nastavte formát exportu bankovního souboru, který vaší bance dá pokyn k provedení inkasní inkasy z bankovního účtu zákazníka na bankovní účet.
* Nastavte způsob platby zákazníka.
* Nastavte zmocnění k přímému debetu, který odráží váš souhlas se zákazníkem získávat jejich platby v určité době trvání smlouvy.

### Nastavení bankovního účtu pro inkaso SEPA
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Bankovní účty** a poté vyberte související odkaz.
2. Otevřete bankovní účet, který chcete použít pro inkaso.
3. Na záložce **Převod** v poli **Formát exportu přímého inkasa SEPA**, vyberte možnost inkasa SEPA.

### Nastavení způsobu platby zákazníka pro inkaso SEPA
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Způsoby platby** a poté vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Nastavte způsob platby. Vyplňte pole pro inkaso, nebo specifická, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Přímý debet** | Určete, zda je způsob platby Přímé inkaso SEPA. |
   | **Kód podmínek  přímého inkasa** | Určete platební podmínky, jako například NEPLATIT, které se zobrazují na prodejních fakturách placených inkasem SEPA, což zákazníkovi oznamuje, že platba bude inkasována automaticky. Případně pole nechte prázdné. |

   > [!NOTE]
   > Nezadávejte hodnotu do pole **Číslo protiúčtu**.

4. Zvolte tlačítko **OK**, chcete-li zavřít stránku **Způsoby platby**.
5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
6. Otevřete zákaznickou kartu zákazníka, kterého chcete nastavit pro příkaz k inkasu SEPA.
7. Vyberte pole **Kód způsobu platby**, a poté vyberte kód platební metody, který jste zadali v kroku číslo 3.
8. Opakujte kroky 6 a 7 pro všechny zákazníky, které chcete nastavit pro příkaz k inkasu SEPA.

#### Chcete-li nastavit mandát k přímému inkasu, který představuje smlouvu se zákazníkem
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Otevřete kartu pro zákazníka, kterého chcete nastavit pro příkaz k inkasu SEPA.
3. Zvolte akci **Bankovní účty**.
4. Na stránce **Přehled bank.účtů zákazníka** odběratele vyberte bankovní účet odběratele, který bude používat inkasa, a pak zvolte **Zmocnění k přímému debetu**.
5. Na stránce **Zmocnění k přímému debetu** vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Kód bankovního účtu zákazníka** | Určuje bankovní účet, ze kterého se platí přímým\inkasem. Toto pole je vyplněno automaticky. |
   | **Platné od** | Zadejte datum zahájení Zmocnění k přímému debetu. |
   | **Platné do** | Určete datum, ukončení zmocnění k přímému debetu. |
   | **Datum podpisu** | Zadejte datum, kdy zákazník schválil zmocnění k přímému debetu. |
   | **Typ sekvence** | Určete, zda se smlouva vztahuje na několik (**Periodický**) nebo jednu (**Jednorázové**) přímé inkaso. |
   | **Očekávaný počet inkas** | Určete, kolik přímých inkas očekáváte, že provedete. Toto pole je relevantní pouze v případě, že jste v poli **Typ sekvence** vybrali  **Periodický**. |
   | **Počet inkas** | Určuje, kolik přímých inkas bylo provedeno pomocí tohoto zmocnění k přímému debetu. Toto pole je automaticky aktualizováno. |
   | **Blokováno** | Určete, že přímé inkasa nelze provést pomocí tohoto zmocnění k přímému debetu. |

6. Opakujte kroky 1 až 5 pro všechny zákazníky, které chcete nastavit pro přímé inkasa SEPA.

Zmocnění k přímému debetu je automaticky vloženo do **ID zmocnění k přímému debetu** při vytváření prodejní faktury pro odběratele, kterého jste vybrali v kroku 2. Další informace naleznete v části [Vytvoření periodických nákupních a prodejních řádků](sales-how-work-standard-lines.md).

## Vytvoření záznamů přímého inkasa SEPA a export do bankovního souboru.
Chcete-li dát pokyn bance, aby převedla částku platby z bankovního účtu zákazníka na účet vaší společnosti, vytvořte Přímé inkaso, která obsahuje informace o bance, ovlivněných prodejních fakturách a Zmocnění k přímému debetu. Z výsledné položky přímého inkasa pak exportujete soubor XML, který odešlete, nebo nahrajete do elektronického bankovnictví ke zpracování. Všechny platby, které nemohly být bankou zpracovány, vám sdělí vaše banka a poté musíte ručně odmítnout Položky přímého inkasa.

> [!NOTE]
> Pro inkaso plateb pomocí příkaz k inkasu SEPA, musí být měna na prodejní faktuře EURO.

### Chcete-li vytvořit přímé inkaso

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Přímá inkasa** a poté vyberte související odkaz.
2. Na stránce **Přímá inkasa** vyberte akci **Vytvořit přímé inkaso**.
3. Na stránce **Vytvořit přímé inkaso**, vyplňte pole podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Od data splatnosti** | Určuje nejdřívější datum splatnosti platby na prodejních fakturách, pro které chcete vytvořit přímé inkaso. |
   | **Do data splatnosti** | Určuje nejnovější data splatnosti na prodejních fakturách, pro které chcete vytvořit přímé inkaso. |
   | **Typ partnera** | Určete, zda je přímé inkaso vytvořeno pro zákazníky typu **Společnost** nebo **Osoba**. |
   | **Pouze zákazníci s platným povolením** | Určete, zda je pro zákazníky, kteří mají platné zmocnění k přímému debitu, vytvořeno přímé inkaso. **Note:** Přímé inkaso je vytvořeno i v případě, že **ID zmocnění k přímému debetu** není vyplněno na prodejní faktuře. |
   | **Pouze faktury s platným povolením** | Určuje, jestli přímé inkaso je vytvořeno pouze pro prodejní faktury, pokud je vybrán platný mandát přímého inkasa v poli  **ID mandátu přímého inkasa** na prodejní faktuře. |
   | **Číslo bankovního účtu** | Určuje, na který z vašich bankovních účtů společnosti budou inkasované platby převedeny z bankovního účtu zákazníka. |
   | **Název bankovního účtu** | Určuje název bankovního účtu, který jste vybrali v poli **Číslo bankovního účtu**. Toto pole je vyplněno automaticky. |

4. Zvolte tlačítko **OK**.

   Přímé inkaso je přidáno na stránku **Přímé inkaso**, a vytvoří se jedna nebo více položek přímého inkasa.

### Pro export položky přímého inkasa do bankovního souboru
1. Na stránce **Přímé inkaso**, vyberte akci **Položky přímého  inkasa**.
2. Na stránce **Položky přímého inkasa** vyberte položku, kterou chcete exportovat, a poté vyberte akci **Vytvořit soubor přímého inkasa**.
3. Uložte exportovaný soubor na místo, odkud jej odešlete nebo nahrajete do svého elektronického bankovnictví.

   Na stránce **Položky přímého inkasa** je změněno pole **Stav přímého inkasa** na soubor vytvořen. Na stránce **SEPA povolení přímého inkasa** je pole **Počet inkas** zvětšeno o jedna.

Pokud exportovaný soubor nelze zpracovat, například z důvodu platební neschopnosti zákazníka, můžete položku přímého inkasa odmítnout. Pokud je exportovaný soubor úspěšně zpracován bankou, jsou splatné platby zahrnutých prodejních faktur automaticky vybírány od vybraných zákazníků. V takovém případě můžete sbírku uzavřít.

### Odmítnutí položky přímého inkasa

* Na stránce **Položky přímého inkasa**, vyberte položku, která nebyla úspěšně zpracována, a poté vyberte akci **Odmítnout položku**.

   Hodnota v poli **Stav** na stránce **Položky přímého  inkasa** je změněno na **Odmítnuto**.

### Zavření přímého inkasa
* Na stránce **Položky přímého inkasa** vyberte položku, která byla úspěšně zpracována, a pak zvolte akci **Zavřít inkaso**.

   Související přímé inkaso je uzavřeno.

Nyní můžete přistoupit k zaúčtování potvrzení o platbě za zahrnuté prodejní faktury. Toto můžete provést tak, jak obvykle zaúčtujete potvrzení o platbě, například na stránce **Platební registrace**, nebo můžete související potvrzení o platbě zaúčtovat přímo ze stránky **Položky přímého  inkasa** Více informací viz [Účtování přijaté platby SEPA – příkaz k inkasu](finance-how-to-post-sepa-direct-debit-payment-receipts.md).

## Účtování přijaté platby SEPA – příkaz k inkasu
Pokud banka úspěšně zpracuje přímé inkaso, můžete přistoupit k zaúčtování přijetí platby za zúčastněné prodejní faktury. Více informací viz [Vytvoření přímého inkasa SEPA a jeho exportace do bankovního souboru](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).

Přijetí platby můžete přímo ze stránky **Přímá inkasa**, nebo ze stránky **Položky přímého inkasa** Případně můžete předat práci jinému uživateli přípravou souvisejících řádků deníku.

### Chcete-li zaúčtovat potvrzení o inkasu ze stránky Přímé inkaso.
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Přímá inkasa** a poté vyberte související odkaz.
2. Vyberte řádek pro inkasní kolekci, která byla exportována do bankovního souboru a úspěšně zpracována bankou.
3. Zvolte akci **Účtovat přijaté platby**.
4. Na stránce **Zaúčtovat přímé inkaso** vyplňte pole podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Číslo přímého inkasa** | Určuje přímé inkaso, pro které chcete zaúčtovat příjem platby. |
   | **Šablona hlavního deníku** | Určuje, která šablona hlavního deníku se použije k účtování přijetí platby, jako je například šablona pro příjmy v hotovosti. |
   | **Název listu finančního deníku** | Určuje, který list finančního deníku použít pro účtování přijetí platby. |
   | **Pouze vytvořit deník** | Určuje, zda chcete zúčtovat příjemku platby, když zvolíte tlačítko **OK**. Příjemka platby bude připravena ve definovaném deníku a nebude zúčtována, dokud někdo nezúčtuje řádky deníku. |

5. Zvolte tlačítko **OK**.

## Viz také
[Správa pohledávek](receivables-manage-receivables.md)  
[Správa servisu](service-service.md)
