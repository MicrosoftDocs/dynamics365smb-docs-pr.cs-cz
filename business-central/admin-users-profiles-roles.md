---
title: Manage users and roles
description: Learn how to manage user profiles and Role Centers in Business Central. Profiles allow administrators to centrally define and manage what users can see and do.
author: SorenGP


ms.topic: conceptual
ms.search.keywords: profiles, users
ms.search.form: 9171
ms.date: 06/14/2021
ms.author: edupont

---
# Správa uživatelských profilů

Všichni uživatelé [!INCLUDE[prod_short](includes/prod_short.md)] mají přiřazený profil, který odráží jejich obchodní roli, oddělení, ve kterém pracují nebo jinou kategorizaci. Profily umožňují správcům centrálně definovat a spravovat, co mohou různé typy uživatelů vidět a dělat v uživatelském rozhraní, aby mohli efektivně plnit své pracovní úkoly.

> [!NOTE]
> Typickým využitím obchondího profilu je role. Profil se proto v uživatelském rozhraní nazývá *Profil (Role)*.

Jako správce vytváříte a spravujete profily na stránce **Profily (role)**. Každý profil má kartu, na které lze spravovat různá nastavení související role, například název role, uživatelská nastavení a to, které Centrul rolí profil používá. Další informace o uživatelských nastaveních a Centrech rolí naleznete v tématu [Změna základního nastavení](ui-change-basic-settings.md).

Než budete moct spravovat profily uživatelů, musí se uživatelé vytvořit a přidat prostřednictvím Centra pro správu Microsoft 365. Poté můžete každému uživateli nebo skupině uživatelů přiřadit oprávnění k definování funkcí, které mohou prohlížet a/nebo upravovat. Další informace o oprávněních naleznete v tématu [Přiřazení práv uživatelům a uživatelským skupinám](ui-define-granular-permissions.md).

## Přizpůsobení stránky
Rozložení stránek pro profil můžete přizpůsobit tak, aby všichni uživatelé přiřazení k profilu viděli tyto přizpůsobené stránky. Jako správce přizpůsobujete stránky pomocí stejných funkcí jako uživatelé při přizpůsobování. Pro další informace se podívejte na [Přizpůsobení stránek pro profily](ui-personalization-manage.md).

## Vytvoření profilu

Pokud nemůžete zkopírovat existující profil, můžete vytvořit nový ručně.

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "Hledat ikonu stránky nebo sestavy"), zadejte **Profily (role)** a poté vyberte související odkaz.
2. Na stránce **Profily (role)** vyberte akci **Nový**.
3. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Pokud chcete, aby byl určitý profil dostupný pouze pro velmi specifické uživatele, můžete pole **Popis** nastavit na `Pouze navigační nabídka`. Tímto způsobem je profil vyloučen ze seznamu dostupných rolí v **Mých nastavení**.

## Kopírování profilu
Chcete-li ušetřit čas, můžete vytvořit nový profil zkopírováním existujícího profilu. Zkopírujte ten, který má podobné nastavení jako ten, který chcete vytvořit.

> [!NOTE]
> Při kopírování profilu se zkopírují i všechna příslušná přizpůsobení stránky, a to jak uživatelsky vytvořená, tak ta z rozšíření.

1. Na stránce **Profily (role)** vyberte řádek profilu, který chcete zkopírovat, a pak zvolte akci **Kopírovat profil**.
2. Vyplňte pole **ID profilu** a **Zobrazit název** a klikněte na tlačítko **OK**.
3. Na stránce **Profily (role)** otevřete nově vytvořenou kartu profilu a podle potřeby upravte další pole.

## Úprava profilu
Profil můžete upravit změnou polí na stránce **Profil (Role)**. Změny však nebudou viditelné pro uživatele přiřazeného k profilu, dokud se neodhlásí a znovu nepřihlásí.

> [!Caution]
> Nepřejmenovávejte profil, pokud jsou uživatelé přiřazení k profilu přihlášeni, protože uživatelé mohou zaznamenat, že Business Central zamrzne a bude nutné jej restartovat.

## Přiřazení profilu uživateli
Uživatelé si mohou přiřadit roli (představující profil) výběrem pole **Role** na stránce **Moje nastavení**. Jako správce můžete provést totéž prostřednictvím stránky **Profily (Role)**.

1. Na stránce **Profily (role)** vyberte profil, který chcete přiřadit, a pak zvolte akci **Seznam přizpůsobení uživateli**.
2. Na stránce **Uživatelská nastavení** vyberte uživatele, kterému chcete profil přiřadit, a pak zvolte akci **Upravit**.
3. V poli **ID profilu** vyberte příslušný profil.

> [!NOTE]
> Pokud uživateli přiřadíte jiný profil, veškeré personalizace provedené uživatelem v předchozím profilu zůstanou zachovány.

## Definování uživatelských nastavení pro profil
Na stránce **Moje nastavení** mohou uživatelé definovat základní chování svého účtu, například Centrum rolí, jazyk a oznámení, která dostávají. Pro více informací navštivte [Změna základního nastavení](ui-change-basic-settings.md).

Jako správce můžete definovat tato nastavení pro profil a tím použít nastavení pro všechny uživatele související role.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Profily (role)** a poté vyberte související odkaz.
2. Vyberte řádek pro profil, pro který chcete změnit nastavení uživatele, a pak zvolte akci **Seznam přizpůsobení uživateli**.
3. Na stránce **Individuální nastavení uživatelů** otevřete kartu pro uživatele, jehož nastavení chcete změnit.
4. Na stránce **Uživatelská nastavení** upravte pole podle potřeby.

## Aktivace profilu
Při vytváření profilu můžete zaškrtnout různá políčka, která definují, zda, kde a jak jsou profil a jeho informace zpřístupněny uživatelům.

