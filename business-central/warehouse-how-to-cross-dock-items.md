---
    title: How to Cross-Dock Items | Microsoft Docs
    description: Cross-docking functionality is available to you if you have set up your location to require warehouse receive and put-away processing.
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
# Přeložení zboží
Funkce přeložení je k dispozici, pokud jste nastavili lokaci tak, aby vyžadovala zpracování příjmu do skladu a zaskladnění.

Při přeložení zboží, jej zpracováváte v procesu příjmu a dodání, aniž byste je někdy uskladnili, a tím urychlujete proces expedice zboží prostřednictvím funkcí zaskladnění a vyskladnění a omezujete fyzické zpracování zboží. Zboží můžete přeložit jak pro dodávky, tak pro výrobní zakázky. Když připravíte dodávku nebo vyskladnění zboží pro výrobu a používáte přihrádky, zboží se automaticky vyskladní z přihrádky přeložení před jakoukoli jinou přihrádkou. Musíte se podívat do oblasti přeložení, abyste zjistili, zda je k dispozici zboží, které potřebujete, než ho získáte v obvyklém úložném prostoru.

Pokud jste vypočítali množství přeložení, řádky zaskladnění do přihrádky přeložení pro výpočty přeložení se vytvoří při zaúčtování příjmu. Ostatní řádky zaskladnění jsou vytvořeny jako obvykle.

Pokud chcete zboží přeložení zaúčtovat ihned, aby bylo k dispozici pro vyskladnění, musíte také zaregistrovat zaskladnění pro ostatní zboží pocházející z řádku příjmu, konkrétně pro zboží, které je třeba uložit. Pokud je pouze některé zboží na řádku příjmu přeloženo, musíte se snažit zaskladnit zbývající zboží co nejrychleji. Případně může být vaše skladová politika nastavena na podporu přeložení celých řádků příjmu, kdykoli je to možné.

V instrukci zaskladnění můžete ve svůj prospěch odstranit řádky instrukce Vzít a Vložit pro každý řádek příjmu, který se týká příjmů, které mají být plně zaskladněny. Tyto řádky mohou být později vytvořeny jako řádky  zaskladnění ze zešitu zaskladnění nebo zaúčtované příjemky. Po jejich odstranění můžete zaskladnit a zapsat řádky, které se týkají položek přeložení.

Pokud jste na kartě lokace vybrali pole **Použít sešit zaskladnění** a zaúčtovali příjem s vypočtenými přeloženími, budou všechny řádky příjmu k dispozici v sešitu. Informace o přeložení jsou ztraceny a nelze je znovu vytvořit. Proto pokud chcete použít funkci přeložení, měli byste předávat řádky do sešitu zaskladnění odstraněním pokynů k zaskladnění, nikoli pomocí funkce automatického přenosu, která je k dispozici v poli **Použít sešit zaskladnění**.

Pokud zaúčtujete příjemku ze skladu a nemáte vybrané pole **Použít sešit zaskladnění**, pak zboží, které má být přeloženo, se zobrazí jako samostatné řádky v instrukci zaskladnění. Pole **Informace o přeložení** na každém řádku zaskladnění zobrazuje, zda řádek obsahuje zboží přeložení, zboží ze stejné příjemky, které musí být uloženo, nebo zboží, které musí být uloženo pocházející z řádku příjmu, kde má být některé zboží přeloženo. V tomto poli mohou zaměstnanci snadno zjistit, proč není celé množství příjmu ukládáno.

Aplikace nevede samostatné záznamy o zboží, které bylo přeloženo, ale zapíše je jako běžné instrukce k zaskladnění.

## Nastavení skladu pro přeložení
1. Pokud používáte přihrádky, nastavte alespoň jednu přihrádku přeložení. Pokud používáte řízené zaskladnění a vyskladnění, nastavte zónu přeložení.

   Přihrádka přeložení má vybrané pole **Přihrádka přeložení** a musí mít vybrány oba typy: **K příjmu** a **Vyskladnění**. Pro více informací navštivte [Vytvoření přihrádek](warehouse-how-to-create-individual-bins.md) a [Nastavení typů přihrádek](warehouse-how-to-set-up-bin-types.md).

   Pokud používáte zóny, vytvořte zónu pro přihrádky přeložení a vyberte pole **Zóna přihrádky přeložení**. Pro více informací navštivte [Nastavení lokací pro použití přihrádek](warehouse-how-to-set-up-locations-to-use-bins.md).

2. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
3. Na stránce **Lokace** vyberte lokaci, kterou chcete nastavit ve skladu pro přeložení, a pak zvolte akci **Upravit**.
4. Na záložce **Sklad** zaškrtněte políčko **Použít přeložení** a vyplňte pole **Výpočet platnosti přeložení** časem pro hledání příležitostí přeložení.

   Možnost **Použít přeložení** je k dispozici pouze v případě, že jsou vybrána pole **Vyžadovat příjem**, **Vyžadovat dodání**, **Vyžadovat vyskladnění** a **Vyžadovat zaskladnění**.

5. Pokud používáte přihrádky, vyplňte na záložce **Přihrádky** pole **Kód přihrádky přeložení** kódem přihrádky, kterou chcete použít jako výchozí přihrádku přeložení.
6. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skladová jednotka** a poté vyberte související odkaz.
7. Pro každé zboží nebo skladovou jednotku, kterou chcete přeložit, vyberte zboží a zvolte akci **Upravit**.
8. Na stránce **Karta skladové jednotky** zaškrtněte políčko **Použít přeložení**.

> [!NOTE]
> Přeložení je možné pouze v případě, že je vaše lokace nastavena tak, aby vyžadovala příjem na sklad a zaskladnění.

## Přeložení zboží bez zobrazení příležitostí
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Příjemky na sklad** a poté vyberte související odkaz.
2. Vytvořte příjemky na sklad pro zboží, které dorazilo a může být případně přeloženo. Pro více informací navštivte [Příjem zboží](warehouse-how-receive-items.md).
3. Vyplňte pole **K  příjmu** a potom vyberte akci **Vypočítat přeložení**.

   Identifikovány jsou odchozí zdrojové doklady vyžadující zboží, u kterého je naplánováno opustit sklad v časovém období vzorců.  [!INCLUDE[d365fin](includes/d365fin_md.md)] vypočítá množství, takže můžete co nejvíce přeložit a vyhnout se nutnosti zaskladnění zboží, aniž byste museli hromadit příliš mnoho zboží v oblasti přeložení. Hodnota v poli **Množ. k přeložení** je tedy součet všech výstupních řádků požadujících zboží v období dopředního vyhledávání minus množství zboží, které již bylo umístěno v oblasti přeložení, nebo je to hodnota v poli **K  příjmu** na řádku příjemky, podle toho, která hodnota je menší. Nelze přeložit více, než jste přijali.

4. Pokud chcete přeložit množství, jak je navrženo, zaúčtujte příjemku. Můžete se také rozhodnout změnit přeložené množství na vyšší nebo nižší hodnotu a poté zaúčtovat příjemku.

   Částky, které mají být přeloženy, se nyní zobrazí jako řádky v zaskladnění, za předpokladu, že je pole **Použít sešit zaskladnění** zrušeno. Množství, která nejsou přeložena, se také stanou řádky v instrukci k zaskladnění.

   Pokud máte přihrádky, přeložené zboží bylo přiřazeno k výchozí přihrádce přeložení definované na kartě lokace.

5. Odstraňte řádky **Vzít** a **Vložit** pro zboží, které nebude přeloženo vůbec.
6. Vytiskněte instrukci pro zaskladnění pro zbývající řádky a umístěte množství příjmu, které musí být uloženo v příslušných přihrádkách nebo v příslušné oblasti skladu. Umístěte přeložené zboží do oblasti nebo přihrádky, která je pro ně určena v politice skladu. Někdy může politika skladu vyžadovat, abyste je prostě nechali v oblasti příjmu.
7. Chcete-li zapsat přeložené zboží jako zaskladněné a dostupné pro vyskladnění, zvolte akci **Zápis**.

