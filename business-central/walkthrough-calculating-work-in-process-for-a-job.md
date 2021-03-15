---
    title: Walkthrough - Calculating Work in Process for a Job | Microsoft Docs
    description: With jobs, you can schedule the usage of your company's resources and keep track of the various costs associated with the usage of resources on a specific project. Jobs involve the consumption of employee hours, machine hours, inventory items, and other types of usage that have to be tracked as a job progresses.
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
# Návod: Výpočet nedokončené výroby projektu

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

Pomocí projektů můžete naplánovat využití zdrojů vaší společnosti a sledovat různé náklady spojené s využitím zdrojů na konkrétním projektu. Projekty zahrnují spotřebu hodin zaměstnanců, hodin strojů, inventárních položek a dalších typů využití, které je třeba sledovat při postupu projektu. Pokud projekt běží delší dobu, možná budete chtít tyto náklady převést na účet Nedokončené výroby (NV) v rozvaze, zatímco se projekt dokončuje. Pokud je to vhodné, můžete na svých účtech ve výkazu zisku a ztráty uznat náklady a tržby.

## Návod
Tento návod ilustruje následující úkoly:

- Výpočet NV.
- Výběr metody výpočtu NV.
- Vyloučení části projektu nedokončené výroby.
- Zaúčtování NV do věcných položek.
- Vratné účtování NV.

Každý krok procesu vypočítá hodnotu a přesune transakce projektu do věcných položek. Kroky výpočtu a zaúčtování jsou odděleny, aby vám pomohly zkontrolovat vaše data a provést úpravy před zaúčtováním do věcných položek. Proto byste se měli ujistit, že jsou všechny informace správné po spuštění dávkových úloh výpočtu a před spuštěním dávkových úloh účtování.

## Role
Tento návod používá jako osobu člena projektového týmu (Tricia).

## Předpoklady
Než budete moci provést úkoly v tomto návodu, musí být ve vašem počítači nainstalován [!INCLUDE[prod_short](includes/prod_short.md)].

## Příběh
Tento návod se zaměřuje na CRONUS International Ltd., projekční a poradenskou firmu, která navrhuje a upravuje nové infrastruktury, jako jsou konferenční sály a kanceláře s nábytkem, doplňky a skladovací jednotky. Většina práce v CRONUS je zaměřena na projekt a Tricia, členka projektového týmu, používá úlohy k získání přehledu o každém probíhajícím projektu, který CRONUS zahájil, a také o dokončených projektech. Některé z těchto prací mohou být velmi zdlouhavé a mohou trvat měsíce. Tricia může použít účet NV k zaznamenání nedokončené výroby a ke sledování nákladů v rámci projektu.

## Výpočet NV
CRONUS přijal zdlouhavý projekt, který se nyní rozšířil na sledovaná období. Tricia, členka projektového týmu, vypočítává nedokončenou výrobu (NV), aby se ujistila, že finanční výkaz společnosti bude přesný.

Během tohoto postupu vybere Tricia konkrétní skupinu úkolů, které budou zahrnuty do výpočtu NV. Na stránce **Řádky úlohy projektu** může tyto řádky zadat ve sloupci **Celkem NV**.

Následující tabulka popisuje tři možnosti.

| Pole | Popis |
|-------------------------------------|---------------------------------------|  
| **<blank>** | Ponechejte prázdné, pokud je úkol projektu součástí skupiny úkolů. |
| **Celkem** | Definuje rozsah nebo skupinu úkolů, které jsou zahrnuty do výpočtu NV a deaktivace. Ve skupině bude jakýkoli úkol projektu s **Typ úlohy projektu** nastavený na **Účtování** zahrnut do Celkem NV, pokud není pole **Celkem NV** nastaveno na **Kromě**. |
| **Kromě** | Platí pouze pro úkol s  **Typem úlohy projektu** **Účtování**. Úkol není zahrnut při výpočtu nedokončené výroby a deaktivaci. |

V následujícím návodu Tricia použije metodu Hodnota nákladů, její firemní standard, k výpočtu nedokončené výroby. Určuje, která část projektu bude zahrnuta do výpočtu NV přiřazením hodnot Celkem NV různým řádkům projektu.

