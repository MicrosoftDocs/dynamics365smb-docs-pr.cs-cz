---
    title: Walkthrough - Setting Up and Invoicing Sales Prepayments | Microsoft Docs
    description: Prepayments are payments that are invoiced and posted to a sales or purchase prepayment order before final invoicing. You may require a deposit before you manufacture items to order, or you may require payment before you ship items to a customer. You use the prepayments functionality in Business Central to invoice and collect deposits that are required from customers or remit deposits to vendors. Thus, you can make sure that all payments are posted against an invoice.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Návod: Nastavení a fakturace prodejních záloh

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

Zálohy jsou platby, které jsou fakturovány a zaúčtovány na prodejní nebo nákupní objednávku zálohy před konečnou fakturací. Než budete vyrábět zboží na objednávku, můžete požadovat zálohu, nebo můžete požadovat platbu před odesláním zboží zákazníkovi. Funkci záloh používáte v [!INCLUDE[prod_short](includes/prod_short.md)] k fakturaci a inkasování vkladů požadovaných od zákazníků nebo k úhradě vkladů prodejcům. Můžete tedy zajistit, aby byly všechny platby zaúčtovány na fakturu.

Požadavky na zálohu lze definovat pro zákazníka nebo dodavatele pro všechny zboží nebo jenom pro vybrané zboží. Po dokončení požadovaného nastavení můžete generovat zálohové faktury z prodejních a nákupních objednávek pro vypočtenou částku zálohy. Výchozí částky na faktuře můžete podle potřeby změnit. Můžete například poslat další zálohové faktury, pokud jsou k objednávce přidány další položky.

## Návod
Tento návod vás provede následujícími scénáři:

- Nastavení záloh
- Vytvoření objednávky, která vyžaduje zálohu
- Vytvoření zálohové faktury
- Oprava požadavků na zálohu u objednávky
- Uplatňování záloh na objednávku
- Fakturace konečné částky za objednávku se zálohou

### Role
Tento návod obsahuje úkoly pro následující role:

- Hlavní účetní (Phyllis)
- Zpracovatel objednávek (Susan)
- Správce pohledávek (Arnie)

## Příběh
Phyllis je hlavní účetní. Před výrobou nebo odesláním zboží rozhoduje o tom, kteří zákazníci jsou povinni zaplatit zálohu. Phyllis nastavuje [!INCLUDE[prod_short](includes/prod_short.md)] k automatickému výpočtu záloh.

Susan je zpracovatelka prodejní objednávky. Když zákazník zavolá a zadá objednávku, Susan zadá objednávku do systému, když je zákazník na telefonu. Tímto způsobem může okamžitě ověřit ceny a platební podmínky se zákazníkem a během jednání se zákazníkem může provádět úpravy objednávky.

Arnie pracuje v oddělení pohledávek, kde zaúčtuje faktury a platby.

V tomto scénáři Phyllis nastaví požadavky na zálohu pro zákazníka Selangorian, na základě jejich úvěrové historie, a dává Susan pokyny, jak zacházet s jejich objednávkami.

Když zákazník zavolá, Susan vyjednáva se zákazníkem, dokud nedosáhnou dohody. Poté se může rozhodnout vypočítat zálohu několika různými způsoby.

Poté, co Susan odešle zálohovou fakturu, zákazník si objedná další zboží. Susan aktualizuje objednávku a vytvoří druhou zálohovou fakturu.

Arnie zaregistruje platbu zákazníka a použije ji na faktury a poté odešle konečnou fakturu.

## Nastavení záloh
Phyllis nastavuje systém pro zpracování záloh pro zákazníky.

- Phyllis se rozhodne mít stejnou číselnou řadu pro zálohy jako ta, která se používá pro prodejní fakturaci.
- Phyllis nastaví aplikaci, aby zkontrolovala, zda jsou před konečnou fakturací objednávky vyžadovány zálohy.
- Phyllis nastavuje výchozí hodnoty pro požadované procento zálohy pro konkrétní položky a zákazníky.

Následující postupy popisují, jak splnit úkoly Phyllis:

#### Nastavení číselných řad pro zálohy
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení prodeje a pohledávek** a poté vyberte související odkaz.
2. Na stránce **Nastavení prodeje a pohledávek** rozbalte záložku **Číslování**.
3. Ověřte, že číselná řada pro zaúčtované zálohové faktury v poli **Čísla účtovaných  zál.  faktur** je stejná jako u zaúčtovaných prodejních faktur (**Čísla zaúčtovaných faktur**) a číselné řady zaúčtovaných dobropisů zálohy (**Čísla účtovaných  zál.  dobropisů**) je stejné jako u zaúčtovaných dobropisů (**Čísla zaúčtovaných dobropisů**).

