---
title: Use Invoicing and Business Central | Microsoft Docs
description: Workaround for accessing Microsoft Invoicing when you have signed up for Dynamics 365 Business Central.
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/30/2020
ms.author: bholtorf

---
# Použití stejného účtu sady Office 365 v [!INCLUDE[d365fin](includes/d365fin_long_md.md)] a Microsoft Invoicing
Když si zaregistrujete na zkoušku [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete přejít na 30-denní zkušební dobu, a poté můžete zahájit předplatné nebo můžete přestat používat [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ve všech případech jste někdy mohli vidět něco, co se nazývá **Microsoft Invoicing** a kliknout na něj. Jednalo se o aplikaci, která byla součástí toho, co je nyní Microsoft 365 Business Standard, dříve známý jako Předplatné Office 365 Business Premium, proto ne každý uvidí dlaždici v jejich Office 365 prostředí.

Microsoft Invoicing již není k dispozici, ale pokud se chcete přihlásit k Invoicing pro načtení dat, může se zobrazit zpráva, že nemáte přístup k Microsoft Invoicing, protože Váš účet je použit v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Podobnou zprávu uvidíte pokud nainstalujete mobilní aplikaci Invoicing.

## Řešení
Invoicing a [!INCLUDE[d365fin](includes/d365fin_md.md)] sdílejí stejnou platformu. To znamená, že jste rozpoznáni jako stávající uživatel [!INCLUDE[d365fin](includes/d365fin_md.md)] když kliknete na Microsoft 365 centrum pro správu. Důvodem je, že Invoicing nemůže používat stejnou společnost jako [!INCLUDE[d365fin](includes/d365fin_md.md)].

Budete se tedy muset přihlásit do [!INCLUDE[d365fin](includes/d365fin_md.md)] a přejmenovat svou stávající společnost a poté vytvořit novou společnost, kterou pak můžete použít ve Invoicing. Během tohoto zástupného řešení nejsou přesunuta ani přepsána žádná data.

### Přejmenování společnosti
1. Přihlašte se do [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. V pravém horním rohu zvolte **Nastavení** ikonu ![Nastavení](media/ui-experience/settings_icon_small.png "Nastavení pro Centrum rolí") a pak zvolte Moje nastavení .
3. V poli **Společnost**, vyberte jinou společnost.
4. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Společnosti** a vyberte související odkaz.
5. Na stránce **Společnosti**, zvolte **Upravit seznam**.
6. Změňte název *Má společnost* na něco jiného.

   Počkejte několik minut V základní databázi provedeme řadu změn a to chvíli potrvá.
7. Až bude systém opět připraven, zvolte **vytvořit novou společnost**.
8. V dialogovém okně, které se zobrazí, zadejte název jako *Moje společnost*, a zvolte **Výroba – pouze nastavení dat**.

To opět trvá několik minut. Po dokončení procesu budete mít přístup k Invoicing jako součást prostředí Microsoft 365 Business Standard. ale pouze pro export dat, protože aplikace Invoicing je zastaralá.

### A co moje data?
Při přejmenování původní Mé společnosti, databázové tabulky, které ukládají Vaše stávající data v [!INCLUDE[d365fin](includes/d365fin_md.md)] jsou přejmenována, ale samotných dat se nedotknete.

Pokud používate oboje Invoicing a [!INCLUDE[d365fin](includes/d365fin_md.md)], data jsou uložen na dvou místech (dvě společnosti). Nic není sdíleno, takže budete muset spravovat zákazníky a zboží v obou společnostech.

## Viz také
[Často kladené otázky](across-faq.md)  
[Administrace](admin-setup-and-administration.md)
