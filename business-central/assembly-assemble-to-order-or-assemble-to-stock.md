---
    title: Understanding Assemble to Order and Assemble to Stock | Microsoft Docs
    description: Assembly items can be supplied either by assembling them when they are ordered or by assembling them to be kept in inventory until they are need on a sales order.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: kit, kitting
    ms.date: 04/01/2020
    ms.author: sgroespe

---
# Princip montáže na zakázku a montáže na sklad
Zboží montáže může být dodáno v následujících dvou procesech:

- Montáž na zakázku.
- Montáž na sklad.

## Montáž na zakázku
Obvykle používáte *montáž na zakázku* pro zboží, které nechcete skladovat, protože očekáváte, že je přizpůsobíte požadavkům zákazníků nebo protože chcete minimalizovat finanční pokrytí skl. nákladů. Mezi podpůrné funkce patří:

- Schopnost přizpůsobit zboží montáže při převzetí prodejní objednávky.
- Přehled dostupnosti zboží montáže a jejích komponent.
- Možnost okamžité rezervace komponent montáže pro zajištění splnění objednávky.
- Funkce pro určení ziskovosti přizpůsobené objednávky zpracováním ceny a nákladů.
- Integrace do skladu usnadňuje montáž a přepravu.
- Možnost montáže na zakázku v okamžiku vytvoření prodejní nabídky nebo hromadné prodejní objednávky.
- Schopnost kombinovat množství zásob s množstvím montáže na zakázku.

V procesu montáže na zakázku se zboží sestavuje jako odpověď na prodejní objednávku a s přímým spojením mezi montážní objednávkou a prodejní objednávkou.

Při zadávání zboží montáže na zakázku na prodejní řádek se automaticky vytvoří montážní zakázka s hlavičkou založenou na prodejním řádku a s řádky založenými na kusovníku montáže zboží vynásobeným množstvím objednávky. Na stránce **Řádky montáže na zakázku** můžete zobrazit propojené řádky montážní objednávky, které vás podporují při přizpůsobování zboží montáže, a datum dodání, které je založeno na informacích o dostupnosti komponent. Pro více informací navštivte [Prodej zboží montáže na zakázku](assembly-how-to-sell-items-assembled-to-order.md).

