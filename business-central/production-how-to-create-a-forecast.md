---
    title: How to Create a Demand Forecast | Microsoft Docs
    description: You can create sales and production forecasts with the **Demand Forecast** page.
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
# Vytvoření prognózy
Prognózy prodeje a výroby můžete vytvořit na stránce **Prognóza poptávky**.

Prognóza se používá k vytvoření očekávané poptávky; skutečná poptávka je vytvořena z prodejních a výrobních zakázek. Při vytváření hlavního plánu výroby (MPS) je prognóza započtena proti prodejním a výrobním objednávkám. Možnost *Komponenta* v prognóze určuje, jaký typ požadavků je třeba zohlednit v procesu vzájemného započtení. Pokud je prognóza pro zboží prodeje, prognózu tvoří pouze prodejní objednávky. Pokud se jedná o komponenty, pouze závislá poptávka z komponent výrobní zakázky vytvoří prognózu.

Prognózování umožňuje vaší společnosti vytvářet scénáře "co kdyby" a efektivně a nákladově efektivně plánovat a uspokojovat poptávku. Přesné předpovědi mohou zásadně změnit úroveň spokojenosti zákazníků s ohledem na slibná data objednávek a včasné dodání.

## Prognózy prodeje a prognózy výroby
Funkce prognózy v aplikaci lze použít k vytvoření prognóz prodeje nebo výroby v kombinaci nebo nezávisle. Například většina společností na zakázku neprovádí zásoby hotových výrobků, protože každé zboží je vyrobeno při objednání. Předvídání objednávek (prognózy prodeje) je rozhodující pro přiměřenou dobu obratu hotového zboží (prognóza výroby). Například součásti s dlouhými dodacími lhůtami, pokud nejsou na objednávce nebo na skladě, mohou zpozdit výrobu.

- Prognóza prodeje je nejlepším odhadem obchodního oddělení ohledně toho, co se bude v budoucnu prodávat, a je určeno zbožím a obdobím. Prognóza prodeje však není vždy pro plánování výroby dostatečná.
- Prognóza výroby je projekce plánovače výroby o tom, kolik koncového zboží a odvozených podsestav má být v určitých obdobích k dispozici pro splnění předpokládaného prodeje.

Ve většině případů tedy plánovač výroby upraví prognózu prodeje tak, aby odpovídala podmínkám výroby, přesto stále ještě splňuje prognózu prodeje.

Prognózy můžete vytvářet ručně na stránce **Prognóza poptávky**. V systému může existovat více prognóz a jsou rozlišeny podle názvu a typu. Prognózy lze podle potřeby kopírovat a upravovat. Všimněte si, že pro plánování je platná pouze jedna předpověď.

Prognóza se skládá z počtu záznamů, z nichž každý uvádí číslo zboží, datum prognózy a předpokládané množství. Prognóza zboží zahrnuje období, které je definováno datem prognózy a datem prognózy dalšího (pozdějšího) záznamu prognózy. Z hlediska plánování by mělo být předpokládané množství dostupné na začátku období poptávky.

Prognózu musíte označit jako *Zboží prodeje*, *Componentu* nebo *Obojí*. Typ prognózy *Zboží prodeje* se používá pro prognózu prodeje. Prognóza výroby je vytvořena pomocí typu *Komponenta*. Typ prognózy *Obojí* se používá pouze k tomu, aby poskytla plánovači přehled o prognóze prodeje i prognóze výroby. Při této možnosti nelze zboží prognózy upravovat. Určením těchto typů prognóz zde můžete použít stejný seznam k zadání prognózy prodeje i prognózy výroby a použít stejný seznam k zobrazení obou prognóz současně. Všimněte si, že systém zachází s různými vstupy (prodeje a výroby) odlišně při výpočtu plánování na základě zboží, výroby a nastavení výroby.

## Prognóza komponent
Prognóza komponenty může být zobrazena jako prognóza možností ve vztahu k nadřazenému zboží. To může být například užitečné, pokud plánovač dokáže odhadnout poptávku po komponentě.

Protože prognóza komponenty je určena k definování možností pro nadřazené zboží, prognóza komponenty by měla být stejná nebo menší než množství prognózy prodejného zboží. Pokud je prognóza komponenty vyšší než prognóza prodejného zboží, považuje systém rozdíl mezi těmito dvěma typy prognózy za nezávislou poptávku.

## Prognóza období
Prognóza období je platná od jeho počátečního data do data, kdy začíná další prognóza. Stránka časového intervalu vám dává více možností, jak vložit poptávku k určitému datu v období. Nedoporučuje se proto měnit rozsah období prognózy, pokud nechcete přesunout všechno zboží prognózy na počáteční datum tohoto období.

## Prognóza podle lokací
Ve výrobním nastavení může být uvedeno, zda chcete při výpočtu plánu filtrovat prognózu podle lokace. Mějte však na paměti, že pokud jsou prognózy založené na lokaci zobrazovány izolovaně, nemusí být celková prognóza reprezentativní.

## Vytvoření prognózy poptávky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prognóza poptávky** a poté vyberte související odkaz.
2. Na záložce **Obecné** vyberte prognózu v poli **Název prognózy poptávky**. Může existovat více prognóz a jsou rozlišeny podle názvu a typu prognózy.
3. V poli **Filtr lokace** vyberte lokaci, na které se tato prognóza použije.
4. V poli **Zobrazit podle** můžete změnit periodu, která je zobrazena v každém sloupci. Můžete si vybrat z následujících intervalů: **Den**, **Týden**, **Měsíc**, **Čtvrtletí**, **Rok** nebo **Účetní období**  nastavené ve vaší finanční oblasti.

> [!NOTE]
> Měli byste zvážit, jaký časový interval chcete použít pro budoucí prognózy, aby byl časový interval v celém průběhu konzistentní. Když zadáte množství prognózy, je platné první den vybraného časového intervalu. Pokud například vyberete měsíc, zadáte odhadované množství první den v měsíci. Pokud vyberete čtvrtletí, zadáte předpokládané množství první den prvního měsíce v čtvrtletí.

5. V poli **Zobrazit jako** vyberte způsob zobrazení předpokládaného množství pro časový interval. Pokud vyberete **Pohyb**, zobrazí se pro časový interval pohyb zůstatku. Pokud vyberete **Saldo do data** zobrazí se na stránce saldo k poslednímu dni v časovém intervalu.
6. V poli **Typ prognózy** vyberte **Zboží prodeje**,  **Componenta** nebo **Obojí**. Pokud vyberete **Zboží prodeje** nebo **Componentu**, můžete upravit množství podle období. Pokud vyberete **Obojí**, nemůžete množství upravit, ale můžete zvolit tlačítko se šipkou rozevíracího seznamu a zobrazit položky prognózy poptávky.
7. Zadejte **Filtr data** pokud chcete omezit množství zobrazených dat.
8. Na záložce **Matice prognózy poptávky** zadejte předpokládané množství zadáním množství do buňky představující zboží k určitému datu nebo období. Všimněte si, že v prázdných buňkách vyhledávací tlačítko otevře prázdnou stránku označující, že je nutné zadat hodnotu ručně.

> [!NOTE]
> Můžete také upravit existující prognózu. Na stránce **Matice prognózy poptávky** vyberte akci **Kopírovat prognźu poptávky**  a vyplňte stránku **Prognóza poptávky** existující prognózou. Množství pak můžete podle potřeby upravit.

## Viz také
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)  
[Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
