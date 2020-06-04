---
title: Nastavení cen a účto skupin projektů | Microsoft Docs
description: 'Popisuje, jak nastavit obecné informace o projektech a nastavit ceny za zboží projektu, zdroje, a finanční účty a účto skupiny projektů.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management
ms.date: 10/01/2018
ms.author: sgroespe
---
# <a name="set-up-jobs"></a>Nastavení projektů
Na stránce **Nastavení projektů** musíte určit, jak chcete používat určité funkce projektu.

Na jednotlivých kartách projektů musíte nastavit ceny za zboží projektů, zdroje projektů a  finanční účty projektů a musíte nastavit účto skupiny projektů.

## <a name="to-set-general-information-for-jobs"></a>Nastavení obecných informací o projektech
1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Nastavení projektů** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Zaškrtávací políčko **Použít propojení spotřeby jako výchozí** je poměrně složité, a proto je vysvětleno v následující části.

## <a name="to-set-up-job-usage-tracking"></a>Pro nastavení sledování spotřeby projektu
Když realizujete projekt, možná budete chtít vědět, jak vaše spotřeba sleduje váš plán. Chcete-li to snadno provést, můžete vytvořit vazbu mezi řádky plánování projektu a skutečným využitím. To vám umožní sledovat vaše náklady a snadno zjistit, kolik práce zbývá ještě udělat. Ve výchozím nastavení je typem řádku plánování projektu **Rozpočet**, ale použití typu řádku **Obojí plán i fakturovatelné** má podobný efekt.

Pokud zaškrtnete zaškrtávací políčko **Použít propojení spotřeby jako výchozí**, můžete zkontrolovat informace na řádku plánování projektu. Můžete nastavit množství zdroje, zboží nebo účtu hlavní knihy a pak určit, jaké množství chcete přenést do deníku projektu. Pole **Zbývající množství** na řádku plánování projektu vám řekne, co zbývá k převodu a zaúčtování do deníku projektů.

Když je zaškrtnuto zaškrtávací políčko **Použít propojení spotřeby jako výchozí** a typ řádku plánování projektu je **Fakturovatelné**, finanční deník vytvoří řádek plánování projektu typu **Rozpočet** po zaúčtování řádku deníku.

> [!NOTE]  
>   Pokud je na kartě projektu zaškrtnuto zaškrtávací políčko**Použít propojení spotřeby jako výchozí** a pole **Typ řádku** na řádku deníku projektů je prázdné, vytvoří se při účtování řádků deníku nové řádky plánování projektu typu **Rozpočet**. Pokud na kartě projektu není zaškrtnuto zaškrtávací políčko **Použít propojení spotřeby jako výchozí** a pole **Typ řádku** na řádku deníku projektů je prázdné, nevytvoří se při účtování řádků deníku žádné nové řádky plánování projektu. Pro více informací navštivte [Zaznamenání spotřeby pro projekty](projects-how-record-job-usage.md).

1. Vyberte ikonu ![Hledat stránku nebo sestavu](media/ui-search/search_small.png "ikona Hledat stránku nebo sestavu"), vstupte do **Nastavení projektů** a poté vyberte související odkaz.
2. Zaškrtněte nebo zrušte zaškrtnutí políčka **Použít propojení spotřeby jako výchozí**. 

> [!NOTE]  
>   Na jednotlivých kartách projektů můžete provést jiné nastavení zaškrtávacího políčka **Použít propojení spotřeby jako výchozí**. V takovém případě má nastavení tohoto projektu přednost před obecným výchozím nastavením popsaným výše.

## <a name="to-set-up-prices-for-job-resources"></a>Nastavení ceny zdrojů projektů
Můžete nastavit konkrétní ceny zdrojů pro projekt. K tomu použijte stránku **Ceny zdrojů projektu**.

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Projekty** a poté vyberte související odkaz.  
2. Vyberte příslušný projekt a pak zvolte akci **Zdroj**.
3. Na stránce **Ceny zdrojů projektu** vyplňte pole podle potřeby.

Volitelné informace v polích **Číslo úlohy projektu**, **Typ práce**, **Kód měny**, **Řádková sleva %** a **Faktor pořizovací ceny** se použijí na řádcích plánování projektu a v denících spotřeby, když je tento zdroj vložen a přidán do projektu.  

Hodnota v poli **Jednotková cena** pro zdroj bude použita na řádcích plánování projektu a v denících projektů, když je tento zdroj, zdroj přiřazený ke skupině zdrojů nebo jakýkoli zdroj zadán.  

> [!NOTE]  
>   Tato cena vždy přepíše všechny ceny nastavené na existující stránce **Prodejní cena zdroje/Prodejní cena skupiny zdrojů**

## <a name="to-set-up-prices-for-job-items"></a>Nastavení ceny zboží projektu
Můžete nastavit konkrétní ceny zboží pro projekt. K tomu použijte stránku **Ceny za zboží projektu**

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Projekty** a poté vyberte související odkaz.  
2. Vyberte příslušný projekt a pak zvolte akci **Zboží**.
3. Na stránce **Ceny za zboží projektu** vyplňte pole podle potřeby.

Volitelné informace v polích **Číslo úlohy projektu**, **Kód měny** a **Řádková sleva %** se použijí na řádcích plánování projektu a v denících projektů, když je toto zboží vloženo nebo přidáno do projektu.  

Hodnota v poli **Jednotková cena** pro zboží bude použita na řádcích plánování projektu a v denících projektů, když je toto zboží zadáno.  

