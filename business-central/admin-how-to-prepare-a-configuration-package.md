---
title: Jak si připravit konfigurační balíček | Microsoft Docs
description: 'Při konfiguraci nové společnosti jsou relace tabulky rozpoznány a zpracovány. Data jsou importována a použita ve správném pořadí. Tabulky dimenzí se také importují, pokud jsou součástí konfiguračního balíčku.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 03/01/2019
ms.author: sgroespe
---
# <a name="prepare-a-configuration-package"></a>Příprava konfiguračního balíčku
Při konfiguraci nové společnosti jsou relace tabulky rozpoznány a zpracovány. Data jsou importována a použita ve správném pořadí. Tabulky dimenzí se také importují, pokud jsou součástí konfiguračního balíčku.  

Chcete-li pomoci zákazníkovi používat konfigurační balíček, můžete do balíčku přidat dotazník nebo sadu dotazníků. Dotazník může zákazníkovi pomoct při pochopení různých možností nastavení. Obvykle jsou vytvářeny dotazníky pro hlavní tabulky nastavení, kde zákazník může vyžadovat další pokyny, jak vybrat vhodné nastavení. Pro více informací navštivte [ Shromáždění hodnot nastavení zákazníka ](admin-gather-customer-setup-values.md).

Ujistěte se, že jste v centru rolí Implementátor služeb RapidStart. Pro více informací navštivte [Používání role Implementátor služeb RapidStart](admin-how-to-use-the-rapidstart-services-role-center-to-track-progress.md).

> [!IMPORTANT]  
>  Při exportu a importu konfiguračních balíčků mezi dvěma databázemi společnosti by databáze měly mít stejné schéma, aby se zajistilo úspěšné přenesení všech dat. To znamená, že databáze by měly mít stejnou tabulku a strukturu polí, ve kterých tabulky mají stejné primární klíče a pole mají stejné ID a datové typy.  
>   
>  Můžete importovat konfigurační balíček, který byl exportován z databáze, která má jiné schéma než tato cílová databáze. Avšak žádné tabulky nebo pole v konfiguračním balíčku, které chybí v cílové databázi, nebudou importovány. Tabulky s různými primárními klíči a poli s různými datovými typy se také neimportují úspěšně. Pokud například konfigurační balíček obsahuje tabulku **50000, zákazník**, která má primární klíč **Kód20**, a databáze, do které importujete balíček, zahrnuje tabulku **50000, bankovní účet zákazníka**, která má primární klíč **Kód20 + Kód20**, potom data nebudou importována.  

## <a name="to-create-a-configuration-package"></a>Pro vytvoření konfiguračního balíčku  
1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Konfigurační balíčky** a poté vyberte související odkaz.  
2. Zvolte akci **Nový**.  
3. V záložce **Obecné** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Chcete-li z balíčku vyloučit konfigurační dotazníky, konfigurační šablony a tabulky konfiguračních sešitů, zaškrtněte políčko **Vyloučit konfigurační tabulky**. V opačném případě budou tyto tabulky při exportu balíčku automaticky přidány do seznamu tabulek balíčků.  
5. Zvolte akci **Získat tabulky**. Otevře se stránka dávkové úlohy **Získat tabulky balíčků**.  
6. Zvolte pole **Vybrat tabulky**. Otevře se okno **Výběr konfigurace**.  
7. Vyberte akci **Vybrat vše,** chcete-li přidat všechny tabulky do balíčku, nebo zaškrtněte políčko **Vybráno** u každé tabulky v seznamu, kterou chcete přidat.
8. Zvolte tlačítko **OK**. Počet tabulek, které jste vybrali, je uveden v poli **Vybrat tabulky**. Zadejte další možnosti a poté klepněte na tlačítko **OK**. [!INCLUDE[d365fin](includes/d365fin_md.md)] tabulky jsou přidány do řádků stránky **Konfigurační balíček**.  

    > [!NOTE]  
    >  Toto můžete také provést v konfiguračním sešitu. Vyberte tabulky, které chcete zahrnout do balíčku, a poté vyberte akci **Přiřadit balíček**.

9. Chcete-li vybrat pole, která chcete zahrnout z tabulky, vyberte tabulku a poté na kartě **Řádky** vyberte akci **Pole**.
Určete, která pole jsou součástí balíčku. Ve výchozím nastavení jsou zahrnuta všechna pole.

    - Chcete-li vybrat pouze pole, která chcete zahrnout, vyberte akci **Odstranit Zahrnuto**. Chcete-li přidat všechna pole, vyberte akci **Nastavit Zahrnuto**.  
    - Chcete-li určit, že data pole by neměla být ověřena, zrušte zaškrtnutí políčka **Ověřit pole** pro konkrétní pole.  

