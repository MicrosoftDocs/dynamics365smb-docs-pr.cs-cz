---
title: Assign Item Charges to Sales and Purchases| Microsoft Docs
description: 'If you want your inventory items to carry added costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing or selling items, you can use the Item Charges feature.'
services: project-madeira
documentationcenter: ''
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: transportation, added cost, landed cost
ms.date: 10/01/2020
ms.author: edupont

---
# Použití poplatku zboží k účtování dodatečných obchodních nákladů
Aby bylo zajištěno správné ocenění, musí vaše skladové zboží nést veškeré dodatečné náklady, jako je přeprava, fyzická manipulace, pojištění a doprava, které vám vzniknou při nákupu nebo prodeji zboží. U nákupů se vyložené náklady na nakoupené zboží skládají z nákupní ceny dodavatele a všech dodatečných přímých poplatků za zboží, které lze přiřadit k jednotlivým příjmům nebo dodávkám vratky. Pro prodej může být znalost nákladů na dopravu prodaných položek pro vaši společnost stejně důležitá jako znalost nákladů na vyložené položky.

Kromě zaznamenání přidaných nákladů do hodnoty zásob můžete použít funkci Poplatky za zboží pro následující:

- Určete náklady na vyložené zboží pro přesnější rozhodování o optimalizaci distribuční sítě.
- Pro účely analýzy rozdělte pořizovací cenu nebo jednotkovou cenu zboží.
- Zahrňte povolenky na nákup a prdej do jednotkové ceny.

Před přiřazením poplatků za zboží je nutné nastavit čísla poplatků za zboží pro různé typy poplatků za zboží, včetně nákladů na účty souvisejících s prodejem, nákupy a úpravami zásob. Číslo poplatku za zboží obsahuje kombinaciobecné účto skupiny zboží, daňové skupiny, DPH účto skupiny zboží a poplatku zboží. dyž zadáte číslo poplatku za zboží na nákupním nebo prodejním dokladu, příslušný účet se načte na základě nastavení čísla poplatku za zboží a informací v dokladu.

U nákupních i prodejních dokladů můžete poplatek za zboží přiřadit dvěma způsoby:
- V dokladu, kde je uvedeno zboží, ke kterému se poplatek za zboží vztahuje. To obvykle děláte pro doklady, které ještě nejsou plně zaúčtovány.
- Na samostatné faktuře propojením poplatku za zboží se zaúčtovanou příjemkou nebo dodávkou, kde je uvedeno zboží, ke kterému se poplatek za zboží vztahuje.

> K objednávkám, fakturám a dobropisům můžete přiřadit poplatky za zboží a to jak pro prodej, tak i pro nákup. Následující postupy popisují, jak pracovat s poplatky za zboží v nákupní faktuře. Kroky jsou podobné pro všechny ostatní nákupní a prodejní doklady.

## Příklad
Toto video ukazuje, jak zpracovat dodatečné náklady na dopravu v rámci nákladů zásob.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## Nastavení čísel poplatků za zboží
Čísla poplatků za zboží slouží k rozlišení mezi různými druhy poplatků za zboží, které se používají ve vaší společnosti.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Poplatky za zboží** a poté vyberte související odkaz.
2. Na stránce **Poplatky za zboží** vyberte tlačítko **Nový** k vytvoření nového řádku..
3. Podle potřeby vyplňte pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Přiřazení poplatku za zboží přímo k nákupní faktuře za zboží
Pokud znáte poplatek za zboží v době, kdy účtujete nákupní fakturu za zboží, postupujte podle tohoto postupu.

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte Mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Nákupní faktury** a poté vyberte související odkaz.
2. Vytvořte novou nákupní fakturu. Pro více informací navštivte [Zaznamenávání nákupu](purchasing-how-record-purchases.md).
3. Ujistěte se, že nákupní faktura má jeden nebo více řádků typu Zboží.
4. Na novém řádku do pole **Typ** vyberte **Poplatek (zboží)**.
5. Do pole **Množství** zadejte jednotky poplatku za zboží, který vám byl fakturován.
6. Do pole **Nákupní cena** zadejte částku poplatku za zboží.
7. Podle potřeby vyplňte zbývající pole. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   V následujících krocích provedete skutečné přiřazení. Dokud není poplatek za zboží plně přiřazen, hodnota v poli **Množství k přiřazení** je napsán červeně.
8. V záložce **Řádky** vyberte tlačítko **Přiřazení poplatku zboží**.

   Otevře se stránka **Přiřazení poplatku zboží** zobrazující jeden řádek pro každý řádek typu Zboží na nákupní faktuře. Chcete-li přiřadit poplatek za zboží k jednomu nebo více řádkům faktury, můžete použít funkci, která vám jej přiřadí nebo  můžete ručně vyplnit množství v poli **Množství k přiřazení**. Následující kroky popisují, jak používat funkci Navrhnout přiřazení poplatku za zboží.

9. Na stránce **Přiřazení poplatku zboží** zvolte tlačítko **Navrhnout přiřazení popl.zboží**.
10. Pokud existuje více než jeden řádek faktury typu Zboží, zvolte jednu ze čtyř možností rozdělení.

To je poplatek za zboží je plně přiřazen, hodnota v poli **Množství k přiřazení** na faktuře je nula.

Poplatek za zboží je nyní přiřazen k nákupní faktuře. Při zaúčtování příjmu nákupní faktury se hodnoty zásob zboží aktualizují o náklady na poplatek za zboží.

## Přiřazení poplatku za zboží ze samostatné faktury k nákupní faktuře za zboží
Pokud jste po zaúčtování původního nákupního dokladu obdrželi fakturu za poplatek za zboží, postupujte podle tohoto postupu.
1. Opakujte kroky 1 až 8 v [Přiřazení poplatku za zboží ze samostatné faktury k nákupní faktuře za zboží](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. Na stránce **Přiřazení poplatku zboží** vyberte tlačítko **Kopie řádků příjemky**.
3. Na stránce **Řádky nák. příjemky** vyberte zaúčtované nákupní doklady pro zboží, ke kterým chcete přiřadit poplatek za zboží a pak zvolte tlačítko **OK** button.
4. Vyberte tlačítko **Navrhnout přiřazení popl.zboží**.

Poplatek za zboží na samostatné nákupní faktuře je nyní přiřazen zboží na zaúčtované nákupní příjemce, čímž se aktualizuje hodnota zásob zboží s náklady na poplatek za zboží.

## Viz také
[Správa závazků](payables-manage-payables.md)  
[Zaznamenávání nákupu](purchasing-how-record-purchases.md)  
[fakturace prodeje](sales-how-invoice-sales.md)  
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]