#### Blokování zásilek pro nezaplacenou zálohu
1. Na stránce **Nastavení prodeje a pohledávek** na záložce **Obecné** zaškrtněte políčko **Zkontrolovat zálohu při účtování**.

   Nyní nemůžete odeslat ani fakturovat objednávku, která má nezaplacenou částku zálohy.

Ve výchozím nastavení vyžaduje Phyllis fakturaci zákazníkovi 20 000 na zálohu 30% na všechny objednávky. Proto zadá výchozí procento zálohy na kartě zákazníka.

Phyllis vyžaduje, aby všem zákazníkům byla fakturována 20% záloha za položku 1100. Zákazník 20000 má špatnou platební historii. Proto požaduje 40% zálohu od zákazníka 20000 za položku 1100. Následující postup znázorňuje, jak nastavit výchozí procenta záloh.

#### Přiřazení výchozích procent záloh zákazníkům a zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Otevřete kartu pro zákazníka 20000 (Selangorian).
3. Do pole **Záloha %** zadejte **30**.
4. Kliknutím na tlačítko **OK** zavřete zákaznickou kartu.
5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zboží** a poté vyberte související odkaz.
6. Otevřete kartu pro zákazníka 1100.
7. Vyberte akci  **Procentní části zálohy**.
8. Vyplňte dva řádky na stránce **Procentní části prodejní zálohy**.

   | **Typ prodeje** | **Kód prodeje** | **Číslo zboží** | **Záloha %** |
   |--------------------|--------------------|------------------|----------------------|  
   | **Zákazník** | **20000** | **1100** | **40** |
   | **Všichni zákazníci** | **1100** | **20** |

   > [!IMPORTANT]  
   > V závislosti na vaší zemi/regionu musíte také uvést kód daňové skupiny na záložce **Fakturace** pro zboží 1000 a 1100.

9. Zavřete všechny stránky.

#### Určení účtu pro prodejní zálohy v nastavení obecného účtování
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení obecného účtování** a poté vyberte související odkaz.
2. Vyberte řádek, kde je pole **Obecná  obch. účto skupina** nastaveno na **EXPORT** a pole **Obecná  účto  skupina zboží** je nastaveno na **RETAIL** a poté vyberte akci **Upravit**.
3. Na stránce **Karta nastavení obecného účto.** v poli **Účet záloh výnosů** zadejte příslušný účet.
4. Zvolte tlačítko **OK**.

## Vytvoření objednávky, která vyžaduje zálohu
V následujícím scénáři Susan, zpracovatel objednávek, vytvoří objednávku při rozhovoru se zákazníkem. Zboží, které zákazník objednává, vyžaduje zálohu a zákazník v minulosti provedl některé opožděné platby. Proto byla Susan instruována, aby požadovala pevnou částku 2 000 jako zálohu na objednávku.

Zákazník požaduje, aby mohl platit 35%, s čím může Susan souhlasit. Proto mění pořadí.

Susan vytvoří zálohovou fakturu a odešle ji zákazníkovi.

#### Vytvoření prodejní objednávky se zálohou
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
2. Vyberte akci **Nový**.
3. V poli **Zákazník-číslo** vyberte **20000**.
5. Přijměte zobrazené varování po splatnosti.
6. Vyplňte dva prodejní řádky následujícími informacemi.

   | **Typ** | **Číslo** | **Množství** |
   |--------------|-------------|------------------|  
   | **Zboží** | **1000** | **1** |
   | **Zboží** | **1100** | **1** |

   Ve výchozím nastavení jsou pole zálohy na prodejním řádku skrytá, takže je nutné je zobrazit.

7. Ověřte, zda pole **Záloha %** na řádku se zbožím **1000** obsahuje **30**. Výchozí hodnota byla převzata z prodejní hlavičky, která byla vyplněna z karty zákazníka.

   Pole **Záloha %** na řádku se zbožím **1100** obsahuje **40**. Toto je procento, které jste zadali na stránce **Procentní části prodejní zálohy** pro zboží **1100** a zákazníka **20000**.

   Pro více informací navštivte [Nastavení záloh](finance-set-up-prepayments.md).
8. Vyberte akci **Statistika**.
9. Na záložce **Záloha**, pole **Částka  řádku zálohy bez  DPH** obsahuje **1 560**. Pokud nyní pro objednávku vytvoříte zálohovou fakturu, pak se jedná o částku, která se zobrazí na faktuře.

   V tomto scénáři byla Susan instruována, aby navrhla celkovou zálohu 2000 za objednávku.

   > [!IMPORTANT]  
   > V závislosti na vaší zemi/regionu nemusí následující krok platit.
