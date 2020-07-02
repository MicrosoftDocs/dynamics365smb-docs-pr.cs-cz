---
title: Merge Duplicate Customer or Vendor Records | Microsoft Docs
description: Describes how to create a customer card to register information about each new customer or client that you sell to.
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2020
ms.author: sgroespe

---
# Sloučení duplikátního záznamu
Vzhledem k tomu, že různí uživatelé vytvářejí v průběhu času nové karty odběratele, dodavatele nebo kontaktů nebo jsou nové záznamy vytvořeny automaticky během migrace, může být v systému zastoupen zákazník, dodavatel nebo kontakt s více než jedním záznamem. V takovém případě můžete použít stránku **Sloučení duplicit** z karty záznamu, který chcete zachovat. Stránka poskytuje přehled duplicitních hodnot polí a poskytuje funkce pro výběr, které hodnoty se mají při sloučení dvou záznamů do jednoho zrušit nebo zahodit.

> [!NOTE]
> Tuto funkci mohou používat pouze uživatelé se sadou oprávnění MERGE DUPLICATES.

> [!TIP]
> Stránka **Sloučení duplicit** zobrazuje všechna pole, ve kterých se hodnoty liší pro dva porovnávané záznamy. Duplikát je proto označen stránkou zobrazující velmi málo polí. Pokud totiž stránka obsahuje mnoho polí, pak podezřelý záznam pravděpodobně není duplikátem.

Následující postup je založen na kartě zákazníka. Kroky jsou podobné pro dodavatele a karty kontaktů.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Vyberte zákazníka, o kterém víte nebo máte podezření, že duplicitní záznam existuje, a poté vyberte akci **Upravit**.
3. Na stránce **Karta zákazníka** vyberte akci **Sloučit s**.
4. Na stránce **Sloučení duplicit** v poli **Sloučit s** vyberte zákazníka, o kterém si myslíte, že je duplikátem toho, který jste otevřeli, označeného v poli **Aktuální**.

   Na záložce **Pole** sou uvedena pole, ve kterých jsou hodnoty pro oba zákazníky odlišné. To znamená, že pokud je vybraný zákazník skutečně duplikátem, pak by mělo být uvedeno pouze velmi málo polí, například chyby při psaní a další chyby při zadávání dat.

   Záložka **Související tabulky** obsahuje tabulky, ve kterých jsou pole s vztahem k oběma zákazníkům. Pole **Aktuální počet** a **Duplicitní počet** ukazují počet polí v souvisejících tabulkách, kde se používá hodnota **Číslo** jak aktuálního, tak i duplicitního zákazníka. Na stránce **Sloučení duplicit** je tato část pouze informativní, pokud však dojde ke konfliktům sloučení, vyřešíte je na stránce **Konflikty sloučení duplicit**. Viz kroky 8 až 12.

5. U každého pole, ve kterém chcete použít jinou hodnotu, než je aktuální, zaškrtněte políčko **Přepsat**. Po dokončení procesu bude hodnota v poli **Alternativní hodnota** převedena na aktuální záznam.
6. Po dokončení výběru hodnot, které chcete zachovat nebo přepsat, vyberte akci **Sloučit**.

   Systém zkontroluje, zda sloučení hodnot duplikovaného zákazníka do aktuálního zákazníka způsobí konflikty. Konflikty existují, pokud je hodnota v alespoň jednom poli primárního klíče stejná pro oba zákazníky, zatímco hodnota v poli **Číslo** je pro oba zákazníky jiná.

7. Pokud nejsou nalezeny žádné konflikty, zvolte tlačítko **Ano** v potvrzovacím okně zprávy.

   Duplicitní zákazník je přejmenován tak, aby veškeré použití jeho hodnoty v poli **Číslo** ve všech polích s vazbami na zákaznickou tabulku bylo nahrazeno hodnotou **Číslo** aktuálního zákazníka.
8. Pokud existují konflikty, vyberte před sloučením akci **Vyřešit (xx) konflikty před sloučením.** na záložce **Konflikty**.
9. Na stránce **Konflikty sloučení duplicit** vyberte řádek pro související tabulku s konfliktem a poté vyberte akci **Zobrazit podrobnosti**.

   Stránka **Sloučení duplicit** nyní zobrazuje pole ve vybrané tabulce, které způsobují sloučení mezi dvěma záznamy zákazníků. Všimněte si jak v souhrnných hodnotách v polích **Aktuální** a **Konflikt s** a na řádcích, že alespoň jedno pole primárního klíče je stejné pro oba zákazníky a hodnota pole **Číslo** se u obou zákazníků liší.
10. Pokud si nepřejete uchovávat duplicitní záznam zákazníka, vyberte akci **Odebrat duplicity** a pak vyberte tlačítko **Zavřít**.

   Identické hodnoty polí, jiné než hodnota v poli **Číslo** jsou odstraněny z duplicitních záznamu a vloženy do aktuálního záznamu.
11. Pokud chcete duplicitní záznam zákazníka po sloučení zachovat, zvolte **Přejmenovat duplicitu**.
12. Na řádcích, nikoli pro pole **Číslo**, kde má pole stejnou hodnotu na obou záznamech, změňte hodnotu v poli **Alternativní hodnota** a poté vyberte pole  **Zavřít**.

   Konfliktní hodnota pole je aktualizována na duplikátním záznamu, takže jej lze sloučit s aktuálním záznamem. Duplicitní záznam přetrvává i po sloučení.
13. Opakujte kroky 8 až 12, dokud nebudou vyřešeny všechny konflikty. Záložka **Konflikty** zmizí.
14. Na stránce **Sloučení duplicit** znovu vyberte akci **Sloučit** a poté v okně potvrzovací zprávy vyberte tlačítko **Ano**.

> [!NOTE]
> U kontaktů můžete pomocí funkce najít duplicitní kontakty před použitím stránky **Sloučení duplicit**. Pro více informací navštivte [Hledání duplicitních kontaktů](marketing-setup-contacts.md).

## Viz také
[Prodej](sales-manage-sales.md)  
[Nastavení kontaktů](marketing-setup-contacts.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
