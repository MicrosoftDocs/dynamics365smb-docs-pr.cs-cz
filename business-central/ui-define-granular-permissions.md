---
title: Define Granular Permissions  | Microsoft Docs
description: Describes how to give users access to objects by assigning permission sets to them.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 04/22/2020
ms.author: sgroespe

---
# Přiřazení oprávnění uživatelům a skupinám uživatelů
Systém zabezpečení v [!INCLUDE[d365fin](includes/d365fin_md.md)] vám umožňuje řídit, ke kterým objektům má uživatel přístup v rámci každé databáze nebo prostředí. Pro každého uživatele můžete určit, zda je schopen číst, upravovat nebo zadávat data do vybraných databázových objektů. Pro více informací navštivte [Zabezpečení dat](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) v ITPro help pro [!INCLUDE[d365fin](includes/d365fin_md.md)].

Před přiřazením oprávnění uživatelům a skupinám uživatelů je nutné definovat, kdo se může přihlásit  pomocí vytvoření uživatelů podle licence definované v Microsoftu 365 Admin Center. Pro více informací navštivte [Vytvoření uživatelů dle licencí](ui-how-users-permissions.md).

V [!INCLUDE[d365fin](includes/d365fin_md.md)],  existují dvě úrovně oprávnění k databázovým objektům:
- Celková oprávnění podle licence, také označovaná jako nároková.
- Podrobnější oprávnění, která byla přidělena v [!INCLUDE[d365fin](includes/d365fin_md.md)].

Chcete-li usnadnit správu oprávnění pro více uživatelů, můžete je uspořádat do skupin uživatelů a tím přiřadit nebo změnit jednu sadu oprávnění pro mnoho uživatelů v jednom okamžiku. Pro více informací navštivte  [Správa oprávnění prostřednictvím skupin uživatelů](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups)