10. Změňte částku v poli **Částka  řádku zálohy bez  DPH** na **2000** a potom stránku zavřete.
11. Ověřte pole **Záloha %** na prodejních řádcích a uvidíte, že bylo přepočítáno na **40,81625**.

   Přepočet zahrnuje všechny řádky, které mají procento platby předem větší než 0.

   Nyní se zákazník zeptá, zda je možné nastavit procento zálohy na 35%. Susanina nadřízená změnu schvaluje.

12. Na stránce **Prodejní objednávka** zadejte do pole **Záloha %** hodnotu **35**.
13. V zobrazeném varování klikněte na tlačítko **Ano**. Jako procento platby pro celou objednávku bude použita sazba 35%.
14. Ověřte, zda byly řádky odpovídajícím způsobem aktualizovány.

## Vytvoření zálohové faktury
Po zadání správných hodnot zálohy na objednávce vytvoří Susan zálohovou fakturu a odešle ji zákazníkovi.

#### Vytvoření zálohové faktury

1. Na stránce **Prodejní objednávka** vyberte akci **Zaúčtovat zálohovou fakturu**.

> [!NOTE]  
> Susan by vybrala **Zaúčtovat a vytisknout zálohovou  fakturu** a fakturu by zaslala zákazníkovi.

## Vytvoření dodatečné zálohové faktury
Následující den zákazník zavolá Susan a provede změny v objednávce. Zákazník chce dva zboží 1100. Susan znovu otevře a aktualizuje objednávku a pak vytvoří druhou zálohovou fakturu na objednávce a odešle ji zákazníkovi.

#### Vytvoření dodatečné zálohové faktury

1. Na stránce **Prodejní objednávka** vyberte akci **Znovu otevřít**.
2. Na řádku pro zboží **1100** zadejte do pole **Množství** hodnotu **2**.

   Posunutím zobrazíte pole zálohy. Pole **Částka řádku zálohy bez  DPH** nyní obsahuje  **630** a pole **Fakt.  částka  zál.  bez  DPH** obsahuje **315**. To ukazuje, že existuje další částka zálohy, která ještě nebyla fakturována.
3. Chcete-li zaúčtovat fakturu s další částkou zálohy, vyberte akci **Zaúčtovat zálohovou fakturu**.

## Uplatnění záloh
Zákazník zaplatí částku zálohy a Arnie, která pracuje v účetním oddělení, zaregistruje platbu a použije ji na zálohové faktury.

#### Použití platby na zálohové faktury

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Deníky přijaté hotovosti** a poté vyberte související odkaz.
2. Vyplňte řádek deníku následujícími informacemi.

   | Název pole | Zadejte |
   |----------------|-----------|  
   | **Typ dokladu** | **Platba** |
   | **Typ účtu** | **Zákazník** |
   | **Číslo účtu** | **20000** |
3. Vyberte akci **Vyrovnat položky**.
4. Na stránce **Vyrovnat položky zákazníka** vyberte první zálohovou fakturu a poté vyberte akci **Nastavit ID vyrovnání**.
5. Opakujte předchozí krok pro druhou zálohu.
6. Zvolte tlačítko **OK**.

   Pole částky bylo nyní vyplněno součtem dvou zálohových faktur.

7. Zaúčtujte deník.

## Fakturace zbývající částky
Nyní byla Arnie informována, že položky v objednávce byly odeslány a že objednávka je připravena k fakturaci. Arnie vytvoří fakturu za objednávku.

#### Fakturace zbývající částky
1. Otevřete prodejní objednávku.
2. Vyberte akci **Dodat a fakturovat** a poté klikněte na tlačítko **OK**.

> [!NOTE]  
> Za normálních okolností by přepravní oddělení zásilku již zaúčtovalo.

Arnie může zobrazit historii a ověřit, zda byla prodejní faktura vytvořena tak, jak bylo zamýšleno.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete udělat"), zadejte **Účtované prodejní faktury** a poté vyberte související odkaz.

## Další kroky
Tento návod vás provedl kroky k nastavení [!INCLUDE[prod_short](includes/prod_short.md)] pro zpracování záloh. Nastavili jste výchozí procenta předplacení u zákazníků a položek a také jste použili různé metody pro výpočet zálohy u objednávky. Pokusili jste se přiřadit jednu celkovú částku zálohy k objednávce a nechali jste si částku zálohy vypočítat jako procento z celé objednávky.

Zaúčtovali jste také zálohovou fakturu, vytvořili jste druhou zálohovou fakturu, když se změnila objednávka, a zaúčtovali jste konečnou fakturu pro zbývající částku.

Funkce záloh v [!INCLUDE[prod_short](includes/prod_short.md)] usnadňuje nastavení a vynucení pravidel záloh pro zákazníky a zboží a umožňuje zaúčtovat každou platbu na fakturu.

## Viz také
[Fakturace záloh](finance-invoice-prepayments.md)    
[Finance](finance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]