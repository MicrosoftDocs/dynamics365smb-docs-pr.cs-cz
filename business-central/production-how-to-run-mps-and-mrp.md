---
    title: How to Run Full Planning, MPS and MRP | Microsoft Docs
    description: The terms "running the planning worksheet" or "running MRP" refer to the calculation of the master production schedule and material requirements based on actual and forecasted demand. The planning system can calculate either Master Planning Schedule (MPS) or Material Requirements Planning (MRP) on request, or it can calculate both at the same time.
    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2019
    ms.author: sgroespe

---
# Spuštění úplného plánování, MPS nebo MRP
Termíny "spuštění sešitu plánování" nebo "spuštění MRP" odkazují na výpočet hlavního výrobního plánu a požadavků na materiál na základě skutečné a předpokládané poptávky. Plánovací systém může na vyžádání vypočítat buď hlavní plán plánování (MPS) nebo plánování požadavků na materiál (MRP), může také vypočítat obojí současně.

- MPS je výpočet hlavního výrobního plánu na základě skutečné poptávky a prognózy poptávky. Výpočet MPS se používá pro koncové položky, které mají prognózu nebo řádek prodejní objednávky. Tyto položky se nazývají položky MPS a jsou dynamicky identifikovány při zahájení výpočtu.
- MRP je výpočet materiálových požadavků založený na skutečné poptávce po komponentách a prognóze poptávky na úrovni komponent. MRP se počítá pouze pro položky, které nejsou položkami MPS. Účelem MRP je poskytnout časově uspořádané formální plány podle položek, dodávat příslušné zboží v příslušném čase, na příslušném místě, v odpovídajícím množství.

Algoritmy plánování používané pro MPS i MRP jsou identické. Algoritmy plánování se týkají určování čistých částek, opětovného použití stávajících objednávek doplňování a zpráv o akci. Proces plánovacího systému zkoumá, co je třeba nebo bude potřeba (poptávka) a co je po ruce nebo se očekává (nabídka). Když jsou tato množství vzájemně započtena, [!INCLUDE[d365fin](includes/d365fin_md.md)] poskytuje zprávy o akcích. Zprávy o akci jsou návrhy na vytvoření nové objednávky, změnu objednávky (množství nebo datum) nebo zrušení objednávky, která již byla na objednávce. Termín „objednávka“ zahrnuje objednávky, montážní objednávky, výrobní zakázky a převody.

Odkazy vytvořené plánovacím modulem mezi poptávkou a související nabídkou lze sledovat na stránce **Sledování objednávek**. Pro více informací navštivte [Sledování vztahů mezi poptávkou a dodávkou](production-how-track-demand-supply.md).

Správné výsledky plánování závisí na nastavení provedeném na kartách zboží, kusovníky montáže, výrobní kusovníky a postupech.

## Metody generování plánu

- **Vypočítat regenerační plán:** Tato funkce zpracuje nebo obnoví materiálový plán. Tento proces začíná odstraněním všech plánovaných objednávek dodávek, které jsou aktuálně načteny. Všechny položky v databázi jsou znovu naplánovány.
- **Vypočítat plánovaný pohyb**: Tato funkce zpracuje plánovaný pohyb. Zboží při plánování pohybu je bráno v úvahu ze dvou typů změn:
   - **Poptávka / změny nabídky:** Patří mezi ně úpravy množství na prodejních objednávkách, prognózách poptávky, objednávkách sestavení, výrobních zakázkách nebo nákupních objednávkách. Neplánovaná změna úrovně zásob se také považuje za změnu množství.
   - **Změna parametru:** Patří mezi ně změny v bezpečnostním skladu, bodu přiobjednání, technologickém postupu, kusovníku a změny výpočtu intervalu dostupnosti nebo výpočet doby realizace
