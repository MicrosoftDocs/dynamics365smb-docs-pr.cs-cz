---
    title: Walkthrough - Planning Supplies Automatically | Microsoft Docs
    description: Phrases like "run planning" and "run MRP" refer to the calculation of the master production schedule (MPS) and the material requirements plan (MRP) based on actual and forecasted demand.
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
# Návod: Automatické plánování dodávek

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

Fráze jako "plánování spustění" a "spustit MRP" odkazují na výpočet hlavního výrobního plánu (MPS) a plánu materiálových požadavků (MRP) na základě skutečné a předpokládané poptávky.

- MPS je výpočet hlavního výrobního plánu na základě skutečné poptávky a prognózy poptávky. Výpočet MPS se používá pro koncové zboží, které má prognózu nebo řádek prodejní objednávky. Tyto položky se nazývají "položky MPS" a jsou dynamicky identifikovány při spuštění výpočtu.
- MRP je výpočet materiálových požadavků na základě skutečné poptávky po komponentách a předpovědi poptávky na úrovni komponent. MRP se počítá pouze pro položky, které nejsou položkami MPS. Celkovým účelem MRP je poskytovat časově rozložené formální plány, podle jednotlivých zboží, dodávat správné zboží ve správný čas, na správném místě a ve správném množství.

Algoritmy plánování používané pro MPS i MRP jsou identické. Algoritmy plánování používají síťování, opětovné použití stávajících objednávek dodávek a zprávy akcí. Proces plánovacího systému zkoumá, co je potřeba nebo bude potřeba (poptávka) a co je dostupné nebo očekávané (nabídka). Když jsou tyto veličiny vzájemně propojeny, zobrazí se v plánovacím listu zprávy o akci. Zprávy o akci jsou návrhy na vytvoření nové objednávky, změnu objednávky (množství nebo datum) nebo zrušení stávající objednávky. Objednávky dodávek mohou být výrobní zakázky, nákupní objednávky a objednávky transferu. Pro více informací navštivte [Detaily návrhu: Plánování dodávek](design-details-supply-planning.md).

Výsledek plánování se vypočítá částečně ze sad poptávky a nabídky v databázi a částečně z nastavení karet skladových jednotek nebo karet zboží, výrobních kusovníků a TNG postupů.

## Návod
Tento návod ukazuje, jak pomocí systému plánování dodávek automaticky plánovat všechny nákupní a výrobní objednávky potřebné k výrobě 15 cestovních jízdních kol požadovaných na různých prodejních objednávkách. Chcete-li poskytnout jasný a realistický návod, je počet řádků plánování vymezen odfiltrováním všech ostatních sad poptávky a nabídky v demonstrační společnosti CRONUS s výjimkou prodejní poptávky v lokaci EAST.

Tento návod ilustruje následující úkoly:

- Vytvoření prodejní objednávky a výpočet kompletního plánu dodávek.
- Zobrazení parametrů plánování a položek sledování objednávek za řádky plánování.
- Automatické vytvoření navrhovaných objednávek dodávek.
- Vytvoření nové prodejní poptávky a odpovídajícího opětovného plánování.

## Role

- Výrobní plánovač
- Nákupní agent

## Předpoklady
K dokončení tohoto návodu budete potřebovat:

- Demonstrační společnost CRONUS CZ s.r.o.  
- Chcete-li změnit různé hodnoty nastavení položky, postupujte podle kroků v části „Příprava ukázkových dat“, dále v tomto návodu.

## Příběh
Zákazník, společnost BYT-KOMPLET s.r.o., si objedná pět cestovních kol k odeslání dne 02-05-2021 (5. února).

Eduardo, plánovač výroby, provádí rutinní plánování dodávek pro první únorový týden 2021. Filtruje na své vlastní lokaci, EAST, a před výpočtem počátečního plánu dodávek zadá plánovací interval pracovního data (01-23-2021) do 02-07-2021.

Jediným požadavkem v tomto týdnu je objednávka odběratele BYT-KOMPLET. Eduardo vidí, že žádný z řádků plánování nemá varování, a pokračuje ve vytváření objednávek dodávek beze změn pro navrhované řádky plánování.

Následujícího dne, před zahájením nebo odesláním některé z počátečních objednávek na dodávku, je Eduardo upozorněn, že jiný zákazník si objednal deset cestovních kol k odeslání 02-12-2021. Přepočítá, aby upravil plán dodávek podle změny poptávky. Přepočet vám poskytne plán čistých změn, který navrhuje změny času i množství některých objednávek dodávek vytvořených při prvním spuštění.

