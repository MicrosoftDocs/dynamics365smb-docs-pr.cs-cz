---
    title: Set Up Resource Allocation | Microsoft Docs
    description: Learn how the system can help ensure that you assign someone who has the skills required to provide a service.
    author: brentholtorf

    
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords: resource, skill, service, zones
    ms.date: 04/01/2021
    ms.author: bholtorf

---

# Nastavení přidělení zdrojů
Aby bylo zajištěno, že servisní úloha bude vykonána dobře, je důležité najít zdroj, který je kvalifikovaný pro požadovanou práci. [!INCLUDE[prod_short](includes/prod_short.md)] můžete nastavit tak, aby bylo snadné alokovat někoho, kdo má pro danou práci správnou odbornost. V [!INCLUDE[prod_short](includes/prod_short.md)], se toto nazývá _přidělení zdrojů_. Zdroje můžete přidělit na základě jejich odbornosti, dostupnosti nebo toho, zda jsou ve stejné zóně servisu jako má zákazník.

Chcete-li použít přidělení zdrojů, musíte nastavit:

* Odbornost potřebnou k opravě a údržbě předmětů servisu. Přiřadíte ji předmětům servisu a prostředkům.
* Geografické oblasti zvané zóny, které definujete pro svůj trh. Například Východní, Západní, Centrální a tak dále. Přiřadíte je zákazníkům a zdrojům.
* Zda se má zobrazovat odbornost a zóny zdrojů a zda se má zobrazit varování, pokud si někdo vybere nekvalifikovaný zdroj nebo zdroj, který není v zákaznické zóně.

## Nastavení odbornosti
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kódy odbornosti** a poté vyberte související odkaz.skli
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Přiřazení odbornosti předmětům servisu a zdrojům
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Předměty servisu** nebo **Zdroje** a vyberte související odkaz.
2. Otevřete kartu pro předmět servisu nebo zdroj a poté vyberte jednu z následujících možností:

   * U předmětů servisu zvolte **Odbornosti zdroje**.
   * U zdroje zvolte **Odbornost**.

## Nastavení zón
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zóny servisu** a poté vyberte související odkaz.
2. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Přiřazení zón zákazníkům a zdrojům
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi.](media/ui-search/search_small.png " Řekněte mi, co chcete udělat"), zadejte **Zákazník** nebo **Zdroje** a poté vyberte související odkaz.
2. Otevřete kartu pro předmět servisu nebo zdroj a poté vyberte jednu z následujících možností:

   * Pro zákazníky vyberte zónu v poli **Kód zóny servisu**.
   * Pro zdroje vyberte akci **Zóny servisu**.

## Určení, co se má zobrazit, když je vybrán zdroj
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nastavení správce servisu** a poté vyberte související odkaz.
2. V poli **Volba odbornosti zdroje** vyberte jednu z možností popsaných v následující tabulce.

   | **Možnost** | **Popis** |
   |------------|-------------|  
   | Zobrazen kód | Zobrazí pouze kód. |
   | Zobrazeno varování | Zobrazí informace a zobrazí varování, pokud zvolíte zdroj, který není kvalifikovaný. |
   | Nepoužito | Nezobrazuje tyto informace. |

## Aktualizace kapacity zdroje
Možná budete muset změnit kapacitu zdrojů.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Kapacita zdroje** a poté vyberte související odkaz.
2. Zvolte zdroj a poté zvolte akci **Nastavit kapacitu**.
3. Proveďte změny a poté zvolte **Aktualizovat kapacitu**.

## Chcete-li aktualizovat odbornost pro zboží, předměty servisu nebo skupiny předmětů servisu
Pokud chcete změnit kódy odbornosti přiřazené k položkám, například z **PC** na **PCS**, můžete tak učinit buď pro zboží, předmět servisu, nebo pro všechny předměty ve skupině předmětů servisu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Položky**, **Předmět servisu**, nebo **Skupiny předmětů servisu**,  a poté vyberte související odkaz.
2. Vyberte entitu, kterou chcete aktualizovat, a poté vyberte akci **Odbornosti zdroje**.
3. Na řádku s kódem, který chcete změnit, vyberte v poli **Kód odbornosti** příslušný kód odbornosti.
4. Pokud má položka přidružené předměty servisu, otevře se dialogové okno s následujícími dvěma možnostmi:

   * Změnit kódy odbornosti na vybranou hodnotu: Tuto možnost vyberte, pokud chcete nahradit starý kód odbornosti novým kódem u všech souvisejících servisních předmětů.
   * Smazat kódy odbornosti nebo aktualizovat jejich vztah: Tuto možnost vyberte, pokud chcete změnit kód odbornosti pouze u této položky. Kód odbornosti u souvisejících předmětů servisu bude znovu přiřazen, to znamená, že pole **Přiděleno od** bude aktualizováno.

## Viz také
[Nastavení Přidělení zdroje](service-how-to-allocate-resources.md)  
[Nastavení Pracovní doby a Servisních hodin](service-how-setup-work-service-hours.md)  
[Nastavení hlášení poruch](service-how-setup-fault-reporting.md)  
[Nastavení Kódů standardního servisu](service-how-setup-service-coding.md)




[!INCLUDE[footer-include](includes/footer-banner.md)]