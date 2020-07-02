---
title: Create Contact Companies| Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2020
ms.author: sgroespe

---
# Vytvoření kontaktů
Pravidelně se setkáváte s osobami z jiných společností, z kterých se mohou časem vyvinout obchodní vztahy, například vztahy se zákazníky. Při navázání takového nového kontaktu musí být na kartě kontaktu zaznamenáno co nejvíce informací, aby mohla komunikace pokračovat.

Kontakt můžete vytvořit jako typ **Společnost**, například pokud se nejedná o jednotlivou osobu, ale o entitu, jako je dodavatel nebo banka. Kontakt můžete také vytvořit jako typ **Osoba**. Funkčnost je pro oba typy víceméně stejná a oba se mohou měnit v závislosti na vývoji vztahu.

Když je například karta kontaktu převedena na zákaznickou kartu, stává se kontaktní osobou nebo kontaktní společností jméno zákazníka. Karta kontaktu zůstane a data na obou kartách budou synchronizována do budoucna, pokud je propojíte.

## Osoba nebo společnost
Můžete se rozhodnout nastavit kontakt jako osobu nebo společnost, obvykle v závislosti na tom, zda znáte jméno kontaktní osoby v době vytvoření. To provedete, když vyplníte pole **Typ** na stránce **Karta kontaktu**. Můžete také udržovat karty kontaktů pro společnost i pro jednu nebo více osob pracujících ve společnosti. K tomu dochází automaticky, když vyplníte pole **Název společnosti** na kartě kontaktu typu **Osoba**.

Funkce je stejná pro oba typy, s tím rozdílem, že možnosti pro další informace se mění v závislosti na typu. Pracovní odpovědnosti můžete například přiřadit pouze osobě a průmyslové skupině ve společnosti. Toto je indikováno v uživatelském rozhraní šedým zaškrtnutím políček a akcí, které se nepoužijí. Hodnotu pole **Typ** můžete později změnit, nebo můžete použít pole na záložce **Dědičnost** na stránce **Nastavení marketingu** ke kontrole, která data jsou sdílena mezi osobou a společností, která je s ní ve spojení. Pro více informací navštivte [Nastavení kontaktů](marketing-setup-contacts.md).

## Ruční vytvoření kontaktu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kontakty** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Do pole **Číslo** zadejte číslo kontaktu.

   Alternativně, pokud jste nastavili číselnou řadu pro kontakty na stránce **Nastavení marketingu**, můžete stisknutím klávesy Enter vložit další dostupné číslo kontaktu.
5. Podle potřeby vyplňte zbývající pole. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Vytvoření kontaktu z karty zákazníka, dodavatele nebo z bankovního účtu
Pokud máte zákazníky, dodavatele a bankovní účty, pro které chcete vytvořit karty kontaktů, můžete pomocí dávkové úlohy **Vytvořit kontakty z** vytvořit kontakty na základě existujících dat. Když vytvoříte kontakt tímto způsobem, kontaktní informace budou následně synchronizovány se souvisejícími informacemi o zákazníkovi, dodavateli nebo bankovním účtu. Pro více informací navštivte [Synchronizace kontaktů se zákazníky, dodavateli a bankovními účty](marketing-create-contact-companies.md).

