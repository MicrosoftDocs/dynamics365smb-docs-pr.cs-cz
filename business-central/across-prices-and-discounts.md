---
title: Set Up Prices and Discounts
description: Describes how to define standard and special price and discount agreements for sales and purchases.
author: bholtorf

ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: price, pricing, discount, discounting, rebate, sale, purchase, invoice
ms.date: 04/01/2021
ms.author: bholtorf

---
# Nastavení cen a slev
> [!NOTE]
> Ve druhé vlně vydání 2020 jsme uvolnili zjednodušené procesy pro nastavení a správu cen a slev. Pokud jste nový zákazník a používáte tuto verzi, používáte nové prostředí. Pokud jste stávajícím zákazníkem, závisí použití nového prostředí na tom, zda váš správce povolil aktualizaci funkce **Nové prodejní ceny** na stránce **Správa funkcí**. Další informace naleznete v tématu [Povolení nadcházejících funkcí s předstihem](/dynamics365/business-central/dev-itpro/administration/feature-management).

Cenové a slevové strategie pro nákup a prodej zboží a služeb jsou základními nástroji úspěšného podnikání. Po nastavení zboží a služeb, které vaše společnost nakupuje a prodává, můžete definovat, kolik za ně zaplatíte nebo naúčtujete, a tyto částky se automaticky přidají do prodejních a nákupních dokladů.

## Nastavení cen a slev
Před vytvořením ceníků je třeba definovat cenové a slevové strategie na stránkách **Nastavení prodeje a pohledávek** a **Nastavení nákupu a závazků**.

Můžete nastavit a používat dva typy slev:

| Typ slevy | Popis |
| --- | --- |
| **Řádková sleva** | Částka slevy, která je uvedena pro řádky v prodejních a nákupních dokladech. Řádkové slevy jsou obvykle založeny na kombinaci zákazníka, zboží, minimálního množství, měrné jednotky nebo časového období, které definujete pro prodej a nákup na stránkách **Nastavení prodeje a pohledávek** a **Nastavení nákupu a závazků**. |
| **Fakturační sleva** | Procento slevy, které se odečte od celkové částky prodejního a nákupního dokladu, pokud součet všech řádků dokladu překročí určité minimum. |

Protože prodejní ceny a slevy na prodejních položkách jsou založeny na kombinaci položky a zákazníka, můžete tuto konfiguraci provést také na stránce položky, kde se pravidla a hodnoty použijí.

> [!TIP]  
> Pokud by zboží nemělo být nikdy prodáváno se slevou, ponechte pole pro slevu na stránce položky prázdné a nezařazujte zboží do žádných nastavení řádkových slev.

## O cenících
Ceníky jsou flexibilní a umožňují určit obchodního partnera nebo činnost, na kterou se vztahují. Můžete například nastavit jeden ceník, který platí pro všechny dodavatele a zákazníky, nebo nabídnout speciální ceny či slevy pro každého obchodního partnera, třeba na základě minimálního množství v nákupních nebo prodejních objednávkách nebo určité kombinace zákazníka, zboží, minimálního množství, měrné jednotky nebo časového období. Vámi definované ceny a slevy se automaticky použijí na nákupní a prodejní doklady.

## Nastavení cen

Tyto kroky se liší podle toho, zda správce zapnul aktualizaci funkce **Nové prodejní ceny**.

#### [Aktuální zkušenosti](#tab/current-experience)

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Vyberte zákazníka a poté vyberte akci **Ceny**.
3. Vyplňte pole na řádku podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vyplňte řádek pro každou kombinaci, která zákazníkovi poskytne speciální prodejní cenu.

#### [Po novu](#tab/new-experience)
Zboží a služby můžete pro každý řádek přidat ručně nebo můžete pomocí akce **Navrhnout řádky** vytvořit nové ceny pro vybrané položky, slevové skupiny položek, zdroje a další typy produktů. Pokud zvolíte možnost **Navrhnout řádky**, můžete na stránce **Řádky cen - Vytvořit nové** pomocí filtrů vybrat položky nebo služby, které chcete do ceníku zahrnout. Můžete také určit, zda se má při výpočtu cen vzít v úvahu minimální množství, faktor úpravy, který se má použít pro nové řádky ceníku, a metoda zaokrouhlení, která se má použít pro ceny.