* Na stránce **Profil (role)** zaškrtněte následující políčka:
   - **Povoleno** určující, zda je souvisejicí profil viditelný na stránce **Dostupné role**, ze kterých si uživatelé mohou vybrat.
   - **Použít jako výchozí profil** k určení profilu, který se vztahuje na uživatele, kterým není přiřazena konkrétní role.
   - **Zakázat přizpůsobení** určující, zda uživatelé role mohou přizpůsobit svůj pracovní prostor.
   - **Zobrazit v Průzkumníku Role** určuje, jestli se akce s obchodními funkcemi zahrnutými v profilu zobrazí v rozšířeném zobrazení Průzkumníka rolí, což je přehled funkcí. Pro více informací navštivte [Vyhledávání stránek pomocí Průzkůmníka rolí](ui-role-explorer.md).

## Export profilů
Profily můžete exportovat z [!INCLUDE[prod_short](includes/prod_short.md)], například pro opětovné použití v jiném tenantovi. Profily jsou exportovány do souboru ZIP obsahujícího soubory AL, které lze znovu použít k vývoji rozšíření. Pro více informací navštivte [Použití klienta k vytváření přizpůsobení profilů a stránek](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

* Na stránce **Profily (role)** vyberte akci **Export profilů**.

Exportuje se soubor ZIP se soubory .al pro všechny profily.

## Import profilů
Můžete importovat profily, které byly exportovány z [!INCLUDE[prod_short](includes/prod_short.md)]. Kroky jsou víceméně opačné než kroky pro export profilů. Pro více informací navštivte  [Export profilů](admin-users-profiles-roles.md#to-export-profiles).

1. Na stránce **Profily (role)** vyberte akci **Import profilů**.
2. Postupujte podle pokynů v Průvodci **Importu profilů**.

   Chcete-li importovat pouze vybrané profily, pomocí zaškrtávacího políčka ** Vybrané** určete, které chcete importovat.
3. Zvolte tlačítko **Importovat vybrané**.

Importuje se soubor zip se soubory .al pro vybrané profily.

## Odstranění profilu
Profil můžete odstranit výběrem akce **Odstranit** na stránce **Profily (role)**. Platí však následující omezení:

- Nemůžete odstranit profil, který je přiřazen uživateli nebo skupině uživatelů.
- Profily, které pocházejí z rozšíření, nelze odstranit. Rozšíření je nutné nejprve odinstalovat.
- V jednom okamžiku můžete odstranit pouze jeden profil.

## Odstranění všech přizpůsobení provedených uživatelem
Můžete odstranit všechny změny, které uživatel provedl na stránkách, které tvoří jeho pracovní prostor. To může být užitečné například v případě, že zaměstnanec změnil roli a již nepotřebuje přizpůsobení. Odstraněním přizpůsobení uživatelů se rozložení stránky změní zpět na to, co je definováno profilem.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat") icon, enter **Přizpůsobení uživatele** a vyberte související odkaz.

   Na stránce **Přizpůsobení uživatele** jsou uvedeni všichni uživatelé, kteří provedli individuální nastavení.

2. Otevřete kartu pro uživatele, jehož přizpůsobení chcete odstranit.
3. Na stránce **Přizpůsobení uživatele** zvolte akci **Odstranit** a přijměte zprávu, která se zobrazí.

Uživatel uvidí změny při příštím přihlášení.

Můžete také odstranit všechna přizpůsobení stránek pro profil. Pro více infortmací navštivte [Odstranění všech vlastních nastavení profilu](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## Odstranění individuálních nastavení pro určité stránky
Můžete odstranit přizpůsobení, která jeden nebo více uživatelů provedlo na konkrétních stránkách, které tvoří jejich pracovní prostor. To může být užitečné například v případě, že změněný obchodní proces znamená, že uživatelé již nesmí používat přizpůsobení. Odstraněním přizpůsobení uživatelů se rozložení stránky změní zpět na to, co je definováno profilem.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat") icon, enter **Přizpůsobení uživatele** a vyberte související odkaz.

   Stránka **Přizpůsobení uživatele** obsahuje seznam všech personalizovaných stránek a uživatele, kterému patří.

   > [!Note]
   > Zaškrtnutí v poli **Zděděné Přizpůsobení** znamená, že personalizace byla provedena ve starší verzi [!INCLUDE[prod_short](includes/prod_short.md)], která personalizaci zpracovávala jinak. Uživatelé, kteří se pokusí tyto stránky přizpůsobit, budou zablokováni, pokud se nerozhodnou stránku odemknout. Pro více informací navštivte  [Proč je stránka uzamčena před přizpůsobením](ui-personalization-locked.md).

2. Vyberte řádek pro přizpůsobení stránky, který chcete odstranit, a pak zvolte akci **Odstranit**.

Uživatel uvidí změny při příštím přihlášení.

Můžete také odstranit jednotlivá přizpůsobení stránky pro profil. Pro více informací navštivte [Odstranění vlastního nastavení pro konkrétní stránky profilu](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## Správa uživatelských relací

Jako správce [!INCLUDE[prod_short](includes/prod_short.md)] online, můžete spravovat uživatelské relace v centru pro správu. Pro více informací navštivte [Správa relací](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions) v obsahu správy.

Pro [! INCLUDE[prod_short](includes/prod_short.md)] v místním prostředí, můžete spravovat relace například pomocí SQL Server Management Studio. Pro více informací navštivte [SQL Server technická dokumentace](/sql/sql-server).

## Viz také
[Přiřazení oprávnění uživatelům a skupině](ui-define-granular-permissions.md)  
[Přizpůsobení stránek pro profily](ui-personalization-manage.md)  
[Přizpůsobte si svůj pracovní prostor](ui-personalization-user.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
