---
title: Reconcile Payments Using Automatic Application
description: Describes how to use the automatic application function to apply payments or cash receipts to their related open entries, and reconcile payments.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 10/01/2020
ms.author: edupont

---
# Odsouhlasení plateb pomocí automatického vyrovnání

Stránka **Deníky odsouhlasení plateb** určuje platby, příchozí nebo odchozí, které byly evidovány jako transakce na Vašem bankovním účtu, které mají být vyrovnány s otevřenými položkami zákazníků, dodavatelů a položkami bankovního účtu.  Řádky v deníku lze vyplnit importem bankovního výpisu, který je jako bankovní zdroj nebo pomocí ručního zadání transakcí, které v platební službě provádíte.

> [!NOTE]
> Stránka nabízí funkci automatického párování, která vyrovnává platby na jejich související otevřené položky na základě shody dat na řádku bankovního výpisu (řádek deníku) s daty na jedné nebo více otevřených položkách. Všimněte si, že navrhované automatické vyrovnání můžete přepsat a můžete se rozhodnout, zda automatické vyrovnání vůbec použijete. Další informace naleznete v kroku 7.

Deník odsouhlasení plateb souvisí s bankovním účtem v [!INCLUDE[prod_short](includes/prod_short.md)], jenž odráží online bankovní účet, na kterém jsou zaznamenány platební transakce. Všechny položky otevřeného bankovního účtu, které souvisejí s vyrovnanými položkami zákazníka nebo dodavatele budou uzavřeny, pokud použijete funkci  **Účtování plateb a odsouhlasení bakovního účtu**. To znamená, že bankovní účet je automaticky odsouhlasen pro platby, které zaúčtujete do deníku.