- **Získat hlášení akcí:** Tato funkce slouží jako nástroj krátkodobého plánování tím, že vydává zprávy o akcích, které uživatele upozorní na všechny změny provedené od výpočtu posledního regeneračního nebo čistého plánu změn.

S každou plánovanou metodou, [!INCLUDE[d365fin](includes/d365fin_md.md)] generuje položky v sešitu plánování za předpokladu nekonečné kapacity. Kapacita pracovního a strojního centra se při vývoji plánů nezvažuje.

> [!IMPORTANT]
> Funkce Vypočítat regenerační plán je nejběžnějším procesem. Avšak funkce Vypočítat plán a Provést hlášené akce, lze použít ke spuštění procesu Vypočítat plánovaný pohyb.
> Funkce Získat plán hlášení akcí může být spuštěna mezi regeneračními a čistými změnami plánování, aby se získala okamžitý náhled na účinek změn plánu, ale není zamýšlen jako náhrada úplných plánů regenerativní nebo síťové změny.
> 
## Výpočet plánovacího listu
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Sešity plánování** a poté vyberte související odkaz.
2. Vyberte akci **Vypočítat regenerační plán** k otevření stránky **Vypočítat plán**.
3. Na záložce s náhledem **Nastavení**, vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **MPS** | Tuto možnost vyberte, chcete-li zahájit výpočet hlavního plánu výroby. V tomto spuštění jsou považovány za položky s otevřenými prodejními objednávkami nebo prognózami poptávky. |
   | **MRP** | Vyberte, chcete-li zahájit výpočet plánování materiálových požadavků. V tomto spuštění jsou požadovány položky se závislými požadavky. Obvykle, jsou MPS and MRP spuštěny současně. Chcete-li současně spustit  MPS and MRP, pole **Kombinovaný výpočet MPS/MRP** musí být zvoleno na záložce s náhledem **Plánování** na stránce **Nastavení výroby**. |
   | **Počáteční datum** | Toto datum se používá k vyhodnocení dostupnosti zásob. Pokud je množství na skladě položky pod bodem přiobjednání, systém dodá objednávku doplnění od tohoto data. Pokud je položka pod její pojistnou zásobou (k počátečnímu datu), systém vrátí zpět objednávku doplnění splatnou k počátečnímu datu plánování. |
   | **Koncové datum** | Toto je koncové datum horizontu plánování. Po tomto datu není uvažována ani poptávka, ani nabídka. Pokud cyklus přiobjednání zboží přesahuje koncové datum, efektivní horizont plánování pro toto zboží se rovná datu objednávky + cyklus přiobjednávky. <br /><br /> Horizont plánování je čas, na který je plán prodloužen. Pokud je horizont příliš krátký, položky s delší dobou realizace nejsou včas objednány. Pokud je horizont příliš dlouhý, strávíte příliš mnoho času kontrolou a zpracováváním informací, které se pravděpodobně změní dříve, než budou potřeba. Je možné nastavit jeden plánovací horizont pro výrobu a delší pro nákupy, i když to není nutné. Plánovací horizont nákupů a výroby by měl být nastaven tak, aby pokrýval kumulativní dobu realizace součástí. |
   | **Zastavit a zobrazit první chybu** | Tuto možnost vyberte, pokud chcete, aby se spuštění plánování zastavilo, jakmile dojde k chybě. Současně se zobrazí zpráva s informacemi o první chybě. Pokud dojde k chybě, budou v plánovacím sešitu zobrazeny pouze úspěšné řádky plánování provedené před výskytem chyby. Pokud toto pole nevyberete, bude dávková úloha **Vypočítat plán** pokračovat, dokud nebude dokončena, to znamená, že dávky nepřeruší dávkovou úlohu. Pokud existuje jedna nebo více chyb, zobrazí se po dokončení zpráva s informacemi o tom, kolik položek je ovlivněno. Stránka **Protokol chyb plánování**, která poskytne další podrobnosti o chybě a odkazy na ovlivněné karty položek. |
   | **Použít prognózu** | Vyberte prognózu, která by měla být zahrnuta jako poptávka při spuštění dávkové úlohy plánování. Výchozí předpověď je nastavena na záložku s náhledem **Plánování** na stránce **Nastavení výroby**. |
   | **Vyloučit prognózu před** | Definujte, kolik z vybrané prognózy chcete zahrnout do plánovacího běhu zadáním data, do kterého není zahrnuta poptávka po prognóze, což vám umožní vyloučit staré informace. |
   | **Respektování parametrů plánování pro varování výjimek** | Ve výchozím nastavení je toto pole vybráno.<br /><br /> Dodávky na plánovacích řádcích s varováním se obvykle nemění podle parametrů plánování. Místo toho plánovací systém pouze navrhuje dodávku, která pokryje přesné množství poptávky. Můžete však definovat určité parametry plánování pro řádky plánování, které mají být dodrženy s určitými upozorněními.<br /><br /> |

