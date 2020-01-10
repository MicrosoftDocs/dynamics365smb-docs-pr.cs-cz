---
    title: How to Manage Company Configuration in a Worksheet | Microsoft Docs
    description: The configuration worksheet is the central location in which you can plan, track, and perform your configuration work. You can create a worksheet for each company that you are working with or create a standard configuration worksheet that can be used for configuring multiple identical companies.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2019
    ms.author: sgroespe

---
# Správa společnosti v Sešitu konfigurace
Sešit konfigurace je centrální umístění, ve kterém můžete plánovat, sledovat a provádět konfiguraci. Pro každou společnost, se kterou pracujete, můžete vytvořit pracovní sešit nebo vytvořit standardní konfigurační pracovní sešit, který lze použít pro konfiguraci více identických společností.

Prvním krokem při přípravě konfiguračního balíčku je výběr společnosti, kterou jste již nastavili a upravili tak, aby vyhovovala většině vašich potřeb řešení. Tato společnost slouží jako základ pro vaši konfigurační práci na nových společnostech. V sešitu určíte tabulky, které má vaše konfigurace kontrolovat a zpracovávat. Protože většina tabulek v [!INCLUDE[d365fin](includes/d365fin_md.md)] má vztahy a závislosti na jiných tabulkách, měli byste také podle potřeby zahrnout tyto související tabulky. Společně budou tyto tabulky sloužit jako struktura, kolem které vytvoříte novou firmu. Následující kroky vám pomohou s vytvořením baličku a nasazením vaší konfigurace.

K asistování při sledování a revizi vaší práce použijte soubor **Tabulky konfiguračního balíčku** informační okno s informacemi o záznamu. Použijte informační okno **Tabulky balíčku** ke sledování vztahů mezi tabulkami.

Následující postupy ukazují, jak přidat a upravit informace o tabulce pro vaši konfiguraci.

## Otevření konfiguračního sešitu
1. V [!INCLUDE[d365fin](includes/d365fin_md.md)] otevřete společnost, která je základ pro konfiguraci, a poté otevřete Centrum rolí - Implementátor služeb RapidStart.
2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit konfigurace** a poté vyberte související odkaz.

## Přidání tabulky do sešitu
1. Na stránce **Konfigurační sešit**, vyberte tlačítko **Upravit seznam**.
2. Na prvním řádku, v poli **Typ řádku**, vyberte **Tabulka**.
4. V poli **ID tabulky** vyberte tabulku, kterou chcete přidat k vaší konfiguraci.
5. V poli  **ID stránky** zadejte stránku, která je přidružena k tabulce. U standardních tabulek je tato hodnota automaticky vyplněna. U vlastních tabulek musíte uvést ID.
6. Do pole <x1 />Odkaz<x2 /> zadejte adresu URL stránky dokumentace, například v nápovědě, která poskytuje informace o nejlepších postupech nebo pokyny o nastavení tabulky.
7. Chcete-li přidat související tabulky, vyberte akci **Získat související tabulky**.

   > [!NOTE]
   > Související tabulky nebudou přidány akcí **Získat související tabulky**, pokud platí některá z následujících skutečností:
   > - Vztah je podmíněný.
> Například: Pokud získáte související tabulky pro tabulku **Zákazníci**, poté tabulka **Lokace** nebude přidána, protože se vztahuje pouze podmíněně na tabulku **Zákazník**, konkrétně, pokud pole**Kód lokace** v tabulce **Zákazník** je vyplněno.
   > - Související tabulka je filtrována.
> Příklad: pole v související tabulce obsahuje klauzuli KDE. Důvodem je to, že související informace o vztazích jsou uloženy v **Poli** v tabulce systému polí, která není pro aplikaci plně přístupná.
> Tyto typy tabulek je nutné přidat ručně pomocí kroku 4 v tomto postupu.


8. Chcete-li změnit výsledný seznam tabulek, vyberte tabulku, kterou chcete odebrat, a pak zvolte tlačítko **Odstranit**.
9. Opakujte kroky pro každou tabulku, kterou chcete přidat do konfigurace.
10. Chcete-li odebrat duplicitní informace z tabulky, které mohou vyplynout z akce **Získat související tabulky** , zvolte možnost **Odstranit duplicitní řádky** . Tím se odstraní duplicitní tabulky, které mají stejný kód balíčku.

