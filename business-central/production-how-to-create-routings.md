---
    title: How to Create Routings | Microsoft Docs
    description: A routing holds master data that captures the process requirements of a given produced item. Once a production order is created for that item, its routing will govern the scheduling of operations as represented on the **Prod. Order Routing** page under the production order.
    services: project-madeira
    documentationcenter: ''
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2019
    ms.author: sgroespe

---
# Vytvoření TNG postupů
Výrobní společnosti používají rutiny k vizualizaci a řízení výrobního procesu.

TNG postup je základem plánování procesů, plánování kapacity, plánovaného přiřazení materiálových potřeb a výrobních dokladů.

Pokud jde o výrobní kusovníky, jsou TNG postupy přiřazeny k vyrobenému zboží. TNG postup obsahuje hlavní data, která zachycují procesní požadavky dané vyráběné zboží. Po vytvoření výrobní zakázky pro toto zboží bude TNG postup řídit plánování operací, jak je znázorněno na řádku **TNG postup  výrobní zakázky** na stránce výrobní zakázky.

Dříve než můžete TNG postup založit, musí být nastaveno následující:

- Karty zboží se vytvářejí pro nadřazené položky, které se podílejí na výrobě. Pro více informací navštivte [Evidence nového zboží](inventory-how-register-new-items.md).
- Jsou nastaveny výrobní zdroje. Pro více informací navštivte [Nastavení pracovních center a strojních center](production-how-to-set-up-work-and-machine-centers.md)

## Vytvoření TNG postupů
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **TNG postupy** a poté vyberte související odkaz.
2. Vyberte tlačítko **Nový**.
3. Vyplňte pole podle potřeby. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. V poli **Typ**, vyberte **Sériový** pro výpočet výrobního postupu podle hodnoty v poli **Číslo operace**.
Vyberte **Paralelní** pro výpočet operací podle hodnoty v poli **Číslo další operace**.
5. Chcete-li TNG postup upravit, nastavte **Stav** na **Nový** nebo **Ve vývoji** . Chcete-li jej aktivovat, nastavte pole **Stav** na **Certifikováno**.

   Pokračujte vyplněním řádků TNG postupu.
