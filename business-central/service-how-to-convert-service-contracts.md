---
    title: How to Convert Service Contracts | Microsoft Docs
    description: Because the VAT rate change tool cannot convert service contracts, these contracts must be converted manually. This topic describes several alternative methods that you can use for service contract conversion.
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
# Převod servisních smluv, které obsahují částky DPH
Vzhledem k tomu, že nástroj pro změnu sazby DPH nemůže převést servisní smlouvy, musí být tyto smlouvy převedeny ručně. Toto téma popisuje několik alternativních metod, které můžete použít pro převod servisní smlouvy.

> [!NOTE]
> Toto téma poskytuje pracovní postup na vysoké úrovni.

Následující postup popisuje, jak opravit fakturu za předplacenou servisní smlouvu, která byla vytvořena rok předem.

> [!NOTE]
> V tomto příkladu musíte změnit své pracovní datum na 01.01.2017.

### Oprava faktury za předplacenou servisní smlouvu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Správa smluv** a poté vyberte související odkaz.
2. V části **Seznamy** vyberte **Servisní smlouvy**.
3. Vytvořte novou předplacenou servisní smlouvu. Zadejte počáteční datum **01.01.2017** a rok fakturačního období pro zákazníka **20000**.
4. Chcete-li smlouvu podepsat, vyberte akci **Podepsat smlouvu**.
5. Vytvořte servisní fakturu.
6. Faktura je uvedena jako neuložená faktura za službu. Chcete-li zobrazit servisní fakturu, vyberte akci **Servis**, **Správa smluv** a poté vyberte akci **Faktura servisu**.
7. Zaúčtujte servisní fakturu.

> [!NOTE]
> Neměňte neodeslanou fakturu za služby. Protože jsou položky servisu vytvořeny při vytvoření faktury, změna v neodeslané faktuře nezmění již vytvořené položky servisu. Položky DPH jsou však vytvořeny při zaúčtování faktury. To vám umožní změnit obecnou skupinu účtování produktů a skupinu účtování produktů GSP na neodeslané servisní faktuře.

### Vytvoření dobropisu pro rozdíl DPH
Následující postup popisuje, jak vytvořit dobropis, který zahrnuje pouze rozdíl DPH za již fakturované období počínaje dnem **01.07.2017**. V tomto příkladu je částka DPH zaúčtována pouze do modulu Správa financí, nikoli do modulu Správa služeb. Položky DPH, které jsou spojeny s položkou servisu, nebudou opraveny.

1. Vytvořte nový účet hlavní knihy pro rozdíl v DPH. Tento účet bude použit pro přímé zaúčtování opravy DPH.
2. Přidejte nový řádek do nastavení účtování DPH.

### Vytvoření dat platnosti smlouvy na řádcích smlouvy
Následující postup popisuje, jak vytvořit nové smlouvy pomocí práce s daty platnosti smlouvy na řádcích servisní smlouvy.

1. Na stránce **Servisní smlouva** nastavte datum vypršení platnosti smlouvy na **30.06.2017**.
2. Vyberte akci **Vytvořit dobropis** a automaticky vytvořte dobropis za červenec 2017 až prosinec 2017.
3. Protože smlouva vypršela, musíte pro období od 1. července 2017 do 31. prosince 2017 vytvořit novou smlouvu s novou sazbou DPH.

### Vytvoření nového dobropisu
Následující postup popisuje, jak vytvořit nový dobropis pomocí dávkové úlohy **Získat položky zálohy smlouvy**. Položky, které nechcete opravit od ledna 2017 do června 2017, budou smazány.

1. Spusťte nástroj pro změnu sazby DPH 1. července 2017. Změní se obecná účto skupina zboží nebo DPH účto skupina zboží. Pro více informací navštivte [Práce s DPH z prodeje a nákupu](finance-work-with-vat.md).
2. Po spuštění nástroje pro změnu sazby DPH zadejte datum vypršení smlouvy pro servisní smlouvu. Nyní můžete odstranit servisní smlouvu a vytvořit novou, která je totožná se starou.
3. Vytvořte novou fakturu pro období od ledna 2017 do prosince 2012 pomocí nové sazby DPH.
4. Chcete-li vytvořit další dobropis, na stránce **Dobropisy servisu** vyberte akci **Nový** a vytvořte nový dobropis servisu.
5. Vyberte akci **Získat položky zálohy smlouvy**.
6. Po dokončení převodu budou položky DPH a servisu správné.

## Viz také
[Práce se servisními smlouvami a nabídkami servisních smluv](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[Finance](finance.md)  
[Ohlásit DPH finančnímu úřadu](finance-how-report-vat.md)  
[Práce s DPH z prodeje a nákupu](finance-work-with-vat.md)