Během různých plánovacích kroků Eduardo vyhledává zahrnuté objednávky a pomocí funkce Sledování objednávek sleduje, která poptávka je pokryta kterou nabídkou.

## Příprava ukázkových dat
Vytvořte skladové jednotky (SKJ) pro cestovní kolo a výběr jeho komponentů, čísla položek 1001 až 1300. (Některé komponenty jsou kvůli zjednodušení postupů vyloučeny.) Upravte parametry plánování vybraných komponent, abyste získali transparentnější výsledek plánování.

### Vytváření skladových jednotek

1. Otevřete kartu zboží pro položku 1001, Turistické kolo.
2. Vyberte akci **Vytvořit skladovou jednotku**.
3. Na stránce **Vytvořit skladovou jednotku** nechejte všechny možnosti a filtry beze změny a poté klikněte na tlačítko **OK**.
4. Opakujte kroky 1 až 3 pro všechno zboží v rozsahu čísel mezi 1100 a 1300.

### Změna vybraných parametrů plánování

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Skladové jednotky** a poté vyberte související odkaz.
2. Otevřete kartu skladové jednotky EAST pro položku 1100, přední kolo.
3. Na záložce **Plánování** vyplňte pole, jak je popsáno v následující tabulce.

   | Způsob přiobjednání | Minimální zásoby | Období kumulace dávky | Období přeplánování |
   |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
   | Dávka-pro-dávku | Prázdné | 2W | 2W |

4. Opakujte kroky 2 a 3 pro všechny SKJ v rozsahu čísel od 1100 do 1300.

Tím je dokončena příprava ukázkových dat pro návod.

## Vytvoření regeneračního plánu dodávek
V reakci na novou prodejní objednávku na pět turistických kol zahajuje Ricardo plánovací proces nastavením možností, filtrů a plánovacího intervalu, aby vyloučil veškerou další poptávku kromě poptávky prvního únorového týdne v lokaci EAST. Začíná výpočtem hlavního výrobního plánu (MPS) a poté pokračuje výpočtem úplného plánu dodávek pro veškerou poptávku na nižší úrovni (MRP).

### Vytvoření prodejní objednávky

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
2. Vyberte akci **Nový**.
3. Na stránce **Prodejní objednávka** vyplňte pole, jak je popsáno v následující tabulce.

   | Zákazník-název | Datum odeslání | Číslo zboží | Lokace | Množství |
   |----------------------------|-------------------|--------------|--------------|--------------|  
   | BYT-KOMPLET | 02-05-2014 | 1001 | EAST | 5 |

4. Přijměte varování o dostupnosti a kliknutím na tlačítko **Ano** zaznamenejte nové množství poptávky.

### Vytvoření regeneračního plánu pro splnění poptávky v lokaci EAST

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat<"), zvolte **Plánovací sešit** a poté vyberte související odkaz.
2. Vyberte akci **Vypočítat regenerační plán**.
3. Na stránce **Výpočet plánu – plán. sešit** vyplňte pole, jak je popsáno v následující tabulce.

   | Vypočítat plán | Počáteční datum | Datum ukončení | Zobrazit výsledky: | Omezit součty na |
   |--------------------|-------------------|-----------------|-------------------|---------------------|  
   | **MPS** = Ano<br /><br /> **MRP** = Ne | 01-23-2021<br /><br /> (pracovní datum) | 02-07-2021 | 1001..1300 | Filtr lokace = EAST |

4. Kliknutím na tlačítko **OK** zahájíte plánovací běh.

   Vytvoří se jeden řádek plánování, který navrhuje, aby byla vydána plánovaná výrobní zakázka na výrobu deseti cestovních kol, položka 1001, do 02-05-2021, datum dodávky prodejní objednávky.

   Dále ověřte, zda se tento řádek plánování vztahuje k prodejní objednávce BYT-KOMPLET použitím **Sledování zakázky**, která dynamicky propojuje poptávku s plánovanou nabídkou.

5. Vyberte nový řádek plánování a pak zvolte akci **Sledování zakázky**.
6. Na stránce **Sledování zakázky** vyberte akci **Zobrazit**.

   Je zobrazena prodejní objednávka na pět turistických kol odeslaných na číslo zákazníka 10 000 dne 02-05-2021.

7. Zavřete stránky **Prodejní objednávka** a **Sledování zakázky**.

