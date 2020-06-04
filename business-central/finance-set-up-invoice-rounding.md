---
    title: Set Up Invoice Rounding | Microsoft Docs
    description: You can round invoice amounts when you create invoices. Additionally, local regulations or custom may require you to round in a specific way, for example, to an amount divisible by 0.05.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: bholtorf

---
# Nastavení zaokrouhlování faktur
Pokud potřebujete při vytváření faktur zaokrouhlit částky faktur, můžete použít funkci automatického zaokrouhlování. Při zaokrouhlování faktury se přidá další řádek se zaokrouhlovací částkou a zaúčtuje se s ostatními řádky faktury.

> [!NOTE]  
> Místní předpisy nebo místní zvyklosti mohou vyžadovat, aby byla faktura zaokrouhlena zvláštním způsobem, například na částku dělitelnou 0,05.

Chcete-li použít automatické zaokrouhlování faktur, musíte:

* Určete účty účetní osnovy, na které budou zaokrouhleny rozdíly.
* Nastavte pravidla pro zaokrouhlení faktur v lokální měně a v cizí měně.
* Aktivujte funkci.

> [!NOTE]  
> Kromě funkcí zaokrouhlování faktur můžete zaokrouhlit částky na fakturách pomocí funkce zaokrouhlení jednotkové ceny a funkce zaokrouhlování částky.

## Nastavení účtů hlavní knihy pro rozdíly zaokrouhlení faktur
Chcete-li použít funkci automatického zaokrouhlování faktur, musíte nastavit účet hlavní knihy nebo účty, na kterých budou zaúčtovány rozdíly zaokrouhlování. Než to budete moci provést, musíte nastavit DPH účto skupiny zboží. Pro více informací navštivte [Nastavení DPH](finance-setup-vat.md).

### Nastavení účtů hlavní knihy pro rozdíly zaokrouhlení faktur
1. Vyberte ikonu ![ Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Účetní osnova** a vyberte související odkaz.
2. Na stránce **Účtová osnova** nastavte účet a pojmenujte ho **Zaokrouhlování faktur** nebo nějak podobně. [!INCLUDE[d365fin](includes/d365fin_md.md)] bude používat název účtu jako text pro faktury, které jsou zaokrouhleny.
3. V závislosti na tom, zda používáte DPH nebo daň z obratu, v polích **DPH účto  skupina zboží** nebo **Účto skupina DPH**, vyberte pro zaokrouhlenou částku skupinu účtování. Možná budete chtít nastavit nový kód skupiny, který se použije pro zaokrouhlování faktur.
4. Nechte pole **Typ  obecného účtování**, a také **Daň.obch.účto skupina** nebo **DPH obchodní  účto skupina** prázdné. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->

Nyní můžete účet zaokrouhlování faktur přiřadit skupinám účtování na stránce **Účto skupiny dodavatele**.  <!-- Why only the vendor posting groups? -->

## Nastavení zaokrouhlení pro cizí a lokální měny
Před použitím funkce automatického zaokrouhlení faktury je nutné nastavit pravidla zaokrouhlení pro cizí a místní měny.

### Nastavení zaokrouhlování cizí měny
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Měny** a vyberte související odkaz.
2. Na stránce **Měny** vyberte cizí měnu a otevřete **Kartu měny** a poté vyplňte pole **Přesnost zaokrouhlování částky**, **Přesnost zaokrouhlování jednotkové ceny**, **Přesnost zaokrouhlení faktury** a **Typ zaokrouhlení faktur**.

### Nastavení zaokrouhlení lokální měny
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Nastavení financí** a vyberte související odkaz.
2. Na stránce **Nastavení financí** v záložce **Obecné** vyplňte pole **Přesnost  zaokrouhlení faktury** a **Typ  zaokrouhlení faktury**.

## Aktivace funkce zaokrouhlení faktur
Chcete-li zajistit automatické zaokrouhlení prodejních a nákupních faktur, je nutné zapnout funkci zaokrouhlení faktur. Zaokrouhlení faktur se zapíná samostatně pro prodejní a nákupní faktury.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png " Řekněte mi, co chcete dělat") zadejte **Nastavení prodeje a poheldávek** a vyberte související odkaz.
2. V záložce **Obecné** zaškrtněte políčko **Zaokrouhlení faktury**.

## Viz také
[Fakturace prodeje](sales-how-invoice-sales.md)  
[Evidence nákupů](purchasing-how-record-purchases.md)