4. Na záložce s náhledem **Zboží**, nastavte filtry pro spuštění plánování na základě položky, popisu položky nebo umístění.
5. Zvolte tlačítko **OK**. Dávková úloha se spustí a sešit plánování se naplní řádky plánování.

## Provádění akčních zpráv
1. Na stránce **Sešity plánování**, zvolte akci **Provést hlášené akce**.
2. Na záložce s náhledem **Nastavení**, určete způsob vytvoření spotřebního materiálu. Vyplňte pole podle popisu v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Výrobní zakázka** | Určete způsob vytvoření výrobních zakázek. Můžete to provést přímo z návrhů řádků plánování. Můžete vytvořit plánované nebo pevně plánované výrobní zakázky. |
   | **Montážní zakázky** | Určete, jak chcete vytvořit montážní zakázky. Můžete to provést přímo z návrhů řádků plánování. |
   | **Nákupní objednávky** | Určete, jak chcete vytvářet nákupní objednávky. Můžete to provést přímo z návrhů řádků plánování.<br /><br /> Pokud jste se rozhodli zkopírovat návrhy řádků plánování pro nákupní objednávky do sešitu požadavků, vyberte šablonu a název listu. |
   | **Objednávka transferu** | Určete, jak chcete vytvořit příkazy k převodu. Můžete to provést přímo z návrhů řádků plánování.<br /><br /> Pokud jste se rozhodli zkopírovat návrhy řádků plánování pro převodní příkazy do sešitu požadavků, vyberte šablonu a název listu. |
   | **Kombinovat objednávky transferu** | Vyberte, zda chcete kombinovat příkazy k převodu. |
   | **Zastavit a zobrazit první chybu** | Vyberte, pokud chcete, aby dávková úloha **Provést hlášení akce - plán.** se zastavila, jakmile narazí na chybu. Současně se zobrazí zpráva s informacemi o první chybě. Pokud dojde k chybě, vytvoří se objednávky dodávky pouze ze řádků plánování zpracovaných před výskytem chyby. |

3. Na záložce **Řádek plánování**, můžete nastavit filtry, které omezí zprávy o akcích provádění.
4. Zvolte tlačítko **OK**.

Dávková úloha odstraní řádky v plánovacím sešitu po provedení zprávy akce. Ostatní řádky zůstanou v plánovacím sešitu, dokud nebudou přijaty později, nebo odstraněny. Řádky můžete také odstranit ručně.

## Akční zprávy
Zprávy akcí jsou vydávány systémem sledování objednávek, pokud je zůstatek v existující síti objednávek nedosažitelný. To lze je považovat za návrh, jak zpracovat změny, které obnoví rovnováhu mezi nabídkou a poptávkou.

Generování akčních zpráv dochází vždy současně pro jednu úroveň, pro každý kód nižší úrovně položky. Tím je zajištěno, že se berou v úvahu všechny položky, které zažijí nebo zažívají změny v nabídce nebo poptávce.

