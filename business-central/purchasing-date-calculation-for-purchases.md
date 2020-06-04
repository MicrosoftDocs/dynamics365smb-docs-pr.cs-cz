---
    title: Date Calculation for Purchases | Microsoft Docs
    description: The application automatically calculates the date on which you must order an item to have it in inventory on a certain date. This is the date on which you can expect items ordered on a particular date to be available for picking.
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
# Výpočet data pro nákupy
[!INCLUDE[d365fin](includes/d365fin_md.md)] automaticky vypočítá datum, kdy musíte objednat zboží, aby bylo v zásobě k určitému datu. Toto je datum, kdy můžete očekávat, že zboží objednané k určitému datu bude k dispozici pro vyskladnění.

Pokud v hlavičce nákupní objednávky zadáte požadované datum příjmu, je vypočtené datum objednávky, kdy musí být objednávka zadána, aby se mohlo přijmout zboží k datu, které jste požadovali. Poté se vypočítá datum, kdy je zboží k dispozici pro vyskladnění, a zadá se do pole **Očekávané datum příjmu**.

Pokud nezadáte požadované datum příjmu, bude datum objednávky na řádku použito jako výchozí bod pro výpočet data, kdy můžete očekávat přijetí zboží, a data, kdy je zboží k dispozici pro výdej.

## Výpočet s požadovaným datem příjmu
Pokud je na řádku nákupní objednávky požadované datum příjmu, použije se toto datum jako výchozí bod pro následující výpočty.

- Požadované datum příjmu - výpočet průběžné doby = datum objednávky
- Požadované datum příjmu + doba  zaskladnění + bezpečná průběžná doba = očekávané datum příjmu

Pokud jste v hlavičce nákupní objednávky zadali požadované datum příjmu, bude toto datum zkopírováno do odpovídajícího pole na všech řádcích. Toto datum můžete změnit na libovolném řádku nebo můžete datum na řádku odebrat.

> [!Note]
> Pokud je váš proces založen na zpětném výpočtu, například pokud k získání data objednávky použijete požadované datum přijetí, doporučujeme použít vzorce data, které mají pevné trvání, například „5D“ po dobu pěti dnů nebo "1T" po dobu jednoho týdne. Vzorce data bez pevných dob trvání, například "SH" pro aktuální týden nebo BM pro aktuální měsíc, mohou vést k nesprávným výpočtům data. Pro více informací o vzorcích data navštivte [Práce s daty a časy kalendáře](ui-enter-date-ranges.md).

## Výpočet bez požadovaného data dodání
Pokud zadáte řádek objednávky bez požadovaného data dodání, pole **Datum objednávky** na řádku se vyplní datem v poli **Datum objednávky** v hlavičce nákupní objednávky. Toto je buď datum, které jste zadali, nebo pracovní datum. Následující data jsou pak vypočtena pro řádek nákupní objednávky, přičemž počáteční bod je datum objednávky.

- Datum objednávky + výpočet průběžné doby = plánované datum příjmu
- Plánované datum příjmu + doba  zaskladnění + bezpečná průběžná doba = očekávané datum příjmu

Pokud změníte datum objednávky na řádku, například když zboží není k dispozici u dodavatele až do pozdějšího data, budou příslušná data na řádku automaticky přepočítána.

Pokud změníte datum objednávky v záhlaví, zkopíruje se toto datum do pole **Datum objednávky** na všech řádcích a všechna související data se pak přepočítají.

## Viz také
[Výpočet data pro prodej](sales-date-calculation-for-sales.md)  
[Výpočet data příslibu objednávek](sales-how-to-calculate-order-promising-dates.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