6. V poli **Číslo operace** zadejte číslo první operace, například **10** .
7. V poli **Typ** zadejte, jaký druh zdroje se používá, například **Pracovní centrum**.
8. V poli **Číslo** vyberte zdroj, který chcete použít, nebo jej zapište do pole.
9. V poli **Kód vazby TNG** zadejte kód pro připojení komponenty k určité operaci. Pro více informací navštivte [Vytvoření TNG vazeb](production-how-to-create-routings.md#to-create-routing-links).
10. V polích **Doba zpracování** a **Doba seřízení** zadejte časy potřebné k provedení operace.

    > [!NOTE]
    > Doba seřízení se počítá podle výrobní zakázky, zatímco doba zpracování se počítá pro vyrobenou položku.

11. V poli **Souběžná kapacita** určete, kolik jednotek vybraného zdroje se použije k provedení operace. Například dva lidé přidělení jedné balicí operaci zkrátí dobu běhu na polovinu.
12. Dále vyplňte řádky pro všechny operace, které se podílejí na výrobě daného zboží.
13. Chcete-li kopírovat řádky z existujícího TNG postupu, vyberte talčítko **Kopie TNG postupu**.
14. Certifikace TNG postupu.
15. Nyní můžete připojit nový TNG postup ke kartě daného zboží vyplněním pole **Číslo TNG postupu** . Pro více informací navštivte **Evidence nového zboží**.

> [!NOTE]
> Nezapomeňte také přepočítat standardní cenu zboží z karty **Zboží**: Vyberte tlačítko **Výroba**, vyberte **Výpočet  pevné pořizovací ceny** a poté vyberte tlačíkto **Všechny úrovně**.

## Vytvoření řádků TNG postupů
Můžete vytvořit řádky TNG postupu propojené s komponenty a určitými operacemi, aby se zachovala jejich relace i v případě, že je změněn výrobní kusovník nebo TNG postup. Zajišťuje také just-in-time vyprazdňování komponent, zejména při zahájení konkrétní propojené operace, nikoli při uvolnění celé výrobní zakázky. Pro více informací navštivte [Spotřeba komponent podle operace výstupu](production-how-to-flush-components-according-to-operation-output.md)

Další důležitou výhodou je, že propojené komponenty a operace jsou zobrazeny ve struktuře logického procesu, když použijete **Deník výroby** pro účtování výstupu a spotřeby.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **TNG postupy** a poté vyberte související odkaz.
2. Otevřete TNG postup obsahující operace, které chcete propojit.

   Zkontrolujte, zda je stav TNG postupu **Ve vývoji** .

3. Na příslušném řádku TNG postupu v poli **Kód vazby TNG** vyberte kód.
4. V případě potřeby pokračujte v přidávání různých kódů vazeb TNG postupu k jiným operacím v TNG postupu.

   > [!NOTE]
   > Neměli byste používat stejný kód vazby TNG postupu v různých operacích TNG postupu, protože je možné, nesprávně propojit komponentu se dvěma různými operacemi, poté bude spotřebováno dvakrát.
   > Je vhodné pojmenovat kód vazby TNG postupu po operaci, aby bylo zajištěno propojení TNG postupu specifické pro danou operaci.
   > 
5. Nastavte TNG postup na **Certifikováno**.

   Kódy vazeb TNG jsou nyní přiřazeny k operacím. Dále je nutné vytvořit skutečný odkaz přiřazením stejných kódů specifickým komponentám v příslušném kusovníku.

6. Otevřete **Kusovník** obsahující komponenty, které chcete propojit s výše uvedenými operacemi. Pro více informací navštivte [Vytvoření výrobního kusovníku](production-how-to-create-production-boms.md).
7. Zkontrolujte, zda je stav TNG postupu **Ve vývoji** .
8. Na příslušném řádku výrobního kusovníku v poli **Kód vazby TNG** vyberte kód, který jste právě přiřadili k příslušné operaci.
9. Pokračujte v přidávání kódů vazeb technologického postupu k jiným součástem podle jedinečných operací, ve kterých jsou použity.
10. Nastavte stav výrobního kusovníku na **Certifikovaný ** .

   > [!NOTE]
Pro povolení propojení vazby TNG na existujicí výrobní zakázku, musíte aktualizovat danou výrobní zakázku. Pro více informací navštivte [Vytvoření montážní zakázky](production-how-to-create-production-orders.md).

Vybrané komponenty budou nyní propojeny s vybranými operacemi, když vytvoříte nebo aktualizujete výrobní zakázku pomocí výrobního kusovníku a příslušného TNG postupu. to je vidět na stránce**Komponenty . výrobní zakázky** v rámci výrobní zakázky a zde můžete kdykoliv odebrat a přidat definované kódy vazeb TNG postupu.

## Přiřazení personálu, nástrojů a opatření kvality k TNG postupu.
Požadujete-li pracovníky s kvalifikací, speciálními znalostmi nebo speciálním oprávněním pro operaci, můžete tyto osoby přiřadit k operaci. Kromě toho můžete k operaci přiřadit nástroje a požadavky na kvalitu. Tento postup popisuje přiřazení zaměstnanců. Postup je podobný jako u jiných typů informací o operacích.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **TNG postupy** a poté vyberte související odkaz.
2. Otevřete příslušný TNG postup.
3. V záložce **Řádky** vyberte řádek, který chcete zpracovat, a pak zvolte tlačítko **Osoby** .
4. Vyplňte políčka na stránce **Osoby TNG postupu**.
5. Stisknutím tlačítka **OK** opustíte stránku. Zadané hodnoty se zkopírují a přiřadí se k operaci.

## Vytvoření nových verzí TNG postupu
Princip verze umožňuje spravovat několik verzí TNG postupu. Struktura verze TNG postupu odpovídá struktuře technologického postupu skládajícího se z hlavičky a z řádků verzovaného TNG postupu. Základní rozdíl je definován počátečním datem.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **TNG postupy** a poté vyberte související odkaz.
2. Vyberte TNG postup, který se má zkopírovat, a zvolte talčítko **Vereze**.
3. Na stránce **verze TNG postupu** zvolte tlačítko **Nový**.
4. Vyplňte pole podle potřeby.
5. Do pole **Kód verze** zadejte jedinečný identifikátor pro danou verzi. Je povolena jakákoli kombinace číslic a písmen.

   Nově vytvořené verzi se automaticky přiřadí stav **Nový** .
6. Chcete-li vytvořit řádky operace, vyberte první prázdný řádek a pak vyplňte pole **Číslo operace** podle posloupnosti operací.

   Řádky operací jsou seřazeny vzestupně podle čísel operací. Chcete-li provést změny později, doporučujeme vybrat odpovídající délku kroku. Pole **Číslo další operace** odkazuje na následující operaci. Číslo operace lze zadat přímo.

7. Po dokončení verze TNG postupu nastavte pole **Stav ** na **Certifikovaný** .

Časová platnost verze je určena políčkem **Počáteční datum**.

## Viz také
[Vytvoření výrobního kusobníku](production-how-to-create-production-boms.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Plánování](production-planning.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nakupování](purchasing-manage-purchasing.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
