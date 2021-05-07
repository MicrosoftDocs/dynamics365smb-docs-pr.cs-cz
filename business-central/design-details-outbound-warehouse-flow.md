---
    title: Design Details - Outbound Warehouse Flow | Microsoft Docs
    description: The outbound flow in the warehouse begins with a request from released source documents to bring the items out of the warehouse location, either to be shipped to an external party or to another company location. From the storage area, warehouse activities are performed at different complexity levels to bring the items out to the shipping docks.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: edupont

---
# Detaily návrhu: Výstupní procesy skladu

Výstupní tok ve skladu začíná požadavkem vydaných zdrojových dokladů na vydání zboží ze skladu, které má být dodáno externí straně nebo do jiného skladu společnosti. Z oblasti skladování se různé skladové činnosti provádějí na jistých úrovních složitosti, aby se zboží dostalo do přepravních doků.

Každá položka je identifikována a spárována s odpovídajícím vstupním zdrojovým dokladem. Existují následující výstupní zdrojové doklady:

- Prodejní objednávka
- Výstupní objednávka transferu
- Objednávka nákupní vratky
- Servisní zakázka

Kromě toho existují následující interní zdrojové doklady, které fungují jako výstupní zdroje:

- Výrobní zakázka s potřebou komponent
- Montážní zakázka s potřebou komponent

Poslední dva doklady představují odchozí toky ze skladu do interních provozních oblastí. Další informace o manipulaci se sklady pro interní příchozí a odchozí procesy najdete v [Detaily návrhu: Interní procesy skladu](design-details-internal-warehouse-flows.md).

Procesy a doklady uživatelského rozhraní v odchozích tocích skladu se liší pro základní a pokročilé nastavení skladu. Hlavním rozdílem je, že aktivity jsou zpracovány po objednávkách v základních konfiguracích skladu a jsou konsolidovány pro více objednávek v pokročilých konfiguracích skladu. Další informace o různých úrovních složitosti skladu najdete v [Detaily návrhu: Přehled skladu](design-details-warehouse-setup.md).

V [!INCLUDE[prod_short](includes/prod_short.md)] odchozí procesy vyskladnění a expedice lze provádět čtyřmi způsoby pomocí různých funkcí v závislosti na úrovni složitosti skladu.

| Metoda | Odchozí proces | Přihrádky | Vyskladnění | Dodávky | Úroveň složitosti (Viz [Detaily návrhu: Nastavení skladu](design-details-warehouse-setup.md)) |
|------|----------------|----|-----|---------|-------------------------------------------------------------------------------------|  
| A | Zaúčtování vyskladnění a dodávky z řádku objednávky | X | 2 |
| B | Zaúčtování vyskladnění a dodávky z dokladu vyskladnění zásob | X | 3 |
| C | Zaúčtování vyskladnění a dodávky z dokladu dodávky ze skladu | X | 4/5/6 |
| D | Zaúčtování vyskladnění z dokladu vyskladnění a zaúčtování dodávky z dokladu dodávky ze skladu | X | X | 4/5/6 |

Výběr přístupu závisí na přijatých postupech společnosti a na úrovni jejich organizační složitosti. V prostředí zpracování objednávek po objednávce s přímočarými procesy a jednoduchou strukturou přihrádek je vhodná metoda A, vychystávání a dodávka z řádku objednávky. V jiných společnostech typu „objednávka po objednávce“, kde zboží pro jeden řádek objednávky může pocházet z více než jedné přihrádky nebo kde pracovníci skladu nemohou pracovat s doklady objednávky, je vhodné použít samostatné doklady vyskladnění, metoda B. Pokud procesy vyskladnění a expedice společnosti zahrnují více zpracování objednávek, a proto vyžadují větší kontrolu a přehled, může se společnost rozhodnout použít doklady dodávky ze skladu a vyskladnění k oddělení výdejních a dodacích úkolů, metod C a Dodávky ze skladu.

