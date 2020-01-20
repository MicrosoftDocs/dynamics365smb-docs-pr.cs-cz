---
title: Nastavení upřednostňovaných metod odesílání prodejních dokladů | Microsoft Docs
description: 'Popisuje, jak nastavit upřednostňovaný způsob odesílání prodejních dokladů jednotlivých zákazníků, například e-mail, PDF, elektronický dokument atd.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'email, PDF, electronic document'
ms.date: 03/29/2017
ms.author: sgroespe
---
# <a name="set-up-document-sending-profiles"></a>Nastavení profilů odesílání dokumentů
Můžete každému zákazníkovi nastavit upřednostňovaný způsob odesílání prodejních dokladů, takže nemusíte vybírat možnost odesílání pokaždé, když vyberete akci **Účtovat a Odeslat**.

V okně **Profily odesílání dokladů** můžete nastavit různé profily odesílání, které si můžete vybrat v poli **Profil odesílání dokladů** na kartě zákazníka. Zaškrtnutím políčka **Výchozí** lze určit, že profil odesílání dokladů je výchozím profilem pro všechny zákazníky, s výjimkou zákazníků, u kterých je v poli **Profily odesílání dokladů** vyplněn jiný profil pro odesílání.

Pokud v prodejním dokladu zvolíte akci **Účtovat a Odeslat**, **Zaúčtovat a odeslat potvrzení** zobrazí v dialogovém okně použitý profil, buď ten, který je nastaven pro zákazníka, nebo výchozí pro všechny zákazníky. V dialogovém okně můžete změnit profil pro odesílání prodejního dokladu. Další informace naleznete v [Prodejní faktury](sales-how-invoice-sales.md).

## <a name="to-set-up-a-document-sending-profile"></a>Nastavení profilu pro odesílání dokumentů
1. Zvolte ikonu ![Vyhledat stránku, nebo sestavu](media/ui-search/search_small.png "ikona vyhledat stránku, nebo sestavu"), zadejte **Profily odesílání dokladů** a pak vyberte související odkaz.
2. V okně **Profily odesílání dokladů**, vyberte akci **Nové**.
3. Vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Určení profilu odesílání na kartě zákazníka
1. Zvolte ikonu ![Vyhledat stránku, nebo sestavu](media/ui-search/search_small.png " vyhledat stránku, nebo sestavu"), zadejte **Zákazník** a pak vyberte související odkaz.
2. Otevřete kartu zákazníka, pro kterého chcete nastavit profil odesílání.
3. V poli **Profil odesílání dokladů** vyberte profil, který jste nastavili, jak je popsáno v předchozím postupu.

## <a name="see-also"></a>Viz také
[Nastavení Prodeje](sales-setup-sales.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