Můžete importovat bankovní transakce pomocí souborů ve fommátu CSV nebo jiným, který vaše banka poskytuje. Pokud chcete importovat bankovní výpisy jako bankovní kanály, musíte nejprve povolit specializovanou službu integrace bank a poté propojit bankovní účet s jeho souvisejícím online bankovním účtem. Deník odsouhlasení plateb pak automaticky detekuje bankovní výpisy, když použijete funkci **Import bankovních transakcí**. Kromě toho můžete nastavit bankovní účet tak, aby každou hodinu automaticky importoval nové bankovní výpisy. Transakce pro platby, které již byly zaúčtovány a jsou vyrovnané nebo odsouhlasené, nebudou importovány. Můžete k tomu použít službu Envestnet Yodlee Bank Feeds, která je předinstalována v některých verzích [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro více informací navštivte [Nastavení služby Envestnet Yodlee Bank](bank-how-setup-bank-statement-service.md). Případně kontaktujte svého partnera společnosti Microsoft a požádejte o pomoc s plněním požadavků vaší firmy nebo země.

**Textové mapování účtů** umožňuje nastavit mapování mezi textem plateb a konkrétními debetními, kreditními účty a protiúčty tak, aby tyto platby byly při zaúčtování deníku odsouhlasení plateb zaúčtovány na zadané účty. To je užitečné například pro opakující se hotovostní příjmy nebo výdaje, jako jsou časté nákupy pohonných hmot pro automobily nebo bankovní poplatky a úroky, které se pravidelně vyskytují na bankovním výpisu a nepotřebují související obchodní doklad. (Viz krok 10 níže) Pro více informací navštivte [Textové namapování opakovaných plateb pro automatické vyrování](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Řádky deníku nemusí mít žádný návrh vyrovnaní. Může to být z různých důvodů, například kvůli chybějícímu dokladu nebo kvůli tomu, že zákazník přeplatil částku, takže po uplatnění platby na jiném řádku deníku existuje nadměrná částka. V takových případech můžete pomocí akce **Převést rozdíl na účet** vytvořit a zaúčtovat chybějící položku hlavní knihy, například pro vrácení peněz, na kterou je potřeba vyrovnat platbu. (Viz krok 11 níže) Pro více informací navštivte [Odsouhlasení plateb, které nemohou být vyrovnány](receivables-how-reconcile-payments-cannot-apply-auto.md).

Funkci **Vyrovnat automaticky** použijete buď při importu bankovního souboru nebo výpisu s platebními transakcemi k vyrovnání plateb na jejich související otevřené položky na základě shody textu v bance na řádek výpisu (řádek deníku) s textem u jedné nebo více otevřených položek. Tato automatizace je založena na pravidlech, které se definují na stránce **Pravidla vyrovnání plateb**, kde také definujete, zda návrh vyrovnání vyžaduje kontrolu. Pro více informací navštivte [Nastavení pravidel pro automatické vyrovnání plateb](receivables-how-set-up-payment-application-rules.md).

Na řádcích deníku, kde byla platba automaticky vyrovnána u jedné nebo více otevřených položek má pole **Spolehlivost párování** hodnotu **Nízká**, **Střední** nebo **Vysoká** k označení kvality shody dat, na které je navrhovaná platba založena.

Některé vyrovnání plateb vyžadují vaši kontrolu, tak jak je definováno pravidlem vyrovnání, například pro řádky se spolehlivostí **Nízká**. Jiné řádky vyžadují vaši kontrolu a ruční změnu, protože je v poli **Rozdíl** hodnota. Chcete-li zkontrolovat jedno nebo více vyrovnání plateb, vyberte pole **Řádky ke kontrole** nebo **Řádky s rozdílem**. Stránka **Přehled vyrovnání plateb** zobrazuje všechny relevantní informace o zákazníkovi nebo dodavateli, ke kterému je platba vyrovnána, dále podrobnosti o spolehlivosti vyrovnání a akci **Akceptovat vyrovnání** ke zpracování řádku. (Viz kroky 7 a 8 níže.)

Pro každý řádek deníku na stránce **Deníky odsouhlasení plateb**, můžete otevřít stránku **Vyrovnání platby** a zobrazit všechny otevřené položky pro vyrovnání plateb, dále detailní náhled na infromace pro každou položku a její spolehlivost párování, na kterém je založeno vyrovnání. Zde můžete ručně vyrovnat platby nebo znovu vyrovnat platby, které byly automaticky vyrovnány na nesprávnou položku. (Viz krok 10 níže.) Pro více informací navštivte [Náhled nebo vyrovnání plateb po automatickém vyrovnání](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Import bankovního výpisu můžete spouštět současně s otevřeným **Deníkem odsouhlasení plateb** pro již existující deník. Následující postup popisuje, jak importovat bankovní výpis na stránce **Deníky odsouhlasení plateb** po vytvoření nového deníku.

## Odsouhlasení plateb pomocí automatického vyrovnání
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Deníky odsouhlasení plateb** a poté vyberte související odkaz.
2. Chcete-li pracovat v novém deníku odsouhlasení plateb vytvořte nový pomocí akce **Nový deník**.
3. Na stránce **Přehled plateb bankovního účtu**, vyberte bankovní účet, pro který chcete odsouhlasit platby a poté zvolte tlačítko **OK**.
   Stránka **Deníky odsouhlasení plateb** se otevře připravená pro vybraný bankovní účet.
4. Vyberte akci **Import Bankovních Transakcí**.
   Pokud bankovní účet vybraného deníku není nastaven pro import bankovních transakcí, otevře se dialogové okno, které vám pomůže vyplnit příslušná pole.
5. Na stránce **Vyberte soubor k importu**, vyberte soubor obsahující bankovní transakce pro platby, které chcete odsouhlasit, a pak zvolte talčítko **Otevřít**.
6. Pokud je povolena služba Envestnet Yodlee Bank Feeds, zadejte na stránce **Filtr bankovního výpisu**, která se otevře automaticky, časový interval pro import bankovnách výpisů.

   Stránka **Deníky odsouhlasení plateb** je vyplněna řádky pro platby představující bankovní transakce z importovaného bankovního výpisu.

   Na řádcích plateb, které byly automaticky vyrovnány se souvisejícími otevřenými položkami, má pole **Spolehlivost párování** hodnotu mezi **Nízký** a **Vysoký** k označení kvality shody dat, na kterém je navrhované platební vyrování založeno. Kromě toho jsou pole **Název účtu**, **Typ účtu** a **Číslo účtu** naplněna informacemi o zákazníkovi nebo dodavateli, na které se platba vztahuje.

   Automatické vyrovnání, spolehlivost párování a to, zda řádky vyžadují kontrolu jsou definovány pravidly, které můžete upravovat a podle toho upravit i výsledky. Pro více informací navštivte [Nastavení pravidel pro automatické vyrovnání plateb](receivables-how-set-up-payment-application-rules.md).

7. Chceteli zkontrolovat, přijmout/odebrat nebo ručně změnit více vyrovnání plateb, které mají hodnotu v polie **Rozdíl** použijte funkci **Řádky s rozdílem**.

   Otevře se stránka **Náhled vyrovnaní plateb**, která zobrazuje první vyrovnání plateb ke kontrole. Další vyrovnání, které je třeba zkontrolovat, se zobrazí na stránce při zpracování předchozího vyrovnání. Všechny relevantní informace o zákazníkovi nebo dodavateli, na které je platba vyrovnána, spolehlivost vyrování a akce pro zpracování řádků, například funkce **Akceptovat vyrovnání** a **Vyrovnat ručně**.

8. Chcete li zkontrolovat, přijmout/odstranit nebo runě změnít více vyrovnání plateb, které mají být zkontrolovány podle pravidel vyrovnání, vyberte akci **Řádky ke kontrole**.  Stejná akce je popsána v kroku 8.

9. Chcete-li změnit automatické vyrovnání, vyberte řádek deníku a pak zvolte akci **Vyrovnat ručně** pro opětovné vyrovnání nebo vyrovnat ručně na stránce **Vyrovnání platby**. Pro více informací navštivte [Náhled nebo vyrovnání plateb po automatickém vyrovnání](receivables-how-review-apply-payments-auto-application.md).

10. Vyberte nevyrovnaný řádek deníku pro opakovaný příjem nebo výdej hotovosti, jako je například nákup pohonných hmot vyberte funkci **Mapování textu na účet**. Další informace naleznete v [Textové namapování opakovaných plateb pro automatické odsouhlasení](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

   Po dokončení mapování textu platby na účty zvolte akci **Vyrovnat ručně**.

   Když je Textové mapování účtů nastavené, výsledné automatické vyrovnání plateb bude obsahovat **Vysoké - Textové mapování účtů** v poli **Spolehlivost párování**.

11. Pokud řádek deníku nemá žádný návrh vyrovnání plateb, protože neexistuje žádná položka, se kterou by mohla být vyrovnána zvolte funci **Převést rozdíl na účet** k vytvoření a zaúčtování položky hlavní knihy, která je nutná pro úhradu platby. Pro více informací navštivte [Odsouhlasené platby, které nemohou být vyrovnány](receivables-how-reconcile-payments-cannot-apply-auto.md).

10. Pokud žádné další řádky nevyžadují kontrolu a pole **Rozdíl** je prázdné na všech řádcích, zvolte funkci **Účtovat** a vyberte jednu z následujích možností.

   - **Účtovat platby a odsouhlasení bankovního účtu** - Pro účtování plateb, které jsou vyrovnané a také k uzavření souvisejicích položek bankovního účtu.
   - **Účtovat pouze platby** - Pro zaúčtování vyrovnaných plateb, ale nechá otevřené položky hlavní knihy, které souvisejí s bankovním účtem. Je zde vyžadováno samostatné odsouhlasení bankovního účtu, například: Více informací naleznete v [Odsouhlasení bankovních účtů](bank-how-reconcile-bank-accounts-separately.md).
   - **Testovací sestava** - Pro kontrolu výsledku účtování, předtím než zaúčtujete data. Spustí se sestava **Výpis bankovního účtu** a zobrazí stejné pole jako v dolní části stránky **Deník odsouhlasení plateb**.

Když zaúčtujete deník odsouhlasení plateb, otevřena vyrovnaná položka je uzavřena a související položka zákazníka, dodavatele nebo fin. účtu je aktualizována. U plateb na řádcích deníku na základě mapování textu na účet se aktualizují zadané účty zákazníků, dodavatelů a hlavní knihy. Pro všechny řádky deníku jsou vytvořeny položky bankovního účtu. Pokud zvolíte akci **Účtování plateb a odsouhlasení bankovního účtu** zavřou se všechny otevřené položky související s vyrovnanými položkami zákazníka, dodavatele a hlavní knihy. To znamená, že bankovní účet je automaticky odsouhlasen pro platby, které zaúčtujete do deníku.

Můžete porovnat hodnotu v poli **Saldo na bankovním účtu po účtování** společně s hodnotou v poli **Konečné saldo bankovního výpisu** a sledovat, kdy je bankovní účet odsouhlasen na základě platby, které se zaúčtují.

> [!NOTE]  
> Pokud nechcete odsouhlasit bankovní účet na stránce **Deníky odsouhlasení plateb** musíte použít stránku **Odsouhlasení bankovního účtu**. Pro více informací navštivte [Odsouhlasení bankovních účtů](bank-how-reconcile-bank-accounts-separately.md).

## Viz také
[Správa pohledávek](receivables-manage-receivables.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]