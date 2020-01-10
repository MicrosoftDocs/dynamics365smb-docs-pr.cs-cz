---
title: Share contacts between Business Central and Outlook| Microsoft Docs
description: This service has deep integration with Office 365 so you can share contacts between Outlook and Business Central.
author: edupont04

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Office 365
ms.date: 04/01/2019
ms.author: edupont

---
# Synchronizace kontaktů v Business Central s kontakty v Microsoft Outlook
Stejné kontakty můžete vidět v [!INCLUDE[d365fin](includes/d365fin_md.md)] jako v aplikaci Outlook, pokud nastavíte synchronizaci kontaktů. Pokud jste například prodejce, můžete provést část práce v aplikaci Outlook a další část v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pokud jsou kontakty na obou místech stejné, je vaše práce jednodušší.

Vyhrazená složka v aplikaci Outlook usnadňuje vyhledávání kontaktů a umožňuje nastavit filtr tak, aby synchronizoval pouze kontakty z aplikace [!INCLUDE[d365fin](includes/d365fin_md.md)], které chcete zobrazit v aplikaci Outlook. Jakmile je nastavena synchronizace kontaktů, můžete zahájit synchronizaci ručně nebo nastavit automatickou synchronizaci, která udrží kontakty synchronizované podle plánu.

## Nastavení synchronizace
Nastavte způsob, jakým chcete synchronizovat kontakty s aplikací Outlook na stránce **Nastavení synchronizace  Exchange** v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Předpokladem je, že váš uživatelský profil v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)] musí obsahovat e-mailový účet sady Office 365. Můžete to zkontrolovat v části **Ověření Office 365** na svém uživatelském profilu v seznamu **Uživatelé**.

Potom na stránce **Nastavení synchronizace  Exchange**, můžete ověřit, že připojení k serveru Exchange funguje, a poté nastavit synchronizaci kontaktů. Otevřete stránku **Nastavení synchhronizace  kontaktů** a spusťte synchronizaci. Volitelně můžete nastavit filtr, pro který budou kontakty synchronizovány mezi [!INCLUDE[d365fin](includes/d365fin_md.md)] a Outlook. Můžete například nastavit filtr na jméno, typ, společnost nebo podobné. Můžete také změnit výchozí název složky, do které budou kontakty synchronizovány v aplikaci Outlook. Výchozí název je *Business Central*.

Po nastavení této synchronizace se veškeré změny kontaktu provedené v aplikaci Outlook nebo v [!INCLUDE[d365fin](includes/d365fin_md.md)] synchronizují s ostatními.

Každý z vašich spolupracovníků může také nastavit vlastní synchronizaci serveru Exchange a nastavit vlastní filtr pro synchronizaci kontaktů.

## Synchronizace kontaktů
Při práci s kontakty v aplikaci [!INCLUDE[d365fin](includes/d365fin_md.md)] je snadné spustit synchronizaci ručně, kdykoli se vám bude hodit ze **Seznamu kontaktů.** Jednoduše zvolte tlačítko **Synchronizovat s Office 365** a rozhodněte, zda chcete změnit nastavený filtr. Když zvolíte tlačítko OK, synchronizace se spustí okamžitě a poslední změny se projeví u vašich kontaktů v aplikaci Outlook.

V seznamu **Kontaktů** můžete kontakty synchronizovat dvěma způsoby:

* **Synchronizace s Office 365**

   Tato akce synchronizuje všechny změny z [!INCLUDE[d365fin](includes/d365fin_md.md)] do Office 365 od předchozí synchronizace na základě data dle poslední modifikace. Všechny nové kontakty z Office 365 budou také synchronizovány zpět do [!INCLUDE[d365fin](includes/d365fin_md.md)]. Toto je obvykle rychlejší než provedení úplné synchronizace.

* **Plná synchronizace s Office 365**

   Tato akce synchronizuje všechny kontakty v obou směrech bez ohledu na datum poslední synchronizace a datum poslední změny.

V obou případech jsou kontakty synchronizovány z aplikace Outlook, pouze pokud mají vyplněna povinná pole. Povinná pole pro synchronizaci s Office 365 jsou **Jméno**, **E-mailová adresa** a kontakt musí být typu Osoba. [!INCLUDE[d365fin](includes/d365fin_md.md)] je zdroj informací o kontaktu, takže [!INCLUDE[d365fin](includes/d365fin_md.md)] kontaktní informace budou uloženy v případě duplicity.

V aplikaci Outlook jsou kontakty z [!INCLUDE[d365fin](includes/d365fin_md.md)] zobrazeny ve složce pod **Ostatní kontakty** v zobrazení **Osoby**. Pokud nejste obeznámeni s zobrazením osob v aplikaci Outlook, můžete se k ní dostat z možností navigace v levém dolním rohu aplikace Outlook.

## Viz také
[Začínáme](product-get-started.md)  
[Finance](finance.md)  
[Prodej](sales-manage-sales.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Použití kontaktů (Osob) ve webové aplikaci Outlook](https://support.office.com/en-us/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)
