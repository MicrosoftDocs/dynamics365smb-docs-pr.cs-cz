---
    title: Defining and Allocating Costs | Microsoft Docs
    description: Cost allocations move costs and revenues between cost types, cost centers, and cost objects. You can define as many allocations as you need.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Definování a rozdělení nákladů
Rozdělení nákladů přesouvá náklady a výnosy mezi typy nákladů, nákladová střediska a nositele nákladů. Můžete definovat tolik rozdělení, kolik potřebujete. Každé rozdělení se skládá z:

- Zdroj rozdělení.
- Jeden nebo více cílů rozdělení.

Zdroj rozdělení stanoví, které náklady musí být rozděleny, a cíle rozdělení určují, kde musí být náklady rozděleny. Například zdrojem rozdělení mohou být náklady na typ nákladů na elektřinu a topení. Veškeré náklady na elektřinu a vytápění rozdělujete třem nákladovým střediskům: Dílna, výroba a prodej. Tato nákladová střediska jsou vaše cíle rozdělení.

Pro každý zdroj rozdělení definujete úroveň rozdělení, dobu platnosti a variantu jako identifikátor seskupení. Dávkovou úlohu můžete použít k nastavení filtrů pro výběr definic rozdělení a poté automaticky spustit rozdělení nákladů.

Pro každý cíl rozdělení definujete základ rozdělení. základ rozdělení může být statický nebo dynamický.

- Statické základy rozdělení jsou založeny na určité hodnotě, jako jsou metre čtvereční nebo stanovený poměr rozdělení, například 5:2:4.
- Dynamické základy rozdělení závisí na proměnlivých hodnotách, jako je počet zaměstnanců v nákladovém středisku nebo tržby z prodeje nositele nákladů v průběhu určitého časového období.

Následující tabulka popisuje posloupnost úkolů s odkazy na témata, která je popisují.

## Nastavení zdroje a cílů rozdělení
Každé rozdělení se skládá ze zdroje rozdělení a jednoho nebo více cílů rozdělení. Zdroj rozdělení definuje, které náklady budou rozděleny. Cíle rozdělení určují, kde budou náklady rozděleny.

### Nastavení rozdělení nákladů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Rozdělení nákladů** a poté vyberte související odkaz.
2. Na stránce **Rozdělení nákladů** vyberte akci **Upravit**.
3. Do pole **ID** zadejte ID zdroje rozdělení.
4. Definujte úroveň jako číslo mezi 1 a 99 v poli  **Úroveň**. Rozdělení nákladů bude odpovídat pořadí úrovní.
5. Do pole **Rozsah druhů nákladů** zadejte typ nákladů a určete, které typy nákladů budou rozděleny. Pokud jsou pro určitý typ nákladů rozděleny všechny náklady, není definován žádný rozsah.
6. Do pole **Kód nákladového střediska** zadejte nákladové středisko spolu s náklady, které mají být rozděleny.
7. Do pole **Kód nositele nákladů** zadejte nositele nákladů spolu s náklady, které mají být rozděleny. Toto pole zůstává nejčastěji prázdné, protože nositele nákladů jsou zřídka přiděleny jiným nositelům nákladů.
8. Do pole **Kredit k typu nákladu** zadejte typ nákladů. Náklady, které jsou rozděleny, budou připsány k typu zdrojových nákladů. Zaúčtování kreditu bude zaúčtováno na typ nákladů zde uvedený.
9. Na záložce **Řádky** definujte cíle rozdělení. Na prvním řádku zadejte typ nákladů do pole **Cílový druh nákladů**. Definuje, jaký typ nákladů se zaúčtuje.
10. Na prvním řádku zadejte první cíl rozdělení do pole **Cílové nákladové středisko** nebo **Cílový nositel nákladů**. Tato dvě pole definují, na které nákladové středisko nebo nositele nákladů se rozdělení zaúčtuje. Můžete vyplnit pouze jedno z těchto polí, ale ne obojí.
11. Stejným postupem na druhém řádku nastavte další cíle rozdělení.
12. Po nastavení cíle a zdrojů rozdělení vyberte akci **Vypočítat klíče rozdělení** a vypočítejte hodnoty celkové sdílené složky.

