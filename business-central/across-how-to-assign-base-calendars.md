---
    title: How to Set Up Base Calendars | Microsoft Docs
    description: You can assign a base calendar to your company and its business partners, such as customers, vendors, or locations. Delivery and receipt dates on future sales order, purchase order, transfer order, and production order lines are calculated according to the calendar’s specified working days.
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
# Nastavení základních kalendářů
Společnosti a jejím obchodním partnerům, jako jsou zákazníci, dodavatelé nebo lokace, můžete přiřadit základní kalendář. Data dodání a příjmu na budoucí prodejní objednávce, nákupní objednávce, objednávce transferu a řádcích výrobní zakázky se počítají podle určených pracovních dnů kalendáře. Hlavním úkolem při nastavování nového základního kalendáře je určení a definování nepracovních dnů, které chcete použít.

## Nastavení základního kalendáře
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Základní kalendáře** a poté vyberte související odkaz.
2. Zvolte tlačítko **Nový**.
3. Vyplňte pole **Kód** field.
4. Choose the **Maintain Base Calendar Changes** action.
5. Na stránce **Změny základního kalendáře**, použijte **Systém periody** k označení určitého data nebo den opakující se jako nepracovní den. Můžete si vybrat mezi **Roční periodou** nebo **Týdenní periodou**.

   Pokud vyberete **Roční opakování**, musíte také zadat příslušné datum do pole **Datum**.

   Pokud vyberete **Týdenní opakování**, musíte také vybrat příslušný den v týdnu v poli **Den**. Pokud pole ponecháte prázdné, musíte vyplnit pole **Datum** . Pole **Den** je vyplněno automaticky.

Po vytoření položky je vybráno pole **Nepracovní**. Můžete se rozhodnout zrušit zaškrtnutí, aby se z něj stal pracovní den.  
Když se vrátíte na kartu základního kalendáře, zjistíte, že provedené záznamy nepracovního dne byly aktualizovány. Tyto položky se nyní zobrazují červeně a je vybráno pole **Nefungující**.

> [!NOTE]  
> Při nastavování nového základního kalendáře můžete vybírat a kopírovat řádky z existujícího kalendáře. To můžete provést na příslušné stránce **Změny základního kalendáře**.

