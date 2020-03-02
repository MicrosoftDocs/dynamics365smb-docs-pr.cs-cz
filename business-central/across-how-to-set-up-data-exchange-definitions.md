---
    title: Define how data is exchanged electronically | Microsoft Docs
    description: You can use an external provider of OCR services to have PDF or image files turned into electronic documents.
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
# Nastavení Definice výměny dat 
Můžete nastavit [!INCLUDE[d365fin](includes/d365fin_md.md)] pro výměnu dat v určitých tabulkách s daty v externích souborech, například pro odesílání a přijímání elektronických dokumentů, import a export bankovních dat nebo jiných dat, jako jsou mzdy, směnné kurzy měn a katalogy položek. Pro více informací navštivte sekci [Elektronická výměna dat](across-data-exchange.md).

Jako příprava pro vytvoření definice výměny dat pro datový soubor, nebo datový proud, můžete pomocí souvisejícího schématu XML definovat, které datové prvky mají být zahrnuty na záložce **Definice sloupců** záložce s náhledem definice sloupců. Viz krok 6 v [Popis formátování řádků a sloupců v souboru](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Pro více informací navštivte [Použití schémat XML k přípravě definic datových výměn](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

Definici výměny dat obvykle nastavíte na stránce **Definice výměny dat**. Pokud však nastavíte definici výměny dat pro službu aktualizací směnných kurzů, spustíte tento proces ve zjednodušené stránce **Nastavení  aktualizace karty sm.kurzů**.

> [!NOTE]
> Pokud je převáděný soubor ve formátu XML, měl by být termín  *„sloupec“* v tomto tématu interpretován jako *“Prvek XML obsahující data”*.

Toto téma obsahuje následující postupy:

* Vytvoření definice výměny dat
* Export definice výměny dat jako souboru XML pro použití jinými uživateli
* Import souboru XML pro existující definici výměny dat

## Vytvoření definice výměny dat
Vytvoření definice výměny dat zahrnuje dva úkoly:

1. Na stránce **Definice výměny dat** popište formátování řádků a sloupců v souboru.
2. Na stránce **Mapování výměny dat**, mapujte sloupce v datovém souboru na pole v [!INCLUDE[d365fin](includes/d365fin_md.md)].

To je popsáno v následujících postupech.

> [!TIP]
> Chcete-li zjistit, které procedury Microsoft používá ve stávajících definicích ve standartním produktu, zkontrolujte pro každou definici tři pole **Procedur** na hlavičce stránky **Mapování polí**.

#### Popsat formátování řádků a sloupců v souboru
1. Do pole **Hledat**, zadejte **Definice výměny dat** a poté vyberte související odkaz.
2. Zvolte akci **Nový**.
3. Na záložce **Obecné**, popište definici výměny dat a typ datového souboru vyplněním polí, jak je popsáno v následující tabulce.

   | Pole | Definice |
   |---------------------------------|---------------------------------------|  
   | **Kód** | Zadejte kód pro identifikaci definice výměny dat. |
   | **Název** | Zadejte název pro definici výměny dat. |
   | **Typ souboru** | Určete, pro jaký typ souboru se používá definice výměny dat. Můžete vybrat mezi čtyřmi typy souborů:<br /><br /> -   **XML**: Vrstvené řetězce obsahu a označení obklopené značkami označujícími funkci.<br />-   **Variable Text**: Záznamy mají proměnnou délku a jsou odděleny znakem, například čárkou, dvojtečkou, nebo středníkem. Známý taky jako *soubor s oddělovači*.<br />-   **Fixed Text**: Záznamy mají stejnou délku, používají vyplňovací znaky a každý záznam je na samostatném řádku Také známý jako *soubor s pevnou šířkou*.<br />- **Json**: Vrstvené řetězce obsahu v JavaScriptu. |
   | **Typ** | Určuje, jaký typ obchodní činnosti se používá pro definici výměny dat, například **Export platby**. |
   | **Procedura zpracování dat** | Zadejte proceduru, která přenáší data do a z tabulek v [!INCLUDE[d365fin](includes/d365fin_md.md)]. |
   | **Procedura validace** | Zadejte proceduru, která je použitá k ověření dat podle předem definovaných obchodních pravidel. |
   | **Procedura čtení/zápisu** | Určuje proceduru, která zpracovává importovaná data před mapováním a exportovaná data po mapování. |
   | **XMLPort čtení/zápisu** | Určuje XMLport, skrz který importované soubory nebo služby vkládají předešlé mapování a skrz který exportovaná data odchází, když jsou zapisována do souboru nebo služby po mapování. |
   | **Procedura  ext. zpracování dat** | Určuje proceduru, která přenáší externí data dovnitř a ven z rámce výměny dat. |
   | **Procedura zpětné vazby uživatelů** | Určuje proceduru, která dělá různé vyčištění po mapování, jako je označení řádků jako exportovaných a mazání dočasných záznamů. |
   | **Kódování souboru** | Určuje kódování souboru. **Poznámka:**  Toto pole je aktuální pouze pro import. |
   | **Oddělovač sloupců** | Určuje, jak jsou sloupce v datovém souboru oddělené, pokud je soubor typu **Variable Text**. |
   | **Řádky hlavičky** | Určuje kolik řádků hlavičky existuje v souboru.<br /><br /> To zajišťuje, že data hlavičky nejsou importována. **Poznámka:** Toto pole je relevantní pouze pro import. |
   | **Značka hlavičky** | Pokud řádek hlavičky existuje na několika pozicích v souboru, otevřete text prvního řádku na řádku hlavičky.<br /><br /> Tím je zajištěno, že data záhlaví nejsou importována. **Poznámka:** Toto pole je relevantní pouze pro import. |
   | **Značka patičky** | Pokud řádek zápatí existuje na několika pozicích v souboru, vložte text prvního sloupce do řádku zápatí.<br /><br /> Tím je zajištěno, že data zápatí nejsou importována. **Poznámka:** Toto pole je relevantní pouze pro import. |

4. Na záložce **Definice řádků**, popište formátování řádků v datovém souboru vyplněním polí, tak jak jsou popsány v následující tabulce.

   > [!NOTE]
   > Pro import bankovních výpisů vytvoříte pouze jeden řádek pro jediný formát souboru bankovních výpisů, který chcete importovat.
   > Pro export plateb můžete každému typu platby, který chcete exportovat, vytvořit řádek. V takovém případě záložka **Definice sloupce** zobrazuje různé sloupce pro každý druh platby.
   > 
   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Kód** | Zadejte kód pro identifikaci řádku v souboru. |
   | **Název** | Zadejte název, který popisuje řádek v souboru. |
   | **Počet sloupců** | Určuje, kolik sloupců má řádek v souboru bankovního výpisu. **Poznámka:**  Toto pole je aktuální pouze pro import. |
   | **Značka řádku dat** | Určuje, pozici prvku v souvisejícím schématu XLM, který představuje hlavní položku datového souboru. **Poznámka:**  Toto pole je aktuální pouze pro import. |
   | **Obor názvů** | Určuje, obor názvů, který je v souboru očekáván, pro umožnění ověření oboru názvů. Toto pole můžete nechat prázdné, pokud nechcete povolit ověření oboru názvů. |

5. Opakujte krok 4 a vytvořte řádek pro každý typ dat souboru, který chcete exportovat.

   Pokračujte v popisu formátování sloupců v datovém souboru vyplněním polí na záložce **Definice sloupce**, jak je popsáno v následující tabulce. Můžete použít soubor struktury, jako například soubor .XSD, aby datový soubor předvyplňoval kartu s náhledem příslušnými prvky. Pro více informací navštivte [Použití schémat XML k přípravě definic datových výměn](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. Na záložce **Definice sloupce**, vyberte **Získat strukturu souboru**.
7. Na stránce **Získat strukturu souboru**, vyberte související soubor struktury a poté zvolte tlačítko **OK**. Řádky na záložce **Definice sloupce** jsou vyplněny podle struktury datového souboru.
8. Na záložce **Definice sloupce**, upravte nebo vyplňte pole, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Číslo sloupce** | Zadejte číslo, které odráží pozici sloupce na řádku v souboru. <br /><br /> U souborů XML zadejte číslo, které odráží typ prvku v souboru, který data obsahuje. |
   | **Název** | Zadejte název sloupce. <br /> <br /> U souborů XML zadejte značky, které označují data, která mají být vyměněna. |
   | **Datový typ** | Určete, zda jsou data, která mají být vyměněna, typu **Text**, **Date**, nebo **Decimal**. |
   | **Formát dat** | Určete formát dat, pokud existují. Například, **MM-dd-yyyy** pokud je datový typ **Datum**. **Poznámka:** Pro export zadejte formát dat podle [!INCLUDE[d365fin](includes/d365fin_md.md)]. Pro import zadejte formát dat podle rozhraní .NET Framework. Více informací viz [Řetězce standardního formátu data a času](https://go.microsoft.com/fwlink/?LinkID=323466). |
   | **Jazyková verze formátování dat** | Zadejte jazykovou verzi datového formátu, pokud existuje. Například, **en-US** pokud je datový typ **Decimal**, abyste se ujistili, že je čárka používána jako oddělovač .000 podle formátu USA. Více informací viz [Řetězce standardního formátu data a času](https://go.microsoft.com/fwlink/?LinkID=323466). **Poznámka:** Toto pole je relevantní pouze pro import. |
   | **Délka** | Určete délku řádku o pevné šířce, který obsahuje sloupec, jestli je soubor typu **Fixed Text**. |
   | **Popis** | Zadejte popis sloupce s informacemi. |
   | **Cesta** | Určete pozici elementu v souvisejícím XML schématu. |
   | **Identifikátor záporného znaménka** | Zadejte hodnotu, která se používá v datovém souboru k identifikaci záporných částek do datových souborů, které nemohou obsahovat záporné znaménka. Tento identifikátor je potom použit ke znegování hodnot během importu. **Poznámka:**  Toto pole je aktuální pouze pro import. |
   | **Konstanta** | Určete jakákoliv data, které chcete exportovat do tohoto sloupce, jako jsou extra informace o typu platby. **Poznámka:** Toto pole je relevantní pouze pro export. |

9. Opakujte krok 8 pro každý sloupec nebo prvek XML v datovém souboru, který obsahuje data, která chcete vyměnit, s [!INCLUDE[d365fin](includes/d365fin_md.md)].

Dalším krokem při vytváření definice výměny dat je rozhodnout, které sloupce nebo elementy XML v datovém souboru mapovat, na jaká pole v [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
Konkrétní mapování závisí na obchodním účelu datového souboru, který má být vyměněn, a na místních variacích. I bankovní standard SEPA má místní variace. [!INCLUDE[d365fin](includes/d365fin_md.md)] podporuje import předpřipravených souborů bankovních výpisů SEPA CAMT. To je reprezentováno kódem záznamu definice výměny dat **SEPA CAMT** na stránce **Definice výměny dat**. Pro více informací o konkrétním mapování polí podporovaného SEPA CAMT, viz [Mapování polí při importu souborů SEPA CAMT](across-field-mapping-when-importing-sepa-camt-files.md).

#### Mapování sloupců v datovém souboru na pole v [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Na záložce **Definice řádků** vyberte řádek, pro který chcete mapovat sloupce na pole, a pak zvolte **Mapování polí**. Otevře se stránka **Mapování výměny dat**.
2. Na záložce **Obecné**, určete nastavené mapování vyplněním polí, jak je popsáno v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **ID tabulky** | Určuje tabulku, která drží pole do nebo z kterých jsou data vyměněna podle mapování. |
   | **Použít jako přechodnou tabulku** | Určuje, že tabulka, kterou jste vybrali v poli **ID tabulky**  je přechodná tabulka, kde importovaná data jsou uchovávána předtím, než jsou nahrána do cílové tabulky. <br /> <br /> Obvykle používáte přechodná tabulku, když se definice výměny dat používá k importu a převodu elektronických dokladů, například faktur dodavatelů na nákupní faktury v [!INCLUDE[d365fin](includes/d365fin_md.md)]. Více informací viz [Elektronická výměna dat](across-data-exchange.md). |
   | **Název** | Zadejte název pro nastavení mapování. |
   | **Procedura předzpracování mapování** | Určuje proceduru, která připraví mapování mezi poli v [!INCLUDE[d365fin](includes/d365fin_md.md)] a externími daty. |
   | **Procedura mapování** | Určuje proceduru, která je použita k mapování specifických sloupců nebo prvků dat XML k polím v [!INCLUDE[d365fin](includes/d365fin_md.md)]. |
   | **Procedura násl.zpracování mapování** | Určuje proceduru, která provede mapování mezi poli v [!INCLUDE[d365fin](includes/d365fin_md.md)] a externími daty. **Poznámka:**  Při používání funkcionality Bank Data Conversion Service, převádí procedura exportovaná data z [!INCLUDE[d365fin](includes/d365fin_md.md)] do obecného formátu, který je připraven k exportu. V případě importu převede kódová jednotka externí data do formátu, který je připraven k importu, do [! INCLUDE[d365fin](includes/d365fin_md.md)]. |

3. Na záložce **Mapování polí**, určete, které sloupce mapují na která pole v části [!INCLUDE[d365fin](includes/d365fin_md.md)] vyplněním polí popsaných v následující tabulce.

   | Pole | Popis |
   |---------------------------------|---------------------------------------|  
   | **Číslo sloupce** | Určuje, pro který sloupec v datovém souboru chcete definovat mapu. <br /><br /> Můžete vybrat pouze sloupce, které jsou reprezentovány řádky na záložce**Definice sloupců** na **Definice výměny dat**. |
   | **ID pole** | Určuje, na které pole se sloupec mapuje v poli **Číslo sloupce**. <br /> <br /> Můžete vybrat pouze z polí, která existují v tabulce, kterou jste zadali v poli **Tabulka** na záložce **Obecné**. |
   | **Volitelné** | Určuje, že mapování bude přeskočeno, pokud je pole prázdné. **Poznámka:** Pokud toto políčko nezaškrtnete, dojde k chybě při exportu, pokud bude pole prázdné. **Poznámka:** Toto pole je relevantní pouze pro export. |
   | **ID cílové tabulky** | Viditelné pouze tehdy, když je zaškrtnuto políčko **Použít jako převodní tabulku**. <br /><br /> Určuje tabulku, z níž bude mapována hodnota v poli **Titulek sloupce**, když pro import dat používáte přechodnou tabulku. |
   | **Titulek cílové tabulky** | Viditelné pouze v případě, že je zaškrtnuto políčko **Použít jako převodní tabulku**. <br /><br /> Určete název tabulky na poli **ID cílové tabulky**, což je tabulka, na kterou je mapována hodnota na poli **Titulek sloupce**, pokud používáte převodní tabulku pro import dat. |
   | **ID cílového pole** | Viditelné, pouze pokud je zaškrtnuto políčko **Použít jako převodní tabulku**.<br /><br /> Zadejte pole v cílové tabulce, na které je mapována hodnota v poli **Titulek sloupce**, pokud pro import dat používáte přechodnou tabulku. |
   | **Titulek cílového pole** | Viditelné, pouze pokud je zaškrtnuto políčko **Použít jako převodní tabulku**. <br /><br />Zadejte název pole v cílové tabulce, na které je mapována hodnota v poli **Titulek sloupce**, pokud pro import dat používáte přechodnou tabulku. |
   | **Volitelné** | Viditelné pouze tehdy, když je zaškrtnuto políčko **Použít jako přechodnou tabulku**. <br /><br /> Určete, zda má být mapování přeskočeno, pokud je pole prázdné. Pokud toto políčko nezaškrtnete, dojde k chybě při exportu, pokud bude pole prázdné. |

Definice výměny dat je nyní připravena k povolení pro uživatele. Další informace naleznete v části [Nastavení odesílání a přijímání elektronického dokladu](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Nastavení převodu SEPA](finance-how-to-set-up-sepa-credit-transfer.md), [Nastavení SEPA – příkaz k inkasu](finance-how-to-set-up-sepa-direct-debit.md), a [Provádění plateb pomocí služby převodu bankovních dat nebo převodem na SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

Pokud jste vytvořili definici výměny dat pro konkrétní datový soubor, můžete exportovat definici výměny dat jako soubor XML, který lze použít k rychlému povolení importu daného datového souboru. To je popsáno v následujícím postupu.

### Export definice výměny dat jako souboru XML pro použití jinými uživateli
1. Do pole **Hledat**, zadejte **Definice výměny dat** a poté vyberte související odkaz.
2. Vyberte definici výměny dat, kterou chcete exportovat.
3. Vyberte akci **Export definice výměny dat**.
4. Uložte soubor XML, který představuje definici výměny dat, do příslušného umístění.

   Pokud již byla vytvořena definice pro výměnu dat, stačí importovat soubor XML do rámce výměny dat. To je popsáno v následujícím postupu.

### Chcete-li importovat existující definici výměny dat
1. Uložte soubor XML, který představuje definici výměny dat, do příslušného umístění.
2. Do pole **Hledat**, zadejte **Definice výměny dat** a poté vyberte související odkaz.
3. Zvolte akci **Nový**. Otevře se stránka **Definice výměny dat**.
4. Vyberte akci **Import definice výměny dat**.
5. Vyberte soubor, který jste uložili v kroku 1.

## Viz také
[Nastavení výměny dat](across-set-up-data-exchange.md)  
[Nastavení odesílání a přijímání elektronického dokladu](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Nastavení převodu SEPA](finance-how-to-set-up-sepa-credit-transfer.md)  
[Nastavení SEPA – příkaz k inkasu](finance-how-to-set-up-sepa-direct-debit.md)  
[Provádění plateb pomocí služby převodu bankovních dat nebo převodem na SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Došlé doklady](across-income-documents.md)  
[Obecné obchodní funkcionality](ui-across-business-areas.md)