> [!NOTE]
> Než budete moci vytvořit kontakty na základě existujících dat, musíte zadat kód obchodního vztahu pro zákazníky, dodavatele nebo bankovní účty na záložce **Interakce** na stránce **Nastavení marketingu**. Pro více informací navštivte [Nastavení kontaktů](marketing-setup-contacts.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte jednu z následujících možností v závislosti na tom, z čeho chcete vytvořit kontakty, a pak zvolte související odkaz.
   * **Vytváření kontaktů ze zákazníků**
   * **Vytváření kontaktů z dodavatelů**
   * **Vytváření kontaktů z bankovních účtů**
2. Na stránce požadavku, která se otevře, v sekci **Zákazník**, **Dodavatel** nebo **Bankovní účet** nastavte filtry, pokud chcete vytvořit kontakty od konkrétních zákazníků, dodavatelů nebo bankovních účtů.
3. Stisknutím tlačítka **OK** zahajte vytváření kontaktů.

Novým kontaktům jsou přiřazena další čísla kontaktů v číselné řadě. Nově vytvořeným kontaktům jsou přiřazeny obchodní vztahy uvedené na stránce **Nastavení marketingu**.

> [!TIP]
> Můžete to udělat i naopak, a to vytvořením zákazníka, dodavatele nebo bankovního účtu z kontaktu. Pro více informací navštivte [Vytvoření kontaktu jako zákazníka, dodavatele nebo bankovního účtu](marketing-create-contact-companies.md).

## Vytvoření zákazníka, dodavatele nebo bankovního účtu z kontaktu
Pokud máte zákazníka, dodavatele nebo bankovní účet pro společnost, pro kterou chcete vytvořit kontakt, můžete použít funkci **Vytvořit jako**. Když vytvoříte kontakt tímto způsobem, kontaktní informace budou následně synchronizovány se souvisejícími informacemi o zákazníkovi, dodavateli nebo bankovním účtu. Pro více informací navštivte [Synchronizace kontaktů se zákazníky, dodavateli a bankovními účty](marketing-create-contact-companies.md).

> [!NOTE]
> Před vytvořením zákazníků, dodavatelů nebo bankovních účtů z kontaktů musíte na záložce **Interakce** na stránce **Nastavení marketingu** zadat obchodní vztah pro zákazníky, dodavatelé nebo bankovní účty. Pro více informací navštivte [Nastavení kontaktů](marketing-setup-contacts.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kontakty** a poté vyberte související odkaz.
2. Vyberte kontakt, který chcete vytvořit jako zákazníka, dodavatele nebo bankovní účet.
3. Vyberte akci **Vytvořit jako** a poté vyberte **Zákazník**, **Dodavatel** nebo **Banka**.
4. Vyberte tlačítko **OK**.

Kontaktní informace jsou přeneseny z karty kontaktu na nového zákazníka, dodavatele nebo kartu bankovního účtu. Možná budete chtít přidat ke každé kartě konkrétní informace, například fakturaci a platební údaje. Pro více informací navštivte například [Registrace nových zákazníků](sales-how-register-new-customers.md).

## Propojení kontaktu s existujícím zákazníkem, dodavatelem nebo bankovním účtem
Pokud máte kontakt a zákazníka, dodavatele nebo bankovní účet pro stejnou společnost, můžete propojit tyto dvě entity, aby byla synchronizována běžná data.

1. Otevřete kontakt, který chcete propojit.
2. Vyberte akci **Spojit s existujícím** a poté vyberte akci **Zákazník**, **Dodavatel** nebo **Banka**.
3. Na stránce, která se otevře, vyberte zákazníka, dodavatele nebo bankovní účet, na který chcete vytvořit odkaz.
4. V poli **Aktuální platná pole** zadejte, která pole mají být upřednostňována v případě konfliktních informací v polích společných pro kontakt a zákazníka, dodavatele nebo účet. Pokud je například kód prodejce na kartě kontaktu odlišný než na kartě zákazníka, můžete si vybrat, zda chcete zachovat tento kód na kartě kontaktu výběrem možnosti **Kontakt**.
5. Vyberte tlačítko **OK**.

## Synchronizace kontaktů se zákazníky, dodavateli a bankovními účty
Pokud jsou některé z vašich kontaktů také zákazníci, dodavatelé nebo bankovní účty, můžete synchronizovat kontaktní informace se souvisejícím zákazníkem, dodavatelem nebo bankovním účtem.

Při synchronizaci kontaktu se zákazníkem, dodavatelem nebo bankovním účtem existují následující výhody.

* Informace je třeba aktualizovat pouze na jednom místě. Pokud například změníte telefonní číslo kontaktu, bude telefonní číslo automaticky aktualizováno se stejnou úpravou u zákazníka, dodavatele nebo bankovního účtu.
* Pokud jste pro kontakty zadali číselnou řadu, při vytváření karty zákazníka, karty dodavatele nebo karty bankovního účtu se automaticky vytvoří karta kontaktu pro zákazníka, dodavatele nebo bankovní účet.
* Můžete vytvořit prodejní nabídky a objednávky a nakupovat jejich pomocí kontaktu.
* Interakce můžete zaznamenat při provádění akcí, jako je tisk objednávek, hromadné objednávky, vytváření prodejních servisních objednávek, odesílání e-mailů a tak dále.
* Pokud odstraníte kontakt propojený se zákazníkem, dodavatelem nebo bankovním účtem, bude odstraněn pouze kontakt. Zákazník, dodavatel nebo bankovní účet zůstane.
* Pokud odstraníte zákazníka, dodavatele nebo bankovní účet, který je spojen s kontaktem, zůstane kontakt nezměněn.

> [!NOTE]
> Na kartě kontaktu se pouze neobjeví některé podrobnosti, například fakturační a účtovací údaje. Proto je vhodné je přidat ručně na kartu zákazníka, kartu dodavatele nebo kartu bankovního účtu při vytváření kontaktů jako zákazníka, dodavatele nebo bankovní účet.

Synchronizace běžných dat mezi kontakty a příbuznými zákazníky, dodavateli nebo bankovními účty je povolena třemi způsoby:

* Při vytváření kontaktů ze zákazníků, dodavatelů nebo bankovních účtů. Viz [Vytvoření kontaktu ze zákazníka, dodavatele nebo bankovního účtu](marketing-create-contact-companies.md).
* Při vytváření zákazníků, dodavatelů nebo bankovních účtů z kontaktů. Viz [Vytvoření zákazníka, dodavatele nebo bankovního účtu z kontaktu](marketing-create-contact-companies.md).
* Když propojíte kontakty s existujícími zákazníky, dodavateli nebo bankovními účty z karty kontaktu. Viz [Propojení kontaktu s existujícím zákazníkem, dodavatelem nebo bankovním účtem](marketing-create-contact-companies.md).

## Zobrazení, se kterým zákazníkem, dodavatelem nebo bankovním účtem kontakt souvisí
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kontakty** a poté vyberte související odkaz.
2. Vyberte řádek kontaktu, zvolte akci **Související informace** a pak vyberte akci **Zákazník/Dodavatel/Banka**.

Otevře se stránka související karty.

## Viz také
[Správa kontaktů](marketing-contacts.md)  
[Nastavení kontaktů](marketing-setup-contacts.md)  
[Práce s Business Central](ui-work-product.md)