> [!NOTE]
> Zaškrtnutím políčka **Uzavřeno** deaktivujete nastavení rozdělení.

## Nastavení filtrů pro dynamické základy rozdělení
Metoda dynamického rozdělování je založena na proměnných hodnotách. Například počet zaměstnanců v nákladovém středisku nebo položky prodané z nositele nákladů v konkrétním časovém období. Existuje devět předdefinovaných základů rozdělení a dvanáct dynamických časových období. Můžete nastavit různé filtry na základě základu rozdělení.

### Nastavení filtrů pro dynamické základy rozdělení
Následující tabulka ukazuje, které filtry jsou možné pro různé základy rozdělení a které hodnoty jsou platné v polích **Filtr  čísla** a **Filtr skupiny**. Stisknutím F1 v poli **Kód filtru data** zobrazíte podrobné popisy.

| **Základ** | **Filtr  čísla** | **Kód filtru data** | **Filtr nákladového střediska** | **Filtr nositele nákladů** | **Filtr skupiny** |
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
| Věcné položky | Finanční účet | Ano | Ano | Ano | N/A |
| Položky finančního rozpočtu | Finanční účet | Ano | Ano | Ano | Název fin.rozpočtu |
| Položky druhu nákladů | Druh nákladu | Ano | Ano | Ano | N/A |
| Položky rozpočtu nákladů | Druh nákladu | Ano | Ano | Ano | Název rozpočtu |
| Počet zaměstnanců | N/A | Ano | Ano | Ano | N/A |
| Zboží prodáno (Mn.) | Číslo zboží | Ano | Ano | Ano | Účto skupina zboží |
| Zboží pořízeno (Mn.) | Číslo zboží | Ano | Ano | Ano | Účto skupina zboží |
| Zboží prodáno (Částka) | Číslo zboží | Ano | Ano | Ano | Účto skupina zboží |
| Zboží pořízeno (Částka) | Číslo zboží | Ano | Ano | Ano | Účto skupina zboží |

## Scénář 1: Definování statických rozdělení na základě poměru rozdělení
Metoda statického rozdělení je založena na určité hodnotě, například použitých metrech čtverečních, nebo na stanoveném poměru rozdělení, například 5:2:4.

Toto téma popisuje, jak definovat tři nové nositele cílových nákladů rozdělení pro nákladové středisko zdroje rozdělení PROD pomocí stanoveného poměru rozdělení 5:2:4. Tři cílové nositele nákladů jsou PRISLUS, BARVA a KOVÁNÍ.

> [!NOTE]
> Příklad používá demo data v [!INCLUDE[d365fin](includes/d365fin_md.md)].

### Definování zdroje rozdělení pro nákladové středisko PROD na záložce Obecné

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Rozdělení nákladů** a poté vyberte související odkaz.
2. Na stránce **Rozdělení nákladů** vyberte akci **Nový**.
3. V poli **ID** stiskněte klávesu Enter nebo zadejte ID.
4. Do pole **Úroveň** zadejte **1**.
5. Do polí **Platnost od** a **Platnost do** zadejte příslušná data.
6. Do pole **Kód nákladového střediska** zadejte **VÝROBA**.
7. Do pole **Kredit k typu nákladu** zadejte typ nákladů **9903**.

### Definování cíle rozdělení nositele nákladů na záložce Řádky