Ve výchozím nastavení je stav nových ceníků **Koncept**. Až budete připraveni začít seznam používat, můžete změnit stav na **Aktivní**.

Chcete-li si prohlédnout ceníky a ceny platné pro konkrétní zákazníky nebo dodavatele, vyberte na stránce **Zákazník** nebo **Dodavatel** akci **Prodejní ceny** nebo **Nákupní ceny**. U položek a zdrojů můžete zobrazit řádky ceníku výběrem **Prodejní ceny** nebo **Nákupní ceny** na stránkách **Zboží** a **Zdroj**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Vyberte zákazníka a poté zvolte akci **Prodejní ceníky**.
3. Chcete-li vytvořit nový prodejní ceník, zvolte **Nový**.
4. Na záložkáck **Obecné** a **Daň** vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Chcete-li přidat zboží do seznamu, proveďte jednu z následujících akcí:
   * Chcete-li přidat více položek, vyberte možnost **Navrhnout řádky** a poté zadejte kritéria filtru, abyste určili typy položek, které chcete přidat. Volitelně můžete také zadat některá další nastavení položek, která jsou specifická pro daný ceník. V případě potřeby je můžete později změnit.
   * Chcete-li zkopírovat položky z jiného ceníku, zvolte **Kopírovat řádky** a poté vyberte ceník, který chcete zkopírovat.
   * Chcete-li přidat položky ručně, vyberte v poli **Typ**, pro který je ceník určen. V závislosti na výběru vyplňte zbývající pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Chcete-li ceník začít používat, vyberte v poli **Stav** možnost **Aktivní**.

---

## Nastavení slevy na prodejní řádek pro zákazníka
Tyto kroky se liší podle toho, zda správce zapnul aktualizaci funkce **Nové prodejní ceny**.

#### [Aktuální zkušenosti](#tab/current-experience/)

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Otevřete příslušnou kartu zákazníka a poté zvolte akci **Řádkové slevy**.
3. Vyplňte pole na řádku podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vyplňte řádek pro každou kombinaci, která zákazníkovi poskytne slevu na prodejní řádek.

> [!Note]
> Při otevření stránek **Prodejní ceny** a **Prodejní řádkové slevy** od konkrétního zákazníka jsou pole **Filtr typu prodeje** a **Filtr kódu prodejního** nastavena pro daného zákazníka a nelze je změnit ani odstranit.
>
> Chcete-li nastavit ceny nebo řádkové slevy pro všechny zákazníky, cenovou skupinu zákazníků nebo kampaň, musíte otevřít stránky z karty položky. Alternativně můžete pro prodejní ceny použít stránku **Sešit prodejní ceny**. Další informace naleznete v tématu [Hromadná aktualizace cen zboží](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).

#### [Po novu](#tab/new-experience/)

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Vyberte zákazníka a poté zvolte akci **Prodejní ceníky**.
3. Otevřete ceník, pro který chcete zadat řádkovou slevu.
4. Zapněte přepínač **Povolit řádkovou slevu**.
5. Vytvořte nový řádek nebo vyberte existující řádek a vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. V poli **Definování** zvolte buď **Cena a sleva**, nebo pouze **Sleva**.
7. V poli **Řádková sleva %** zadejte procento slevy.

   > [!TIP]
   > Pokud upravujete existující řádek, můžete filtrovat řádky výběrem příslušné možnosti v poli **Zobrazit sloupce pro**.

---

## Práce s fakturační slevou a poplatky za služby
Při použití fakturačních slev určuje velikost poskytnuté slevy velikost fakturované částky. Na stránce **Fakturační slevy** můžete také přidat servisní poplatek k fakturám nad určitou částku.  <!--The Invoice Discounts page is hard to find.-->

Před použitím fakturačních slev s prodejem je nutné zadat určité informace do aplikace. Musíte se rozhodnout, kterým zákazníkům bude tento typ slevy poskytnut, a procenta slev, která použijete.

Pokud chcete, aby se fakturační slevy počítaly automaticky, můžete to zadat na stránce **Nastavení prodeje a pohledávek**.

