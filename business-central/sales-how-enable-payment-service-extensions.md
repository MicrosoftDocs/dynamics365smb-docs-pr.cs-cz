---
title: Povolení platbeb zákazníků prostřednictvím platebních služeb | Microsoft Docs
description: Usnadníte zákazníkům zaplacení faktur povolením platebních služeb.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="enable-customer-payments-through-payment-services"></a>Povolení platby zákazníků prostřednictvím platebních služeb
Jako alternativu k vybírání plateb prostřednictvím bankovních převodů nebo kreditních karet Vám Vaši zákazníci mohou zaplatit prostřednictvím svého účtu u platebních služeb, jako je například Microsoft Pay, PayPal nebo WorldPay.  

Po povolení platebních služeb v [!INCLUDE[d365fin](includes/d365fin_md.md)], je k dispozici odkaz na tuto službu v prodejních dokladech, které odesíláte e-mailem vašim zákazníkům. Zákazníci mohou pomocí tohoto odkazu přejít na platební službu a zaplatit účet přímo z prodejního dokladu. Pokud nechcete zahrnout odkaz, například pokud zákazník zaplatí hotovostí, můžete před zaúčtováním odebrat platební službu z faktury.  

V [!INCLUDE[d365fin](includes/d365fin_md.md)] jsou instalovány standardní rozšíření Microsoft Pay, PayPal Payments Standart a WorldPay Payments a připraveny k povolení.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365fin_mdmd"></a>Povolení platební služby v [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Služby pro platby** a poté vyberte související odkaz.  
2. Na stránce **Služby pro platby**, vyberte akci **Nové**.  
3. Vyberte platební službu a poté zavřete stránku.  
4. Na stránce **Služby pro platby**, vyberte akci **Instalace**.  
5. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Zavřete stránku.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Pro výběr platební služby na prodejní faktuře
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní faktury** a poté vyberte související odkaz.  
2. Otevřete prodejní fakturu, kterou chcete uhradit pomocí platební služby.  
3. Na poli **Služby pro platby**, vyberte platební službu.  

    > [!NOTE]  
    > Pole **Služby pro platby** je k dispozici pouze v případě, že jste povolili platební službu.  

## <a name="see-also"></a>Viz také  
[Nastavení Prodeje](sales-setup-sales.md)  
[Prodej](sales-manage-sales.md)  
[Přizpůsobení [!INCLUDE[d365fin](includes/d365fin_md.md)] Pomocí rozšíření](ui-extensions.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
