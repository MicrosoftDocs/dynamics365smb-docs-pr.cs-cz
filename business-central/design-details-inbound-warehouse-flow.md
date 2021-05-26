---
    title: Design Details - Inbound Warehouse Flow | Microsoft Docs
    description: The inbound flow in a warehouse begins when items arrive in the warehouse of the company location, either received from external sources or from another company location. An employee registers the items, typically by scanning a bar code. From the receiving dock, warehouse activities are performed at different complexity levels to bring the items into the storage area.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 04/01/2021
    ms.author: edupont

---
# Detaily návrhu: Vstupní procesy skladu
Vstupní procesy ve skladu začínají, když zboží dorazí do skladu v sídle společnosti, buď je přijaté z externích zdrojů, nebo z jiného sídla společnosti. Zaměstnanec zboží zaregistruje, obvykle naskenováním čárového kódu. Z přijímacího doku se skladové činnosti provádějí na různých úrovních složitosti, aby se zboží přeneslo do skladovací oblasti.

Každé zboží je identifikováno a spárováno s odpovídajícím vstupním zdrojovým dokladem. Existují následující vstupní zdrojové doklady:

- Nákupní objednávka
- Objednávka příchozího transferu
- Objednávka prodejní vratky

Kromě toho existují následující interní zdrojové doklady, které fungují jako vstupní zdroje:

- Účtování výrobní zakázka s výstupem
- Účtování montážní zakázky s výstupem

Poslední dva představují příchozí toky do skladu z interních provozních oblastí. Další informace o manipulaci se sklady pro interní příchozí a odchozí procesy najdete v [Detaily návrhu: Interní procesy skladu](design-details-internal-warehouse-flows.md).

Procesy a doklady uživatelského rozhraní v příchozích tocích skladu se liší pro základní a pokročilé konfigurace skladu. Hlavním rozdílem je, že aktivity jsou zpracovány po objednávkách v základních konfiguracích skladu a jsou konsolidovány pro více objednávek v pokročilých konfiguracích skladu. Další informace o různých úrovních složitosti skladu najdete v [Detaily návrhu: Přehled skladu](design-details-warehouse-setup.md).

V [!INCLUDE[prod_short](includes/prod_short.md)] příchozí procesy příjmu a zaskladnění lze provádět čtyřmi způsoby pomocí různých funkcí v závislosti na úrovni složitosti skladu.

| Metoda | Příchozí proces | Přihrádky | Příjmy | Vyskladnění | Úroveň složitosti (Viz [Detaily návrhu: Nastavení skladu](design-details-warehouse-setup.md)) |
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
| A | Zaúčtujte příjemku a zaskladněte zboží z řádku objednávky | X | | |2 |
| B | Zaúčtujte příjemku a zaskladněte zboží z dokladu zaskladnění zásob | | | X | 3 |
| C | Zaúčtujte příjemku a zaskladněte zboží z příjemky skladu | | X | | 4/5/6 |
| D | Zaúčtujte příjemku z příjemky skladu a zaskladnění z dokladu zaskladnění skladu | | X | X | 4/5/6 |

Výběr přístupu závisí na přijatých postupech společnosti a na úrovni jejich organizační složitosti. V prostředí skladu se spracováním zboží po objednávkách, kde většina zaměstnanců skladu pracuje přímo s doklady objednávky, se společnost může rozhodnout použít metodu A. U skladu spracování zboží po objednávkách, který má složitější proces zaskladnění nebo kde jsou vyhrazení zaměstnanci skladu k provádění skladových funkcí, se může firma rozhodnout oddělit své funkce zaskladnění od dokladu objednávky, metoda B. Pro společnosti, které potřebují naplánovat zpracování více objednávek, může být užitečné použít doklady příjemky skladu, metoda C a D.

V metodách A, B a C jsou akce příjmu a zaskladnění kombinovány v jednom kroku při zaúčtování odpovídajících dokladů jako přijatých. V metodě D je příjem zaúčtován jako první, aby bylo možné rozpoznat nárůst zásob a to, že zboží je k dispozici k prodeji. Pracovník skladu poté zaregistruje zaskladnění zboží, aby bylo dostupné pro vyskladnění.

## Základní konfigurace skladu
Následující diagram znázorňuje toky vstupního skladu podle typu dokladu v základních konfiguracích skladu. Čísla v diagramu odpovídají krokům v následujících částech diagramu.

![Příchozí tok v základních konfiguracích skladu](media/design_details_warehouse_management_inbound_basic_flow.png "Příchozí tok v základních konfiguracích skladu")

### 1: Vydání zdrojového dokladu / Vytvoření zaskladnění zásob
Když je zboží přijato ve skladu, uživatel, který je zodpovědný za příjem, vydá zdrojový doklad, například nákupní objednávku nebo vstupní objednávku transferu, aby signalizoval pracovníkům skladu, že přijaté zboží může být zaskladněné ve skladu. Alternativně uživatel vytvoří doklady zaskladnění zásob pro jednotlivé řádky objednávky nabízeným způsobem na základě zadaných přihrádek a množství, které je možné zpracovat.

### 2: Vytvoření vstupního požadavku
Po vydání vstupního zdrojového dokladu se automaticky vytvoří vstupní požadavek skladu. Obsahuje odkazy na typ a číslo zdrojového dokladu a není pro uživatele viditelný.

### 3: Vytvoření zaskladnění zásob
Na stránce **Zaskladnění zásob** pracovník skladu načte vyžádaně řádky čekajícího zdrojového dokladu na základě vstupního požadavku skladu. Případně jsou řádky zaskladnění zásob již vytvořeny způsobem Doručení bez vyžádání uživatelem, který je zodpovědný za zdrojový doklad.

