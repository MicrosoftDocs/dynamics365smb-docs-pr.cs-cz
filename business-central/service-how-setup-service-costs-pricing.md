---
    title: Set Up Pricing and Costs for Services
    description: Learn how to use pricing features to set up and customize your application so that you apply and adjust pricing on service items, repairs and orders.
    author: SorenGP

    
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: service, cost, service order
    ms.date: 06/25/2021
    ms.author: edupont

---

# Nastavení Ceny a Dodatečných nákladů za servis
K nastavení a přizpůsobení aplikace můžete použít cenové funkce [!INCLUDE[prod_short](includes/prod_short.md)], abyste mohli aplikovat a upravovat ceny na servisu, oprav a objednávek. Taty ceny se pak snadno přenášejí do procesu fakturace.

Podle potřeby implementace můžete nastavit cenové skupiny a namapovat je na konkrétní časová období, zákazníky nebo měnu. V závislosti na smlouvách o poskytování služeb uzavřených se zákazníky můžete nastavit pevné, minimální nebo maximální ceny. Nakonec můžete při úpravě cen zobrazit a schválit změny před jejich zaúčtováním do hlavní knihy.

## Nastavení Cenových skupin servisu
Můžete nastavit skupiny obsahující položky služeb, na které se mají vztahovat stejné speciální ceny služeb. Skupiny cen služeb přiřadíte k předmětům servisu na řádcích servisu. Cenové skupiny servisu můžete také přiřadit ke skupinám předmětu servisu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat<"), zvolte **Cenové skupiny servisu** a poté vyberte související odkaz.
2. Vytvoření Cenové skupiny servisu
3. Vyplňte pole **Kód** a **Popis**.
4. Zvolte akci **Nastavení**.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!Tip]
> Pole **Typ úpravy** a **Částka** spolupracují a určují, zda se úprava týká pevné částky, nebo se použije pouze v případě, že celková cena služby překročí nebo je nižší než částka v poli **Částka**.

## Nastavení skupin úprav cen servisu
Můžete nastavit skupiny pro úpravu cen, abyste mohli upravit ceny předmětů servisu. Můžete například nastavit skupiny úprav cen, které upraví cenu dopravného nebo náhradních dílů.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat<"), zvolte **Skupina úpravy ceny servisu** a poté vyberte související odkaz.
2. Vytvořte novou skupinu úpravy ceny servisu
3. Vyplňte pole **Kód** a **Popis**.
4. Do pole **Typ** zadejte typ položky, kterou chcete upravit.

   * Chcete-li upravit pouze jednu konkrétní položku, zadejte číslo této položky do pole **Číslo**. Když toto pole necháte prázdné, vaše skupina úprav upraví všechny položky typu definovaného v poli **Typ**.
   * Chcete-li upravit ceny služeb související pouze s jednou konkrétní službou, vyplňte pole **Typ práce** Když toto pole necháte prázdné, bude ignorováno.

5. Do pole **Popis** zadejte krátký popis úpravy ceny servisu.
6. Chcete-li upravit ceny servisu související pouze s jednou konkrétní obecnou skupinou účtování produktů, vyplňte **Obecná účto  skupina zboží.** field.

> [!Tip]
> Můžete zvolit **Podrobnosti** a přidat další informace o skupině úprav. Můžete například určit, která položka patří do skupiny úpravy ceny služby a zda se jedná o položku, zdroj, skupinu zdrojů nebo poplatek za servis.

## Nastavení dodatečných nákladů na servis
Při práci se předměty servisu a servisními zakázkami může být nutné evidovat další náklady, například náklady na cesty do jednotlivých servisních zón nebo startovné. Při vytváření servisní zakázky můžete tyto náklady vložit a do zakázky se přidá řádek typu **náklady**. Pokud chcete náklady použít na všechny servisní zakázky, můžete nastavit výchozí náklady. Například pokud chcete vždy uplatnit počáteční poplatek.

### Nastavení servisních nákladů
1. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Náklady na servis** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### To specify a default cost for service orders
1. Vyberte ikonu ![Žárovky, která otevře ikonu Řekněte mi](media/ui-search/search_small.png "Řeknete mi, co chcete dělat"), zadejte **Nastavení servisu** a poté vyberte související odkaz.
2. V poli **Počáteční poplatek za servisní zakázku** vyberte příslušné náklady na služby.

## Viz také
[Nastavení správy servisu](service-setup-service.md)  
[Správa servisu](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]