> [!IMPORTANT]  
> Jakýkoli základní kalendář definovaný pro dodavatele nebo lokaci ovlivňuje způsob výpočtu dat a zaokrouhlování na pracovní dny.
> Určuje vzorec data pro čas potřebný k doplnění zboží. Používá se k výpočtu **Plánované datum příjmu**, pokud počítáte dopředu a pole **Datum objednávky**, pokud počítáte zpětně. Viz [Výpočet průběžné doby](across-how-to-assign-base-calendars.md#lead-time-calculation).

## Výpočet průběžné doby
Jakýkoli základní kalendář definovaný pro dodavatele nebo místo ovlivňuje způsob výpočtu dat a zaokrouhlování na pracovní dny. Proto jsou dvě pole data na řádcích nákupní objednávky vypočtena následujícím způsobem za různých podmínek.

| Směr výpočtu | Kalendář dodavatele definován | Kalendář dodavatele není definován |
|---------------------|-----------------------|---------------------------|
| Dopředu | plánované datum přijetí = datum objednávky + dodací lhůta dodavatele (podle kalendáře dodavatele a zaokrouhleno na další pracovní den nejprve v kalendáři dodavatele a poté v kalendáři lokace) | plánované datum přijetí = datum objednávky + dodací lhůta dodavatele (podle místního kalendáře) |
| Zpětně | datum objednávky = plánované datum přijetí - dodací lhůta dodavatele (podle kalendáře dodavatele a zaokrouhlena na předchozí pracovní den nejprve v kalendáři dodavatele a poté v kalendáři lokace) | datum objednávky = plánované datum přijetí - dodací lhůta dodavatele (podle místního kalendáře) |

> [!NOTE]
> Kromě výpočtu dodací lhůty, která ovlivňuje plánované datum přijetí a datum objednávky, jak je uvedeno ve výše uvedené tabulce, mohou být do vzorců přidány časy manipulace se skladem a bezpečnostní dodací čas, aby se hodnota v  **Plánované dotum příjmu** takto : Plánované datum příjmu + Bezpečná průběžná doba + doba zaskladnění = očekávané datum příjmu.

> [!Important]
> Pokud vaše lokace používá výrazně odlišný kalendář než vaši dodavatelé, je důležité pro tyto dodavatele nastavit konkrétní kalendáře, abyste mohli vypočítat optimální dodací lhůty dodavatele. Další informace o nastavení kalendářů dodavatelů naleznete v [Přiřazení základního kalendáře](across-how-to-assign-base-calendars.md#to-assign-a-base-calendar).

Obsah pole **Výpočet průběžné doby** je zkopírován z karty zboží nebo z karty skladového zboží, pokud je pro zboží definována průběžná doba nebo na stránce **Katalog zboží dodavatele** pokud je průběžná doba definována pro dodavatele.

## Přizpůsobení kalendáře
Hlavním úkolem při přizpůsobení základního kalendáře pro vaši společnost nebo jednoho z jejích obchodních partnerů je zadání změn stavu pracovního a nepracovního dne.

Zatímco například základní kalendář obvykle uvádí všechny soboty jako nepracovní dny, přizpůsobený kalendář pro určité umístění může uvádět všechny soboty v měsících listopadu a prosinci, které se zadjí být jako prázninové, tak mohou být jako pracovní dny.

Následující postup používá případ lokace jako příklad. Všimněte si, že v tomto okamžiku jste již k lokaci přiřadili základní kalendář.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Lokace** a poté vyberte související odkaz.
2. Otevřete kartu lokace, které chcete aktualizovat, a poté vyberte pole **Upravený kalendář**. V poli **Kód základního kalendáře** musí být vybrán kalendář.
3. Na stránce se otevřou **Položky upraveného kalendáře**, vyberte **Udržovat změny upraveného kalendáře** action.
4. V **Uživatelské změny kalendáře** přidejte řádek upravených položek kalendáře.

   Když zadáte řádek, je zaškrtnuto políčko **Nepracovní**. Pokud chcete změnit stav na pracovní den, můžete toto políčko zrušit.

   Můžete použít pote **Systém periody** k nastavení určitého data nebo dne jako opakovaného nepracovního dne. Můžete vybrat možnost **Roční opakování** nebo **Týdenní opakování**.

   Pokud vyberete **Roční opakování**, musíte také zadat příslušné datum do pole **Datum**. Pokud vyberete **Týdenní opakování**, musíte také vybrat příslušný den v týdnu v poli **Den**. Pokud pole necháte prázdné, musíte vyplnit pole **Datum**. Pole **Den** je poté vyplněno automaticky. To může být užitečné, pokud chcete označit jednotlivé datum jako nepracovní nebo pracovní den.

5. Vyberte tlačítko **OK**.

Na stránce **Položky upraveného kalendáře** zjistíte, že položky data jsou aktualizovány provedenými změnami.

Na kartě zboží zjistíte, že pole **Upravený kalendář** obsahuje **Ano**, což znamená, že byl nastaven vlastní kalendář.

> [!Important]
> Pokud nevyplníte na řádku objednávky **Kód lokace**je použit kalendář Vaší společnosti.


Pokud nevyplníte pole **Kód přepravce** na řádku objednávky, je použit kalendář Vaší společnosti.

> [!NOTE]  
> Pokud provedete změny základního kalendáře, pro který existují přizpůsobené změny kalendáře, automaticky se aktualizují všechny existující přizpůsobené kalendáře.

## Přiřazení základního kalendáře
Následující postup ukáže příklad jak naplánovat datum dodání na řádcích prodejních objednávek pro určitého zákazníka.

Základní kalendáře jsou přiřazeny k vaší vlastní společnosti, zákazníkům, prodejcům, lokacím a přepravcům takto:

- Na kartě **Informace o společnosti** a **Zákazníka**, je základní kalendář umístěn na záložce **Dodávka**.
- Na kartě **Dodavatele**, je umístěn základní kalendář na záložce **Příjem**.
- Na kartě **Lokace**je základní kalendář umístěn na záložce **Sklad**.
- Na stránce **Přepravci** je základní kalendář umístěn na stránce **Služby přepravce**.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Zákazníci** a poté vyberte související odkaz.
2. Otevřete kartu **Zákazníka**, pro kterého chcete přiřadit základní kalendář.
3. Na záložce **Dodávka** v poli **Kód záklandího kalendáře**, vyberte základní kalendář, který chcete přiřadit.

> [!IMPORTANT]
> - Pokud společnosti nepřiřadíte základní kalendář, všechna data se počítají jako pracovní dny.
> - Pokud na řádku objednávky zadáte prázdné místo, všechna data se počítají jako pracovní dny.
> - Jakýkoli základní kalendář definovaný pro dodavatele nebo místo ovlivňuje způsob výpočtu dat a zaokrouhlování na pracovní dny.

> [!NOTE]  
> Předím než upravíte položky kalendáře, musíte nejdříve přiřadit základní kalendář společnosti.

## Viz také
[Nakupování](purchasing-manage-purchasing.md)  
[Výroba](production-manage-manufacturing.md)    
[Zásoby](inventory-manage-inventory.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
