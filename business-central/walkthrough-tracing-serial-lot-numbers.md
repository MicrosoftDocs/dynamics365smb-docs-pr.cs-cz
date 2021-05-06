---
    title: Walkthrough - Tracing Serial-Lot Numbers | Microsoft Docs
    description: This topic describes the actions to take to stop selling a defective item.
    author: bholtorf

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 10/01/2020
    ms.author: bholtorf

---
# Návod: Sledování sériových čísel

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

Pokud se vyskytnou vady produktu, musí být chyby identifikovány a musí se zabránit tomu, aby dotčené zboží opustilo společnost. Pokud již bylo vadné zboží odesláno, musíte sledovat, kdo jej obdržel, a pokud potřebujete zboží odvolat.

Prvním úkolem řízení závad je prošetřit, odkud vadné zboží pochází a kde bylo použito. Toto šetření je založeno na historických datech a tím je usnadněno prohledávání položek sledování zboží pomocí stránky **Trasování zboží**.

Druhým úkolem správy závad je určit, zda je vysledované zboží plánováno v otevřených dokladech, jako jsou nezaúčtované prodejní objednávky nebo deníky spotřeby. Tato práce se provádí na stránce **Najít položky**. Funkci Najít položky můžete použít k prohledávání všech druhů databázových záznamů.

## Návod

Tento návod ukazuje, jak zjistit, které položky jsou vadné, který dodavatel je dodal a kde jsou používány, aby bylo možné tyto objednávky zastavit nebo stáhnout.

Tento návod ilustruje následující úkoly:

- Sledování využití k původu.
- Sledování původu k použití.
- Hledání všech aktuálních záznamů, které obsahují sledované sériové číslo / číslo šarže.

## Role

Tento návod ukazuje úkoly, které jsou prováděny následujícími uživatelskými rolemi:

- Kontrolor kvality
- Správce skladu
- Zpracovatel objednávek
- Nákupní agent

## Předpoklady

K dokončení tohoto návodu budete potřebovat:

- Společnost [!INCLUDE[prod_short](includes/prod_short.md)].
- Chcete-li vytvořit nové zboží a několik obchodních transakcí, postupujte podle [Příprava ukázkových dat](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data)..

## Příběh

Ricardo, kontrolor kvality, jedná o návratnost prodeje položky 1002, Závodní kolo. Zákazník, společnost Selangorian Ltd., si stěžoval, že rám kola je prasklý. Kontrolor kvality potvrdil, že závodní rám vráceného kola je vadný. Kontrolor kvality musí nyní určit:

- Které závodní rámy byly vadné.
- Na kterou nákupní objednávku byla chybná šarže přijata.

Z obchodního oddělení kontrolér kvality ví, že vrácené závodní kolo, položka 1002, mělo sériové číslo SN1. Pomocí těchto základních informací musí určit, kde bylo hotové závodní kolo naposledy použito, a pak ho musí vysledovat zpět k nejstaršímu původu, aby zjistil, ze kterého čísla šarže vadná součást pochází.

Výsledky tohoto prvního úkolu sledování zboží identifikují, které závodní rámy byly vadné a který dodavatel je dodal. Poté, ale ve stejném celkovém sledovacím procesu, musí kontrolor kvality najít všechna prodaná závodní kola, která obsahují závodní rámy z vadné šarže, aby bylo možné tyto objednávky zastavit nebo odvolat. A konečně, kontrolor kvality musí najít všechny otevřené dokumenty, kde se používá vadná šarže, aby se neprováděly žádné další transakce.

První dvě úlohy správy vad se provádějí na stránce **Trasování zboží**. Poslední úkol se provádí na stránce **Najít položky** v integraci se stránkou **Trasování zboží**.

## Příprava ukázkových dat

Musíte vytvořit následující nové zboží:

- 2000, Závodní rám: sledování specifické pro šarže, součást 1002
- 1002, Závodní kolo: sledování specifické pro sériové číslo

Pak musíte vytvořit různé nákupní, výrobní a prodejní transakce, které obsahují oba zboží.