### Výpočet MRP tak, aby zahrnoval potřeby základních komponent

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat<"), zvolte **Plánovací sešit** a poté vyberte související odkaz.
2. Vyberte akci **Vypočítat regenerační plán**.
3. Na stránce **Výpočet plánu – plán. sešit** vyplňte pole, jak je popsáno v následující tabulce.

   | Výpočet | Počáteční datum | Datum ukončení | Zobrazit výsledky: | Omezit součty na: |
   |---------------|-------------------|-----------------|-------------------|----------------------|  
   | **MPS** = Ano<br /><br /> **MRP** = Ano | 01-23-2021 | 02-07-2021 | 1001..1300 | Filtr lokace = EAST |

4. Kliknutím na tlačítko **OK** zahájíte plánovací běh.

   Celkem je vytvořeno 14 řádků plánování, které navrhují objednávky dodávek pro veškerou poptávku, kterou představuje objednávka prodeje cestovních kol v lokaci EAST.

## Analýza výsledku plánování
Chcete-li analyzovat navrhovaná množství, Eduardo rozbalí vybrané řádky plánování a zobrazí položky sledování objednávek a parametry plánování.

Na stránce **Plánovací sešit** si ve sloupci **Datum vyřízení** všimněte, že navrhované objednávky dodávek jsou naplánovány zpětně od data splatnosti prodejní objednávky, 02-05-2021. Časová osa začíná na horním řádku plánování s výrobní zakázkou na výrobu hotových cestovních kol. Časová osa končí na spodním řádku plánování nákupní objednávky pro jednu z položek na nejnižší úrovni, 1255, Zadní lůžko, splatná 01-30-2021. Stejně jako plánovací řádek pro položku 1251, Oska zadního kola, představuje tento řádek nákupní objednávku pro komponenty, které jsou splatné k datu zahájení jeho vyrobené nadřazené položky podsestavy 1250, což je splatné 02-03-2014. V celém listu můžete vidět, že všechny podkladové položky jsou splatné k počátečnímu datu jejich rodičů.

Řádek plánování položky 1300, Soustava převodů, navrhuje deset kusů. To se liší od pěti kusů, které podle nás potřebují ke splnění prodejní objednávky. Pokračujte zobrazením záznamů sledování objednávky.

### Zobrazení položek sledování objednávek pro zboží 1300

1. Vyberte řádek plánování pro položku 1300 a pak zvolte akci **Sledování zakázky**.

   Dva řádky na stránce **Sledování zakázky** ukazují, že je sledováno pět kusů od plánovacího řádku (první řádek sledování objednávky) po prodejní objednávku 1001 (druhý řádek sledování objednávky). Posledních pět kusů navrhovaných na řádku plánování nesouvisí s žádnými řádky dokladu, ale s parametrem plánování, položkou prognózy nebo položkou hromadné objednávky. Taková nesledovaná množství jsou sečtena v poli **Nesledované množství** v záhlaví stránky **Sledování zakázky**.

2. Vyberte pole **Nesledované množství**.

   Stránka **Nesledované prvky plánování** ukazuje, že položka 1300 používá plánovací parametr, Minimální množství objednávky, 10,00. Řádek plánování je tedy celkem na deset kusů, z nichž lze podle poptávky sledovat pouze pět. Posledních pět kusů je nesledované množství, které uspokojí parametr plánování. Pokračujte kontrolou parametru plánování.

### Kontrola parametru plánování

1. Na stránce **Nesledované prvky plánování** vyberte řádek sledování objednávky pro položku 1300.
2. Vyberte pole **Číslo zboží** a poté vyberte akci **Rozšíření**.
3. Na stránce **Přehled zboží** vyberte akci **Skladové jednotky**.
4. Na stránce **Přehled skladových jednotek** otevřete kartu EAST jednotky skladu.
5. Na záložce **Plánování** si všimněte, že pole **Minimální obj.množství** obsahuje 10.
6. Zavřete všechny stránky kromě stránky **Plánovací sešit**.

### Zobrazení dalších položek sledování objednávek

1. Vyberte řádek plánování pro položku 1110, Ráfek a pak zvolte akci **Sledování zakázky**.

   Stránka **Sledování zakázky** ukazuje, že pro každou výrobní zakázku je potřeba pět ráfků pro přední a zadní kola.

   Stejné sledování objednávek platí pro řádky plánování pro položky 1120, 1160 a 1170. U položky 1120 je pole **Množství za** na kusovníku výroby každé položky kola 50 KS, což má za následek celkovou potřebu 100.

   Řádek plánování položky 1150 pro šest kusů vypadá nepravidelně. Pokračujte v analýze.