1. Na prvním řádku zadejte do pole **Cílový druh nákladů** **9903**.
2. Na prvním řádku v poli **Cílový nositel nákladů** vyberte **PRISLUS**.
3. Na prvním řádku v poli **Typ cíle rozdělení** vyberte **Všechny náklady** a definujte, jak budou rozděleny všechny vzniklé náklady.
4. Na prvním řádku v poli **Základ** vyberte **Staticky** a použijte metodu statického rozdělení.
5. Na prvním řádku zadejte do pole **Podíl** poměr rozdělení **5**.
6. Na druhém řádku zadejte do pole **Cílový druh nákladů** **9903**.
7. Na druhém řádku v poli **Cílový nositel nákladů** vyberte **BARVA**.
8. Na druhém řádku v poli **Typ cíle rozdělení** vyberte **Všechny náklady** a definujte, jak budou rozděleny všechny vzniklé náklady.
9. Na druhém řádku v poli **Základ** vyberte **Staticky** a použijte metodu statického rozdělení.
10. Na druhém řádku zadejte do pole **Podíl** poměr rozdělení **2**.
11. Na třetím řádku zadejte do pole **Cílový druh nákladů** **9903**.
12. Na třetím řádku v poli **Cílový nositel nákladů** vyberte **KOVÁNÍ**.
13. Na třetím řádku v poli **Typ cíle rozdělení** vyberte **Všechny náklady** a definujte, jak budou rozdeleny všechny vzniklé náklady.
14. Na třetím řádku v poli **Základ** vyberte **Staticky** a použijte metodu statického rozdělení.
15. Na třetím řádku zadejte do pole **Podíl** poměr rozdělení **4**.

> [!IMPORTANT]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky vypočítá pole **Procento** pomocí procentuální sazby, která je závislá na všech třech poměrech rozdělení zadaných do pole **Podíl** pro všechny tři řádky.

## Scénář 2: Definování dynamických rozdělení na základě prodaných položek
Toto téma ukazuje příklad, jak definovat rozdělení pomocí metody dynamického rozdělování. V příkladu změníte dynamické rozdělení nákladů pro nákladové středisko PRODEJE na podporu nového nositele nákladů IT VYBAVENÍ. Balíčky IT VYBAVENÍ mají čísla položek v rozsahu od 8904-W do 8924-W. K výpočtu podílu použijete údaje z prodeje za předchozí rok. Rozdělení je zaúčtováno na typ nákladů 9903.

> [!NOTE]
> Příklad používá demo data v [!INCLUDE[d365fin](includes/d365fin_md.md)].

### Definování dynamických rozdělení na základě položek prodaných v předchozím roce

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Rozdělení nákladů** a poté vyberte související odkaz.
2. Na stránce **Rozdělení nákladů** vyberte akci **Nový**.
3. V poli **ID** stiskněte klávesu Enter nebo zadejte ID.
4. Do pole **Úroveň** zadejte **1**.
5. Do polí **Platnost od** a **Platnost do** zadejte příslušná data.
6. Do pole **Kód nákladového střediska** zadejte **PRODEJ**.
7. Do pole **Kredit k typu nákladu** zadejte typ nákladů **9903**.
8. Do pole **Cílový druh nákladů** zadejte typ nákladů **9903**.
9. V poli **Cílový nositel nákladů** vyberte **Nový** a vytvořte nového nositele nákladů IT VYBAVENÍ a podle potřeby vyplňte pole. Vyberte **IT VYBAVENÍ**. Pole **Cílové nákladové středisko** ponechte prázdné.
10. V poli **Typ cíle rozdělení** vyberte **Všechny náklady** a určete, jak budou rozděleny všechny akumulované náklady.
11. V poli **Základ** vyberte základ rozdělení **Zboží prodáno (Částka)**.
12. V poli **Filtr  čísla**, zadejte **8904-W..8924-W**.
13. V poli **Kód filtru data**, zadejte **Poslední rok**.
14. Vyberte akci **Vypočítat klíče rozdělení** pro výpočet podílu.

> [!IMPORTANT]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] používá údaje o obratu z minulých let pro výpočet podílu 1596.50 LM se 100 procenty pro balíčky IT VYBAVENÍ. To znamená, že všechny položky prodané v loňském roce budou rozděleny do nákladového objektu IT VYBAVENÍ.

## Viz také
[Nastavení nákladového účetnictví](finance-set-up-cost-accounting.md)  
[Transfer a účtování položek nákladů](finance-transfer-and-post-cost-entries.md)  
[Účtování nákladů](finance-manage-cost-accounting.md)  
[Terminologie v nákladovém účetnictví](finance-terminology-in-cost-accounting.md)  
[O nákladovém účetnictví](finance-about-cost-accounting.md)
