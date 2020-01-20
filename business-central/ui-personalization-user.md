---
title: Přizpůsobení stránek | Microsoft Docs
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

# <a name="personalizing-your-workspace"> </a>Přizpůsobení vašeho pracovního prostoru

<!--NAV in the Web client-->

Můžete si upravit nebo *přizpůsobit* váš pracovní prostor, který bude vyhovovat vaší práci a preferencím změnou stránek tak, aby se zobrazovaly pouze ty informace, které potřebujete tam, kde jsou potřeba. Změny přizpůsobení, které provedete, ovlivní pouze váš pracovní prostor, nikoli to, co vidí ostatní uživatelé.

Podle typu stránky a jejího obsahu, můžete:

- Přidat, přesunout nebo odstranit pole.
- Přidat, přesunout nebo odstranit sloupce v seznamu.
- Změnit ukotvení podokna sloupců v seznamu. Ukotvení podokna uzamče jeden nebo více sloupců na levé straně seznamu tak, aby byly vždy k dispozici, i když horizontálně rolujete.
- Upravit šířku sloupců v seznamu.
- Přesunout nebo odstranit Hromádky (dlaždice).
- Přesunout nebo odstranit díly. Díly jsou podsekce nebo oblasti na stránce, která obsahuje věci, jako například více polí, jinou stránku, graf nebo dlaždice.

> [!NOTE]
> Kromě toho, co si uživatelé mohou přizpůsobit, i administrátoři a superuživatelé mohou přepisovat přizpůsobení uživatelů a definovat, které funkce jsou dostupné ve všech nebo jen v konkrétních společnostech. Pro více informací, navštivte [Přizpůsobení Business Central](ui-customizing-overview.md) 

## <a name="to-personalize-a-page"> </a>Pro přizpůsobení stránky

1. V pravém horním rohu vyberte ikonu ![Nastavení](media/ui-experience/settings_icon_small.png "ikona Nastavení pro Cetrum rolí") a poté vyberte **Přizpůsobit**.
   
    Banner **Přizpůsobení**  se objeví v horní části, aby naznačil, že můžete začít dělat změny.
   
    ![Mód přizpůsobení](media/ui_personalize_mode_small.png "Mód přizpůsobení")

2. Přejděte na stránku, kterou chcete přizpůsobit.
   
   Pokud v banneru vidíte ikonu zámku, přejděte na [Proč je stránka uzamčena](ui-personalization-locked.md) pro více podrobností.

3. Přesuňte ukazatel na oblast, kterou chcete přizpůsobit, například pole nebo záhlaví sloupce seznamu. Vše, co můžete přizpůsobit, je okamžitě zvýrazněno šipkou nebo rámečkem.
   
   <!--
   -  If a component can be personalized, an arrow head (![Personalization indicator arrow left](media/ui_personalize_arrow_left.png "Personalization indicator arrow left") or ![Personalization indicator arrow down](media/ui_personalize_arrow_down.png "Personalization indicator arrow down")) appears.
   -   If the component is a part, the extent of the part is indicated by a border.
   -   The freeze pane in a list is indicated by a vertical line along the entire right-side of the last column of the freeze pane.
   -->

4. Použijte tuto tabulku pro pomoc k provedení změn:     <table>
   
       <tr><th>Co chcete dělat</td><th>Jak to chcete dělat</th></tr>
       <tr><td>Něco přesunout, například pole, sloupec v seznamu, dlaždici nebo díl</td><td> Přesuňte ukazatel na cokoliv, co chcete přesunout a přetáhňete to na nové místo. Místo je označeno silnou vodorovnou nebo svislou čarou.</td></tr>
       <tr><td>Odstranění</td><td>Vyberte hrot šipky a zvolte <b>Odstranit</b> </td></tr>
       <tr><td>Přidání pole nebo sloupce</td><td>V banneru <b>Přizpůsobení</b>, zvolte <b>Více</b> a poté zvolte <b>Pole</b><br /></br>Podokno <b>Přidat pole na stránku</b> se napravo otevře. Uvádí pole, která můžete na stránku přidat. Pole označená jako <b>Umístěno</b> jsou již na stránce. Pole označená jako <b>Připraveno</b> nejsou aktuálně na stránce.<br /></br>Pro přidání pole, přetáhněte jej z podokna na potřebné místo. Místo je označeno silnou vodorovnou nebo svislou čarou.</td></tr>
       <tr><td>Změnit ukotvení podokna v seznamu do jiného sloupce</td><td>Vyberte hrot šipky sloupce, který chcete jako poslední sloupec ukotvení podokna a pak zvolte <b>Nastavit podokno</b>.<br /><br/>Pokud chcete nastavit ukotvení podokna zpět na původní navržené umístění, vyberte hrot šipky pro aktuální ukotvené podokno sloupce a zvolte <b>Vyčistit podokno</b> Poznámka: Nemůžete smazat toto ukotvení podokna.</td></tr>
       <tr><td>Změnit šířku sloupce</td><td>V záhlaví řádku tabulky přetáhněte pravé ohraničení sloupce. <br /><br />Chcete-li maximalizovat šířku sloupce tak, aby se vešel i nejdelší řádek textu ve sloupci, dvakrát klikněte na pravý okraj.</td></tr>
   
   </table>
   
   > [!IMPORTANT]  
   >   Nemůžete provádět změny v listu, pokud je list zobrazen v dlaždicích. Nejprve musíte přepnou stránku do zobrazení seznamu výběrem ikony ![Zobrazit jako seznam](media/ui_show_as_list_icon.png "Zobrazit jako seznam vlevo").

5. Můžete pokračovat v provádění změn na stejné stránce nebo se můžete přesunout na jinou stránku. Vaše změny jsou automaticky ukládány při jejich provádění. Po dokončení v banneru **Přizpůsobení** vyberte **Hotovo**.

## <a name="clear-personalization-to-change-a-page-back-to-its-original-layout"> </a>Vymazáním přizpůsobení změníte stránku zpět na původní rozvržení.

V některých případech můžete chtít vrátit zpět všechny změny přizpůsobení, které jste na stránce provedli v průběhu času, takže tato stránka bude vypadat jako původně. V banneru **Přizpůsobení**, zvolte **Více** a poté zvolte **Vyčisti přizpůsobení**.

## <a name="personalization-in-detail"> </a>Přizpůsobení v detailu

Zde je několik bodů, která vám pomohou lépe porozumět přizpůsobení:  

- Když provedete změny na stránce karty, kterou otevřete ze seznamu, změny se projeví na všech záznamech, které z tohoto seznamu otevřete. Řekněme například, že otevřete konkrétního zákazníka ze stránky Seznam zákazníků a poté stránku přizpůsobíme přidáním pole. Když otevřete další zákazníky ze seznamu, zobrazí se také pole, které jste přidali.
- Změny, které provedete, se projeví ve všech vašich Centrech rolí. Pokud například změníte Seznam zákazníků, když je Centra rolí nastaveno na Obchodní ředitel, uvidíte také změnu v Seznamu zákazníků, když je Centrum rolí nastaveno na Zpracovatel prodejních objednávek.
- Změny na stránce v podokně se projeví na stránce, kdekoliv je zobrazena.  
- Pole a sloupce můžete přidat pouze z předdefinovaného seznamu, který je založen na stránce. Nemůžete vytvářet nové.

## <a name="see-also"> </a>Viz také

[Správa přizpůsobení](ui-personalization-manage.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Změna základního nastavení](ui-change-basic-settings.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
