---
title: Fakturace Vašich rezervací Business Central | Microsoft Docs
description: 'Naučte se, jak můžete provádět hromadnou fakturaci z Microsoft Bookings v Business Central'
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'invoicing, bookings'
ms.date: 01/07/2019
ms.author: edupont
---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365fin_mdmd"></a>Hromadná fakturace v Microsoft Bookings v  [!INCLUDE[d365fin](includes/d365fin_md.md)]
Pokud vaše společnost používá aplikaci Bookings v Office 365, můžete provést hromadnou fakturaci. Stránka **Booking Nevyfakturované položky** v [!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje seznam dokončených rezervací společnosti. Na této stránce můžete rychle vybrat události, které chcete fakturovat, a vytvořit návrhy faktury za poskytované služby.  

## <a name="connect-to-bookings"></a>Připojení k Bookings
Chcete-li se spojit v [!INCLUDE[d365fin](includes/d365fin_md.md)] s Bookings, musíte určit Účetní společnost, co synchronizovat s Bookings, jak často synchronizovat a jaké šablony použít. Tyto položky můžete nastavit v **Booking Nastavení  synchronizace**, kterou můžete spustit z **Nastavení synchronizace  Exchange**, kterou můžete najít skrz [Vyhledat](ui-search.md)  

Pokud například chcete synchronizovat zákazníky mezi Bookings a [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte určit výchozí šablonu, pomocí které se budou přidávat noví zákazníci v [!INCLUDE[d365fin](includes/d365fin_md.md)] na základě zákazníků ve vaší Účetní společnosti.  

> [!NOTE]
> Aplikace Bookings je určena k rezervování schůzek pro jednotlivé zákazníky, než pro společnosti. Synchronizace s [!INCLUDE[d365fin](includes/d365fin_md.md)] bude tedy pouze synchronizovat kontakty se zákazníkem s typem „Osoba“. Pro synchronizaci je potřeba zadat také e-mailovovou adresu.  

Podobně, jako když chcete synchronizovat předměty servisu mezi Bookings a [!INCLUDE[d365fin](includes/d365fin_md.md)], musíte určit výchozí šablonu, pomocí které se budou přidávat nové předměty servisu v [!INCLUDE[d365fin](includes/d365fin_md.md)] na základě služeb ve vaší Účetní společnosti.  

> [!NOTE]
> Pouze položky typu *Služby* se budou synchronizovat mezi Bookings a [!INCLUDE[d365fin](includes/d365fin_md.md)]. Šablona, kterou jste nastavili na stránce **Konfigurační šablony**, aby mohla být použita pro synchronizaci položky, musí být definována jako *Služba*.

## <a name="invoice-appointments"></a>Fakturační události
Když je čas poslat faktury za dokončené rezervace, běžte na stránku **Nefakturované rezervace**. V závislosti na tom, jak často jsou informace synchronizovány, je seznam dlouhý nebo krátký. Můžete vytvářet faktury pro všechny rezervace v seznamu nebo jednu rezervaci najednou. V seznamu můžete vybrat jednu nebo více položek a fakturovat je pouze je.  

Podpora Fakturační události z Bookings je jednodušší než workflow práce s prodejními nabídkami, prodejními objednávkami a prodejními fakturami. Další informace naleznete v [Prodejní faktury](sales-how-invoice-sales.md). Můžete si vybrat, zda chcete své služby prodat pomocí [!INCLUDE[d365fin](includes/d365fin_md.md)], nebo si vybrat, zda chcete rezervovat Bookings, v závislosti na vašich obchodních potřebách.  

## <a name="see-also"></a>Viz také
[Finance](finance.md)  
[Prodejní faktury](sales-how-invoice-sales.md)  
[Nastavení Prodeje](sales-setup-sales.md)  
[Microsoft Bookings](https://products.office.com/en-us/business/scheduling-and-booking-app)  
