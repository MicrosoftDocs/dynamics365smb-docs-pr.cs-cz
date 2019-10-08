---
title: Správa přizpůsobení jako správce v Business Central | Microsoft Docs
description: 'Naučte se, jak přizpůsobit uživatelské rozhraní tak, aby vyhovovalo vašemu způsobu práce.'
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.date: 10/01/2018
ms.author: jswymer
---
# <a name="managing-personalization-as-an-administrator"></a>Správa přizpůsobení jako správce
<!--NAV in the Web client-->
Uživatelé si mohou přizpůsobit svůj pracovní prostor podle svých vlastních preferencí. Jako správce můžete ovládat a spravovat přizpůsobení tím, že zakážete uživatelům možnost přizpůsobit stránky a vymažete všechna přizpůsobení stránek, která uživatelé měli.

## <a name="disable-personalization-for-a-profile"></a>Zakázání přizpůsobení profilu
Můžete zabránit všem uživatelům, kteří patří k určitému profilu, možnost přizpůsobení svých stránek.
1.  Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Přehled profilů** a poté vyberte související odkaz.
2.  Vyberte profil ze seznamu, který chcete upravit.
3. Zaškrtněte políčko **Zakázat přizpůsobení** a poté klepněte na tlačítko **OK**.

## <a name="clear-user-personalizations"></a>Vymazání přizpůsobení uživatelů

Vymazání přizpůsobení stránky změní stránku zpět na původní rozvržení před provedením jakéhokoli přizpůsobení, Existují dva způsoby, jak vymazat přizpůsobení, která uživatelé na stránkách provedli: pomocí stránky **Odstranit přizpůsobení uživatelem** a pomocí stránky **Karta přizpůsobení uživateli**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Vymazání přizpůsobení uživatele pomocí stránky Odstranit přizpůsobení uživatelem

Stránka **Odstranit přizpůsobení uživatelem** umožňuje vymazat jednotlivá přizpůsobení na stránce pro každého uživatele zvlášť.

1.  Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Odstranit přizpůsobení uživatelem** a poté vyberte související odkaz.

    Na stránce jsou uvedeny všechny stránky, které byly přizpůsobeny a uživatel, k němuž patří.

    >[!NOTE]
    > Zaškrtnutí ve sloupcích **Starší verze přizpůsobení** označuje, že přizpůsobení bylo provedeno ve starší verzi [!INCLUDE[d365fin](includes/d365fin_md.md)], která zpracovávala přizpůsobení jinak, než se to dělá teď. Uživatelé, kteří se pokoušejí přizpůsobit tyto stránky, jsou uzamčeni, pokud se rozhodnou stránku odemknout. Pro více informací, navštivte [Proč je stránka uzamčena před přizpůsobením](ui-personalization-locked.md).

2. Vyberte položku, kterou chcete odstranit, a poté vyberte akci **Odstranit**.

    Uživatel uvidí změny při příštím přihlášení.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Vymazání přizpůsobení uživatele pomocí stránky Karta přizpůsobení uživateli

Stránka **Karta přizpůsobení uživateli** umožňuje vymazat přizpůsobení na všech stránkách konkrétního uživatele. To vyžaduje oprávnění k zápisu do Tabulky 2000000072 **Profil**.

1.  Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Přizpůsobení uživatelem** a poté vyberte související odkaz.

    Na stránce **Přizpůsobení uživatelem** jsou uvedeny všichni uživatelé, kteří mají potenciálně přizpůsobené stránky. Pokud nemůžete najít uživatele v seznamu, znamená to, že nemá žádné přizpůsobené stránky.

2. Vyberte uživatele ze seznamu a poté zvolte akci **Upravit**.

3.  Na záložce **Akce** zvolte **Vymazat přizpůsobené stránky**.

    Uživatel uvidí změny při příštím přihlášení.

## <a name="see-also"></a>Viz také
[Přizpůsobení Vašeho Pracovního prostoru](ui-personalization-user.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Změna základního nastavení](ui-change-basic-settings.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