## Přeložení zboží po zobrazení příležitostí
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Příjemky na sklad** a poté vyberte související odkaz.
2. Vytvořte příjemky na sklad pro zboží, které dorazilo a může být případně přeloženo. Pro více informací navštivte [Příjem zboží](warehouse-how-receive-items.md).

   Můžete chtít zobrazit řádky zdrojového dokladu, které požadují zboží před zaúčtováním příjmu.
3. Vyberte akci **Vypočítat přeložení**.

   Na stránce **Možnosti přeložení** se zobrazí nejdůležitější podrobnosti o řádcích požadujících zboží, například typ dokladu, požadované množství a datum splatnosti. Tyto informace vám mohou pomoci při rozhodování o tom, kolik chcete zboží přeložit, kam v oblasti přeložení zboží umístit, nebo jak je seskupit.

4. Vyberte akci **Automat.vyplnit  množ.k přel.**, abyste viděli, jak se vypočítávají množství na řádcích příjmu. Když změníte počet zboží v poli **Množ. k přeložení** na každém řádku, výpočet se aktualizuje při provádění změn. To neznamená, že konkrétní dodávka nebo výrobní zakázka skutečně obdrží zboží, které je navrženo pro přeložení, protože tyto manipulace jsou pouze pro testovací účely. Tento proces však může být informativní, pokud se jedná o více než jednu měrnou jednotku.
5. Pokud chcete rezervovat množství zboží pro konkrétní řádek objednávky, umístěte kurzor na tento řádek a pak zvolte akci **Rezervovat**. Na stránce **Rezervace** si nyní můžete rezervovat jakékoli dostupné množství zboží pro tuto konkrétní objednávku. Tato rezervace je jako každá jiná rezervace a nemá vyšší prioritu, protože byla vytvořena v souvislosti s přeložením. Pro více informací navštivte [Rezervovace zboží](inventory-how-to-reserve-items.md).
6. Po dokončení přepočtu nebo rezervace zvolte tlačítko **OK** abyste výpočet přenesli tak, jak jste jej revidovali, do pole **Množ. k přeložení** na řádku příjemky nebo zvolte tlačítko **Zrušit** pokud se chcete vrátit do příjemky skladu, kde můžete znovu vypočítat přeložení, pokud si budete přát.
7. Nyní můžete zaúčtovat příjemku a pokračovat v zaskladnění, jak je popsáno v krocích 3 až 7 v části „Přeložení zboží bez zobrazení příležitostí“.

> [!NOTE]
> V zaskladnění můžete podle potřeby i nadále měnit množství, která jsou zaskladněna do skladu nebo přeložena. Můžete se například rozhodnout přeložit další množství, abyste urychlili registraci přeložení.

## Zobrazení přeloženého zboží v sešitě dodávky nebo vyskladnění
Pokud používáte přihrádky, můžete při každém otevření dodávky nebo sešitu vyskladnění zobrazit aktualizovaný výpočet množství každého zboží v přihrádkách přeložení. To je cenná informace, pokud čekáte na příjem zboží. Když zjistíte, že zboží je k dispozici v přihrádce přeložení, můžete rychle vytvořit vyskladnění pro veškeré zboží v dodávce. V sešitu vyskladnění můžete řádky podle potřeby upravit a pak vytvořit vyskladnění.

Při vyskladnění zboží pro dodávku musíte nejprve vyhledat zboží v oblasti přeložení. Pokud jste během procesu příjmu zaznamenali zdrojové doklady, které byly základem pro přeložení, máte lepší představu o tom, zda lze zboží nalézt v oblasti přeložení nebo ne.

Po vydání výrobní zakázky jsou řádky k dispozici v sešitu vyskladnění a zobrazí se v poli **Množ. v přihr.přeložení** informace, zda zboží, na které čekáte, dorazilo a bylo umístěno do přihrádek přeložení. Při vytváření instrukce vyskladnění aplikace navrhne, abyste nejprve vybrali přeložené zboží a pak  vyhledali zboží v přihrádkách úložiště.

Pokud nepoužíváte přihrádky, musíte si čas od času zkontrolovat oblast přeložení nebo se spoléhat na oznámení z příjemky, že zboží pro výrobu dorazilo.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