2. Vyberte řádek plánování pro položku 1150 a pak zvolte akci **Sledování zakázky**.

   Stránka **Sledování zakázky** ukazuje, že pět jednotek je sledováno k přednímu kolu a jedna jednotka není sledována. Pokračujte zobrazením nesledovaného množství.

3. Vyberte pole **Nesledované množství**.

   Stránka **Nesledované prvky plánování** ukazuje, že položka 1150 používá plánovací parametr Násobek objednávky, 2,00, který určuje, že když je položka objednána, musí být v množství, které je dělitelné 2. Nejbližší číslo k 5, které je dělitelné 2, je 6.

   Stejné sledování objednávek platí pro řádky plánování pro komponenty Předního náboje, položky 1151 a 1155, kromě toho, že každá potřeba je vynásobena procentem šrotu, který je definován pro položku 1150 v poli **% odpadu** na karta zboží.

Tím se dokončí analýza původního plánu dodávek. Všimněte si, že je zaškrtnuto políčko **Přijmout hlášené akce** ve všech plánovacích řádcích, což znamená, že jsou připraveni k převodu na objednávky dodávky.

## Provádění zpráv o akcích
Poté Eduardo převede navrhované řádky plánování na dodávání objednávek pomocí funkce **Provést hlášení akce-pož.**.

### Automatické vytvoření navrhovaných objednávek dodávek

1. Zaškrtněte políčko **Přijmout hlášené akce** na všech řádcích plánování s varováním typu Výjimka.
2. Vyberte akci **Provést hlášené akce**.
3. Na stránce **Provést hlášení akce - plán.** vyplňte pole, jak je popsáno v následující tabulce.

   | Výrobní zakázka | Nákupní objednávka | Objednávka transferu |
   |----------------------|--------------------|--------------------|  
   | Pevně plánováno | Vytvořit nák. objednávky | Vytvořit objednávky  transferu |

4. Klepnutím na tlačítko **OK** automaticky vytvoříte všechny navrhované objednávky spotřebního materiálu.
5. Zavřete prázdnou stránku **Plánovací sešit**.

Tím se dokončí počáteční výpočet, analýza a vytvoření plánu dodávek poptávky v lokaci EAST v prvním únorovém týdnu. V následující části si další zákazník objedná deset turistických kol a Eduardo musí znovu nastoupit.

## Vytvoření plánovaného pohybu
Následujícího dne, před spuštěním nebo zaúčtováním jakýchkoli objednávek na dodávky, dorazí nová prodejní objednávka od společnosti Libros S.A. pro odeslání deseti turistických kol 02-12-2021. Eduardo je informován o nové poptávce a pokračuje v přeplánování, aby upravil aktuální plán dodávek. Eduardo používá funkci Vypočítat plánovaný pohyb k výpočtu pouze změn provedených v poptávce nebo nabídce od posledního běhu plánování. Kromě toho rozšiřuje plánovací období na 02-14-2021 tak, aby zahrnovalo novou prodejní poptávku na období 02-12-2014.

Systém plánování vypočítává nejlepší způsob, jak pokrýt poptávku po těchto dvou identických produktech, například konsolidovat některé nákupní a výrobní zakázky, přeplánovat další objednávky a vytvořit nové objednávky tam, kde je to nutné.

### Vytvoření nové prodejní poptávky s odpovídajícím způsobem přeplánování

1. Vyberte akci **Nový**.
2. Na stránce **Prodejní objednávka** vyplňte pole, jak je popsáno v následující tabulce.

   | Zákazník-název | Datum odeslání | Číslo zboží | Lokace | Množství |
   |----------------------------|-------------------|--------------|--------------|--------------|  
   | Libros S.A. | 02-12-2021 | 1001 | EAST | 10 |

3. Přijměte varování o dostupnosti a kliknutím na tlačítko **Ano** zaznamenejte množství poptávky.
4. Pokračujte v přeplánování a upravte aktuální plán dodávek.
5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat<"), zvolte **Plánovací sešit** a poté vyberte související odkaz.
6. Vyberte akci **Vypočítat plánovaný pohyb**.
7. Na stránce **Výpočet plánu – plán. sešit** vyplňte pole, jak je popsáno v následující tabulce.

   | Vypočítat plán | Počáteční datum | Datum ukončení | Zobrazit výsledky: | Omezit součty na |
   |--------------------|-------------------|-----------------|-------------------|---------------------|  
   | **MPS** = Ano<br /><br /> **MRP** = Ano | 01-23-2021 | 02-14-2021 | 1001..1300 | Filtr lokace = EAST |