V metodách A, B a C jsou akce vyskladnění a dodávky kombinovány v jednom kroku při zaúčtování odpovídajícího dokladu jako dodaný. V metodě D je vyskladnění nejprve zapsáno a poté je dodávka zaúčtována z jiného dokladu.

## Základní konfigurace skladu

Následující diagram znázorňuje výstupní toky ze skladu podle typu dokladu v základním nastavení skladu. Čísla v diagramu odpovídají krokům v následujících částech diagramu.

![Výstupní tok v základním nastavení skladu](media/design_details_warehouse_management_outbound_basic_flow.png "Čísla v diagramu odpovídají krokům v následujících částech diagramu.")

### 1: Vydání zdrojového dokladu / Vytvoření vyskladění nebo přesunu

Pokud je uživatel, který je zodpovědný za zdrojové doklady, například zpracovatel prodejních objednávek nebo plánovač výroby, připraven na výstupního aktivitu skladu, vydá zdrojový doklad, aby dal pracovníkům skladu signál, že prodané zboží nebo komponenty lze vyskladní a umístit do zadaných přihrádek. Alternativně uživatel vytvoří doklady vyskladnění nebo přesunu zásob pro jednotlivé řádky objednávky nabízeným způsobem na základě zadaných přihrádek a množství, která mají být zpracovávána.

> [!NOTE]  
> Pohyby zásob se používají k přesunu zboží do interních provozních oblastí v základním nastavení skladu na základě zdrojových dokladů nebo na základě ad hoc přesunutí.

### 2: Vytvoření odchozího požadavku

Po vydání výstupního zdrojového dokladu je automaticky vytvořen výstupní požadavek skladu. Obsahuje odkazy na typ a číslo zdrojového dokladu a není pro uživatele viditelný.

### 3: Vytvoření vyskaladnění nebo přesunu

Na stránce **Vyskladnění zásob** nebo **Pohyby zásob**, pracovník skladu obdrží vyžádaně řádky čekajícího zdrojového dokladu na základě odchozích požadavků skladu. Případně jsou řádky vyskladnění zásob již vytvořené uživatelem, který je zodpovědný za zdrojový doklad.

### 4: Zápis vyskladnění nebo zaevidování Přesunu zásob

Na každém řádku pro zboží, které bylo částečně nebo úplně vyskladněno, pracovník skladu vyplní pole **Množství**, a potom zapíše vyskladnění zásob nebo zaeviduje přesun zásob. Zdrojové doklady související s vyskladněním zásob jsou zaúčtovány jako dodané nebo spotřebované. Zdrojové doklady související s přesuny zásob nejsou zaúčtovány.

Pro vyskladnění zásob jsou vytvořeny záporné položky zboží, vytvořeny položky skladu a odstraněn požadavek na vyskladnění, pokud je plně zpracován. Například pole **Dodané množství** na řádku výstupního zdrojového dokladu. Vytvoří se zaúčtovaný doklad dodávky, který odráží například prodejní objednávku a dodané zboží.

## Pokročílé nastavení skladu

Následující diagram znázorňuje výstupní tok ze skladu podle typu dokladu při pokročilém nastavení skladu. Čísla v diagramu odpovídají krokům v následujících částech diagramu.

![Výstupní tok v pokročilém nastavení skladu](media/design_details_warehouse_management_outbound_advanced_flow.png "Výstupní tok v pokročilém nastavení skladu")

### 1: Vydání zdrojového dokladu

Pokud je uživatel, který je zodpovědný za zdrojové doklady, například zpracovatel prodejních objednávek nebo plánovač výroby, připraven na výstupního aktivitu skladu, vydá zdrojový doklad, aby dal pracovníkům skladu signál, že prodané zboží nebo komponenty lze vyskladní a umístit do zadaných přihrádek.

### 2: Vytvoření výstupního požadavku (2)

Po vydání výstupního zdrojového dokladu je automaticky vytvořen výstupní požadavek skladu. Obsahuje odkazy na typ a číslo zdrojového dokladu a není pro uživatele viditelný.

