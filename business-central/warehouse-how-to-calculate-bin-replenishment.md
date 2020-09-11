---
    title: How to Calculate Bin Replenishment | Microsoft Docs
    description: When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.
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
# Výpočet doplnění přihrádky
Pokud je lokace nastavena tak, aby používala řízené zaskladnění a vyskladnění, při zaskladnění příjmů se pak zohlední priority šablony zaskladnění pro lokaci. Priority zahrnují minimální a maximální množství obsahu přihrádky, které byly stanoveny pro konkrétní přihrádku a pořadí přihrádek. Pokud je tedy zboží přijímáno stálým tempem, budou při vyprázdnění nejpoužívanější přihrádky vyskladnění vyplněny.

Ale zásoby ne vždy dorazí do skladu postupně bez změny. Někdy je zboží nakupováno ve velkém množství, takže společnost může získat rabat nebo výrobní jednotka může vyrábět velké množství jedného zboží k dosažení nízkých jednotkových nákladů. Poté nebude zboží po určitou dobu znovu přijato do skladu a sklad musí pravidelně přesouvat zboží do vyskladňovacích přihrádek z objemných skladových prostor.

Může se také stát, že sklad očekává, že brzy dorazí nová skladová zásoba, a chce vyprázdnit objemný skladový prostor zboží před příchodem nového zboží.

Nakonec, pokud jste definovali přihrádky hromadného skladu pouze akcí přihrádky typu **Zaskladnění** to znamená, že typ přihrádky nemá vybranou akci **Vyskladnění**, musíte vždy ponechat vyskladněné přihrádky doplněny, protože přihrádky typu Zaskladnění nejsou navrženy pro vyskladnění zásob.

## Doplnění přihrádek vyskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit přesunu** a poté vyberte související odkaz.
2. Vyberte akci **Vypočítat doplnění přihrádky** chcete-li otevřít stránku dialogu sestavy.
3. Vyplňte stránku požadavku na dávkovou úlohu a omezte rozsah návrhů na doplnění, které budou vypočteny. Můžete se například zabývat určitým zbožím, zónami nebo přihrádky.
4. Vyberte tlačítko **OK**. Řádky jsou vytvářeny pro pohyby doplňování, které je třeba provádět podle pravidel stanovených pro přihrádky a obsah přihrádky, tedy zboží v přihrádkách.
5. Pokud chcete provést všechna navrhovaná doplňování, vyberte akci **Vytvořit přesun**. Zaměstnanci nyní mohou najít pokyny v položce nabídky **Přesuny**, provést je a zapsat.
6. Pokud chcete provést pouze některé pokyny, odstraňte méně důležité řádky a vytvořte přesun.

Při příštím výpočtu doplňování přihrádky budou návrhy, které jste smazali, znovu vytvořeny, pokud jsou v té době stále platné.

> [!NOTE]
> Pokud jsou u zboží splněny následující podmínky:
> - Zboží má datum vypršení platnosti a
> - Je vybráno pole **Vybrat na základě metody FEFO** na kartě lokace a
- Používáte funkci **Vypočítat doplnění přihrádky**

pak budou pole **Ze zóny** a **Z přihrádky** prázdná, protože algoritmus pro výpočet, odkud se má zboží přesouvat, se spustí, pouze když aktivujete funkci **Vytvořit přesun**.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Povolení vyskladnění pomocí FEFO](warehouse-picking-by-fefo.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
