---
title: Consolidate Balances for a Company that is a Customer and a Vendor
description: Describes how to consolidate balances for a customer that is also a vendor.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.search.form: 5052, 21, 5050 
ms.date: 03/20/2023
ms.author: bholtorf

---
# Konsolidace zůstatků pro společnost, která je zákazníkem a dodavatelem

Společnost, se kterou obchodujete, může být zákazníkem i dodavatelem. V takovém případě se můžete vyhnout zbytečným platbám nebo příjmům a možná ušetřit na transakčních poplatcích konsolidací zůstatků zákazníků a dodavatelů společnosti. Konsolidace porovná zůstatky společnosti jako dodavatele a jako zákazníka a poté započítá částku tak, aby zůstal zůstatek zákazníka nebo dodavatele v závislosti na tom, která částka byla vyšší.

Chcete-li konsolidovat zůstatky, musíte nejprve propojit společnosti zákazníka a dodavatele prostřednictvím kontaktu, který má typ **Společnost**. Zákazník nebo dodavatel může mít pouze jeden kontakt typu **Společnost**. Další informace naleznete v části [Vytváření kontaktů](marketing-create-contact-companies.md).

Po propojení společností stránka **Karta zákazníka** nabídne pole **Zůstatek jako prodejce** a stránka **Karta dodavatele** obsahuje pole **Zůstatek jako Zákazník**.

I když to není požadavek, společnosti zákazníka a dodavatele jsou obvykle stejná právnická osoba.

## Než začnete
Před konsolidací zůstatků zadejte na stránce **Nastavení marketingu** několik nastavení.

* Na záložce **Interakce** je nutné zadat kódy obchodních vztahů v polích **Zákazníci** a **Dodavatelé**. [!INCLUDE[prod_short](includes/prod_short.md)] používá tyto informace k určení typu relace, která se má zobrazit pro kontakty.
* Volitelné: Na záložce **Duplikáty** zapněte nebo vypněte duplicitní vyhledávání. Ve výchozím nastavení je duplicitní vyhledávání zapnuto. Další informace naleznete v tématu [Zpracování duplicit](#Zpracování duplicit).

## Propojte stávajícího zákazníka a dodavatelskou společnost prostřednictvím kontaktu

Následující kroky popisují, jak propojit zákazníka a dodavatele prostřednictvím kontaktu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png " Řekněte mi, co chcete udělat"), zadejte **Zákazník** nebo **Dodavatel** a poté vyberte související odkaz.
2. Vyberte zákazníka nebo dodavatele a poté zvolte akci **Kontakt**.
3. Pokud pole **Obchodní vztah kontaktu** obsahuje jinou hodnotu než **Žádná**, je nutné relaci odebrat. Chcete-li to provést, použijte akci **Obchodní vztah** a poté vztah odstraňte.
4. V závislosti na tom, zda jste v kroku 1 vybrali **Zákazník** nebo **Dodavatel**, vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png " Řekněte mi, co chcete udělat") a poté zadejte protější stranu. To znamená, že pokud zvolíte **Dodavatel**, měli byste hledat **Zákazník**.
5. Vyberte dodavatele nebo zákazníka a poté vyberte akci **Kontakty**.
6. Zvolte akci **Propojit s existující** a poté možnost **Zákazník** nebo **Dodavatel**.
7. Vyberte zákazníka nebo dodavatele.

## Vytvoření dodavatele od zákazníka nebo naopak

Můžete vytvořit nového dodavatele od existujícího zákazníka nebo nového zákazníka od dodavatele. Na stránce **Zákazník** nebo **Dodavatel** otevřete stránku **Kontakt**. Zvolte akci **Vytvořit jako** a pak možnosti **Zákazník** nebo **Dodavatel**.

## Vytvořte nového zákazníka nebo dodavatele a propojte je prostřednictvím kontaktu na dodavatele nebo zákazníka

1. Vytvořte nového zákazníka nebo dodavatele. Další informace naleznete v tématu [Registrace nových zákazníků](sales-how-register-new-customers.md).
2. Po nastavení zákazníka nebo dodavatele zvolte akci **Vytvořit** a poté zvolte možnosti **Zákazník** nebo **Dodavatel**.

## Konsolidace zůstatků zákazníků a dodavatelů pro kontaktní společnost

Na stránce **Deník plateb** použijte akci **Čisté zůstatky zákazníků/dodavatelů** ke konsolidaci zůstatků zákazníků a dodavatelů do jedné čisté částky. Akce vytvoří, ale nezaúčtuje řádky deníku plateb, které obsahují čisté zůstatky.

> [!NOTE]
> Pokud zůstatky zákazníka nebo dodavatele obsahují částky, které jsou v různých měnách, vytvoří se řádek pro částku v každé měně.

## Zpracování duplicit

Pokud zapnete duplicitní vyhledávání na záložce **Duplikáty** na stránce **Nastavení marketingu**, zobrazí se upozornění při změně hodnot polí, která jsou součástí nastavení duplicitních vyhledávacích řetězců. Když je nalezen duplikát, můžete provést následující akce:

* Zkombinujte duplicitní kontakty do jednoho kontaktu, který je stejný pro zákazníka i dodavatele pomocí funkce **Sloučit s** na stránce **Karta kontaktu**. Sloučení kontaktů se obvykle provádí pouze v případě, že zákazník a dodavatel jsou stejná právnická osoba. Další informace naleznete v tématu [Sloučení duplicitních záznamů](sales-how-merge-duplicate-records.md).
* Odstraňte obchodní vztah dodavatele pro kontakt dodavatele nebo zákazníka a potom pomocí akce **Odkaz na existující** vytvořte odkaz na jiný kontakt.

## Viz také

[Prodej](sales-manage-sales.md)
[Evidence nových zákazníků](sales-how-register-new-customers.md)  