10. Zjistěte, zda jste zavedli potenciální chyby, výběrem akce **Ověřit balíček**. K tomu může dojít, pokud nezahrnete tabulky, na které vaše konfigurace spoléhá.  
11. Zvolte tlačítko **OK**.  

Po upřesnění seznamu polí, která mají být zahrnuta z tabulky, můžete zkontrolovat své výsledky v aplikaci Excel.  

### <a name="to-filter-and-review-your-dataset"></a>Pro filtrování a kontrolu sady dat  
1. Pro filtrování určité sady záznamů, která má být součástí balíčku, vyberte na kartě **Řádky** akci **Filtry** a zadejte příslušné hodnoty filtru.  
2. Na kartě balíčku vyberte na kartě **Řádky** akci **Exportovat do aplikace Excel**.  
3. Potvrďte zprávy, které umožňují export dat do Excelu. Otevře se pojmenovaný soubor .xlsx. Zkontrolujte záznamy, které byly exportovány.  
4. Zavřete aplikaci Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>Pro zahrnutí šablony pro aplikaci do tabulky  
Pro určité tabulky, jako je tabulka, která bude obsahovat hlavní data, můžete určit šablonu, která se použije na data. Šablona může obsahovat povinná pole, která chcete použít pro všechna hlavní data a která nikdy nechcete měnit. Můžete například vytvořit šablonu, kterou lze použít na zákaznická data. Šablona může obsahovat všechna povinná pole, což umožňuje konzistentní import standardizovaných informací. Informace, které nelze standardizovat, jako například jméno zákazníka, budou zpracovány při importu zákaznických dat.

1. Na stránce **Karta konfiguračního balíčku** zvolte tabulku a poté vyberte pole **Šablona dat**. Zobrazí se seznam šablon na základě tabulky.
2. Vybere šablonu a poté klepněte na tlačítko **OK**.  

Po dokončení balíčku ho uložte do souboru podle následujícího postupu. Pak můžete dát balíček zákazníkovi nebo partnerovi k použití.

### <a name="to-save-and-export-a-configuration-package"></a>Pro uložení a export konfiguračního balíčku  
- Na stránce **Karta konfiguračního balíčku** zvolte akci **Exportovat balíček**.  

Balíček je vytvořen v souboru .rapidstart, který doručuje obsah balíčku v komprimovaném formátu. Konfigurační dotazník, konfigurační šablony a konfigurační sešit jsou do balíčku přidávány automaticky, pokud se výslovně nerozhodnete je vyloučit.  

Můžete uložit soubor s názvem, který je pro vás smysluplný, ale nemůžete změnit příponu souboru. Ta musí být .rapidstart.  

### <a name="to-copy-a-configuration-package"></a>Pro zkopírování konfiguračního balíčku  
Po vytvoření balíčku, který splňuje většinu vašich potřeb, můžete jej použít jako základ pro vytváření podobných balíčků. To může urychlit dobu implementace a zvyšuje opakovatelnost služeb RapidStart.

1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Konfigurační balíčky** a poté vyberte související odkaz.  
2. Vyberte balíček ze seznamu a poté vyberte akci **Kopírovat balíček**.  
3. Do pole **Kód nového balíčku** zadejte kód nového balíčku.  
4. Pokud chcete také kopírovat data databáze z existujícího balíčku, zaškrtněte políčko **Kopírovat data**.  
5. Zvolte tlačítko **OK**.

## <a name="to-customize-a-configuration-package"></a>Pro přizpůsobení konfiguračního balíčku
Pomocí konfiguračního sešitu můžete shromažďovat a kategorizovat informace, které chcete použít ke konfiguraci nové společnosti, a uspořádat tabulky logickým způsobem. Formátování v sešitu je založeno na jednoduché hierarchii: Oblasti obsahují skupiny, které zase obsahují tabulky. Oblasti a skupiny jsou volitelné, ale nezbytné pro umožnění přehledu procesu konfigurace v centru rolí služeb RapidStart.

1.  Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Konfigurační sešitu** a poté vyberte související odkaz.  
2.  V poli **Typ řádku** vyberte **Oblast**. Do pole **Název** zadejte popisný název.  
3.  V poli **Typ řádku** vyberte **Skupina**. Do pole **Název** zadejte popisný název.  
4.  V poli **Typ řádku** vyberte **Tabulka**. V poli **ID tabulky** vyberte tabulku, kterou chcete do sešitu zahrnout.  