### 3: Vytvoření dodávky ze skladu

Na stránce **Dodávky ze skladu**pracovník, který je odpovědný za výstup ze skladu, vidí čekající řádky zdrojového dokladu na základě požadavku. Několik řádků zdrojového dokladu lze kombinovat v jednom dokladu dodávky ze skladu.

### 4: Vydání dodávky ze skladu / Vytvoření vyskladnění

Odpovědný pracovník expedice vydá dodávku ze skladu, aby pracovníci skladu mohli vytvořit nebo koordinovat vyskladnění pro příslušnou dodávku.

Alternativně může uživatel vytvořit doklad vyskladnění pro jednotlivé řádky dodávky nabízeným způsobem na základě zadaných přihrádek a množství, které má být zpracováno.

### 5: Vydání interní operace / Vytvoření vyskladnění

Uživatel odpovědný za interní operace vydá interní zdrojový doklad, například výrobní a montážní zakázku, aby pracovníci skladu mohli vytvářet nebo koordinovat vyskladnění pro interní operaci.

Alternativně uživatel vytvoří doklady vyskladnění pro jednotlivé výrobní nebo montážní zakázky nabízeným způsobem na základě zadaných přihrádek a množství, která mají být zpracována.

### 6: Vytvoření požadavku vyskladnění

Po vydání výstupního zdrojového dokladu se automaticky vytvoří požadavek na vyskladnění. Obsahuje odkazy na typ a číslo zdrojového dokladu a není pro uživatele viditelný. V závislosti na nastavení se vytvoří spotřeba z výrobní a montážní zakázky a také požadavek na vyskladnění potřebných komponent ze skladu.

### 7: Generování řádků sešitu vyskladnění

Uživatel, který je zodpovědný za koordinaci vyskladnění, načte řádky vyskladnění v **Sešitu vyskladnění** na základě požadavků na vyskladnění z dodávek ze skladu nebo interních operací se spotřebou komponent.  Uživatel vybere řádky, které mají být vyskladněné a připraví vyskladnění určením přihrádek, ze kterých se má odebírat a vkládat a kolik jednotek má být manipulováno. Přihrádky mohou být předdefinovány nastavením skladu nebo zdroje.

Uživatel určuje metody vyskladnění pro optimalizované zpracování skladu a potom pomocí funkce vytvoří odpovídající doklady vyskladnění, které jsou přiřazeny různým pracovníkům skladu, kteří provádějí vyskladnění. Po úplném přiřazení vyskladnění budou řádky v  **Sešitu vyskladnění** smazány.

### 8: Vytvoření dokladů vyskladnění

Pracovník skladu, který provádí vyskladnění, vytvoří doklad vyskladnění na základě vydaméjp zdrojové dokladu. Alternativně je doklad vyskladnění vytvořen a přiřazen pracovníkovi skladu nabízeným způsobem.

### 9: Zápis vyskladnění

Na každém řádku pro zboží, které bylo vyskladněno, částečně nebo úplně, pracovník skladu vyplní pole **Množství** na stránce **Vyskladnění** a poté ho zapíše.

Položky skladu jsou vytvořeny a řádky vyskladnění jsou odstraněny, pokud jsou plně zpracovány. Doklad vyskladnění zůstane otevřený, dokud není zapsáno celé množství související dodávky ze skladu. Pole ** Množství k vyskladnění** je na řádcích dodávek ze skladu je odpovídajícím způsobem aktualizováno.

### 10: Účtování dodávky ze skladu

Když jsou všechny položky v dokladu dodávky ze skladu zapsané jako vyskladněné do určených přihrádek, pracovník, který je zodpovědný za zaúčtování dodávky ze skladu dodávku zaúčtuje. Vytvoří se záporné položky zboží. Například pole **Dodané množství** na řádku výstupního zdrojového dokladu.

## Viz také

[Detaily návrhu: Správa skladu](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]