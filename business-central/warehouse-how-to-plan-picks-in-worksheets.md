---
    title: How to Plan Picks in Worksheets | Microsoft Docs
    description: If your warehouse is set up to require both pick and shipment processing, the warehouse can choose to operate so that the lines on shipment documents are not automatically transformed into pick instructions, but are made available instead to the pick worksheet.
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
# Plánování v sešitech vyskladnění
Pokud je váš sklad nastaven tak, aby vyžadoval zpracování vyskladnění i dodávky, může sklad pracovat tak, aby řádky na dodací doklady nebyly automaticky transformovány na pokyny k vyskladnění, ale byly k dispozici místo toho v sešitu vyskladnění.

> [!NOTE]
> Pokud již byly vytvořeny pokyny pro vyskladnění a chcete je kombinovat do jedného pokynu vyskladnění, musíte jednotlivé vyskladnění odstranit. Řádky, které mají být vyskladněny, mohou být nyní uvedeny v přehledu.

V sešitu vyskladnění můžete nastavit seznamy vyskladnění pro zaměstnance, které minimalizují dobu, po kterou se zaměstnanec musí pohybovat kolem zboží pro vyskladnění. Existují pole, která obsahují informace o množství zboží, které je k dispozici v přihrádkách přeložení. To je užitečné v situacích přeložení k plánování pracovních přiřazení, protože aplikace vždy navrhne vyskladnění z přihrádky přeložení před jakoukoli jinou přihrádku, bez ohledu na měrnou jednotku. Řádky v sešitu mohou pocházet z několika původních dokladů a mohou být seřazeny podle zboží, čísla police, původního dokladu, data splatnosti nebo adresy dodání.

Pokud řadíte podle termínu splatnosti, můžete ze sešitu odstranit všechny řádky kromě těch, které vyžadují okamžitou pozornost. Méně naléhavé řádky nejsou jako takové odstraněny, ale pouze odeslány zpět do sešitu **Výběr vyskladnění**. Když vytvoříte vyskladnění pro řádky, které již byly seřazeny podle data splatnosti, můžete se rozhodnout přiřadit vyskladnění konkrétnímu zaměstnanci.

> [!NOTE]
> Vyskladnění ddávek ze skladu u zboží, které je spojeno s dodanou prodejní objednávkou, probíhá podle stejných kroků jako u pravidelných vyskladnění zboží k dodání, jak je popsáno v tomto tématu. Počet řádků vyskladnění pro množství, které má být dodáno, však může být vyšší, protože vybíráte komponenty, nikoli zboží montáže.
> Řádky vyskladnění jsou vytvořeny pro hodnotu v poli **Zůstatek (množství)** na řádcích montážní zakázky, která je spojena s řádkem prodejní objednávky, který je dodán. Tím zajistíte, že všechny komponenty jsou vyskladněny v jedné akci.
> Pro více informací navštivte “Princip montáže na zakázku v dodávce ze skladu”.
Obecné informace o vyskladněných komponentách pro montážní objednávky, včetně situací, kdy zboží montáže není splatné u prodejní dodávky, naleznete v tématu [Vyskladnění pro výrobu nebo montáž v rozšířených konfiguracích skladu](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## Plánování v sešitech vyskladnění
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešit vyskladnění** a poté vyberte související odkaz.
2. Vyberte akci **Kopie dokladů  skladu**.
3. Vyberte dodávky, pro které chcete připravit vyskladnění. Nyní můžete řádky do určité míry seřadit, ale řazení, které zde provedete, nebude provedeno do pokynu vyskladnění. Můžete také odstranit některé řádky, aby bylo možné zboží efektivněji vyskladnit. Pokud například existuje několik řádků se zbožím v přihrádkách přeložení, můžete vytvořit vyskladnění pro všechny řádky přidružené k těmto řádkům. Přeložené zboží bude dodáno spolu s ostatními položkami v dodávkách a přihrádky přeložení budou mít prostor pro další příchozí zboží.
4. Vyberte akci **Vytvořit vyskladnění** a vyplňte stránku požadavku **Vytvořit vyskladnění**. Řazení, které zde požadujete, uspořádá řádky vyskladnění, které vytvoříte. Můžete například vytvořit jedno vyskladnění pro každou zónu a seřadit řádky podle pořadí přihrádek v rámci každého vyskladnění.
5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vyskladnění** a poté vyberte související odkaz. Otevře se stránka **Vyskladnění**.
6. Přiřazení vyskladnění, které jste právě vytvořili, můžete nyní najít výběrem vyskladnění s nejvyšším číslem.
7. Ve vyskladnění můžete v případě potřeby změnit přiřazené ID uživatele a způsob řazení řádků.
8. Vyberte akci **Tisk** a vytiskněte pokyny k vyskladnění.
9. Po provedení vyskladnění zvolte akci **Zapsat**.

Pokud byly přihrádky očíslovány způsobem, který odráží fyzické rozložení skladu, řádky seřazené podle kódu přihrádky umožňují pracovníkovi vyskladnit několik dodávek v jednom kole. Pracovník vytáhne z každé přihrádky požadovaný počet zboží pro každý řádek dodávky a umístí je spolu s ostatním zbožím pro konkrétní dodávku. Pracovník může ušetřit spoustu času výběrem několika dodávek při jedné návštěvě přihrádky.

Další účinnou možností třídění je pořadí přihrádek, pokud je fyzické rozložení skladu více podle pořadí přihrádky než kódu přihrádky.

V sešitu vyskladnění můžete také řadit podle dodací adresy, což vám umožní nejprve sestavit a odeslat objednávky vzdáleným zákazníkům.

## Viz také
[Správa skladu](warehouse-manage-warehouse.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nastavení správy skladu](warehouse-setup-warehouse.md)  
[Správa montáže](assembly-assemble-items.md)  
[Design Details: Detaily návrhu: Správa skladu](design-details-warehouse-management.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