Aby se předešlo malým, zbytečným nebo nedůležité akčním zprávám, může uživatel zřídit prodlevu, která slouží k omezení generování akčních zpráv pouze na ty změny, které přesahují definované množství nebo počet dní.

Poté, co jste zkontrolovali akční zprávy a určili, zda chcete přijmout některé nebo všechny navrhované změny, vyberte pole **Přijmout hlášené akce**, a pak jste připraveni odpovídajícím způsobem aktualizovat plány.

> [!NOTE]
Akční zpráva je návrhem na vytvoření nové objednávky, zrušení objednávky nebo změnu množství nebo data objednávky. Objednávka je nákupní objednávka, objednávka transferu nebo výrobní zakázka.

V reakci na jakékoli nerovnováhy mezi nabídkou a poptávkou se generují následující zprávy o činnosti:

| Zpráva akce | Popis |
|--------------------|---------------------------------------|  
| **Nový** | Pokud poptávka nemůže být vyplněna a pomocí navrhováním akčních zpráv, které mají vést k **Změna množ.**, **Přeplánování**, nebo **Přeplánování a Změna množ..** a stávajících objednávkách , je vygenerována akční zpráva **Nový**, která navrhne novou objednávku. Kromě toho, je zpráva **Nový** vygenerována, pokud neexistují objednávky dodávek v cyklu změny pořadí dotyčné položky. Tento parametr určuje počet období vpřed a vzad v profilech dostupnosti při hledání objednávky k přeplánování. |
| **Změnit množství** | Pokud dojde ke změně množství poptávky, která je sledována na objednávce dodávky, je generována zpráva **Změna množství**, která naznačuje, že související nabídka by měla být změněna vzhledem ke změně poptávky. Pokud se objeví nová poptávka, [!INCLUDE[d365fin](includes/d365fin_md.md)] vyhledá nejbližší existující neobsazené pořadí objednávek dodávky v cyklu přiobjednání a vydá změnu zprávy akce pro tuto objednávku. |
| **Přeplánování** | Když dojde k objednávce dodávky nebo požadavku na změnu data způsobující nerovnováhu v síti objednávek, je vygenerována zpráva akce **Přeplánovat**. Pokud existuje vztah 1:1 mezi poptávkou a nabídkou, je generována zpráva akce, která naznačuje, že objednávka dodávky byla odpovídajícím způsobem přesunuta. Pokud objednávka dodávky pokrývá poptávku z více než jedné prodejní objednávky, je objednávka dodávky přeplánována tak, aby byla rovna datu první poptávky. |
| **Přeplán. změna množ.** | Pokud byly jak data, tak množství objednávky změněny, musíte změnit plány s ohledem na obě okolnosti. Zprávy o akci shromažďují obě akce v jedné zprávě, **Přeplán. změna  množ.**, aby se zajistilo, že se síť objednávek vrátí do rovnováhy. |
| **Zrušit** | Pokud je poptávka, která byla pokryta na základě zakázky-na-zakázku, je odstraněna, je zpráva vygenerována zpráva o akci, která zruší související objednávku na dodávku. Pokud vztah není typu zakázka-na-zakázku, an action message is generated to change in order to reduce the supply. Pokud prostřednictvím jiných faktorů, například úprav zásob, není vyžadována objednávka dodávky v okamžiku, kdy uživatel generuje zprávy akcí, [!INCLUDE[d365fin](includes/d365fin_md.md)] navrhne v listu zprávu akcí s **Zrušit**. |

## Viz také
[Plánování](production-planning.md)  
[Nastavení výroby](production-configure-production-processes.md)  
[Výroba](production-manage-manufacturing.md)  
[Zásoby](inventory-manage-inventory.md)  
[Nákup](purchasing-manage-purchasing.md)  
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)  
[Doporučené postupy nastavení: Plánování dodávek](setup-best-practices-supply-planning.md)  
[Práce s [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