8. Kliknutím na tlačítko **OK** zahájíte plánovací běh.

Celkem je vytvořeno 14 řádků plánování. Na prvním plánovacím řádku si všimněte, že pole **Hlášení akce** obsahuje **Nový**, pole **Množství** obsahuje 10 a pole **Datum splatnosti** obsahuje hodnotu 02-12-21. Tento nový řádek pro nejvyšší nadřazenou položku 1001, Cestovní kolo, je vytvořen proto, že položka používá zásadu přeobjednání **Zakázka** což znamená, že musí být dodána ve vztahu 1:1 k poptávce, prodejní objednávce deseti kusů.

Další dva řádky plánování jsou výrobní zakázky na cestovní kola. Každá existující objednávka pěti v poli **Původní množství** se zvýší na 15 v poli **Množství**. Obě výrobní zakázky mají nezměněné termíny splatnosti, jak je uvedeno v poli **Hlášení akce**, které obsahuje **Změna množ.** To je také případ plánovacího řádku pro položku 1300, s výjimkou její objednávky, kdy násobek 10,00 zaokrouhlí sledovanou poptávku po 15 kusech až na 20 kusů.

Všechny ostatní řádky plánování mají zprávu akce **Přeplán.  změna  množ.**. To znamená, že kromě zvýšení množství se data splatnosti přesunou ve vztahu k plánu dodávek tak, aby zahrnovala další množství do dostupného času výroby (kapacity). Nakoupené komponenty jsou přeplánovány a zvýšeny tak, aby dodávaly výrobní zakázky. Pokračujte v analýze nového plánu.

## Analýza změněného výsledku plánování
Protože všechny položky plánované na šarži ve filtru, 1100 až 1300, mají období přeplánování dva týdny, jejich stávající objednávky dodávek jsou upraveny tak, aby vyhovovaly nové poptávce, ke které dojde během zadaných dvou týdnů.

Několik řádků plánování je jednoduše vynásobeno třemi, aby bylo možné poskytnout 15 cestovních kol namísto 5, a termíny splatnosti jsou přesunuty zpět v čase, aby bylo možné poskytnout zvýšené množství do data odeslání prodejní objednávky skupině BYT-KOMPLET. U těchto řádků plánování lze sledovat všechna množství. Zbývající řádky plánování se kromě přesunu jejich termínů zvětší o deset kusů. U těchto řádků plánování je část množství nesledována z důvodu různých parametrů plánování. Pokračujte zobrazením některých z těchto položek sledování objednávek.

### Zobrazení položek sledování objednávek pro zboží 1300

1. Vyberte řádek plánování pro zboží 1250 a pak zvolte akci **Sledování zakázky**.

   Sedm řádků na stránce **Sledování zakázky** ukazuje, že pět a deset kusů je sledováno přes zadní kolo k cestovním kolům na dvou prodejních objednávkách.

   Posledních pět kusů je nesledovaných. Pokračujte v analýze.

2. Vyberte pole **Nesledované množství**.

   Stránka **Nesledované prvky plánování** ukazuje, že položka 1250 používá plánovací parametr, Objednávka více, 10,00. Proto je řádek plánování pro celkem 20 kusů, aby zaokrouhlily skutečnou potřebu až na nejbližší číslo dělitelné 10. Posledních pět kusů je nesledované množství, které uspokojí parametr plánování.

3. Zavřete všechny stránky kromě stránky **Plánovací sešit**.

### Zobrazení existující objednávky

1. V řádku plánování zboží 1250 zvolte pole **Číslo  ref.zakázky**.
2. Přejděte na stránku **Pevně plánovaná výr. zakázky** pro Zadní náboj. Otevře se stávající objednávka deseti kusů, kterou jste vytvořili při prvním plánování.
3. Zavřete pevně plánovanou výrobní zakázku.

Tím je dokončen návod, jak se plánovací systém používá k automatické detekci poptávky, výpočtu příslušných objednávek dodávek podle parametrů poptávky a plánování a následnému automatickému vytvoření různých typů objednávek dodávek s příslušnými daty a množstvími.

## Viz také
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)     
[Návod: Ruční plánování dodávek](walkthrough-planning-supplies-manually.md)     
[Detaily návrhu: Plánování dodávek](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]