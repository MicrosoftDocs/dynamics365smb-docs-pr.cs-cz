---
    title: How to Combine Receipts | Microsoft Docs
    description: If you want to invoice more than one purchase receipt at a time, you can use the Combine Receipts function.
    services: project-madeira
    documentationcenter: ''
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
# Kombinace příjmů na jedné faktuře
Pokud chcete fakturovat více než jednu nákupní příjemku současně, můžete použít funkci **Kombinace příjmů**.

Než budete moci vytvořit kombinovanou nákupní příjemku, musíte zaúčtovat více než jeden doklad od stejného dodavatele ve stejné měně. Jinými slovy, musíte vyplnit dvě nebo více nákupních objednávek a zaúčtovat je jako přijaté, ale nefakturované.

Když jsou doklady o nákupu sloučeny do faktury a zaúčtovány, vytvoří se pro fakturované řádky zaúčtovaná nákupní faktura. Pole **Fakturované množství** v původní objednávce nebo v hromadní nákupní objednávce se aktualizuje na základě fakturovaného množství. Tento původní nákupní doklad se však neodstraní, a to ani v případě, že byl zcela přijat a fakturován, a proto je nutné jej odstranit.

## Kombinace příjmů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktury** a poté vyberte související odkaz.
2. Vyberte akci **Nový**. Pro více informací navštivte [Záznam nákupu](purchasing-how-record-purchases.md).
3. Na záložce **Řádky** vyberte akci **Kopie řádků příjemky**.
4. Vyberte více řádků příjmů, které chcete zahrnout do faktury.

   Pokud byl vybrán nesprávný řádek příjmu nebo chcete začít znovu, stačí vymazat řádky na nákupní faktuře a poté znovu použít funkci **Kopie řádků příjemky**.
5. Chcete-li fakturu zaúčtovat, vyberte akci **Účtovat**.

## Odebrání otevřených nákupních objednávek po kombinovaném zaúčtování příjmu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Odstranit fakt. nák. objednávky** a poté vyberte související odkaz.
2. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Vyberte tlačítko **OK**.

Případně můžete jednotlivé objednávky odstranit ručně.

Opakujte kroky 1 až 3 pro všechny ostatní ovlivněné doklady, například hromadné nákupní objednávky.

## Viz také
[Nákup](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
