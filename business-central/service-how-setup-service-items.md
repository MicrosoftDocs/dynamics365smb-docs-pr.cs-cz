---
    title: Service Items and Service Item Components
    description: Learn about the things you must set up before you can use service items, including default values such as response time and service price group.
    author: SorenGP

    
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 06/25/2021
    ms.author: edupont

---
# Nastavení Předmětů servisu a Komponent předmětů servisu
Chcete-li pracovat s předměty servisu, je nutné nastavit následující

* Skupiny předmětu servisu
* Volitelný

## Nastavení Skupin předmětů servisu
Můžete nastavit skupiny předmětů, které spolu souvisejí z hlediska oprav a údržby. Můžete definovat výchozí hodnoty pro předměty servisu ve skupině předmětů servisu, jako je doba odezvy, procento slevy smlouvy a cenová skupina servisu. U položek ve skupině předmětů servisu můžete zvolit, zda mají být při prodeji automaticky evidovány jako předměty servisu.

Skupiny předmětů servisu přiřadíte k položkám na kartě **Zboží** a k předmětům servisu na kartě **Předměty servisu**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skupiny předmětů servisu** a poté vyberte související odkaz.
2. Vytvoření nové Skupiny předmětu servisu
3. Vyplňte pole **Kód** a **Popis**.
4. V poli **Výchozí % slevy smlouvy** zadejte výchozí procento smluvní slevy, které chcete, aby předměty servosu ve skupině měly.
5. V poli **Výchozí kód skupiny servisu** zadejte výchozí kód cenové skupiny servisu, který chcete, aby předměty servisu ve skupině měly.
6. V poli **Výchozí doba odezvy (hodiny)** zadejte výchozí dobu odezvy v hodinách, kterou mají mít předměty servisu ve skupině.
7. Pokud chcete předměty ve skupině při prodeji zaevidovat jako předměty servisu, vyberte pole **Vytvořit předmět servisu**.

## Nastavení součástí předmětů servisu
Předmět servisu se může skládat z několika součástí, které lze při servisu vyměnit za náhradní díly. Tyto součásti jsou nastaveny na stránce **Přehled komp.předmětu servisu**. Navíc, pokud chcete nastavit komponenty pro servisní položky, které jsou kusovníky, můžete zkopírovat položky kusovníku a vytvořit je jako součásti servisních položek.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Předměty servisu** a poté vyberte související odkaz.
2. Otevřete předmět servisu, pro který chcete nastavit komponenty.
3. Zvolte akci **Komponenty**. Otevře se stránka **Přehled komp.předmětu servisu**.
4. Přidejte novou komponentu.
5. V poli **Typ** zvolte **Předmět servisu**, pokud je komponenta sama o sobě evidovaným předmětem servisu. V opačném případě vyberte **Zboží**.
6. V poli **Číslo** vyberte zboží nebo předmět servisu, který je součástí předmětu servisu.

## Nastavení komponent předmětu servisu z kusovníku
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Předměty servisu** a poté vyberte související odkaz.
2. Otevřete předmět servisu, pro který chcete nastavit součásti z kusovníku.
3. Zvolte akci **Komponenty**. Otevře se stránka **Přehled komp.předmětu servisu**.
4. Vyberte akci **Kopírovat z kusovníku**.

   Pokud je položka, se kterou je předmět servisu propojen, kusovník, komponenty pro všechny položky v kusovníku jsou vytvořeny automatick

## Nastavení servisního regálu
Můžete nastavit servisní regály, které identifikují, kam ukládáte předměty servisu. Servisní regály přiřadíte předmětům servisu na stránkách **Servisní zákazka** a **Sešit předmětu servisu**.

1. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Police servisu** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby.

## Viz také
[Nastavení Kódů standardního servisu](service-how-setup-service-coding.md)   
[Řešení problémů s nastavením](service-how-setup-troubleshooting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]