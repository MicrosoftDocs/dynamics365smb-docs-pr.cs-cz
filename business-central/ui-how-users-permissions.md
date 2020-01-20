---
title: Přiřazení nebo úprava uživatelských oprávnění | Microsoft Docs
description: 'Popisuje, jak přidat uživatele Office 365 do Business Central a poté přiřadit oprávnění, přístupová práva a nastavení zabezpečení.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'access, right, security'
ms.date: 03/01/2019
ms.author: sgroespe
---
# <a name="managing-users-and-permissions"></a>Správa uživatelů a práv
Chcete-li přidat uživatele do [!INCLUDE[d365fin](includes/d365fin_md.md)], musí správce vaší společnosti Office 365 nejprve vytvořit uživatele v Admin Center Office 365. Pro více informací navštivte [Přidejte uživatele k Office 365 pro firmy](https://aka.ms/CreateOffice365Users).

Po vytvoření uživatelů v sadě Office 365 je lze importovat na stránku **Uživatelů** v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Uživatelům jsou přiřazeny sady oprávnění v závislosti na plánu přiřazeném uživateli v Office 365. Podrobné informace o licencích naleznete v [Licenčním průvodci Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing).

Poté můžete přistoupit k přiřazení sad oprávnění uživatelům, k definování, které databázové objekty a ke kterým prvkům uživatelského rozhraní, mají uživatelé přístup a ve kterých společnostech. Můžete přidat uživatele do skupin uživatelů. To usnadňuje přiřazení stejných sad oprávnění více uživatelům.

Sada oprávnění je souhrn oprávnění pro konkrétní objekty v databázi. Všichni uživatelé musí mít před přístupem [!INCLUDE[d365fin](includes/d365fin_md.md)] přidělenu jednu nebo více sad oprávnění.

Na stránce **Karty uživatele** můžete otevřít stránku **Platná oprávnění** a zjistit, jaká oprávnění má uživatel a skrze které sady oprávnění jsou udělována. Zde můžete také změnit podrobnosti oprávnění pro sady oprávnění **uživatelsky definovaného** typu. Pro více informací navštivte [Získání přehledu oprávnění uživatele](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

Správci mohou pomocí stránky **Nastavení uživatele** definovat časové intervaly, během nichž jsou určití uživatelé schopni účtovat, a také určit systémové protokoly množství času, po který jsou uživatelé přihlášeni.

Další systém, který definuje, k čemu mají uživatelé přístup, je Nastavení skušenosti. Pro další informace navštivte [Změnu zobrazování funkcí](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Přidání uživatele v Business Central
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uživatelé** a poté vyberte související odkaz.
2. Vyberte akci **Získat uživatele z Office 365**.

Na stránce **Uživatelé** bude přidán každý nový uživatel, který byl vytvořen pro vaše předplatné Office 365.

## <a name="to-group-users-in-user-groups"></a>Seskupení uživatelů do skupin uživatelů
Můžete nastavit skupiny uživatelů, které vám pomohou spravovat sady oprávnění pro skupiny uživatelů ve vaší společnosti.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny uživatelů** a poté vyberte související odkaz.
2. Případně na stránce **Uživatelé** vyberte akci **Skupiny uživatelů**.
3. Na stránce **Uživatelé** vyberte akci **Členové skupiny uživatelů**.
4. Na stránce **Členové skupiny uživatelů** vyberte akci **Přidat uživatele**.

Při vytváření uživatelů nebo skupin uživatelů musíte každému z nich přiřadit sady oprávnění, abyste mohli definovat, ke kterému objektu má uživatel přístup. Nejprve musíte uspořádat příslušná oprávnění do sad oprávnění. Pro více informací navštivte [Získání přehledu oprávnění uživatele](ui-how-users-permissions.md#to-get-an-overview-of-a-users-permissions).

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Kopírování skupiny uživatelů a všech jejích sad oprávnění
Chcete-li rychle definovat novou skupinu uživatelů, můžete zkopírovat všechny sady oprávnění z existující skupiny uživatelů do nové skupiny uživatelů.

Členové skupiny uživatelů nejsou zkopírováni do nové skupiny uživatelů. Poté je musíte přidat ručně.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny uživatelů** a poté vyberte související odkaz.
2. Vyberte skupinu uživatelů, kterou chcete kopírovat, a poté vyberte akci **Kopírovat skupinu uživatelů**.
3. Do pole **Kód nové skupiny uživatelů** zadejte název skupiny a poté stiskněte tlačítko **OK**.

Nová skupina uživatelů se přidá na stránku **Skupiny uživatelů**. Pokračujte v přidávání uživatelů. Pro více informací navštivte [Seskupení uživatelů do skupin uživatelů](ui-how-users-permissions.md#to-group-users-in-a-user-group).  

## <a name="to-set-up-user-time-constraints"></a>Nastavení uživatelských časových omezení
Správci mohou definovat časové období, během kterého jsou určití uživatelé schopni účtovat a také určit systémové protokoly množství času, po který jsou uživatelé přihlášeni. Administrátoři mohou také uživatelům přiřadit centra odpovědnosti. Pro více informací navštivte [Práce s Centry zodpovědnosti](inventory-responsibility-centers.md).

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny uživatelů** a poté vyberte související odkaz.
2. Na stránce **Nastavení uživatelů** vyberte akci **Nový**.
3. Do pole **ID uživatele** zadejte ID uživatele nebo vyberte pole pro zobrazení všech aktuálních uživatelů systému Windows v systému.
4. Vyplňte pole podle potřeby.

## <a name="to-create-or-modify-a-permission-set"></a>Vytvoření nebo úprava sady oprávnění
Sady oprávnění fungují jako kontejnery oprávnění, takže můžete snadno spravovat více oprávnění v jednom záznamu. Po vytvoření sady oprávnění musíte přidat konkrétní oprávnění. Pro více informací navštivte [Ruční vytvoření nebo úprava oprávnění](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).

> [!NOTE]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] Řešení obvykle obsahuje řadu předdefinovaných sad oprávnění přidaných společností Microsoft nebo poskytovatelem softwaru. Tyto sady oprávnění jsou **Systémového** typu nebo typu **Rozšíření**. Tyto typy sad oprávnění nebo oprávnění bez těchto typů nelze vytvářet ani upravovat. Můžete je však zkopírovat a definovat v nich vlastní sady a oprávnění. <br /><br />
Sady oprávnění, které uživatelé vytvářejí, z nových nebo jako kopie, jsou typu  **Definováno uživatelem** a lze je upravovat.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sady oprávnění** a poté vyberte související odkaz.
2. Chcete-li vytvořit novou sadu oprávnění, vyberte akci **Nový**.
3. Na novém řádku vyplňte pole dle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Kopírování sady oprávnění
Při vytváření nových sad oprávnění můžete pomocí funkce kopírování rychle přenést všechna oprávnění jiného oprávnění nastaveného na novou sadu oprávnění.

> [!NOTE]  
> Pokud se změní systémová oprávnění, kterou jste zkopírovali, budete upozorněni (v závislosti na vašem výběru), abyste mohli zvážit, zda jsou změny relevantní pro kopírování nebo zápis do vaší uživatelem definované sady oprávnění.

1. Na stránce **Sady oprávnění** vyberte řádek sady oprávnění, kterou chcete zkopírovat, a poté vyberte akci **Kopírovat sadu oprávnění**.
2. Na stránce **Kopírovat sadu oprávnění** zadejte název nové sady oprávnění a poté klepněte na tlačítko **OK**.
3. Pokud chcete zachovat propojení mezi originálem a zkopírovanou sadou oprávnění, zaškrtněte políčko **Upozornit na změněné oprávnění**. Odkaz se potom použije k upozornění, pokud se název nebo obsah původní sady oprávnění změní v budoucí verzi, na kterou bude řešení upgradováno.

Nová sada oprávnění obsahující všechna oprávnění zkopírované sady oprávnění je přidána jako nový řádek na stránce **Nastavení oprávnění**. Řádky jsou řazeny abecedně v rámci každého typu.

## <a name="to-create-or-modify-permissions-manually"></a>Ruční vytvoření nebo úprava oprávnění
Tento postup vysvětluje, jak ručně přidat nebo upravit oprávnění. V uživatelském rozhraní můžete také nechat generovat sady oprávnění automaticky z vašich akcí. Pro více informací navštivte [Vytvoření nebo úprava sady oprávnění zaznamenáním své akce](ui-how-users-permissions.md#to-create-or-modify-permission-sets-by-recording-your-actions).

1. Na stránce **Sady oprávnění** vyberte řádek sady oprávnění, a poté vyberte akci **Oprávnění**.
2. Na stránce **Oprávnění** vytvořte nový řádek nebo upravte pole na existujícím řádku.

V každém z pěti polí typu přístupu, **Právo čtení**, **Právo vložit**, **Právo změnit**, **Právo odstranit** a **Právo spustit**, můžete vybrat jednu z následujících tří možností oprávnění:

|Možnost|Popis|Hodnocení|
|------|-----------|
|**Ano**|Uživatel může provést akci s dotyčným objektem.|Nejvyšší|
|**Nepřímé**|Uživatel může provést akci na dotyčném objektu, ale pouze prostřednictvím jiného souvisejícího objektu, ke kterému má uživatel plný přístup.|Druhý nejvyšší|
|**Prázdné**|Uživatel nemůže provést akci s dotyčným objektem.|Nejnižší|

### <a name="example---indirect-permission"></a>Příklad - nepřímé povolení
Můžete použít nepřímé oprávnění k použití objektu pouze prostřednictvím jiného objektu.
Například uživatel může mít oprávnění ke spuštění procedury 80, Účtovaná dodávka. Procedura účtové dodávky vykonává mnoho úkolů, včetně úpravy tabulky 37, Prodejní řádek. Když uživatel zaúčtuje prodejní doklad, procedura účtové dodávky,  [!INCLUDE[d365fin](includes/d365fin_md.md)] zkontroluje, zda má uživatel oprávnění upravovat tabulku Prodejních řádků. Pokud ne, procedura nemůže dokončit své úkoly a uživatel obdrží chybovou zprávu. Pokud ano, procedura se spustí úspěšně.

Uživatel však nemusí mít plný přístup k tabulce Prodejní řádek, aby mohl spustit proceduru. Pokud má uživatel nepřímé povolení pro tabulku Prodejní řádek, pak se  procedura Účtové dodávky úspěšně spustí. Pokud má uživatel nepřímé oprávnění, může tento uživatel upravit pouze tabulku Prodejní řádek spuštěním procedury Účtové dodávky nebo jiného objektu, který má oprávnění k úpravě tabulky Prodejní řádek. Uživatel může upravit tabulku Prodejní řádek pouze v případě, že tak činí z podporovaných oblastí aplikace. Uživatel nemůže tuto funkci spustit neúmyslně nebo škodlivě jinými metodami.

### <a name="to-limit-a-users-access-to-specific-records-in-a-table"></a>Omezení přístupu uživatele ke konkrétním záznamům v tabulce
Pro zabezpečení na úrovni záznamu v [!INCLUDE[d365fin](includes/d365fin_md.md)], použijte filtry zabezpečení k omezení přístupu uživatele k datům v tabulce. Vytvořte filtry zabezpečení na data tabulky. Filtr zabezpečení popisuje sadu záznamů v tabulce, ke kterým má uživatel oprávnění. Můžete například určit, že uživatel může číst pouze záznamy, které obsahují informace o konkrétním zákazníkovi. To znamená, že uživatel nemá přístup k záznamům, které obsahují informace o jiných zákaznících. Pro více informací navštivte [Používání bezpečnostních filtrů](/dynamics365/business-central/dev-itpro/security/security-filters) v nápovědě pro vývojáře a IT-Pro.


## <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Vytvoření nebo úprava sady oprávnění zaznamenáním své akce
1.  Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sady oprávnění** a poté vyberte související odkaz.
2.  Případně na stránce **Uživatelé** vyberte akci **Sady oprávnění**.
3.  Na stránce **Nastavení uživatelů** vyberte akci **Nový**.
4.  Na novém řádku vyplňte pole dle potřeby.
5.  Zvolte akci **Oprávnění**.
6.  Na stránce **Oprávnění** vyberte akci **Zaznamenat oprávnění** a poté vyberte akci **Spustit**.

    Tím se spustí proces nahrávání, který zachytí všechny vaše akce v uživatelském rozhraní.
7.  Přejděte na různé stránky a aktivity v [!INCLUDE[d365fin](includes/d365fin_md.md)] že chcete, aby uživatelé s tímto oprávněním měli přístup. Musíte provést úkoly, pro které chcete zaznamenat oprávnění.
8.  Pokud chcete nahrávání dokončit, vraťte se na stránku **Oprávnění** a poté vyberte akci **Zastavit**.
9.  Klepnutím na tlačítko **Ano** přidáte zaznamenaná oprávnění do nové sady oprávnění.
10. U každého objektu v zaznamenaném seznamu určete, zda uživatelé mohou do zaznamenaných tabulek vkládat, upravovat nebo mazat záznamy.

> [!NOTE]  
> Když upravíte oprávnění a tím související sadu oprávnění, změny se budou vztahovat také na ostatní uživatele, kteří mají přiřazenou tuto sadu oprávnění.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Přiřazení sad oprávnění uživatelům nebo skupinám uživatelů
Oprávnění můžete uživatelům přiřadit dvěma způsoby:
- Definujte sady oprávnění na uživatelské kartě uživatele.
- Zaškrtněte políčko pro uživatele, ve sloupci, pro související sadu oprávnění, na řádku, na stránce **Sada oprávnění dle uživatele**.
    Pomocí této metody můžete také přiřadit sady oprávnění skupinám uživatelů.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Přiřazení sady oprávnění na kartě uživatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uživatelé** a poté vyberte související odkaz.
2. Vyberte uživatele, kterému chcete přiřadit oprávnění.
Všechny sady oprávnění, které jsou již uživateli přiřazeny, jsou zobrazeny v záložce **Sad oprávnění**.
3. Zvolte akci **Upravit** a otevřete stránku **Karta uživatele**.
4. Na záložce s náhledem **Sady oprávnění uživatele**, na novém řádku vyplňte pole podle potřeby. Pro více informací navštivte [Vytvoření nebo úprava sady oprávnění](ui-how-users-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Přiřazení sady oprávnění na stránce **Sada oprávnění dle uživatele**  
Následující postup vysvětluje, jak přiřadit sady oprávnění uživateli na stránce **Sada oprávnění dle uživatele**. Kroky jsou podobné na stránce **Sada oprávnění dle skupiny uživatelů**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uživatelé** a poté vyberte související odkaz.
2. Na stránce **Uživatelů** vyberte příslušného uživatele a poté vyberte akci **Sada oprávnění dle uživatele**.
3. Na stránce **Sada oprávnění dle uživatele** zaškrtněte políčko **[Název uživatele]** na řádku pro příslušnou sadu oprávnění.
4. Zaškrtněte políčko **Všichni uživatelé** a přiřaďte sadu oprávnění všem uživatelům.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Získání přehledu oprávnění uživatele
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Uživatelé** a poté vyberte související odkaz.
2. Otevřete kartu příslušného uživatele.
3. Zvolte akci **Efektivní oprávnění**.

    Část **Oprávnění** obsahuje seznam všech databázových objektů, ke kterým má uživatel přístup. Tuto sekci nelze upravit.

    Část **Podle sady oprávnění** zobrazuje přiřazené sady oprávnění, prostřednictvím kterých jsou oprávnění udělena uživateli, zdroj a typ sady oprávnění a pro které jsou povoleny různé typy přístupu.

    Pro každý řádek, který vyberete v části **Oprávnění**, část **Podle sady oprávnění** zobrazuje sadu nebo sady oprávnění, prostřednictvím kterých je oprávnění udělováno. V této části můžete upravit hodnotu v každém z pěti polí typu přístupu, **Právo čtení**, **Právo vložit**, **Právo změnit**, **Právo odstranit** a **Právo spustit**.   

    > [!NOTE]  
    > Lze upravovat pouze sady oprávnění typu **Definováno uživatelem**.<br /><br />
    > Řádky zdrojového oprávnění pocházejí z plánu předplatného. Hodnoty oprávnění hodnot zrušení nároku nadřazují hodnoty v jiných sadách oprávnění, pokud mají vyšší hodnocení. Hodnota v sadě oprávnění bez nároku, která má vyšší hodnocení než související hodnota v nároku, bude ohraničena závorkami, což znamená, že není účinná, protože je potlačena nárokem. Pro více informací navštivte [Ruční vytvoření nebo úprava oprávnění](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

4. Chcete-li upravit sadu oprávnění, v části **Podle sady oprávnění** na řádku pro příslušnou sadu oprávnění typu **Definováno uživatelem** vyberte jedno z pěti polí typu přístupu a vyberte jinou hodnotu.

5. Chcete-li upravit jednotlivá oprávnění v rámci sady oprávnění, vyberte hodnotu v poli **Sada oprávnění** a otevřete stránku **Oprávnění**. Postupujte podle pokynů v části [Vytvoření nebo úprava oprávnění](ui-how-users-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Při úpravě sady oprávnění se změny projeví také u ostatních uživatelů, kterým byla sada oprávnění přiřazena.

## <a name="see-also"></a>Viz také
[Zabezpečení a ochrana v Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)  
[Porozumění uživatelům, profilům a centrům rolí](admin-users-profiles-roles.md)  
[Příprava na podnikání](ui-get-ready-business.md)  
[Změna zobrazovaných funkcí](ui-experiences.md)  
[Správa](admin-setup-and-administration.md)  
[Přidávaní uživatele k Office 365 pro podnikání](https://aka.ms/CreateOffice365Users)  
[Průvodce licencí Microsoft Dynamics 365 Business Central](https://aka.ms/BusinessCentralLicensing)
