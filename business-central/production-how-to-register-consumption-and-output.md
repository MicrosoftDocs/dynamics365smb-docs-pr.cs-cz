---
    title: Register Consumption and Output for One Production Order | Microsoft Docs
    description: This execution task is performed on the **Production Journal** page. The journal combines the functions of the separate consumption journal and output journals into one journal. The combined journal is accessed directly from a released production order. Its main purpose is to manually post the consumption of components, the quantity of end items produced, and the time spent in operations.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Zaúčtování spotřeby a výstupu pro jeden řádek vydané výrobní zakázky
Tato úloha se provádí na stránce **Deník výroby**. Deník kombinuje funkce samostatného deníku spotřeby a deníků výstupů do jednoho deníku. Kombinovaný deník je přístupný přímo z vydané výrobní zakázky. Jeho hlavním účelem je manuální účtování spotřeby komponent, množství vyrobeného konečného zboží a čas strávený v provozu. Hodnoty jsou zaúčtovány do položek v rámci vydané výrobní zakázky. Spotřební množství jsou zaúčtovány jako záporné položky zboží, výstupní množství jsou zaúčtovány jako kladné položky a vynaložené časy jsou zaúčtovány jako položky kapacity. Tyto zaúčtované hodnoty lze také zobrazit ve spodní části deníku jako skutečné množství.

> [!NOTE]
> Protože jsou data o spotřebě zpracovávána společně s výstupními daty, nabízí tento deník příležitost zobrazit propojené komponenty a operace v logické struktuře procesů. Komponenty jsou odsazeny podle jejich příslušných operací. To vyžaduje použití kódů vazeb TNG postupu.

> [!NOTE]
> Komponenty bez kódů vazeb TNG postupu jsou uvedeny jako první v deníku.

## Registrace spotřeby a výstupu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vydané výr.  zakázky** a poté vyberte související odkaz.
2. Otevřete vydanou výrobní zakázku, která je připravena k registraci, a poté na záložce **Řádky** vyberte akci **Řádek** a potom vyberte akci **Deník výroby**.

   Otevře se stránka **Deník výroby** ukazující řádky deníku pro výrobní zakázku podle stránek **Komponenta  výrobní zakázky** a **TNG  postup výrobní zakázky**. Tyto řádky pocházejí z výrobního kusovníku a TNG postupu přiřazeného k vyráběnému zboží. Pro více informací navštivte [Vytvoření výrobních kusovníků](production-how-to-create-routings.md).

3. Do pole **Zúčtovací datum** v horní části deníku zadejte zúčtovací datum, které se vztahuje na všechny řádky. Ve výchozím nastavení je zadáno pracovní datum. Pole má sloužit jako rychlý způsob, jak zarovnat data účtování na všech řádcích, je-li to relevantní.

   > [!NOTE]
   > Zúčtovací data zadaná na jednotlivých řádcích toto pole přepíše.

4. V poli **Filtr metody spotřeby** v horní části deníku můžete také zobrazit spotřebu a výstup, který je zaúčtován automaticky podle metod vyprázdnění definovaných pro zboží a zdroj.

   Na každém typu řádku v deníku se zobrazí pouze příslušná pole. Ostatní pole jsou prázdné a chráněné proti zápisu.

   Při otevření deníku je přednastaveno množství, které má být zaúčtováno. Pokud není dosud nic zaúčtováno, všechna pole množství budou ve výchozím nastavení zobrazovat očekávaná množství převedená z výrobní zakázky. Pokud byly provedeny dílčí účtování, v polích množství na řádcích se zobrazí zbývající množství. Množství a časy již zaúčtované pro zakázku jsou zobrazeny v dolní části deníku jako skutečné položky.

   Pokud jde o množství v poli **Výstupní množství**, máte možnost nastavit hodnoty, které se mají přednastavit při prvním otevření deníku. To se provádí na stránce **Nastavení výroby** na záložce **Obecné** v poli **Přednastav. výstupní množství**.

5. Pokračujte zadáním příslušné spotřeby a výstupních množství do upravitelných polí.

   > [!NOTE]
   > Pouze výstupní množství na posledním řádku záznamu typu záznamu **Výstup** upraví úroveň zásob při účtování deníku. Proto nezaúčtujte deník s přednastaveným očekávaným výstupním množstvím na posledním výstupním řádku, dokud nebude všechno koncové zboží skutečně vyrobeno.

6. Vyberte pole **Dokončeno** na výstupních řádcích, což znamená, že operace je dokončena. Toto pole souvisí s polem **Stav postupu** na řádku TNG postupu výrobní zakázky.
7. Vyberte akci **Účtovat**, chcete-li evidovat množství, která jste zadali, a potom deník zavřete.

Pokud hodnoty zůstanou zaúčtovány, deník bude obsahovat tyto zbývající hodnoty při příštím otevření. Zaúčtované hodnoty jsou zobrazeny jako skutečné hodnoty v dolní části deníku.

> [!NOTE]
> Pokud je spotřebované zboží zablokováno, deník nebude účtovat spotřební množství tohoto zboží. Je-li strojní nebo pracovní centrum zablokováno, deník nezaúčtuje výstupní množství ani dobu zpracování pro daný řádek výstupu.

> [!NOTE]
> Pokud zavřete deník bez účtování, budou změny ztraceny.

> [!WARNING]
> Stránku **Deník výroby** nemohou dva uživatelé používat současně. To znamená, že pokud uživatel 2 otevře stránku a zadá data, když uživatel 1 již pracuje na stránce, může uživatel 2 ztratit data, když uživatel 1 zavře stránku.

## Viz také
[Výroba](production-manage-manufacturing.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