> [!NOTE]
> Dalším způsobem, jak definovat, ke kterým funkcím má uživatel přístup, je nastavení pole **Zkušenost** na stránce **Informace o společnosti**. Pro další informace se podívejte na [Změna zobrazování funkcí](ui-experiences.md).
>
> Prostřednictvím stránek můžete také definovat, co se uživatelům zobrazí v uživatelském rozhraní a jak pracují s povolenými funkcemi. To provedete prostřednictvím profilů, které přiřadíte různým typům uživatelů podle jejich pracovní role nebo oddělení. Pro více informací navštivte [Správa profilů](admin-users-profiles-roles.md) a [Úpravy [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md).

## Přiřazení sad oprávnění uživatelům
Sada oprávnění je kolekce oprávnění pro konkrétní databázové objekty. Všem uživatelům musí být před přístupem přiřazena jedna nebo více sad oprávnění [!INCLUDE[d365fin](includes/d365fin_md.md)].

Řešení [!INCLUDE[d365fin](includes/d365fin_md.md)] obsahuje řadu předdefinovaných sad oprávnění, které jsou přidány společností Microsoft nebo poskytovatelem řešení. Můžete také přidat nové sady oprávnění přizpůsobené potřebám vaší organizace. Pro více informací navštivte [Vytvoření nebo úprava sady oprávnění](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

> [!NOTE]
> Pokud nechcete omezit přístup uživatele více než stanoveno licencí, můžete uživateli přiřadit speciální sadu oprávnění s názvem SUPER. Tato sada oprávnění zajišťuje, že uživatel má přístup ke všem objektům uvedeným v licenci.<br /><br />
> Uživatel s licencí Essential a sadou oprávnění SUPER má přístup k více funkcím než uživatelé s licencí Team Member a sadou oprávnění SUPER.

Sady oprávnění můžete uživatelům přiřadit dvěma způsoby:
- Na **Kartě uživatele** vybráním sady oprávnění a přiřazením k uživateli.
- Ze stránky **Sada oprávnění dle uživatele** vybráním uživatelů a oprávnění, která je jim přiřazena.

### Přiřazení sady oprávnění na kartě uživatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Uživatelé** a vyberte související odkaz.
2. Vyberte uživatele, kterému chcete přiřadit oprávnění.
   Všechny sady oprávnění, které jsou již přiřazeny uživateli, jsou zobrazeny v informačním okně **Sady oprávnění**.
3. Zvolte akci **Upravit** a otevřete stránku **Karta uživatele**.
4. Na záložce s náhledem **Sady oprávnění uživatele**, na novém řádku vyplňte pole podle potřeby. Pro více informací navštivte [Vytvoření nebo úprava sady oprávnění](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### Přiřazení sady oprávnění na stránce **Sada oprávnění dle uživatel**
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Uživatelé** a vyberte související odkaz.
2. Na stránce **Uživatelů** vyberte příslušného uživatele a poté vyberte akci **Sada oprávnění dle uživatele**.
3. Na stránce **Sada oprávnění** dle uživatele zaškrtněte políčko **[Název uživatele]** na řádku pro příslušnou sadu oprávnění k přiřazení sady uživateli.
4. Zaškrtněte políčko **Všichni uživatelé** a přiřaďte sadu oprávnění všem uživatelům.

## Získání přehledu oprávnění uživatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Uživatelé** a vyberte související odkaz.
2. Otevřete kartu příslušného uživatele.
3. Zvolte akci **Platná oprávnění**.

   Část **Oprávnění obsahuje** seznam všech databázových objektů, ke kterým má uživatel přístup. Tuto sekci nelze upravit.

   Část **Podle sady oprávnění** zobrazuje přiřazené sady oprávnění, prostřednictvím kterých jsou oprávnění udělena uživateli, zdroj a typ sady oprávnění a pro které jsou povoleny různé typy přístupu.

   Pro každý řádek, který vyberete v části **Oprávnění**, část **Podle sady oprávnění** zobrazuje sadu nebo sady oprávnění, prostřednictvím kterých je oprávnění udělováno. V této části můžete upravit hodnotu v každém z pěti polí typu přístupu, **Právo čtení**, **Právo vložit**, **Právo změnit**, **Právo odstranit** a **Právo spustit**.

   > [!NOTE]  
   > Lze upravovat pouze sady oprávnění typu **Uživatelem definované**.<br /><br />
   > Řádky zdrojového oprávnění pocházejí z předplacené licence. Hodnoty oprávnění hodnot oprávnění nadřazují hodnoty v jiných sadách oprávnění, pokud mají vyšší hodnocení. Hodnota v sadě oprávnění bez nároku, která má vyšší hodnocení než související hodnota v nároku, bude ohraničena závorkami, což znamená, že není účinná, protože je potlačena nárokem..<br /><br />
   > Vysvětlení hodnocení viz [Vytvoření nebo úprava práv ručně](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

4. Chcete-li upravit sadu oprávnění, v části **Podle sady oprávnění** na řádku pro příslušnou sadu oprávnění typu **Definováno uživatelem** vyberte jedno z pěti polí typu přístupu a vyberte jinou hodnotu.

5. Chcete-li upravit jednotlivá oprávnění v rámci sady oprávnění, zvolte hodnotu v poli **Sady oprávnění** k otevření stránky **Práva**. Postupujte podle pokynů v části [Vytvoření nebo úprava oprávnění](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

> [!NOTE]  
> Při úpravě sady oprávnění se změny projeví také u ostatních uživatelů, kterým byla sada oprávnění přiřazena.

## Vytvoření nebo úprava sady oprávnění
Sady oprávnění fungují jako kontejnery oprávnění, takže můžete snadno spravovat více oprávnění v jednom záznamu.

> [!NOTE]  
> Řešení [!INCLUDE[d365fin](includes/d365fin_md.md)] řešení obvykle obsahuje řadu předdefinovaných sad oprávnění přidaných společností Microsoft nebo poskytovatelem softwaru. Tyto sady oprávnění jsou typu **Systém** nebo **Extension**. Tyto typy sad oprávnění nelze vytvářet ani upravovat. Můžete je však zkopírovat a definovat vlastní sady oprávnění a oprávnění. <br /><br />
> Sady oprávnění, které uživatelé vytvářejí, nové nebo jako kopie jsou typu **Uživatelem definované** a mohou být upraveny.

### Vytvoření nové sady oprávnění od nuly
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sady oprávnění** a poté vyberte související odkaz.
2. Chcete-li vytvořit novou sadu oprávnění, vyberte akci **Nový**.
3. Na novém řádku vyplňte pole dle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
   Po vytvoření sady oprávnění musíte přidat skutečná oprávnění. Pro více informací navštivte [Ruční vytvoření nebo úprava oprávnění](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### Kopírování sady oprávnění
Funkci kopírování můžete také použít k rychlému přenesení všech oprávnění jiného oprávnění nastaveného na novou sadu oprávnění.

> [!NOTE]  
> Pokud se změní systémová oprávnění, která jste zkopírovali, budete upozorněni (v závislosti na vašem výběru), abyste mohli zvážit, zda jsou změny relevantní pro kopírování nebo zápis do vaší uživatelem definované sady oprávnění.

1. Na stránce **Sady oprávnění**vyberte řádek pro sadu oprávnění, kterou chcete kopírovat, a poté vyberte akci **Kopírovat sadu oprávnění**.
2. Na stránce **Kopírovat sadu oprávnění**zadejte název nové sady oprávnění a pak zvolte tlačítko **OK**.
3. Zaškrtněte políčko **Upozornit na změněnou sadu oprávnění** pokud chcete zachovat propojení mezi originálem a zkopírovanou sadou oprávnění. Propojení se potom použije k upozornění, pokud se název nebo obsah původní sady oprávnění změní v budoucí verzi, na kterou bude řešení upgradováno na později.

Nová sada oprávnění obsahující všechna oprávnění zkopírované sady oprávnění je přidána jako nový řádek na stránce **Sada oprávnění**. Nyní mužete začít upravovat opravnění v nové sadě oprávnění. Všimněte si, že řádky jsou seřazeny abecedně v rámci každého typu.

### Export a import sady oprávnění
Chcete-li rychle nastavit oprávnění, můžete importovat sady oprávnění, které jste exportovali z jiného [!INCLUDE[d365fin](includes/d365fin_md.md)].

Ve víceklientských prostředích bude sada oprávnění importována do konkrétního klienta.

1. V prvním klientu, na stránce **Sada oprávnění**, Vyberte řádek nebo řádky oprávnění pro exporta zvolte tlačítko **Export Sady oprávnění**.

   Soubor XML je vytvořen ve složce pro stahování ve vašem počítači. Ve výchozím nastavení se nazývá "Export Permission Sets.xml"

2. V druhém klientu, na stránce **Sada oprávnění**, vyberte **Import Sady oprávnění**.
3. V dialogové stránce **Import Sady oprávnění** zvažte, zda chcete sloučit stávající sady oprávnění s novými sadami oprávnění v souboru xml.

   Pokud zaškrtnete políčko **Aktualizovat existující oprávnění**, existující sady oprávnění se stejným názvem jako ty, které existují v souboru XML, budou sloučeny s importovanými sadami oprávnění.

   Pokud nezaškrtnete políčko **Aktualizovat existující oprávnění**, budou během importu přeskočeny sady oprávnění se stejným názvem jako ty, které existují v souboru XML. V takovém případě budete informováni o přeskočených sadách oprávnění.

4. Na stránce dialogového okna **Import** najděte a vyberte soubor XML, který chcete importovat, a pak zvolte **Otevřít**.

Sady oprávnění jsou importovány.

## Ruční vytvoření nebo úprava oprávnění
Tento postup vysvětluje, jak ručně přidat nebo upravit oprávnění. Můžete také mít oprávnění generována automaticky z vašich akcí v uživatelském rozhraní. Pro více informací navštivte [Vytvoření nebo úprava sady oprávnění zaznamem uživatelských akcí](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions).

> [!NOTE]
> Když upravíte oprávnění a tím související sadu oprávnění, změny se budou vztahovat také na ostatní uživatele, kterým je sada oprávnění přiřazena.

1. Na stránce **Sady oprávnění** vyberte řádek sady oprávnění, a poté vyberte akci **Oprávnění**.
2. Na stránce **Oprávnění** vytvořte nový řádek nebo upravte pole na existujícím řádku.

V každém z pěti polí typu přístupu, **Právo čtení**, **Právo vložit**, **Právo změnit**, **Právo odstranit** a **Právo spustit**, můžete vybrat jednu z následujících tří možností oprávnění:

| Možnost | Popis | Hodnocení |
|------|-----------|
| **Ano** | Uživatel může provést akci s dotyčným objektem. | Nejvyšší |
| **Nepřímo** | Uživatel může provést akci na dotyčném objektu, ale pouze prostřednictvím jiného souvisejícího objektu, ke kterému má uživatel plný přístup. Další informace o nepřímých oprávněních naleznete v části [Vlastnosti oprávnění](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) v Developer and IT-Pro Help | Druhý nejvyšší |
| **Prázdný** | Uživatel nemůže provést akci s daným objektem. | Nejnižší |

### Příklad - Nepřímé opravnění
Můžete přiřadit nepřímé oprávnění k použití objektu pouze prostřednictvím jiného objektu.
Uživatel může mít například oprávnění ke spuštění Codeunity 80 Sales-Post. Codeunita Sales-Post ykonává mnoho úkolů, včetně úpravy tabulky 37, prodejní řádek. Když uživatel zaúčtuje prodejní doklad, Codeunita Sales-Post [!INCLUDE[d365fin](includes/d365fin_md.md)]  zkontroluje, zda má uživatel oprávnění k úpravám tabulky Prodejní řádek. Pokud ne, Codeunita nemůže dokončit své úlohy a uživatel obdrží chybovou zprávu. Pokud ano, Codeunita se spustí úspěšně.

Uživatel však nemusí mít úplný přístup k tabulce Prodejní řádek, aby mohl spustit codeunitu. Pokud má uživatel nepřímé oprávnění pro tabulku Prodejní řádek, bude Codeunita Sales-Post úspěšně spuštěna. Pokud má uživatel nepřímé oprávnění, může upravit tabulku Prodejní řádek pouze spuštěním Codeunity Sales-Post nebo jiného objektu, který má oprávnění k úpravě tabulky Prodejní řádek. Uživatel může upravit tabulku Prodejní řádek pouze v případě, že tak činí z podporovaných oblastí aplikace. Uživatel nemůže tuto funkci spustit neúmyslně nebo škodlivě jinými metodami.

## Vytvoření nebo úprava sady oprávnění zaznamenáním vlastní akce
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sady oprávnění** a poté vyberte související odkaz.
2. Případně na stránce **Uživatelé** vyberte akci **Sady oprávnění**.
3. Na stránce **Sady oprávnění** vyberte akci **Nový**.
4. Na novém řádku vyplňte pole dle potřeby.
5. Zvolte akci **Oprávnění**.
6. Na stránce **Oprávnění** vyberte akci **Zaznamenat oprávnění** a poté vyberte akci **Spustit**.

    Tím se spustí proces nahrávání, který zachytí všechny akce v uživatelském rozhraní.
7. Projděte různé stránky a aktivity v [!INCLUDE[d365fin](includes/d365fin_md.md)] , ke kterým chcete, aby uživatelé s tímto oprávněním měli přístup. Je nutné provést úkoly, pro které chcete zaznamenat oprávnění.
8. Pokud chcete nahrávání ukončit, vraťte se na stránku **Práva** a poté vyberte akci **Stop**.
9. Zvolte tlačítko **Ano**, chcete-li přidat zaznamenaná oprávnění do nové sady oprávnění.
10. U každého objektu v zaznamenaném seznamu určete, zda jsou uživatelé schopni do zaznamenaných tabulek vkládat, upravovat nebo mazat záznamy.

## Filtry zabezpečení - omezení přístupu uživatele k určitým záznamům v tabulce
Pro zabezpečení na úrovni záznamu v [!INCLUDE[d365fin](includes/d365fin_md.md)], můžete pomocí bezpečnostních filtrů omezit přístup uživatele k datům v tabulce. Vytvořte filtry zabezpečení na data tabulky. Filtr zabezpečení popisuje sadu záznamů v tabulce, ke kterým má uživatel oprávnění. Můžete například určit, že uživatel může číst pouze záznamy, které obsahují informace o konkrétním zákazníkovi. To znamená, že uživatel nemá přístup k záznamům, které obsahují informace o jiných zákaznících. Pro více informací navštivte [Používání bezpečnostních filtrů](/dynamics365/business-central/dev-itpro/security/security-filters) v nápovědě pro vývojáře a IT-Pro help.

## Správa oprávnění prostřednictvím Skupiny uživatelů
Můžete nastavit skupiny uživatelů, které vám pomohou spravovat sady oprávnění pro skupiny uživatelů ve vaší společnosti.

Začnete vytvořením skupiny uživatelů. Potom skupině přiřadíte sady oprávnění, které definují, ke kterému objektu mají uživatelé skupiny přístup. Když přidáte uživatele do skupiny, budou se na něj vztahovat sady oprávnění definované pro skupinu.

Sady oprávnění přiřazené uživateli prostřednictvím skupiny uživatelů zůstanou synchronizovány tak, aby změna oprávnění skupiny uživatelů byla automaticky rozšířena na uživatele. Pokud odeberete uživatele ze skupiny uživatelů, příslušná oprávnění budou automaticky odebrána.

### Seskupení uživatelů do skupin uživatelů
Následující postup vysvětluje, jak vytvořit skupiny uživatelů ručně. Chcete-li vytvořit skupiny uživatelů automaticky, přečtěte si téma [Kopírování skupiny uživatelů a všech jejích sad oprávnění](ui-define-granular-permissions.md#to-copy-a-user-group-and-all-its-permission-sets).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat") icon, enter **Skupiny uživatelů** a vyberte související odkaz.
2. Případně na stránce **Uživatelé** vyberte akci **Skupiny uživatelů**.
3. Na stránce **Skupiny uživatelů** vyberte akci **Člen skupiny uživatelů**.
4. Na stránce **Skupiny uživatelů** vyberte akci **Přidat uživatele**

### Kopírování skupiny uživatelů a všech jejích sad oprávnění
Chcete-li rychle definovat novou skupinu uživatelů, můžete zkopírovat všechny sady oprávnění z existující skupiny uživatelů do nové skupiny uživatelů.

> [!NOTE]
> Členové skupiny uživatelů nejsou zkopírováni do nové skupiny uživatelů. Poté je musíte přidat ručně. Pro více informací navštivte [Seskupení uživatelů do skupin uživatelů](ui-define-granular-permissions.md#to-group-users-in-user-groups).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat") icon, enter **Skupiny uživatelů** a vyberte související odkaz.
2. Vyberte skupinu uživatelů, kterou chcete kopírovat, a poté vyberte akci **Kopírovat skupinu uživatelů**.
3. Do pole **Kód nové skupiny uživatelů** adejte název skupiny a poté vyberte tlačítko **OK**.

Nová skupina uživatelů se přidá na stránku **Skupiny uživatelů** page. Pokračujte v přidávání uživatelů. Pro více informací navštivte [Seskupení uživatelů do skupin uživatelů](ui-define-granular-permissions.md#to-group-users-in-user-groups).

### Přiřazení sad oprávnění skupinám uživatelů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat") icon, enter **Skupiny uživatelů** a vyberte související odkaz.
2. Vyberte skupinu uživatelů, kterým chcete přiřadit oprávnění.
   Všechny sady oprávnění, které jsou již přiřazeny uživateli, jsou zobrazeny v informačním okně **Sady oprávnění**.
3. Zvolte tlačítko **Sady oprávnění uživatele** k otevření stránky **Sady oprávnění uživatele**.
4. Na stránce **Sady oprávnění uživatele** a novém řádku vyplňte pole podle potřeby.

### Přiřazení sady oprávnění na stránce **Sada oprávnění dle skupiny uživatelů**
Následující postup vysvětluje, jak přiřadit sady oprávnění skupině uživatelů na stránce **Sada oprávnění dle skupiny uživatelů**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Uživatelé** a vyberte související odkaz.
2. Na stránce **Uživatelé** vyberte příslušného uživatele a poté vyberte akci**Sada oprávnění dle skupiny uživatelů**.
3. Na stránce **Sada oprávnění dle skupiny uživatelů** vyberte zaškrtávací políčko **[Název skupiny uživatelů]** na řádku pro příslušnou sadu oprávnění, která má přiřadit sadu skupině uživatelů.
4. Zaškrtněte políčko **Všechny skupiny uživatelů** a přiřaďte sadu oprávnění všem skupinám uživatelů.

## Odstranění zastaralých oprávnění ze všech sad oprávnění
1. Na stránce **Sady oprávnění** vyberte **Odstranit zastaralá oprávnění**.

## Nastavení časových omezení uživatele
Správci mohou definovat časové období, během kterého mohou zadaní uživatelé účtovat, a také určit, zda systém zaznamenává dobu, po kterou jsou uživatelé přihlášeni. Administrátoři mohou také uživatelům přiřadit centra odpovědnosti. Pro více informací navštivte [Práce s Centry zodpovědnosti](inventory-responsibility-centers.md).

1. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Nastavení uživatelů** a poté vyberte související odkaz.
2. Na stránce **Nastavení uživatelů** vyberte akci **Nový**.
3. Do pole **ID uživatele** zadejte ID uživatele nebo vyberte pole pro zobrazení všech aktuálních uživatelů systému Windows v systému.
4. Podle potřeby vyplňte pole.

## Viz také
[Vytváření uživatelů dle licence](ui-how-users-permissions.md)  
[Správa profilů](admin-users-profiles-roles.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
[Úprava [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Připřavte se na business](ui-get-ready-business.md)  
[Administrace](admin-setup-and-administration.md)  
[Přidání uživatelů Office 365](https://aka.ms/CreateOffice365Users)  
[Zabezpečení a ochrana v Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) v Developer and IT-pro Help