### Vytvoření zboží

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat") zadejte **Zboží** a poté vyberte související odkaz.
2. Vyberte akci **Nový**.
3. Do pole **Číslo** zadejte **2000** a poté vyplňte následující pole.

   | Popis | Základní měrná jednotka | Obecná  účto  skupina zboží | DPH účto  skupina zboží | Účto skupiny zboží | Kód sledování zboží |
   |-----------|--------------------|------------------------|-----------------------|--------------------|------------------|  
   | Závodní rám | KS | SUROVINY | DPH19 | SUROVINY | DÁVKAVŠE |

   > [!NOTE]  
   > Chcete-li zadat základní měrnou jednotku, zvolte tlačítko **Nový** a poté na stránce **Měrné jednotky zboží** vyberte **KS**.

4. Všechna ostatní pole mají přijatelná výchozí data nebo nemusí být vyplněna.
5. Zvolte tlačítko **OK** a vytvořte první novou kartu položky, 2000..
6. Vyberte **Nový**.
7. Do pole **Číslo** zadejte **1002** a poté vyplňte následující pole.

   | Popis | Základní měrná jednotka | Obecná  účto  skupina zboží | DPH účto  skupina zboží | Účto skupiny zboží | Systém doplnění | Kód sledování zboží |
   |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
   | Závodní kolo | KS | OBCHOD | DPH19 | DOKONČENÉ | výr. zakázky | SČVŠE |

   > [!NOTE]  
   > Chcete-li zadat základní měrnou jednotku, zvolte tlačítko **Nový** a poté na stránce **Měrné jednotky zboží** vyberte **KS**.

   Dále definujte nastavení výroby položky.

8. Na záložce **Doplnění** zadejte do pole **Číslo TNG postupu** hodnotu **1000**.
9. Vyberte pole **Číslo výrobního kusovníku** a poté vyberte **Detaily**.
10. Na stránce **Přehled výr.kusovníků** vyberte první řádek, **1000**, a poté vyberte akci **Upravit**.
11. Na stránce **Výrobní kusovník**  změňte hodnotu v poli **Stav** na **Ve vývoji**.
12. Přejděte na prázdný řádek, zadejte **2000** v poli **Číslo** a pak zadejte **1** do pole **Množství za**.
13. Změňte hodnotu v poli **Stav** zpět na **Certifikováno**.
14. Kliknutím na tlačítko **OK** vložíte výrobní kusovník na kartu zboží a zavřete stránku **Výrobní kusovník**.

   Dále nakupte závodní rámy od Custom Metals Incorporated.

### Nákup komponent