U každého zákazníka můžete zadat, zda při splnění požadavku (tj. při dostatečně vysoké fakturované částce) poskytnete slevu na faktuře. Podmínky fakturační slevy můžete definovat v místní měně pro tuzemské zákazníky a v cizí měně pro zahraniční zákazníky.

Na stránce **Fakturační slevy** propojíte procenta slev s konkrétními částkami faktur. Můžete zadat tolik procent, kolik potřebujete. Každý zákazník může mít svou vlastní stránku nebo můžete propojit několik zákazníků se stejnou stránkou.

Kromě (nebo namísto) procenta slevy můžete propojit částku poplatku za službu s určitou částkou faktury.

> [!TIP]  
> Než začnete tyto informace zadávat, je dobré si předem připravit strukturu slev, aby bylo snazší zjistit, které zákazníky propojit se stejnou slevou na faktuře.< Další informace o prdejních slevách naleznete v tématu [Nastavení slev pro zákazníky](/learn/modules/customer-discounts-dynamics-365-business-central/index) na webu Microsoft Learn.

### Nastavení fakturační slevy pro zýkazníka
Poté, co se rozhodnete, kteří zákazníci mají nárok na fakturační slevy, zadejte kód fakturační slevy na kartách zákazníka a nastavte podmínky pro každý kód.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Otevřete stránku zákazníka pro zákazníka, který bude mít nárok na fakturační slevy.
3. Do pole **Kód fakturační slevy** vyberte kód pro příslušné podmínky fakturační slevy, které se mají použít k výpočtu fakturních slev pro zákazníka. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Kódy fakturačních slev jsou reprezentovány existujícími zákaznickými kartami. To vám umožní rychle přiřadit podmínky fakturační slevy zákazníkům výběrem jména jiného zákazníka, který bude mít stejné podmínky.

Pokračujte nastavením nových podmínek slevy prodejní faktury.

1. Na stránce **Zákazníci** zvolte akci **Fakturační slevy** . Stránka **Fakturační slevy zákazníka** se otevře.
2. Do pole **Kód měny** zadejte kód měny, na kterou se vztahují podmínky slevy na faktuře na řádku. Chcete-li nastavit podmínky fakturační slevy v USD, ponechte pole prázdné.
3. Do pole **Minimální částka** zadejte minimální částku, kterou musí mít faktura nárok na slevu.
4. Do pole **Procento slevy** zadejte fakturační slevu jako procento částky faktury.
5. Opakujte kroky 5 až 7 pro každou měnu, pro kterou zákazník obdrží jinou fakturační slevu.

Fakturační sleva je nyní nastavena a přiřazena k zákazníkovi. Když vyberete kód zákazníka v poli **Kód fakturační slevy** na jiných kartách zákazníka, je těmto zákazníkům přiřazena stejná fakturační sleva.

## Kopírování prodejních cen
Tyto kroky se liší podle toho, zda správce zapnul aktualizaci funkce **Nové prodejní ceny**.

#### [Aktuální zkušenosti](#tab/current-experience/)

Chcete-li kopírovat prodejní ceny, například prodejní ceny jednotlivých zákazníků, které chcete použít pro cenovou skupinu zákazníka, je nutné spustit dávkovou úlohu **Navrhnout cenu z ceny** v sešitu **Sešit prodejní ceny**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat<"), zvolte **Sešit prodejní ceny** a poté vyberte související odkaz.
2. Vyberte akci **Navrhnout cenu z ceny**.
3. V záložce **Prodejní ceny** vyplňte pole **Typ prodeje** a **Kód prodeje** původními prodejními cenami, které chcete zkopírovat.
4. V horní části stránky požadavku vyplňte pole **Typ prodeje** a **Kód prodeje** typem a názvem, do které chcete zkopírovat prodejní ceny.
5. Pokud chcete, aby dávková úloha vytvářela nové ceny, zaškrtněte políčko **Vytvořit nové ceny**.
6. Vyberte tlačítko **OK** pro vyplnění řádků na stránce **Sešitu prodejní ceny** navrhovanými cenami, které označují, že jsou platné pro vybraný typ prodeje.

   > [!NOTE]  
   > Tato dávková úloha vytváří pouze návrhy a neimplementuje navrhované změny. Pokud jste s návrhy spokojeni a chcete je implementovat, to znamená vložit je na stránku **Prodejní ceny**, zvolte akci **Provést změnu ceny** na stránce **Sešit prodejní ceny**.

