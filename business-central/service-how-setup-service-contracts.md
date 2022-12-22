---
    title: Set Up Service Contracts
    description: Learn how to set up service contracts with required prerequisites including service contract groups, contract templates and customer templates.
    author: SorenGP

    
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: service, cost, service order
    ms.date: 06/23/2021
    ms.author: edupont

---

# Založení Servisních smluv
Než budete moci pracovat se smlouvami, musíte nastavit následující:

* **Skupiny servisních smluv**, které shromažďují servisní smlouvy, které spolu nějakým způsobem souvisejí.
* **Skupiny účtů servisní smlouvy**, které se používají k seskupování účtů servisních smluv pro servisní faktury vytvořené pro servisní smlouvy. Tyto skupiny přiřadíte k servisním smlouvám.
* **Šablony smluv**, které definují rozvržení smluv obsahujících nejčastěji používané detaily servisní smlouvy. Když vytváříte nabídky servisních smluv, můžete je vytvořit pomocí šablon. Při vytváření nabídky smlouvy pole automaticky obsahují obsah polí šablony.
* **Šablony zákazníků**, které vám umožňují vytvářet nabídky pro smlouvy nebo pro potenciální zákazníky a zároveň nejsou evidování jako zákazníci v [!INCLUDE[prod_short](includes/prod_short.md)].

## Nastavení Skupiny servisních smluv
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny servisních smluv** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vyberte akci **Sleva pouze na zak. ze smlouvy** pokud chcete, aby smluvní nebo servisní slevy byly platné pouze pro objednávky servisní smlouvy, jako je údržba.

## Nastavení skupin účtů servisní smlouvy
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupina čtů servisní smlouvy**, a pak vyberte související odkaz.
2. Vytvořte novou skupinu účtů servisní smlouvy.
3. Vyplňte pole **Kód** a **Popis**. Tato pole popisují Skupinu servisních účtů.
4. Vyplňte pole **Účet smlouvy bez zálohy**, vyberte číslo účtu hlavní knihy pro účet bez zálohy.
5. V poli **Účet smlouvy se zálohou** vyberte číslo účtu hlavní knihy pro účet se zálohou.

## Nastavení šablony smlouvy
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony servisních smluv** a poté vyberte související odkaz.
2. Vytvořte novou šablonu servisní smlouvy.
3. Do pole **Číslo ** zadejte číslo šablony smlouvy.

   Alternativně, pokud jste nastavili číselné řady pro šablony smlouvy na stránce **Nastavení Správce servisu<f0>, stisknutím klávesy Enter zadejte další dostupné číslo šablony smlouvy. Vyplňte ostatní pole podle potřeby.

4. Na záložce **Faktura**, vyplňte pole **Kód skupiny účtů servisní smlouvy**, **Období fakturace** a tak dále. Vyplňte ostatní pole podle potřeby.
5. Zvolte akci **Servisní slevy** pro přidání smluvních slev.

## Nastavení šablony zákazníka
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Šablony zákazníka<x5/> a poté vyberte související odkaz.
2. Vytvořte novou kartu šablony zákazníka
3. V záložce **Obecné** s náhledem zadejte kód a popis pro šablonu zákazníka do polí **Kód** a **Popis**.
4. Chcete-li definovat vyhledávací kritéria, vyplňte další pole, například **Kód země/oblasti**, **Kód teritoria** a **Kód jazyka**.
5. Vyplňte pole **Obecná účto  Obch. účto skupina** a **Účto skupina zákazníka**.

## Viz také
[Nastavení správy servisu](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]