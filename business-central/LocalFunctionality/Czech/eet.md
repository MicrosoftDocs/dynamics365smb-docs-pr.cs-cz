---
    title: Registration of Sales (EET)
    description: The entrepreneur who realizes sales to be registered has the obligation to register sales. A sale to be registered is a payment in cash, by card, or by similar means, which entails a business income and which is not exempt from registration.
    author: v-pejano

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.search.keywords: CZ, Czech, local, VAT, Control Report
    ms.date: 10/12/2018
    ms.reviewer: v-pejano
    ms.author: v-pejano
---

# Elektronická evidence tržeb (EET)

Elektronická Evidence Tržeb (EET) je evidence tržeb z obchodních činností vyplácených v hotovosti. Informace o těchto transakcích jsou zasílány finančnímu úřadu. V okamžiku platby je vytvořena datová zpráva a odeslána online na portál finanční správy. Odpověď ze serveru je zpráva s jedinečným FIK kódem, který musí být vytištěn na účtence pro zákazníka.

Platební metody obsažené v EET:

- V hotovosti
- Kartou
- Šek
- Cizí směnka
- Jiné podobné typy jako dárkové poukazy, kupóny, bitcoiny atd.

Pro více informací navštivte oficiální portál [ www.etrzby.cz ](http://www.etrzby.cz).

## Jak to funguje v [!INCLUDE[d365fin](../../includes/d365fin_md.md)]

Následující prodejní doklady jsou zahrnuty v aplikaci [!INCLUDE[d365fin](../../includes/d365fin_md.md)]:

- Platba prodejní faktury
- Platba zálohové faktury
- Refundace prodejního dobropisu
- Refundace zálohové faktury
- Příjmový pokladní doklad na Finanční účet (bez prodejního dokladu původu)

Při zaúčtování definovaných dokladů (a s definovanou platební metodou) se vytvoří položka EET a na základě funkčního režimu se zpracuje:

- On-line – položka EET je vytvořena a uložena v aplikaci [!INCLUDE[d365fin](../../includes/d365fin_md.md)], je generována zpráva finančnímu úřadu a odeslána na server. Odpověď ze serveru je zpracována, uložena a na účtence zákazníka je vytištěno jedinečné ID transakce generované daňovými úřady.
- Off-line – záznam EET je vytvořen a uložen v [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. Na účtence zákazníka je vytištěno jedinečné ID generované v [!INCLUDE[d365fin](../../includes/d365fin_md.md)] (Identifikace společnosti a dokladu). Záznamy EET jsou zpracovány později pomocí dávkové úlohy.

## Hlavní funkčnosti

- Položky knihy EET - tabulka, kde jsou uloženy a zpracovány registrované dokumenty. Každý záznam obsahuje údaje o prodeji vyžadované daňovými úřady, potřebné pro tisk účtenky a data z elektronické komunikace. Nové záznamy jsou vytvářeny automaticky zaúčtováním dokladů původu.
- Nastavení služby EET.
- Nastavení certifikátu
- Terminály EET POS – identifikace registrovaných míst.

## Viz také

[Česká lokální funkcionalita](czech-local-functionality.md)  
[Finance](../../finance.md)