Nyní můžete tabulky přiřadit ke konkrétním konfiguračním balíčkům, které jste vytvořili nebo plánujete vytvořit. Pro více informací navštivte [Pro přiřazení tabulky konfiguračnímu balíčku](admin-how-to-prepare-a-configuration-package.md#to-assign-a-table-to-a-configuration-package).

## <a name="to-work-with-promoted-tables"></a>Pro práci s zvýrazněnými tabulkami  
1. Zaškrtněte políčko **Zvýrazněná tabulka** a označte tabulku, která se často používá během procesu nastavení typickým zákazníkem, například tabulka **Finanční účet**. Pokud má tabulka toto označení, bude zákazník moci snadno filtrovat svůj sešit a zobrazit pouze seznam zvýrazněných tabulek, které vyžadují pozornost.  
2. Chcete-li zobrazit filtrované zobrazení, vyberte akci **Pouze zvýrazněné**. Seznam tabulek obsahuje pouze ty tabulky, které mají zaškrtnuté políčko.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Pro přiřazení tabulky konfiguračnímu balíčku  
Po definování tabulek, které chcete považovat za součást vaší konfigurace, můžete tabulky snadno přiřadit konfiguračním balíčkům. Tabulku můžete přiřadit pouze k jednomu balíčku. V následujícím postupu přiřadíte balíček zevnitř konfiguračního sešitu.  

> [!NOTE]  
>  Balíček můžete také vytvořit přímo a přidat do něj tabulky. Pro více informací navštivte [Pro vytvoření konfiguračního balíčku](admin-how-to-prepare-a-configuration-package.md#to-create-a-configuration-package).

1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Konfigurační sešitu** a poté vyberte související odkaz.
2. V konfiguračním sešitu vyberte řádek nebo skupinu řádků, které chcete přiřadit konfiguračnímu balíčku, a poté vyberte akci **Přiřadit balíček**.  
3.  Vyberte balíček ze seznamu nebo zvolte akci **Nový** a vytvořte nový balíček a poté stiskněte tlačítko **OK**.  

    Pokud tabulka již není součástí balíčku, bude přidána nyní. Pole kódu balíčku na řádku sešitu bude vyplněno kódem balíčku, ke kterému je tabulka přiřazena.  
4. Pokud vyberete existující balíček, můžete zjistit, kolik tabulek je již v balíčku, a to kontrolou informací v poli **Počet tabulek**.

## <a name="to-review-or-customize-existing-database-data"></a>Pro zkontrolování nebo úpravu existujících dat databáze
Při vytváření konfiguračního balíčku pro řešení si můžete prohlížet a přizpůsobovat dostupná databázová data podle svých potřeb. Databázová tabulka musí mít přidruženou stránku.  

1. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Konfigurační sešitu** a poté vyberte související odkaz.
2. V konfiguračním sešitu určete tabulky, jejichž data chcete zobrazit nebo přizpůsobit.  

    > [!NOTE]  
    >  Ujistěte se, že každé tabulce je přiřazeno ID stránky. U standardních tabulek [!INCLUDE[d365fin](includes/d365fin_md.md)] je tato hodnota automaticky vyplněna. U vlastních tabulek musíte ID uvést.

3. Vyberte akci **Data databáze**. Otevře se stránka pro související stránky.
4. Zkontrolujte dostupné informace. Upravte ji podle potřeb odstraněním záznamů, které nejsou relevantní, nebo přidáním nových.    

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Pro kopírování dat z testovacího prostředí do produkčního prostředí  
Po prověření a otestování všech vašich informací o nastavení můžete pokračovat v kopírování dat do produkčního prostředí. Ve stejné databázi vytvoříte novou společnost.

1. Otevřete a inicializujte novou společnost.  
2. Vyberte ikonu ![Žárovka, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zvolte **Konfigurační sešitu** a poté vyberte související odkaz.  
3. Zvolte akci **Kopírovat data ze společnosti**.  
4. Na stránce **Kopírovat data společnosti** vyberte pole **Kopie z**. Otevře se stránka **Společnosti**.  
5. Vyberte společnost, ze které chcete data zkopírovat, a poté stiskněte tlačítko **OK**. Otevře se seznam tabulek vybraných v konfiguračním sešitu. Tento seznam obsahuje pouze tabulky, které obsahují záznamy.
6. Vyberte tabulky, ze kterých chcete kopírovat data, a poté vyberte akci **Kopírovat data**. Na stránce **Kopírovat data společnosti** stiskněte tlačítko **OK**.  

## <a name="see-also"></a>Viz také  
[Shromáždění hodnot nastavení zákazníka](admin-gather-customer-setup-values.md)  
[Nastavení konfigurace společnosti](admin-set-up-company-configuration.md)  
[Založení společnosti pomocí služeb RapidStart](admin-set-up-a-company-with-rapidstart.md)  
[Správa](admin-setup-and-administration.md)