## Přidání více tabulek do konfiguračního sešitu
1. Zvolte akci **Získat tabulky** . Otevře se stránka dávkové úlohy **Získat konfigurační tabulky**.
2. Na záložce s náhledem **Možnosti** zadejte typy tabulek, které chcete přidat do konfigurace, jak je popsáno v následující tabulce.

   | Možnost | Popis |
   |----------------------------------|---------------------------------------|  
   | **Zahrnout pouze s daty** | Zaškrtnutím políčka zahrnete pouze tabulky obsahující data. Můžete například přidat tabulku, která již definuje typické platební podmínky, které vaše řešení podporuje. |
   | **Zahrnout související tabulky** | Zaškrtněte políčko, chcete-li zahrnout všechny související tabulky. Chcete-li přidat podmnožinu souvisejících tabulek, viz krok 3 v tomto postupu. |
   | **Zahrnout tabulky dimenzí** | Zaškrtněte políčko, chcete-li zahrnout tabulky dimenzí. |
   | **Zahrnout pouze licencované tabulky** | Zaškrtněte políčko, chcete-li zahrnout pouze tabulky, ke kterým vám umožňuje přístup k licenci, pod kterou vytváříte sešit. |

3. Na záložce s náhledem  **AllObj** nastavte filtry podle potřeby pro určení typů tabulek, které chcete zahrnout nebo vyloučit.
4. Klikněte na tlačítko **OK**. [!INCLUDE[d365fin](includes/d365fin_md.md)] přidá tabulky do sešitu. Každá položka v seznamu má typ **Tabulka**.
5. Chcete-li odebrat duplicitní informace o tabulce, které mohou být výsledkem akce **Získat tabulky**, vyberte akci **Smazat duplicitní řádky**. Tím se odstraní duplicitní tabulky, které mají stejný kód balíčku.
6. Do sešitu můžete přidat tabulky, které souvisejí s vybranou tabulkou. Zkontrolujte informace v informační okně **Související tabulky**se podívejte, zda chybí tabulky. Chcete-li přidat související tabulky pro konkrétní tabulku, vyberte tabulku v seznamu a poté vyberte talčítko **Získat související tabulky**.

   > [!NOTE]
   > Související tabulky nebudou přidány akcí **Získat související tabulky**, pokud platí některá z následujících skutečností:
   > - Vztah je podmíněný.
> Například: Pokud získáte související tabulky pro tabulku **Zákazníci**, poté tabulka **Lokace** nebude přidána, protože se vztahuje pouze podmíněně na tabulku **Zákazník**, konkrétně, pokud pole**Kód lokace** v tabulce **Zákazník** je vyplněno.
   > - Související tabulka je filtrována.
