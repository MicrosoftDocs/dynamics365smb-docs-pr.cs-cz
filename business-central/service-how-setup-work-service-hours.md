---
    title: How to Set Up Work Hours and Service Hours
    description: Learn how to set up the work and service hours used to calculate the response date and time for service orders and quotes.
    author: SorenGP

    
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 06/23/2021
    ms.author: edupont

---
# Nastavení Pracovní doby a Servisních hodin
Systém správy servisu obvykle sleduje hodiny prostředků a stav servisní zakázky, aby bylo možné předpovídat úlohy a potřeby servisu. [!INCLUDE[prod_short](includes/prod_short.md)] má vestavěné nástroje, které můžete přizpůsobit pro záznam tohoto druhu informací.

Po nastavení výchozích servisních hodin vaší společnosti můžete vypočítat doby odezvy servisních zakázek nebo odeslat upozornění nebo výstrahy při příchozích servisních voláních. Funkce výstrahy je implementována společně s plánovačem úloh.

Při práci na servisní zakázce budete chtít aktualizovat její stav, abyste mohli sledovat průběh. Stav servisní zakázky odráží stav opravy všech předmětů servisu v servisní zakázce. Pro více informací navštivte [Pochopení Servisních zakázek a stavu opravy](service-order-repair-status.md).

## Nastavení Výchozích servisních hodin
Stránka **Výchozí servisní hodiny** slouží k nastavení obvyklé servisní doby ve vaší společnosti. Tyto servisní hodiny se používají k výpočtu data a času odezvy pro servisní zakázky a nabídky a k odeslání upozornění na dobu odezvy. Výchozí servisní hodiny se používají pro servisní smlouvy, pokud pro smlouvu nezadáte zvláštní servisní hodiny.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Výchozí servisní hodiny** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!IMPORTANT]  
> Pokud necháte řádky na stránce **Výchozí servisní hodiny** prázdné, bude výchozí hodnota 24 hodin platná pouze pro kalendářní pracovní dny.

## Nastavení šablon pracovní doby
Stránku **Šablona pracovní doby** můžete použít k nastavení šablon, které obsahují typickou pracovní dobu ve vaší společnosti. Můžete například vytvořit šablony pro techniky na plný a částečný úvazek. Šablony pracovní doby můžete použít při přidávání kapacity ke zdrojům.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony pracovní doby** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!Note]
> Po zadání pracovní doby pro každý den se automaticky vypočítá hodnota v poli **Celkem za týden**.

## Nastavení specifických servisních hodin dle smlouvy
Na stránce **Servisní hodiny** můžete nastavit konkrétní servisní hodiny pro odběratele, který vlastní servisní smlouvu. Servisní hodiny se používají k výpočtu data a času odezvy pro servisní zakázky a nabídky, které patří do servisní smlouvy.

Pokud pro servisní smlouvu nenastavíte konkrétní servisní hodiny, použijí se výchozí servisní hodiny pro servisní smlouvy.

1. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Servisní smlouvy** a poté vyberte související odkaz.
2. Otevřete servisní smlouvu, pro kterou chcete nastavit konkrétní servisní hodiny, a zvolte **Servisní hodiny**.
4. Chcete-li nastavit servisní hodiny na základě výchozích servisních hodin, vyberte akci **Kopírovat výchozí servisní hodiny**.
5. Upravte pole v položkách servisních hodin. Vložení nebo odstranění položek pro nastavení servisních hodin pro smlouvu. Všimněte si, že pole **Den**, **Počáteční čas** a **Koncový čas** jsou povinná pro každý řádek.
6. Pokud chcete, aby servisní hodiny byly platné od určitého data, vyplňte pole **Počáteční datum**.
7. Pokud chcete, aby servisní hodiny byly platné o svátcích, zaškrtněte políčko v poli **Platné o svátcích**.

## Viz také
[Pochopení přidělení stavu a stavu opravy](service-allocation-status-and-repair-status.md)  
[Nastavení správy servisu](service-setup-service.md)  
[Pochopení servisních zakázek a Stavu opravy](service-order-repair-status.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]