### Výpočet NV

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi ](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Projekty** a poté vyberte související odkaz.
2. V seznamu **Projekty** vyberte projekt **Domov** a poté vyberte akci **Upravit**. Tím se karta projektu otevře v režimu úprav.

   NV lze vypočítat na základě hodnoty nákladů, hodnoty prodeje, nákladů na prodej, procenta dokončení nebo dokončené smlouvy. V tomto příkladu používá CRONUS metodu Hodnota nákladů.

3. Na záložce **Účtování** vyberte pole **Metoda NV** a poté vyberte **Hodnota nákladů**.
4. Vyberte akci **Řádky úlohy projektu** a v poli **Celkem NV** nastavte následující hodnoty.

   Následující tabulka popisuje hodnoty.

   | Číslo úlohy projektu | Pole Celkem NV |
   |------------------|----------------------|  
   | 1130 | Kromě |
   | 1190 | Celkem |
   | 1210 | Kromě |
   | 1310 | Kromě |

5. Vyberte akci **NV** a poté vyberte akci **Vypočítat NV**.
6. Na stránce **Vypočítat NV projektu** můžete vybrat projekt, pro který chcete vypočítat NV. Na záložce **Projekt** vyberte **Domov** v poli **Číslo**.
7. V poli **Zúčtovací datum** zadejte datum, který je pozdější než pracovní datum.
8. Do pole **Číslo dokladu** zadejte **1**. Tím se vytvoří dokument, na který se můžete později odvolat kvůli sledovatelnosti.
9. Zvolte tlačítko **OK** pro spuštění dávkové úlohy. Zobrazí se zpráva. Pokračujte kliknutím na tlačítko **OK**. Zavžete stránku **Řádky úlohy projektu**.

   > [!NOTE]  
   > Zpráva uvádí, že s výpočtem NV jsou spojena varování. Upozornění si projdete v dalším postupu.

10. Na karte **Projekt** rozbalte záložku **NV a deaktivace** abyste zhodnotili vypočtené hodnoty. Můžete také zobrazit **Zúčtovací datum NV** a hodnoty, které byly zaúčtovány do věcných položek, pokud existují.

Všimněte si, že hodnota pro **Uzn.  částka nákladů** je 215,60 ve sloupci **K zaúčtování**. To odráží celkové náklady dvou zboží ve skupině pracovních úkolů 1110 – 1130. Třetí zboží bylo nastaveno na **Kromě**, a proto není zahrnuto do výpočtu NV.

### Kontrola upozornění NV

1. Vyberte ikonu ![Žárovky, která otevře funkci Řeknete mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vypočítat NV projektu** a poté vyberte související odkaz.
2. Vyberte projekt **Domov** a poté vyberte akci **Zobrazit upozornění**.
3. Na stránce **Upozornění NV projektu** zkontrolujte varování spojené s projektem.

Po skončení účetního období musí Tricia přepočítat NV, aby do tohoto bodu zahrnovala dokončenou práci.

### Přepočítání NV

1. Na karte **Projekt** vyberte akci **Položky NV** a zobrazte výpočet NV.

   Stránka **Položky NV projektu** zobrazuje položky NV, které byly naposledy vypočítány pro projekt, i když NV ještě nebyl zaúčtován do věcných položek.

2. Můžete postupovat podle pokynů v postupu, který vysvětluje, jak vypočítat a přepočítat NV. Pokaždé, když se vypočítá NV, vytvoří se záznam na stránce **Položky NV projektu**.
3. Zavřete stránku.

> [!NOTE]  
> Nedokončená výroba a Deaktivace se pouze počítá. Není zaúčtováno do věcných položek. Chcete-li tak učinit, musíte po výpočtu Nedokončené výroby a Deaktivace spustit dávkovou úlohu **Zaúčtovat NV**.

## Zaúčtování NV do věcných položek
Nyní, když Tricia pro tuto práci vypočítala NV, může ji zaúčtovat do věcných položek.

### Zaúčtování NV do věcných položek

1. Ze seznamu **Projekty** vyberte projekt **Domov**.
2. Vyberte akci **NV** a poté vyberte akci **Zaúčtovat NV**.
3. Na stránce **Zaúčtovat NV projektu** na záložce **Projekt**, vyberte **Domov** v poli **Číslo**.
4. Na záložce **Možnosti** v poli **Číslo dokladu storna** vložte hodnotu **1**.
5. Kliknutím na tlačítko **OK** odešlete NV do věcných položek.
6. Kliknutím na tlačítko **OK** zavřete stránku pro potvrzení.

   Po dokončení odeslání můžete zobrazit informace o odeslání na stránce **Věcné položky NV**.

7. V seznamu **Projekty** vyberte projekt **Domov** a poté vyberte akci **Věcné položky NV**.

   Na stránce **Věcné položky NV projektu** ověřte, zda byla NV zaúčtována do věcných položek.

8. Zavřete stránku.
9. Otevřete kartu **Projektu** pro projekt **Domov**.
10. Na záložce **NV a deaktivace** si všimněte, že ve sloupci **Účtováno** je nyní pole **Uzn.  fin. částka nákladů** vyplňeno, což znamená, že NV byla úspěšně zaúčtována do věcných položek.
11. Kartu zavřete kliknutím na tlačítko **OK**.

## Vratné účtování NV
Tricia určuje, že projektoví úkoly, které byly vyloučeny z výpočtu NV, měly být vypočítány v NV. Může stornovat nesprávné účtování, aniž by musela účtovat nová účtování nedokončené výroby.

### Vratné účtování NV

1. Ze seznamu **Projekty** vyberte projekt **Domov**.
2. Vyberte akci **NV** a poté vyberte akci **Zaúčtovat NV**.
3. Na stránce **Zaúčtovat NV projektu** na záložce **Projekt**, vyberte **Domov** v poli **Číslo**.
4. Na záložce **Možnosti** v poli **Číslo dokladu storna** vložte hodnotu **1**.
5. V poli **Zúčtovací datum storna** zadejte původní zúčtovací datum. Mělo by to být stejné datum, které jste použili k prvnímu výpočtu NV.
6. Zaškrtněte políčko **Pouze stornovat**. Tím se stornuje dříve zaúčtovaná nedokončená výroba, ale do věcných položek se účtuje nová nedokončená výroba.
7. Kliknutím na tlačítko **OK** spustíte dávkovou úlohu a kliknutím na tlačítko **OK** zavřete stránku pro potvrzení.
8. Otevřete kartu **Projekt** pro **Domov**.
9. Na záložce **NV a deaktivace** ověřte, že neexistují žádné zaúčtované položky NV.
10. Zavřete tuto stránku.
11. V seznamu **Projekty** vyberte projekt **Domov**, zvolte akci **NV** a poté zvolte akci **Věcné položky NV**. U položek NV je zaškrtnuto políčko **Stornováno**.
12. Zavřete tuto stránku.
13. Pro projekt otevřete **Řádky úlohy projektu**, zahrňte části projektu, které by měly být ve výpočtu NV, a poté přepočítejte a zaúčtujte novou hodnotu do věcných položek.

   > [!NOTE]  
   > Předpokládejme, že Tricia vypočítá a zaúčtuje NV pro úlohu s nesprávnými daty. Podle metody, která byla popsána dříve, může stornovat nesprávné účtování, opravovat data a znovu zaúčtovat do věcných položek.

## Další kroky
Tento návod vás provedl kroky výpočtu NV v [!INCLUDE[prod_short](includes/prod_short.md)]. U větších úloh může být užitečné pravidelně převádět náklady na účet NV, zatímco se úloha dokončuje. Tento návod ukázal, jak vyloučit řádky úkolu z výpočtu. To také ukazuje, kdy budete muset přepočítat. A nakonec tento návod ukazuje, jak zaúčtovat NV do věcných položek. Součástí je také příklad, jak stornovat zaúčtování nedokončené výroby do věcných položek.

## Viz také
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)    
[Návod: Správa projektů pomocí úloh](walkthrough-managing-projects-with-jobs.md)     
[Metody nedokončené výroby](projects-understanding-wip.md)     
[Sledování průběhu a výkonu projektu](projects-how-monitor-progress-performance.md)    
[Práce s [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]