1. Vyberte ![Žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete delat"), zadejte **Nákupní objednávky**a pak zvolte související odkaz.
2. Vyberte akci **Nový**.
3. Vytvořte nákupní objednávku pro dodavatele Custom Metals Incorporated vyplněním následujících polí v řádku.

   | Zboží | Množství | Číslo šarže |
   |----|--------|-------|  
   | 2000 | 10 | ŠARŽE1 |

4. Chcete-li zadat číslo šarže, zvolte akci **Řádky sledování zboží**.
5. Na stránce **Řádky sledování zboží** vyplňte pole **Číslo šarže** a **Množství (základ)** a poté stránku zavřete.
6. Do pole **Číslo faktury dodavatele** zadejte libovolnou hodnotu.
7. Zvolte akci **Účtovat**, vyberte možnost **Příjem a fakturace** a poté klikněte na tlačítko **OK**.

   Dále si zakupte závodní rámy od Coolwood Technologies.
8. Vyberte ![Žárovku, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete delat"), zadejte **Nákupní objednávky**a pak zvolte související odkaz.
9. Vyberte akci **Nový**.
10. Vytvořte nákupní objednávku pro dodavatele Coolwood Technologies vyplněním následujících řádkových polí.

   | Zboží | Množství | Číslo šarže |
   |----------|--------------|-------------|  
   | 2000 | 11 | ŠARŽE2 |

11. Chcete-li zadat číslo šarže, na záložce **Řádky** ve skupině **Řádek** vyberte akci **Řádky sledování zboží**.
12. Na stránce **Řádky sledování zboží** vyplňte pole **Číslo šarže** a **Množství (základ)** a poté stránku zavřete.
13. Do pole **Číslo faktury dodavatele** zadejte libovolnou hodnotu.
14. Zvolte akci **Účtovat**, vyberte možnost **Příjem a fakturace** a poté klikněte na tlačítko **OK**.

   Dále vyrobte dvě závodní kola, SN1 a SN2.

### Vytvoření koncových položek

1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vydané výr.  zakázky** a poté vyberte související odkaz.
2. Vyberte skupinu **Nový**.
3. Vytvořte novou vydanou výrobní zakázku vyplněním následujících polí.

   | Číslo původu | Množství | Sériové číslo |
   |----------|--------|----------|  
   | 1002 | 2 | SČ1 |
   | 1002 | 2 | SČ2 |

4. Zvolte akci **Aktualizace výrobní zakázky** a poté kliknutím na tlačítko **OK** vyplňte řádek.
5. Chcete-li zadat sériová čísla, vyberte akci **Řádky sledování zboží**.
6. Na stránce **Řádky sledování zboží** vyplňte pole **Sériové číslo** a **Množství (základ)** a poté stránku zavřete.

   Dále uaúčtujte spotřebu závodních rámů ze ŠARŽE1.
7. Na stránce **Vydaná výrobní zakázka** vyberte akci **Deník výroby**.
8. Na stránce **Deník výroby** vyberte řádek spotřeby pro zboží 2000 a zvolte akci **Řádky sledování zboží**.
9. Na stránce **Řádky sledování zboží** vyberte pole **Číslo šarže**, zvolte **ŠARŽE1** a pak zvolte tlačítko **OK**.
10. Všechny ostatní výchozí hodnoty ponechejte na stránce **Deník výroby** a poté vyberte akci **Účtovat**.

   Dále vyrobte další dvě závodní kola, SČ3 a SČ4.

11. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Vydané výr.  zakázky** a poté vyberte související odkaz.
12. Vyberte akci **Nový**.
13. Vytvořte novou vydanou výrobní zakázku vyplněním následujících polí v záhlaví.

   | Číslo původu | Množství | Sériové číslo |
   |----------------|--------------|----------------|  
   | 1002 | 2 | SČ3 |
   | 1002 | 2 | SČ4 |

14. Vyberte akci **Aktualizace výrobní zakázky** a vyplňte řádek.
15. Chcete-li zadat sériová čísla, vyberte akci **Řádky sledování zboží** a poté čísla na dvou řádcích v poli **Sériové číslo** na stránce **Řádky sledování zboží**.

   Dále zaúčtujte větší spotřebu závodních rámů ze ŠARŽE1.
16. Na stránce **Vydaná výrobní zakázka** vyberte akci **Deník výroby**.
17. Na stránce **Deník výroby** vyberte řádek spotřeby pro zboží 2000 a zvolte akci **Řádky sledování zboží**.
18. Na stránce **Řádky sledování zboží** vyberte pole **Číslo šarže**, zvolte **ŠARŽE1** a pak zvolte tlačítko **OK**.
19. Všechny ostatní výchozí hodnoty ponechejte na stránce **Deník výroby** a poté vyberte akci **Účtovat**.

   Vyrobili jste čtyři závodní kola, SČ1 až SČ4, a spotřebovali jste čtyři z deseti závodních rámů ze ŠARŽE1, dva rámy v každé výrobní zakázce.

20. Zavřete deník výroby a výrobní zakázky.

   Dále prodejte závodní kola. Nejprve prodejte závodní kolo se SČ1 společnosti J V v.o.s..

### Prodej koncového zboží
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
2. Vyberte akci **Nový** a poté vytvořte prodejní objednávku vyplněním následujících polí.

   | Zákazník | Zboží | Množství | Sériové číslo |
   |--------------|----------|----------|----------------|  
   | J V v.o.s. | 1002 | 1 | SČ1 |

3. Chcete-li zadat sériové číslo, vyberte akci **Řádky sledování zboží** a poté číslo v poli **Sériové číslo** na stránce **Řádky sledování zboží**.
4. Vyberte akci **Účtovat** , vyberte možnost **Dodat a fakturovat** a poté klikněte na tlačítko **OK**.

   Dále prodejte závodní kolo se SČ2 společnosti BYT-KOMPLET s.r.o..

5. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
6. Vyberte akci **Nový** a poté vytvořte prodejní objednávku vyplněním následujících polí.

   | Zákazník | Zboží | Množství | Sériové číslo |
   |--------------|----------|----------|----------------|  
   | BYT-KOMPLET s.r.o. | 1002 | 1 | SČ2 |

7. Chcete-li zadat sériové číslo, vyberte akci **Řádky sledování zboží** a poté číslo v poli **Sériové číslo** na stránce **Řádky sledování zboží**.
8. Vyberte akci **Účtovat** , vyberte možnost **Dodat a fakturovat** a poté klikněte na tlačítko **OK**.

   Nakonec prodejte některé závodní rámy samostatně. BYT-KOMPLET s.r.o. také objednává čtyři samostatné závodní rámy pro vlastní montážní linku.

9. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Prodejní objednávky** a poté zvolte související odkaz.
10. Vyberte akci **Nový** a poté vytvořte prodejní objednávku vyplněním následujících polí.

   | Zákazník | Zboží | Množství | Sériové číslo |
   |--------------|----------|----------|----------------|  
   | BYT-KOMPLET s.r.o. | 2000 | 5 | ŠARŽE1 |

11. Chcete-li zadat sériové číslo, na záložce **Řádky** ve skupině **Řádek** vyberte akci **Řádky sledování zboží** a poté číslo v poli **Sériové číslo** na stránce **Řádky sledování zboží**.

   > [!NOTE]  
   > Neúčtujte poslední prodejní objednávku pro pět závodních rámů.

   Tím je dokončena příprava dat k předvedení funkcí trasování zboží a hledání položek.

## Trasování od využití k původu
Od obchodního oddělení kontrolor kvality ví, že vrácené závodní kolo, položka 1002, má sériové číslo SČ1. Pomocí těchto základních informací může určit, kde bylo hotové závodní kolo naposledy použito, v tomto případě na prodejní zdodávce společnosti J V v.o.s. Poté musí kontrolor kvality vysledovat zboží zpět k nejstaršímu původu, aby zjistil, ze kterého čísla šarže vadný závodní rám pochází a který dodavatel ho dodal.

### Určení, která šarže obsahovala vadný rám a kdo ji dodal
1. Vyberte ikonu ![Žárovky, která otevře funkci Řekněte mi](media/ui-search/search_small.png "Řekněte mi, co chcete dělat"), zadejte **Trasování zboží** a poté vyberte související odkaz.
2. Na stránce **Trasování zboží** zadejte **SČ1** do pole **Filtr sériového  čísla** a poté do pole **Filtr zboží** zadejte **1002**.
3. Ponechte výchozí nastavení **Se sledováním zboží** v poli **Zobrazit komponenty** a ponechte výchozí metodu trasování **Použití -> Původ** v poli **Metoda sledování**.
4. Vyberte akci **Sledovat**.

   Všimněte si, že jedna hlavička prodejní dodávky odpovídá kritériím vyhledávání. Než budete pokračovat ve sledování, ověřte, zda tato dodávka je ta, která odeslala vadné závodní kolo společnosti J V v.o.s.

5. Vyberte řádek sledování a pak zvolte **Zobrazit doklad**.

   Nyní pokračujte ve sledování původu prodejní dodávky závodního kola s číslem SČ1.
6. Zvolte ikonu + na řádcích sledování a postupně sledujte zboží zpět v řetězci sledování, ze které prodejní dodávky pochází.

   Můžete sledovat následující historii transakcí:

   - Prvním zaúčtovaným dokumentem zpětně v řetězci transakcí je zaúčtování výstupu SČ1 z první vydané výrobní zakázky.
   - Dalším zaúčtovaným dokumentem zpětně poté je účtování spotřeby z první vydané výrobní zakázky. Zde kontrolér kvality vidí, že byl použit závodní rám ze ŠARŽE1.
   - Nejnižší zaúčtovaný dokument v tomto řetězci je zaúčtovaná nákupní příjemka, na které závodní rámy se ŠARŽE1 vstoupily do zásob společnosti.

   Kontrolér kvality nyní zjistil, které závodní rámy byly vadné, a může vyhledat poslední stopu, aby zjistil, který prodejce je dodal, konkrétně Custom Metals Incorporated.

   > [!NOTE]  
   > Neprovádějte žádné další úpravy výsledku sledování, protože ho použijete v další části.

   Tím je dokončena první úloha správy vad pomocí stránky **Trasování zboží**. Kontrolor kvality musí nyní určit, zda ostatní zaúčtované dokumenty zpracovávaly závodní rámy ze ŠARŽE1.

## Trasování od původu k použití
Kontrolor kvality stanovil, že vadné závodní rámy pocházejí ze ŠARŽE1. Nyní musí najít další závodní kola, která obsahují závodní rámy z vadné šarže, aby tato kola by měla být zastavena nebo stažena.

Jedním ze způsobů, jak připravit tento úkol trasování na stránce **Trasování zboží** , je ruční zadání ŠARŽE1 do pole **Filtr čísla  šarže** a hodnoty 2000 do pole **Filtr zboží**. Tento návod však bude používat funkci **Sledovat opačné – od řádku**.

### Vyhledání veškerého využití vadné šarže

1. Na stránce **Trasování zboží** vyberte řádek nákupní příjemky, poslední sledovací řádek a poté zvolte **Sledovat opačné – od řádku**.

   Výsledek trasování je nyní založen na filtrech řádku trasování pro nákupní příjemku, ŠARŽE1 a položku 2000 a výsledek je založen na trasovací metodě **Původ -> Použití**.

   Chcete-li získat přehled o veškerém využití zboží 2000 pomocí ŠARŽE1, pokračujte v rozbalování všech řádků trasování.

2. Vyberte akci **Rozbalit vše**.

   První čtyři řádky trasování odkazují na prodejní dodávku společnosti J V v.o.s., která je již vyřešena. Poslední řádek označuje, že ještě jedno závodní kolo, SČ2, bylo vyrobeno ve stejné vydané výrobní objednávce a poté prodáno a odesláno v jiné prodejní dodávce.

   Kontrolor kvality okamžitě informuje obchodní oddělení, aby mohlo zahájit stažení vadného závodního kola od zákazníka, BYT-KOMPLET s.r.o.

   Zároveň z posledních tří trasovacích řádků vidí, že na základě závodních rámů ze ŠARŽE1 byly vyrobeny další dvě položky, SČ3 a SČ4. Proto přijme opatření k zablokování těchto koncových položek v zásobách.

   Tím se dokončí druhá úloha správy závad pomocí stránky **Trasování zboží** pro správu závad. Vzhledem k tomu, že stránka **Trasování zboží** je založena pouze na zaúčtovaných položkách, musí kontrolor kvality pokračovat na stránku **Najít položky** , aby se ujistil, že ŠARŽE1 není použita v neúčtovaných dokladech.

## Vyhledání všech záznamů sériového čísla/čísla šarže
Na stránce **Trasování zboží** se kontrolor kvality dozvěděl, že ŠARŽE1 obsahuje vadné závodní rámy, které jim dodavatel dodal a ve které zaúčtované transakci byly použity. Nyní musí určit, zda je ŠARŽE1 v jakýchkoli otevřených dokumentech integrací z výsledku trasování na stránku **Najít položky**, kde může provádět vyhledávání ve všech databázových záznamech.

### Vyhledání všech výskytů ŠARŽE1 v nezaúčtovaných záznamech, například otevřených objednávkách

1. Na stránce **Trasování zboží** vyberte první sledovací řádek, potvrzení o nákupu ŠARŽE1.
2. Vyberte akci **Najít položky**.

   Stránka **Najít položky** je přednastavena pomocí vyhledávacích filtrů založených na výsledku trasování pro ŠARŽE1. Kontrolor kvality rozpozná většinu záznamů, které se týkají dokumentů již identifikovaných na stránce **Trasování zboží**. Například poslední řádek nalezených položek typu výrobní zakázka odkazuje na dvě vydané výrobní zakázky, které spotřebovaly závodní rámy ze ŠARŽE1.

   Druhý řádek nalezené položky typu **Prodejní řádek** je však nezaúčtovaný řádek dokladu, takže kontrolor kvality pokračuje v prošetřování.

3. Chcete-li otevřít záznam prodejního řádku, vyberte druhý řádek nalezených položek a zvolte akci **Zobrazit**. Případně vyberte hodnotu v poli **Počet  záznamů**.

   Zde kontrolor kvality vidí jeden otevřený prodejní řádek pro vadné závodní rámy. Okamžitě navrhuje prodejnímu oddělení, aby byla tato objednávka zrušena a byla zahájena nová výrobní zakázka založená na dobrých závodních rámech.

Tím je dokončen návod, jak používat stránku **Najít položky** pro správu závad v integraci se stránkou **Trasování zboží**.

## Viz také
[Práce se sériovými čísly a čísly šarže](inventory-how-work-item-tracking.md)    
[Sledování zboží - Sledované zboží](inventory-how-to-trace-item-tracked-items.md)    
[Nájdění položek](ui-find-entries.md)    
[Návody obchodních procesů](walkthrough-business-process-walkthroughs.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]