#### [Po novu](#tab/new-experience/)

Stav ceníku musí být **Koncept**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat<"), zvolte **Sešit prodejní ceny** a poté vyberte související odkaz.
2. Vyberte ceník, který chcete zkopírovat, a poté zvolte **Kopírovat řádky**.
3. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Nemůžete mít dva řádky, které mají stejné nastavení, ale různé ceny. Pokud k tomu dojde, zobrazí se při aktivaci ceníku zpráva. Cenu, kterou chcete použít, můžete zvolit otevřením seznamu a odstraněním nesprávné ceny.

---

## Hromadná aktualizace cen zboží
Tyto kroky se liší podle toho, zda správce zapnul aktualizaci funkce **Nové prodejní ceny**.

#### [Aktuální zkušenosti](#tab/current-experience/)

Chcete-li hromadně aktualizovat ceny zboží, například zvýšit všechny ceny zboží o určité procento, je nutné spustit dávkovou úlohu **Navrhnout cenu ze zboží**. Odkaz na dávkovou úlohu najdete na stránce **Sešit prodejní ceny**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat<"), zvolte **Sešit prodejní ceny** a poté vyberte související odkaz.
2. Zvolte akci **Navrhnout cenu zboží**.
3. V záložce **Zboží** vyplňte pole **Číslo** nebo **Účto skupina zboží** nebo jiná pole s původními cenami zboží, které chcete aktualizovat.
4. V horní části stránky požadavku vyplňte **Typ prodeje** a **Kód prodeje** typem a názvem, do kterého chcete prodejní ceny zkopírovat.
5. Pokud chcete, aby dávková úloha automaticky zpravovala ceny navrhovaných položek, zadejte úpravu do pole **Faktor úpravy**. Například pokud zadáte 1,15 do **faktoru úpravy** pro 15% zvýšení ceny zboží.
6. Pokud chcete, aby dávková úloha vytvořila nové ceny, vyberte pole **Vytvořit nové ceny**.
7. Vyberte tlačítko **OK** pro vyplnění řádků na stránce **Sešitu prodejní ceny** navrhovanými cenami, které označují, že jsou platné pro vybrané **Zboží**

> [!NOTE]
> Tato dávková úloha vytváří pouze návrhy a neimplementuje navrhované změny. Pokud jste s návrhy spokojeni a chcete je implementovat, to znamená vložit je do tabulky **Prodejní ceny**, můžete použít dávkovou úlohu **Provést změnu ceny**, která se nachází na ve skupině **Akce** v záložce **Funkce** na stránce **Sešit prodejní ceny**.

#### [Po novu](#tab/new-experience/)

Chcete-li aktualizovat ceny pro více položek, je nutné vytvořit nový ceník a potom zkopírovat řádky z existujícího ceníku. Při kopírování řádků můžete pomocí filtrů určit, co se má kopírovat, a v poli **Faktor úpravy** můžete zadat celé číslo nebo desetinné číslo pro zvýšení nebo snížení cen. Ceník musí být ve stavu **Koncept.**. V případě potřeby můžete starý ceník deaktivovat.

> [!NOTE]
> Nemůžete mít dva řádky, které mají stejné nastavení, ale různé ceny. Pokud k tomu dojde, zobrazí se při aktivaci ceníku zpráva. Cenu, kterou chcete použít, můžete zvolit otevřením seznamu a odstraněním nesprávné ceny.

---

## Výpočet nejlepší ceny
Pokud jste zaznamenali speciální ceny a řádkové slevy pro prodej a nákup, [!INCLUDE[d365fin](includes/d365fin_md.md)] zajistí, že váš zisk z obchodu se zbožím bude vždy optimální, protože automaticky vypočítá nejlepší cenu na prodejních a nákupních dokladech a na řádcích deníku zakázek a položek. Pro více informací navštivte [Výpočet nejlepší ceny](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

## Viz také
[Nastavení prodeje](sales-setup-sales.md)  
[Prodej](sales-manage-sales.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