> [!NOTE]  
>   Tato cena vždy přepíše běžnou zákaznickou cenu (mechanismus „nejlepší ceny“) u zboží. Pokud chcete použít běžné mechanismy zákaznických cen, neměli byste pro projekt vytvářet žádné ceny za zboží projektu.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Chcete-li nastavit ceny za účty hlavní knihy projektu
Můžete nastavit konkrétní ceny pro finanční výdaje za projekt. K tomu použijte stránku **Ceny fin. účtu projektu**.

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Projekty** a poté vyberte související odkaz.  
2. Vyberte příslušný projekt a pak zvolte akci **Finanční účet**.  
3. Na stránce **Ceny fin. účtu projektu** vyplňte pole podle potřeby.

Volitelné informace v polích **Číslo úlohy projektu**, **Kód měny**, **Řádková sleva %**, **Faktor pořizovací ceny** a **Pořizovací cena** se použijí na řádcích plánování úloh a v denících projektů, když je tento účet hlavní knihy zadán a přidán do projektu.  

Hodnota v poli **Pořizovací cena** pro částku výdajů v hlavní knize projektu bude použita na řádcích plánování projektu a v denících projektů, když je tento účet hlavní knihy zadán.

## <a name="to-set-up-job-posting-groups"></a>Pro nastavení účto skupin
Jedním aspektem plánování projektů je rozhodování, které účty pro účtování se použijí pro kalkulaci nákladů na projekt. Abyste mohli účtovat projekty, musíte nastavit účty pro účtování pro každou účto skupinu projektu. Účto skupina představuje spojení mezi projektem a tím, jak by se s ním mělo zacházet v hlavní knize. Při vytváření projektu zadáte účto skupinu a ve výchozím nastavení je každá úloha, kterou pro projekt vytvoříte, spojena s touto účto skupinou. Při vytváření úkolů však můžete přepsat výchozí nastavení a vybrat vhodnější účto skupinu.  

> [!NOTE]  
>   Než nastavíte účto skupiny, je nutné nastavit potřebné účty v účetní osnově. Pro více informací navštivte [Nastavení nebo změna účetní osnovy](finance-setup-chart-accounts.md).  

1. Vyberte ikonu ![Žárovka, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), vstupte do **Účto skupiny projektů** a poté vyberte související odkaz.  
2. Zvolte akci **Nový** a pak vyplňte pole účtu, jak je popsáno v následující tabulce.  

| Pole účtu | Popis |
| --- | --- |
| **Kód** |Kód pro účto skupinu. Můžete zadat až 10 znaků včetně mezer. |
| **Účet nákladů NV** |Účet NV pro vypočítané náklady na projekt, což je účet rozvahových majetkových aktiv. |
| **Účet kumulovaných nákladů NV** |Účet pro metody Hodnota nákladů nebo Náklady na prodej pro výpočet NV, což je účet rozvahových majetkových pasiv. To bude zaúčtováno, když úprava NV vyžaduje, aby se zvýšily náklady na spotřebu zaúčtované ve výsledovce. |
| **Účet použitých nákladů projektu** |Vyrovnávací účet k účtu nákladů NV, což je protiklad k účtu záporných výdajů. |
| **Účet použitých nákladů zboží** |Vyrovnávací účet k účtu nákladů NV, což je protiklad k účtu záporných výdajů. |
| **Účet použitých nákladů zdroje** |Vyrovnávací účet k účtu nákladů NV, což je protiklad k účtu záporných výdajů. |
| **Účet použitých nákladů** |Vyrovnávací účet k účtu nákladů NV, což je protiklad k účtu záporných výdajů. |
| **Účet adjustace nákladů projektu** |Vyrovnávací účet k účtu kumulovaných nákladů NV |
| **Účet časového rozlišení výdajového účtu (Rozpočet)** |Prodejní účet, který bude použit pro výdaje hlavní knihy v úkolech projektu s touto účto skupinou. Pokud zůstane prázdný, použije se účet hlavní knihy zadaný na řádku plánování projektu. |
| **Účet kumulovaných výnosů NV** |Účet NV pro vypočítanou prodejní hodnotu NV, což je účet rozvahových časově rozlišených výnosů. To se zaúčtuje, když úprava NV vyžaduje zvýšení vykázaných výnosů. |
| **Účet fakturovaných výnosů NV** |Účet pro fakturovanou prodejní hodnotu NV, kterou nelze deaktivovat. Jedná se o účet rozvahy nevydělaných výnosů. |
| **Účet použitých výnosů projektu** |Vyrovnávací účet k účtu fakturovaných výnosů NV, což je protiklad k účtu příjmů. |
| **Účet adjustace výnosů projektu** |Vyrovnávací účet k účtu prodeje NV projektů, což je účet příjmů. |
| **Účet deaktiv.nákladů** |Účet výdajů, který obsahuje deaktivované náklady za projekt. Jedná se obvykle o debetní účet výdajů. |
| **Účet deaktiv.výnosů** |Účet příjmů, který obsahuje uznané příjmy za projekt. Jedná se obvykle o účet s příjmem z úvěru. |

## <a name="see-also"></a>Viz také
[Nastavení správy projektu](projects-setup-projects.md)  
[Správa projektů](projects-manage-projects.md)  
[Finance](finance.md)  
[Nakupování](purchasing-manage-purchasing.md)         
[Prodej](sales-manage-sales.md)      
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