### 4: Účtování zaskladnění zásob
Na každém řádku pro zboží, které bylo zaskladněno, částečně nebo úplně, pracovník skladu vyplní pole **Množství** a pak zaúčtuje zaskladnění zásob. Zdrojové doklady, které souvisejí se zaskladněním zásob, jsou zaúčtovány jako přijaté.

Vytvoří se kladné položky zbož a položky skladu a odstraní se požadavek na zaskladnění, pokud je plně zpracován. Například je aktualizováno pole **Přijaté množství** na řádku vstupního zdrojového dokladu. Vytvoří se zaúčtovaný doklad o přijetí, který odráží například nákupní objednávku a přijaté zboží.

## Pokročílé nastavení skladu
Následující diagram znázorňuje tok vstupního skladu podle typu dokladu v pokročilých konfiguracích skladu. Čísla v diagramu odpovídají krokům v následujících částech diagramu.

![Příchozí tok v pokročilých konfiguracích skladu](media/design_details_warehouse_management_inbound_advanced_flow.png "Příchozí tok v pokročilých konfiguracích skladu")

### 1: Vydání zdrojového dokladu
Když je zboží přijato ve skladu, uživatel, který je zodpovědný za příjem, vydá zdrojový doklad, například nákupní objednávku nebo vstupní objednávku transferu, aby signalizoval pracovníkům skladu, že přijaté zboží může být zaskladněné ve skladu.

### 2: Vytvoření vstupního požadavku
Po vydání vstupního zdrojového dokladu se automaticky vytvoří vstupní požadavek skladu. Obsahuje odkazy na typ a číslo zdrojového dokladu a není pro uživatele viditelný.

### 3: Vytvoření příjemky na sklad
Na stránce **Příjemka na sklad** uživatel, který je zodpovědný za příjem zboží, načte čekající řádky zdrojového dokladu na základě vstupního požadavku skladu. Několik řádků zdrojového dokladu lze kombinovat v jednom dokladu příjemky na sklad.

Uživatel vyplní pole **Množ. ke zpracování** a v případě potřeby vybere přijímací zónu a přihrádku.

### 4: Zaúčtování příjemky na sklad
Uživatel zaúčtuje příjemku na sklad. Vytvoří se kladné položky zboží. Například je aktualizováno pole **Přijaté množství** na řádku vstupního zdrojového dokladu.

### 5: Vytvoření interního zaskladnění skladu
Uživatel, který je zodpovědný za zaskladnění z interních operací, vytvoří interní zaskladnění skladu pro zboží, které musí být zaskladněno ve skladu, jako je výroba nebo výstup sestavy. Uživatel určuje množství, zónu a přihrádku, ze které má být zboží zaskladněno, případně to může udělat pomocí funkce **Načíst obsah přihrádky**. Uživatel vydá interní zaskladnění skladu, který vytvoří požadavek příchozího skladu, aby bylo možné úlohu načíst v dokladech zaskladnění skladu nebo v sešitu zaskladnění.

### 6: Vytvoření požadavku na zaskladnění
Při zaúčtování vstupního zdrojového dokladu je automaticky vytvořen požadavek na zaskladnění. Obsahuje odkazy na typ a číslo zdrojového dokladu a není pro uživatele viditelný. V závislosti na nastavení vytvoří výstup z výrobní zakázky také požadavek na zaskladnění dokončeného zboží do skladu.

### 7: Generování řádků sešitu zaskladnění (Volitelné)
Uživatel, který je zodpovědný za koordinaci zaskladnění, načte řádky zaskladnění skladu v **Sešitu zaskladnění** na základě zaúčtování příjemek na sklad nebo interních operací s výstupem. Uživatel vybere řádky, které mají být zaskladněny, a připraví zaskladnění určením, ze kterých přihrádek se má zboží vzít, do kterých přihrádek umístit a kolik jednotek má být spracováno. Přihrádky mohou být předdefinovány nastavením lokace skladu nebo provozního zdroje.

Když jsou všechny doklady zaskladnění naplánovány a přiřazeny pracovníkům skladu, uživatel vygeneruje doklady zaskladnění skladu. Plně přiřazené řádky zaskladnění jsou ze **Sešitu zaskladnění** odstraněny.

> [!NOTE]  
> Pokud na kartě lokace není vybráno pole **Použít sešit zaskladnění**, budou doklady zaskladnění skladu vytvořeny přímo na základě zaúčtovaných příjemek ze skladu. V takovém případě je krok 7 vynechán.

### 8: Vytvoření dokladu zaskladnění skladu
Pracovník skladu, který provádí zaskladnění, vytvoří doklad zaskladnění na základě zaúčtované příjemky na sklad. Alternativně je vytvořen doklad zaskladnění skladu, který je přiřazen skladníkovi formou Doručit bez vyžádání.

### 9: Zaregistrace zaskladnění skladu
Na každém řádku pro zboží, které bylo zaskladněno, částečně nebo úplně, pracovník skladu vyplní pole **Množství** na stránce **Zaskladnění** a poté zaregistruje zaskladněné zboží.

Jsou vytvořeny položky skladu a řádky zaskladnění skladu jsou odstraněny, pokud jsou plně zpracovány. Doklad o vyskladnění skladu zůstává otevřený, dokud není zaregistrováno celé množství souvisejícího zaúčtovaného skladového dokladu. Pole **Zaskladněné  množství** na řádcích objednávky příjemky ze skladu je aktualizováno.

## Viz také
[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]