> Příklad: pole v související tabulce obsahuje klauzuli KDE. Důvodem je to, že informace o vztazích jsou uloženy ve virtuální tabulce **Pole** a nejsou k dispozici na stránkách, jako je konfigurační sešit z důvodů výkonosti.
<x4 /> Související tabulky s tak komplexními vztahy musíte přidat ručně podle kroku 4 v [Přidání tabulky do sešitu](admin-how-to-manage-company-configuration-in-a-worksheet.md#to-add-a-table-to-the-worksheet).


7. Chcete-li odstranit tabulky z výsledného seznamu tabulek, vyberte tabulku, kterou chcete odebrat, a poté vyberte akci **Odstranit**.

Pomocí následujícího postupu určete, která pole tabulky mají být zahrnuta. Po provedení této specifikace můžete exportovat tabulku do Excelu a strukturu tabulky použít jako šablonu pro shromažďování zákaznických dat. Pro více infortmací navštivte [Příprava na migraci zákaznických dat](admin-use-templates-to-prepare-customer-data-for-migration.md)

## Určení sady polí a záznamů pro konfigurační tabulku
1. Vyberte tabulku v seznamu konfiguračních tabulek a poté vyberte akci **Upravit seznam**.
2. Vyberte tabulku, pro kterou chcete zadat informace o poli, a poté vyberte tlačítko **Pole**.
3. Chcete-li vybrat pouze pole, která chcete zahrnout, vyberte **Odstranit Zahrnuto<x2 />. Chcete-li přidat všechna pole, vyberte **Nastavit zahrnuto**.
4. Pro určení, zda data pole nemají být ověřena, zrušte zaškrtnutím políčka **Ověřit pole** pro vybrané pole.
5. Klikněte na tlačítko **OK**.
6. Chcete-li filtrovat na určitou sadu záznamů, které mají být zahrnuty do konfiguračního sešitu, vyberte akci **Filtry** a poté zadejte příslušné hodnoty filtru.

Můžete vytvořit oblasti funkčnosti a skupin tabulek v sešitu, aby bylo možné podobné funkce umístit společně. Například při nastavování účetní osnovy pro vaši konfiguraci se můžete rozhodnout vytvořit skupinu účtovacích tabulek. Obvykle se oblasti používají k seskupení sady tabulek, které odpovídají funkční oblasti. Každá oblast může obsahovat skupiny. Skupinu lze použít k uspořádání tabulek, které mají společný význam.

Následující postup popisuje, jak přidat označení oblastí a skupin poté, co jste vytvořili počáteční seznam tabulek. Po přidání těchto kategorií můžete pokračovat v přidávání a úpravách seznamu tabulek.

## Zařazení a seskupení funkcionalit v sešitu
1. Na začátku oblasti vložte do sešitu nový řádek.
2. V poli **Typ řádku** vyberte **Oblast**. Do pole **Název** zadejte název oblasti.
3. Na začátku seskupování tabulek vložte do Sešitu nový řádek.
4. V poli **Typ řádku** vyberte **Skupina**. Do pole **Název** zadejte název oblasti. Název skupiny je automaticky odsazen.
5. Chcete-li přesunout tabulky do příslušné kategorie, vyberte tabulku, kterou chcete přesunout, a poté vyberte akci **Přesunout nahoru** nebo **Přesunout dolů**. Případně můžete odstranit řádek Sešitu a tabulku znovu vložit na požadované místo.

Některé tabulky [!INCLUDE[d365fin](includes/d365fin_md.md)] jsou standardní a data v nich se pravděpodobně nezmění z implementace na implementaci. V důsledku toho můžete tyto tabulky po zahrnutí do konfiguračního balíčku odstranit ze sešitu. Po přidání jsou tabulky součástí konfiguračního balíčku.

## Odebrání standardní tabulky v sešitu
Po přidání všech nezbytných tabulek do konfiguračního balíčku určete, které tabulky nebudou vyžadovat pozornost zákazníka.
1. Vyberte tabulky a poté je odstraňte volbou akce **Odstranit**.

   > [!NOTE]
   > Tabulky zůstávají v balíčku, i když jsou ze sešitu odstraněny.

## Kontrola a přizpůsobení existujících databázových dat
Při vytváření konfiguračního balíčku pro řešení si můžete prohlížet a přizpůsobovat dostupná databázová data podle svých potřeb. Databázová tabulka musí mít přidruženou stránku.

## Přizpůsobení dat v databázi

1. Na stránce **Konfigurační sešit** identifikujte tabulky, jejichž data chcete zobrazit nebo přizpůsobit.

   > [!NOTE]
   > Ujistěte se, že každé tabulce je přiřazeno ID stránky. Pro standardní [!INCLUDE[d365fin](includes/d365fin_md.md)] tabulky je tato hodnota automaticky vyplněna. U vlastních tabulek musíte uvést ID.

2. Vyberte tlačítko **Data databáze**.

   Stránka [!INCLUDE[d365fin](includes/d365fin_md.md)]  se otevře.

3. Kontrola dostupných informací. Upravte data podle potřeby odstraněním záznamů, které nejsou relevantní, nebo přidáním nových.

## Viz také
[Nastavení konfigurace společnosti](admin-set-up-company-configuration.md)  
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Administrace](admin-setup-and-administration.md)