> [!NOTE]
> Ačkoli to není součástí výchozího procesu, můžete prodat množství zásob s množstvím montáže na zakázku. Pro více informací navštivte [Prodej skladového zboží podle montáže na zakázku](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Chcete-li tento proces povolit, musí být pole **Způsob montáže** na kartě zboží nastaveno na **Montáž-na-zakázku**.

## Montáž na sklad
Obvykle používáte *montáž na sklad* u zboží, které chcete sestavit před prodejem, například na přípravu na kampaň a skladovat na skladě, dokud toto zboží nebude objednáno. Toto zboží je obvykle standardní, jako jsou zabalené sady, které nenabízíte k přizpůsobení požadavkům zákazníků.

V procesu montáže na sklad je zboží sestaveno bez okamžité prodejní poptávky a je skladováno ve skladu jako skladová položka pro pozdější prodej nebo pro spotřebu jako polotovar. Pro více informací navštivte [Správa montáže](assembly-how-to-assemble-items.md). Od tohoto okamžiku je zboží vyskladněno a zpracováno jako jedno zboží a je považováno za dokončené výrobní zboží.

Když zadáte zboží montáže na sklad na prodejním řádku, zboží je považováno za jakékoli jiné zboží prodané ze skladu. Například dostupnost je kontrolována pouze pro zboží montáže.

> [!NOTE]
> Ačkoli to není součástí výchozího procesu, můžete sestavit zboží na objednávku, i když je nastavena na montáž na sklad. Pro více informací navštivte [Prodej zboží montáže na zakázku a skladového zboží dohromady](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

Chcete-li tento proces povolit, musí být pole **Způsob montáže** na kartě zboží nastaveno na hodnotu **Montáž-na-sklad**.

## Kombinované scénáře
Obecným principem v montážním managementu je to, že při kombinaci na řádku prodejní objednávky musí být množství montáže na zakázku dodáno před množstvím zásob.

Pokud je montážní zakázka propojena s řádkem prodejní objednávky, pak se hodnota v poli **Mn. k montáži na zakázku** na řádku prodejní objednávky zkopíruje do pole **Množství k montáži** prostřednictvím pole **Množství** v záhlaví montážní zakázky. Pro více informací navštivte [Prodej zboží montáže na obejdnávku](assembly-how-to-sell-items-assembled-to-order.md).

Kromě toho se hodnota v poli **Množství k montáži** vztahuje k  poli **K  dodání** na řádku prodejní objednávky a tento vztah řídí přepravu množství montáže na zakázku, a to jak částečně, tak úplně. To platí jak při montáži celého množství prodejního řádku na zakázku, tak v kombinovaných scénářích, kdy je jedna část množství prodejního řádku sestavena na zakázku a další díl je dodáván ze skladu. V kombinovaném scénáři však máte větší flexibilitu při částečném dodání v tom, že můžete upravit pole **Množství k montáži** v rámci předdefinovaných pravidel, abyste určili, kolik jednotek se má částečně dodat ze skladu a kolik částečně dodat montáží na zakázku.

Pokud musí být celé množství prodejního řádku sestaveno na objednávku a dodáno, pak se hodnota v poli **K  dodání** zkopíruje do pole **Množství k montáži** v propojené montážní zakázke, když změníte množství k dodání. Tím je zajištěno, že expedované množství je plně dodáno množstvím montáže na zakázku.

V kombinovaných scénářích není však plná hodnota v poli **K  dodání** zkopírována do pole **Množství k montáži** v záhlaví montážní zakázky. Místo toho je do pole **Množství k montáži** vložena výchozí hodnota, která je vypočtena z pole **K  dodání** podle předdefinovaného pravidla, které zajišťuje, že nejprve se přepravuje množství montáže na zakázku.

Pokud se chcete odchýlit od tohoto výchozího nastavení, například proto, že chcete sestavit pouze více či méně množství v poli **K  dodání**, pak můžete upravit pole **Množství k montáži**, ale pouze v rámci předdefinovaných pravidel, jak je znázorněno níže.

Příkladem, proč byste chtěli upravit množství, které chcete sestavit, je to, že chcete částečně odeslat dodávku množství zásob, než bude možné odeslat výstup montáže.

Následující text vysvětluje pravidla, která definují minimální a maximální hodnoty, které můžete ručně zadat do pole **Množství k montáži** a odchýlit se od výchozí hodnoty v kombinovaném scénáři. Tabulka ukazuje kombinovaný scénář, kde se pole **K  dodání** na propojeném řádku prodejní objednávky změnilo ze 7 na 4, a proto je výchozí hodnota pole **Množství k montáži** nastavena na 4.

||Řádek prod.objednávky|Hlavička montážní zakázky|
|-|----------------------|---------------------------|
||**Množství**|**K  dodání**|**Mn.  k montáži na zakázku**|**Dodané množství**|**Množství**|**Množství k montáži**|**Smontované možství**|**Zůstatek (množství)**|
|Počáteční|10|7|7|0|7|7|0|7|
|Změna||4||||4 (vložené ve výchozím nastavení)|||

Na základě výše uvedené situace můžete pole **Množství k montáži** upravit pouze následovně:

- Minimální množství, které můžete zadat, je 1. Důvodem je to, že k tomu, abyste mohli tyto čtyři jednotky prodat, musíte sestavit alespoň jednu jednotku za předpokladu, že zbývající tři jednotky jsou k dispozici ve skladu.
- Maximální množství, které můžete zadat, je 4. Tím je zajištěno, že nesestavujete více tohoto zboží montáže na zakázku, než co je potřeba k prodeji.

## Viz také
[Správa montáže](assembly-assemble-items.md)  
[Práce s kusovníky](inventory-how-work-BOMs.md)  
[Zásoby](inventory-manage-inventory.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
