---
title: Přiřazení uživatelských oprávnění a vytvoření nebo úprava sad oprávnění | Microsoft Docs
description: 'Popisuje, jak přidat uživatele Office 365 do Business Central a poté přiřadit oprávnění, přístupová práva a nastavení zabezpečení.'
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'access, right, security'
ms.date: 03/08/2018
ms.author: sgroespe
---
# <a name="manage-users-and-permissions"></a>Správa uživatelů a práv
Chcete-li přidat uživatele do [!INCLUDE [d365fin](includes/d365fin_md.md)], musí správce vaší společnosti Office 365 nejprve vytvořit uživatele v Admin Center Office 365. Pro více informací navštivte [Přidejte uživatele do Office 365 pro firmy](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Jakmile jsou uživatelé vytvořeni v Office 365, mohou být importováni do okna **Uživatelé** pomocí akce **Získat uživatele z Office 365**. Uživatelům jsou přiřazeny sady oprávnění v závislosti na plánu přiřazeném uživateli v Office 365.

Poté můžete přistoupit k přiřazení sad oprávnění uživatelům, k definování, které databázové objekty a ke kterým prvkům uživatelského rozhraní, mají uživatelé přístup a ve kterých společnostech. Můžete přidat uživatele do skupin uživatelů. To usnadňuje přiřazení stejných sad oprávnění více uživatelům.

Sada oprávnění je souhrn oprávnění pro konkrétní objekty v databázi. Všichni uživatelé musí mít před přístupem [!INCLUDE [d365fin](includes/d365fin_md.md)] přidělenu jednu nebo více sad oprávnění. Ve výchozím nastavení je k dispozici řada předdefinovaných sad oprávnění. Můžete tyto předdefinované sady oprávnění použít, změnit jich nebo vytvořit další sady oprávnění.

Správci mohou pomocí okna **Nastavení uživatele** definovat časové intervaly, během nichž jsou určití uživatelé schopni účtovat položky, a také určit systémové protokoly množství času, po který jsou uživatelé přihlášeni.

## <a name="to-assign-permissions-to-a-user"></a>Přiřazení oprávnění uživateli
1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Uživatelé** a pak vyberte související odkaz.
2. Vyberte uživatele, kterému chcete přiřadit oprávnění.
   Všechny sady oprávnění, které jsou již uživateli přiřazeny, jsou zobrazeny v FactBoxu **Sad oprávnění**.
3. Zvolte akci **Upravit** a otevřete okno **Karta uživatele**.
4. Na záložce s náhledem **Sady oprávnění uživatele**, na novém řádku vyplňte pole podle potřeby. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Seskupení uživatelů do skupin uživatelů
Můžete nastavit skupiny uživatelů, které vám pomohou spravovat sady oprávnění pro skupiny uživatelů ve vaší společnosti. Pomocí funkce můžete zkopírovat všechny sady oprávnění z existující skupiny uživatelů do nové skupiny uživatelů. Členové uživatelské skupiny nejsou zkopírováni.

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Skupiny uživatelů** a pak vyberte související odkaz.
2. Případně v okně **Uživatelé** vyberte akci **Skupiny uživatelů**.
3. V okně **Uživatelé** vyberte akci **Členové skupiny uživatelů**.
6. V okně **Členové skupiny uživatelů** vyberte akci **Přidat uživatele**.
7. Chcete-li přidat nové nebo další sady oprávnění, vyberte v okně **Skupin uživatelů** akci **Sady oprávnění skupiny uživatelů**.
8. V okno **Sady oprávnění skupiny uživatelů**, na novém řádku vyplňte pole podle potřeby výběrem ze stávajících sad oprávnění.

## <a name="to-set-up-user-time-constraints"></a>Nastavení uživatelských časových omezení
Správci mohou definovat časové období, během kterého jsou určití uživatelé schopni účtovat položky, a také určit systémové protokoly množství času, po který jsou uživatelé přihlášeni. Administrátoři mohou také uživatelům přiřadit centra odpovědnosti. Pro více informací navštivte [Práce s Centry zodpovědnosti](inventory-responsibility-centers.md).

1. Zvolte ikonu ![Vyhledat stránku nebo sestavu](media/ui-search/search_small.png "Ikona Vyhledat stránku nebo sestavu"), zadejte **Nastavení uživatelů** a pak vyberte související odkaz.
2. V okně **Nastavení uživatelů** vyberte akci **Nový**.
3. Do pole **ID uživatele** zadejte ID uživatele nebo vyberte pole pro zobrazení všech aktuálních uživatelů systému Windows v systému.
4. Vyplňte pole podle potřeby.

## <a name="see-also"></a>Viz také
[Příprava na podnikání](ui-get-ready-business.md)  
[Nastavení a správa [!INCLUDE[d365fin](includes/d365fin_md.md)]](admin-setup-and-administration.md)  
[Vítejte v [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
